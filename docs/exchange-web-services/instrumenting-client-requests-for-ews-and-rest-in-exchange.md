---
title: Handhaben von Clientanforderungen für EWS und REST in Exchange
manager: sethgros
ms.date: 4/13/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 330de503-498d-447e-b4a9-c20fc1699fd1
description: Erfahren Sie mehr über die HTTP-Header in EWS-und Rest-Anforderungen und-Antworten, die Ihnen bei der Überwachung und Problembehandlung Ihrer Exchange-Anwendung helfen können.
ms.openlocfilehash: 3a8ce889ec7a6b9e70ec25a95ac248902f48ca6c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456304"
---
# <a name="instrumenting-client-requests-for-ews-and-rest-in-exchange"></a>Handhaben von Clientanforderungen für EWS und REST in Exchange

Erfahren Sie mehr über die HTTP-Header in EWS-und Rest-Anforderungen und-Antworten, die Ihnen bei der Überwachung und Problembehandlung Ihrer Exchange-Anwendung helfen können.
  
Ist dir das je passiert? Ein Benutzer Ihrer Anwendung meldet einen unerwarteten Fehler. Sie möchten untersuchen, aber nicht reproduzieren. Der Fehler ist für den Benutzer verschwunden, und es sind nur sehr wenige Daten mit Aktionen mehr möglich. Frustrierend, oder? Sehen wir uns an, wie Sie sich proaktiv auf dieses Szenario vorbereiten können, und dass Sie in Zukunft hoffentlich Frustration vermeiden.
  
## <a name="add-instrumentation-to-requests"></a>Hinzufügen von Instrumentation zu Anforderungen

Es wird empfohlen, Ihren Anforderungen zusätzliche HTTP-Header hinzuzufügen, um die Problembehandlung zu erleichtern. Sie sollten diese Informationen irgendwo aufzeichnen (beispielsweise in einer Protokolldatei), damit Sie Sie später bei Bedarf abrufen können. Dies ist hilfreich, wenn Sie den Netzwerkdatenverkehr untersuchen, und ist auch hilfreich, wenn Sie sich an den Microsoft-Support wenden.
  
**Tabelle 1. Anforderungs Kopfzeilen für die Problembehandlung**

|**HTTP-Header (EWS)**|**Entsprechung in der verwalteten EWS-API**|**Hinweise**|
|:-----|:-----|:-----|
|Benutzer-Agent  <br/> |[Datei "ExchangeService. UserAgent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.useragent%28v=exchg.80%29.aspx) <br/> |Legen Sie dies auf einen eindeutigen Wert fest, der Ihre Clientanwendung identifiziert.<br/><br/> Wenn der gleiche Wert für alle von der Anwendung gesendeten Anforderungen verwendet wird, kann Microsoft bei der Behandlung von Anruf Fehlern helfen, falls diese auftreten.  <br/> |
|Client-Request-ID  <br/> |[Datei "ExchangeService. ClientRequestId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.clientrequestid%28v=exchg.80%29.aspx) <br/> |Legen Sie dies für jede Anforderung, die Ihre Anwendung sendet, auf einen anderen eindeutigen Wert fest.<br/><br/> Es wird empfohlen, eine GUID zu verwenden. Dieser eindeutige Bezeichner dient zum Korrelieren von Aktivitäten zwischen zwei Systemen für den Fall, dass etwas schief geht.  <br/> |
|Return-Client-Request-ID  <br/> |[Datei "ExchangeService. ReturnClientRequestId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.returnclientrequestid%28v=exchg.80%29.aspx) <br/> |Legen Sie diese auf **true** fest, um dem Exchange-Server mitteilen zu können, dass der Wert Ihrer Client-Request-ID in der entsprechenden Antwort zurückgegeben werden soll.<br/><br/> Sie können dies verwenden, um Anforderungen und Antworten in Netzwerkablaufverfolgungen oder verwaltete EWS-API Ablaufverfolgungen zu korrelieren.  <br/> |
|X-ClientStatistics  <br/> |[Datei "ExchangeService. SendClientLatencies](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.sendclientlatencies%28v=exchg.80%29.aspx) <br/> |Wird verwendet, um [EWS-Latenzen](#bk_ReportLatency) an Microsoft zu melden, wenn Ihre Anwendung auf Exchange Online oder Exchange Online im Rahmen von Office 365 zugreift.  <br/> |
   
## <a name="log-information-from-responses"></a>Protokollieren von Informationen aus Antworten

So wie Ihr Client den von ihm gesendeten Anforderungen zusätzliche Instrumentation hinzufügen kann, fügt Exchange der Antwort in Form von HTTP-Headern zusätzliche Instrumentation hinzu. Ihr Client sollte diese Informationen erfassen, um mit den Informationen zur Anforderungs Instrumentation zusammenzukehren.
  
> [!NOTE]
> Wenn Sie die verwaltete EWS-API verwenden, gibt es keine direkte Entsprechung für die HTTP-Header. Allerdings kann über die [Datei "ExchangeService. HttpResponseHeaders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.httpresponseheaders%28v=exchg.80%29.aspx) -Eigenschaft auf alle HTTP-Antwortheader zugegriffen werden. 
  
**Tabelle 2. HTTP-Antwortheader**

|**HTTP-Header**|**Beschreibung**|
|:-----|:-----|
|Anforderungs-ID  <br/> |Eine vom Server generierte ID für die Anforderung, die dieser Antwort entspricht.  <br/> |
|Client-Request-ID  <br/> |Der Wert des Client-Request-ID-Headers in der Anforderung.<br/><br/> Dieser Header ist nur vorhanden, wenn die Anforderung den Return-Client-Request-ID-Header mit dem Wert " **true**" enthält.  <br/> |
|X-FEServer  <br/> |Der FQDN des Client Zugriffsservers, der die Anforderung verarbeitet hat.  <br/> |
|X-TargetBEServer  <br/> |Der FQDN des Postfachservers, der die Anforderung verarbeitet hat.  <br/> |
|X-DiagInfo  <br/> |Je nach Anforderung zusätzliche Diagnoseinformationen.  <br/> |
|x-ms-Diagnostics  <br/> | Diese Kopfzeile gilt nur, wenn die OAuth-Authentifizierung in der Anforderung verwendet wird.<br/><br/> Es enthält einen expliziten Fehlercode, der angibt, warum eine OAuth-Authentifizierung fehlgeschlagen ist.<br/><br/> Es hat das folgende Format:`errorId;reason="reason"error_type="error type"`<br/><br/> Das **Grund** Feld ist eine lesbare Beschreibung des Fehlers.<br/><br/> Das Feld **Fehler** -Nr ist eine ganze Zahl, und das Feld **Fehlertyp \_ ** ist die Zeichenfolgendarstellung dieser ganzen Zahl, wie folgt:<ul><li>2 Millionen: Ungültige \_ Signatur</li><li>2000001: ungültiges \_ Token</li><li>  2000002: Token \_ abgelaufen</li><li>2000003: Ungültige \_ Ressource</li><li>2000004: Ungültiger \_ Mandant  </li><li>2000005: Ungültiger \_ Benutzer</li><li>2000006: Ungültiger \_ Client</li><li>2000007: interner \_ Fehler</li><li>2000008: Ungültige \_ Berechtigung</li></ul> |
   
## <a name="report-ews-latency-to-microsoft"></a>Melden der EWS-Wartezeit für Microsoft
<a name="bk_ReportLatency"> </a>

Wenn Ihre Anwendung die verwaltete EWS-API oder EWS verwendet, um eine Verbindung mit Exchange Online herzustellen, können Sie die Wartezeit in EWS-Anforderungen direkt an Microsoft melden. Die Informationen werden über den X-ClientStatistics-Anforderungsheader übergeben. Wenn Sie die verwaltete EWS-API verwenden, müssen Sie lediglich die [Datei "ExchangeService. SendClientLatencies](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.sendclientlatencies%28v=exchg.80%29.aspx) -Eigenschaft auf **true**festlegen. Wenn Sie EWS verwenden, müssen Sie die Zeit zwischen dem Ausgeben einer Anforderung und dem Empfangen einer Antwort Messen und dann den X-ClientStatistics-Header der nächsten von der Anwendung gesendeten EWS-Anforderung mithilfe des folgenden Formats hinzufügen.
  
`X-ClientStatistics: MessageId=<value of request-id header>,ResponseTime=<time in milliseconds>,SoapAction=<EWS operation>`
  
Wir halten Berichte zu diesen Wartezeiten und verwenden diese, um die EWS-Dienste in Exchange Online kontinuierlich zu verbessern.
  
## <a name="next-steps"></a>Nächste Schritte
<a name="bk_ReportLatency"> </a>

Nachdem Sie die Client Instrumentation zu Ihrer Anwendung hinzugefügt haben, sind Sie besser vorbereitet, wenn etwas schief geht. In diesem Fall können Sie Ihre Instrumentationsdaten zur [Problembehandlung Ihrer Anwendung](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)verwenden.
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)
- [Ablaufverfolgungsanforderungen und -antworten zur Problembehandlung bei EWS-verwalteten API-Anwendungen](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
- [Tools und Ressourcen für die Problembehandlung bei EWS-Anwendungen für Exchange](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

