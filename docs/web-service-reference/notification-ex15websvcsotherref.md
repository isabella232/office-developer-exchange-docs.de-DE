---
title: Benachrichtigung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Notification
api_type:
- schema
ms.assetid: c9070936-0930-438e-839c-91127256a6c8
description: Das Element Benachrichtigung enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.
ms.openlocfilehash: a769d8988eb68d0fa0b02f3838cd891e714571b6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830547"
---
# <a name="notification"></a><span data-ttu-id="5a4c9-103">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="5a4c9-103">Notification</span></span>

<span data-ttu-id="5a4c9-104">Das Element **Benachrichtigung** enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="5a4c9-104">The **Notification** element contains information about the subscription and the events that have occurred since the last notification.</span></span> 
  
```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <CopiedEvent/>
</Notification>
```

 <span data-ttu-id="5a4c9-105">**NotificationType**</span><span class="sxs-lookup"><span data-stu-id="5a4c9-105">**NotificationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5a4c9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5a4c9-106">Attributes and elements</span></span>

<span data-ttu-id="5a4c9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5a4c9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5a4c9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5a4c9-108">Attributes</span></span>

<span data-ttu-id="5a4c9-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5a4c9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5a4c9-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5a4c9-110">Child elements</span></span>

|<span data-ttu-id="5a4c9-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="5a4c9-111">**Element**</span></span>|<span data-ttu-id="5a4c9-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5a4c9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5a4c9-113">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="5a4c9-113">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="5a4c9-114">Stellt den Bezeichner für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5a4c9-114">Represents the identifier for a subscription.</span></span>  <br/> |
|[<span data-ttu-id="5a4c9-115">PreviousWatermark</span><span class="sxs-lookup"><span data-stu-id="5a4c9-115">PreviousWatermark</span></span>](previouswatermark.md) <br/> |<span data-ttu-id="5a4c9-116">Stellt das Wasserzeichen des letzten Ereignisses, die erfolgreich übermittelt wurde an den Client für das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5a4c9-116">Represents the watermark of the latest event that was successfully communicated to the client for the subscription.</span></span>  <br/> |
|[<span data-ttu-id="5a4c9-117">MoreEvents</span><span class="sxs-lookup"><span data-stu-id="5a4c9-117">MoreEvents</span></span>](moreevents.md) <br/> |<span data-ttu-id="5a4c9-118">Gibt an, ob es sind mehr Ereignisse in der Warteschlange an den Client übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="5a4c9-118">Indicates whether there are more events in the queue to be delivered to the client.</span></span>  <br/> |
|[<span data-ttu-id="5a4c9-119">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="5a4c9-119">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="5a4c9-120">Stellt ein Ereignis in der eines Elements oder Ordners kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="5a4c9-120">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="5a4c9-121">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="5a4c9-121">CreatedEvent</span></span>](createdevent.md) <br/> |<span data-ttu-id="5a4c9-122">Stellt ein Ereignis in der eines Elements oder Ordners erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5a4c9-122">Represents an event in which an item or folder is created.</span></span>  <br/> |
|[<span data-ttu-id="5a4c9-123">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="5a4c9-123">DeletedEvent</span></span>](deletedevent.md) <br/> |<span data-ttu-id="5a4c9-124">Stellt ein Ereignis in der eines Elements oder Ordners gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="5a4c9-124">Represents an event in which an item or folder is deleted.</span></span>  <br/> |
|[<span data-ttu-id="5a4c9-125">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="5a4c9-125">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="5a4c9-126">Stellt ein Ereignis in der eines Elements oder Ordners geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5a4c9-126">Represents an event in which an item or folder is modified.</span></span>  <br/> |
|[<span data-ttu-id="5a4c9-127">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="5a4c9-127">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="5a4c9-128">Stellt ein Ereignis in der eines Elements oder Ordners von einem übergeordneten Ordner in einer anderen übergeordneten Ordner verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="5a4c9-128">Represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
|[<span data-ttu-id="5a4c9-129">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="5a4c9-129">NewMailEvent</span></span>](newmailevent.md) <br/> |<span data-ttu-id="5a4c9-130">Stellt ein Ereignis, das durch eine neue e-Mail-Element in einem Postfach ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="5a4c9-130">Represents an event that is triggered by a new mail item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="5a4c9-131">StatusEvent</span><span class="sxs-lookup"><span data-stu-id="5a4c9-131">StatusEvent</span></span>](statusevent.md) <br/> |<span data-ttu-id="5a4c9-132">Stellt eine Benachrichtigung, dass keine neue Aktivität im Postfach aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="5a4c9-132">Represents a notification that no new activity has occurred in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="5a4c9-133">FreeBusyChangedEvent</span><span class="sxs-lookup"><span data-stu-id="5a4c9-133">FreeBusyChangedEvent</span></span>](freebusychangedevent.md) <br/> |<span data-ttu-id="5a4c9-134">Stellt ein Ereignis in der Frei/Gebucht-Zeit eines Elements geändert hat.</span><span class="sxs-lookup"><span data-stu-id="5a4c9-134">Represents an event in which an item's free/busy time has changed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5a4c9-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5a4c9-135">Parent elements</span></span>

|<span data-ttu-id="5a4c9-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="5a4c9-136">**Element**</span></span>|<span data-ttu-id="5a4c9-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5a4c9-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5a4c9-138">GetEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5a4c9-138">GetEventsResponseMessage</span></span>](geteventsresponsemessage.md) <br/> |<span data-ttu-id="5a4c9-139">Enthält den Status und das Ergebnis einer GetEvents Anforderung.</span><span class="sxs-lookup"><span data-stu-id="5a4c9-139">Contains the status and result of a single GetEvents request.</span></span>  <br/> |
|[<span data-ttu-id="5a4c9-140">SendNotificationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5a4c9-140">SendNotificationResponseMessage</span></span>](sendnotificationresponsemessage.md) <br/> |<span data-ttu-id="5a4c9-141">Enthält den Status und das Ergebnis einer SendNotification Anforderung.</span><span class="sxs-lookup"><span data-stu-id="5a4c9-141">Contains the status and result of a single SendNotification request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5a4c9-142">Textwert</span><span class="sxs-lookup"><span data-stu-id="5a4c9-142">Text value</span></span>

<span data-ttu-id="5a4c9-143">Keine.</span><span class="sxs-lookup"><span data-stu-id="5a4c9-143">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5a4c9-144">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5a4c9-144">Remarks</span></span>

<span data-ttu-id="5a4c9-145">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="5a4c9-145">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5a4c9-146">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5a4c9-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5a4c9-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="5a4c9-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5a4c9-148">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5a4c9-148">Schema Name</span></span>  <br/> |<span data-ttu-id="5a4c9-149">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5a4c9-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="5a4c9-150">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5a4c9-150">Validation File</span></span>  <br/> |<span data-ttu-id="5a4c9-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5a4c9-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5a4c9-152">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5a4c9-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="5a4c9-153">False</span><span class="sxs-lookup"><span data-stu-id="5a4c9-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5a4c9-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a4c9-154">See also</span></span>



[<span data-ttu-id="5a4c9-155">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="5a4c9-155">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="5a4c9-156">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5a4c9-156">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="5a4c9-157">GetStreamingEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5a4c9-157">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="5a4c9-158">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="5a4c9-158">Unsubscribe operation</span></span>](unsubscribe-operation.md)

