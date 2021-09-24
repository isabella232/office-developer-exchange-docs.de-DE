---
title: BaseShape
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- BaseShape
api_type:
- schema
ms.assetid: 42c04f3b-abaa-4197-a3d6-d21677ffb1c0
description: Das BaseShape-Element identifiziert den Satz von Eigenschaften, die in einer Element- oder Ordnerantwort zurückgegeben werden sollen.
ms.openlocfilehash: b4e7f5c6d6520e7338f274b6275e371366b1bed5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514858"
---
# <a name="baseshape"></a>BaseShape

Das **BaseShape-Element** identifiziert den Satz von Eigenschaften, die in einer Element- oder Ordnerantwort zurückgegeben werden sollen. 
  
```xml
<BaseShape>IdOnly or Default or AllProperties</BaseShape>
```

 **DefaultShapeNamesType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keines
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> | Identifies the folder properties to include in the GetFolder, FindFolder, or SyncFolderHierarchy response.<br/><br/>Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>`/GetFolder/FolderShape` <br/>  `/FindFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[ItemShape](itemshape.md) <br/> | Identifiziert die Elementeigenschaften und -inhalte, die in eine GetItem-, FindItem- oder SyncFolderItems-Antwort eingeschlossen werden sollen.<br/><br/>Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>`/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. In der folgenden Tabelle sind die möglichen Textwerte aufgeführt.
  
**Textwerte für das BaseShape-Element**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|IdOnly  <br/> |Gibt nur die Element- oder Ordner-ID zurück.  <br/> |
|Standard  <br/> |Gibt einen Satz von Eigenschaften zurück, die als Standard für das Element oder den Ordner definiert sind.  <br/> |
|AllProperties  <br/> |Gibt alle Eigenschaften zurück, die von der Exchange Geschäftslogikebene zum Erstellen eines Ordners verwendet werden.  <br/> |
   
In der folgenden Tabelle sind die Standardeigenschaften aufgeführt, die für eine FindFolder-Anforderung zurückgegeben werden. Alle Unterordner eines bestimmten Ordners werden nach Namen sortiert zurückgegeben.
  
**Standardeigenschaften**

|**Ordner**|**Standardeigenschaften**|
|:-----|:-----|
|Posteingang  <br/> |FolderId, Anzeigename, ungelesene Anzahl, Gesamtanzahl, Unterordneranzahl  <br/> |
|Kontakte  <br/> |FolderId, Anzeigename, Gesamtanzahl, Unterordneranzahl  <br/> |
|Kalender  <br/> |FolderId, Anzeigename, Unterordneranzahl  <br/> |
|Entwürfe  <br/> |FolderId, Anzeigename, ungelesene Anzahl, Gesamtanzahl, Unterordneranzahl  <br/> |
|Gelöschte Elemente  <br/> |FolderId, Anzeigename, ungelesene Anzahl, Gesamtanzahl, Unterordneranzahl  <br/> |
|Andere Ordner  <br/> |FolderId, Anzeigename, ungelesene Anzahl, Gesamtanzahl, Unterordneranzahl  <br/> |
|Postausgang  <br/> |FolderId, Anzeigename, ungelesene Anzahl, Gesamtanzahl, Unterordneranzahl  <br/> |
|Aufgaben  <br/> |FolderId, Anzeigename, Überfällige Anzahl, Gesamtanzahl, Unterordneranzahl  <br/> |
|Notizen  <br/> |FolderId, Anzeigename, Gesamtanzahl, Unterordneranzahl  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie das [AdditionalProperties-Element,](additionalproperties.md) um zusätzlich zu den vom [BaseShape-Element](baseshape.md) identifizierten Eigenschaften Eigenschaften zurückzugeben. 
  
## <a name="example"></a>Beispiel

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [FolderShape](foldershape.md)
- [ItemShape](itemshape.md)

