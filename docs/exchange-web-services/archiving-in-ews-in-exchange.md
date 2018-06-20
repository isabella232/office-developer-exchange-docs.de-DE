---
title: Archivierung in EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 78ae179b-ae4f-4f64-911a-e0c70e0fa314
description: Informationen Sie zu Archivierung in EWS in Exchange.
ms.openlocfilehash: bc282a7774bb74e57550bc663512987839324b83
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756813"
---
# <a name="archiving-in-ews-in-exchange"></a>Archivierung in EWS in Exchange

Informationen Sie zu Archivierung in EWS in Exchange.
  
Archivpostfächer sind sekundäre Postfächer, die einem Benutzer zugeordnet sind. Archivpostfächer sind in der Regel zum Verwalten von Speichergrenzen für e-Mail verwendet. Beispielsweise könnte der älteren e-Mail-Elemente in regelmäßigen Abständen aus dem Posteingang in das Archivpostfach verschoben werden. 
  
Exchange Online, Exchange Online als Teil von Office 365 und Exchange Server 2013 eine Einführung in zwei neue Exchange-Webdienste (EWS)-Vorgänge, die Sie verwenden können, um eine Reihe von e-Mail-Elementen aus einem primären Postfach archivieren. Archivierung von Elementen im Posteingang auf diese Weise wird die Hierarchie der Ordner Elemente beibehalten. Darüber hinaus können archivpostfächer jetzt gespeichert werden, entweder lokal auf einem Client oder Remote, in eine Möglichkeit, die mit einem Ordnerpfad auf den Inhalt des Archivs zeigen hauptsächlich an einen Benutzer nicht transparent ist.
  
## <a name="archiving-operations-in-ews"></a>Archivierung in Exchange-Webdienste

Die folgende Tabelle enthält die Archivierung Vorgänge, die in Exchange 2013 eingeführt wurden. 
  
|**Name des Vorgangs**|**Beschreibung**|
|:-----|:-----|
|[ArchiveItem](http://msdn.microsoft.com/library/1af216b3-13ea-498e-b4fc-23513755d731%28Office.15%29.aspx) <br/> |Verschiebt ein Element aus dem Hauptpostfach in das Archivpostfach.  <br/> |
|[CreateFolderPath](http://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |Erstellt einen URI, der auf den Speicherort für das Archivpostfach verweist.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [Erste Schritte mit Webdiensten in Exchange](start-using-web-services-in-exchange.md)
    
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)
    

