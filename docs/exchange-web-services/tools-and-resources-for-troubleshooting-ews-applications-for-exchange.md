---
title: Tools und Ressourcen für die Problembehandlung bei EWS-Anwendungen für Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: ee7fcd05-35d7-47bf-bac4-e719c49c11fe
description: Hier finden Sie Ressourcen, die Sie bei der Problembehandlung Ihrer verwaltete EWS-API oder EWS-Anwendung unterstützen.
localization_priority: Priority
ms.openlocfilehash: 7c7cbe8c93edec5ad99df079c6eb96286c1ba063
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463741"
---
# <a name="tools-and-resources-for-troubleshooting-ews-applications-for-exchange"></a>Tools und Ressourcen für die Problembehandlung bei EWS-Anwendungen für Exchange

Hier finden Sie Ressourcen, die Sie bei der Problembehandlung Ihrer verwaltete EWS-API oder EWS-Anwendung unterstützen.
  
Die Dinge gehen nicht immer wie geplant. Manchmal scheitern EWS-Anforderungen oder liefern unerwartete Ergebnisse. Dies kann frustrierend sein, vor allem, wenn der Grund nicht offensichtlich ist. Hoffentlich geschieht dies nie, aber wenn dies der Fall ist, enthält dieser Artikel Informationen zu Tools und Ressourcen, die Sie bei der Problembehandlung verwenden können.
  
> [!NOTE]
> Dieser Artikel enthält allgemeine Tipps zur Problembehandlung und Quellen für die Problembehandlung von Informationen. Leider ist es nicht möglich, detaillierte Schritte zur Problembehandlung anzugeben. Unterstützung bei der Problembehandlung Ihres spezifischen Fehlers finden Sie in den [nächsten Schritten](#bk_NextSteps). 
  
## <a name="examine-the-soap-requests-and-responses"></a>Untersuchen der SOAP-Anforderungen und-Antworten

Wenn die Dinge nicht ordnungsgemäß funktionieren, kann es wirklich hilfreich sein, um zu sehen, was vor sich geht. Die erste Abfrage bei der Untersuchung eines Problems mit EWS oder der verwaltete EWS-API besteht darin, die Anforderungen zu überprüfen, die Ihre Anwendung über das Netzwerk sendet, und die Antworten, die der Server zurücksendet.
  
Die verwaltete EWS-API vereinfacht die Untersuchung von SOAP-Anforderungen und-Antworten mit der [integrierten Ablaufverfolgungsfunktionalität](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md). Wenn Sie EWS verwenden, haben Sie möglicherweise oder haben keinen Zugriff auf ähnliche Ablaufverfolgungsfunktionen, je nachdem, welche Plattform oder Klassen Sie zum Senden Ihrer Anforderungen verwenden. Sie können jedoch immer ein Tool für die Netzwerkablaufverfolgung wie [Netzwerk Monitor](https://www.microsoft.com/download/details.aspx?id=4865) oder [Fiddler](http://www.telerik.com/fiddler) verwenden, um den Netzwerkdatenverkehr zu untersuchen und die Nutzlast für Anforderung und Antwort anzuzeigen. 
  
Darüber hinaus können Sie [Ihre Clientanforderungen Instrumentieren](instrumenting-client-requests-for-ews-and-rest-in-exchange.md) , um die in Anforderungen und Antworten verfügbaren Informationen zu verbessern. 
  
Nachdem Sie die Anforderungen und Antworten haben, Fragen Sie sich Folgendes: sehen Sie richtig aus? Werden die Werte, die Ihre Anwendung sendet, erwartet? Sind die Antworten sinnvoll?
  
## <a name="examine-error-codes"></a>Untersuchen von Fehlercodes

Manchmal kann der Fehlercode einen weiten Weg in Richtung auf das Problem darstellen, auch wenn es auf den ersten Blick nicht sinnvoll erscheint. Gibt der Fehler an, dass Ihr Client [gedrosselt](ews-throttling-in-exchange.md)wird? Ist ein Aufruf der AutoErmittlung zum [Aktualisieren von Konfigurationsinformationen](how-to-refresh-configuration-information-by-using-autodiscover.md) vielleicht in Ordnung? 
  
Weitere Informationen zum behandeln bestimmter Fehler finden Sie in den folgenden Artikeln:
  
- [Behandeln von AutoErmittlungs-Fehlermeldungen](handling-autodiscover-error-messages.md)
    
- [Umgang von Fehlern im Zusammenhang mit Benachrichtigungen in EWS in Exchange](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [Umgang mit Fehlern im Zusammenhang mit der Synchronisierung in EWS in Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [Umgang mit Fehlern in Exchange im Zusammenhang mit Löschungen in EWS](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="verify-versions"></a>Überprüfen von Versionen

Es gibt eine Reihe von verschiedenen Komponenten, die an EWS-Vorgängen beteiligt sind, und die Versionen dieser Komponenten können die Ergebnisse beeinflussen.
  
**Tabelle 1. Versionen von Komponenten, die sich auf EWS-Prozesse auswirken können**

|**Komponente**|**EWS Managed API**|**EWS**|**Hinweise**|
|:-----|:-----|:-----|:-----|
|Angeforderte Server Version  <br/> |[ExchangeServiceBase. RequestedServerVersion](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx) -Eigenschaft  <br/> |[RequestServerVersion](https://msdn.microsoft.com/library/af4032d5-42b3-463e-9d0a-8236d78e5b75%28Office.15%29.aspx) -Element  <br/> |Dieser Wert steuert, welche Version des EWS-Schemas zum Verarbeiten der EWS-Anforderung verwendet wird. Stellen Sie sicher, dass die hier angegebene Schemaversion für die Anforderung, die Sie senden, sinnvoll ist. Einige Eigenschaften und Vorgänge sind in früheren Versionen des Schemas nicht verfügbar.  <br/> |
|Die Server Version  <br/> |[ExchangeServiceBase. Klasse Server Info](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.serverinfo%28v=exchg.80%29.aspx) -Eigenschaft  <br/> |[ServerVersionInfo](https://msdn.microsoft.com/library/c04a6872-ca27-432b-aac2-36b023d0afc6%28Office.15%29.aspx) -Element  <br/> |Dieser Wert wird vom Server in EWS-Antworten zurückgegeben und gibt die Version des Servers an, der die Antwort verarbeitet hat. Stellen Sie sicher, dass dieser Wert Ihren Erwartungen entspricht. Stellen Sie nach Möglichkeit sicher, dass auf dem Exchange-Server das neueste Update für Ihre Hauptversion von Exchange läuft.  <br/> |
|Die verwaltete EWS-API Version  <br/> |Die Produkt Versionseigenschaft der Datei "Microsoft. Exchange. Webservices. dll".  <br/> |Nicht zutreffend  <br/> |Wenn Sie die verwaltete EWS-API verwenden, stellen Sie sicher, dass Sie [die neueste Version](https://aka.ms/ews-managed-api-readme)verwenden.  <br/> |
   
## <a name="verify-access"></a>Überprüfen des Zugriffs

EWS ist standardmäßig aktiviert, aber [Standardwerte können geändert werden](how-to-control-access-to-ews-in-exchange.md). Verwenden Sie das Cmdlet [Get-OrganizationConfig](https://technet.microsoft.com/library/bb124754.aspx) , um sicherzustellen, dass EWS auf dem Server aktiviert ist, und das Cmdlet [Get-CASMailbox](https://technet.microsoft.com/library/aa997571.aspx) , um sicherzustellen, dass EWS für das Postfach des Benutzers aktiviert ist. Überprüfen Sie auch die beiden Cmdlet-Antworten auf eine EWS-Zulassungs-oder Sperrliste, und stellen Sie sicher, dass Ihre Anwendung nicht mit EWS blockiert wird. 
  
Sie sollten auch sicherstellen, dass die [Standardauthentifizierungseinstellungen](https://technet.microsoft.com/library/gg247612%28v=exchg.150%29.aspx) für das virtuelle Verzeichnis EWS nicht geändert wurden. 
  
## <a name="try-another-ews-client"></a>Testen eines anderen EWS-Clients

Manchmal ist es hilfreich, die gleiche Anforderung von einem anderen Client auszuprobieren und Ergebnisse zu vergleichen. Wenn ein anderer Client unterschiedliche Ergebnisse erhält, was ist anders? Wenn Sie herausfinden, was sich zwischen einer erfolgreichen Anforderung und einer fehlgeschlagenen Anforderung unterscheidet, können Sie erklären, warum eine bestimmte Anforderung fehlschlägt.
  
Sie können zwar sicherlich einen anderen zu testenden Client schreiben, aber Sie müssen dies nicht tun! [EWSEditor](http://ewseditor.codeplex.com/) ist ein Beispiel Client, der die verwaltete EWS-API und EWS verwendet. Sie können den Client (einschließlich des Quellcodes) herunterladen und ihn verwenden, um dieselben Anforderungen zu testen, die in Ihrer Anwendung fehlschlagen. 
  
## <a name="examine-iis-logs"></a>Untersuchen von IIS-Protokollen

Wenn Sie Zugriff auf den Exchange-Server haben, können die von Internet Information Services (IIS) auf den Client Zugriffsservern bereitgestellten Protokollierungsfunktionen Weitere Informationen zu Fehlern liefern. Beachten Sie jedoch, dass IIS-Protokolle nur dann hilfreich sind, wenn Sie einen HTTP-Fehler erhalten.
  
IIS bietet zwei verschiedene Protokollierungsmethoden: [IIS-Protokollierung](http://www.iis.net/learn/manage/provisioning-and-managing-iis/configure-logging-in-iis) und [Ablaufverfolgung fehlgeschlagener Anforderungen](http://www.iis.net/learn/troubleshoot/using-failed-request-tracing/troubleshooting-failed-requests-using-tracing-in-iis). Zum Arbeiten mit IIS-Protokollen können Sie [Log Parser Studio](https://blogs.technet.com/b/exchange/archive/2012/03/07/introducing-log-parser-studio.aspx)verwenden, das eine Reihe integrierter EWS-Abfragen enthält.
  
## <a name="next-steps"></a>Nächste Schritte
<a name="bk_NextSteps"> </a>

Da Sie nun die Tools und Ressourcen kennen, die Sie bei der Problembehandlung verwenden können, benötigen Sie möglicherweise Hilfe zum Verständnis der von diesen Tools bereitgestellten Informationen. Im folgenden finden Sie einige Optionen zum Aufrufen von Hilfe:
  
- [Exchange Server Development Forum auf MSDN](https://social.msdn.microsoft.com/Forums/home?category=exchangeserver) – stellen Sie eine Frage der MSDN Exchange Server Development Community. 
    
- [StackOverflow](http://stackoverflow.com/tags/ews) – stellen Sie eine Frage der StackOverflow-Community. Achten Sie darauf, ihren Beitrag mit "EWS" zu markieren. 
    
- [Microsoft-Support](https://support.microsoft.com/ph/730/en-us) – wenden Sie sich an einen Microsoft-Supportmitarbeiter, um Hilfe zu erhalten. 
    
## <a name="see-also"></a>Siehe auch


Lesen Sie die folgenden Artikel:
  
- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [Ablaufverfolgungsanforderungen und -antworten zur Problembehandlung bei EWS-verwalteten API-Anwendungen](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
    
- [Handhaben von Clientanforderungen für EWS und REST in Exchange](instrumenting-client-requests-for-ews-and-rest-in-exchange.md)
    
- [EWS-Einschränkung in Exchange](ews-throttling-in-exchange.md)
    
- [Aktualisieren von Konfigurationsinformationen mithilfe der AutoErmittlung](how-to-refresh-configuration-information-by-using-autodiscover.md)
    
- [Behandeln von AutoErmittlungs-Fehlermeldungen](handling-autodiscover-error-messages.md)
    
- [Umgang von Fehlern im Zusammenhang mit Benachrichtigungen in EWS in Exchange](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [Umgang mit Fehlern im Zusammenhang mit der Synchronisierung in EWS in Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [Umgang mit Fehlern in Exchange im Zusammenhang mit Löschungen in EWS](handling-deletion-related-errors-in-ews-in-exchange.md)
    
- [Konfigurieren der Protokollierung in IIS](http://www.iis.net/learn/manage/provisioning-and-managing-iis/configure-logging-in-iis)
    
- [Problembehandlung bei fehlgeschlagenen Anforderungen mithilfe der Ablaufverfolgung in IIS 7](http://www.iis.net/learn/troubleshoot/using-failed-request-tracing/troubleshooting-failed-requests-using-tracing-in-iis)
    
- [Einführung: Log Parser Studio](https://blogs.technet.com/b/exchange/archive/2012/03/07/introducing-log-parser-studio.aspx)
    
- [Standardeinstellungen für virtuelle Exchange-Verzeichnisse](https://technet.microsoft.com/library/gg247612%28v=exchg.150%29.aspx)
    
Laden Sie Folgendes herunter:
  
- [Microsoft Network Monitor 3.4](https://www.microsoft.com/download/details.aspx?id=4865)
    
- [Fiddler](http://www.telerik.com/fiddler)
    
- [EWSEditor](http://ewseditor.codeplex.com/)
    
- [Exchange Webdienste Managed API](https://go.microsoft.com/fwlink/?LinkID=255472)
    

