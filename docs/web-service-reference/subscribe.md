---
title: Abonnieren
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Subscribe
api_type:
- schema
ms.assetid: 6c2ee57d-e216-4a94-92db-faa3cb0e244a
description: Das Subscribe-Element enthält die Eigenschaften, die zum Erstellen von Abonnements verwendet.
ms.openlocfilehash: 9f23f566f9105c655b289ed9b434c5e7b917207f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831618"
---
# <a name="subscribe"></a><span data-ttu-id="d9597-103">Abonnieren</span><span class="sxs-lookup"><span data-stu-id="d9597-103">Subscribe</span></span>

<span data-ttu-id="d9597-104">Das **Subscribe** -Element enthält die Eigenschaften, die zum Erstellen von Abonnements verwendet.</span><span class="sxs-lookup"><span data-stu-id="d9597-104">The **Subscribe** element contains the properties used to create subscriptions.</span></span> 
  
```XML
<Subscribe>
   <PullSubscriptionRequest/>
   <PushSubscriptionRequest/>
   <StreamingSubscriptionRequest/>
</Subscribe>
```

 <span data-ttu-id="d9597-105">**SubscribeType**</span><span class="sxs-lookup"><span data-stu-id="d9597-105">**SubscribeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d9597-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d9597-106">Attributes and elements</span></span>

<span data-ttu-id="d9597-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d9597-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d9597-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d9597-108">Attributes</span></span>

<span data-ttu-id="d9597-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d9597-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d9597-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d9597-110">Child elements</span></span>

|<span data-ttu-id="d9597-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d9597-111">**Element**</span></span>|<span data-ttu-id="d9597-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d9597-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d9597-113">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="d9597-113">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="d9597-114">Stellt ein Abonnement für eine Benachrichtigung Pull-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="d9597-114">Represents a subscription to a pull-based event notification.</span></span>  <br/> |
|[<span data-ttu-id="d9597-115">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="d9597-115">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="d9597-116">Stellt ein Abonnement für eine Benachrichtigung Push-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="d9597-116">Represents a subscription to a push-based event notification.</span></span>  <br/> |
|[<span data-ttu-id="d9597-117">StreamingSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="d9597-117">StreamingSubscriptionRequest</span></span>](streamingsubscriptionrequest.md) <br/> |<span data-ttu-id="d9597-118">Stellt ein Abonnement für eine streaming ereignisbenachrichtigung dar.</span><span class="sxs-lookup"><span data-stu-id="d9597-118">Represents a subscription to a streaming event notification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d9597-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d9597-119">Parent elements</span></span>

<span data-ttu-id="d9597-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="d9597-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d9597-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d9597-121">Remarks</span></span>

<span data-ttu-id="d9597-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d9597-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d9597-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d9597-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9597-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="d9597-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d9597-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d9597-125">Schema name</span></span>  <br/> |<span data-ttu-id="d9597-126">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d9597-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d9597-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d9597-127">Validation file</span></span>  <br/> |<span data-ttu-id="d9597-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d9597-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d9597-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d9597-129">Can be empty</span></span>  <br/> |<span data-ttu-id="d9597-130">False</span><span class="sxs-lookup"><span data-stu-id="d9597-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d9597-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9597-131">See also</span></span>



[<span data-ttu-id="d9597-132">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="d9597-132">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="d9597-133">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d9597-133">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="d9597-134">GetStreamingEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d9597-134">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="d9597-135">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="d9597-135">Unsubscribe operation</span></span>](unsubscribe-operation.md)

