---
title: GroupBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupBy
api_type:
- schema
ms.assetid: 9728619b-4674-4b9d-9f6c-e75c6165966c
description: GroupBy-Element gibt eine beliebige Gruppierung für FindItem Abfragen an.
ms.openlocfilehash: d85c0fddec244c99dfbea1f85da331fc5319536d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829753"
---
# <a name="groupby"></a><span data-ttu-id="8b4bb-103">GroupBy</span><span class="sxs-lookup"><span data-stu-id="8b4bb-103">GroupBy</span></span>

<span data-ttu-id="8b4bb-104">**GroupBy** -Element gibt eine beliebige Gruppierung für FindItem Abfragen an.</span><span class="sxs-lookup"><span data-stu-id="8b4bb-104">The **GroupBy** element specifies an arbitrary grouping for FindItem queries.</span></span> 
  
- [<span data-ttu-id="8b4bb-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="8b4bb-105">FindItem</span></span>](finditem.md)
- [<span data-ttu-id="8b4bb-106">GroupBy</span><span class="sxs-lookup"><span data-stu-id="8b4bb-106">GroupBy</span></span>](groupby.md)
  
```xml
<GroupBy Order="">
   <FieldURI/>
   <AggregateOn/>
</GroupBy>
```

 <span data-ttu-id="8b4bb-107">**GroupByType**</span><span class="sxs-lookup"><span data-stu-id="8b4bb-107">**GroupByType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8b4bb-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8b4bb-108">Attributes and elements</span></span>

<span data-ttu-id="8b4bb-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8b4bb-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8b4bb-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="8b4bb-110">Attributes</span></span>

|<span data-ttu-id="8b4bb-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="8b4bb-111">**Attribute**</span></span>|<span data-ttu-id="8b4bb-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8b4bb-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8b4bb-113">**Order**</span><span class="sxs-lookup"><span data-stu-id="8b4bb-113">**Order**</span></span> <br/> | <span data-ttu-id="8b4bb-114">Bestimmt die Reihenfolge der Gruppen im Array gruppierten Element, das in der Antwort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8b4bb-114">Determines the order of the groups in the grouped item array that is returned in the response.</span></span> <span data-ttu-id="8b4bb-115">Dieses Attribut ist vom Typ SortDirectionType.</span><span class="sxs-lookup"><span data-stu-id="8b4bb-115">This attribute is of type SortDirectionType.</span></span>  <br/> |
   
#### <a name="order-attribute-values"></a><span data-ttu-id="8b4bb-116">Reihenfolge-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="8b4bb-116">Order attribute values</span></span>

|<span data-ttu-id="8b4bb-117">**Wert**</span><span class="sxs-lookup"><span data-stu-id="8b4bb-117">**Value**</span></span>|<span data-ttu-id="8b4bb-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8b4bb-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8b4bb-119">Ascending</span><span class="sxs-lookup"><span data-stu-id="8b4bb-119">Ascending</span></span>  <br/> |<span data-ttu-id="8b4bb-120">Die Gruppen werden in aufsteigender Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="8b4bb-120">The groups are ordered in ascending order.</span></span>  <br/> |
|<span data-ttu-id="8b4bb-121">Absteigend</span><span class="sxs-lookup"><span data-stu-id="8b4bb-121">Descending</span></span>  <br/> |<span data-ttu-id="8b4bb-122">Die Gruppen werden in absteigender Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="8b4bb-122">The groups are ordered in descending order.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8b4bb-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8b4bb-123">Child elements</span></span>

|<span data-ttu-id="8b4bb-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="8b4bb-124">**Element**</span></span>|<span data-ttu-id="8b4bb-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8b4bb-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8b4bb-126">FieldURI</span><span class="sxs-lookup"><span data-stu-id="8b4bb-126">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="8b4bb-127">Identifiziert die Eigenschaften von URI häufig verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8b4bb-127">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="8b4bb-128">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="8b4bb-128">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="8b4bb-129">Einzelne Elemente eines Wörterbuchs identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8b4bb-129">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="8b4bb-130">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="8b4bb-130">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="8b4bb-131">Bezeichnet die extended MAPI-Eigenschaften zum Abrufen oder festlegen, oder erstellen.</span><span class="sxs-lookup"><span data-stu-id="8b4bb-131">Identifies extended MAPI properties to get, set, or create.</span></span>  <br/> |
|[<span data-ttu-id="8b4bb-132">AggregateOn</span><span class="sxs-lookup"><span data-stu-id="8b4bb-132">AggregateOn</span></span>](aggregateon.md) <br/> |<span data-ttu-id="8b4bb-133">Stellt das dar, das verwendet wird, um die Reihenfolge der Gruppen in einer Antwort zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="8b4bb-133">Represents the field that is used to determine the order of groups in a response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8b4bb-134">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8b4bb-134">Parent elements</span></span>

|<span data-ttu-id="8b4bb-135">**Element**</span><span class="sxs-lookup"><span data-stu-id="8b4bb-135">**Element**</span></span>|<span data-ttu-id="8b4bb-136">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8b4bb-136">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8b4bb-137">FindItem</span><span class="sxs-lookup"><span data-stu-id="8b4bb-137">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="8b4bb-138">Definiert eine Anforderung zum Suchen von Elementen in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="8b4bb-138">Defines a request to find items in a mailbox.</span></span>  <br/><br/> <span data-ttu-id="8b4bb-139">Es folgt der XPath-Ausdruck, der dieses Element:`/FindItem`</span><span class="sxs-lookup"><span data-stu-id="8b4bb-139">The following is the XPath expression to this element:  `/FindItem`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b4bb-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8b4bb-140">Remarks</span></span>

<span data-ttu-id="8b4bb-141">Die Antwort FindItem enthält eine Auflistung von Gruppen.</span><span class="sxs-lookup"><span data-stu-id="8b4bb-141">The FindItem response will contain a collection of groups.</span></span> <span data-ttu-id="8b4bb-142">Jede Gruppe enthält alle Elemente, die übereinstimmenden Werte für die **GroupBy** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8b4bb-142">Each group will contain all items that had matching values for the **GroupBy** property.</span></span> <span data-ttu-id="8b4bb-143">Die Eigenschaft, die bestimmt, die Gruppierung wird im [FieldURI](fielduri.md), [IndexedFieldURI](indexedfielduri.md)oder [ExtendedFieldURI](extendedfielduri.md) -Element identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8b4bb-143">The property that determines the grouping is identified in the [FieldURI](fielduri.md), [IndexedFieldURI](indexedfielduri.md), or [ExtendedFieldURI](extendedfielduri.md) element.</span></span> 
  
<span data-ttu-id="8b4bb-144">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="8b4bb-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8b4bb-145">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8b4bb-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8b4bb-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="8b4bb-146">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8b4bb-147">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8b4bb-147">Schema Name</span></span>  <br/> |<span data-ttu-id="8b4bb-148">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="8b4bb-148">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8b4bb-149">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8b4bb-149">Validation File</span></span>  <br/> |<span data-ttu-id="8b4bb-150">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8b4bb-150">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8b4bb-151">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8b4bb-151">Can be Empty</span></span>  <br/> |<span data-ttu-id="8b4bb-152">False</span><span class="sxs-lookup"><span data-stu-id="8b4bb-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8b4bb-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b4bb-153">See also</span></span>

- [<span data-ttu-id="8b4bb-154">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8b4bb-154">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="8b4bb-155">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8b4bb-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="8b4bb-156">Finding Items</span><span class="sxs-lookup"><span data-stu-id="8b4bb-156">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

