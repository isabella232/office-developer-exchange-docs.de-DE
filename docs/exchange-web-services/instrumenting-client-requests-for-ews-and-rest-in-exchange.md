---
title: Instrumentation Clientanforderungen für EWS und REST in Exchange
manager: sethgros
ms.date: 4/13/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 330de503-498d-447e-b4a9-c20fc1699fd1
description: Informationen Sie zu den HTTP-Headern EWS und REST-Anforderungen und-Antworten, mit die Hilfe Sie die Überwachung und Problembehandlung von Exchange-Anwendung.
ms.openlocfilehash: bcf362952c29956729c44397043a56bf3603d0af
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757026"
---
# <a name="instrumenting-client-requests-for-ews-and-rest-in-exchange"></a>Instrumentation Clientanforderungen für EWS und REST in Exchange

Informationen Sie zu den HTTP-Headern EWS und REST-Anforderungen und-Antworten, mit die Hilfe Sie die Überwachung und Problembehandlung von Exchange-Anwendung.
  
Ist dies jemals Ihnen passiert? Ein Benutzer Ihre Anwendung meldet ist ein unerwarteten Fehler. Sie untersuchen möchten, aber Sie können nicht reproduzieren. Der Fehler ist verschwunden für den Benutzer, und mit wenig bearbeitungsfähige Daten übrig. Welche Suchaktionen? Sehen wir uns wie Sie proaktiv für dieses Szenario vorbereiten und hoffentlich Frustration in Zukunft vermeiden können.
  
## <a name="add-instrumentation-to-requests"></a>Hinzufügen von Instrumentation zu Anfragen

Es wird empfohlen, dass Sie Ihre Anforderungen an die Problembehandlung zu vereinfachen zusätzliche HTTP-Headern hinzufügen. Sie sollten diese Informationen, die sich irgendwo (beispielsweise in einer Protokolldatei) festzuhalten, damit Sie sie bei Bedarf später abrufen können. Dies ist hilfreich, wenn der Netzwerkdatenverkehr zu untersuchen und sind ebenfalls hilfreich, wenn Sie Microsoft-Supportmitarbeiter kontaktieren.
  
**In Tabelle 1. Anforderungsheader für die Problembehandlung**

|**HTTP-Header (EWS)**|**EWS Managed-API-Entsprechung**|**Anmerkungen**|
|:-----|:-----|:-----|
|Benutzer-Agent  <br/> |[ExchangeService.UserAgent](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.useragent%28v=exchg.80%29.aspx) <br/> |Legen Sie den ein eindeutiger Wert, der die Clientanwendung identifiziert.<br/><br/> Verwenden den gleichen Wert für alle Anfragen, die Ihre Anwendung sendet Microsoft zur Problembehandlung für Fehler beim Aufrufen können, sollten diese auftreten.  <br/> |
|Client-Anforderung-id  <br/> |[ExchangeService.ClientRequestId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.clientrequestid%28v=exchg.80%29.aspx) <br/> |Legen Sie dies auf einen anderen eindeutigen Wert für jede Anforderung, die Ihre Anwendung sendet.<br/><br/> Es wird empfohlen, eine GUID zu verwenden. Diese eindeutige ID soll verwendet werden, um Aktivitäten zwischen zwei Systemen korrelieren, falls ein Fehler auftritt.  <br/> |
|Return-Client-Anforderung-id  <br/> |[ExchangeService.ReturnClientRequestId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.returnclientrequestid%28v=exchg.80%29.aspx) <br/> |Legen Sie dies auf **true fest,** auf dem Exchange-Server zu signalisieren, dass den Wert der Ihrer Client-Anforderung-Id in der entsprechenden Antwort zurückgegeben werden soll.<br/><br/> Dadurch können Sie die Anforderungen und Antworten in netzwerkablaufverfolgung oder EWS Managed API Spuren korrelieren.  <br/> |
|X-ClientStatistics  <br/> |[ExchangeService.SendClientLatencies](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.sendclientlatencies%28v=exchg.80%29.aspx) <br/> |Verwendet, um [EWS Wartezeiten von Bericht](#bk_ReportLatency) an Microsoft, wenn die Anwendung Exchange Online oder Exchange Online als Teil von Office 365 zugreift.  <br/> |
   
## <a name="log-information-from-responses"></a>Protokollinformationen von Antworten

Ebenso wie Ihrer Client zusätzliche Instrumentation auf die Anforderungen, die es sendet hinzufügen kann, wird die Antworten in Form von HTTP-Headern von Exchange zusätzliche Instrumentation hinzugefügt. Der Client sollte diese Informationen sowie die Instrumentation Anforderungsinformationen wechseln erfassen.
  
> [!NOTE]
> Wenn Sie die EWS Managed API verwenden, gibt es keine direkte Entsprechung für die HTTP-Header. Alle HTTP-Antwortheader können jedoch über die [ExchangeService.HttpResponseHeaders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.httpresponseheaders%28v=exchg.80%29.aspx) -Eigenschaft zugegriffen werden. 
  
**In Tabelle 2. HTTP-Antwortheader**

|**HTTP-header**|**Beschreibung**|
|:-----|:-----|
|Anforderung-id  <br/> |Ein Server generierte ID für die Anforderung, die dieser Antwort entspricht.  <br/> |
|Client-Anforderung-id  <br/> |Der Wert der Client-Anforderung-Id-Header in der Anforderung.<br/><br/> Diese Kopfzeile ist nur vorhanden, wenn die Anforderung die Kopfzeile Return-Client-Anforderung-Id mit dem Wert **true**enthält.  <br/> |
|X-FEServer  <br/> |Der FQDN des Clientzugriffs-Server, der die Anforderung verarbeitet.  <br/> |
|X-TargetBEServer  <br/> |Der FQDN des Postfachservers an, die die Anforderung verarbeitet.  <br/> |
|X-DiagInfo  <br/> |Zusätzliche Diagnoseinformationen, je nach der Anforderung.  <br/> |
|X-ms-diagnostics  <br/> | Diese Kopfzeile ist nur anwendbar, wenn OAuth-Authentifizierung in der Anforderung verwendet wird.<br/><br/> Es enthält einen expliziten Fehlercode, der angibt, warum eine OAuth-Authentifizierung fehlgeschlagen ist.<br/><br/> Es dauert das folgende Format:`errorId;reason="reason"error_type="error type"`<br/><br/> Das Feld **Grund** ist eine lesbare Beschreibung des Fehlers.<br/><br/> Das **Fehler-ID** -Feld ist eine ganze Zahl und der **Fehler\_Typ** Feld ist die Zeichenfolgendarstellung, Integer, wie folgt:<ul><li>2000000: Ungültige\_Signatur</li><li>2000001: Ungültige\_token</li><li>  2000002: token\_abgelaufen</li><li>2000003: Ungültige\_Ressource</li><li>2000004: Ungültige\_Mandanten  </li><li>2000005: Ungültige\_Benutzer</li><li>2000006: Ungültige\_Client</li><li>2000007: interne\_Fehler</li><li>2000008: Ungültige\_erteilen</li></ul> |
   
## <a name="report-ews-latency-to-microsoft"></a>Bericht EWS Wartezeit an Microsoft
<a name="bk_ReportLatency"> </a>

Wenn die Anwendung die EWS Managed API oder EWS Verbindung zu Exchange Online verwendet, können Sie die Wartezeit in EWS-Anforderungen direkt an Microsoft melden. Die Informationen werden über den X-ClientStatistics Anforderungsheader übergeben. Wenn Sie die EWS Managed API verwenden, haben Sie führen die [ExchangeService.SendClientLatencies](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.sendclientlatencies%28v=exchg.80%29.aspx) -Eigenschaft auf **true**festgelegt ist. Wenn Sie Exchange-Webdienste verwenden, müssen Sie die Zeit zwischen eine Anforderung und Empfangen einer Antwort zu messen, fügen Sie der Kopfzeile X ClientStatistics auf die nächste EWS-Anforderung, die Ihre Anwendung sendet, verwenden das folgende Format.
  
`X-ClientStatistics: MessageId=<value of request-id header>,ResponseTime=<time in milliseconds>,SoapAction=<EWS operation>`
  
Wir Berichte für diese Wartezeiten verwalten und deren Verwendung EWS-Dienste in Exchange Online kontinuierlich verbessern.
  
## <a name="next-steps"></a>Nächste Schritte
<a name="bk_ReportLatency"> </a>

Nachdem Sie Ihre Anwendung Client Instrumentation hinzugefügt haben, sind Sie besser vorbereitet haben, falls ein Fehler auftritt. In diesem Fall können Sie Ihre Instrumentationsdaten für die [Problembehandlung bei der Anwendung](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)verwenden.
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)
- [TRACE-Anfragen und-Antworten EWS Managed API behandeln](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
- [Tools und Ressourcen für die Problembehandlung bei EWS-Anwendungen für Exchange](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

