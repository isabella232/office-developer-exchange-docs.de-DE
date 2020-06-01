---
title: IndexedPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IndexedPageItemView
api_type:
- schema
ms.assetid: 6d1b0b04-cc35-4a57-bd7a-824136d14fda
description: Das IndexedPageItemView-Element beschreibt, wie die Seiten Unterhaltung oder Elementinformationen für eine FindItem-Operation oder eine FindConversation-Vorgangsanforderung zurückgegeben werden.
ms.openlocfilehash: 0a66f17855fd425082e3651886d3eeec4f217ac4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456913"
---
# <a name="indexedpageitemview"></a><span data-ttu-id="d9004-103">IndexedPageItemView</span><span class="sxs-lookup"><span data-stu-id="d9004-103">IndexedPageItemView</span></span>

<span data-ttu-id="d9004-104">Das **IndexedPageItemView** -Element beschreibt, wie die Seiten Unterhaltung oder Elementinformationen für eine [FindItem-Operation](finditem-operation.md) oder eine [FindConversation-Vorgangs](findconversation-operation.md) Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d9004-104">The **IndexedPageItemView** element describes how paged conversation or item information is returned for a [FindItem operation](finditem-operation.md) or [FindConversation operation](findconversation-operation.md) request.</span></span> 
  
```XML
<IndexedPageViewItemView MaxEntriesReturned="" Offset="" BasePoint=""/>
```

 <span data-ttu-id="d9004-105">**IndexedPageViewType**</span><span class="sxs-lookup"><span data-stu-id="d9004-105">**IndexedPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d9004-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d9004-106">Attributes and elements</span></span>

<span data-ttu-id="d9004-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d9004-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d9004-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d9004-108">Attributes</span></span>

|<span data-ttu-id="d9004-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d9004-109">**Attribute**</span></span>|<span data-ttu-id="d9004-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d9004-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d9004-111">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="d9004-111">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="d9004-112">Beschreibt die maximale Anzahl von Elementen oder Unterhaltungen, die in der Antwort zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d9004-112">Describes the maximum number of items or conversations to return in the response.</span></span> <span data-ttu-id="d9004-113">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="d9004-113">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="d9004-114">**Offset**</span><span class="sxs-lookup"><span data-stu-id="d9004-114">**Offset**</span></span> <br/> |<span data-ttu-id="d9004-115">Beschreibt den Offset aus dem **Basepoint**.</span><span class="sxs-lookup"><span data-stu-id="d9004-115">Describes the offset from the **BasePoint**.</span></span> <span data-ttu-id="d9004-116">Wenn **Basepoint** gleich dem Anfang ist, ist der Offset positiv.</span><span class="sxs-lookup"><span data-stu-id="d9004-116">If **BasePoint** is equal to Beginning, the offset is positive.</span></span> <span data-ttu-id="d9004-117">Wenn **Basepoint** gleich End ist, wird der Offset so behandelt, als wäre er negativ.</span><span class="sxs-lookup"><span data-stu-id="d9004-117">If **BasePoint** is equal to End, the offset is handled as if it were negative.</span></span> <span data-ttu-id="d9004-118">Dadurch wird angegeben, welches Element oder welche Unterhaltung als erstes in der Antwort zugestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d9004-118">This identifies which item or conversation will be the first to be delivered in the response.</span></span> <span data-ttu-id="d9004-119">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d9004-119">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="d9004-120">**Basepoint**</span><span class="sxs-lookup"><span data-stu-id="d9004-120">**BasePoint**</span></span> <br/> |<span data-ttu-id="d9004-121">Beschreibt, ob die Seite von Elementen oder Unterhaltungen am Anfang oder am Ende der Gruppe von Elementen oder Unterhaltungen beginnt, die mit den Suchkriterien gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="d9004-121">Describes whether the page of items or conversations will start from the beginning or the end of the set of items or conversations that are found by using the search criteria.</span></span> <span data-ttu-id="d9004-122">Suche von Ende aus sucht immer rückwärts.</span><span class="sxs-lookup"><span data-stu-id="d9004-122">Seeking from the end always searches backward.</span></span> <span data-ttu-id="d9004-123">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d9004-123">This attribute is required.</span></span>  <br/> |
   
#### <a name="basepoint-attribute"></a><span data-ttu-id="d9004-124">Basepoint-Attribut</span><span class="sxs-lookup"><span data-stu-id="d9004-124">BasePoint Attribute</span></span>

|<span data-ttu-id="d9004-125">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d9004-125">**Value**</span></span>|<span data-ttu-id="d9004-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d9004-126">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d9004-127">Anfang</span><span class="sxs-lookup"><span data-stu-id="d9004-127">Beginning</span></span>  <br/> |<span data-ttu-id="d9004-128">Die ausgelagerte Ansicht beginnt am Anfang der gefundenen Unterhaltung oder des Elementsatzes.</span><span class="sxs-lookup"><span data-stu-id="d9004-128">The paged view starts at the beginning of the found conversation or item set.</span></span>  <br/> |
|<span data-ttu-id="d9004-129">Ende</span><span class="sxs-lookup"><span data-stu-id="d9004-129">End</span></span>  <br/> |<span data-ttu-id="d9004-130">Die ausgelagerte Ansicht beginnt am Ende der gefundenen Unterhaltung oder des Elementsatzes.</span><span class="sxs-lookup"><span data-stu-id="d9004-130">The paged view starts at the end of the found conversation or item set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d9004-131">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d9004-131">Child elements</span></span>

<span data-ttu-id="d9004-132">Keine.</span><span class="sxs-lookup"><span data-stu-id="d9004-132">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d9004-133">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d9004-133">Parent elements</span></span>

|<span data-ttu-id="d9004-134">**Element**</span><span class="sxs-lookup"><span data-stu-id="d9004-134">**Element**</span></span>|<span data-ttu-id="d9004-135">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d9004-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d9004-136">FindItem</span><span class="sxs-lookup"><span data-stu-id="d9004-136">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="d9004-137">Definiert eine Anforderung zum Suchen von Elementen in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="d9004-137">Defines a request to find items in a mailbox.</span></span>  <br/> <span data-ttu-id="d9004-138">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="d9004-138">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
|[<span data-ttu-id="d9004-139">FindConversation</span><span class="sxs-lookup"><span data-stu-id="d9004-139">FindConversation</span></span>](findconversation.md) <br/> |<span data-ttu-id="d9004-140">Definiert eine Anforderung zum Suchen von Unterhaltungen in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="d9004-140">Defines a request to find conversations in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9004-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9004-141">Remarks</span></span>

<span data-ttu-id="d9004-142">Bei der Suche ab dem Ende wird der durch den Offset angegebene Ursprung verschoben.</span><span class="sxs-lookup"><span data-stu-id="d9004-142">Seeking from the end involves moving to the origin identified by the offset.</span></span> <span data-ttu-id="d9004-143">Darüber hinaus wird der Zeiger nach der Anzahl der angeforderten Datensätze zurück verschoben.</span><span class="sxs-lookup"><span data-stu-id="d9004-143">Additionally, the pointer is moved back by the number of requested records.</span></span> <span data-ttu-id="d9004-144">Wenn beispielsweise 100 Datensätze vorhanden sind und der Offset 25 vom Ende ist, beginnt die Suche von 75.</span><span class="sxs-lookup"><span data-stu-id="d9004-144">For example, if there are 100 records and the offset is 25 from the end, the search starts from 75.</span></span> <span data-ttu-id="d9004-145">Wenn 10 Datensätze zurückgegeben werden, wird der Zeiger rückwärts um weitere 10 Datensätze nach 65 verschoben und gibt Datensätze 65 bis 75 zurück.</span><span class="sxs-lookup"><span data-stu-id="d9004-145">If 10 records are returned, the pointer is moved backward an additional 10 records to 65 and returns records 65 through 75.</span></span> <span data-ttu-id="d9004-146">Der nächste Index lautet 64.</span><span class="sxs-lookup"><span data-stu-id="d9004-146">The next index is 64.</span></span> <span data-ttu-id="d9004-147">Der nächste Offset vom Ende für eine Seite ist 100 minus 64, was 36 entspricht.</span><span class="sxs-lookup"><span data-stu-id="d9004-147">The next offset from the end for a page is 100 minus 64 which equals 36.</span></span> <span data-ttu-id="d9004-148">36 ist der Wert für den nächsten Offset vom Ende, um die nächste indizierte Seite abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d9004-148">36 is the value for the next offset from the end to get the next indexed page.</span></span>
  
<span data-ttu-id="d9004-149">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d9004-149">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="d9004-150">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d9004-150">Example</span></span>

<span data-ttu-id="d9004-151">Das folgende Beispiel zeigt eine [FindItem-Vorgangs](finditem-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d9004-151">The following example shows a [FindItem operation](finditem-operation.md) request.</span></span> <span data-ttu-id="d9004-152">Jedes Element wird mit seiner ID und seinem Betreff zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d9004-152">Each item is returned with its ID and subject.</span></span> <span data-ttu-id="d9004-153">Es werden maximal sechs Elemente in der Antwort zurückgegeben, wie im **MaxEntriesReturned** -Attribut angegeben.</span><span class="sxs-lookup"><span data-stu-id="d9004-153">A maximum of six items are returned in the response, as specified by the **MaxEntriesReturned** attribute.</span></span> <span data-ttu-id="d9004-154">Die Elemente werden in aufsteigender Reihenfolge nach Wichtigkeit gruppiert aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d9004-154">The items are listed in ascending order grouped by importance.</span></span> <span data-ttu-id="d9004-155">Elemente in einer Gruppe werden nach Betreff aggregiert.</span><span class="sxs-lookup"><span data-stu-id="d9004-155">Items in a group are aggregated by subject.</span></span> 
  
```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AdditionalProperties>
      </ItemShape>
      <IndexedPageItemView MaxEntriesReturned="6" BasePoint="Beginning" Offset="0" />
      <GroupBy Order="Ascending">
        <t:FieldURI FieldURI="item:Importance"/>
        <t:AggregateOn Aggregate="Maximum">
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AggregateOn>
      </GroupBy>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="d9004-156">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d9004-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9004-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="d9004-157">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d9004-158">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d9004-158">Schema Name</span></span>  <br/> |<span data-ttu-id="d9004-159">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d9004-159">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d9004-160">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d9004-160">Validation File</span></span>  <br/> |<span data-ttu-id="d9004-161">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d9004-161">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d9004-162">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d9004-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="d9004-163">False</span><span class="sxs-lookup"><span data-stu-id="d9004-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d9004-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9004-164">See also</span></span>



[<span data-ttu-id="d9004-165">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d9004-165">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="d9004-166">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="d9004-166">FindConversation operation</span></span>](findconversation-operation.md)


[<span data-ttu-id="d9004-167">Finding Items</span><span class="sxs-lookup"><span data-stu-id="d9004-167">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

