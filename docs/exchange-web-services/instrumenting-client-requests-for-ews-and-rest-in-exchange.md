---
title: Handhaben von Clientanforderungen für EWS und REST in Exchange
manager: sethgros
ms.date: 4/13/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 330de503-498d-447e-b4a9-c20fc1699fd1
description: Erfahren Sie mehr über die HTTP-Header in EWS- und REST-Anforderungen und -Antworten, die Ihnen bei der Überwachung und Problembehandlung ihrer Exchange-Anwendung helfen können.
ms.openlocfilehash: f32a164436a1f8ab06192e71a287f5092fe9a6c4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520990"
---
# <a name="instrumenting-client-requests-for-ews-and-rest-in-exchange"></a>Handhaben von Clientanforderungen für EWS und REST in Exchange

Erfahren Sie mehr über die HTTP-Header in EWS- und REST-Anforderungen und -Antworten, die Ihnen bei der Überwachung und Problembehandlung ihrer Exchange-Anwendung helfen können.
  
Ist Ihnen dies jemals passiert? Ein Benutzer Ihrer Anwendung meldet einen unerwarteten Fehler. Sie möchten dies untersuchen, können sie jedoch nicht reproduzieren. Der Fehler ist für den Benutzer nicht mehr vorhanden, und Sie haben nur sehr wenige Aktionen erfordernde Daten. Frustrierend, oder? Sehen wir uns an, wie Sie sich proaktiv auf dieses Szenario vorbereiten und in Zukunft hoffentlich Frustration vermeiden können.
  
## <a name="add-instrumentation-to-requests"></a>Hinzufügen von Instrumentierung zu Anforderungen

Es wird empfohlen, zusätzliche HTTP-Header zu Ihren Anforderungen hinzuzufügen, um die Problembehandlung zu vereinfachen. Sie sollten diese Informationen an einer bestimmten Stelle (z. B. in einer Protokolldatei) aufzeichnen, damit Sie sie später bei Bedarf abrufen können. Dies ist hilfreich, wenn Sie den Netzwerkdatenverkehr untersuchen, und ist auch hilfreich, wenn Sie sich an den Microsoft-Support wenden, um Unterstützung zu erhalten.
  
**Tabelle 1. Anforderungsheader für die Problembehandlung**

|**HTTP-Header (EWS)**|**Entsprechung in der verwalteten EWS-API**|**Hinweise**|
|:-----|:-----|:-----|
|User-Agent  <br/> |[ExchangeService.UserAgent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.useragent%28v=exchg.80%29.aspx) <br/> |Legen Sie dies auf einen eindeutigen Wert fest, der Ihre Clientanwendung identifiziert.<br/><br/> Wenn Sie denselben Wert für alle Anforderungen verwenden, die Ihre Anwendung sendet, kann Microsoft bei der Problembehandlung von Anruffehlern helfen, falls diese auftreten.  <br/> |
|Clientanforderungs-ID  <br/> |[ExchangeService.ClientRequestId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.clientrequestid%28v=exchg.80%29.aspx) <br/> |Legen Sie für jede Anforderung, die Ihre Anwendung sendet, einen anderen eindeutigen Wert fest.<br/><br/> Es wird empfohlen, eine GUID zu verwenden. Dieser eindeutige Bezeichner soll verwendet werden, um Aktivitäten zwischen zwei Systemen im Falle eines Fehlers zu korrelieren.  <br/> |
|return-client-request-id  <br/> |[ExchangeService.ReturnClientRequestId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.returnclientrequestid%28v=exchg.80%29.aspx) <br/> |Legen Sie diesen Wert auf **"true"** fest, um dem Exchange Server zu signalisieren, dass er den Wert Ihrer Clientanforderungs-ID in der entsprechenden Antwort zurückgeben soll.<br/><br/> Sie können dies verwenden, um Anforderungen und Antworten in Netzwerkablaufverfolgungen oder EWS Managed API-Ablaufverfolgungen zu korrelieren.  <br/> |
|X-ClientStatistics  <br/> |[ExchangeService.SendClientLatencies](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.sendclientlatencies%28v=exchg.80%29.aspx) <br/> |Wird verwendet, um [EWS-Latenzen](#bk_ReportLatency) an Microsoft zu melden, wenn Ihre Anwendung im Rahmen Office 365 auf Exchange Online oder Exchange Online zugreift.  <br/> |
   
## <a name="log-information-from-responses"></a>Protokollieren von Informationen aus Antworten

Ebenso wie Ihr Client den gesendeten Anforderungen zusätzliche Instrumentierung hinzufügen kann, fügt Exchange den Antworten zusätzliche Instrumentierung in Form von HTTP-Headern hinzu. Ihr Client sollte diese Informationen erfassen, um die Informationen der Anforderungsinstrumentation zu erfassen.
  
> [!NOTE]
> Wenn Sie die verwaltete EWS-API verwenden, gibt es keine direkte Entsprechung für die HTTP-Header. Auf alle HTTP-Antwortheader kann jedoch über die [ExchangeService.HttpResponseHeaders-Eigenschaft](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.httpresponseheaders%28v=exchg.80%29.aspx) zugegriffen werden. 
  
**Tabelle 2. HTTP-Antwortheader**

|**HTTP-Header**|**Beschreibung**|
|:-----|:-----|
|Anforderungs-ID  <br/> |Eine servergenerierte ID für die Anforderung, die dieser Antwort entspricht.  <br/> |
|Clientanforderungs-ID  <br/> |Der Wert des Headers "client-request-id" in der Anforderung.<br/><br/> Dieser Header ist nur vorhanden, wenn die Anforderung den Header "return-client-request-id" mit dem Wert **"true"** enthält.  <br/> |
|X-FEServer  <br/> |Der FQDN des Clientzugriffsservers, der die Anforderung verarbeitet hat.  <br/> |
|X-TargetBEServer  <br/> |Der FQDN des Postfachservers, der die Anforderung verarbeitet hat.  <br/> |
|X-DiagInfo  <br/> |Zusätzliche Diagnoseinformationen, je nach Anforderung.  <br/> |
|x-ms-diagnostics  <br/> | Dieser Header gilt nur, wenn die OAuth-Authentifizierung in der Anforderung verwendet wird.<br/><br/> Es enthält einen expliziten Fehlercode, der angibt, warum eine OAuth-Authentifizierung fehlgeschlagen ist.<br/><br/> Es hat das folgende Format: `errorId;reason="reason"error_type="error type"`<br/><br/> Das **Grundfeld** ist eine lesbare Beschreibung des Fehlers.<br/><br/> Das **ErrorId-Feld** ist eine ganze Zahl, und das **\_ Fehlertypfeld** ist die Zeichenfolgendarstellung dieser ganzen Zahl, wie folgt:<ul><li>2000000: Ungültige \_ Signatur</li><li>2000001: ungültiges \_ Token</li><li>  2000002: Token \_ ist abgelaufen</li><li>2000003: ungültige \_ Ressource</li><li>2000004: ungültiger \_ Mandant  </li><li>2000005: ungültiger \_ Benutzer</li><li>2000006: ungültiger \_ Client</li><li>2000007: interner \_ Fehler</li><li>2000008: ungültige \_ Erteilung</li></ul> |
   
## <a name="report-ews-latency-to-microsoft"></a>Melden der EWS-Latenz an Microsoft
<a name="bk_ReportLatency"> </a>

Wenn Ihre Anwendung die verwaltete EWS-API oder EWS zum Herstellen einer Verbindung mit Exchange Online verwendet, können Sie die Latenz in EWS-Anforderungen direkt an Microsoft melden. Die Informationen werden über den X-ClientStatistics-Anforderungsheader übergeben. Wenn Sie die verwaltete EWS-API verwenden, müssen Sie nur die [ExchangeService.SendClientLatencies-Eigenschaft](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.sendclientlatencies%28v=exchg.80%29.aspx) auf **"true"** festlegen. Wenn Sie EWS verwenden, müssen Sie die Zeit zwischen dem Ausgeben einer Anforderung und dem Empfangen einer Antwort messen und dann den X-ClientStatistics-Header zur nächsten EWS-Anforderung hinzufügen, die Ihre Anwendung mit dem folgenden Format sendet.
  
`X-ClientStatistics: MessageId=<value of request-id header>,ResponseTime=<time in milliseconds>,SoapAction=<EWS operation>`
  
Wir verwalten Berichte für diese Latenzen und verwenden sie, um EWS-Dienste in Exchange Online kontinuierlich zu verbessern.
  
## <a name="next-steps"></a>Nächste Schritte
<a name="bk_ReportLatency"> </a>

Nachdem Sie Ihrer Anwendung die Client-Instrumentierung hinzugefügt haben, sind Sie besser vorbereitet, wenn ein Fehler auftritt. In diesem Fall können Sie ihre Instrumentierungsdaten verwenden, um Probleme mit der Anwendung zu [beheben.](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)
- [Ablaufverfolgungsanforderungen und -antworten zur Problembehandlung bei EWS-verwalteten API-Anwendungen](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
- [Tools und Ressourcen für die Problembehandlung bei EWS-Anwendungen für Exchange](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

