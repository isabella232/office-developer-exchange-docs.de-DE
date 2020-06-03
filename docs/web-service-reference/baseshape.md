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
description: Das BaseShape-Element gibt die Gruppe von Eigenschaften an, die in einer Element-oder Ordner Antwort zurückgegeben werden sollen.
ms.openlocfilehash: 9b3f00ff94fbfe6ad6373b16ad95eb9136f81c64
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464490"
---
# <a name="baseshape"></a>BaseShape

Das **BaseShape** -Element gibt die Gruppe von Eigenschaften an, die in einer Element-oder Ordner Antwort zurückgegeben werden sollen. 
  
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
|[FolderShape](foldershape.md) <br/> | Identifiziert die Ordner Eigenschaften, die in die GetFolder-, FindFolder-oder SyncFolderHierarchy-Antwort eingeschlossen werden sollen.<br/><br/>Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>`/GetFolder/FolderShape` <br/>  `/FindFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[ItemShape](itemshape.md) <br/> | Identifiziert die Elementeigenschaften und Inhalte, die in einer GetItem-, FindItem-oder SyncFolderItems-Antwort enthalten sein sollen.<br/><br/>Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>`/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. In der folgenden Tabelle sind die möglichen Text Werte aufgeführt.
  
**Textwerte für das BaseShape-Element**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|IdOnly  <br/> |Gibt nur die Element-oder Ordner-ID zurück.  <br/> |
|Standard  <br/> |Gibt eine Reihe von Eigenschaften zurück, die als Standard für das Element oder den Ordner definiert sind.  <br/> |
|AllProperties  <br/> |Gibt alle Eigenschaften zurück, die von der Exchange-Geschäftslogikschicht zum Erstellen eines Ordners verwendet werden.  <br/> |
   
In der folgenden Tabelle sind die Standardeigenschaften aufgeführt, die für eine FindFolder-Anforderung zurückgegeben werden. Alle Unterordner eines bestimmten Ordners werden in der Reihenfolge nach Namen zurückgegeben.
  
**Standardeigenschaften**

|**Ordner**|**Standardeigenschaften**|
|:-----|:-----|
|Posteingang  <br/> |Ordner-Nr, Anzeigename, ungelesene Anzahl, Gesamtanzahl, Unterordner Anzahl  <br/> |
|Kontakte  <br/> |Ordner-und Anzeigename, Gesamtanzahl, Unterordner Anzahl  <br/> |
|Kalender  <br/> |Ordner-und Anzeigename, Unterordner Anzahl  <br/> |
|Entwürfe  <br/> |Ordner-Nr, Anzeigename, ungelesene Anzahl, Gesamtanzahl, Unterordner Anzahl  <br/> |
|Gelöschte Elemente  <br/> |Ordner-Nr, Anzeigename, ungelesene Anzahl, Gesamtanzahl, Unterordner Anzahl  <br/> |
|Andere Ordner  <br/> |Ordner-Nr, Anzeigename, ungelesene Anzahl, Gesamtanzahl, Unterordner Anzahl  <br/> |
|Postausgang  <br/> |Ordner-Nr, Anzeigename, ungelesene Anzahl, Gesamtanzahl, Unterordner Anzahl  <br/> |
|Aufgaben  <br/> |Ordner-und Anzeigename, überfällige Anzahl, Gesamtanzahl, Unterordner Anzahl  <br/> |
|Notes  <br/> |Ordner-und Anzeigename, Gesamtanzahl, Unterordner Anzahl  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Verwenden Sie das [AdditionalProperties](additionalproperties.md) -Element, um zusätzlich zu den durch das [BaseShape](baseshape.md) -Element identifizierten Eigenschaften zurückzugeben. 
  
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

