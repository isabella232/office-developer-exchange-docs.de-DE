---
title: SavedItemFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SavedItemFolderId
api_type:
- schema
ms.assetid: 4b8b475c-9ca5-48c9-acb0-8848b53be1ce
description: Das SavedItemFolderId-Element identifiziert den Zielordner für Vorgänge, die Elemente in einem Postfach aktualisieren, senden und erstellen.
ms.openlocfilehash: 75245cf842336621aa098c115d62a7802711dd54
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546119"
---
# <a name="saveditemfolderid"></a>SavedItemFolderId

Das **SavedItemFolderId-Element** identifiziert den Zielordner für Vorgänge, die Elemente in einem Postfach aktualisieren, senden und erstellen. 
  
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
|[FolderId](folderid.md) <br/> |Enthält den Bezeichner und den Änderungsschlüssel eines Zielordners für Vorgänge, die Elemente im Exchange Speicher aktualisieren, senden und erstellen.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifiziert einen Zielordner anhand eines benannten Bezeichners für Vorgänge, die Elemente im Exchange Speicher aktualisieren, senden und erstellen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CreateItem](createitem.md) <br/> |Definiert eine Anforderung zum Erstellen eines Elements im Exchange Speicher.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/CreateItem` <br/> |
|[UpdateItem](updateitem.md) <br/> |Definiert eine Anforderung zum Aktualisieren eines Elements im Exchange Speicher.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/UpdateItem` <br/> |
|[SendItem](senditem.md) <br/> |Definiert eine Anforderung zum Senden eines Elements im Exchange Speicher.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/SendItem` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   

