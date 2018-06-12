---
title: EWS-Einschränkung in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: b4fff4c9-c625-4d2a-9d14-bb28a5da5baf
description: Lernen Sie die Einschränkungsrichtlinien kennen, die sich bei Verwendung von Exchange auf EWS auswirken.
ms.openlocfilehash: e7966f67753b3998235e000a022e41c90fa227b8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756887"
---
# <a name="ews-throttling-in-exchange"></a>EWS-Einschränkung in Exchange

Lernen Sie die Einschränkungsrichtlinien kennen, die sich bei Verwendung von Exchange auf EWS auswirken.
  
**Bereitgestellt von:** Glen Scales; Michael Mainer, Microsoft Corporation 
  
Dieser Artikel enthält Informationen über EWS-Einschränkungen in Exchange Online, Exchange Online als Teil von Office 365 und lokale Versionen von Exchange ab Exchange 2010. Einschränkungen in Exchange dienen zur Sicherstellung von Serverzuverlässigkeit und -betriebszeit durch Begrenzung der Menge an Serverressourcen, die ein einzelner Benutzer oder eine einzelne Anwendung verbrauchen kann. Einschränkungen sind eine reaktive Antwort auf die übermäßige Nutzung von Systemressourcen, die die Zuverlässigkeit und die Funktionalität von Diensten beeinflussen kann. Exchange überwacht kontinuierlich die Integrität kritischer Infrastrukturressourcen, z. B. von Postfachdatenbanken. Wenn hohe Lastfaktoren entdeckt werden, die die Leistung dieser Ressourcen beeinträchtigen, werden EWS-Verbindungen proportional basierend auf dem Anteil eingeschränkt, den jede aufrufende Person oder Anwendung zu dieser hohen Lastbedingung beigetragen hat. Dies kann dazu führen, dass ein Benutzer, der die Einschränkungsgrenzwerte nicht überschreitet, möglicherweise trotzdem Verzögerungen hinnehmen muss, bis die Integrität der Ressource wieder das Betriebniveau erreicht.
  
Jedes Clientzugriffsprotokoll in Exchange, einschließlich EWS, verfügt über eine Einschränkungsrichtlinie. Beim Entwerfen von Anwendungen, die EWS verwenden, müssen Einschränkungsrichtlinien berücksichtigt werden, um die Anwendungszuverlässigkeit und die Integrität des Exchange-Servers sicherzustellen. In diesem Artikel werden die verschiedenen Einschränkungsrichtlinien und Dienstgrenzwerte für EWS für Exchange Online oder Versionen von Exchange lokal ab Exchange Server 2010 vorgestellt. Gegebenenfalls werden in diesem Artikel außerdem Unterschiede bei den Einschränkungsrichtlinien in verschiedenen Exchange-Versionen aufgezeigt.
  
> [!IMPORTANT]
> [!WICHTIG] Die standardmäßige Einschränkungsrichtlinie, der Zugriff auf Einschränkungsrichtlinien und die Konfiguration von Einschränkungsrichtlinien unterscheiden sich zwischen Exchange Online und Exchange lokal. Bestimmte Werte von Einschränkungseinstellungen sind nur für eine bestimmte Version von Exchange zutreffend. Da Einstellungswerte nach Version variieren und Exchange-Administratoren die standardmäßigen Richtlinien für lokale Bereitstellungen ändern können, werden die standardmäßigen Einstellungswerte in diesem Artikel nicht angegeben. Es ist wichtiger, dass Ihnen die Überlegungen bekannt sind, die Sie zum Entwerfen einer Anwendung berücksichtigen müssen, die innerhalb von Einschränkungsgrenzwerten funktioniert und angemessen auf Einschränkungsszenarien reagiert. 
  
Als Anwendungsentwickler müssen Sie in Ihrem Anwendungsentwurf Einschränkungen berücksichtigen. Unterschiedliche Exchange-Versionen haben unterschiedliche Standardwerte für die EWS-Einschränkungsparameter. Client- und Dienstanwendungen, die für den Zugriff auf verschiedene Exchange-Versionen konzipiert sind, müssen diese Einstellungen berücksichtigen, egal ob es sich um Standardwerte, von einem Exchange-Administrator festgelegte benutzerdefinierte Werte oder - wie im Fall von Exchange Online - standardmäßig festgelegte und nicht auffindbare Werte handelt. Da Werte für Einschränkungsparameter nicht programmgesteuert ermittelt werden können, sollten die Cliententwurfsspezifikationen einen Plan enthalten, wie sich die Anwendung an verschiedene mögliche Einschränkungsgrenzwerte anpasst. Beim Entwerfen von Multithreadanwendungen, die auf eine große Anzahl von Postfächern zugreifen, oder wenn viele Clients auf dasselbe Postfach zugreifen, berücksichtigen Sie die Grenzwerte für Parallelität, die die Standardrichtlinie auf Exchange anwendet. 
  
## <a name="throttling-policies-that-affect-ews"></a>Einschränkungsrichtlinien mit Auswirkung auf EWS
<a name="bk_PolicyParameters"> </a>

Die Einschränkungsrichtlinien in Exchange wirken sich nicht nur auf EWS, sondern auch auf alle Clientverbindungen mit dem Exchange-Server aus, einschließlich der von Office Outlook, Outlook Web App und Exchange ActiveSync verwendeten Protokolle. 
  
Die **CPUStartPercent** -Einschränkungsrichtlinie kann sich auf die EWS-Leistung auswirken, wenn Sie Exchange 2010 ausführen. Wenn die durchschnittliche CPU-Auslastung von Exchange-Prozessen, die auf dem Clientzugriffsserver ausgeführt werden (einschließlich, aber nicht beschränkt auf den EWS-Prozess), den von dieser Richtlinie angegebenen Wert überschreitet, werden eingehende Anfragen verzögert, um die CPU-Auslastung zu verringern. Sie können den Wert dieser Richtlinie nicht ändern, ihn zu kennen, kann jedoch bei der Behebung von Leistungsproblemen helfen. Die Samplinglogik, die der Clientzugriffsserver für diesen Wert ausführt, ist ein Mittelwert über ein 10-Sekunden-Gleitfenster. Dadurch kann der Prozess angemessen auf schnelle Spitzen in der CPU-Auslastung reagieren. Wenn dieser Schwellenwert überschritten wird, werden eingehende Verbindungen mit EWS verzögert. Diese Verzögerung ist auf 500 Millisekunden (ms) bei einer theoretischen 100-prozentigen CPU-Auslastung pro EWS-Anforderung begrenzt. Wenn eine EWS-Batchanforderung zum Abrufen von 100 Elementen übergeben wird, überprüft der Server die CPU-Auslastung 100 Mal (ein Mal pro Element), und es kann eine maximale Verzögerung von 50 Sekunden entstehen. Die Verzögerungsdauer ist linear proportional zur CPU-Auslastung. Bei **CPUStartPercent** beträgt die Verzögerung 0 (ein Threadergebnis) und erhöht sich linear auf bis zu 500 ms bei 100-prozentiger CPU-Auslastung. Da Einschränkungsrichtlinien für alle Exchange-Benutzer gelten, ist es unwahrscheinlich, dass die CPU-Auslastung den **CPUStartPercent** -Grenzwert auf einem Exchange-Clientzugriffsserver überschreitet, da einzelne Benutzer oder Anwendungen nicht genügend CPU-Auslastung erzeugen können, um den Serverbetrieb zu beeinflussen. 
  
In der folgenden Tabelle sind die Einschränkungsrichtlinienparameter aufgeführt, die sich auf Anwendungen mit EWS-Nutzung auswirken.
  
**Tabelle 1: Einschränkungsrichtlinienparameter mit Auswirkung auf EWS**

|**Name des Einschränkungsrichtlinienparameters**|**Betrifft**|**Beschreibung**|
|:-----|:-----|:-----|
|**DiscoveryMaxConcurrency** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Gibt die Anzahl der gleichzeitigen Discoverysuchverbindungen an, die ein Benutzer zur gleichen Zeit geöffnet haben kann.  <br/> |
|**DiscoveryMaxKeywords** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Gibt die maximale Anzahl an Schlüsselwörtern an, die ein Benutzer in eine Discoverysuche einschließen kann.  <br/> |
|**DiscoveryMaxKeywordsPerPage** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Gibt die Anzahl an Schlüsselwörtern an, für die Statistiken angezeigt werden sollen.  <br/> |
|**DiscoveryMaxMailboxes** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Gibt die maximale Anzahl an Quellpostfächern an, die ein Benutzer in eine Discoverysuche einschließen kann.  <br/> |
|**DiscoveryMaxMailboxesResultsOnly** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Gibt die maximale Anzahl an Postfächern an, die Sie in einer In-Situ-eDiscovery-Suche durchsuchen können, ohne die Statistik anzeigen zu können.  <br/> |
|**DiscoveryPreviewSearchResultsPageSize** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Gibt die Anzahl an Nachrichten an, die in der Vorschauantwort einer eDiscovery-Suche zurückgegeben werden.  <br/> |
|**EwsCutoffBalance** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Definiert die Grenzwerte für die Ressourcennutzung für EWS-Benutzer, bevor der Benutzer vollständig an der Ausführung von Vorgängen für eine bestimmte Komponente gehindert wird.  <br/> |
|**EwsMaxBurst** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Definiert den Zeitraum, für den ein EWS-Benutzer eine erhöhte Menge von Ressourcen verbrauchen darf, bevor er eingeschränkt wird. Dieser Zeitraum wird in Millisekunden gemessen. Dieser Wert wird für jede Komponente einzeln festgelegt.  <br/> |
|**EwsRechargeRate** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Definiert die Rate, mit der das Budget eines EWS-Benutzers während der Budgetzeit aufgeladen wird (um die das Budget wächst).  <br/> |
|**EWSMaxSubscriptions** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |Definiert die maximale Anzahl an aktiven Push-, Pull- und Streamingbenachrichtigungsabonnements, über die ein Benutzer auf einem bestimmten Clientzugriffsserver gleichzeitig verfügen kann. Dies wird je nach Exchange-Version anders budgetiert.  <br/> |
|**EWSFastSearchTimeoutInSeconds** <br/> |Exchange 2010  <br/> |Definiert die Zeitspanne in Sekunden, die mit der Exchange-Suche in EWS durchgeführte schnelle Suchläufe fortgesetzt werden, bevor ein Timeout eintritt. Schnelle Suchläufe sind Suchvorgänge, die mithilfe einer AQS-Abfragezeichenfolge (Advanced Query Syntax, erweiterte Abfragesyntax) in einem [FindItem-Vorgang](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) ausgeführt werden.    <br/> |
|**EWSFindCountLimit** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |Definiert die maximale Anzahl an Elementen aus einem [FindItem-Vorgang](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) oder einem [FindFolder Operation](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx), die gleichzeitig für einen bestimmten Benutzer im Arbeitsspeicher auf dem Clientzugriffsserver vorhanden sein können. Der Standardwert für diese Eigenschaft ist 1000. Der [Ausweichwert](http://technet.microsoft.com/en-us/library/dd297964%28v=exchg.141%29.aspx#fallback) für diesen Wert ist 1000.  <br/> In Exchange Online und lokalen Versionen von Exchange ab Exchange 2013 kann diese Einschränkungsrichtlinie nicht abgefragt oder von einem Cmdlet konfiguriert werden. In Exchange Online und lokalen Versionen von Exchange ab Exchange 2013 beträgt der EWSFindCountLimit für die [AQS-Suche](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md) und alle Exchange-Suchvorgänge mit einer Beschränkung 250 Ergebnisse. Eine Exchange-Suche ohne Beschränkung gibt bis zu 1000 Ergebnisse zurück.  <br/> |
|**EWSPercentTimeInAD** <br/> |Exchange 2010  <br/> |Definiert die Zeit pro Minute in Prozent, für die ein bestimmter Benutzer Active Directory-Anforderungen ausführen kann.  <br/> |
|**EWSPercentTimeInCAS** <br/> |Exchange 2010  <br/> |Definiert die Zeit pro Minute in Prozent, für die ein bestimmter Benutzer Clientzugriffsserver-Code ausführen kann.  <br/> |
|**EWSPercentTimeInMailboxRPC** <br/> |Exchange 2010  <br/> |Definiert die Zeit pro Minute in Prozent, für die ein bestimmter Benutzer Postfach-RPC-Anforderungen ausführen kann.  <br/> |
|**EWSMaxConcurrency** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |Definiert die Anzahl der Verbindungen, die ein bestimmter Benutzer gleichzeitig auf einem Exchange-Server geöffnet haben kann, auf dem EWS ausgeführt wird. Der Standardwert für Exchange 2010 ist 10. Der Standardwert für Exchange 2013 und Exchange Online ist 27.  <br/> Diese Richtlinie gilt für alle Vorgänge mit Ausnahme von Streamingbenachrichtigungen. Streamingbenachrichtigungen verwenden den **HangingConnectionLimit**, um die Anzahl der verfügbaren geöffneten Streamingereignisverbindungen anzugeben. Weitere Informationen finden Sie unter [Welche Drosselung Werte muss ich berücksichtigen?](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling).  <br/> |
|**MessageRateLimit** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |Definiert die Anzahl an Nachrichten pro Minute, die gesendet werden können.  <br/> |
|**RecipientRateLimit** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |Definiert den Grenzwert für die Anzahl an Empfängern, die ein Benutzer in einem Zeitraum von 24 Stunden adressieren kann.  <br/> |
|**ForwardeeLimit** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |Definiert den Grenzwert für die Anzahl an Empfängern für Weiterleitungs-/Umleitungsaktionen im Posteingang in einem Zeitraum von 24 Stunden.  <br/> |
   
> [!CAUTION]
> [!VORSICHT] Legen Sie Einschränkungsrichtlinien nicht auf **null** fest. Hierdurch wird die Richtlinie auf "unbegrenzt" festgelegt, was bedeutet, dass eine Einschränkungsrichtlinie nicht festgelegt ist. 
  
## <a name="displaying-the-policies-that-apply-to-exchange-mailboxes"></a>Anzeigen der für Exchange-Postfächer geltenden Richtlinien
<a name="bk_PolicyCmdlets"> </a>

Exchange lokal stellt Exchange-Verwaltungsshell-Cmdlets zur Verfügung, mit denen Sie Einschränkungsrichtlinien festlegen und abrufen können. Exchange Online bietet keinen Zugriff auf die Einschränkungsrichtlinien-Cmdlets.
  
Sie können die folgenden Cmdlets verwenden, um Einschränkungsrichtlinien für eine lokale Bereitstellung von Exchange Server anzuzeigen:
  
- **Get-ThrottlingPolicy** - Ruft die Clienteinschränkungseinstellungen für eine oder mehrere Einschränkungsrichtlinien ab. Weitere Informationen finden Sie unter [Get-ThrottlingPolicy ](http://technet.microsoft.com/en-us/library/dd351264.aspx) in TechNet. 
    
- **Get-ThrottlingPolicyAssociation** - Ermöglicht es Ihnen, die Beziehung zwischen einem Objekt und den zugeordneten Einschränkungsrichtlinien anzuzeigen. Bei dem Objekt kann es sich um einen Benutzer mit einem Postfach, einen Benutzer ohne Postfach oder einen Kontakt handeln. Weitere Informationen finden Sie unter [Get-ThrottlingPolicyAssociation](http://technet.microsoft.com/en-us/library/ff459241.aspx) in TechNet. 
    
Verwenden Sie den folgenden Befehl, um die standardmäßige Einschränkungsrichtlinie für Exchange 2010 anzuzeigen.
  
**Get-ThrottlingPolicy | Where-Object {$_.IsDefault -eq "True"} | format-list**
  
Verwenden Sie den folgenden Befehl, um die globale Einschränkungsrichtlinie in Exchange 2013 anzuzeigen (die der standardmäßigen Einschränkungsrichtlinie in Exchange 2010 entspricht).
  
**Get-ThrottlingPolicy | Where-Object {$_.ThrottlingPolicyScope -eq "Global"} | format-list**
  
Verwenden Sie den folgenden Befehl, um die einem Benutzer in Exchange 2010 oder Exchange 2013 zugeordnete Einschränkungsrichtlinie anzuzeigen. Ersetzen Sie den Benutzernamen john@contoso.com durch den Benutzernamen des Zielbenutzers, für den Sie Informationen zu Einschränkungsrichtlinien abrufen möchten.
  
**Get-ThrottlingPolicyAssociation john@contoso.com | format-list**
  
Bei Ausführung dieses Befehls in der Exchange-Verwaltungsshell wird eine Ausgabe ähnlich der folgenden generiert.
  
```powershell
PS C:\>Get-ThrottlingPolicyAssociation john@contoso.com
RunspaceId               : 72153d6-9dce-2fae-8dbd-5ca5f760g2df
ObjectId                 : john
ThrottlingPolicyId       :
Name                     : john
Identity                 : FHXB-28178dom.contoso.com/Users/john
IsValid                  : True
NeedsToSuppressPii       : False
ExchangeVersion          : 0.10 (15.0.0.0)
DistinguishedName        : CN=john,CN=Users,DC=FHXB-28178dom,DC=contoso,DC=com
Guid                     : 2c10dab6-de28-1937-ad8g-535832613a08
```

> [!NOTE]
> [!HINWEIS] Wenn die **ThrottlingPolicyId** -Eigenschaft leer ist, wird die Standardrichtlinie auf das Postfach angewendet. 
  
Sie können Einschränkungsrichtlinien auf einem Exchange-Server mithilfe der Cmdlets [Set-ThrottlingPolicy](http://technet.microsoft.com/en-us/library/dd298094.aspx) und [Set-ThrottlingPolicyAssociation](http://technet.microsoft.com/en-us/library/ff459231.aspx) festlegen. Zum Erstellen und Entfernen nicht standardmäßiger Einschränkungsrichtlinien können Sie die Cmdlets [New-ThrottlingPolicy](http://technet.microsoft.com/en-us/library/dd351045.aspx) und [Remove-ThrottlingPolicy](http://technet.microsoft.com/en-us/library/dd351178.aspx) verwenden. 
  
> [!TIP]
> [!TIPP] Es wird empfohlen, Anwendungen so zu entwerfen, dass sie die standardmäßige Einschränkungsrichtlinie einhalten. Nehmen Sie nur dann Änderungen an standardmäßigen Einschränkungsrichtlinien vor, wenn der Clientanwendungsentwurf die Standardrichtlinie nicht berücksichtigen kann. Beachten Sie, dass weniger restriktive Einschränkungsrichtlinien die Dienstzuverlässigkeit beeinträchtigen können. 
  
## <a name="throttling-considerations-for-applications-that-use-ews-impersonation"></a>Einschränkungsüberlegungen für Anwendungen, die EWS-Identitätswechsel verwenden
<a name="bk_ThrottlingConsiderations"> </a>

[Identitätswechsel](impersonation-and-ews-in-exchange.md) ist eine Autorisierungsmethode, die einem einzelnen Konto den Zugriff auf viele Konten ermöglicht. Wenn ein Dienstkonto die Identität von Benutzern annimmt, agiert es als diese Benutzer und übernimmt daher die Rechte, die diesen Benutzern zugewiesen sind. Protokolldateien zeichnen den Zugriff als den Benutzer auf, dessen Identität angenommen wird. Administratoren verwenden die rollenbasierte Zugriffssteuerung (Role-Based Access Control, RBAC), um den Identitätswechsel über die Exchange-Verwaltungsshell zu konfigurieren. 
  
Wenn Identitätswechsel verwendet wird, gelten die Budgets für alle Einschränkungsschwellenwerte je nach Exchange-Version unterschiedlich. Das Budget wird entweder für das Konto, dessen Identität angenommen wird, oder für das Dienstkonto verrechnet. Im Fall einer Multithreadanwendung, die gleichzeitige Anforderungen für mehrere Postfächer ausführt, sollten Sie überlegen, wie sich der Einschränkungsschwellenwert auf die Leistung Ihrer Anwendung auswirkt. Im Allgemeinen sollten Sie die folgenden Grenzwerte für Dienstkonten berücksichtigen, wenn Sie eine dienstbasierte Anwendung erstellen, die Identitätswechsel für den Zugriff auf alle Postfächer verwendet: 
  
- Bei Verwendung von Identitätswechsel hat das Dienstkonto ein getrenntes Budget für die folgenden Richtlinienparameter:
    
  - **EWSMaxConcurrency**
    
  - **EWSPercentTimeInAD**
    
  - **EWSPercentTimeInCAS**
    
  - **EWSPercentTimeInMailboxRPC**
    
  - **EWSMaxSubscriptions**
    
  - **EWSFastSearchTimeoutInSeconds**
    
  - **EWSFindCountLimit**
    
- Das **EWSMaxConcurrency** -Budget wird vom Dienstkonto und von dem Konto, dessen Identität angenommen wird, gemeinsam verwendet, und zwar für alle Verbindungen mit Exchange-Versionen vor Exchange 2010 Service Pack 2 (SP2) Update Rollup 4 (RU4). Ab Exchange 2010 SP2 RU4 und einschließlich Exchange Online verwendet der Dienstkontozugriff ein vom **EWSMaxConcurrency** -Budget des Benutzers getrenntes Budget. Weitere Informationen zum Update auf die Exchange-Einschränkungsrichtlinie für gleichzeitige Verbindungen für EWS finden Sie unter [Hinweise zum Updaterollup 4 für Exchange Server 2010 Servicepack 2](http://support.microsoft.com/kb/2706690).
    
    EWS-Streamingbenachrichtigungen in Exchange-Versionen ab Exchange 2010 und einschließlich Exchange Online haben ein zusätzliches geklontes **EWSMaxConcurrency** -Budget von allen anderen EWS-Clientverbindungen. Verbindungen für Streamingbenachrichtigungen werden mit einem von allen anderen EWS-Vorgängen getrennten Budget verrechnet. Das maximale Parallelitätsbudget für Streamingbenachrichtigungen besteht tatsächlich aus zwei verschiedenen Budgets: einem Budget für alle Dienstkonten und einem Budget für das Konto. dessen Identität angenommen wird. Streamingbenachrichtigungen in Exchange Online und Exchange-Versionen ab Exchange 2013 verwenden den [HangingConnectionLimit](ews-throttling-in-exchange.md#bk_ThrottlingNotifications), um die Anzahl der Verbindungen zu begrenzen. 
    
    Nehmen wir beispielsweise einen **EWSMaxConcurrency** -Wert von fünf an. Ein Benutzer kann fünf geöffnete Pullbenachrichtigungsverbindungen haben, während ein Dienstkonto zeitgleich mit dem Benutzer fünf gleichzeitige Pullbenachrichtigungsverbindungen für das Postfach des Benutzers haben kann. 
    
- Die folgende Tabelle zeigt, wie **EWSMaxSubscriptions** -Einschränkungsbudgets für das Dienstkonto und das Konto, dessen Identität angenommen werden soll, verrechnet werden. 
    
   **Tabelle 2: EWSMaxSubscriptions-Budgetberechnung**

   |**Exchange-Version**|**EWSMaxSubscriptions-Einschränkungsbudgetberechnung**|
   |:-----|:-----|
   |Exchange Online  <br/> |Mit Zielpostfach verrechnet  <br/> |
   |Exchange 2013  <br/> |Mit Zielpostfach verrechnet  <br/> |
   |Exchange 2010 SP3  <br/> |Mit Zielpostfach verrechnet  <br/> |
   |Exchange 2010 SP2  <br/> |Mit aufrufendem Konto verrechnet  <br/> |
   |Exchange 2010 SP1  <br/> |Mit aufrufendem Konto verrechnet  <br/> |
   |Exchange 2010  <br/> |Mit aufrufendem Konto verrechnet  <br/> |
   
- Da das **EWSMaxSubscriptions** -Einschränkungsbudget mit dem Konto verrechnet wird, dessen Identität angenommen wird, ist die Anzahl der Postfächer, die ein Dienstkonto abonnieren und für die es Streamingbenachrichtigungen erhalten kann, unbegrenzt, solange der Identitätswechsel verwendet wird. Das Konto, dessen Identität angenommen wird, kann maximal  _n_ gleichzeitige Anforderungen pro Zielpostfach ausführen, wobei  _n_ der **EWSMaxSubscriptions** -Wert ist. Wenn kein Identitätswechsel verwendet wird, sind für das gleiche Dienstkonto insgesamt maximal  _n_ gleichzeitige Anforderungen zulässig. Dies bedeutet, dass durch Verwendung des Identitätswechsels für ein Dienstkonto die Anzahl der Postfächer, die bedient werden kann, exponentiell erhöht wird. Weitere Informationen finden Sie unter [Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver in Exchange verwalten](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md).
    
- Die Richtlinienparameter **EWSPercentTimeInMailboxRPC**, **EWSPercentTimeInCAS** und **EWSPercentTimeInAD** beziehen sich auf Aktionen, die von einem einzigen Thread durchgeführt werden. Wenn eine Anwendung mehrere gleichzeitige Vorgänge ausführt, müssen Sie den kumulativen Effekt dieser Vorgänge auf das Benutzerressourcenbudget berücksichtigen. 
    
## <a name="throttling-implications-for-ews-batch-requests"></a>Auswirkungen von Einschränkungen für EWS-Batchanforderungen
<a name="bk_ThrottlingBatch"> </a>

Mithilfe von EWS können Sie mehrere Elementanforderungen zu einer einzigen Batchanforderung zusammenfassen, die vom Clientzugriffsserver ausgeführt wird. Dies sorgt für mehr Effizienz und Leistung. Wenn ein Exchange-Server eine Batchanforderung ausführt, wird nach Ausführung jedes einzelnen Elements im Batch das Budget des Benutzers überprüft. Wenn die Anwendung das Budget überschreitet, wird die Verarbeitung des nächsten Elements im Batch verzögert, bis das Budget für den betreffenden Benutzer wiederaufgeladen wurde. Um die erfolgreiche Ausführung von Anwendungen sicherzustellen, die Batchvorgänge nutzen, begrenzen Sie die Anzahl der Elementanforderungen in einem einzelnen Batch, und teilen Sie große Batches in mehrere kleinere Batches auf, um die Zuverlässigkeit der Ergebnisse zu erhöhen. Die Auswirkung eines Batchvorgangs auf bestimmte Einschränkungsschwellenwerte hängt von dem Typ der Anforderung, der Größe der zu verarbeitenden Elemente (z. B. in **UploadItems** - oder **ExportItems** -Vorgängen) und dem Postfachinhalt ab. Einschränkungsrichtlinien wirken sich insofern auf Batchvorgänge aus, als sie die Verarbeitung der Anforderung verlangsamen. Die aufrufende Person oder Anwendung muss daher länger auf die Antwort warten, und es kann zu einem Aufruftimeout kommen, da EWS die Ausführungszeit einer Batchanforderung auf eine Minute beschränkt. 
  
Um die optimale Batchgröße für eine Anwendung zu bestimmen, führen Sie Komponententests mit verschiedenen Eingabesätzen durch, um sicherzustellen, dass in einer Produktionsumgebung keine Fehler in der Anwendung auftreten. 
  
## <a name="throttling-policy-parameters-that-affect-ews-search-operations"></a>Einschränkungsrichtlinienparameter mit Auswirkung auf EWS-Suchvorgänge
<a name="bk_ThrottlingSearch"> </a>

[Suchvorgänge in EWS](search-and-ews-in-exchange.md) können sehr viel Zeit und Ressourcen beanspruchen, je nachdem, wie die Suche ausgeführt wird und welche Informationen angefordert werden. Zum Steuern des Ressourceneinsatzes bei Suchvorgängen können zwei Richtlinienparameter verwendet werden: **EWSFastSearchTimeoutInSeconds** und **EWSFindCountLimit**. 
  
Der **EWSFastSearchTimeoutInSeconds** -Richtlinienparameter gibt die Zeitspanne in Sekunden an, die schnelle EWS-Suchläufe (auch als Inhaltsindizierungssuche bezeichnet) ausgeführt werden, bevor ein Timeout eintritt. Schnelle Suchläufe sind Suchvorgänge, die mithilfe einer AQS-Abfragezeichenfolge (Advanced Query Syntax, erweiterte Abfragesyntax) in einem [FindItem-Vorgang](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) ausgeführt werden.
  
Sie können einen Exchange-Postfachordner auf zwei Arten durchsuchen:
  
- Mithilfe einer Exchange-Informationsspeichersuche, die einen sequenziellen Scan aller Nachrichten im Zielsuchbereich durchführt
    
- Mithilfe des Exchange-Suchdiensts (Inhaltsindizierung)
    
Bei beiden Suchvorgangstypen können Timeouts auftreten. Verwenden Sie nach Möglichkeit den Exchange-Suchdienst, da diese Suchvorgänge häufig für Postfachindizes ausgeführt werden und AQS-Abfragen verwenden. Das folgende Beispiel zeigt, wie eine AQS-Suche im Posteingang mithilfe von EWS und des Exchange-Suchdiensts ausgeführt wird.
  
```cs
ItemView iv = new ItemView(1000);
FindItemsResults<Item> fiitems = service.FindItems(WellKnownFolderName.Inbox, "subject:football", iv);
```

Wenn Sie keine AQS-Suche verwenden können, vermeiden Sie übermäßig komplexe Suchfilter. Vermeiden Sie nach Möglichkeit außerdem, Suchfilter auf der Grundlage berechneter Werte zu erstellen, wenn die Abfrage erweiterte MAPI-Eigenschaften enthält. Die AQS-Suche wurde in Exchange 2010 eingeführt.
  
> [!NOTE]
> [!HINWEIS] Die erste Ausführung einer komplexen Suchabfrage des Exchange-Informationsspeichers ist sehr langsam und führt möglicherweise zu einem Timeout. Danach erfolgt die Antwort auf die Abfrage schneller. Weitere Informationen zu den Exchange-Back-End-Serverprozessen, die während Suchabfragen des Exchange-Informationsspeichers stattfinden, finden Sie unter [Grundlagen der Auswirkungen einer großen Anzahl von Elementen und mit Einschränkungen versehener Ansichten auf die Leistung](http://technet.microsoft.com/en-us/library/cc535025%28EXCHG.80%29.aspx) in TechNet. Die Verwendung eines **SearchFilter** erstellt eine dynamische Beschränkung, die bei zukünftigen ähnlichen Abfragen hilfreich ist. Da diese Beschränkungen jedoch dynamisch sind, sind sie nicht dauerhaft oder zuverlässig und werden nach maximal drei Tagen gelöscht. 
  
Der **EWSFindCountLimit** -Richtlinienparameter gibt die maximale Anzahl an Elementen aus den Ergebnissen eines **FindItem** - oder **FindFolder** -Vorgangs an, die gleichzeitig für einen bestimmten Benutzer im Arbeitsspeicher auf dem Clientzugriffsserver vorhanden sein können. Jedes Element bzw. jeder Ordner, das bzw. den EWS in einer **FindItem** - oder **FindFolder** -Anforderung verarbeitet, wird mit dem im **EWSFindCountLimit** -Element angegebenen Budget verrechnet. Wenn eine Antwort an die anfordernde Person zurückgesendet wird, wird die FindCount-Gebühr für den aktuellen Aufruf freigegeben. Welche Antwort der Server bei Überschreitung des Budgets an eine anfordernde Person zurückgibt, basiert auf dem Wert des **RequestServerVersion** -Elements und darauf, ob die anfordernde Person die Auslagerung angegeben hat. Wenn der Wert des **RequestServerVersion** -Elements Exchange 2010 oder eine frühere Exchange-Version angibt, sendet der Server eine Fehlerantwort mit einem Fehlercode. **ErrorServerBusy**. Wenn der Wert des **RequestServerVersion** -Elements eine Exchange-Version ab Exchange 2010 SP1 oder Exchange Online angibt, und der Client Auslagerung verwendet, gibt EWS möglicherweise ein teilweises Resultset anstelle eines Fehlers zurück. Die Anwendung sollte damit rechnen, dass EWS nicht alle Elemente zurückgibt. Wenn der Wert des **IncludesLastItemInRange** -Elements "false" ist, sollte die Anwendung eine weitere **FindItem** - oder **FindFolder** -Anforderung mit dem neuen Offset durchführen und fortfahren, bis das **IncludesLastItemInRange** -Element "true" zurückgibt. 
  
Bei Ausführung eines **FindItem** - oder **FindFolder** -Vorgangs ist die Verwendung von Auslagerung wichtig. Die verwaltete EWS-API erzwingt die Verwendung von Auslagerung, wenn Sie jedoch andere Methoden wie z. B. EWS-Proxyobjekte oder Raw-SOAP verwenden, muss die Auslagerung explizit festgelegt werden. Das folgende Beispiel zeigt die Verwendung von Auslagerung in der verwalteten EWS-API. 
  
```cs
ItemView iv = new ItemView(1000);
FindItemsResults<Item> fiFindItemResults = service.FindItems(WellKnownFolderName.Inbox, iv);
```

> [!NOTE]
> [!HINWEIS] Die Standardrichtlinie in Exchange beschränkt die Seitengröße auf 1000 Elemente. Die Festlegung der Seitengröße auf einen größeren Wert hat keine praktischen Auswirkungen. 
  
Anwendungen müssen außerdem berücksichtigen, dass der Wert des  _EWSFindCountLimit_-Einschränkungsparameters dazu führen kann, dass ein teilweises Resultset für Anwendungen zurückgegeben wird, die gleichzeitige Anforderungen ausführen. Das folgende Beispiel zeigt, wie die **MoreAvailable** -Eigenschaft in der verwalteten EWS-API verwendet wird, um die Aufnahme aller Ergebnisse in eine Abfrage sicherzustellen. 
  
```cs
ItemView iv = new ItemView(1000);
service.TraceEnabled = false;
FindItemsResults<Item> fiResults = null;
Do 
{
    fiResults = service.FindItems(WellKnownFolderName.Inbox, iv);
    PropertySet itItemPropSet = new PropertySet(BasePropertySet.IdOnly) { EmailMessageSchema.Body };
    //Process Items in Result Set
    iv.Offset += fiResults.Items.Count;
}
while (fiResults.MoreAvailable == true);
```

## <a name="throttling-policies-and-concurrency"></a>Einschränkungsrichtlinien und Parallelität
<a name="bk_ThrottlingConcurrency"> </a>

Parallelität bezeichnet die Anzahl der Verbindungen von einem bestimmten Benutzer. Eine Verbindung wird ab dem Moment gehalten, an dem eine Anforderung empfangen wird, bis eine Antwort an die anfordernde Person gesendet wird. Wenn Benutzer versuchen, mehr gleichzeitige Anforderungen zu stellen, als ihre Richtlinie zulässt, tritt beim erneuten Verbindungsversuch ein Fehler auf. Die bestehenden Verbindungen bleiben jedoch gültig. Einschränkungsrichtlinien können sich auf verschiedene Weise auf Parallelität auswirken.
  
Der **EWSMaxConcurrency** -Einschränkungsrichtlinienparameter legt die Anzahl der gleichzeitigen Verbindungen fest, die ein bestimmter Benutzer zur gleichen Zeit mit einem Exchange-Server haben kann. Um die maximal zuzulassende Anzahl gleichzeitiger Verbindungen zu bestimmen, betrachten Sie die Verbindungen, die von Outlook-Clients verwendet werden. Outlook 2007 und Outlook 2010 verwenden EWS zum Zugreifen auf Verfügbarkeits- und Abwesenheitsinformationen. Mac Outlook 2011 verwendet EWS für alle Clientzugriffsfunktionen. Abhängig von der Anzahl der Outlook-Clients, die aktiv eine Verbindung mit Postfach eines Benutzers herstellen, kann die Anzahl der für einen Benutzer verfügbaren gleichzeitigen Verbindungen beschränkt sein. Wenn Ihre Anwendung in einem einzigen Sicherheitskontext eine Verbindung mit mehreren Postfächern gleichzeitig herstellen muss, muss außerdem der Wert der **EWSMaxConcurrency** -Richtlinie berücksichtigt werden. Weitere Informationen über die Verwendung eines einzigen Sicherheitskontexts mit gleichzeitigen Verbindungen finden Sie unter [Einschränkungsüberlegungen für Anwendungen, die EWS-Identitätswechsel verwenden](http://msdn.microsoft.com/library/961f773a-8b8e-4b4f-a4b9-64305e107ca4.aspx#bk_ThrottlingConsiderations) weiter vorne in diesem Artikel. 
  
Anwendungen, die gleichzeitig Verbindungen mit mehreren Postfächer herstellen, müssen den Ressourceneinsatz auf Clientseite verfolgen können. Da EWS-Vorgänge anforderungs-/antwortbasiert sind, können Sie die ordnungsgemäße Funktion Ihrer Anwendungen innerhalb des **EWSMaxConcurrency** -Schwellenwerts sicherstellen, indem Sie die Anzahl der Verbindungen verfolgen, die zwischen dem Start einer Anforderung und dem Erhalt der Antwort stattfinden, und sicherstellen, dass höchstens zehn offene Anforderungen gleichzeitig vorliegen. 
  
Der **EWSFindCountLimit** -Richtlinienparameter gibt die maximale Ergebnisgröße an, die ein **FindItem** - oder **FindFolder** -Vorgang auf einem Clientzugriffsserver für einen Benutzer gleichzeitig verwenden kann. Wenn eine Anwendung (oder auch mehrere Anwendungen) zwei gleichzeitige EWS- **FindItem** -Anforderungen ausführt, die jeweils 100 Elemente für einen bestimmten Benutzer zurückgeben, wird für **EWSFindCountLimit** ein Wert von 200 auf das Budget des betreffenden Benutzers angerechnet. Wenn die Rückgabe der ersten Anforderung erfolgt, sinkt das Budget auf 100, und bei Rückgabe der zweiten Anforderung sinkt das Budget auf 0 (null). Wenn dieselbe Anwendung zwei gleichzeitige Anforderungen für 1000 Elemente ausführt, beträgt der Budgetwert 2000 Elemente, was den **EWSFindCountLimit** -Wert überschreitet. Wenn das Budget des Benutzers für Elemente unter null fällt, resultiert die nächste Anforderung in einem Fehler, bis das Budget des Benutzer wieder auf eins oder mehr aufgeladen wurde. 
  
## <a name="throttling-considerations-for-ews-notification-applications"></a>Einschränkungsüberlegungen für EWS-Benachrichtigungsanwendungen
<a name="bk_ThrottlingNotifications"> </a>

Wenn Sie EWS-Benachrichtigungsanwendungen erstellen, die Push-, Pull- oder Streamingbenachrichtigungen verwenden, müssen Sie die Auswirkungen der Einschränkungsrichtlinien **EWSMaxSubscriptions** und **EWSMaxConcurrency** sowie des **HangingConnectionLimit** berücksichtigen. 
  
Der **EWSMaxSubscriptions** -Richtlinienparameter definiert die maximale Anzahl an aktiven Push-, Pull- und Streamingabonnements, über die ein Benutzer auf einem bestimmten Clientzugriffsserver gleichzeitig verfügen kann. Dies wird je nach Exchange-Version anders budgetiert. Der Standardwert für diesen Parameter ist je nach Exchange-Version unterschiedlich. Mit der **SubscribeToAllFolders** -Eigenschaft kann ein Benutzer alle Ordner in einem Postfach abonnieren; hierbei wird ein einziges Abonnement auf das **EWSMaxSubscriptions** -Budget angerechnet. Benutzer können einzelne Ordner abonnieren, wobei jedes Ordnerabonnement auf das **EWSMaxSubscriptions** -Budget angerechnet wird, und zwar bis zu einem vom Wert des **EWSMaxSubscriptions** -Parameters festgelegten Grenzwert (Benutzer können z. B. 20 Kalenderordner in verschiedenen Postfächern abonnieren, wenn **EWSMaxSubscriptions** auf 20 festgelegt ist). 
  
Informationen zum Identitätswechsel und zum **EWSMaxSubscriptions** -Parameter finden Sie unter [Einschränkungsüberlegungen für Anwendungen, die EWS-Identitätswechsel verwenden](ews-throttling-in-exchange.md#bk_ThrottlingConsiderations) weiter vorne in diesem Artikel. 
  
Auch der **EWSMaxConcurrency** -Richtlinienparameter kann ein Problem für EWS-Benachrichtigungen darstellen. Beispiel: 
  
- Wenn EWS die Anzahl der Verbindungen für den Besitzer des Abonnements erhöht, während ein Pushabonnement eine Benachrichtigung generiert.
    
- Wenn eine Anwendung dafür entwickelt wurde, mehrere Benutzerpostfächer zu überwachen, und Benutzer gleichzeitige Benachrichtigungen für eine Instanz einer Nachricht erhalten, die an eine Verteilerliste gesendet wird.
    
Wenn die Benachrichtigungsanwendung eine Multithreadanwendung ist und gleichzeitige Verbindungsanforderungen ausführt, um mehr Informationen zu einer bestimmten Nachricht zu erhalten, die von einem Benutzerkonto empfangen wurde, kann der **EWSMaxConcurrency** -Richtliniengrenzwert überschritten werden. Um dies zu berücksichtigen, können Sie die gleichzeitigen Verbindungen in Ihrer Anwendung überwachen, einschließlich derjenigen, die möglicherweise vom Server verwendet werden, und Sie können Anforderungswarteschlangen auf dem Client implementieren. 
  
Der **HangingConnectionLimit** gilt nur für Streamingbenachrichtigungen. Dieser Grenzwert wird in der Datei "Web.config" festgelegt, was bedeutet, dass ein Exchange-Administrator diesen Wert auf einem lokalen Exchange-Server festlegen kann, aber Exchange Online-Postfächer den Standardwert für diesen Grenzwert (3 für Exchange Online und Exchange 2013) verwenden müssen. Weitere Informationen finden Sie unter [Welche Drosselung Werte muss ich berücksichtigen?](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling)
  
## <a name="throttling-policy-and-application-performance"></a>Einschränkungsrichtlinie und Anwendungsleistung
<a name="bk_PercentTimeIn"> </a>

Die folgenden drei Parameter der **PercentTimeIn** -Einschränkungsrichtlinie wirken sich auf die Zeitspanne aus, die eine ESW-Anwendung auf einem Clientzugriffsserver nutzen kann: 
  
- **EWSPercentTimeInAD**
    
- **EWSPercentTimeInCAS**
    
- **EWSPercentTimeInMailboxRPC**
    
Die in den **PercentTimeIn** -Richtlinienparametern angegebenen Werte geben die Zeitspanne an, die einem Thread zugewiesen wird, der eine Anforderung ausführt. Nehmen wir beispielweise für **EWSPercentTimeInCAS** den Wert 90 an. Wenn ein Prozess zwei gleichzeitige Anforderungen ausführt, die jeweils 54 Sekunden lang Code auf dem Clientzugriffsserver ausführen, verwendet der Prozess 108 Sekunden in einem 60-Sekunden-Fenster. Dies stellt einen **EWSPercentTimeInCAS** -Parameterwert von 180 Prozent dar. 
  
> [!NOTE]
> [!HINWEIS] Der **EWSPercentTimeInCAS** -Parameterwert ist eine überlappende Obermenge der Parameterwerte **EWSPercentTimeInAD** und **EWSPercentTimeInMailboxRPC**. Dies bedeutet, dass die Ausgaben für Verarbeitungszeit auf dem Clientzugriffsserver immer höher sein werden als die Ausgaben für **EWSPercentTimeInAD** und **EWSPercentTimeInMailboxRPC**. Dies liegt daran, dass die Exchange-Komponente nur dann einen Active Directory- oder RPC-Aufruf durchführen kann, wenn sie bereits Clientzugriffsserver-Code ausführt. Darüber hinaus laufen die Ausgaben für Verarbeitungszeit für **EWSPercentTimeInCAS** während der Ausführung von LDAP- oder RPC-Aufrufen weiter. Obwohl die Anforderung möglicherweise synchron auf eine Antwort von Active Directory Domain Services (AD DS) oder dem Exchange-Informationsspeicher wartet, verbraucht der Prozess trotzdem einen Thread auf dem Server, daher sollte dem Thread diese Nutzung in Rechnung gestellt werden. 
  
Die von einer Anwendung innerhalb eines 60-Sekunden-Zeitraums genutzte CPU-Zeit überschreitet diese Einschränkungsgrenzwerte möglicherweise; daher ist es wichtig, den Umfang und die Art der gestellten Anforderungen zu berücksichtigen. Beispielsweise kann ein großer Batch gleichzeitig ausgeführter **ResolveNames** -Vorgänge den Wert des **EWSPercentTimeInAD** -Richtlinienparameters überschreiten. Die in der standardmäßigen Einschränkungsrichtlinie enthaltenen Richtlinienwerte sind so festgelegt, dass sie die problemlose Funktion der meisten EWS-Anwendungen erlauben; wenn jedoch umfangreiche Multithreadanwendungen sehr viele Anforderungen an einen bestimmten Clientzugriffsserver stellen, kann dies zu Problemen führen. Um dies zu vermeiden, können Sie die Größe der auf dem Server ausgeführten Batches beschränken. 
  
## <a name="throttling-policies-and-applications-that-send-a-large-volume-of-email"></a>Einschränkungsrichtlinien und Anwendungen mit hohem E-Mail-Versandvolumen
<a name="bk_RateLimits"> </a>

Die standardmäßigen Einschränkungsrichtlinien enthalten drei Richtlinienparameter zur Ratenbegrenzung, die Auswirkungen auf Anwendungen haben können, die EWS zum Senden einer großen Anzahl von Nachrichten oder zum Senden von Nachrichten in großen Batches innerhalb kurzer Zeit nutzen. 
  
> [!NOTE]
> [!HINWEIS] Im Allgemeinen wird empfohlen, EWS nicht für den Massenversand von E-Mail-Nachrichten einzusetzen. Verwenden Sie einen SMTP-Host, der auf Massen-E-Mail-Dienste spezialisiert ist, wenn Sie häufig einen Massenversand großer E-Mail-Nachrichten durchführen. 
  
Der **MessageRateLimit** -Richtlinienparameter gibt die Anzahl der Nachrichten pro Minute an, die von einem beliebigen Exchange-Client wie z. B. EWS gesendet werden können. Standardmäßig ist diese Richtlinie auf 30 Nachrichten pro Minute festgelegt. Für normale Benutzer ist dies in der Regel ausreichend. Bei Anwendungen, die große Batches mit E-Mail-Nachrichten senden, z. B. als Teil eines Fakturierungsprogramms, können jedoch Probleme auftreten. Wenn dieser Richtliniengrenzwert überschritten wird, wird die Nachrichtenübermittlung für das Postfach verzögert. Insbesondere kann es passieren, dass Nachrichten für einen längeren Zeitraum im Ordner "Postausgang" oder "Entwürfe" angezeigt werden, wenn ein Benutzer oder eine Anwendung eine größere Anzahl von Nachrichten sendet, als vom Wert des **MessageRateLimit** -Parameters angegeben. Achten Sie darauf, dass Sie diesen Aspekt bei der Entwicklung eines Übermittlungsverfolgungssystems berücksichtigen, insbesondere, wenn die Anwendung ein Postfach verwendet, mit dem sich Benutzer über Outlook verbinden. Wenn verzögerte Elemente im Ordner "Postausgang" oder "Entwürfe" gespeichert werden, können Benutzer dies als Fehler interpretieren. 
  
Der **RecipientRateLimit** -Richtlinienparameter gibt den Grenzwert für die Anzahl von Empfängern an, die ein Benutzer in einem Zeitraum von 24 Stunden adressieren darf. Wenn dieser Wert auf 500 festgelegt ist, bedeutet dies beispielsweise, dass ein einzelnes Exchange-Postfachkonto Nachrichten an maximal 500 Empfänger pro Tag senden darf. Dieser Grenzwert gilt für Nachrichten an Empfänger innerhalb und außerhalb der Organisation. Dieser Standardgrenzwert verursacht möglicherweise Probleme bei einigen Branchenanwendungen, die Rechnungsläufe am Monatsende ausführen und Nachrichten an mehr als diese Anzahl von Empfängern senden müssen. Sie können externe Dienste verwenden, die die Batchverarbeitung von Nachrichten ermöglichen, oder separate lokale ausgehende Relaylösungen, um diese Einschränkung zu umgehen. 
  
Der **ForwardeeLimit** -Richtlinienparameter gibt die maximale Anzahl von Empfängern an, an die Nachrichten mithilfe von Posteingangsregeln weitergeleitet oder umgeleitet werden können. Dieser Parameter beschränkt nicht die Anzahl der Nachrichten, die an die Empfänger weitergeleitet oder umgeleitet werden können. 
  
## <a name="errors-generated-when-throttling-limits-are-exceeded"></a>Bei Überschreitung von Einschränkungsgrenzwerten generierte Fehler
<a name="bk_ThrottlingErrors"> </a>

Wenn Einschränkungsrichtlinien überschritten werden, generiert EWS einen der in der folgenden Tabelle aufgeführten Fehler.
  
**Tabelle 3: Fehler bei Überschreitung von Einschränkungsgrenzwerten**

|**Fehler**|**Einschränkungsrichtlinienparameter**|**Beschreibung**|
|:-----|:-----|:-----|
|ErrorExceededConnectionCount  <br/> |**EWSMaxConcurrency** <br/> |Gibt an, dass mehr gleichzeitige Anforderungen an den Server gestellt werden, als die Richtlinie des Benutzers zulässt.  <br/> |
|ErrorExceededSubscriptionCount  <br/> |**EWSMaxSubscriptions** <br/> |Gibt an, dass die maximale Abonnementanzahl für Richtlinieneinschränkungen eines Benutzers überschritten wurde.  <br/> |
|ErrorExceededFindCountLimit  <br/> |**EWSFindCountLimit** <br/> |Gibt an, dass ein Suchvorgangsaufruf die Gesamtzahl der Elemente überschritten hat, die zurückgegeben werden können.  <br/> |
|ErrorServerBusy  <br/> |**EWSPercentTimeInMailboxRPC** **EWSPercentTimeInCAS** **EWSPercentTimeInAD**                   <br/> |Tritt auf, wenn der Server ausgelastet ist. Der mit ErrorServerBusy-Fehlern zurückgegebene BackOffMilliseconds-Wert gibt an, wie lange der Client warten muss, bevor die Anforderung erneut gesendet werden kann, für deren Antwort dieser Fehlercode zurückgegeben wurde.  <br/> |
   
Die folgende Tabelle enthält die HTTP-Statuscodes, die von Einschränkungsfehlern zurückgegeben werden.
  
**Tabelle 4: Von Einschränkungsfehlern zurückgegebene HTTP-Statuscodes**

|**HTTP-Statuscode**|**Beschreibung**|
|:-----|:-----|
|HTTP 503  <br/> |Gibt an, dass EWS-Anforderungen bei IIS in der Warteschlange stehen. Der Client sollte das Senden weiterer Anforderungen auf einen späteren Zeitpunkt verschieben.  <br/> |
|HTTP 500  <br/> |Zeigt einen internen Fehler mit dem ErrorServerBusy-Fehlercode an. Dies weist darauf hin, dass der Client das Senden weiterer Anforderungen auf einen späteren Zeitpunkt verschieben sollte. Die Antwort enthält möglicherweise einen Backoff-Hinweis namens BackOffMilliseconds. Falls vorhanden, verwenden Sie den Wert von BackOffMilliseconds als die Zeitspanne, die der Client bis zum erneuten Senden einer Anforderung wartet.  <br/> |
|HTTP 200  <br/> |Enthält eine auf dem EWS-Schema basierende Fehlerantwort mit einem ErrorInternalServerError-Fehlercode. Ein interner ErrorServerBusy-Fehlercode kann vorhanden sein. Dies weist darauf hin, dass der Client das Senden weiterer Anforderungen auf einen späteren Zeitpunkt verschieben sollte.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Verwaltung von Exchange-Arbeitsauslastungen](http://technet.microsoft.com/en-us/library/jj150503.aspx)
- [New-ThrottlingPolicy-Cmdlet](http://technet.microsoft.com/en-us/library/dd351045.aspx)
- [Grundlegendes zu Clienteinschränkungsrichtlinien](http://technet.microsoft.com/en-us/library/dd297964.aspx)
- [ThrottlingPolicy-Klasse](http://msdn.microsoft.com/en-us/library/ff342496%28v=EXCHG.140%29.aspx)
- [Einschränkungsrichtlinie und EWSFindCountLimit](http://blogs.msdn.com/b/exchangedev/archive/2010/03/12/throttling-policies-and-the-ewsfindcountlimit.aspx)
- [Budgetmomentaufnahmen in den IIS-Protokollen](http://blogs.msdn.com/b/exchangedev/archive/2010/03/10/budget-snapshots-in-the-iis-logs.aspx)
- [Auswirkung der Einschränkung Ihrer Bereitstellung in Exchange 2010 SP1](http://msexchangeteam.com/archive/2010/08/27/456040.aspx)
- [Einschränkungsrichtlinienzuordnungen in Exchange 2010 SP1](http://msexchangeteam.com/archive/2010/08/02/455707.aspx)
- [Einschränkungsrichtlinien und CPUStartPercent](http://blogs.msdn.com/b/exchangedev/archive/2010/03/11/throttling-policies-and-cpustartpercent.aspx)
- [Identitätswechsel und EWS in Exchange](impersonation-and-ews-in-exchange.md)
    

