---
title: Tools und Ressourcen für die Problembehandlung EWS-Anwendungen für Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ee7fcd05-35d7-47bf-bac4-e719c49c11fe
description: Hier finden Sie Ressourcen, die die EWS Managed API oder EWS-Anwendung zu beheben.
ms.openlocfilehash: d8d8ea736ca3b896642ad06f5987caeba8d8d059
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757131"
---
# <a name="tools-and-resources-for-troubleshooting-ews-applications-for-exchange"></a>Tools und Ressourcen für die Problembehandlung EWS-Anwendungen für Exchange

Hier finden Sie Ressourcen, die die EWS Managed API oder EWS-Anwendung zu beheben.
  
Dinge gehen Sie nicht immer wie geplant. In einigen Fällen EWS fordert Fail oder unerwartete Ergebnisse bereitstellen. Dies kann insbesondere dann, wenn der Grund nicht offensichtlich ist frustrierend sein. Hoffentlich dies nie geschieht Ihnen, aber wenn dies der Fall ist, wird dieser Artikel enthält Informationen zu Tools und Ressourcen, die Sie zur Behebung des Problems verwenden können.
  
> [!NOTE]
> Dieser Artikel enthält allgemeine Hinweise zur Fehlerbehebung und Quellen Informationen zur Problembehandlung. Leider ist es nicht möglich, geben Sie ausführliche Schritte zur Problembehandlung. Unterstützung bei Problemen mit einen bestimmten Fehler finden Sie unter [Nächste Schritte](#bk_NextSteps). 
  
## <a name="examine-the-soap-requests-and-responses"></a>Überprüfen Sie die SOAP-Anforderungen und Antworten

Wenn Dinge nicht ordnungsgemäß funktionieren, sollten sie wirklich sehen, was passiert, werden ignoriert. Die erste Zeile des Anfrage beim Untersuchen von Problemen mit EWS oder die EWS Managed API besteht darin, untersuchen Sie die Anforderungen, die Ihre Anwendung über das Netzwerk sendet und die Antworten, die der Server, zurück sendet.
  
Die EWS Managed API erleichtert untersuchen SOAP-Anforderungen und-Antworten mit seiner [Ablaufverfolgungsfunktionen integriert](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md). Wenn Sie Exchange-Webdienste verwenden, möglicherweise oder möglicherweise keinen Zugriff auf ähnliche Funktionalität Tracing, je nachdem, welche Plattform oder Klassen, die Sie verwenden, um Ihre Anforderungen zu senden. Sie können jedoch immer ein Tool zur netzwerkablaufverfolgung wie [Netzwerkmonitor](http://www.microsoft.com/en-us/download/details.aspx?id=4865) oder [Fiddler](http://www.telerik.com/fiddler) verwenden, zum Überprüfen des Netzwerkverkehrs und die Anfrage und-Antwort Nutzlast anzeigen. 
  
Darüber hinaus können Sie [Ihre Clientanforderungen Instrumentieren](instrumenting-client-requests-for-ews-and-rest-in-exchange.md) zum Verbessern der Informationen in Anforderungen und Antworten zur Verfügung. 
  
Nachdem Sie die Anforderungen und Antworten haben, sollten Sie sich Folgendes: Suchen sie richtige? Sind die Werte, die die Anwendung erwartet senden? Führen Sie die Antworten sinnvoll?
  
## <a name="examine-error-codes"></a>Untersuchen von Fehlercodes

In einigen Fällen kann der Fehlercode entscheidend Ermittlung des Problems wechseln, auch wenn auf den ersten Blick erscheint es nicht sinnvoll. Angibt der Fehler, dass es sich bei Ihrem Client [gedrosselt](ews-throttling-in-exchange.md)wird? Möglicherweise ist ein Aufruf von AutoErmittlung [Konfigurationsinformationen](how-to-refresh-configuration-information-by-using-autodiscover.md) aktualisiert in Reihenfolge? 
  
Weitere Informationen zu bestimmten Fehlerbehandlung finden Sie unter den folgenden Artikeln:
  
- [Behandeln von AutoErmittlungs-Fehlermeldungen](handling-autodiscover-error-messages.md)
    
- [Fehlerbehandlung Benachrichtigung-bezogene in EWS in Exchange](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [Fehlerbehandlung Synchronisierung-bezogene in EWS in Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [Fehlerbehandlung Löschung-bezogene in EWS in Exchange](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="verify-versions"></a>Überprüfen der Versionen

Eine Vielzahl von verschiedenen Komponenten EWS-Vorgänge beteiligt, und die Versionen dieser Komponenten können die Ergebnisse beeinflussen.
  
**In Tabelle 1. Mit Versionsangabe Komponenten, die EWS-Prozesse auswirken können**

|**Komponente**|**EWS Managed API**|**EWS**|**Anmerkungen**|
|:-----|:-----|:-----|:-----|
|Angeforderte Serverversion  <br/> |[ExchangeServiceBase.RequestedServerVersion](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx) -Eigenschaft  <br/> |[RequestServerVersion](http://msdn.microsoft.com/library/af4032d5-42b3-463e-9d0a-8236d78e5b75%28Office.15%29.aspx) -element  <br/> |Dieser Wert steuert, welche Version des Schemas EWS zum Verarbeiten der EWS-Anforderung verwendet wird. Stellen Sie sicher, dass die hier angegebene Schemaversion ist sinnvoll für die Anforderung, dass Sie senden. Einige Eigenschaften und Vorgänge sind nicht verfügbar in früheren Versionen des Schemas.  <br/> |
|Die Server-version  <br/> |[ExchangeServiceBase.ServerInfo](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.exchangeservicebase.serverinfo%28v=exchg.80%29.aspx) -Eigenschaft  <br/> |[ServerVersionInfo](http://msdn.microsoft.com/library/c04a6872-ca27-432b-aac2-36b023d0afc6%28Office.15%29.aspx) -element  <br/> |Dieser Wert wird vom Server in EWS Antworten zurückgegeben, und gibt die Version des Servers, der die Antwort verarbeitet. Stellen Sie sicher, dass dieser Wert ist, was Sie erwartet. Wenn möglich, stellen Sie sicher, dass der Exchange-Server die letzte Aktualisierung für Ihre Hauptversion von Exchange ausgeführt wird.  <br/> |
|Die Version EWS Managed API  <br/> |Die Produkt-Version-Eigenschaft der Microsoft.Exchange.WebServices.dll-Datei.  <br/> |Nicht zutreffend  <br/> |Wenn Sie die EWS Managed API verwenden, stellen Sie sicher, dass Sie [die aktuellste Version](http://aka.ms/ews-managed-api-readme)verwenden.  <br/> |
   
## <a name="verify-access"></a>Überprüfen des Zugriffs

EWS wird von [Standardwerte können geändert werden](how-to-control-access-to-ews-in-exchange.md), aber standardmäßig aktiviert. Verwenden Sie das Cmdlet [Get-OrganizationConfig](http://technet.microsoft.com/en-us/library/bb124754.aspx) , um sicherzustellen, dass der Exchange-Webdienste auf dem Server aktiviert ist und das Cmdlet [Get-CASMailbox](http://technet.microsoft.com/en-us/library/aa997571.aspx) , um sicherzustellen, dass der Exchange-Webdienste für das Postfach des Benutzers aktiviert ist. Überprüfen Sie auch beide Cmdlet Antworten für ein EWS zulassen oder Blockierliste, und stellen Sie sicher, dass die Anwendung aus mithilfe der Exchange-Webdienste nicht gesperrt. 
  
Sie sollten Sie außerdem sicher, dass die [Standardeinstellungen für die Authentifizierung](http://technet.microsoft.com/en-us/library/gg247612%28v=exchg.150%29.aspx) für das virtuelle EWS-Verzeichnis nicht geändert wurden. 
  
## <a name="try-another-ews-client"></a>Versuchen Sie es einem anderen EWS-client

In einigen Fällen ist es hilfreich, versuchen Sie es der gleichen Anforderung von einem anderen Client und die Ergebnisse verglichen. Wenn ein anderer Client unterschiedliche Ergebnisse Ruft, was anderen ist? Herauszufinden, was zwischen einer erfolgreichen Anforderung und eine fehlerhafte Anforderung unterscheidet helfen wird erläutert, warum eine bestimmte Anforderung Fehler aufgetreten ist.
  
Während Sie einen anderen Client zum Testen sicherlich schreiben können, müssen Sie nicht auf! [EWSEditor](http://ewseditor.codeplex.com/) ist ein Beispielclient, der die EWS Managed API und EWS verwendet. Sie können den Client (einschließlich des Quellcodes) herunterladen und verwenden, um die gleichen Anforderungen, die in der Anwendung ein Fehler auftritt, versuchen Sie es. 
  
## <a name="examine-iis-logs"></a>Untersuchen Sie die IIS-Protokolle

Wenn Sie Zugriff auf den Exchange-Server verfügen, kann die Protokollierung Funktionalität von Internetinformationsdienste (Internet Information Services, IIS) auf den Clientzugriffsservern Weitere Informationen zu Fehlern bereitstellen. Denken Sie daran, die IIS-Protokolle nur werden jedoch nützlich, wenn Sie einen HTTP-Fehler erhalten.
  
IIS bietet zwei verschiedene Protokollierungsmethoden: [IIS-Protokollierung](http://www.iis.net/learn/manage/provisioning-and-managing-iis/configure-logging-in-iis) und [tracing gescheiterten Anforderungen](http://www.iis.net/learn/troubleshoot/using-failed-request-tracing/troubleshooting-failed-requests-using-tracing-in-iis). Für die Verwendung mit IIS-Protokolle können Sie [Log Parser Studio](http://blogs.technet.com/b/exchange/archive/2012/03/07/introducing-log-parser-studio.aspx), die eine Anzahl von integrierten EWS-Abfragen enthält.
  
## <a name="next-steps"></a>Nächste Schritte
<a name="bk_NextSteps"> </a>

Nun, dass Sie über die Tools und Ressourcen, die Sie verwenden können, für die Problembehandlung bei gelernt haben, sollten Sie Hilfe beim Verständnis der Metriken aufgelistet, die diese Tools. Im folgenden sind einige Optionen zum Anzeigen der Hilfe:
  
- [Exchange Server-Entwicklerforum auf MSDN](http://social.msdn.microsoft.com/Forums/en-US/home?category=exchangeserver) – stellen Sie eine Frage der MSDN Exchange Server-Entwicklercommunity. 
    
- [StackOverflow](http://stackoverflow.com/tags/ews) – der Community StackOverflow Frage stellen. Achten Sie darauf, dass Sie Ihren Beitrag mit "Ews" markieren. 
    
- [Microsoft Support](http://support.microsoft.com/ph/730/en-us) – wenden Sie sich an einen Microsoft-Supportmitarbeiter, um Hilfe zu erhalten. 
    
## <a name="see-also"></a>Siehe auch


Finden Sie in den folgenden Artikeln:
  
- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [TRACE-Anfragen und-Antworten EWS Managed API behandeln](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
    
- [Instrumentieren Client-Anfragen für EWS und REST in Exchange](instrumenting-client-requests-for-ews-and-rest-in-exchange.md)
    
- [EWS-Einschränkung in Exchange](ews-throttling-in-exchange.md)
    
- [Aktualisieren von Konfigurationsinformationen mithilfe der AutoErmittlung](how-to-refresh-configuration-information-by-using-autodiscover.md)
    
- [Behandeln von AutoErmittlungs-Fehlermeldungen](handling-autodiscover-error-messages.md)
    
- [Fehlerbehandlung Benachrichtigung-bezogene in EWS in Exchange](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [Fehlerbehandlung Synchronisierung-bezogene in EWS in Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [Fehlerbehandlung Löschung-bezogene in EWS in Exchange](handling-deletion-related-errors-in-ews-in-exchange.md)
    
- [Konfigurieren der Protokollierung in IIS](http://www.iis.net/learn/manage/provisioning-and-managing-iis/configure-logging-in-iis)
    
- [Problembehandlung bei fehlgeschlagenen Anfragen mit Tracing in IIS 7](http://www.iis.net/learn/troubleshoot/using-failed-request-tracing/troubleshooting-failed-requests-using-tracing-in-iis)
    
- [Einführung in: Log Parser Studio](http://blogs.technet.com/b/exchange/archive/2012/03/07/introducing-log-parser-studio.aspx)
    
- [Standardeinstellungen Sie für die virtuellen Verzeichnisse für Exchange](http://technet.microsoft.com/en-us/library/gg247612%28v=exchg.150%29.aspx)
    
Laden Sie die folgenden:
  
- [Microsoft Netzwerkmonitor 3.4](http://www.microsoft.com/en-us/download/details.aspx?id=4865)
    
- [Fiddler](http://www.telerik.com/fiddler)
    
- [EWSEditor](http://ewseditor.codeplex.com/)
    
- [Exchange Web Services Managed API](http://go.microsoft.com/fwlink/?LinkID=255472)
    

