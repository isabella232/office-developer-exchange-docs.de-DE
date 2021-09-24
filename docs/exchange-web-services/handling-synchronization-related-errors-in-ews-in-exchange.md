---
title: Umgang mit Fehlern im Zusammenhang mit der Synchronisierung in EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: a0807b90-645a-4ea6-aee1-96828df14be0
description: Erfahren Sie, wie Sie Synchronisierungsfehler in Anwendungen behandeln, die Sie entwickeln, indem Sie die verwaltete EWS-API oder EWS in Exchange verwenden.
ms.openlocfilehash: fd52b54413c6fc791132fb01b47bc9077d0266b2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513248"
---
# <a name="handling-synchronization-related-errors-in-ews-in-exchange"></a>Umgang mit Fehlern im Zusammenhang mit der Synchronisierung in EWS in Exchange

Erfahren Sie, wie Sie Synchronisierungsfehler in Anwendungen behandeln, die Sie entwickeln, indem Sie die verwaltete EWS-API oder EWS in Exchange verwenden.
  
Wenn Ihre Anwendung Elemente und Ordner synchronisiert, müssen Sie möglicherweise synchronisierungsbezogene Fehler behandeln. Sie können diese Fehler zur Laufzeit oder während der Entwicklung Ihrer EWS-Anwendung behandeln. Die meisten dieser Fehler werden durch die [ResponseCodeType-Enumeration](https://msdn.microsoft.com/library/exchangewebservices.responsecodetype%28v=exchg.80%29.aspx) in der verwalteten EWS-API und das [ResponseCode-Element](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) in Exchange Webdienste (EWS) definiert. 
  
**Tabelle 1. Synchronisierungsbezogene Fehler und deren Behandlung**

|**Error**|**Tritt auf, wenn Sie versuchen, ...**|**Behandeln von...**|
|:-----|:-----|:-----|
|ErrorInvalidSyncStateData  <br/> | Synchronisieren Sie Elemente oder Ordner mithilfe eines ungültigen Synchronisierungsstatuswerts.  <br/>  Schließen Sie einen Stammordner in Der ursprünglichen SyncFolderHierarchy-Anforderung aus, wenn ihre nachfolgende Anforderung einen Stammordner enthält.  <br/>  Verwenden Sie unterschiedliche Stammordner in nachfolgenden Anforderungen.  <br/> | Stellen Sie sicher, dass der Synchronisierungsstatuswert, den Sie senden, mit dem Synchronisierungsstatuswert übereinstimmt, der während einer vorherigen Synchronisierung zurückgegeben wurde.  <br/>  Sicherstellen, dass Sie beim Versuch, Elemente zu synchronisieren, den Synchronisierungsstatus für die Ordnerhierarchie nicht senden und umgekehrt.  <br/>  Stellen Sie sicher, dass Sie den Synchronisierungsstatus für den richtigen Stammordner senden.  <br/>  Sicherstellen, dass in jeder Anforderung derselbe Stammordner angegeben ist.  <br/>  Sicherstellen, dass in der vorherigen Anforderung kein Stammordner von NULL angegeben wurde, während die aktuelle Anforderung einen Stammordner des Stammordners enthält. Null und Stamm werden nicht gleich behandelt.  <br/> |
|ErrorSyncFolderNotFound  <br/> |Synchronisieren Sie Unterordner oder Elemente in einem Ordner, der auf dem Server nicht gefunden werden kann.  <br/> |Sicherstellen, dass die in der Anforderung angegebene Ordner-ID mit einer Ordner-ID übereinstimmt, die vom Server in einer vorherigen Synchronisierungsantwort zurückgegeben wurde.  <br/> |
|ErrorTimeoutExpired  <br/> |Senden Sie zu viele Anforderungen.  <br/> |Beschränken Sie Ihre Batches auf 10 Elemente pro Batch, um zu vermeiden, dass sie [gedrosselt werden.](ews-throttling-in-exchange.md)  <br/> |
|[ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx) <br/> |Verbinden zu EWS, wenn der Server offline ist oder ein Problem mit der Verbindung besteht.  <br/> |Überprüfen der Verbindung mit dem Server und erneutes Wiederholen Ihrer Anforderung zu einem späteren Zeitpunkt. Dies ist wahrscheinlich ein vorübergehender Dienst- oder Netzwerkfehler.  <br/> |
   
## <a name="see-also"></a>Siehe auch


- [Postfachsynchronisierung und EWS in Exchange](mailbox-synchronization-and-ews-in-exchange.md)
    
- [Synchronisieren von Ordnern unter Verwendung von EWS in Exchange](how-to-synchronize-folders-by-using-ews-in-exchange.md)
    
- [Synchronisieren von Elementen unter Verwendung von EWS in Exchange](how-to-synchronize-items-by-using-ews-in-exchange.md)
    
- [ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)
    

