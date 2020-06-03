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
description: Das Subscribe-Element enthält die Eigenschaften, die zum Erstellen von Abonnements verwendet werden.
ms.openlocfilehash: f60e67654fb6af76e8081036a3463f5be401862d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530958"
---
# <a name="subscribe"></a><span data-ttu-id="587b5-103">Abonnieren</span><span class="sxs-lookup"><span data-stu-id="587b5-103">Subscribe</span></span>

<span data-ttu-id="587b5-104">Das **subscribe** -Element enthält die Eigenschaften, die zum Erstellen von Abonnements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="587b5-104">The **Subscribe** element contains the properties used to create subscriptions.</span></span> 
  
```XML
<Subscribe>
   <PullSubscriptionRequest/>
   <PushSubscriptionRequest/>
   <StreamingSubscriptionRequest/>
</Subscribe>
```

 <span data-ttu-id="587b5-105">**SubscribeType**</span><span class="sxs-lookup"><span data-stu-id="587b5-105">**SubscribeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="587b5-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="587b5-106">Attributes and elements</span></span>

<span data-ttu-id="587b5-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="587b5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="587b5-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="587b5-108">Attributes</span></span>

<span data-ttu-id="587b5-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="587b5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="587b5-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="587b5-110">Child elements</span></span>

|<span data-ttu-id="587b5-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="587b5-111">**Element**</span></span>|<span data-ttu-id="587b5-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="587b5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="587b5-113">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="587b5-113">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="587b5-114">Stellt ein Abonnement für eine Pull-basierte Ereignisbenachrichtigung dar.</span><span class="sxs-lookup"><span data-stu-id="587b5-114">Represents a subscription to a pull-based event notification.</span></span>  <br/> |
|[<span data-ttu-id="587b5-115">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="587b5-115">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="587b5-116">Stellt ein Abonnement für eine Push-basierte Ereignisbenachrichtigung dar.</span><span class="sxs-lookup"><span data-stu-id="587b5-116">Represents a subscription to a push-based event notification.</span></span>  <br/> |
|[<span data-ttu-id="587b5-117">StreamingSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="587b5-117">StreamingSubscriptionRequest</span></span>](streamingsubscriptionrequest.md) <br/> |<span data-ttu-id="587b5-118">Stellt ein Abonnement einer Streaming-Ereignisbenachrichtigung dar.</span><span class="sxs-lookup"><span data-stu-id="587b5-118">Represents a subscription to a streaming event notification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="587b5-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="587b5-119">Parent elements</span></span>

<span data-ttu-id="587b5-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="587b5-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="587b5-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="587b5-121">Remarks</span></span>

<span data-ttu-id="587b5-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="587b5-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="587b5-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="587b5-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="587b5-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="587b5-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="587b5-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="587b5-125">Schema name</span></span>  <br/> |<span data-ttu-id="587b5-126">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="587b5-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="587b5-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="587b5-127">Validation file</span></span>  <br/> |<span data-ttu-id="587b5-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="587b5-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="587b5-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="587b5-129">Can be empty</span></span>  <br/> |<span data-ttu-id="587b5-130">False</span><span class="sxs-lookup"><span data-stu-id="587b5-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="587b5-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="587b5-131">See also</span></span>



[<span data-ttu-id="587b5-132">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="587b5-132">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="587b5-133">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="587b5-133">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="587b5-134">GetStreamingEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="587b5-134">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="587b5-135">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="587b5-135">Unsubscribe operation</span></span>](unsubscribe-operation.md)

