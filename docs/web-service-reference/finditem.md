---
title: FindItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindItem
api_type:
- schema
ms.assetid: f7624f5c-c390-4563-ab9a-08f1024fb914
description: Das FindItem-Element definiert eine Anforderung zum Suchen von Elementen in einem Postfach.
ms.openlocfilehash: 3aeda1cffc03292734a91bc3fff3289d51c9b445
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460995"
---
# <a name="finditem"></a>FindItem

Das **FindItem** -Element definiert eine Anforderung zum Suchen von Elementen in einem Postfach. 
  
```xml
<FindItem Traversal="">
   <ItemShape/>
   <IndexedPageItemView/>
   <GroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <IndexedPageItemView/>
   <DistinguishedGroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <ContactsView/>
   <GroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <ContactsView/> 
   <DistinguishedGroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <CalendarView/>
   <GroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <FractionalPageItemView/>
   <GroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <FractionalPageItemView/>
   <DistinguishedGroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```


**FindItemType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Traversal** <br/> |Definiert, ob die Suche Elemente in Ordnern oder in den Papier korben der Ordner findet. Dieses Attribut ist erforderlich.  <br/> |
   
#### <a name="traversal-attribute-values"></a>Traversal-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Flachen  <br/> |Gibt nur die Identitäten von Elementen im Ordner zurück.  <br/> |
|SoftDeleted  <br/> |Gibt nur die Identitäten von Elementen zurück, die sich im Papierkorb eines Ordners befinden. Beachten Sie, dass durch einen weich gelöschten Durchlauf in Kombination mit einer sucheinschränkung keine Elemente zurückgegeben werden, auch wenn es Elemente gibt, die mit den Suchkriterien übereinstimmen.  <br/> |
|Zugeordnet  <br/> |Gibt nur die Identitäten der zugeordneten Elemente im Ordner zurück.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> |Identifiziert die Elementeigenschaften und Inhalte, die in eine [FindItem-Vorgangs](finditem-operation.md) Antwort eingeschlossen werden sollen.  <br/> |
|[IndexedPageItemView](indexedpageitemview.md) <br/> |Beschreibt, wie Informationen zum ausgelagerten Element für eine **FindItem** -Anforderung zurückgegeben werden. Dieses Element ist optional.  <br/> |
|[FractionalPageItemView](fractionalpageitemview.md) <br/> |Beschreibt, wo die ausgelagerte Ansicht beginnt und die maximale Anzahl von Elementen, die in einer **FindItem** -Anforderung zurückgegeben werden. Der Offset der Seitenansicht vom Anfang der Gruppe gefundener Elemente wird durch einen Bruch beschrieben. Dieses Element ist optional.  <br/> |
|[CalendarView](calendarview.md) <br/> |Bietet Zeitspannen Grenzen zum Definieren einer Suche nach Kalenderelementen. Dieses Element ist optional.  <br/> |
|[ContactsView](contactsview.md) <br/> |Definiert eine Suche nach Kontaktelementen basierend auf alphabetischen Anzeigenamen. Dieses Element ist optional.  <br/> |
|[GroupBy](groupby.md) <br/> |Gibt willkürliche Gruppierungen für **FindItem** -Abfragen an. Dieses Element ist optional.  <br/> |
|[DistinguishedGroupBy](distinguishedgroupby.md) <br/> |Stellt Standardgruppierungen für **FindItem** -Abfragen bereit. Dieses Element ist optional.  <br/> |
|[Restriction](restriction.md) <br/> |Definiert die Einschränkung oder Abfrage, die zum Filtern von Elementen oder Ordnern in **FindItem** /  -**FindFolder** und Suchordner Vorgängen verwendet wird. Dieses Element ist optional.  <br/> |
|[SortOrder](sortorder.md) <br/> |Definiert, wie Elemente in einer FindItem-Anforderung sortiert werden. Dieses Element ist optional.  <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |Identifiziert Ordner, die für die FindItem-und FindFolder-Vorgänge gesucht werden sollen.  <br/> |
|[QueryString (querystringtype)](querystring-querystringtype.md) <br/> |Enthält eine Post Fach Abfragezeichenfolge basierend auf der erweiterten Abfrage Syntax (AQS).  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Bemerkungen

Nur eines der [IndexedPageItemView](indexedpageitemview.md)-, [FractionalPageItemView](fractionalpageitemview.md)-, [CalendarView](calendarview.md)-oder [ContactsView](contactsview.md) -Elemente kann in eine **FindItem** -Anforderung eingeschlossen werden. Nur eines der [GroupBy](groupby.md) -oder [DistinguishedGroupBy](distinguishedgroupby.md) -Elemente kann in eine **FindItem** -Anforderung eingeschlossen werden. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [FindItem-Vorgang](finditem-operation.md)
- [Finding Items](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

