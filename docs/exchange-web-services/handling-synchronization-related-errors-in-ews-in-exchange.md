---
title: Umgang mit Fehlern im Zusammenhang mit der Synchronisierung in EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a0807b90-645a-4ea6-aee1-96828df14be0
description: Erfahren Sie, wie synchronisierungsbezogene Fehler in Anwendungen behandelt werden, die Sie mit dem verwaltete EWS-API oder EWS in Exchange entwickeln.
ms.openlocfilehash: f62937ec444d64b0b358581371f1260f565215b3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455940"
---
# <a name="handling-synchronization-related-errors-in-ews-in-exchange"></a>Umgang mit Fehlern im Zusammenhang mit der Synchronisierung in EWS in Exchange

Erfahren Sie, wie synchronisierungsbezogene Fehler in Anwendungen behandelt werden, die Sie mit dem verwaltete EWS-API oder EWS in Exchange entwickeln.
  
Wenn Ihre Anwendung Elemente und Ordner synchronisiert, müssen Sie möglicherweise synchronisierungsbezogene Fehler behandeln. Sie können diese Fehler zur Laufzeit oder während der Entwicklung ihrer EWS-Anwendung behandeln. Die meisten dieser Fehler werden durch die [ResponseCodeType](https://msdn.microsoft.com/library/exchangewebservices.responsecodetype%28v=exchg.80%29.aspx) -Aufzählung in der verwaltete EWS-API und das [Response Code](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) -Element in Exchange-Webdienste definiert. 
  
**Tabelle 1. Synchronisierungsbezogene Fehler und deren Handhabung**

|**Error**|**Tritt auf, wenn Sie versuchen,...**|**Behandeln von...**|
|:-----|:-----|:-----|
|ErrorInvalidSyncStateData  <br/> | Synchronisieren von Elementen oder Ordnern mithilfe eines ungültigen Synchronisierungsstatus Werts  <br/>  Schließen Sie einen Stammordner in Ihrer anfänglichen SyncFolderHierarchy-Anforderung aus, wenn die nachfolgende Anforderung einen Stammordner enthält.  <br/>  Verwenden Sie unterschiedliche Stammordner in nachfolgenden Anforderungen.  <br/> | Stellen Sie sicher, dass der von Ihnen gesendete Sync State-Wert dem Sync State-Wert entspricht, der während einer vorherigen Synchronisierung zurückgegeben wurde.  <br/>  Sicherstellen, dass Sie nicht den Synchronisierungsstatus für die Ordnerhierarchie senden, wenn Sie versuchen, Elemente zu synchronisieren, und umgekehrt.  <br/>  Stellen Sie sicher, dass Sie den Synchronisierungsstatus für den richtigen Stammordner senden.  <br/>  Sicherstellen, dass in jeder Anforderung derselbe Stammordner angegeben wird.  <br/>  Sicherstellen, dass die vorherige Anforderung keinen Stammordner NULL angegeben hat, während die aktuelle Anforderung einen Stammordner des Stammverzeichnisses enthält. NULL und root werden nicht gleich behandelt.  <br/> |
|ErrorSyncFolderNotFound  <br/> |Synchronisieren von Unterordnern oder Elementen in einem Ordner, der auf dem Server nicht gefunden werden kann.  <br/> |Sicherstellen, dass die in der Anforderung angegebene Ordner-ID mit einer Ordner-ID übereinstimmt, die von dem Server in einer vorherigen Synchronisierungsantwort zurückgegeben wurde.  <br/> |
|ErrorTimeoutExpired  <br/> |Senden Sie zu viele Anforderungen.  <br/> |Beschränken der Batches auf 10 Elemente pro Batch, um eine [Drosselung](ews-throttling-in-exchange.md)zu vermeiden.  <br/> |
|[ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx) <br/> |Stellen Sie eine Verbindung mit EWS her, wenn der Server offline ist oder wenn ein Problem mit der Konnektivität vorliegt.  <br/> |Überprüfen der Konnektivität mit dem Server und erneutes Testen der Anforderung. Dies ist wahrscheinlich ein vorübergehender Dienstfehler oder Netzwerkfehler.  <br/> |
   
## <a name="see-also"></a>Siehe auch


- [Postfachsynchronisierung und EWS in Exchange](mailbox-synchronization-and-ews-in-exchange.md)
    
- [Synchronisieren von Ordnern unter Verwendung von EWS in Exchange](how-to-synchronize-folders-by-using-ews-in-exchange.md)
    
- [Synchronisieren von Elementen unter Verwendung von EWS in Exchange](how-to-synchronize-items-by-using-ews-in-exchange.md)
    
- [ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)
    

