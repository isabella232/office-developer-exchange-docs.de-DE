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
description: Das RecipientTrackingEvent-Element enthält Informationen für ein einzelnes Ereignis für einen Empfänger.
ms.openlocfilehash: e9a014cdfac122f112205cfa5032535a770f9d82
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465485"
---
# <a name="recipienttrackingevent"></a><span data-ttu-id="c4663-103">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="c4663-103">RecipientTrackingEvent</span></span>

<span data-ttu-id="c4663-104">Das **RecipientTrackingEvent** -Element enthält Informationen für ein einzelnes Ereignis für einen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="c4663-104">The **RecipientTrackingEvent** element contains information for a single event for a recipient.</span></span> 
  
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

 <span data-ttu-id="c4663-105">**RecipientTrackingEventType**</span><span class="sxs-lookup"><span data-stu-id="c4663-105">**RecipientTrackingEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c4663-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c4663-106">Attributes and elements</span></span>

<span data-ttu-id="c4663-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c4663-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c4663-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c4663-108">Attributes</span></span>

<span data-ttu-id="c4663-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c4663-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c4663-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c4663-110">Child elements</span></span>

|<span data-ttu-id="c4663-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c4663-111">**Element**</span></span>|<span data-ttu-id="c4663-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c4663-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4663-113">Datum (MessageTracking)</span><span class="sxs-lookup"><span data-stu-id="c4663-113">Date (MessageTracking)</span></span>](date-messagetracking.md) <br/> |<span data-ttu-id="c4663-114">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c4663-114">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="c4663-115">Empfänger</span><span class="sxs-lookup"><span data-stu-id="c4663-115">Recipient</span></span>](recipient.md) <br/> |<span data-ttu-id="c4663-116">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c4663-116">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="c4663-117">DeliveryStatus</span><span class="sxs-lookup"><span data-stu-id="c4663-117">DeliveryStatus</span></span>](deliverystatus.md) <br/> |<span data-ttu-id="c4663-118">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c4663-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="c4663-119">EventDescription</span><span class="sxs-lookup"><span data-stu-id="c4663-119">EventDescription</span></span>](eventdescription.md) <br/> |<span data-ttu-id="c4663-120">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c4663-120">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="c4663-121">EventData</span><span class="sxs-lookup"><span data-stu-id="c4663-121">EventData</span></span>](eventdata.md) <br/> |<span data-ttu-id="c4663-122">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="c4663-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="c4663-123">Server (MessageTracking)</span><span class="sxs-lookup"><span data-stu-id="c4663-123">Server (MessageTracking)</span></span>](server-messagetracking.md) <br/> |<span data-ttu-id="c4663-124">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c4663-124">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="c4663-125">Interne-Nr</span><span class="sxs-lookup"><span data-stu-id="c4663-125">InternalId</span></span>](internalid.md) <br/> |<span data-ttu-id="c4663-126">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c4663-126">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="c4663-127">BccRecipient</span><span class="sxs-lookup"><span data-stu-id="c4663-127">BccRecipient</span></span>](bccrecipient.md) <br/> |<span data-ttu-id="c4663-128">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="c4663-128">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="c4663-129">HiddenRecipient</span><span class="sxs-lookup"><span data-stu-id="c4663-129">HiddenRecipient</span></span>](hiddenrecipient.md) <br/> |<span data-ttu-id="c4663-130">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="c4663-130">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="c4663-131">UniquePathId</span><span class="sxs-lookup"><span data-stu-id="c4663-131">UniquePathId</span></span>](uniquepathid.md) <br/> |<span data-ttu-id="c4663-132">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="c4663-132">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="c4663-133">RootAddress</span><span class="sxs-lookup"><span data-stu-id="c4663-133">RootAddress</span></span>](rootaddress.md) <br/> |<span data-ttu-id="c4663-134">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="c4663-134">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="c4663-135">Eigenschaften (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="c4663-135">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="c4663-136">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="c4663-136">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c4663-137">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c4663-137">Parent elements</span></span>

|<span data-ttu-id="c4663-138">**Element**</span><span class="sxs-lookup"><span data-stu-id="c4663-138">**Element**</span></span>|<span data-ttu-id="c4663-139">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c4663-139">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4663-140">RecipientTrackingEvents</span><span class="sxs-lookup"><span data-stu-id="c4663-140">RecipientTrackingEvents</span></span>](recipienttrackingevents.md) <br/> |<span data-ttu-id="c4663-141">Enthält eine Liste mit einem oder mehreren Überwachungsereignissen für einen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="c4663-141">Contains a list of one or more tracking events for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c4663-142">Textwert</span><span class="sxs-lookup"><span data-stu-id="c4663-142">Text value</span></span>

<span data-ttu-id="c4663-143">Keine.</span><span class="sxs-lookup"><span data-stu-id="c4663-143">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c4663-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4663-144">Remarks</span></span>

<span data-ttu-id="c4663-145">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c4663-145">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c4663-146">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c4663-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4663-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="c4663-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c4663-148">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c4663-148">Schema Name</span></span>  <br/> |<span data-ttu-id="c4663-149">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c4663-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="c4663-150">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c4663-150">Validation File</span></span>  <br/> |<span data-ttu-id="c4663-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c4663-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c4663-152">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c4663-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="c4663-153">False</span><span class="sxs-lookup"><span data-stu-id="c4663-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c4663-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4663-154">See also</span></span>



[<span data-ttu-id="c4663-155">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c4663-155">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="c4663-156">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c4663-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

