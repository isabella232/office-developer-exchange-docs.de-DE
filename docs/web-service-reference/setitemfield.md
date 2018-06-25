---
title: SetItemField
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetItemField
api_type:
- schema
ms.assetid: 85284fcb-bd1e-4fda-9dab-cb4cd637cd5b
description: Das SetItemField-Element stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einem UpdateItem Vorgang dar.
ms.openlocfilehash: 012e6ae21af653b4bf12588e5a97334a62884059
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831439"
---
# <a name="setitemfield"></a><span data-ttu-id="12334-103">SetItemField</span><span class="sxs-lookup"><span data-stu-id="12334-103">SetItemField</span></span>

<span data-ttu-id="12334-104">Das Element **SetItemField** stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einem [UpdateItem Vorgang](updateitem-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="12334-104">The **SetItemField** element represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>
  
```xml
<SetItemField>
   <FieldURI/>
   <Item/>
</SetItemField>
```

 <span data-ttu-id="12334-105">**SetItemFieldType**</span><span class="sxs-lookup"><span data-stu-id="12334-105">**SetItemFieldType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="12334-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="12334-106">Attributes and elements</span></span>

<span data-ttu-id="12334-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="12334-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="12334-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="12334-108">Attributes</span></span>

<span data-ttu-id="12334-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="12334-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="12334-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="12334-110">Child elements</span></span>

|<span data-ttu-id="12334-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="12334-111">**Element**</span></span>|<span data-ttu-id="12334-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="12334-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="12334-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="12334-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="12334-114">Identifiziert die Eigenschaften von URI häufig verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="12334-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="12334-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="12334-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="12334-116">Einzelne Elemente eines Wörterbuchs identifiziert.</span><span class="sxs-lookup"><span data-stu-id="12334-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="12334-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="12334-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="12334-118">Bezeichnet die extended MAPI-Eigenschaften festlegen.</span><span class="sxs-lookup"><span data-stu-id="12334-118">Identifies extended MAPI properties to set.</span></span>  <br/> |
|[<span data-ttu-id="12334-119">Element</span><span class="sxs-lookup"><span data-stu-id="12334-119">Item</span></span>](item.md) <br/> |<span data-ttu-id="12334-120">Stellt ein Element im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="12334-120">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="12334-121">Message</span><span class="sxs-lookup"><span data-stu-id="12334-121">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="12334-122">Stellt eine E-mail-Nachricht Exchange zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="12334-122">Represents an Exchange e-mail message to update.</span></span>  <br/> |
|[<span data-ttu-id="12334-123">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="12334-123">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="12334-124">Stellt ein Element des Exchange-Kalender zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="12334-124">Represents an Exchange calendar item to update.</span></span>  <br/> |
|[<span data-ttu-id="12334-125">Contact</span><span class="sxs-lookup"><span data-stu-id="12334-125">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="12334-126">Stellt ein Exchange-Kontaktelement zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="12334-126">Represents an Exchange contact item to update.</span></span>  <br/> |
|[<span data-ttu-id="12334-127">DistributionList</span><span class="sxs-lookup"><span data-stu-id="12334-127">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="12334-128">Stellt eine Verteilerliste aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="12334-128">Represents a distribution list to update.</span></span>  <br/> |
|[<span data-ttu-id="12334-129">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="12334-129">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="12334-130">Stellt eine Besprechungsnachricht zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="12334-130">Represents a meeting message to update.</span></span>  <br/> |
|[<span data-ttu-id="12334-131">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="12334-131">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="12334-132">So aktualisieren Sie eine Besprechungsanfrage darstellt.</span><span class="sxs-lookup"><span data-stu-id="12334-132">Represents a meeting request to update.</span></span>  <br/> |
|[<span data-ttu-id="12334-133">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="12334-133">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="12334-134">Stellt eine Antwort auf Besprechungsanfrage aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="12334-134">Represents a meeting response to update.</span></span>  <br/> |
|[<span data-ttu-id="12334-135">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="12334-135">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="12334-136">Aktualisieren einen Besprechungsabsage darstellt.</span><span class="sxs-lookup"><span data-stu-id="12334-136">Represents a meeting cancellation to update.</span></span>  <br/> |
|[<span data-ttu-id="12334-137">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="12334-137">Task</span></span>](task.md) <br/> |<span data-ttu-id="12334-138">Stellt eine Aufgabe zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="12334-138">Represents a task to update.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="12334-139">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="12334-139">Parent elements</span></span>

|<span data-ttu-id="12334-140">**Element**</span><span class="sxs-lookup"><span data-stu-id="12334-140">**Element**</span></span>|<span data-ttu-id="12334-141">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="12334-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="12334-142">Updates (Element)</span><span class="sxs-lookup"><span data-stu-id="12334-142">Updates (Item)</span></span>](updates-item.md) <br/> |<span data-ttu-id="12334-143">Enthält eine Reihe von Elementen, definieren anfügen, festlegen und Löschen von Änderungen an Elementeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="12334-143">Contains a set of elements that define append, set, and delete changes to item properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12334-144">Hinweise</span><span class="sxs-lookup"><span data-stu-id="12334-144">Remarks</span></span>

<span data-ttu-id="12334-145">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="12334-145">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="12334-146">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="12334-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="12334-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="12334-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="12334-148">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="12334-148">Schema Name</span></span>  <br/> |<span data-ttu-id="12334-149">Schematypen</span><span class="sxs-lookup"><span data-stu-id="12334-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="12334-150">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="12334-150">Validation File</span></span>  <br/> |<span data-ttu-id="12334-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="12334-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="12334-152">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="12334-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="12334-153">False</span><span class="sxs-lookup"><span data-stu-id="12334-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="12334-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12334-154">See also</span></span>



[<span data-ttu-id="12334-155">UpdateItem Operation</span><span class="sxs-lookup"><span data-stu-id="12334-155">UpdateItem operation</span></span>](updateitem-operation.md)

