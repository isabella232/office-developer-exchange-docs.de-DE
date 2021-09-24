---
title: Archivierung in EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 78ae179b-ae4f-4f64-911a-e0c70e0fa314
description: Erfahren Sie mehr über die Archivierung in EWS in Exchange.
ms.openlocfilehash: f2ca4cc783556b089b732c75d166b77c0dcd891c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520227"
---
# <a name="archiving-in-ews-in-exchange"></a>Archivierung in EWS in Exchange

Erfahren Sie mehr über die Archivierung in EWS in Exchange.
  
Archivpostfächer sind sekundäre Postfächer, die einem Benutzer zugeordnet sind. Archivpostfächer werden in der Regel zum Verwalten von E-Mail-Speicherlimits verwendet. Beispielsweise können ältere E-Mail-Elemente in regelmäßigen Abständen aus dem Posteingang in das Archivpostfach verschoben werden. 
  
Exchange Online führen Exchange Online im Rahmen von Office 365 und Exchange Server 2013 zwei neue EWS-Vorgänge (Exchange Web Services) ein, mit denen Sie eine Gruppe von E-Mail-Elementen aus einem primären Postfach archivieren können. Die Archivierung von Posteingangselementen auf diese Weise behält die Ordnerhierarchie der Elemente bei. Darüber hinaus können Archivpostfächer jetzt entweder lokal auf einem Client oder remote auf eine für einen Benutzer undurchsichtige Weise gespeichert werden, indem ein Ordnerpfad verwendet wird, um auf den Inhalt des Archivs zu zeigen.
  
## <a name="archiving-operations-in-ews"></a>Archivierungsvorgänge in EWS

In der folgenden Tabelle sind die Archivierungsvorgänge aufgeführt, die in Exchange 2013 eingeführt wurden. 
  
|**Name des Vorgangs**|**Beschreibung**|
|:-----|:-----|
|[ArchiveItem](https://msdn.microsoft.com/library/1af216b3-13ea-498e-b4fc-23513755d731%28Office.15%29.aspx) <br/> |Verschiebt ein Element aus dem primären Postfach in das Archivpostfach.  <br/> |
|[CreateFolderPath](https://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |Erstellt einen URI, der auf den Speicherort für das Archivpostfach verweist.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [Erste Schritte mit Webdiensten in Exchange](start-using-web-services-in-exchange.md)
    
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)
    

