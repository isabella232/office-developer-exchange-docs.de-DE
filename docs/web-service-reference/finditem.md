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
# <a name="finditem"></a><span data-ttu-id="3ac4f-103">FindItem</span><span class="sxs-lookup"><span data-stu-id="3ac4f-103">FindItem</span></span>

<span data-ttu-id="3ac4f-104">Das **FindItem** -Element definiert eine Anforderung zum Suchen von Elementen in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-104">The **FindItem** element defines a request to find items in a mailbox.</span></span> 
  
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


<span data-ttu-id="3ac4f-105">**FindItemType**</span><span class="sxs-lookup"><span data-stu-id="3ac4f-105">**FindItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="3ac4f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3ac4f-106">Attributes and elements</span></span>

<span data-ttu-id="3ac4f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3ac4f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3ac4f-108">Attributes</span></span>

|<span data-ttu-id="3ac4f-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="3ac4f-109">**Attribute**</span></span>|<span data-ttu-id="3ac4f-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3ac4f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3ac4f-111">**Durchqueren**</span><span class="sxs-lookup"><span data-stu-id="3ac4f-111">**Traversal**</span></span> <br/> |<span data-ttu-id="3ac4f-112">Definiert, ob die Suche Elemente im Ordner oder die Ordner Pflügen findet.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-112">Defines whether the search finds items in folders or the folders' dumpsters.</span></span> <span data-ttu-id="3ac4f-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-113">This attribute is required.</span></span>  <br/> |
   
#### <a name="traversal-attribute-values"></a><span data-ttu-id="3ac4f-114">Traversal Attributwerte</span><span class="sxs-lookup"><span data-stu-id="3ac4f-114">Traversal attribute values</span></span>

|<span data-ttu-id="3ac4f-115">**Wert**</span><span class="sxs-lookup"><span data-stu-id="3ac4f-115">**Value**</span></span>|<span data-ttu-id="3ac4f-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3ac4f-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3ac4f-117">Flach</span><span class="sxs-lookup"><span data-stu-id="3ac4f-117">Shallow</span></span>  <br/> |<span data-ttu-id="3ac4f-118">Gibt nur die Identitäten der Elemente im Ordner zurück.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-118">Returns only the identities of items in the folder.</span></span>  <br/> |
|<span data-ttu-id="3ac4f-119">SoftDeleted</span><span class="sxs-lookup"><span data-stu-id="3ac4f-119">SoftDeleted</span></span>  <br/> |<span data-ttu-id="3ac4f-120">Gibt nur die Identitäten der Elemente, die in eines Ordners werden muss.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-120">Returns only the identities of items that are in a folder's dumpster.</span></span> <span data-ttu-id="3ac4f-121">Beachten Sie, dass eine vorläufig gelöschten durchqueren in Kombination mit einer Einschränkung Suche keine Elemente zurückgegeben führt, auch wenn es Elemente sind, die den Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-121">Note that a soft-deleted traversal combined with a search restriction will result in zero items returned even if there are items that match the search criteria.</span></span>  <br/> |
|<span data-ttu-id="3ac4f-122">Verknüpft ist</span><span class="sxs-lookup"><span data-stu-id="3ac4f-122">Associated</span></span>  <br/> |<span data-ttu-id="3ac4f-123">Gibt nur die Identitäten verknüpften Elemente im Ordner zurück.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-123">Returns only the identities of associated items in the folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3ac4f-124">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3ac4f-124">Child elements</span></span>

|<span data-ttu-id="3ac4f-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="3ac4f-125">**Element**</span></span>|<span data-ttu-id="3ac4f-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3ac4f-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3ac4f-127">ItemShape</span><span class="sxs-lookup"><span data-stu-id="3ac4f-127">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="3ac4f-128">Identifiziert die Elementeigenschaften und den Inhalt in einer Antwort [FindItem Vorgang](finditem-operation.md) aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-128">Identifies the item properties and content to include in a [FindItem operation](finditem-operation.md) response.</span></span>  <br/> |
|[<span data-ttu-id="3ac4f-129">IndexedPageItemView</span><span class="sxs-lookup"><span data-stu-id="3ac4f-129">IndexedPageItemView</span></span>](indexedpageitemview.md) <br/> |<span data-ttu-id="3ac4f-130">Beschreibt, wie ausgelagerten Elementinformationen für eine Anforderung **FindItem** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-130">Describes how paged item information is returned for a **FindItem** request.</span></span> <span data-ttu-id="3ac4f-131">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-131">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3ac4f-132">FractionalPageItemView</span><span class="sxs-lookup"><span data-stu-id="3ac4f-132">FractionalPageItemView</span></span>](fractionalpageitemview.md) <br/> |<span data-ttu-id="3ac4f-133">Beschreibt, in der Seitenansicht startet und die maximale Anzahl von Elementen in einer Anforderung **FindItem** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-133">Describes where the paged view starts and the maximum number of items returned in a **FindItem** request.</span></span> <span data-ttu-id="3ac4f-134">Der Seitenansicht Offset vom Anfang des Satzes von gefundenen Elemente wird durch eine Bruchzahl beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-134">The paged view offset from the beginning of the set of found items is described by a fraction.</span></span> <span data-ttu-id="3ac4f-135">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-135">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3ac4f-136">CalendarView</span><span class="sxs-lookup"><span data-stu-id="3ac4f-136">CalendarView</span></span>](calendarview.md) <br/> |<span data-ttu-id="3ac4f-137">Bietet Zeit umfassen Grenzwerte, eine Suche für Kalenderelemente zu definieren.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-137">Provides time span limits to define a search for calendar items.</span></span> <span data-ttu-id="3ac4f-138">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-138">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3ac4f-139">ContactsView</span><span class="sxs-lookup"><span data-stu-id="3ac4f-139">ContactsView</span></span>](contactsview.md) <br/> |<span data-ttu-id="3ac4f-140">Definiert eine Suche für Kontaktelemente basierend auf alphabetische Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-140">Defines a search for contact items based on alphabetical display names.</span></span> <span data-ttu-id="3ac4f-141">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-141">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3ac4f-142">GroupBy</span><span class="sxs-lookup"><span data-stu-id="3ac4f-142">GroupBy</span></span>](groupby.md) <br/> |<span data-ttu-id="3ac4f-143">Gibt beliebige Gruppen für **FindItem** Abfragen an.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-143">Specifies arbitrary groupings for **FindItem** queries.</span></span> <span data-ttu-id="3ac4f-144">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-144">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3ac4f-145">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="3ac4f-145">DistinguishedGroupBy</span></span>](distinguishedgroupby.md) <br/> |<span data-ttu-id="3ac4f-146">**FindItem** Abfragen bereit standard Gruppen.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-146">Provides standard groupings for **FindItem** queries.</span></span> <span data-ttu-id="3ac4f-147">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-147">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3ac4f-148">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="3ac4f-148">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="3ac4f-149">Definiert die Einschränkung oder Abfrage, die zum Filtern von Elementen oder Ordner in **FindItem**/ **FindFolder** , und suchen Sie Ordner Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-149">Defines the restriction or query that is used to filter items or folders in **FindItem**/ **FindFolder** and search folder operations.</span></span> <span data-ttu-id="3ac4f-150">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-150">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3ac4f-151">SortOrder</span><span class="sxs-lookup"><span data-stu-id="3ac4f-151">SortOrder</span></span>](sortorder.md) <br/> |<span data-ttu-id="3ac4f-152">Definiert, wie Elemente in einer Anforderung FindItem sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-152">Defines how items are sorted in a FindItem request.</span></span> <span data-ttu-id="3ac4f-153">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-153">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3ac4f-154">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="3ac4f-154">ParentFolderIds</span></span>](parentfolderids.md) <br/> |<span data-ttu-id="3ac4f-155">Ordner für die Suche für die Vorgänge FindItem und FindFolder identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-155">Identifies folders to search for the FindItem and FindFolder operations.</span></span>  <br/> |
|[<span data-ttu-id="3ac4f-156">QueryString (QueryStringType)</span><span class="sxs-lookup"><span data-stu-id="3ac4f-156">QueryString (QueryStringType)</span></span>](querystring-querystringtype.md) <br/> |<span data-ttu-id="3ac4f-157">Enthält eine Postfach Abfragezeichenfolge basierend auf Erweiterte Query Syntax (AQS).</span><span class="sxs-lookup"><span data-stu-id="3ac4f-157">Contains a mailbox query string based on Advanced Query Syntax (AQS).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3ac4f-158">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3ac4f-158">Parent elements</span></span>

<span data-ttu-id="3ac4f-159">Keine.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-159">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3ac4f-160">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3ac4f-160">Remarks</span></span>

<span data-ttu-id="3ac4f-161">Nur eine der [IndexedPageItemView](indexedpageitemview.md), [FractionalPageItemView](fractionalpageitemview.md), [CalendarView](calendarview.md)oder [ContactsView](contactsview.md) Elemente kann in einer **FindItem** Anforderung enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-161">Only one of the [IndexedPageItemView](indexedpageitemview.md), [FractionalPageItemView](fractionalpageitemview.md), [CalendarView](calendarview.md), or [ContactsView](contactsview.md) elements can be included in a **FindItem** request.</span></span> <span data-ttu-id="3ac4f-162">Nur eines der Elemente [GroupBy](groupby.md) oder [DistinguishedGroupBy](distinguishedgroupby.md) kann in einer **FindItem** Anforderung enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-162">Only one of the [GroupBy](groupby.md) or [DistinguishedGroupBy](distinguishedgroupby.md) elements can be included in a **FindItem** request.</span></span> 
  
<span data-ttu-id="3ac4f-163">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3ac4f-163">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3ac4f-164">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3ac4f-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3ac4f-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="3ac4f-165">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3ac4f-166">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3ac4f-166">Schema Name</span></span>  <br/> |<span data-ttu-id="3ac4f-167">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="3ac4f-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3ac4f-168">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3ac4f-168">Validation File</span></span>  <br/> |<span data-ttu-id="3ac4f-169">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3ac4f-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3ac4f-170">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3ac4f-170">Can be Empty</span></span>  <br/> |<span data-ttu-id="3ac4f-171">False</span><span class="sxs-lookup"><span data-stu-id="3ac4f-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3ac4f-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ac4f-172">See also</span></span>

- [<span data-ttu-id="3ac4f-173">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3ac4f-173">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="3ac4f-174">Finding Items</span><span class="sxs-lookup"><span data-stu-id="3ac4f-174">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

