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
description: Das IndexedPageItemView-Element wird beschrieben, wie ausgelagerten Unterhaltung oder Element Informationen für einen FindItem oder FindConversation Vorgang Anforderung zurückgegeben.
ms.openlocfilehash: f1743e22087158c1889977f03774fccbc5577390
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829919"
---
# <a name="indexedpageitemview"></a><span data-ttu-id="dd5c7-103">IndexedPageItemView</span><span class="sxs-lookup"><span data-stu-id="dd5c7-103">IndexedPageItemView</span></span>

<span data-ttu-id="dd5c7-104">Das **IndexedPageItemView** -Element wird beschrieben, wie ausgelagerten Unterhaltung oder Element Informationen für eine Anforderung [FindItem](finditem-operation.md) oder [FindConversation-Operation](findconversation-operation.md) zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-104">The **IndexedPageItemView** element describes how paged conversation or item information is returned for a [FindItem operation](finditem-operation.md) or [FindConversation operation](findconversation-operation.md) request.</span></span> 
  
```XML
<IndexedPageViewItemView MaxEntriesReturned="" Offset="" BasePoint=""/>
```

 <span data-ttu-id="dd5c7-105">**IndexedPageViewType**</span><span class="sxs-lookup"><span data-stu-id="dd5c7-105">**IndexedPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dd5c7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="dd5c7-106">Attributes and elements</span></span>

<span data-ttu-id="dd5c7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dd5c7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="dd5c7-108">Attributes</span></span>

|<span data-ttu-id="dd5c7-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="dd5c7-109">**Attribute**</span></span>|<span data-ttu-id="dd5c7-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dd5c7-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dd5c7-111">**"MaxEntriesReturned"**</span><span class="sxs-lookup"><span data-stu-id="dd5c7-111">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="dd5c7-112">Beschreibt die maximale Anzahl von Elementen oder Unterhaltungen in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-112">Describes the maximum number of items or conversations to return in the response.</span></span> <span data-ttu-id="dd5c7-113">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-113">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="dd5c7-114">**Offset**</span><span class="sxs-lookup"><span data-stu-id="dd5c7-114">**Offset**</span></span> <br/> |<span data-ttu-id="dd5c7-115">Beschreibt die **Basispunkt**-Offset.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-115">Describes the offset from the **BasePoint**.</span></span> <span data-ttu-id="dd5c7-116">Wenn **Basispunkt** Anfang gleich ist, ist der Offset positiv.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-116">If **BasePoint** is equal to Beginning, the offset is positive.</span></span> <span data-ttu-id="dd5c7-117">Wenn **Basispunkt** End entspricht, wird der Offset behandelt, als wäre es negative.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-117">If **BasePoint** is equal to End, the offset is handled as if it were negative.</span></span> <span data-ttu-id="dd5c7-118">Dies bezeichnet, welches Element oder Unterhaltung werden zuerst in der Antwort übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-118">This identifies which item or conversation will be the first to be delivered in the response.</span></span> <span data-ttu-id="dd5c7-119">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-119">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="dd5c7-120">**Basispunkt**</span><span class="sxs-lookup"><span data-stu-id="dd5c7-120">**BasePoint**</span></span> <br/> |<span data-ttu-id="dd5c7-121">Beschreibt, ob die Seite Elemente oder Unterhaltungen gestartet wird, aus der Anfang oder das Ende des Satzes von Elementen oder Unterhaltungen, die mithilfe der Suchkriterien gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-121">Describes whether the page of items or conversations will start from the beginning or the end of the set of items or conversations that are found by using the search criteria.</span></span> <span data-ttu-id="dd5c7-122">Vom Ende immer bemüht sucht rückwärts.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-122">Seeking from the end always searches backward.</span></span> <span data-ttu-id="dd5c7-123">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-123">This attribute is required.</span></span>  <br/> |
   
#### <a name="basepoint-attribute"></a><span data-ttu-id="dd5c7-124">Basispunkt-Attribut</span><span class="sxs-lookup"><span data-stu-id="dd5c7-124">BasePoint Attribute</span></span>

|<span data-ttu-id="dd5c7-125">**Wert**</span><span class="sxs-lookup"><span data-stu-id="dd5c7-125">**Value**</span></span>|<span data-ttu-id="dd5c7-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dd5c7-126">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dd5c7-127">Anfang</span><span class="sxs-lookup"><span data-stu-id="dd5c7-127">Beginning</span></span>  <br/> |<span data-ttu-id="dd5c7-128">Die Seitenansicht beginnt am Anfang des gefundenen Unterhaltung oder Element.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-128">The paged view starts at the beginning of the found conversation or item set.</span></span>  <br/> |
|<span data-ttu-id="dd5c7-129">Ende</span><span class="sxs-lookup"><span data-stu-id="dd5c7-129">End</span></span>  <br/> |<span data-ttu-id="dd5c7-130">Die Seitenansicht beginnt am Ende der Unterhaltung oder Element gefundenen Menge.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-130">The paged view starts at the end of the found conversation or item set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="dd5c7-131">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dd5c7-131">Child elements</span></span>

<span data-ttu-id="dd5c7-132">Keine.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-132">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dd5c7-133">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dd5c7-133">Parent elements</span></span>

|<span data-ttu-id="dd5c7-134">**Element**</span><span class="sxs-lookup"><span data-stu-id="dd5c7-134">**Element**</span></span>|<span data-ttu-id="dd5c7-135">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dd5c7-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dd5c7-136">FindItem</span><span class="sxs-lookup"><span data-stu-id="dd5c7-136">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="dd5c7-137">Definiert eine Anforderung zum Suchen von Elementen in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-137">Defines a request to find items in a mailbox.</span></span>  <br/> <span data-ttu-id="dd5c7-138">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="dd5c7-138">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
|[<span data-ttu-id="dd5c7-139">FindConversation</span><span class="sxs-lookup"><span data-stu-id="dd5c7-139">FindConversation</span></span>](findconversation.md) <br/> |<span data-ttu-id="dd5c7-140">Definiert eine Anforderung an Unterhaltungen in einem Postfach suchen.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-140">Defines a request to find conversations in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd5c7-141">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dd5c7-141">Remarks</span></span>

<span data-ttu-id="dd5c7-142">Suchvorgänge vom Ende umfasst das Verschieben in den Offset identifizierten Ursprung.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-142">Seeking from the end involves moving to the origin identified by the offset.</span></span> <span data-ttu-id="dd5c7-143">Darüber hinaus wird der Mauszeiger durch die Anzahl der angeforderten Datensätze zurück verschoben.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-143">Additionally, the pointer is moved back by the number of requested records.</span></span> <span data-ttu-id="dd5c7-144">Beispielsweise wenn 100 Datensätze vorhanden sind und der Offset 25 vom Ende ist, beginnt für die Suche von 75.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-144">For example, if there are 100 records and the offset is 25 from the end, the search starts from 75.</span></span> <span data-ttu-id="dd5c7-145">Wenn 10 Datensätze zurückgegeben werden, wird der Mauszeiger rückwärts verschoben, zusätzlich 10 65 Datensätze und Datensätze 65 bis 75 zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-145">If 10 records are returned, the pointer is moved backward an additional 10 records to 65 and returns records 65 through 75.</span></span> <span data-ttu-id="dd5c7-146">Der nächste Index ist 64.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-146">The next index is 64.</span></span> <span data-ttu-id="dd5c7-147">Der nächste Offset vom Ende einer Seite wird 100 minus 64 was 36 entspricht.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-147">The next offset from the end for a page is 100 minus 64 which equals 36.</span></span> <span data-ttu-id="dd5c7-148">36 ist der Wert für den nächsten Offset vom Ende zum Abrufen der nächsten Seite indizierten.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-148">36 is the value for the next offset from the end to get the next indexed page.</span></span>
  
<span data-ttu-id="dd5c7-149">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-149">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="dd5c7-150">Beispiel</span><span class="sxs-lookup"><span data-stu-id="dd5c7-150">Example</span></span>

<span data-ttu-id="dd5c7-151">Das folgende Beispiel zeigt eine Anforderung [FindItem Vorgang](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="dd5c7-151">The following example shows a [FindItem operation](finditem-operation.md) request.</span></span> <span data-ttu-id="dd5c7-152">Jedes Element wird mit dem-ID und der Betreff zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-152">Each item is returned with its ID and subject.</span></span> <span data-ttu-id="dd5c7-153">Maximal sechs Elemente werden in der Antwort, gemäß dem Attribut **"MaxEntriesReturned"** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-153">A maximum of six items are returned in the response, as specified by the **MaxEntriesReturned** attribute.</span></span> <span data-ttu-id="dd5c7-154">Die Elemente werden in aufsteigender Reihenfolge gruppiert nach Priorität aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-154">The items are listed in ascending order grouped by importance.</span></span> <span data-ttu-id="dd5c7-155">Nach Betreff werden Elemente in einer Gruppe zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="dd5c7-155">Items in a group are aggregated by subject.</span></span> 
  
```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="element-information"></a><span data-ttu-id="dd5c7-156">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="dd5c7-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dd5c7-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="dd5c7-157">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dd5c7-158">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="dd5c7-158">Schema Name</span></span>  <br/> |<span data-ttu-id="dd5c7-159">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="dd5c7-159">Messages schema</span></span>  <br/> |
|<span data-ttu-id="dd5c7-160">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="dd5c7-160">Validation File</span></span>  <br/> |<span data-ttu-id="dd5c7-161">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="dd5c7-161">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dd5c7-162">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="dd5c7-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="dd5c7-163">False</span><span class="sxs-lookup"><span data-stu-id="dd5c7-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dd5c7-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd5c7-164">See also</span></span>



[<span data-ttu-id="dd5c7-165">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="dd5c7-165">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="dd5c7-166">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="dd5c7-166">FindConversation operation</span></span>](findconversation-operation.md)


[<span data-ttu-id="dd5c7-167">Finding Items</span><span class="sxs-lookup"><span data-stu-id="dd5c7-167">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

