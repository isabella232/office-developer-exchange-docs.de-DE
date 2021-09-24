---
title: FindItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FindItem
api_type:
- schema
ms.assetid: f7624f5c-c390-4563-ab9a-08f1024fb914
description: Das FindItem-Element definiert eine Anforderung zum Suchen nach Elementen in einem Postfach.
ms.openlocfilehash: 7005b4a837c61ffa00a49b687e729de7ed769bcf
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541315"
---
# <a name="finditem"></a>FindItem

Das **FindItem-Element** definiert eine Anforderung zum Suchen nach Elementen in einem Postfach. 
  
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
|**Traversal** <br/> |Definiert, ob die Suche Elemente in Ordnern oder den Dumpstern der Ordner findet. Dieses Attribut ist erforderlich.  <br/> |
   
#### <a name="traversal-attribute-values"></a>Traversalattributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Flachen  <br/> |Gibt nur die Identitäten von Elementen im Ordner zurück.  <br/> |
|Vorläufig gelöscht  <br/> |Gibt nur die Identitäten von Elementen zurück, die sich im Dumpster eines Ordners befinden. Beachten Sie, dass ein vorläufig gelöschtes Traversal in Kombination mit einer Sucheinschränkung zu null zurückgegebenen Elementen führt, auch wenn Elemente vorhanden sind, die den Suchkriterien entsprechen.  <br/> |
|Zugeordneten  <br/> |Gibt nur die Identitäten der zugeordneten Elemente im Ordner zurück.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> |Identifiziert die Elementeigenschaften und -inhalte, die in eine [FindItem-Vorgangsantwort](finditem-operation.md) eingeschlossen werden sollen.  <br/> |
|[IndexedPageItemView](indexedpageitemview.md) <br/> |Beschreibt, wie Seitenelementinformationen für eine **FindItem-Anforderung** zurückgegeben werden. Dieses Element ist optional.  <br/> |
|[FractionalPageItemView](fractionalpageitemview.md) <br/> |Beschreibt, wo die seitenierte Ansicht beginnt, und die maximale Anzahl von Elementen, die in einer **FindItem-Anforderung** zurückgegeben werden. Der Seitenansichtsversatz vom Anfang der Gruppe gefundener Elemente wird durch einen Bruch beschrieben. Dieses Element ist optional.  <br/> |
|[CalendarView](calendarview.md) <br/> |Stellt Zeitlimits bereit, um eine Suche nach Kalenderelementen zu definieren. Dieses Element ist optional.  <br/> |
|[ContactsView](contactsview.md) <br/> |Definiert eine Suche nach Kontaktelementen basierend auf alphabetischen Anzeigenamen. Dieses Element ist optional.  <br/> |
|[GroupBy](groupby.md) <br/> |Gibt beliebige Gruppierungen für **FindItem-Abfragen** an. Dieses Element ist optional.  <br/> |
|[DistinguishedGroupBy](distinguishedgroupby.md) <br/> |Stellt Standardgruppierungen für **FindItem-Abfragen** bereit. Dieses Element ist optional.  <br/> |
|[Restriction](restriction.md) <br/> |Definiert die Einschränkung oder Abfrage, die zum Filtern von Elementen oder Ordnern in **FindItem** /  **FindFolder-** und Suchordnervorgängen verwendet wird. Dieses Element ist optional.  <br/> |
|[SortOrder](sortorder.md) <br/> |Definiert, wie Elemente in einer FindItem-Anforderung sortiert werden. Dieses Element ist optional.  <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |Identifiziert Ordner, die nach den FindItem- und FindFolder-Vorgängen gesucht werden sollen.  <br/> |
|[QueryString (QueryStringType)](querystring-querystringtype.md) <br/> |Enthält eine Postfachabfragezeichenfolge basierend auf der erweiterten Abfragesyntax (Advanced Query Syntax, AQS).  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Nur eines der Elemente [IndexedPageItemView,](indexedpageitemview.md) [FractionalPageItemView,](fractionalpageitemview.md) [CalendarView](calendarview.md)oder [ContactsView](contactsview.md) kann in eine **FindItem-Anforderung** eingeschlossen werden. Nur eines der [GroupBy-](groupby.md) oder [DistinguishedGroupBy-Elemente](distinguishedgroupby.md) kann in eine **FindItem-Anforderung** eingeschlossen werden. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [FindItem-Vorgang](finditem-operation.md)
- [Suchen von Elementen](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

