---
title: Updates (Ordner)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Updates
api_type:
- schema
ms.assetid: b047e3a4-a5ab-4098-b7a0-273bc809e702
description: Das Updates-Element enthält eine Reihe von Elementen, die Änderungen an Ordnereigenschaften definieren, festlegen und löschen.
ms.openlocfilehash: cb40f2a5b66f407b02c636c5115bcab5d382a6fd
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510764"
---
# <a name="updates-folder"></a>Updates (Ordner)

Das **Updates-Element** enthält eine Reihe von Elementen, die Änderungen an Ordnereigenschaften definieren, festlegen und löschen. 
  
- [UpdateFolder](updatefolder.md)
  
- [FolderChanges](folderchanges.md)
  
- [FolderChange](folderchange.md)
  
- [Updates (Ordner)](updates-folder.md)
  
```xml
<Updates>
   <AppendToFolderField/>
   <SetFolderField/>
   <DeleteFolderField/>
</Updates>
```

**NonEmptyArrayOfFolderChangeDescriptionsType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AppendToFolderField](appendtofolderfield.md) <br/> |Stellt Daten dar, die während eines [UpdateFolder-Vorgangs](updatefolder-operation.md)an eine Ordnereigenschaft angefügt werden sollen.  <br/> |
|[SetFolderField](setfolderfield.md) <br/> |Stellt eine Aktualisierung auf eine einzelne Eigenschaft in einem Ordner in einer [UpdateFolder-Vorgang](updatefolder-operation.md)dar.  <br/> |
|[DeleteFolderField](deletefolderfield.md) <br/> |Stellt einen Vorgang zum Löschen einer bestimmten Eigenschaft aus einem Ordner während eines [UpdateFolder-Vorgangs](updatefolder-operation.md)dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderChange](folderchange.md) <br/> |Stellt eine Auflistung von Änderungen dar, die für einen einzelnen Ordner ausgeführt werden sollen.  <br/> Es folgt der XPath-Ausdruck für dieses Element:  `/UpdateFolder/FolderChanges/FolderChange[i]` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [UpdateFolder-Vorgang](updatefolder-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

