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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460995"
---
# <a name="finditem"></a><span data-ttu-id="3c76e-103">FindItem</span><span class="sxs-lookup"><span data-stu-id="3c76e-103">FindItem</span></span>

<span data-ttu-id="3c76e-104">Das **FindItem** -Element definiert eine Anforderung zum Suchen von Elementen in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="3c76e-104">The **FindItem** element defines a request to find items in a mailbox.</span></span> 
  
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


<span data-ttu-id="3c76e-105">**FindItemType**</span><span class="sxs-lookup"><span data-stu-id="3c76e-105">**FindItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="3c76e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3c76e-106">Attributes and elements</span></span>

<span data-ttu-id="3c76e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3c76e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3c76e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3c76e-108">Attributes</span></span>

|<span data-ttu-id="3c76e-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="3c76e-109">**Attribute**</span></span>|<span data-ttu-id="3c76e-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3c76e-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3c76e-111">**Traversal**</span><span class="sxs-lookup"><span data-stu-id="3c76e-111">**Traversal**</span></span> <br/> |<span data-ttu-id="3c76e-112">Definiert, ob die Suche Elemente in Ordnern oder in den Papier korben der Ordner findet.</span><span class="sxs-lookup"><span data-stu-id="3c76e-112">Defines whether the search finds items in folders or the folders' dumpsters.</span></span> <span data-ttu-id="3c76e-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3c76e-113">This attribute is required.</span></span>  <br/> |
   
#### <a name="traversal-attribute-values"></a><span data-ttu-id="3c76e-114">Traversal-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="3c76e-114">Traversal attribute values</span></span>

|<span data-ttu-id="3c76e-115">**Wert**</span><span class="sxs-lookup"><span data-stu-id="3c76e-115">**Value**</span></span>|<span data-ttu-id="3c76e-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3c76e-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3c76e-117">Flachen</span><span class="sxs-lookup"><span data-stu-id="3c76e-117">Shallow</span></span>  <br/> |<span data-ttu-id="3c76e-118">Gibt nur die Identitäten von Elementen im Ordner zurück.</span><span class="sxs-lookup"><span data-stu-id="3c76e-118">Returns only the identities of items in the folder.</span></span>  <br/> |
|<span data-ttu-id="3c76e-119">SoftDeleted</span><span class="sxs-lookup"><span data-stu-id="3c76e-119">SoftDeleted</span></span>  <br/> |<span data-ttu-id="3c76e-120">Gibt nur die Identitäten von Elementen zurück, die sich im Papierkorb eines Ordners befinden.</span><span class="sxs-lookup"><span data-stu-id="3c76e-120">Returns only the identities of items that are in a folder's dumpster.</span></span> <span data-ttu-id="3c76e-121">Beachten Sie, dass durch einen weich gelöschten Durchlauf in Kombination mit einer sucheinschränkung keine Elemente zurückgegeben werden, auch wenn es Elemente gibt, die mit den Suchkriterien übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3c76e-121">Note that a soft-deleted traversal combined with a search restriction will result in zero items returned even if there are items that match the search criteria.</span></span>  <br/> |
|<span data-ttu-id="3c76e-122">Zugeordnet</span><span class="sxs-lookup"><span data-stu-id="3c76e-122">Associated</span></span>  <br/> |<span data-ttu-id="3c76e-123">Gibt nur die Identitäten der zugeordneten Elemente im Ordner zurück.</span><span class="sxs-lookup"><span data-stu-id="3c76e-123">Returns only the identities of associated items in the folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3c76e-124">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3c76e-124">Child elements</span></span>

|<span data-ttu-id="3c76e-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="3c76e-125">**Element**</span></span>|<span data-ttu-id="3c76e-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3c76e-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3c76e-127">ItemShape</span><span class="sxs-lookup"><span data-stu-id="3c76e-127">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="3c76e-128">Identifiziert die Elementeigenschaften und Inhalte, die in eine [FindItem-Vorgangs](finditem-operation.md) Antwort eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3c76e-128">Identifies the item properties and content to include in a [FindItem operation](finditem-operation.md) response.</span></span>  <br/> |
|[<span data-ttu-id="3c76e-129">IndexedPageItemView</span><span class="sxs-lookup"><span data-stu-id="3c76e-129">IndexedPageItemView</span></span>](indexedpageitemview.md) <br/> |<span data-ttu-id="3c76e-130">Beschreibt, wie Informationen zum ausgelagerten Element für eine **FindItem** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3c76e-130">Describes how paged item information is returned for a **FindItem** request.</span></span> <span data-ttu-id="3c76e-131">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="3c76e-131">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3c76e-132">FractionalPageItemView</span><span class="sxs-lookup"><span data-stu-id="3c76e-132">FractionalPageItemView</span></span>](fractionalpageitemview.md) <br/> |<span data-ttu-id="3c76e-133">Beschreibt, wo die ausgelagerte Ansicht beginnt und die maximale Anzahl von Elementen, die in einer **FindItem** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3c76e-133">Describes where the paged view starts and the maximum number of items returned in a **FindItem** request.</span></span> <span data-ttu-id="3c76e-134">Der Offset der Seitenansicht vom Anfang der Gruppe gefundener Elemente wird durch einen Bruch beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3c76e-134">The paged view offset from the beginning of the set of found items is described by a fraction.</span></span> <span data-ttu-id="3c76e-135">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="3c76e-135">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3c76e-136">CalendarView</span><span class="sxs-lookup"><span data-stu-id="3c76e-136">CalendarView</span></span>](calendarview.md) <br/> |<span data-ttu-id="3c76e-137">Bietet Zeitspannen Grenzen zum Definieren einer Suche nach Kalenderelementen.</span><span class="sxs-lookup"><span data-stu-id="3c76e-137">Provides time span limits to define a search for calendar items.</span></span> <span data-ttu-id="3c76e-138">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="3c76e-138">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3c76e-139">ContactsView</span><span class="sxs-lookup"><span data-stu-id="3c76e-139">ContactsView</span></span>](contactsview.md) <br/> |<span data-ttu-id="3c76e-140">Definiert eine Suche nach Kontaktelementen basierend auf alphabetischen Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="3c76e-140">Defines a search for contact items based on alphabetical display names.</span></span> <span data-ttu-id="3c76e-141">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="3c76e-141">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3c76e-142">GroupBy</span><span class="sxs-lookup"><span data-stu-id="3c76e-142">GroupBy</span></span>](groupby.md) <br/> |<span data-ttu-id="3c76e-143">Gibt willkürliche Gruppierungen für **FindItem** -Abfragen an.</span><span class="sxs-lookup"><span data-stu-id="3c76e-143">Specifies arbitrary groupings for **FindItem** queries.</span></span> <span data-ttu-id="3c76e-144">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="3c76e-144">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3c76e-145">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="3c76e-145">DistinguishedGroupBy</span></span>](distinguishedgroupby.md) <br/> |<span data-ttu-id="3c76e-146">Stellt Standardgruppierungen für **FindItem** -Abfragen bereit.</span><span class="sxs-lookup"><span data-stu-id="3c76e-146">Provides standard groupings for **FindItem** queries.</span></span> <span data-ttu-id="3c76e-147">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="3c76e-147">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3c76e-148">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="3c76e-148">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="3c76e-149">Definiert die Einschränkung oder Abfrage, die zum Filtern von Elementen oder Ordnern in **FindItem** /  -**FindFolder** und Suchordner Vorgängen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3c76e-149">Defines the restriction or query that is used to filter items or folders in **FindItem**/ **FindFolder** and search folder operations.</span></span> <span data-ttu-id="3c76e-150">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="3c76e-150">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3c76e-151">SortOrder</span><span class="sxs-lookup"><span data-stu-id="3c76e-151">SortOrder</span></span>](sortorder.md) <br/> |<span data-ttu-id="3c76e-152">Definiert, wie Elemente in einer FindItem-Anforderung sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="3c76e-152">Defines how items are sorted in a FindItem request.</span></span> <span data-ttu-id="3c76e-153">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="3c76e-153">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3c76e-154">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="3c76e-154">ParentFolderIds</span></span>](parentfolderids.md) <br/> |<span data-ttu-id="3c76e-155">Identifiziert Ordner, die für die FindItem-und FindFolder-Vorgänge gesucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3c76e-155">Identifies folders to search for the FindItem and FindFolder operations.</span></span>  <br/> |
|[<span data-ttu-id="3c76e-156">QueryString (querystringtype)</span><span class="sxs-lookup"><span data-stu-id="3c76e-156">QueryString (QueryStringType)</span></span>](querystring-querystringtype.md) <br/> |<span data-ttu-id="3c76e-157">Enthält eine Post Fach Abfragezeichenfolge basierend auf der erweiterten Abfrage Syntax (AQS).</span><span class="sxs-lookup"><span data-stu-id="3c76e-157">Contains a mailbox query string based on Advanced Query Syntax (AQS).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3c76e-158">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3c76e-158">Parent elements</span></span>

<span data-ttu-id="3c76e-159">Keine.</span><span class="sxs-lookup"><span data-stu-id="3c76e-159">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3c76e-160">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c76e-160">Remarks</span></span>

<span data-ttu-id="3c76e-161">Nur eines der [IndexedPageItemView](indexedpageitemview.md)-, [FractionalPageItemView](fractionalpageitemview.md)-, [CalendarView](calendarview.md)-oder [ContactsView](contactsview.md) -Elemente kann in eine **FindItem** -Anforderung eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="3c76e-161">Only one of the [IndexedPageItemView](indexedpageitemview.md), [FractionalPageItemView](fractionalpageitemview.md), [CalendarView](calendarview.md), or [ContactsView](contactsview.md) elements can be included in a **FindItem** request.</span></span> <span data-ttu-id="3c76e-162">Nur eines der [GroupBy](groupby.md) -oder [DistinguishedGroupBy](distinguishedgroupby.md) -Elemente kann in eine **FindItem** -Anforderung eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="3c76e-162">Only one of the [GroupBy](groupby.md) or [DistinguishedGroupBy](distinguishedgroupby.md) elements can be included in a **FindItem** request.</span></span> 
  
<span data-ttu-id="3c76e-163">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3c76e-163">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3c76e-164">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3c76e-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c76e-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="3c76e-165">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3c76e-166">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3c76e-166">Schema Name</span></span>  <br/> |<span data-ttu-id="3c76e-167">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="3c76e-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3c76e-168">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3c76e-168">Validation File</span></span>  <br/> |<span data-ttu-id="3c76e-169">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="3c76e-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3c76e-170">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3c76e-170">Can be Empty</span></span>  <br/> |<span data-ttu-id="3c76e-171">False</span><span class="sxs-lookup"><span data-stu-id="3c76e-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3c76e-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c76e-172">See also</span></span>

- [<span data-ttu-id="3c76e-173">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3c76e-173">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="3c76e-174">Suchen von Elementen</span><span class="sxs-lookup"><span data-stu-id="3c76e-174">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

