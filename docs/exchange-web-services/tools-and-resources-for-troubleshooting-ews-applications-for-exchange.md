---
title: Tools und Ressourcen zur Problembehandlung bei EWS-Anwendungen für Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: ee7fcd05-35d7-47bf-bac4-e719c49c11fe
description: Hier finden Sie Ressourcen, die Ihnen bei der Problembehandlung Ihrer EWS verwalteten API oder EWS-Anwendung helfen.
localization_priority: Priority
ms.openlocfilehash: 8a65b06cf911cd033d7fe5fe1b4566a7496de784
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542582"
---
# <a name="tools-and-resources-for-troubleshooting-ews-applications-for-exchange"></a>Tools und Ressourcen zur Problembehandlung bei EWS-Anwendungen für Exchange

Hier finden Sie Ressourcen, die Ihnen bei der Problembehandlung Ihrer EWS verwalteten API oder EWS-Anwendung helfen.
  
Nicht immer läuft alles wie geplant. Manchmal schlagen EWS-Anforderungen fehl oder liefern unerwartete Ergebnisse. Dies kann frustrierend sein, insbesondere, wenn der Grund nicht offensichtlich ist. Hoffentlich geschieht Ihnen dies nie, aber wenn dies der Fall ist, enthält dieser Artikel Informationen zu Tools und Ressourcen, die Sie zur Problembehandlung verwenden können.
  
> [!NOTE]
> Dieser Artikel enthält allgemeine Hinweise zur Problembehandlung und Quellen für Informationen zur Problembehandlung. Leider ist es nicht möglich, detaillierte Schritte zur Problembehandlung anzugeben. Hilfe bei der Problembehandlung Ihres spezifischen Fehlers finden Sie unter [Nächste Schritte](#bk_NextSteps). 
  
## <a name="examine-the-soap-requests-and-responses"></a>Überprüfen der SOAP-Anforderungen und -Antworten

Wenn etwas nicht ordnungsgemäß funktioniert, hilft es wirklich, die Vorgänge zu sehen. Die erste Fragestellung bei der Untersuchung eines Problems mit EWS oder der EWS verwalteten API besteht darin, die Anforderungen zu untersuchen, die Ihre Anwendung über das Netzwerk sendet, und die Antworten, die der Server zurücksendet.
  
Die EWS verwaltete API erleichtert die Untersuchung von SOAP-Anforderungen und -Antworten mit ihrer[integrierten Ablaufverfolgungsfunktionalität](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md). Wenn Sie EWS verwenden, haben Sie möglicherweise Zugriff auf ähnliche Ablaufverfolgungsfunktionen, je nachdem, welche Plattform oder Klassen Sie zum Senden Ihrer Anforderungen verwenden. Sie können jedoch immer ein Netzwerkablaufverfolgungstool wie [Network Monitor](https://www.microsoft.com/download/details.aspx?id=4865) oder [Fiddler](http://www.telerik.com/fiddler) verwenden, um den Netzwerkdatenverkehr zu untersuchen und die Anforderung- und Antwortnutzlasten anzuzeigen. 
  
Darüber hinaus können Sie [Ihre Clientanforderungen instrumentieren](instrumenting-client-requests-for-ews-and-rest-in-exchange.md), um die in Anforderungen und Antworten verfügbaren Informationen zu verbessern. 
  
Nachdem Sie die Anforderungen und Antworten erhalten haben, fragen Sie sich Folgendes: Sehen sie richtig aus? Entsprechen die Werte, die Ihre Anwendung sendet, den Erwartungen? Sind die Antworten sinnvoll?
  
## <a name="examine-error-codes"></a>Überprüfen von Fehlercodes

Manchmal kann der Fehlercode einen großen Beitrag zur Lokalisierung des Problems leisten, auch wenn er auf den ersten Blick nicht sinnvoll erscheint. Gibt der Fehler an, dass Ihr Client [gedrosselt](ews-throttling-in-exchange.md)wird? Ist vielleicht ist ein Aufruf der AutoErmittlung zum [Aktualisieren von Konfigurationsinformationen](how-to-refresh-configuration-information-by-using-autodiscover.md) dran? 
  
Weitere Informationen zur Behandlung bestimmter Fehler finden Sie in den folgenden Artikeln:
  
- [Umgang mit AutoErmittlung-Fehlermeldungen](handling-autodiscover-error-messages.md)
    
- [Umgang mit Fehlern im Zusammenhang mit Benachrichtigungen in EWS in Exchange](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [Umgang mit Fehlern im Zusammenhang mit der Synchronisierung in EWS in Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [Umgang mit löschbezogenen Fehlern in EWS in Exchange](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="verify-versions"></a>Überprüfen von Versionen

An EWS-Vorgängen sind eine Reihe verschiedener Komponenten beteiligt, und die Versionen dieser Komponenten können die Ergebnisse beeinflussen.
  
**Tabelle 1. Versionsangabe der Komponenten, die sich auf EWS-Prozesse auswirken können**

|**Komponente**|**EWS verwaltete API**|**EWS**|**Notizen**|
|:-----|:-----|:-----|:-----|
|Angeforderte Serverversion  <br/> |[ExchangeServiceBase.RequestedServerVersion](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx)-Eigenschaft  <br/> |[RequestServerVersion](https://msdn.microsoft.com/library/af4032d5-42b3-463e-9d0a-8236d78e5b75%28Office.15%29.aspx)-Element  <br/> |Dieser Wert steuert, welche Version des EWS-Schemas zum Verarbeiten der EWS-Anforderung verwendet wird. Stellen Sie sicher, dass die hier angegebene Schemaversion für die Anforderung, die Sie senden, sinnvoll ist. Einige Eigenschaften und Vorgänge sind in früheren Versionen des Schemas nicht verfügbar.  <br/> |
|Die Serverversion  <br/> |[ExchangeServiceBase.ServerInfo](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.serverinfo%28v=exchg.80%29.aspx)-Eigenschaft  <br/> |[ServerVersionInfo](https://msdn.microsoft.com/library/c04a6872-ca27-432b-aac2-36b023d0afc6%28Office.15%29.aspx)-Element  <br/> |Dieser Wert wird vom Server in EWS-Antworten zurückgegeben und gibt die Version des Servers an, der die Antwort verarbeitet hat. Stellen Sie sicher, dass dieser Wert ihren Erwartungen entspricht. Stellen Sie nach Möglichkeit sicher, dass auf dem Exchange-Server das neueste Update für Ihre Hauptversion von Exchange ausgeführt wird.  <br/> |
|Die Version der EWS verwalteten API  <br/> |Die Produktversionseigenschaft der Microsoft.Exchange.WebServices.dll-Datei.  <br/> |Nicht zutreffend  <br/> |Wenn Sie die EWS verwaltete API verwenden, stellen Sie sicher, dass Sie [die neueste Version](https://aka.ms/ews-managed-api-readme)verwenden.  <br/> |
   
## <a name="verify-access"></a>Überprüfen des Zugriffs

EWS ist standardmäßig aktiviert, [die Standardwerte können allerdings geändert werden](how-to-control-access-to-ews-in-exchange.md). Verwenden Sie das Cmdlet [Get-OrganizationConfig](https://technet.microsoft.com/library/bb124754.aspx), um sicherzustellen, dass EWS auf dem Server aktiviert ist, und das Cmdlet [Get-CASMailbox](https://technet.microsoft.com/library/aa997571.aspx), um sicherzustellen, dass EWS für das Postfach des Benutzers aktiviert ist. Überprüfen Sie außerdem beide Cmdlet-Antworten auf eine EWS-Zulassung- oder Sperrliste, und stellen Sie sicher, dass ihre Anwendung nicht für die Verwendung von EWS blockiert ist. 
  
Sie sollten auch überprüfen, ob die [Standardauthentifizierungseinstellungen](https://technet.microsoft.com/library/gg247612%28v=exchg.150%29.aspx) im virtuellen EWS-Verzeichnis nicht geändert wurden. 
  
## <a name="try-another-ews-client"></a>Probieren Sie einen anderen EWS-Client aus.

Manchmal ist es hilfreich, dieselbe Anforderung von einem anderen Client auszuprobieren, und die Ergebnisse zu vergleichen. Was ist anders, wenn ein anderer Client andere Ergebnisse erhält? Herauszufinden, was sich zwischen einer erfolgreichen und einer fehlgeschlagenen Anforderung unterscheidet, kann helfen zu erklären, warum eine bestimmte Anforderung fehlschlägt.
  
Sie können zwar sicherlich einen anderen Client zum Testen schreiben, müssen Sie aber nicht! [EWSEditor](http://ewseditor.codeplex.com/) ist ein Beispielclient, der die EWS verwaltete API und EWS verwendet. Sie können den Client (einschließlich des Quellcodes) herunterladen und damit dieselben Anforderungen ausprobieren, die in Ihrer Anwendung fehlschlagen. 
  
## <a name="examine-iis-logs"></a>Überprüfen von IIS-Protokollen

Wenn Sie Zugriff auf den Exchange-Server haben, kann die Protokollierungsfunktion, der Internetinformationsdienste (IIS) auf den Clientzugriffsservern weitere Informationen zu Fehlern bereitstellen. Beachten Sie jedoch, dass IIS-Protokolle nur dann hilfreich sind, wenn Sie einen HTTP-Fehler erhalten.
  
IIS bietet zwei verschiedene Protokollierungsmethoden: [IIS-Protokollierung](http://www.iis.net/learn/manage/provisioning-and-managing-iis/configure-logging-in-iis) und [Ablaufverfolgung fehlgeschlagener Anforderungen](http://www.iis.net/learn/troubleshoot/using-failed-request-tracing/troubleshooting-failed-requests-using-tracing-in-iis). Um mit IIS-Protokollen zu arbeiten, können Sie [Log Parser Studio](https://blogs.technet.com/b/exchange/archive/2012/03/07/introducing-log-parser-studio.aspx)verwenden, das eine Reihe integrierter EWS-Abfragen enthält.
  
## <a name="next-steps"></a>Nächste Schritte
<a name="bk_NextSteps"> </a>

Nachdem Sie nun mehr über die Tools und Ressourcen erfahren haben, die Sie für die Problembehandlung verwenden können, benötigen Sie möglicherweise Hilfe beim Verständnis der von diesen Tools bereitgestellten Informationen. Im Folgenden sind einige Optionen aufgeführt, um Hilfe zu erhalten:
  
- [Exchange Server-Entwicklungsforum auf MSDN](https://social.msdn.microsoft.com/Forums/home?category=exchangeserver) – Stellen Sie eine Frage an die MSDN Exchange Server-Entwicklungscommunity. 
    
- [StackOverflow](http://stackoverflow.com/tags/ews) – Stellen Sie eine Frage an die StackOverflow-Community. Achten Sie darauf, Ihren Beitrag mit "ews" zu markieren. 
    
- [Microsoft-Support](https://support.microsoft.com/ph/730/en-us) – Wenden Sie sich an einen Microsoft-Support-Experten, um Unterstützung zu erhalten. 
    
## <a name="see-also"></a>Siehe auch


Lesen Sie die folgenden Artikel:
  
- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [Ablaufverfolgungsanforderungen und -antworten zur Problembehandlung bei EWS-verwalteten API-Anwendungen](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
    
- [Handhaben von Clientanforderungen für EWS und REST in Exchange](instrumenting-client-requests-for-ews-and-rest-in-exchange.md)
    
- [EWS-Drosselung in Exchange](ews-throttling-in-exchange.md)
    
- [Aktualisieren von Konfigurationsinformationen mithilfe der AutoErmittlung](how-to-refresh-configuration-information-by-using-autodiscover.md)
    
- [Behandeln von AutoErmittlungs-Fehlermeldungen](handling-autodiscover-error-messages.md)
    
- [Umgang mit Fehlern im Zusammenhang mit Benachrichtigungen in EWS in Exchange](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [Umgang mit Fehlern im Zusammenhang mit der Synchronisierung in EWS in Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [Umgang mit löschbezogenen Fehlern in EWS in Exchange](handling-deletion-related-errors-in-ews-in-exchange.md)
    
- [Konfigurieren der Protokollierung in IIS](http://www.iis.net/learn/manage/provisioning-and-managing-iis/configure-logging-in-iis)
    
- [Problembehandlung bei fehlgeschlagenen Anforderungen mithilfe der Ablaufverfolgung in IIS 7](http://www.iis.net/learn/troubleshoot/using-failed-request-tracing/troubleshooting-failed-requests-using-tracing-in-iis)
    
- [Einführung: Protokollparser Studio](https://blogs.technet.com/b/exchange/archive/2012/03/07/introducing-log-parser-studio.aspx)
    
- [Standardeinstellungen für virtuelle Exchange-Verzeichnisse](https://technet.microsoft.com/library/gg247612%28v=exchg.150%29.aspx)
    
Laden Sie Folgendes herunter:
  
- [Microsoft-Netzwerkmonitor 3.4](https://www.microsoft.com/download/details.aspx?id=4865)
    
- [Fiddler](http://www.telerik.com/fiddler)
    
- [EWSEditor](http://ewseditor.codeplex.com/)
    
- [Managed API für Exchange-Webdienste](https://www.nuget.org/packages/Microsoft.Exchange.WebServices/)
