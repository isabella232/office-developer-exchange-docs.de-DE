---
title: Verwalten von Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 1bda4094-88c3-4f61-9219-6ee70f6e81cf
description: Informieren Sie sich über die Beibehaltung der Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver.
localization_priority: Priority
ms.openlocfilehash: 1618216cf69e08b2ae774264e0910856a59851af
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455757"
---
# <a name="maintain-affinity-between-a-group-of-subscriptions-and-the-mailbox-server-in-exchange"></a>Verwalten von Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver in Exchange

Informieren Sie sich über die Beibehaltung der Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver.
  
Affinität ist die Zuordnung einer Sequenz von Anforderungs-und Antwortnachrichten mit einem bestimmten Postfachserver. Für die meisten Funktionen in Exchange wird die Affinität vom Server verarbeitet. Benachrichtigungen sind jedoch eine Ausnahme. Der Client ist für die Beibehaltung der Affinität mit dem Postfachserver für Benachrichtigungsabonnements verantwortlich. Diese Affinität ermöglicht es dem Lastenausgleich und den Clientzugriffsservern zwischen dem Client und dem Server, Benachrichtigungsabonnements und zugehörige Anforderungen an den Postfachserver weiterzuleiten, der das Abonnement verwaltet. Ohne Affinität wird die Anforderung möglicherweise an einen anderen Postfachserver weitergeleitet, der nicht die Abonnements des Clients enthält, was dazu führen kann, dass ein [ErrorSubscriptionNotFound](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Fehler zurückgegeben wird. 
  
## <a name="how-is-affinity-maintained"></a>Wie wird Affinität beibehalten?
<a name="bk_howmaintained"> </a>

Affinität in Exchange ist Cookie-basiert. Der Client löst die Erstellung des Cookies durch einschließen bestimmter Kopfzeilen in der Abonnementanforderung aus, und die Abonnement Antwort enthält dann das Cookie. Der Client sendet dann dieses Cookie in nachfolgenden Anforderungen, um sicherzustellen, dass die Anforderung an den richtigen Postfachserver weitergeleitet wird.
  
Konkret wird Affinität in Exchange wie folgt behandelt: 
  
- X-AnchorMailbox – ein HTTP-Header, der in der anfänglichen Abonnementanforderung enthalten ist. Er identifiziert das erste Postfach in einer Gruppe von Postfächern, die die Affinität mit dem gleichen Postfachserver gemeinsam nutzen.
    
- X-PreferServerAffinity – ein HTTP-Header, der in der anfänglichen Abonnementanforderung mit dem x-AnchorMailbox-Header enthalten ist und auf true festgelegt ist, um anzugeben, dass der Client die Beibehaltung der Affinität mit dem Postfachserver beantragt.
    
- X-BackEndOverrideCookie – ein Cookie, das in der anfänglichen Abonnement Antwort enthalten ist und ein Cookie enthält, mit dem der Lastenausgleich und der Client Zugriffsserver nachfolgende Anforderungen an denselben Postfachserver weiterleiten.
    
## <a name="how-do-i-maintain-affinity-by-using-the-ews-managed-api-or-ews"></a>Wie kann ich die Affinität mit dem verwaltete EWS-API oder EWS beibehalten?
<a name="bk_howdoimaintain"> </a>

Sie können die gleichen Schritte verwenden, um die Affinität für mehrere Post Fach Abonnements und deren Postfachserver beizubehalten, unabhängig davon, ob Sie Streaming-, Pull-oder Push-Benachrichtigungen verwenden, und unabhängig davon, ob Sie auf einen lokalen Exchange-Server oder auf Exchange Online ausgerichtet sind.
  
1. Rufen Sie für jedes Postfach die [AutoErmittlung](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) auf, und rufen Sie die Benutzereinstellungen GroupingInformation und ExternalEwsUrl ab. Für die SOAP-AutoErmittlung verwenden Sie das [Setting](https://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) -Element, und für POX AutoErmittlung verwenden Sie das [GroupingInformation](https://msdn.microsoft.com/library/2d8a007f-d79c-43c8-90e3-2c6d883f3a7c%28Office.15%29.aspx) -Element. 
    
2. Platzieren Sie mithilfe der GroupingInformation-und ExternalEwsUrl-Einstellungen aus den Antworten der AutoErmittlung Postfächer mit dem gleichen ExternalEwsUrl-und GroupingInformation-verketteten Wert in derselben Gruppe. Wenn Gruppen über mehr als 200 Postfächer verfügen, unterbrechen Sie die Gruppen weiter, sodass jede Gruppe nicht mehr als 200 Postfächer aufweist.
    
3. Erstellen Sie und verwenden Sie ein [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=EXCHG.80%29.aspx) -Objekt für den Rest der Prozedur. Wenn Sie dasselbe **Datei "ExchangeService** -Objekt verwenden, werden Cookies und Kopfzeilen (wenn Sie festgelegt sind) automatisch verwaltet. Beachten Sie, dass Sie, wenn Sie nicht beabsichtigen, Streaming-Abonnements in einer einzelnen Verbindung zu gruppieren, ein anderes **Datei "ExchangeService** -Objekt für jeden imitierten Benutzer erstellen können. 
    
4. [Senden Sie eine Abonnement](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) Anforderung für den Benutzer, dessen Benutzername zuerst angezeigt wird, wenn alle Benutzer in der Gruppe alphabetisch sortiert sind (dieser Benutzer wird als Anker Postfachbenutzer bezeichnet). Gehen Sie wie folgt vor: 
    
  - Fügen Sie den X-AnchorMailbox-Header mit einem Wert ein, der auf die SMTP-Adresse des Anker Postfachbenutzers festgelegt ist.
    
  - Fügen Sie den X-PreferServerAffinity-Header hinzu, wobei der Wert auf true festgelegt ist.
    
  - Verwenden Sie die [ApplicationImpersonation](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx) -Rolle (der [ExchangeImpersonation](https://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) -Typ). 
    
5. Rufen Sie in der Abonnement Antwort den X-BackEndOverrideCookie-Wert ab. Fügen Sie diesen Wert in jede der nachfolgenden Abonnementanforderungen für Benutzer in dieser Gruppe ein.
    
6. Senden Sie für jeden weiteren Benutzer in der Gruppe eine Abonnementanforderung, und führen Sie die folgenden Schritte aus:
    
  - Fügen Sie den X-AnchorMailbox-Header mit einem Wert ein, der auf die SMTP-Adresse des Anker Postfachbenutzers für die Gruppe festgelegt ist.
    
  - Fügen Sie den X-PreferServerAffinity-Header hinzu, wobei der Wert auf true festgelegt ist.
    
  - Schließen Sie die X-BackEndOverrideCookie ein, die in der Abonnement Antwort des Anchor-Postfachbenutzers zurückgegeben wurde.
    
  - Verwenden Sie die [ApplicationImpersonation](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx) -Rolle (der [ExchangeImpersonation](https://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) -Typ). 
    
    Beachten Sie, dass der Server die Werte x-PreferServerAffinity und x-BackendOverrideCookie zusammen verwendet, um das Routing an den Postfachserver durchzuführen. Der X-AnchorMailbox-Header ist ebenfalls erforderlich, wird vom Server jedoch ignoriert, wenn die beiden anderen Werte gültig sind. Wenn sich x-AnchorMailbox und x-PreferServerAffinity in einer Anforderung befinden und x-BackendOverrideCookie nicht enthalten ist, wird der x-AnchorMailbox-Wert verwendet, um die Anforderungen weiterzuleiten.
    
    Da die x-PreferServerAffinity-und x-BackendOverrideCookie-Werte das Routing durchführen, ändert sich die Logik nicht, wenn das Anker Postfach jemals auf eine andere Gruppe oder einen anderen Server verschoben wird, da die x-BackendOverrideCookie die Anforderung an den richtigen Server für die Gruppe weiterleitet.
    
7. Senden Sie eine einzelne [GetStreamingEvents](https://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) -oder [GetEvents](https://msdn.microsoft.com/library/22d4da6b-d8a8-484f-82c4-3e4b8f5431cd%28Office.15%29.aspx) -Anforderung für die Gruppe, und führen Sie die folgenden Schritte aus: 
    
  - Fügen Sie die in jeder einzelnen Abonnement Antwort für Postfächer in der Gruppe zurückgegebenen [Subscription](https://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) -Wert-Werte ein. 
    
  - Wenn mehr als 200 Abonnements für die Gruppe vorhanden sind, erstellen Sie mehrere Anforderungen. Die maximale Anzahl von [Subskriptions](https://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) -ID-Werten, die in eine Anforderung eingeschlossen werden sollen, lautet 200. 
    
  - Wenn Sie mehr Verbindungen benötigen, als für das Zielpostfach zur Verfügung stehen, verwenden Sie das Dienstkonto, um die Identität des Anker Postfachs für die Gruppe zu imitieren. Verwenden Sie andernfalls keinen Identitätswechsel. Idealerweise möchten Sie die Identität eines eindeutigen Postfachs pro [GetStreamingEvents](https://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) -oder [GetEvents](https://msdn.microsoft.com/library/22d4da6b-d8a8-484f-82c4-3e4b8f5431cd%28Office.15%29.aspx) -Anforderung annehmen, damit keine Einschränkungs Grenzwerte auftreten. 
    
  - Verwenden Sie ApplicationImpersonation, wenn Sie [mehr Verbindungen benötigen, als für das Zielpostfach verfügbar sind](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling). Verwenden Sie andernfalls nicht ApplicationImpersonation.
    
  - Fügen Sie den X-PreferServerAffinity-Header hinzu, und legen Sie ihn auf true fest. Dieser Wert wird automatisch einbezogen, wenn Sie das **Datei "ExchangeService** -Objekt verwenden, das Sie in Schritt 2 erstellt haben. 
    
  - Schließen Sie die x-BackEndOverrideCookie für die Gruppe ein (die x-BackEndOverrideCookie, die in der Abonnement Antwort des Anchor-Postfachbenutzers zurückgegeben wurde). Dieser Wert wird automatisch einbezogen, wenn Sie das **Datei "ExchangeService** -Objekt verwenden, das Sie in Schritt 2 erstellt haben. 
    
8. Übergeben Sie die zurückgegebenen Ereignisse zur Verarbeitung an einen separaten Thread.
    
## <a name="what-throttling-values-do-i-need-to-take-into-consideration"></a>Welche Drosselungswerte muss ich berücksichtigen?
<a name="bk_throttling"> </a>

Während Sie Ihre Benachrichtigungs Implementierung planen, sollten Sie zwei Werte berücksichtigen: die Anzahl der Verbindungen und die Anzahl der Abonnements. In der folgenden Tabelle sind die Standardwerte für jede [Einschränkungs](ews-throttling-in-exchange.md) Einstellung und die Verwendung der Einstellungen aufgeführt. Für jeden Wert wird das Budget dem Zielpostfach zugewiesen. Aus diesem Grund ist die Verwendung eines Identitätswechsels zur Gewinnung zusätzlicher Verbindungen ein erforderlicher Schritt in vielen Szenarien. 
  
**Tabelle 1. Standardmäßige Drosselungswerte**

|**Beachtung des Bereichs**|**Einschränkungseinstellung**|**Standardwert**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
|Streaming-Verbindungen  <br/> |Grenzwert für die standardmäßige hängende Verbindung  <br/> |10 für Exchange Online  <br/> 3 für Exchange 2013  <br/> |Die maximale Anzahl gleichzeitiger Streaming-Verbindungen, die ein Konto auf dem Server gleichzeitig geöffnet haben kann. Wenn Sie innerhalb dieses Grenzwerts arbeiten möchten, verwenden Sie ein Dienstkonto mit der ApplicationImpersonation-Rolle, die für die Zielpostfächer zugewiesen ist, und imitieren Sie den ersten Benutzer in jeder Abonnement-ID-Gruppe, wenn Sie Streaming-Ereignisse erhalten.  <br/> |
|Pull-oder Push-Verbindungen  <br/> |EWSMaxConcurrency  <br/> |27  <br/> |Die maximale Anzahl gleichzeitiger Pull-oder Push-Verbindungen (Anforderungen, die empfangen wurden, aber noch nicht beantwortet wurden), die ein Konto auf dem Server gleichzeitig öffnen kann.  <br/> |
|Abonnements  <br/> |EWSMaxSubscriptions  <br/> |20 für Exchange Online  <br/> 5000 für Exchange 2013  <br/> |Die maximale Anzahl von nicht abgelaufenen Abonnements, die ein Konto auf einmal haben kann. Dieser Wert wird dekrementiert, wenn das Abonnement auf dem Server erstellt wird.  <br/> |
   
Im folgenden Beispiel wird gezeigt, wie die Budgets zwischen einem beliebigen Zielpostfach und dem Dienstkonto verarbeitet werden, dem die [ApplicationImpersonation](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx) -Rolle für die Zielpostfächer zugewiesen ist. 
  
- Dienstkonto1 (SA1) imitiert viele Benutzer (M1, m2, M3 usw.) und erstellt Abonnements für jedes Postfach. Beachten Sie Folgendes: Wenn die Abonnements erstellt werden, ist der Abonnementbesitzer SA1, wenn SA1 also eine Verbindung mit den Abonnements öffnet, erzwingt EWS, dass die Abonnements Eigentum von SA1 sind.
    
- Sa1 kann die Verbindung wie folgt öffnen:
    
1. Ohne Identitätswechsel, sodass die Verbindung mit SA1 aufgeladen wird.
    
2. Durch die Identität eines beliebigen Benutzers, beispielsweise M1, damit die Verbindung mit einer Kopie des m1's-Budgets belastet wird. (M1 selbst kann zehn Verbindungen mit Exchange Online öffnen, und alle Dienstkonten, die die Identität M1 annehmen, können zehn Verbindungen mit dem kopierten Budget öffnen.)
    
- Wenn der Verbindungsgrenzwert erreicht ist, stehen die folgenden Problemumgehungen zur Verfügung:
    
  - Wenn Option 1 verwendet wird, kann der Administrator mehrere Dienstkonten erstellen, um die Identität weiterer Benutzer zu imitieren.
    
  - Wenn Option 2 verwendet wird, kann der Code die Identität eines anderen Benutzers annehmen-beispielsweise m2.
    
## <a name="example-maintaining-affinity-between-a-group-of-subscriptions-and-the-mailbox-server"></a>Beispiel: beibehalten der Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver
<a name="bk_ce"> </a>

Okay, lassen Sie es uns in Aktion sehen. Im folgenden Codebeispiel wird veranschaulicht, wie Sie Benutzer gruppieren und die x-AnchorMailbox-und x-PreferServerAffinity-Header und das x-BackendOverrideCookie-Cookie verwenden, um die Affinität mit dem Postfachserver beizubehalten. Da die Header und das Cookie im Affinitäts Text von größter Wichtigkeit sind, konzentriert sich dieses Beispiel auf die EWS-XML-Anforderungen und-Antworten. Informationen zum Erstellen des Textkörpers der Abonnementanforderungen und-Antworten mithilfe der verwaltete EWS-API finden Sie unter [Stream notifications about Mailbox Events by using EWS in Exchange](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md) and [Pull notifications about Mailbox Events by using EWS in Exchange](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md). Dieser Abschnitt enthält zusätzliche Schritte für die Beibehaltung der Affinität und das Hinzufügen der Kopfzeilen zu Ihren Anforderungen.
  
Dieses Beispiel besteht aus vier Benutzern: Alfred@contoso.com, Alisa@contoso.com, Ronnie@contoso.com und Sadie@contoso.com. In der folgenden Abbildung sind die GroupingInformation-und ExternalEwsUrl- [AutoErmittlungseinstellungen](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) für die Benutzer dargestellt. 
  
**Abbildung 1. Zum Gruppieren von Postfächern verwendete AutoErmittlungseinstellungen**

![Tabelle mit den Werten "GroupingInformation" und "ExternalEwsUrl" für jeden Benutzer.](media/Exchange2013_NotificationAffinityAutoDResults.png)
  
Mithilfe der Einstellungen der Auto Ermittlungs Antworten werden die Postfächer nach dem verketteten Wert der GroupingInformation-und ExternalEwsUrl-Einstellungen gruppiert. In diesem Beispiel haben Alfred und Sadie die gleichen Werte, also sind Sie in einer Gruppe, und Alisa und Ronnie teilen die gleichen Werte, sodass Sie sich in einer anderen Gruppe befinden.
  
**Abbildung 2. Erstellen von Post Fachgruppen**

![Tabelle, die zeigt, wie Postfachgruppen mithilfe von AutoErmittlungseinstellungen erstellt werden.](media/Exchange2013_NotificationAffinityGrouping.png)
  
Im Rahmen dieses Beispiels konzentrieren wir uns auf Gruppe A. Wir würden die gleichen Schritte für Gruppe B verwenden, verwenden jedoch einen anderen X-AnchorMailbox-Wert für diese Gruppe.
  
Erstellen Sie mithilfe von [ApplicationImpersonation](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx)die Abonnementanforderung für das Anker Postfach (Alfred@contoso.com), wobei der x-AnchorMailbox-Header auf die e-Mail-Adresse und den x-PreferServerAffinity-Headerwert true festgelegt ist. Durch Festlegen dieser beiden Headerwerte wird der Server ausgelöst, um eine X-BackEndOverrideCookie für die Antwort zu erstellen.
  
Wenn Sie die verwaltete EWS-API verwenden, fügen Sie die beiden Kopfzeilen mithilfe der [httpheaders-](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice_members%28v=exchg.80%29.aspx)-[Add](https://msdn.microsoft.com/library/cy7xta5e) -Methode wie dargestellt zu ihrer Abonnementanforderung hinzu. 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", Mailbox.SMTPAddress);
service.HttpHeaders.Add("X-PreferServerAffinity", "true");
```

Alfreds Abonnement-Anforderung sieht also so aus.
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
Accept: text/xml
User-Agent: ExchangeServicesClient/15.00.0516.014
X-AnchorMailbox: alfred@contoso.com
X-PreferServerAffinity: true
Host: outlook.office365.com
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
    <t:ExchangeImpersonation>
      <t:ConnectingSID>
        <t:SmtpAddress>alfred@contoso.com</t:SmtpAddress>
      </t:ConnectingSID>
    </t:ExchangeImpersonation>
  </soap:Header>
  <soap:Body>
    <m:Subscribe>
      <m:StreamingSubscriptionRequest>
        <t:FolderIds>
          <t:DistinguishedFolderId Id="inbox" />
        </t:FolderIds>
        <t:EventTypes>
          <t:EventType>NewMailEvent</t:EventType>
        </t:EventTypes>
      </m:StreamingSubscriptionRequest>
    </m:Subscribe>
  </soap:Body>
</soap:Envelope>
```

Die folgende XML-Nachricht ist die Antwort auf die Abonnementanforderung von Alfred und enthält die X-BackEndOverrideCookie. Senden Sie dieses Cookie erneut für alle nachfolgenden Anforderungen für Benutzer in dieser Gruppe. Beachten Sie, dass die Antwort auch zusätzliche Cookies enthält, beispielsweise das von Exchange 2010 verwendete exchangecookie-Cookie. Exchange Online, Exchange Online im Rahmen von Office 365 und Exchange-Versionen, die mit Exchange 2013 beginnen, ignorieren Sie exchangecookie, wenn Sie in nachfolgenden Abonnementanforderungen enthalten sind.
  
```XML
HTTP/1.1 200 OK
Content-Type: text/xml; charset=utf-8
Set-Cookie: exchangecookie=ddb8c383aef34c7694132aa679744feb; expires=Thu, 25-Sep-2014 18:42:45 GMT; path=/;
    HttpOnly
Set-Cookie: X-BackEndOverrideCookie=CO1PR06MB222.namprd06.prod.outlook.com~1941996295; path=/; secure; HttpOnly
Set-Cookie: X-BackEndCookie=alfred@contoso.com=Ox8XKzcXLxg==; 
    expires=Wed, 25-Sep-2013 18:52:49 GMT; path=/EWS; secure; HttpOnly
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="775"
                         MinorBuildNumber="7"
                         Version="V2_4"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SubscribeResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SubscribeResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SubscriptionId>JgBjbzFwcjA2bWIyMjIubmFtcHJkMDYucHJvZC5vdXRsb29rLmNvbRAAAAAUeGk+7JFdSaFM8/NI/gQQpVdgZX6H0Ag=</m:SubscriptionId>
        </m:SubscribeResponseMessage>
      </m:ResponseMessages>
    </m:SubscribeResponse>
  </s:Body>
</s:Envelope>
```

Wenn Sie die x-BackEndOverrideCookie von Alfreds Antwort und den x-AnchorMailbox-Header verwenden, wird die Abonnementanforderung für Sadie erstellt, das andere Mitglied der Abonnementanforderung der Gruppe A. Sadie sieht wie folgt aus.
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
Accept: text/xml
User-Agent: ExchangeServicesClient/15.00.0516.014
X-AnchorMailbox: alfred@contoso.com
X-PreferServerAffinity: true
Host: outlook.office365.com
Cookie: X-BackEndOverrideCookie=CO1PR06MB222.namprd06.prod.outlook.com~1941996295
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
    <t:ExchangeImpersonation>
      <t:ConnectingSID>
        <t:SmtpAddress>sadie@contoso.com </t:SmtpAddress>
      </t:ConnectingSID>
    </t:ExchangeImpersonation>
  </soap:Header>
  <soap:Body>
    <m:Subscribe>
      <m:StreamingSubscriptionRequest>
        <t:FolderIds>
          <t:DistinguishedFolderId Id="inbox" />
        </t:FolderIds>
        <t:EventTypes>
          <t:EventType>NewMailEvent</t:EventType>
        </t:EventTypes>
      </m:StreamingSubscriptionRequest>
    </m:Subscribe>
  </soap:Body>
</soap:Envelope>

```

Sadies Abonnement Antwort sieht wie folgt aus. Beachten Sie, dass die X-BackEndOverrideCookie nicht enthalten ist. Der Client ist für die Zwischenspeicherung dieses Werts für zukünftige Anforderungen verantwortlich.
  
```XML
HTTP/1.1 200 OK
Content-Type: text/xml; charset=utf-8
Set-Cookie: exchangecookie=640ea858f69d47ff8cce8b44c337f6d9; path=/
Set-Cookie: X-BackEndCookie=alfred@contoso.com=Ox8XKzcXLxg==; 
   expires= Wed, 25-Sep-2013 18:53:06 GMT; path=/EWS; secure; HttpOnly
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="775"
                         MinorBuildNumber="7"
                         Version="V2_4"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SubscribeResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SubscribeResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SubscriptionId>JgBjbzFwcjA2bWIyMjIubmFtcHJkMDYucHJvZC5vdXRsb29rLmNvbRAAAAB4EQOy2pfrQJfM3hzs/nZJIZssan6H0Ag=</m:SubscriptionId>
        </m:SubscribeResponseMessage>
      </m:ResponseMessages>
    </m:SubscribeResponse>
  </s:Body>
</s:Envelope>
```

Mithilfe der [Subscription](https://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) -Werte aus den Abonnement Antworten wurde eine [GetStreamingEvents](https://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) -Vorgangsanforderung für alle Abonnements in der Gruppe erstellt. Da in dieser Gruppe weniger als 200 Abonnements vorhanden sind, werden Sie alle in einer einzigen Anforderung gesendet. Der x-PreferServerAffinity-Header ist auf true festgelegt, und die x-BackEndOverrideCookie ist enthalten. 
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
Accept: text/xml
User-Agent: ExchangeServicesClient/15.00.0516.014
X-AnchorMailbox: alfred@contoso.com
X-PreferServerAffinity: true
Host: outlook.office365.com
Cookie: X-BackEndOverrideCookie=CO1PR06MB222.namprd06.prod.outlook.com~1941996295
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
    <t:ExchangeImpersonation>
      <t:ConnectingSID>
        <t:SmtpAddress>sadie@contoso.com</t:SmtpAddress>
      </t:ConnectingSID>
    </t:ExchangeImpersonation>
  </soap:Header>
  <soap:Body>
    <m:GetStreamingEvents>
      <m:SubscriptionIds>
        <t:SubscriptionId>JgBjbzFwcjA2bWIyMjIubmFtcHJkMDYucHJvZC5vdXRsb29rLmNvbRAAAAB4EQOy2pfrQJfM3hzs/nZJIZssan6H0Ag=</t:SubscriptionId>
        <t:SubscriptionId>JgBjbzFwcjA2bWIyMjIubmFtcHJkMDYucHJvZC5vdXRsb29rLmNvbRAAAAAUeGk+7JFdSaFM8/NI/gQQpVdgZX6H0Ag=</t:SubscriptionId>
      </m:SubscriptionIds>
      <m:ConnectionTimeout>10</m:ConnectionTimeout>
    </m:GetStreamingEvents>
  </soap:Body>
</soap:Envelope>
```

Die zurückgegebenen Ereignisse werden dann zur Verarbeitung an einen separaten Thread übergeben.
  
## <a name="how-has-affinity-changed"></a>Wie wurde die Affinität geändert?
<a name="bk_howchanged"> </a>

In Exchange 2010 werden Abonnements auf dem Client Zugriffsserver verwaltet, wie in Abbildung 3 dargestellt. In Versionen von Exchange später als Exchange 2010 werden Abonnements auf dem Postfachserver verwaltet, wie in Abbildung 4 dargestellt.
  
**Abbildung 3. Prozess zum Beibehalten der Affinität in Exchange 2010**

![Abbildung, die zeigt, wie die Tabelle aktiver Abonnements auf dem Clientzugriffsserver in Exchange 2010 verwaltet wird.](media/Exchange2013_NoficationAffinity2010.png)
  
**Abbildung 4. Prozess zum Beibehalten der Affinität in Exchange Online und Exchange 2013**

![Abbildung, die zeigt, wie der Lastenausgleich und Clientzugriffsserver Anforderungen an den Postfachserver leiten, der die Tabelle aktiver Abonnements in Exchange Server und Exchange Online verwaltet.](media/Exchange2013_NoficationAffinity2013.png)
  
In Exchange 2010 kennt der Client nur die Adresse des Lastenausgleichsmoduls, und die vom Server zurückgegebene exchangecookie stellt sicher, dass die Anforderung an den richtigen Clientzugriffsserver weitergeleitet wird. In höheren Versionen müssen das Lastenausgleichsmodul und die Client Zugriffs-Serverrollen beide Anforderungen jedoch entsprechend weiterleiten, bevor Sie zum Postfachserver gelangen. Dafür sind zusätzliche Informationen erforderlich, weshalb die neuen Header und Cookies eingeführt wurden. In den Artikeln [Benachrichtigungsabonnements, Post Fach Ereignisse und EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) wird erklärt, wie Abonnements in Exchange 2013 verwaltet werden. 
  
Möglicherweise wird feststellen, dass die exchangecookie, die von Exchange 2010 verwendet werden, noch von höheren Versionen zurückgegeben werden. Es schadet nicht, dieses Cookie in Anforderungen einzubinden, aber spätere Versionen von Exchange ignorieren es.
  
## <a name="see-also"></a>Siehe auch

- [Benachrichtigungsabonnements, Postfachereignisse und EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
- [Streambenachrichtigungen zu Postfachereignissen mithilfe von EWS in Exchange](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
- [Pullbenachrichtigungen zu Postfachereignissen mithilfe von EWS in Exchange](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
- [Umgang von Fehlern im Zusammenhang mit Benachrichtigungen in EWS in Exchange](handling-notification-related-errors-in-ews-in-exchange.md)
- [Änderungen beim Verwalten der Affinität für EWS-Abonnements...](https://blogs.msdn.com/b/mstehle/archive/2013/04/17/changes-in-managing-affinity-for-ews-subscriptions.aspx)
- [EWS-Einschränkung in Exchange](ews-throttling-in-exchange.md)
    

