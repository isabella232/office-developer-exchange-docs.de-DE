---
title: Archivierung in EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 78ae179b-ae4f-4f64-911a-e0c70e0fa314
description: Erfahren Sie mehr über die Archivierung in EWS in Exchange.
ms.openlocfilehash: b433b9f88905ee255720e8b341d560fa0e464975
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456213"
---
# <a name="archiving-in-ews-in-exchange"></a>Archivierung in EWS in Exchange

Erfahren Sie mehr über die Archivierung in EWS in Exchange.
  
Archivpostfächer sind sekundäre Postfächer, die einem Benutzer zugeordnet sind. Archivpostfächer werden in der Regel zum Verwalten von e-Mail-Speichergrenzwerten verwendet. Beispielsweise können ältere e-Mail-Elemente in regelmäßigen Abständen aus dem Posteingang in das Archivpostfach verschoben werden. 
  
Exchange Online, Exchange Online im Rahmen von Office 365 und Exchange Server 2013 Einführung zweier neuer Exchange-Webdienste Vorgänge, die Sie zum Archivieren einer Gruppe von e-Mail-Elementen aus einem primären Postfach verwenden können. Wenn Sie Posteingangs Elemente auf diese Weise archivieren, wird die Ordnerhierarchie der Elemente beibehalten. Darüber hinaus können Archivpostfächer nun entweder lokal auf einem Client oder Remote in einer für einen Benutzer undurchsichtigen Weise gespeichert werden, indem ein Ordnerpfad verwendet wird, um auf den Inhalt des Archivs zu deuten.
  
## <a name="archiving-operations-in-ews"></a>Archivierungsvorgänge in EWS

In der folgenden Tabelle sind die in Exchange 2013 eingeführten Archivierungsvorgänge aufgeführt. 
  
|**Name des Vorgangs**|**Beschreibung**|
|:-----|:-----|
|[ArchiveItem](https://msdn.microsoft.com/library/1af216b3-13ea-498e-b4fc-23513755d731%28Office.15%29.aspx) <br/> |Verschiebt ein Element aus dem primären Postfach in das Archivpostfach.  <br/> |
|[CreateFolderPath](https://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |Erstellt einen URI, der auf den Speicherort für das Archivpostfach zeigt.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [Erste Schritte mit Webdiensten in Exchange](start-using-web-services-in-exchange.md)
    
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)
    

