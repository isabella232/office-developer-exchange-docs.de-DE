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
description: Das AppendToItemField-Element identifiziert Daten, die während eines UpdateItem-Vorgangs an eine einzelne Eigenschaft eines Elements angefügt werden sollen.
ms.openlocfilehash: 902239155bff45d6f81989de954c9459cf012288
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466045"
---
# <a name="appendtoitemfield"></a><span data-ttu-id="15638-103">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="15638-103">AppendToItemField</span></span>

<span data-ttu-id="15638-104">Das **AppendToItemField** -Element identifiziert Daten, die während eines [UpdateItem-Vorgangs](updateitem-operation.md)an eine einzelne Eigenschaft eines Elements angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="15638-104">The **AppendToItemField** element identifies data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>
  
- [<span data-ttu-id="15638-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="15638-105">UpdateItem</span></span>](updateitem.md)
  
- [<span data-ttu-id="15638-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="15638-106">ItemChanges</span></span>](itemchanges.md)
  
- [<span data-ttu-id="15638-107">ItemChange</span><span class="sxs-lookup"><span data-stu-id="15638-107">ItemChange</span></span>](itemchange.md)
  
- [<span data-ttu-id="15638-108">Updates (Element)</span><span class="sxs-lookup"><span data-stu-id="15638-108">Updates (Item)</span></span>](updates-item.md)
  
- [<span data-ttu-id="15638-109">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="15638-109">AppendToItemField</span></span>](appendtoitemfield.md)
  
```xml
<AppendToItemField>
   <FieldURI/>
   <Item/>
</AppendToItemField>
```

 <span data-ttu-id="15638-110">**AppendToItemFieldType**</span><span class="sxs-lookup"><span data-stu-id="15638-110">**AppendToItemFieldType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="15638-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="15638-111">Attributes and elements</span></span>

<span data-ttu-id="15638-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="15638-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="15638-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="15638-113">Attributes</span></span>

<span data-ttu-id="15638-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="15638-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="15638-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="15638-115">Child elements</span></span>

|<span data-ttu-id="15638-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="15638-116">**Element**</span></span>|<span data-ttu-id="15638-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="15638-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="15638-118">FieldURI</span><span class="sxs-lookup"><span data-stu-id="15638-118">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="15638-119">Identifiziert häufig referenzierte Eigenschaften nach URI.</span><span class="sxs-lookup"><span data-stu-id="15638-119">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="15638-120">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="15638-120">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="15638-121">Identifiziert einzelne Member eines Wörterbuchs.</span><span class="sxs-lookup"><span data-stu-id="15638-121">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="15638-122">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="15638-122">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="15638-123">Identifiziert erweiterte MAPI-Eigenschaften, die angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="15638-123">Identifies extended MAPI properties to append.</span></span>  <br/> |
|[<span data-ttu-id="15638-124">Element</span><span class="sxs-lookup"><span data-stu-id="15638-124">Item</span></span>](item.md) <br/> |<span data-ttu-id="15638-125">Stellt ein Element im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="15638-125">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="15638-126">Message</span><span class="sxs-lookup"><span data-stu-id="15638-126">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="15638-127">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="15638-127">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="15638-128">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="15638-128">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="15638-129">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="15638-129">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="15638-130">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="15638-130">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="15638-131">Stellt ein Exchange-Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="15638-131">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="15638-132">DistributionList</span><span class="sxs-lookup"><span data-stu-id="15638-132">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="15638-133">Stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="15638-133">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="15638-134">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="15638-134">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="15638-135">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="15638-135">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="15638-136">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="15638-136">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="15638-137">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="15638-137">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="15638-138">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="15638-138">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="15638-139">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="15638-139">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="15638-140">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="15638-140">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="15638-141">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="15638-141">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="15638-142">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="15638-142">Task</span></span>](task.md) <br/> |<span data-ttu-id="15638-143">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="15638-143">Represents a task in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="15638-144">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="15638-144">Parent elements</span></span>

|<span data-ttu-id="15638-145">**Element**</span><span class="sxs-lookup"><span data-stu-id="15638-145">**Element**</span></span>|<span data-ttu-id="15638-146">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="15638-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="15638-147">Updates (Element)</span><span class="sxs-lookup"><span data-stu-id="15638-147">Updates (Item)</span></span>](updates-item.md) <br/> |<span data-ttu-id="15638-148">Enthält ein Array, das Append-, festlegen-und DELETE-Änderungen an Elementeigenschaften definiert.</span><span class="sxs-lookup"><span data-stu-id="15638-148">Contains an array that defines append, set, and delete changes to item properties.</span></span>  <br/> <span data-ttu-id="15638-149">Im folgenden finden Sie den XPath-Ausdruck für dieses Element:`/UpdateItem/ItemChanges/ItemChange[i]/Updates`</span><span class="sxs-lookup"><span data-stu-id="15638-149">The following is the XPath expression to this element:  `/UpdateItem/ItemChanges/ItemChange[i]/Updates`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15638-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15638-150">Remarks</span></span>

<span data-ttu-id="15638-151">Nur bestimmte Eigenschaften unterstützen Append-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="15638-151">Only certain properties support append operations.</span></span> <span data-ttu-id="15638-152">Ein Versuch, an eine Eigenschaft anzufügen, die das Anfügen nicht unterstützt, führt zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="15638-152">An attempt to append to a property that does not support appending will result in an error.</span></span>
  
<span data-ttu-id="15638-153">Bei Aktualisierungsvorgängen kann nur eine Eigenschaft innerhalb einer einzelnen Anforderung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="15638-153">For update operations, only one property can be modified within a single request.</span></span> <span data-ttu-id="15638-154">Auf diese einzelne Eigenschaft muss im [path](path.md) -Element verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="15638-154">That single property must be referenced in the [Path](path.md) element.</span></span> <span data-ttu-id="15638-155">Das **Item** -Element in den abgeleiteten Klassen kann dann nur eine einzelne Eigenschaft enthalten, die mit dem einzelnen **Pfad** -Element übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="15638-155">The **Item** element in the derived classes can then only hold a single property that is in agreement with the single **Path** element.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="15638-156">Das [path](path.md) -Element ist abstrakt.</span><span class="sxs-lookup"><span data-stu-id="15638-156">The [Path](path.md) element is abstract.</span></span> <span data-ttu-id="15638-157">Es muss durch das [FieldURI](fielduri.md)-, [IndexedFieldURI](indexedfielduri.md)-oder [ExtendedFieldURI](extendedfielduri.md) -Element ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="15638-157">It must be substituted by the [FieldURI](fielduri.md), [IndexedFieldURI](indexedfielduri.md), or [ExtendedFieldURI](extendedfielduri.md) element.</span></span> 
  
<span data-ttu-id="15638-158">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="15638-158">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="15638-159">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="15638-159">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="15638-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="15638-160">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="15638-161">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="15638-161">Schema Name</span></span>  <br/> |<span data-ttu-id="15638-162">Schematypen</span><span class="sxs-lookup"><span data-stu-id="15638-162">Types schema</span></span>  <br/> |
|<span data-ttu-id="15638-163">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="15638-163">Validation File</span></span>  <br/> |<span data-ttu-id="15638-164">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="15638-164">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="15638-165">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="15638-165">Can be Empty</span></span>  <br/> |<span data-ttu-id="15638-166">False</span><span class="sxs-lookup"><span data-stu-id="15638-166">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="15638-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15638-167">See also</span></span>

- [<span data-ttu-id="15638-168">UpdateItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="15638-168">UpdateItem operation</span></span>](updateitem-operation.md)
- [<span data-ttu-id="15638-169">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="15638-169">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

