---
title: EventType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EventType
api_type:
- schema
ms.assetid: 04b70f9e-c226-4130-958e-0db0275cf58b
description: Das EventType-Element wird verwendet, um ein Abonnement zu erstellen und identifiziert ein Ereignis in einer Benachrichtigung gemeldet werden.
ms.openlocfilehash: fb54c9e042f105d10e68cb0e9b48feae7ed8bf7b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758278"
---
# <a name="eventtype"></a><span data-ttu-id="e0bd3-103">EventType</span><span class="sxs-lookup"><span data-stu-id="e0bd3-103">EventType</span></span>

<span data-ttu-id="e0bd3-104">Das **EventType** -Element wird verwendet, um ein Abonnement zu erstellen und identifiziert ein Ereignis in einer Benachrichtigung gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="e0bd3-104">The **EventType** element is used to create a subscription and identifies an event type to be reported in a notification.</span></span> 
  
```xml
<EventType/>
```

 <span data-ttu-id="e0bd3-105">**NotificationEventTypeType**</span><span class="sxs-lookup"><span data-stu-id="e0bd3-105">**NotificationEventTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e0bd3-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e0bd3-106">Attributes and elements</span></span>

<span data-ttu-id="e0bd3-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e0bd3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e0bd3-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e0bd3-108">Attributes</span></span>

<span data-ttu-id="e0bd3-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e0bd3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e0bd3-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e0bd3-110">Child elements</span></span>

<span data-ttu-id="e0bd3-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="e0bd3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e0bd3-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e0bd3-112">Parent elements</span></span>

|<span data-ttu-id="e0bd3-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e0bd3-113">**Element**</span></span>|<span data-ttu-id="e0bd3-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e0bd3-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e0bd3-115">EventTypes</span><span class="sxs-lookup"><span data-stu-id="e0bd3-115">EventTypes</span></span>](eventtypes.md) <br/> |<span data-ttu-id="e0bd3-116">Enthält eine Auflistung von Ereignis Benachrichtigung Ereignistypen, die zum Erstellen eines Abonnements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0bd3-116">Contains a collection of event notification event types that are used to create a subscription.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e0bd3-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="e0bd3-117">Text value</span></span>

<span data-ttu-id="e0bd3-118">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e0bd3-118">A text value is required.</span></span> <span data-ttu-id="e0bd3-119">Im Folgenden sind die möglichen Werte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="e0bd3-119">The following are the possible values:</span></span>
  
- <span data-ttu-id="e0bd3-120">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="e0bd3-120">CopiedEvent</span></span>
    
- <span data-ttu-id="e0bd3-121">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="e0bd3-121">CreatedEvent</span></span>
    
- <span data-ttu-id="e0bd3-122">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="e0bd3-122">DeletedEvent</span></span>
    
- <span data-ttu-id="e0bd3-123">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="e0bd3-123">ModifiedEvent</span></span>
    
- <span data-ttu-id="e0bd3-124">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="e0bd3-124">MovedEvent</span></span>
    
- <span data-ttu-id="e0bd3-125">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="e0bd3-125">NewMailEvent</span></span>
    
- <span data-ttu-id="e0bd3-126">FreeBusyChangedEvent</span><span class="sxs-lookup"><span data-stu-id="e0bd3-126">FreeBusyChangedEvent</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e0bd3-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e0bd3-127">Remarks</span></span>

<span data-ttu-id="e0bd3-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e0bd3-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e0bd3-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e0bd3-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0bd3-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="e0bd3-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e0bd3-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e0bd3-131">Schema Name</span></span>  <br/> |<span data-ttu-id="e0bd3-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e0bd3-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="e0bd3-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e0bd3-133">Validation File</span></span>  <br/> |<span data-ttu-id="e0bd3-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e0bd3-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e0bd3-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e0bd3-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="e0bd3-136">False</span><span class="sxs-lookup"><span data-stu-id="e0bd3-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e0bd3-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0bd3-137">See also</span></span>



[<span data-ttu-id="e0bd3-138">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="e0bd3-138">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="e0bd3-139">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e0bd3-139">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="e0bd3-140">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="e0bd3-140">Unsubscribe operation</span></span>](unsubscribe-operation.md)

