---
title: UniqueBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UniqueBody
api_type:
- schema
ms.assetid: 06bc95d7-121c-433b-bd27-c2b0eb8c011f
description: Das UniqueBody-Element stellt ein HTML-Fragment oder nur-Text, der den eindeutigen Text an dieser Unterhaltung darstellt.
ms.openlocfilehash: 49d3607926e0b985074d79cde76cad084f537f01
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839301"
---
# <a name="uniquebody"></a><span data-ttu-id="5b314-103">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="5b314-103">UniqueBody</span></span>

<span data-ttu-id="5b314-104">Das **UniqueBody** -Element stellt ein HTML-Fragment oder nur-Text, der den eindeutigen Text an dieser Unterhaltung darstellt.</span><span class="sxs-lookup"><span data-stu-id="5b314-104">The **UniqueBody** element represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span> 
  
```XML
<UniqueBody BodyType=""/>
```

 <span data-ttu-id="5b314-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="5b314-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5b314-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5b314-106">Attributes and elements</span></span>

<span data-ttu-id="5b314-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5b314-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5b314-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5b314-108">Attributes</span></span>

|<span data-ttu-id="5b314-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="5b314-109">**Attribute**</span></span>|<span data-ttu-id="5b314-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5b314-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5b314-111">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="5b314-111">**BodyType**</span></span> <br/> |<span data-ttu-id="5b314-112">Beschreibt, wie den Textkörper des Elements im Element gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="5b314-112">Describes how the item body is stored in the item.</span></span>  <br/> |
   
#### <a name="bodytype-attribute"></a><span data-ttu-id="5b314-113">BodyType-Attribut</span><span class="sxs-lookup"><span data-stu-id="5b314-113">BodyType Attribute</span></span>

|<span data-ttu-id="5b314-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5b314-114">**Value**</span></span>|<span data-ttu-id="5b314-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5b314-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5b314-116">**HTML**</span><span class="sxs-lookup"><span data-stu-id="5b314-116">**HTML**</span></span> <br/> |<span data-ttu-id="5b314-117">Konvertiert alle Texte in HTML.</span><span class="sxs-lookup"><span data-stu-id="5b314-117">Converts all bodies to HTML.</span></span>  <br/> |
|<span data-ttu-id="5b314-118">**Text**</span><span class="sxs-lookup"><span data-stu-id="5b314-118">**Text**</span></span> <br/> |<span data-ttu-id="5b314-119">Alle Texte konvertiert in nur-Text.</span><span class="sxs-lookup"><span data-stu-id="5b314-119">Converts all bodies to plain text.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5b314-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5b314-120">Child elements</span></span>

<span data-ttu-id="5b314-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="5b314-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5b314-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5b314-122">Parent elements</span></span>

|<span data-ttu-id="5b314-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="5b314-123">**Element**</span></span>|<span data-ttu-id="5b314-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5b314-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5b314-125">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="5b314-125">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="5b314-126">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="5b314-126">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="5b314-127">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="5b314-127">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="5b314-128">Stellt ein Exchange-Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="5b314-128">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="5b314-129">DistributionList</span><span class="sxs-lookup"><span data-stu-id="5b314-129">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="5b314-130">Stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="5b314-130">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="5b314-131">Element</span><span class="sxs-lookup"><span data-stu-id="5b314-131">Item</span></span>](item.md) <br/> |<span data-ttu-id="5b314-132">Stellt ein Element im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="5b314-132">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5b314-133">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="5b314-133">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="5b314-134">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="5b314-134">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5b314-135">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="5b314-135">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="5b314-136">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="5b314-136">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5b314-137">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="5b314-137">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="5b314-138">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="5b314-138">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5b314-139">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="5b314-139">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="5b314-140">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="5b314-140">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5b314-141">Message</span><span class="sxs-lookup"><span data-stu-id="5b314-141">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="5b314-142">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="5b314-142">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="5b314-143">PostItem-Objekt</span><span class="sxs-lookup"><span data-stu-id="5b314-143">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="5b314-144">Stellt ein Post-Element im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="5b314-144">Represents a post item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5b314-145">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="5b314-145">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="5b314-146">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="5b314-146">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5b314-147">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="5b314-147">Task</span></span>](task.md) <br/> |<span data-ttu-id="5b314-148">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="5b314-148">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5b314-149">Textwert</span><span class="sxs-lookup"><span data-stu-id="5b314-149">Text value</span></span>

<span data-ttu-id="5b314-150">Keine.</span><span class="sxs-lookup"><span data-stu-id="5b314-150">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5b314-151">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5b314-151">Remarks</span></span>

<span data-ttu-id="5b314-152">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="5b314-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5b314-153">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5b314-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b314-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="5b314-154">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5b314-155">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5b314-155">Schema Name</span></span>  <br/> |<span data-ttu-id="5b314-156">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5b314-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="5b314-157">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5b314-157">Validation File</span></span>  <br/> |<span data-ttu-id="5b314-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5b314-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5b314-159">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5b314-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="5b314-160">False</span><span class="sxs-lookup"><span data-stu-id="5b314-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5b314-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b314-161">See also</span></span>



- [<span data-ttu-id="5b314-162">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5b314-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

