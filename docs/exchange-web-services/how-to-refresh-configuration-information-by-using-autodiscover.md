---
title: Aktualisieren von Konfigurationsinformationen mithilfe der AutoErmittlung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: c2f3c6a5-e8ea-4375-b41a-686a6f238d33
description: Erfahren Sie, wie und wann Konfigurationsinformationen für Ihre Exchange Verbindung mithilfe der AutoErmittlung aktualisiert werden.
ms.openlocfilehash: 0ec6910fcd8ab66085de2414f02a4f78419ec78b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513115"
---
# <a name="refresh-configuration-information-by-using-autodiscover"></a>Aktualisieren von Konfigurationsinformationen mithilfe der AutoErmittlung

Erfahren Sie, wie und wann Konfigurationsinformationen für Ihre Exchange Verbindung mithilfe der AutoErmittlung aktualisiert werden.
  
Wenn Ihre EWS-Anwendung zum ersten Mal ausgeführt wird, bietet die AutoErmittlung eine hervorragende Möglichkeit, die Informationen zu sammeln, die Sie zum Herstellen einer Verbindung mit dem Exchange Postfach des Benutzers benötigen. Die AutoErmittlung erfolgt jedoch nicht nur bei der ersten Verwendung. Die regelmäßige Verwendung der AutoErmittlung kann dazu beitragen, dass Ihre Anwendung verbunden bleibt, indem sie auf Änderungen in der Exchange Bereitstellung reagiert.
  
## <a name="cache-autodiscover-endpoint-and-ews-settings"></a>Cache-AutoErmittlungsendpunkt und EWS-Einstellungen
<a name="bk_CacheSettings"> </a>

Es wird zwar empfohlen, die AutoErmittlung regelmäßig zu verwenden, aber wie regelmäßig Sie sie verwenden, erfordert einige Überlegungen. Im Idealfall können Sie schnell auf Änderungen in der Umgebung reagieren und zu viel unnötigen Netzwerkdatenverkehr generieren. Wenn Ihre Anwendung zum ersten Mal eine erfolgreiche AutoErmittlungsantwort erhält, sollten Sie die folgenden Informationen speichern, damit Sie den AutoErmittlungsprozess nicht jedes Mal wiederholen müssen, wenn Sie eine EWS-Anforderung senden.
  
**Tabelle 1. Informationen zum Zwischenspeichern für AutoErmittlungsanforderungen**

|**Festlegen des Zwischenspeicherns**|**Gültig für...**|**Details**|
|:-----|:-----|:-----|
|AutoErmittlungsendpunkt  <br/> |Solange es funktioniert  <br/> |Wenn Sie den AutoErmittlungsendpunkt speichern, der eine erfolgreiche Antwort zurückgegeben hat, müssen Sie den Vorgang zum [Generieren einer Liste von AutoErmittlungsendpunkten](how-to-generate-a-list-of-autodiscover-endpoints.md) und zum Testen dieser Endpunkte nicht wiederholen, bis Sie eine erfolgreiche Antwort erhalten.<br/><br/> **HINWEIS:** Die verwaltete EWS-API unterstützt das Zwischenspeichern des AutoErmittlungsendpunkts nicht.           |
|EWS-URL und alle anderen Einstellungen, die aus der AutoErmittlungsantwort abgerufen wurden  <br/> |Eine Woche  <br/> |Wenn Sie die EWS-URL und andere zugehörige Einstellungen speichern, müssen Sie keine [neue AutoErmittlungsanforderung](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) für jede EWS-Anforderung senden, oder wenn die Anwendung neu gestartet wird. Auch wenn eine EWS-URL für Ihren Benutzer funktioniert, ist möglicherweise ein Server verfügbar, der optimaler ist.<br/><br/> Beispielsweise könnte das Postfach des Benutzers auf einen neuen Postfachserver verschoben worden sein, was zu einem neuen bevorzugten EWS-Endpunkt führt. Es wird empfohlen, die Benutzereinstellungen zu aktualisieren, indem Sie eine neue AutoErmittlungsanforderung senden, nachdem eine Woche seit der letzten AutoErmittlungsanforderung vergangen ist. Diese Zeit kann an die Anforderungen Ihrer Anwendung angepasst werden.  <br/> |
   
## <a name="refresh-cached-configuration-information"></a>Aktualisieren zwischengespeicherter Konfigurationsinformationen
<a name="bk_RefreshConfig"> </a>

Nachdem Sie die Informationen zwischengespeichert haben, wollen wir untersuchen, wie Sie diesen Cache aktuell halten können. Es wird empfohlen, die zwischengespeicherten Informationen in folgenden Fällen zu aktualisieren:
  
- Der Gültigkeitszeitraum der Informationen läuft ab.
    
- Es tritt ein [Verbindungsfehler](#bk_ConnectionErrors) auf, UND Ihre zwischengespeicherten Informationen wurden zuletzt vor einer Stunde aktualisiert.
    
Um die zwischengespeicherten Informationen zu aktualisieren, senden Sie eine AutoErmittlungsanforderung an einen zwischengespeicherten AutoErmittlungsendpunkt, und führen Sie die folgenden Schritte aus:
  
- Wenn die Anforderung erfolgreich ist, vergleichen Sie den EWS-Endpunkt in der Antwort mit dem zwischengespeicherten EWS-Endpunkt, und führen Sie die folgenden Schritte aus:
    
  - Wenn sie unterschiedlich sind, verwenden Sie den neuen EWS-Endpunkt. Wenn Sie aktualisieren, um nach einem Fehler wiederherzustellen, wiederholen Sie die fehlgeschlagene Anforderung mit dem neuen Endpunkt.
    
  - Wenn sie identisch sind, verwenden Sie weiterhin den ursprünglichen EWS-Endpunkt. Wenn Sie aktualisieren, um nach einem Fehler wiederherzustellen, behandeln Sie den Fehler nach Bedarf.
    
- Wenn die Anforderung fehlschlägt, starten Sie den [AutoErmittlungsprozess](autodiscover-for-exchange.md) von vorne. Nachdem Sie eine erfolgreiche Antwort erhalten haben, ersetzen Sie den zwischengespeicherten AutoErmittlungsendpunkt durch den erfolgreichen AutoErmittlungsendpunkt, und verwenden Sie weiterhin den neuen EWS-Endpunkt. Wenn Sie keine erfolgreiche Antwort erhalten, verwenden Sie weiterhin den ursprünglichen AutoErmittlungsendpunkt und den EWS-Endpunkt. Wenn Sie aktualisieren, um nach einem Fehler wiederherzustellen, behandeln Sie den Fehler nach Bedarf. 
    
Die folgende Abbildung enthält eine visuelle Darstellung dieses Prozesses.
  
**Abbildung 1. Prozess zum Aktualisieren von Konfigurationsinformationen mithilfe der AutoErmittlung**

![Schematisches Diagramm, das zeigt, wie die AutoErmittlung Konfigurationsinformationen aktualisiert.](media/Ex15_Autodiscover_Refresh_Flowchart.png)
  
### <a name="connection-related-errors"></a>Verbindungsbezogene Fehler
<a name="bk_ConnectionErrors"> </a>

Das Aktualisieren der zwischengespeicherten Konfigurationsinformationen kann bei einigen Fehlern hilfreich sein, aber nicht bei allen. 
  
**Tabelle 2. Fehler beim Aktualisieren des Caches**

|**Error**|**Implementierung der verwalteten EWS-API**|**Hinweise**|
|:-----|:-----|:-----|
|DNS- oder Netzwerkfehler<br/><br/> Beispiel: Hostname konnte nicht gefunden werden.  <br/> |[ServiceRemoteException](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.data.serviceremoteexception?view=exchange-ews-api) <br/> |Jeder Fehler, der angibt, dass der Server nicht gefunden oder nicht erreicht werden konnte, kann durch Versuchen der AutoErmittlung behoben werden. <br/><br/> Ihr zwischengespeicherter EWS-Endpunkt ist möglicherweise nicht mehr gültig, und die AutoErmittlung kann Sie möglicherweise auf den neuen Server verweisen.  <br/> |
|HTTP-Statusfehler<br/><br/> Beispiel: 503 Dienst nicht verfügbar  <br/> |[ServiceRemoteException](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.data.serviceremoteexception?view=exchange-ews-api) <br/> |HTTP-Statusfehler können aus vielen verschiedenen Gründen auftreten.<br/><br/> Es empfiehlt sich jedoch, die AutoErmittlung auszuprobieren, um festzustellen, ob ein neuer EWS-Endpunkt für den Benutzer verfügbar ist.  <br/> |
|EWS-Fehlercodes <br/><br/> Beispiel: ErrorConnectionFailed <br/> |[ResponseCodeType](../web-service-reference/responsecode.md) <br/> | Die meisten EWS-Fehlercodes erfordern keine Aktualisierung ihrer Konfigurationsinformationen.<br/><br/> Die folgenden Angaben deuten jedoch ausdrücklich darauf hin, dass die Konfigurationsinformationen aktualisiert werden müssen:<br/>- **ErrorConnectionFailed** <br/>- **ErrorMailboxMoveInProgress** <br/> |
   
## <a name="see-also"></a>Siehe auch

- [AutoErmittlung für Exchange](autodiscover-for-exchange.md)  
- [Generieren einer Liste mit AutoErmittlungs-Endpunkten](how-to-generate-a-list-of-autodiscover-endpoints.md)   
- [Abrufen von Benutzereinstellungen von Exchange mithilfe der AutoErmittlung](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    

