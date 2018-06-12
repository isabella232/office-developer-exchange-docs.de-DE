---
title: RecipientTrackingEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecipientTrackingEvents
api_type:
- schema
ms.assetid: c4f729aa-674e-43b2-97f2-bf49740b0a34
description: Das Element RecipientTrackingEvents stellt eine Auflistung von Ereignissen, für eine Nachricht.
ms.openlocfilehash: 5fa5df422eff533891d021b77d5443b314d36244
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830993"
---
# <a name="recipienttrackingevents"></a><span data-ttu-id="7a7ff-103">RecipientTrackingEvents</span><span class="sxs-lookup"><span data-stu-id="7a7ff-103">RecipientTrackingEvents</span></span>

<span data-ttu-id="7a7ff-104">Das Element **RecipientTrackingEvents** stellt eine Auflistung von Ereignissen, für eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="7a7ff-104">The **RecipientTrackingEvents** element represents a collection of one or more events for a message.</span></span> 
  
```XML
<RecipientTrackingEvents>
   <RecipientTrackingEvent/>
</RecipientTrackingEvents>
```

 <span data-ttu-id="7a7ff-105">**ArrayOfRecipientTrackingEventType**</span><span class="sxs-lookup"><span data-stu-id="7a7ff-105">**ArrayOfRecipientTrackingEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7a7ff-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7a7ff-106">Attributes and elements</span></span>

<span data-ttu-id="7a7ff-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7a7ff-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7a7ff-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7a7ff-108">Attributes</span></span>

<span data-ttu-id="7a7ff-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7a7ff-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7a7ff-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7a7ff-110">Child elements</span></span>

|<span data-ttu-id="7a7ff-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="7a7ff-111">**Element**</span></span>|<span data-ttu-id="7a7ff-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7a7ff-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a7ff-113">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="7a7ff-113">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="7a7ff-114">Enthält Details für ein bestimmtes Ereignis in den Nachrichtenverfolgungsbericht.</span><span class="sxs-lookup"><span data-stu-id="7a7ff-114">Contains details for a specific event in the tracking report.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7a7ff-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7a7ff-115">Parent elements</span></span>

|<span data-ttu-id="7a7ff-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="7a7ff-116">**Element**</span></span>|<span data-ttu-id="7a7ff-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7a7ff-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a7ff-118">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="7a7ff-118">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="7a7ff-119">Enthält eine Nachricht, die in einem [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7a7ff-119">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a7ff-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7a7ff-120">Remarks</span></span>

<span data-ttu-id="7a7ff-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7a7ff-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7a7ff-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7a7ff-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7a7ff-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="7a7ff-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7a7ff-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7a7ff-124">Schema Name</span></span>  <br/> |<span data-ttu-id="7a7ff-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7a7ff-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="7a7ff-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7a7ff-126">Validation File</span></span>  <br/> |<span data-ttu-id="7a7ff-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7a7ff-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7a7ff-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7a7ff-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="7a7ff-129">False</span><span class="sxs-lookup"><span data-stu-id="7a7ff-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7a7ff-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a7ff-130">See also</span></span>



[<span data-ttu-id="7a7ff-131">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7a7ff-131">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="7a7ff-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7a7ff-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

