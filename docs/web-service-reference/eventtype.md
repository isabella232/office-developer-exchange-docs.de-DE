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
description: Das EventType-Element wird zum Erstellen eines Abonnements und zum Identifizieren eines Ereignistyps verwendet, der in einer Benachrichtigung gemeldet werden soll.
ms.openlocfilehash: 58c7ce571434b6fb8ac0b1dc2a3f8cd4fd56ff17
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526172"
---
# <a name="eventtype"></a><span data-ttu-id="3a108-103">EventType</span><span class="sxs-lookup"><span data-stu-id="3a108-103">EventType</span></span>

<span data-ttu-id="3a108-104">Das **eventType** -Element wird zum Erstellen eines Abonnements und zum Identifizieren eines Ereignistyps verwendet, der in einer Benachrichtigung gemeldet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3a108-104">The **EventType** element is used to create a subscription and identifies an event type to be reported in a notification.</span></span> 
  
```xml
<EventType/>
```

 <span data-ttu-id="3a108-105">**NotificationEventTypeType**</span><span class="sxs-lookup"><span data-stu-id="3a108-105">**NotificationEventTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3a108-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3a108-106">Attributes and elements</span></span>

<span data-ttu-id="3a108-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3a108-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3a108-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3a108-108">Attributes</span></span>

<span data-ttu-id="3a108-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3a108-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3a108-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3a108-110">Child elements</span></span>

<span data-ttu-id="3a108-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="3a108-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3a108-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3a108-112">Parent elements</span></span>

|<span data-ttu-id="3a108-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3a108-113">**Element**</span></span>|<span data-ttu-id="3a108-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3a108-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a108-115">EventTypes</span><span class="sxs-lookup"><span data-stu-id="3a108-115">EventTypes</span></span>](eventtypes.md) <br/> |<span data-ttu-id="3a108-116">Enthält eine Auflistung von Ereignis Benachrichtigungsereignis Typen, die zum Erstellen eines Abonnements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a108-116">Contains a collection of event notification event types that are used to create a subscription.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3a108-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="3a108-117">Text value</span></span>

<span data-ttu-id="3a108-118">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3a108-118">A text value is required.</span></span> <span data-ttu-id="3a108-119">Im Folgenden sind die möglichen Werte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="3a108-119">The following are the possible values:</span></span>
  
- <span data-ttu-id="3a108-120">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="3a108-120">CopiedEvent</span></span>
    
- <span data-ttu-id="3a108-121">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="3a108-121">CreatedEvent</span></span>
    
- <span data-ttu-id="3a108-122">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="3a108-122">DeletedEvent</span></span>
    
- <span data-ttu-id="3a108-123">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="3a108-123">ModifiedEvent</span></span>
    
- <span data-ttu-id="3a108-124">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="3a108-124">MovedEvent</span></span>
    
- <span data-ttu-id="3a108-125">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="3a108-125">NewMailEvent</span></span>
    
- <span data-ttu-id="3a108-126">FreeBusyChangedEvent</span><span class="sxs-lookup"><span data-stu-id="3a108-126">FreeBusyChangedEvent</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3a108-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a108-127">Remarks</span></span>

<span data-ttu-id="3a108-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3a108-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3a108-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3a108-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3a108-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a108-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3a108-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3a108-131">Schema Name</span></span>  <br/> |<span data-ttu-id="3a108-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3a108-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="3a108-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3a108-133">Validation File</span></span>  <br/> |<span data-ttu-id="3a108-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3a108-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3a108-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3a108-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="3a108-136">False</span><span class="sxs-lookup"><span data-stu-id="3a108-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3a108-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a108-137">See also</span></span>



[<span data-ttu-id="3a108-138">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="3a108-138">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="3a108-139">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3a108-139">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="3a108-140">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="3a108-140">Unsubscribe operation</span></span>](unsubscribe-operation.md)

