---
title: BaseShape
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BaseShape
api_type:
- schema
ms.assetid: 42c04f3b-abaa-4197-a3d6-d21677ffb1c0
description: Das BaseShape-Element identifiziert die Gruppe von Eigenschaften in einer Antwort Elements oder Ordners zurückgegeben werden sollen.
ms.openlocfilehash: 69b27d23fd75d4c1a274f31dfa419b759dbb2bbe
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757439"
---
# <a name="baseshape"></a>BaseShape

Das **BaseShape** -Element identifiziert die Gruppe von Eigenschaften in einer Antwort Elements oder Ordners zurückgegeben werden sollen. 
  
```xml
<BaseShape>IdOnly or Default or AllProperties</BaseShape>
```

 **DefaultShapeNamesType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> | Identifiziert die Ordnereigenschaften in der Antwort GetFolder, FindFolder oder SyncFolderHierarchy aufzunehmen.<br/><br/>Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>`/GetFolder/FolderShape` <br/>  `/FindFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[ItemShape](itemshape.md) <br/> | Identifiziert die Elementeigenschaften und den Inhalt in einer Antwort GetItem, FindItem oder SyncFolderItems aufzunehmen.<br/><br/>Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>`/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Die folgende Tabelle enthält die möglichen Textwerte.
  
**Textwerte für das BaseShape-element**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|IdOnly  <br/> |Gibt nur die ID Elements oder Ordners zurück.  <br/> |
|Standard  <br/> |Gibt einen Satz von Eigenschaften, die als Standard für das Element oder Ordner definiert sind.  <br/> |
|AllProperties  <br/> |Gibt die Eigenschaften, die für die durch die Ebene des Exchange-Geschäftslogik verwendet, um einen Ordner zu erstellen.  <br/> |
   
Die folgende Tabelle enthält die Standardeigenschaften, die für eine Anforderung FindFolder zurückgegeben werden. Alle Unterordner eines bestimmten Ordners werden namentlich in der Reihenfolge zurückgegeben.
  
**Standardeigenschaften**

|**Folder**|**Standardeigenschaften**|
|:-----|:-----|
|Posteingang  <br/> |FolderId, Anzeigename, ungelesenen, Gesamtzahl, Anzahl der Unterordner  <br/> |
|Kontakte  <br/> |FolderId, Anzeigename, Gesamtzahl, Anzahl der Unterordner  <br/> |
|Kalender  <br/> |FolderId, Anzeigename, Anzahl der Unterordner  <br/> |
|Entwürfe  <br/> |FolderId, Anzeigename, ungelesenen, Gesamtzahl, Anzahl der Unterordner  <br/> |
|Gelöschte Elemente  <br/> |FolderId, Anzeigename, ungelesenen, Gesamtzahl, Anzahl der Unterordner  <br/> |
|Andere Ordner  <br/> |FolderId, Anzeigename, ungelesenen, Gesamtzahl, Anzahl der Unterordner  <br/> |
|Postausgang  <br/> |FolderId, Anzeigename, ungelesenen, Gesamtzahl, Anzahl der Unterordner  <br/> |
|Aufgaben  <br/> |FolderId Anzeigename überfälligen Count, Gesamtzahl, Anzahl der Unterordner  <br/> |
|Anmerkungen  <br/> |FolderId, Anzeigename, Gesamtzahl, Anzahl der Unterordner  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Zurückgeben von Eigenschaften zusätzlich zu den durch das [BaseShape](baseshape.md) -Element, das [AdditionalProperties](additionalproperties.md) -Element ein. 
  
## <a name="example"></a>Beispiel

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindFolder>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [FolderShape](foldershape.md)
- [ItemShape](itemshape.md)

