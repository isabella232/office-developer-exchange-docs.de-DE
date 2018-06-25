---
title: Aktualisieren von Konfigurationsinformationen mithilfe der AutoErmittlung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: c2f3c6a5-e8ea-4375-b41a-686a6f238d33
description: Hier erfahren Sie, wie und wann zum Aktualisieren von Konfigurationsinformationen für Ihre Exchange-Verbindung mit der AutoErmittlung.
ms.openlocfilehash: ef3b61781cbafa6e7b873336a050c0b8c33a28ec
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757012"
---
# <a name="refresh-configuration-information-by-using-autodiscover"></a>Aktualisieren von Konfigurationsinformationen mithilfe der AutoErmittlung

Hier erfahren Sie, wie und wann zum Aktualisieren von Konfigurationsinformationen für Ihre Exchange-Verbindung mit der AutoErmittlung.
  
Wenn die EWS-Anwendung zum ersten Mal ausgeführt wird, bietet AutoErmittlung eine hervorragende Möglichkeit, die Informationen zu sammeln, die Sie benötigen, um mit Exchange-Postfach des Benutzers zu verbinden. Aber AutoErmittlung nicht nur für die erstmalige Verwendung. Verwenden der AutoErmittlung in regelmäßigen Abständen können Sie Ihre Anwendung verbunden werden, da es zur Beantwortung von Änderungen in der Exchange-Bereitstellung schützen.
  
## <a name="cache-autodiscover-endpoint-and-ews-settings"></a>Cache für die AutoErmittlung Endpunkt und EWS-Einstellungen
<a name="bk_CacheSettings"> </a>

Während wir erfordert mithilfe von AutoErmittlung regelmäßig, wie häufig Sie verwenden sollten einige berücksichtigt. Im Idealfall können Sie abstimmen, reagieren schnell auf Änderungen in der Umgebung mit zu hohem Datenverkehr Netzwerk unnötig generieren. Wenn die Anwendung zum ersten Mal eine erfolgreiche Antwort der AutoErmittlung erhält, sollten Sie die folgende Informationen speichern, so, dass Sie keine AutoErmittlung-Prozesses wiederholen jedes Mal, wenn Sie eine webdienstanforderung senden.
  
**In Tabelle 1. Fordert Informationen zu den Cache für die AutoErmittlung**

|**Durch Festlegen auf cache**|**Gilt für...**|**Details**|
|:-----|:-----|:-----|
|AutoErmittlung-Endpunkt  <br/> |Solange es funktioniert  <br/> |Wenn Sie den AutoErmittlung-Endpunkt, der eine erfolgreiche Antwort zurückgegeben speichern, müssen Sie keinen wiederholen den Vorgang [generieren Sie eine Liste der AutoErmittlung-Endpunkten](how-to-generate-a-list-of-autodiscover-endpoints.md) und versuchen sie, bis Sie eine erfolgreiche Antwort erhalten.<br/><br/> **Hinweis**: die EWS Managed API unterstützt nicht das Zwischenspeichern des AutoErmittlung-Endpunkts.           |
|EWS-URL und alle anderen Einstellungen aus der Antwort der AutoErmittlung abgerufen  <br/> |24 Stunden  <br/> |Durch Speichern der EWS-URL und andere verwandte Einstellungen, die Sie nicht bei jeder Anforderung EWS [Senden Sie eine neue autoermittlungsanforderung](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) verfügen oder wenn die Anwendung neu gestartet wird. Selbst wenn EWS-URL für Ihre Benutzer funktioniert, ein Server möglicherweise jedoch verfügbar d. h. mehr optimale.<br/><br/> Beispielsweise kann das Postfach des Benutzers auf einen neuen Mailbox-Server, was zu einem neuen bevorzugten EWS-Endpunkt verschoben haben. Es wird empfohlen, dass Sie Ihre benutzereinstellungen durch Senden einer neuen autoermittlungsanforderung nach Ablauf von 24 Stunden seit der letzten AutoErmittlung-Anforderung aktualisieren. Dieses Mal kann die erfüllen Ihrer Anwendung angepasst werden.  <br/> |
   
## <a name="refresh-cached-configuration-information"></a>Aktualisieren von zwischengespeicherten Konfigurationsinformationen
<a name="bk_RefreshConfig"> </a>

Nun, da Sie die Daten, die zwischengespeichert werden, betrachten wir wie Sie diesem Cache aktuell beibehalten können. Es wird empfohlen, dass Sie die zwischengespeicherte Informationen zu aktualisieren wenn:
  
- Die Informationen Gültigkeitsdauer läuft ab.
    
- Ein [Verbindungsfehler](#bk_ConnectionErrors) auftritt. 
    
Um die zwischengespeicherten Informationen zu aktualisieren, senden Sie eine autoermittlungsanforderung an einen zwischengespeicherten AutoErmittlung-Endpunkt, und gehen Sie folgendermaßen vor:
  
- Wenn die Anforderung erfolgreich ist, vergleichen Sie EWS-Endpunkts in der Antwort mit dem Cache EWS-Endpunkt, und gehen Sie folgendermaßen vor:
    
  - Wenn sie unterschiedlich sind, verwenden Sie neue EWS-Endpunkts. Wenn Sie zum Wiederherstellen eines Fehlers aktualisieren sind, wiederholen Sie die fehlerhafte Anforderung mit dem neuen Endpunkt.
    
  - Wenn sie identisch sind, auch weiterhin mithilfe den ursprünglichen EWS-Endpunkt. Wenn Sie zum Wiederherstellen eines Fehlers aktualisieren sind, wird der Fehler entsprechend behandelt.
    
- Wenn die Anforderung ein Fehler auftritt, beginnen Sie der [AutoErmittlung-Prozesses](autodiscover-for-exchange.md) am Anfang. Nachdem Sie eine erfolgreiche Antwort erhalten, ersetzen Sie den zwischengespeicherten AutoErmittlung-Endpunkt mit der AutoErmittlung-Endpunkt, der erfolgreich abgeschlossen wurde, und fahren Sie mit der neuen EWS-Endpunkt verwenden. Wenn Sie keine erfolgreiche Antwort erhalten, auch weiterhin mithilfe der ursprünglichen AutoErmittlung-Endpunkt und EWS-Endpunkt. Wenn Sie zum Wiederherstellen eines Fehlers aktualisieren sind, wird der Fehler entsprechend behandelt. 
    
Die folgende Abbildung bietet eine visuelle Darstellung dieses Prozesses.
  
**Abbildung 1. Prozess für die Aktualisierung von Konfigurationsinformationen mithilfe der AutoErmittlung**

![Schematisches Diagramm, das zeigt, wie die AutoErmittlung Konfigurationsinformationen aktualisiert.](media/Ex15_Autodiscover_Refresh_Flowchart.png)
  
### <a name="connection-related-errors"></a>Verbindungsfehler
<a name="bk_ConnectionErrors"> </a>

Aktualisiert die zwischengespeicherten Konfigurationsinformationen kann mit einigen Fehlern, jedoch nicht alle helfen. 
  
**In Tabelle 2. Fehler behoben, indem Sie den Cache aktualisieren**

|**Fehler**|**EWS Managed API-Implementierung**|**Anmerkungen**|
|:-----|:-----|:-----|
|DNS- oder Fehler bei Fehlern<br/><br/> Beispiel: Hostname konnte nicht gefunden werden.  <br/> |[ServiceRemoteException](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ServiceRemoteException.aspx) <br/> |Etwaige Fehler, der angibt, dass der Server nicht gefunden oder nicht erreicht werden konnte möglicherweise durch Versuch der AutoErmittlung behoben werden. <br/><br/> Ihrer zwischengespeicherte EWS-Endpunkt möglicherweise nicht mehr gültig sein, und möglicherweise AutoErmittlung können Sie auf den neuen Server verweisen.  <br/> |
|HTTP-Status-Fehler<br/><br/> Beispiel: 503 Dienst nicht verfügbar  <br/> |[ServiceRemoteException](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ServiceRemoteException.aspx) <br/> |HTTP-Status Fehler können auftreten, verschiedene Ursachen haben.<br/><br/> Jedoch ist es ratsam, versuchen Sie es AutoErmittlung, um festzustellen, ob eine neue EWS-Endpunkts für den Benutzer zur Verfügung steht.  <br/> |
|EWS-Fehlercodes <br/><br/> Beispiel: ErrorConnectionFailed <br/> |[ResponseCodeType](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ResponseCodeType.aspx) <br/> | Die meisten EWS-Fehlercodes rechtfertigen nicht aktualisieren Ihre Konfigurationsinformationen.<br/><br/> Allerdings geben Sie die folgenden insbesondere, dass die Konfigurationsinformationen aktualisiert werden muss:<br/>- **ErrorConnectionFailed** <br/>- **ErrorMailboxMoveInProgress** <br/> |
   
## <a name="see-also"></a>Siehe auch

- [AutoErmittlung für Exchange](autodiscover-for-exchange.md)  
- [Generieren Sie eine Liste von Endpunkten für die AutoErmittlung](how-to-generate-a-list-of-autodiscover-endpoints.md)   
- [Abrufen von benutzereinstellungen aus Exchange mithilfe der AutoErmittlung](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    

