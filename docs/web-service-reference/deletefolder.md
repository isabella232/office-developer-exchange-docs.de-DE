---
title: DeleteFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DeleteFolder
api_type:
- schema
ms.assetid: e37963f4-af9e-4481-b389-16175711e66d
description: Das DeleteFolder-Element definiert eine Anforderung zum Löschen von Ordnern aus einem Postfach im Exchange Speicher.
ms.openlocfilehash: d1d64b84604acec54d9153144e5bfd7abaece94c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542477"
---
# <a name="deletefolder"></a>DeleteFolder

Das **DeleteFolder-Element** definiert eine Anforderung zum Löschen von Ordnern aus einem Postfach im Exchange Speicher. 
  
```XML
<DeleteFolder DeleteType="">
   <FolderIds/>
</DeleteFolder>
```

 **DeleteFolderType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**DeleteType** <br/> |Beschreibt, wie ein Ordner gelöscht wird. Dieses Attribut ist erforderlich.  <br/> |
   
#### <a name="deletetype-attribute"></a>DeleteType-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|HardDelete  <br/> |Ein Ordner wird dauerhaft aus dem Speicher entfernt.  <br/> |
|SoftDelete  <br/> |Ein Ordner wird in den Dumpster verschoben, wenn der Dumpster aktiviert ist.  <br/> |
|MoveToDeletedItems  <br/> |Ein Ordner wird in den Ordner "Gelöschte Elemente" verschoben.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderIds](folderids.md) <br/> |Enthält ein Array von Ordnerbezeichnern, die zum Identifizieren von zu löschenden Ordnern verwendet werden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine
  
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Die Optionen **MoveToDeletedItems** und **HardDelete** sind transaktional, d. h., wenn ein Webdienstaufruf abgeschlossen ist, hat die Datenbank das Element in den Ordner "Gelöschte Elemente" verschoben oder das Element dauerhaft aus der Exchange Datenbank entfernt. Dieses Verhalten ist für MicrosoftExchange Server 2007 und Exchange Server 2010 identisch. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [DeleteFolder-Vorgang](deletefolder-operation.md)

