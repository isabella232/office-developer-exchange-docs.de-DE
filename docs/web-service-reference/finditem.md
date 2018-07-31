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
ms.openlocfilehash: 6664cd91007f1d39db7e8d446e0135f47d5ab932
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353924"
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
|**Durchqueren** <br/> |Definiert, ob die Suche Elemente im Ordner oder die Ordner Pflügen findet. Dieses Attribut ist erforderlich.  <br/> |
   
#### <a name="traversal-attribute-values"></a>Traversal Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Flach  <br/> |Gibt nur die Identitäten der Elemente im Ordner zurück.  <br/> |
|SoftDeleted  <br/> |Gibt nur die Identitäten der Elemente, die in eines Ordners werden muss. Beachten Sie, dass eine vorläufig gelöschten durchqueren in Kombination mit einer Einschränkung Suche keine Elemente zurückgegeben führt, auch wenn es Elemente sind, die den Suchkriterien entsprechen.  <br/> |
|Verknüpft ist  <br/> |Gibt nur die Identitäten verknüpften Elemente im Ordner zurück.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> |Identifiziert die Elementeigenschaften und den Inhalt in einer Antwort [FindItem Vorgang](finditem-operation.md) aufzunehmen.  <br/> |
|[IndexedPageItemView](indexedpageitemview.md) <br/> |Beschreibt, wie ausgelagerten Elementinformationen für eine Anforderung **FindItem** zurückgegeben wird. Dieses Element ist optional.  <br/> |
|[FractionalPageItemView](fractionalpageitemview.md) <br/> |Beschreibt, in der Seitenansicht startet und die maximale Anzahl von Elementen in einer Anforderung **FindItem** zurückgegeben. Der Seitenansicht Offset vom Anfang des Satzes von gefundenen Elemente wird durch eine Bruchzahl beschrieben. Dieses Element ist optional.  <br/> |
|[CalendarView](calendarview.md) <br/> |Bietet Zeit umfassen Grenzwerte, eine Suche für Kalenderelemente zu definieren. Dieses Element ist optional.  <br/> |
|[ContactsView](contactsview.md) <br/> |Definiert eine Suche für Kontaktelemente basierend auf alphabetische Anzeigenamen. Dieses Element ist optional.  <br/> |
|[GroupBy](groupby.md) <br/> |Gibt beliebige Gruppen für **FindItem** Abfragen an. Dieses Element ist optional.  <br/> |
|[DistinguishedGroupBy](distinguishedgroupby.md) <br/> |**FindItem** Abfragen bereit standard Gruppen. Dieses Element ist optional.  <br/> |
|[Einschränkung](restriction.md) <br/> |Definiert die Einschränkung oder Abfrage, die zum Filtern von Elementen oder Ordner in **FindItem**/ **FindFolder** , und suchen Sie Ordner Vorgänge. Dieses Element ist optional.  <br/> |
|[SortOrder](sortorder.md) <br/> |Definiert, wie Elemente in einer Anforderung FindItem sortiert werden. Dieses Element ist optional.  <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |Ordner für die Suche für die Vorgänge FindItem und FindFolder identifiziert.  <br/> |
|[QueryString (QueryStringType)](querystring-querystringtype.md) <br/> |Enthält eine Postfach Abfragezeichenfolge basierend auf Erweiterte Query Syntax (AQS).  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Hinweise

Nur eine der [IndexedPageItemView](indexedpageitemview.md), [FractionalPageItemView](fractionalpageitemview.md), [CalendarView](calendarview.md)oder [ContactsView](contactsview.md) Elemente kann in einer **FindItem** Anforderung enthalten sein. Nur eines der Elemente [GroupBy](groupby.md) oder [DistinguishedGroupBy](distinguishedgroupby.md) kann in einer **FindItem** Anforderung enthalten sein. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [FindItem-Vorgang](finditem-operation.md)
- [Finding Items](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

