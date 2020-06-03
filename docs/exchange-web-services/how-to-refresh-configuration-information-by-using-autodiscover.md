---
title: Aktualisieren von Konfigurationsinformationen mithilfe der AutoErmittlung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: c2f3c6a5-e8ea-4375-b41a-686a6f238d33
description: Erfahren Sie, wie und wann die Konfigurationsinformationen für Ihre Exchange-Verbindung mithilfe der AutoErmittlung aktualisiert werden.
ms.openlocfilehash: b9a4264d150d09b0e143e0bf7365af351bb2ef44
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527754"
---
# <a name="refresh-configuration-information-by-using-autodiscover"></a>Aktualisieren von Konfigurationsinformationen mithilfe der AutoErmittlung

Erfahren Sie, wie und wann die Konfigurationsinformationen für Ihre Exchange-Verbindung mithilfe der AutoErmittlung aktualisiert werden.
  
Wenn Ihre EWS-Anwendung zum ersten Mal ausgeführt wird, bietet die AutoErmittlung eine großartige Möglichkeit, um die Informationen zu sammeln, die Sie benötigen, um eine Verbindung mit dem Exchange-Postfach Ihres Benutzers herzustellen. Die AutoErmittlung ist aber nicht nur für die erstmalige Verwendung. Die regelmäßige Verwendung der AutoErmittlung kann dazu beitragen, dass Ihre Anwendung verbunden bleibt, indem Sie auf Änderungen in der Exchange-Bereitstellung reagiert.
  
## <a name="cache-autodiscover-endpoint-and-ews-settings"></a>Cache Auto ermittlungsendpunkt und EWS-Einstellungen
<a name="bk_CacheSettings"> </a>

Es wird empfohlen, dass Sie die AutoErmittlung regelmäßig verwenden, aber wie regelmäßig Sie es verwenden, erfordert eine gewisse Überlegung. Idealerweise können Sie die Reaktion schnell auf Änderungen in der Umgebung abstimmen, um zu viel unnötigen Netzwerkdatenverkehr zu generieren. Wenn Ihre Anwendung zum ersten Mal eine erfolgreiche Auto Ermittlungs Antwort erhält, sollten Sie die folgenden Informationen speichern, damit Sie den Auto Ermittlungsprozess nicht jedes Mal wiederholen müssen, wenn Sie eine EWS-Anforderung senden.
  
**Tabelle 1. Cache Informationen für Auto Ermittlungsanforderungen**

|**Festlegen auf Cache**|**Gültig für...**|**Details**|
|:-----|:-----|:-----|
|Auto ermittlungsendpunkt  <br/> |Solange es funktioniert  <br/> |Wenn Sie den Auto ermittlungsendpunkt speichern, der eine erfolgreiche Antwort zurückgegeben hat, müssen Sie den Prozess des [Generierens einer Liste mit Auto Ermittlungs Endpunkten](how-to-generate-a-list-of-autodiscover-endpoints.md) nicht wiederholen und versuchen, Sie zu testen, bis Sie eine erfolgreiche Antwort erhalten.<br/><br/> **Hinweis**: das verwaltete EWS-API unterstützt nicht das Zwischenspeichern des Auto Ermittlungs Endpunkts.           |
|EWS-URL und alle anderen von der Auto Ermittlungs Antwort abgerufenen Einstellungen  <br/> |Eine Woche  <br/> |Wenn Sie die EWS-URL und andere zugehörige Einstellungen speichern, müssen Sie keine [neue Auto Ermittlungsanforderung](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) für jede EWS-Anforderung senden oder wenn Ihre Anwendung neu gestartet wird. Selbst wenn eine EWS-URL für Ihren Benutzer funktioniert, ist möglicherweise ein Server verfügbar, der optimal ist.<br/><br/> Beispielsweise wurde das Postfach des Benutzers möglicherweise auf einen neuen Postfachserver verschoben, was zu einem neuen bevorzugten EWS-Endpunkt führte. Es wird empfohlen, dass Sie Ihre Benutzereinstellungen aktualisieren, indem Sie eine neue Auto Ermittlungsanforderung senden, nachdem eine Woche seit der letzten Auto Ermittlungsanforderung vergangen ist. Diese Zeit kann angepasst werden, um die Anforderungen Ihrer Anwendung zu erfüllen.  <br/> |
   
## <a name="refresh-cached-configuration-information"></a>Aktualisieren zwischengespeicherter Konfigurationsinformationen
<a name="bk_RefreshConfig"> </a>

Nun, da Sie die Informationen zwischengespeichert haben, lassen Sie uns untersuchen, wie Sie diesen Cache aktuell halten können. Es wird empfohlen, die zwischengespeicherten Informationen zu aktualisieren, wenn:
  
- Der Gültigkeitszeitraum der Informationen läuft ab.
    
- Ein [Verbindungs bezogener Fehler](#bk_ConnectionErrors) tritt auf, und ihre zwischengespeicherten Informationen wurden zuletzt vor mehr als einer Stunde aktualisiert.
    
Um die zwischengespeicherten Informationen zu aktualisieren, senden Sie eine Auto Ermittlungsanforderung an einen zwischengespeicherten Auto ermittlungsendpunkt, und führen Sie die folgenden Schritte aus:
  
- Wenn die Anforderung erfolgreich ist, vergleichen Sie den EWS-Endpunkt in der Antwort mit dem zwischengespeicherten EWS-Endpunkt, und führen Sie die folgenden Schritte aus:
    
  - Wenn Sie unterschiedlich sind, verwenden Sie den neuen EWS-Endpunkt. Wenn Sie aktualisieren, um einen Fehler wiederherzustellen, versuchen Sie es mit dem neuen Endpunkt erneut mit der fehlgeschlagenen Anforderung.
    
  - Wenn Sie identisch sind, fahren Sie mit dem ursprünglichen EWS-Endpunkt fort. Wenn Sie aktualisieren, um einen Fehler wiederherzustellen, behandeln Sie den Fehler entsprechend.
    
- Wenn die Anforderung fehlschlägt, starten Sie den [Auto Ermittlungsprozess](autodiscover-for-exchange.md) von Anfang an. Nachdem Sie eine erfolgreiche Antwort erhalten haben, ersetzen Sie den zwischengespeicherten Auto ermittlungsendpunkt mit dem Endpunkt der AutoErmittlung, der erfolgreich war, und verwenden Sie weiterhin den neuen EWS-Endpunkt. Wenn Sie keine erfolgreiche Antwort erhalten, fahren Sie mit der Verwendung des ursprünglichen Auto Ermittlungs Endpunkts und des EWS-Endpunkts fort. Wenn Sie aktualisieren, um einen Fehler wiederherzustellen, behandeln Sie den Fehler entsprechend. 
    
Die folgende Abbildung bietet eine visuelle Darstellung dieses Prozesses.
  
**Abbildung 1. Prozess zum Aktualisieren von Konfigurationsinformationen mithilfe der AutoErmittlung**

![Schematisches Diagramm, das zeigt, wie die AutoErmittlung Konfigurationsinformationen aktualisiert.](media/Ex15_Autodiscover_Refresh_Flowchart.png)
  
### <a name="connection-related-errors"></a>Verbindungsbezogene Fehler
<a name="bk_ConnectionErrors"> </a>

Das Aktualisieren der zwischengespeicherten Konfigurationsinformationen kann bei einigen Fehlern helfen, jedoch nicht bei allen. 
  
**Tabelle 2. Durch Aktualisieren des Caches behobene Fehler**

|**Error**|**Implementierung der verwalteten EWS-API**|**Hinweise**|
|:-----|:-----|:-----|
|DNS-oder Netzwerkfehler<br/><br/> Beispiel: Host Name konnte nicht gefunden werden.  <br/> |[ServiceRemoteException](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.data.serviceremoteexception?view=exchange-ews-api) <br/> |Jeder Fehler, der angibt, dass der Server nicht gefunden wurde oder nicht erreicht werden konnte, kann durch einen Versuch der AutoErmittlung aufgelöst werden. <br/><br/> Der zwischengespeicherte EWS-Endpunkt ist möglicherweise nicht mehr gültig, und die AutoErmittlung kann Sie auf den neuen Server hinweisen.  <br/> |
|HTTP-Statusfehler<br/><br/> Beispiel: 503 Dienst nicht verfügbar  <br/> |[ServiceRemoteException](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.data.serviceremoteexception?view=exchange-ews-api) <br/> |HTTP-Status Fehler können aus vielen verschiedenen Gründen auftreten.<br/><br/> Es empfiehlt sich jedoch, die AutoErmittlung zu testen, um festzustellen, ob ein neuer EWS-Endpunkt für den Benutzer verfügbar ist.  <br/> |
|EWS-Fehlercodes <br/><br/> Beispiel: ErrorConnectionFailed <br/> |[ResponseCodeType](../web-service-reference/responsecode.md) <br/> | Die meisten EWS-Fehlercodes gewährleisten keine Aktualisierung Ihrer Konfigurationsinformationen.<br/><br/> Im folgenden wird jedoch ausdrücklich darauf hingewiesen, dass die Konfigurationsinformationen aktualisiert werden müssen:<br/>- **ErrorConnectionFailed** <br/>- **ErrorMailboxMoveInProgress** <br/> |
   
## <a name="see-also"></a>Siehe auch

- [AutoErmittlung für Exchange](autodiscover-for-exchange.md)  
- [Generieren einer Liste mit AutoErmittlungs-Endpunkten](how-to-generate-a-list-of-autodiscover-endpoints.md)   
- [Abrufen von Benutzereinstellungen von Exchange mithilfe der AutoErmittlung](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    

