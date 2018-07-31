---
title: SavedItemFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SavedItemFolderId
api_type:
- schema
ms.assetid: 4b8b475c-9ca5-48c9-acb0-8848b53be1ce
description: Das Element des SavedItemFolderId identifiziert den Zielordner für Vorgänge, die zu aktualisieren, senden und Elemente in einem Postfach erstellen.
ms.openlocfilehash: 3f46070a538f5e03007925565a8888efe06b62b7
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354162"
---
# <a name="saveditemfolderid"></a>SavedItemFolderId

Das Element **des SavedItemFolderId** identifiziert den Zielordner für Vorgänge, die zu aktualisieren, senden und Elemente in einem Postfach erstellen. 
  
```xml
<SavedItemFolderId>
   <FolderId/>
</SavedItemFolderId>
```

```xml
<SavedItemFolderId>
   <DistinguishedFolderId/>
</SavedItemFolderId>
```

**TargetFolderIdType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Enthält den Bezeichner und ein Änderungsprotokoll Schlüssel einen Zielordner für Vorgänge, die zu aktualisieren, senden und Elemente im Exchange-Speicher zu erstellen.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Gibt einen Zielordner durch einen benannten Bezeichner für Vorgänge, die zu aktualisieren, senden und erstellen Sie Elemente im Exchange-Speicher.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CreateItem](createitem.md) <br/> |Definiert eine Anforderung zum Erstellen eines Elements im Exchange-Speicher.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/CreateItem` <br/> |
|[UpdateItem](updateitem.md) <br/> |Definiert eine Anforderung zum Aktualisieren eines Elements in der Exchange-Speicher.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/UpdateItem` <br/> |
|[SendItem](senditem.md) <br/> |Definiert eine Anforderung zum Senden eines Elements im Exchange-Speicher.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/SendItem` <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   

