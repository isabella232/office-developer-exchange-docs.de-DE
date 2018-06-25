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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830993"
---
# <a name="recipienttrackingevents"></a><span data-ttu-id="f36c1-103">RecipientTrackingEvents</span><span class="sxs-lookup"><span data-stu-id="f36c1-103">RecipientTrackingEvents</span></span>

<span data-ttu-id="f36c1-104">Das Element **RecipientTrackingEvents** stellt eine Auflistung von Ereignissen, für eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="f36c1-104">The **RecipientTrackingEvents** element represents a collection of one or more events for a message.</span></span> 
  
```XML
<RecipientTrackingEvents>
   <RecipientTrackingEvent/>
</RecipientTrackingEvents>
```

 <span data-ttu-id="f36c1-105">**ArrayOfRecipientTrackingEventType**</span><span class="sxs-lookup"><span data-stu-id="f36c1-105">**ArrayOfRecipientTrackingEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f36c1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f36c1-106">Attributes and elements</span></span>

<span data-ttu-id="f36c1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f36c1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f36c1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f36c1-108">Attributes</span></span>

<span data-ttu-id="f36c1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f36c1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f36c1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f36c1-110">Child elements</span></span>

|<span data-ttu-id="f36c1-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f36c1-111">**Element**</span></span>|<span data-ttu-id="f36c1-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f36c1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f36c1-113">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="f36c1-113">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="f36c1-114">Enthält Details für ein bestimmtes Ereignis in den Nachrichtenverfolgungsbericht.</span><span class="sxs-lookup"><span data-stu-id="f36c1-114">Contains details for a specific event in the tracking report.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f36c1-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f36c1-115">Parent elements</span></span>

|<span data-ttu-id="f36c1-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="f36c1-116">**Element**</span></span>|<span data-ttu-id="f36c1-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f36c1-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f36c1-118">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="f36c1-118">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="f36c1-119">Enthält eine Nachricht, die in einem [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f36c1-119">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f36c1-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f36c1-120">Remarks</span></span>

<span data-ttu-id="f36c1-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f36c1-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f36c1-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f36c1-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f36c1-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="f36c1-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f36c1-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f36c1-124">Schema Name</span></span>  <br/> |<span data-ttu-id="f36c1-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f36c1-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="f36c1-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f36c1-126">Validation File</span></span>  <br/> |<span data-ttu-id="f36c1-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f36c1-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f36c1-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f36c1-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="f36c1-129">False</span><span class="sxs-lookup"><span data-stu-id="f36c1-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f36c1-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f36c1-130">See also</span></span>



[<span data-ttu-id="f36c1-131">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f36c1-131">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="f36c1-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f36c1-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

