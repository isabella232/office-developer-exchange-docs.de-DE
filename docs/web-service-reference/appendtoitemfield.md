---
title: AppendToItemField
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AppendToItemField
api_type:
- schema
ms.assetid: 66dbcb4a-ae6d-4648-8610-67187bdb105c
description: Das AppendToItemField-Element identifiziert Daten an eine einzelne Eigenschaft eines Elements während eines Vorgangs UpdateItem angefügt.
ms.openlocfilehash: b432399e84ee4a3fd7edc5d3f803079435c79143
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757280"
---
# <a name="appendtoitemfield"></a><span data-ttu-id="79b19-103">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="79b19-103">AppendToItemField</span></span>

<span data-ttu-id="79b19-104">Das **AppendToItemField** -Element identifiziert Daten an eine einzelne Eigenschaft eines Elements während eines [Vorgangs UpdateItem](updateitem-operation.md)angefügt.</span><span class="sxs-lookup"><span data-stu-id="79b19-104">The **AppendToItemField** element identifies data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>
  
- [<span data-ttu-id="79b19-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="79b19-105">UpdateItem</span></span>](updateitem.md)
  
- [<span data-ttu-id="79b19-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="79b19-106">ItemChanges</span></span>](itemchanges.md)
  
- [<span data-ttu-id="79b19-107">ItemChange</span><span class="sxs-lookup"><span data-stu-id="79b19-107">ItemChange</span></span>](itemchange.md)
  
- [<span data-ttu-id="79b19-108">Updates (Element)</span><span class="sxs-lookup"><span data-stu-id="79b19-108">Updates (Item)</span></span>](updates-item.md)
  
- [<span data-ttu-id="79b19-109">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="79b19-109">AppendToItemField</span></span>](appendtoitemfield.md)
  
```xml
<AppendToItemField>
   <FieldURI/>
   <Item/>
</AppendToItemField>
```

 <span data-ttu-id="79b19-110">**AppendToItemFieldType**</span><span class="sxs-lookup"><span data-stu-id="79b19-110">**AppendToItemFieldType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="79b19-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="79b19-111">Attributes and elements</span></span>

<span data-ttu-id="79b19-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="79b19-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="79b19-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="79b19-113">Attributes</span></span>

<span data-ttu-id="79b19-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="79b19-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="79b19-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="79b19-115">Child elements</span></span>

|<span data-ttu-id="79b19-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="79b19-116">**Element**</span></span>|<span data-ttu-id="79b19-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="79b19-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="79b19-118">FieldURI</span><span class="sxs-lookup"><span data-stu-id="79b19-118">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="79b19-119">Identifiziert die Eigenschaften von URI häufig verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="79b19-119">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="79b19-120">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="79b19-120">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="79b19-121">Einzelne Elemente eines Wörterbuchs identifiziert.</span><span class="sxs-lookup"><span data-stu-id="79b19-121">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="79b19-122">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="79b19-122">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="79b19-123">Bezeichnet die extended MAPI-Eigenschaften, angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="79b19-123">Identifies extended MAPI properties to append.</span></span>  <br/> |
|[<span data-ttu-id="79b19-124">Element</span><span class="sxs-lookup"><span data-stu-id="79b19-124">Item</span></span>](item.md) <br/> |<span data-ttu-id="79b19-125">Stellt ein Element im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="79b19-125">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="79b19-126">Message</span><span class="sxs-lookup"><span data-stu-id="79b19-126">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="79b19-127">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="79b19-127">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="79b19-128">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="79b19-128">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="79b19-129">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="79b19-129">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="79b19-130">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="79b19-130">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="79b19-131">Stellt ein Exchange-Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="79b19-131">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="79b19-132">DistributionList</span><span class="sxs-lookup"><span data-stu-id="79b19-132">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="79b19-133">Stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="79b19-133">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="79b19-134">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="79b19-134">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="79b19-135">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="79b19-135">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="79b19-136">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="79b19-136">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="79b19-137">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="79b19-137">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="79b19-138">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="79b19-138">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="79b19-139">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="79b19-139">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="79b19-140">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="79b19-140">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="79b19-141">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="79b19-141">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="79b19-142">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="79b19-142">Task</span></span>](task.md) <br/> |<span data-ttu-id="79b19-143">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="79b19-143">Represents a task in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="79b19-144">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="79b19-144">Parent elements</span></span>

|<span data-ttu-id="79b19-145">**Element**</span><span class="sxs-lookup"><span data-stu-id="79b19-145">**Element**</span></span>|<span data-ttu-id="79b19-146">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="79b19-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="79b19-147">Updates (Element)</span><span class="sxs-lookup"><span data-stu-id="79b19-147">Updates (Item)</span></span>](updates-item.md) <br/> |<span data-ttu-id="79b19-148">Enthält ein Array, definiert anfügen, festlegen und Löschen von Änderungen an Elementeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="79b19-148">Contains an array that defines append, set, and delete changes to item properties.</span></span>  <br/> <span data-ttu-id="79b19-149">Es folgt der XPath-Ausdruck, der dieses Element:`/UpdateItem/ItemChanges/ItemChange[i]/Updates`</span><span class="sxs-lookup"><span data-stu-id="79b19-149">The following is the XPath expression to this element:  `/UpdateItem/ItemChanges/ItemChange[i]/Updates`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79b19-150">Hinweise</span><span class="sxs-lookup"><span data-stu-id="79b19-150">Remarks</span></span>

<span data-ttu-id="79b19-151">Fügen Sie nur bestimmte Eigenschaften Support Vorgänge an.</span><span class="sxs-lookup"><span data-stu-id="79b19-151">Only certain properties support append operations.</span></span> <span data-ttu-id="79b19-152">Ein Versuch, eine Eigenschaft angefügt werden soll, die anhängen nicht unterstützt, tritt ein Fehler bewirken.</span><span class="sxs-lookup"><span data-stu-id="79b19-152">An attempt to append to a property that does not support appending will result in an error.</span></span>
  
<span data-ttu-id="79b19-153">Für Aktualisierungsvorgänge kann nur eine Eigenschaft innerhalb einer einzelnen Anforderung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="79b19-153">For update operations, only one property can be modified within a single request.</span></span> <span data-ttu-id="79b19-154">Einzelne Eigenschaft im [Pfad](path.md) -Element verwiesen werden muss.</span><span class="sxs-lookup"><span data-stu-id="79b19-154">That single property must be referenced in the [Path](path.md) element.</span></span> <span data-ttu-id="79b19-155">**Das Element in den abgeleiteten Klassen** kann dann nur eine einzelne Eigenschaft enthalten, mit dem einzelne **Path** -Element.</span><span class="sxs-lookup"><span data-stu-id="79b19-155">The **Item** element in the derived classes can then only hold a single property that is in agreement with the single **Path** element.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="79b19-156">Das [Path](path.md) -Element ist abstrakt.</span><span class="sxs-lookup"><span data-stu-id="79b19-156">The [Path](path.md) element is abstract.</span></span> <span data-ttu-id="79b19-157">Es muss vom [FieldURI](fielduri.md), [IndexedFieldURI](indexedfielduri.md)oder [ExtendedFieldURI](extendedfielduri.md) -Element durch ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="79b19-157">It must be substituted by the [FieldURI](fielduri.md), [IndexedFieldURI](indexedfielduri.md), or [ExtendedFieldURI](extendedfielduri.md) element.</span></span> 
  
<span data-ttu-id="79b19-158">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="79b19-158">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="79b19-159">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="79b19-159">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="79b19-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="79b19-160">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="79b19-161">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="79b19-161">Schema Name</span></span>  <br/> |<span data-ttu-id="79b19-162">Schematypen</span><span class="sxs-lookup"><span data-stu-id="79b19-162">Types schema</span></span>  <br/> |
|<span data-ttu-id="79b19-163">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="79b19-163">Validation File</span></span>  <br/> |<span data-ttu-id="79b19-164">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="79b19-164">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="79b19-165">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="79b19-165">Can be Empty</span></span>  <br/> |<span data-ttu-id="79b19-166">False</span><span class="sxs-lookup"><span data-stu-id="79b19-166">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="79b19-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79b19-167">See also</span></span>

- [<span data-ttu-id="79b19-168">UpdateItem Operation</span><span class="sxs-lookup"><span data-stu-id="79b19-168">UpdateItem operation</span></span>](updateitem-operation.md)
- [<span data-ttu-id="79b19-169">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="79b19-169">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

