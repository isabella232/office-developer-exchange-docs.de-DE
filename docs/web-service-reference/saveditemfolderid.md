---
title: Des SavedItemFolderId
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
ms.openlocfilehash: c57a7fb4abc2f7ee7b599f56f016811d6ff2c21c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831277"
---
# <a name="saveditemfolderid"></a>Des SavedItemFolderId

Das Element **des SavedItemFolderId** identifiziert den Zielordner für Vorgänge, die zu aktualisieren, senden und Elemente in einem Postfach erstellen. 
  
```xml
<SavedItemFolderId>
   <FolderId/>
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
|[CreateItem](createitem.md) <br/> |Definiert eine Anforderung zum Erstellen eines Elements im Exchange-Speicher.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/CreateItem` <br/> |
|[UpdateItem](updateitem.md) <br/> |Definiert eine Anforderung zum Aktualisieren eines Elements in der Exchange-Speicher.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/UpdateItem` <br/> |
|[SendItem](senditem.md) <br/> |Definiert eine Anforderung zum Senden eines Elements im Exchange-Speicher.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/SendItem` <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   

