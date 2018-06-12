---
title: RecipientTrackingEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecipientTrackingEvent
api_type:
- schema
ms.assetid: 2bffdac7-c2f5-4805-ae7e-bd865301acb6
description: Das RecipientTrackingEvent-Element enthält Informationen für ein einzelnes Ereignis für einen Empfänger an.
ms.openlocfilehash: c5488ba105f9a853a490d6f0f4ff9ff15b537e23
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830989"
---
# <a name="recipienttrackingevent"></a><span data-ttu-id="6e8a9-103">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="6e8a9-103">RecipientTrackingEvent</span></span>

<span data-ttu-id="6e8a9-104">Das **RecipientTrackingEvent** -Element enthält Informationen für ein einzelnes Ereignis für einen Empfänger an.</span><span class="sxs-lookup"><span data-stu-id="6e8a9-104">The **RecipientTrackingEvent** element contains information for a single event for a recipient.</span></span> 
  
```XML
<RecipientTrackingEvent>
   <Date/>
   <Recipient/>
   <DeliveryStatus/>
   <EventDescription/>
   <EventData/>
   <Server/>
   <InternalId/>
   <BccRecipient/>
   <HiddenRecipient/>
   <UniquePathId/>
   <RootAddress/>
   <Properties/>
</RecipientTrackingEvent>
```

 <span data-ttu-id="6e8a9-105">**RecipientTrackingEventType**</span><span class="sxs-lookup"><span data-stu-id="6e8a9-105">**RecipientTrackingEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6e8a9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6e8a9-106">Attributes and elements</span></span>

<span data-ttu-id="6e8a9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6e8a9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6e8a9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6e8a9-108">Attributes</span></span>

<span data-ttu-id="6e8a9-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6e8a9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6e8a9-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6e8a9-110">Child elements</span></span>

|<span data-ttu-id="6e8a9-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="6e8a9-111">**Element**</span></span>|<span data-ttu-id="6e8a9-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6e8a9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6e8a9-113">Datum (MessageTracking)</span><span class="sxs-lookup"><span data-stu-id="6e8a9-113">Date (MessageTracking)</span></span>](date-messagetracking.md) <br/> |<span data-ttu-id="6e8a9-114">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6e8a9-114">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="6e8a9-115">Recipient</span><span class="sxs-lookup"><span data-stu-id="6e8a9-115">Recipient</span></span>](recipient.md) <br/> |<span data-ttu-id="6e8a9-116">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6e8a9-116">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="6e8a9-117">DeliveryStatus</span><span class="sxs-lookup"><span data-stu-id="6e8a9-117">DeliveryStatus</span></span>](deliverystatus.md) <br/> |<span data-ttu-id="6e8a9-118">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6e8a9-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="6e8a9-119">EventDescription</span><span class="sxs-lookup"><span data-stu-id="6e8a9-119">EventDescription</span></span>](eventdescription.md) <br/> |<span data-ttu-id="6e8a9-120">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6e8a9-120">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="6e8a9-121">EventData</span><span class="sxs-lookup"><span data-stu-id="6e8a9-121">EventData</span></span>](eventdata.md) <br/> |<span data-ttu-id="6e8a9-122">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="6e8a9-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="6e8a9-123">Server (MessageTracking)</span><span class="sxs-lookup"><span data-stu-id="6e8a9-123">Server (MessageTracking)</span></span>](server-messagetracking.md) <br/> |<span data-ttu-id="6e8a9-124">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6e8a9-124">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="6e8a9-125">InternalId</span><span class="sxs-lookup"><span data-stu-id="6e8a9-125">InternalId</span></span>](internalid.md) <br/> |<span data-ttu-id="6e8a9-126">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6e8a9-126">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="6e8a9-127">BccRecipient</span><span class="sxs-lookup"><span data-stu-id="6e8a9-127">BccRecipient</span></span>](bccrecipient.md) <br/> |<span data-ttu-id="6e8a9-128">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="6e8a9-128">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="6e8a9-129">HiddenRecipient</span><span class="sxs-lookup"><span data-stu-id="6e8a9-129">HiddenRecipient</span></span>](hiddenrecipient.md) <br/> |<span data-ttu-id="6e8a9-130">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="6e8a9-130">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="6e8a9-131">UniquePathId</span><span class="sxs-lookup"><span data-stu-id="6e8a9-131">UniquePathId</span></span>](uniquepathid.md) <br/> |<span data-ttu-id="6e8a9-132">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="6e8a9-132">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="6e8a9-133">RootAddress</span><span class="sxs-lookup"><span data-stu-id="6e8a9-133">RootAddress</span></span>](rootaddress.md) <br/> |<span data-ttu-id="6e8a9-134">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="6e8a9-134">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="6e8a9-135">Eigenschaften (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="6e8a9-135">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="6e8a9-136">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="6e8a9-136">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6e8a9-137">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6e8a9-137">Parent elements</span></span>

|<span data-ttu-id="6e8a9-138">**Element**</span><span class="sxs-lookup"><span data-stu-id="6e8a9-138">**Element**</span></span>|<span data-ttu-id="6e8a9-139">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6e8a9-139">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6e8a9-140">RecipientTrackingEvents</span><span class="sxs-lookup"><span data-stu-id="6e8a9-140">RecipientTrackingEvents</span></span>](recipienttrackingevents.md) <br/> |<span data-ttu-id="6e8a9-141">Enthält eine Liste mit mindestens Überwachungsereignissen für einen Empfänger an.</span><span class="sxs-lookup"><span data-stu-id="6e8a9-141">Contains a list of one or more tracking events for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6e8a9-142">Textwert</span><span class="sxs-lookup"><span data-stu-id="6e8a9-142">Text value</span></span>

<span data-ttu-id="6e8a9-143">Keine.</span><span class="sxs-lookup"><span data-stu-id="6e8a9-143">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6e8a9-144">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6e8a9-144">Remarks</span></span>

<span data-ttu-id="6e8a9-145">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="6e8a9-145">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6e8a9-146">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6e8a9-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6e8a9-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="6e8a9-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6e8a9-148">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6e8a9-148">Schema Name</span></span>  <br/> |<span data-ttu-id="6e8a9-149">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6e8a9-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="6e8a9-150">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6e8a9-150">Validation File</span></span>  <br/> |<span data-ttu-id="6e8a9-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6e8a9-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6e8a9-152">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6e8a9-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="6e8a9-153">False</span><span class="sxs-lookup"><span data-stu-id="6e8a9-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6e8a9-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e8a9-154">See also</span></span>



[<span data-ttu-id="6e8a9-155">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6e8a9-155">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="6e8a9-156">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6e8a9-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

