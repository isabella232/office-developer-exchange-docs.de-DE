---
title: Fehlerbehandlung Synchronisierung-bezogene in EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a0807b90-645a-4ea6-aee1-96828df14be0
description: Erfahren Sie, wie Synchronisierung-bezogene Behandlung von Fehlern in Anwendungen, die Sie entwickeln, indem Sie die EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: 6de27d585e467d900941f34b2210877d17205502
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756836"
---
# <a name="handling-synchronization-related-errors-in-ews-in-exchange"></a>Fehlerbehandlung Synchronisierung-bezogene in EWS in Exchange

Erfahren Sie, wie Synchronisierung-bezogene Behandlung von Fehlern in Anwendungen, die Sie entwickeln, indem Sie die EWS Managed API oder EWS in Exchange.
  
Wenn Ihre Anwendung Elemente und Ordner synchronisiert wird, müssen Sie möglicherweise Synchronisierung-bezogene Fehler zu behandeln. Sie können diese Fehler zur Laufzeit oder während Sie die EWS-Anwendung entwickeln behandeln. Die meisten dieser Fehler werden durch die [ResponseCodeType](http://msdn.microsoft.com/en-us/library/exchangewebservices.responsecodetype%28v=exchg.80%29.aspx) -Aufzählung in die EWS Managed API und das [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) -Element in der Exchange-Webdienste (EWS) definiert. 
  
**In Tabelle 1. Sync-bezogene Fehler und deren Behandlung**

|**Fehler**|**Tritt auf, wenn Sie versuchen...**|**Behandeln von...**|
|:-----|:-----|:-----|
|ErrorInvalidSyncStateData  <br/> | Synchronisieren Sie Elemente oder Ordner mithilfe von eine ungültige Sync-Statuswert.  <br/>  Schließen Sie einen Stammordner in Ihrer anfänglichen SyncFolderHierarchy Anforderung aus, wenn Ihre nachfolgende Anforderung einen Stammordner.  <br/>  Verwenden Sie unterschiedliche Stammordner in nachfolgenden Anforderungen.  <br/> | Sicherstellen, dass der Wert der Sync-Zustand, den Sie Übereinstimmungen Senden der Statuswert Sync während einer vorherigen Synchronisierung zurückgegeben.  <br/>  Sicherstellen, dass Sie den Synchronisierungsstatus beim Synchronisieren von Elementen, nicht für die Ordnerhierarchie senden und umgekehrt.  <br/>  Sicherstellen, dass Sie den Synchronisierungsstatus für den richtigen Stammordner senden.  <br/>  Sicherstellen, dass der gleichen Stammordner in jeder Anforderung angegeben ist.  <br/>  Sicherstellen, dass die vorherige Anforderung nicht einen Stammordner NULL, angegeben haben während die aktuelle Anforderung einen Stammordner der Stammzertifizierungsstellen enthält. NULL und die Stammwebsitesammlung sind nicht die gleiche Weise behandelt.  <br/> |
|ErrorSyncFolderNotFound  <br/> |Synchronisieren von Unterordnern oder Elementen in einem Ordner, der auf dem Server nicht gefunden werden kann.  <br/> |Sicherstellen, dass des Ordners-ID in der Anforderung angegebene ermittelt eine Ordner-ID, die in einer vorherigen Sync-Antwort vom Server zurückgegeben.  <br/> |
|ErrorTimeoutExpired  <br/> |Senden Sie zu viele Anforderungen.  <br/> |Begrenzen Ihre Batches auf 10 Elemente pro Batch von [gedrosselt](ews-throttling-in-exchange.md)zu vermeiden.  <br/> |
|[ServiceResponseException](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx) <br/> |Verbinden Sie mit EWS auf, wenn der Server offline ist oder ein Problem mit der Konnektivität vorliegt.  <br/> |Überprüfen der Konnektivität mit dem Server, und wiederholen die Anforderung weiter unten. Dies ist wahrscheinlich eine vorübergehende Dienstfehler oder Netzwerkfehler.  <br/> |
   
## <a name="see-also"></a>Siehe auch


- [Postfachsynchronisierung und EWS in Exchange](mailbox-synchronization-and-ews-in-exchange.md)
    
- [Synchronisieren von Ordnern in Exchange mithilfe der Exchange-Webdienste](how-to-synchronize-folders-by-using-ews-in-exchange.md)
    
- [Synchronisieren von Elementen mithilfe von EWS in Exchange](how-to-synchronize-items-by-using-ews-in-exchange.md)
    
- [ServiceResponseException](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)
    

