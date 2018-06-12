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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839301"
---
# <a name="uniquebody"></a><span data-ttu-id="9d42e-103">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="9d42e-103">UniqueBody</span></span>

<span data-ttu-id="9d42e-104">Das **UniqueBody** -Element stellt ein HTML-Fragment oder nur-Text, der den eindeutigen Text an dieser Unterhaltung darstellt.</span><span class="sxs-lookup"><span data-stu-id="9d42e-104">The **UniqueBody** element represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span> 
  
```XML
<UniqueBody BodyType=""/>
```

 <span data-ttu-id="9d42e-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="9d42e-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9d42e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9d42e-106">Attributes and elements</span></span>

<span data-ttu-id="9d42e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9d42e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9d42e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9d42e-108">Attributes</span></span>

|<span data-ttu-id="9d42e-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9d42e-109">**Attribute**</span></span>|<span data-ttu-id="9d42e-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d42e-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9d42e-111">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="9d42e-111">**BodyType**</span></span> <br/> |<span data-ttu-id="9d42e-112">Beschreibt, wie den Textkörper des Elements im Element gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="9d42e-112">Describes how the item body is stored in the item.</span></span>  <br/> |
   
#### <a name="bodytype-attribute"></a><span data-ttu-id="9d42e-113">BodyType-Attribut</span><span class="sxs-lookup"><span data-stu-id="9d42e-113">BodyType Attribute</span></span>

|<span data-ttu-id="9d42e-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9d42e-114">**Value**</span></span>|<span data-ttu-id="9d42e-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d42e-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9d42e-116">**HTML**</span><span class="sxs-lookup"><span data-stu-id="9d42e-116">**HTML**</span></span> <br/> |<span data-ttu-id="9d42e-117">Konvertiert alle Texte in HTML.</span><span class="sxs-lookup"><span data-stu-id="9d42e-117">Converts all bodies to HTML.</span></span>  <br/> |
|<span data-ttu-id="9d42e-118">**Text**</span><span class="sxs-lookup"><span data-stu-id="9d42e-118">**Text**</span></span> <br/> |<span data-ttu-id="9d42e-119">Alle Texte konvertiert in nur-Text.</span><span class="sxs-lookup"><span data-stu-id="9d42e-119">Converts all bodies to plain text.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9d42e-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9d42e-120">Child elements</span></span>

<span data-ttu-id="9d42e-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="9d42e-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9d42e-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9d42e-122">Parent elements</span></span>

|<span data-ttu-id="9d42e-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="9d42e-123">**Element**</span></span>|<span data-ttu-id="9d42e-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d42e-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9d42e-125">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="9d42e-125">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="9d42e-126">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="9d42e-126">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="9d42e-127">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="9d42e-127">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="9d42e-128">Stellt ein Exchange-Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="9d42e-128">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="9d42e-129">DistributionList</span><span class="sxs-lookup"><span data-stu-id="9d42e-129">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="9d42e-130">Stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="9d42e-130">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="9d42e-131">Element</span><span class="sxs-lookup"><span data-stu-id="9d42e-131">Item</span></span>](item.md) <br/> |<span data-ttu-id="9d42e-132">Stellt ein Element im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="9d42e-132">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9d42e-133">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="9d42e-133">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="9d42e-134">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="9d42e-134">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9d42e-135">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="9d42e-135">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="9d42e-136">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="9d42e-136">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9d42e-137">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="9d42e-137">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="9d42e-138">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="9d42e-138">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9d42e-139">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="9d42e-139">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="9d42e-140">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="9d42e-140">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9d42e-141">Message</span><span class="sxs-lookup"><span data-stu-id="9d42e-141">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="9d42e-142">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="9d42e-142">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="9d42e-143">PostItem-Objekt</span><span class="sxs-lookup"><span data-stu-id="9d42e-143">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="9d42e-144">Stellt ein Post-Element im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="9d42e-144">Represents a post item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9d42e-145">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="9d42e-145">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="9d42e-146">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="9d42e-146">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9d42e-147">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="9d42e-147">Task</span></span>](task.md) <br/> |<span data-ttu-id="9d42e-148">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="9d42e-148">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9d42e-149">Textwert</span><span class="sxs-lookup"><span data-stu-id="9d42e-149">Text value</span></span>

<span data-ttu-id="9d42e-150">Keine.</span><span class="sxs-lookup"><span data-stu-id="9d42e-150">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9d42e-151">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9d42e-151">Remarks</span></span>

<span data-ttu-id="9d42e-152">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9d42e-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9d42e-153">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9d42e-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d42e-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d42e-154">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9d42e-155">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9d42e-155">Schema Name</span></span>  <br/> |<span data-ttu-id="9d42e-156">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9d42e-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="9d42e-157">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9d42e-157">Validation File</span></span>  <br/> |<span data-ttu-id="9d42e-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9d42e-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9d42e-159">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9d42e-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="9d42e-160">False</span><span class="sxs-lookup"><span data-stu-id="9d42e-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9d42e-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d42e-161">See also</span></span>



- [<span data-ttu-id="9d42e-162">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9d42e-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

