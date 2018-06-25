---
title: EventTypes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EventTypes
api_type:
- schema
ms.assetid: 29ded9e5-f191-4aa3-bc3e-500de2fc8818
description: EventTypes-Element enthält eine Auflistung von Benachrichtigung Ereignistypen, die zum Erstellen eines Abonnements verwendet werden.
ms.openlocfilehash: f4c622376f6b607ed390511d7bb5f0f723889420
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758280"
---
# <a name="eventtypes"></a><span data-ttu-id="38857-103">EventTypes</span><span class="sxs-lookup"><span data-stu-id="38857-103">EventTypes</span></span>

<span data-ttu-id="38857-104">**EventTypes** -Element enthält eine Auflistung von Benachrichtigung Ereignistypen, die zum Erstellen eines Abonnements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38857-104">The **EventTypes** element contains a collection of event notification types that are used to create a subscription.</span></span> 
  
```xml
<EventTypes>
   <EventType/>
</EventTypes>
```

 <span data-ttu-id="38857-105">**NonEmptyArrayOfNotificationEventTypesType**</span><span class="sxs-lookup"><span data-stu-id="38857-105">**NonEmptyArrayOfNotificationEventTypesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="38857-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="38857-106">Attributes and elements</span></span>

<span data-ttu-id="38857-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="38857-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="38857-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="38857-108">Attributes</span></span>

<span data-ttu-id="38857-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="38857-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="38857-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="38857-110">Child elements</span></span>

|<span data-ttu-id="38857-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="38857-111">**Element**</span></span>|<span data-ttu-id="38857-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="38857-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="38857-113">EventType</span><span class="sxs-lookup"><span data-stu-id="38857-113">EventType</span></span>](eventtype.md) <br/> |<span data-ttu-id="38857-114">Stellt einen angeforderte Benachrichtigung Ereignistyp, der zum Erstellen eines Abonnements verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="38857-114">Represents a requested event notification type that is used to create a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="38857-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="38857-115">Parent elements</span></span>

|<span data-ttu-id="38857-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="38857-116">**Element**</span></span>|<span data-ttu-id="38857-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="38857-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="38857-118">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="38857-118">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="38857-119">Stellt ein Abonnement für ein Benachrichtigungsabonnement Pull-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="38857-119">Represents a subscription to a pull-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="38857-120">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="38857-120">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="38857-121">Stellt ein Abonnement für ein Benachrichtigungsabonnement Push-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="38857-121">Represents a subscription to a push-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="38857-122">StreamingSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="38857-122">StreamingSubscriptionRequest</span></span>](streamingsubscriptionrequest.md) <br/> |<span data-ttu-id="38857-123">Stellt ein Abonnement für eine streaming Benachrichtigungsabonnement Ereignis dar.</span><span class="sxs-lookup"><span data-stu-id="38857-123">Represents a subscription to a streaming event notification subscription.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="38857-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="38857-124">Text value</span></span>

<span data-ttu-id="38857-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="38857-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="38857-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="38857-126">Remarks</span></span>

<span data-ttu-id="38857-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="38857-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="38857-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="38857-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="38857-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="38857-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="38857-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="38857-130">Schema Name</span></span>  <br/> |<span data-ttu-id="38857-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="38857-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="38857-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="38857-132">Validation File</span></span>  <br/> |<span data-ttu-id="38857-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="38857-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="38857-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="38857-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="38857-135">False</span><span class="sxs-lookup"><span data-stu-id="38857-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="38857-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38857-136">See also</span></span>



[<span data-ttu-id="38857-137">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="38857-137">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="38857-138">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="38857-138">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="38857-139">GetStreamingEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="38857-139">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="38857-140">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="38857-140">Unsubscribe operation</span></span>](unsubscribe-operation.md)

