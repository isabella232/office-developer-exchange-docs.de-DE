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
description: Das Benachrichtigungs Element enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.
ms.openlocfilehash: c4a5206c14985ec46cf40162a9ce4eaec68242ff
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530387"
---
# <a name="notification"></a><span data-ttu-id="d95a3-103">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="d95a3-103">Notification</span></span>

<span data-ttu-id="d95a3-104">Das **Benachrichtigungs** Element enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="d95a3-104">The **Notification** element contains information about the subscription and the events that have occurred since the last notification.</span></span> 
  
```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <CopiedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <CreatedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <DeletedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <ModifiedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <MovedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <NewMailEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <StatusEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <FreeBusyChangedEvent/>
</Notification>
```

<span data-ttu-id="d95a3-105">**NOTIFICATIONTYPE**</span><span class="sxs-lookup"><span data-stu-id="d95a3-105">**NotificationType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d95a3-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d95a3-106">Attributes and elements</span></span>

<span data-ttu-id="d95a3-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d95a3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d95a3-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d95a3-108">Attributes</span></span>

<span data-ttu-id="d95a3-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d95a3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d95a3-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d95a3-110">Child elements</span></span>

|<span data-ttu-id="d95a3-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d95a3-111">**Element**</span></span>|<span data-ttu-id="d95a3-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d95a3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d95a3-113">Abonnement-Nr (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="d95a3-113">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="d95a3-114">Stellt den Bezeichner für ein Abonnement dar.</span><span class="sxs-lookup"><span data-stu-id="d95a3-114">Represents the identifier for a subscription.</span></span>  <br/> |
|[<span data-ttu-id="d95a3-115">PreviousWatermark</span><span class="sxs-lookup"><span data-stu-id="d95a3-115">PreviousWatermark</span></span>](previouswatermark.md) <br/> |<span data-ttu-id="d95a3-116">Stellt das Wasserzeichen des letzten Ereignisses dar, das erfolgreich an den Client für das Abonnement kommuniziert wurde.</span><span class="sxs-lookup"><span data-stu-id="d95a3-116">Represents the watermark of the latest event that was successfully communicated to the client for the subscription.</span></span>  <br/> |
|[<span data-ttu-id="d95a3-117">MoreEvents</span><span class="sxs-lookup"><span data-stu-id="d95a3-117">MoreEvents</span></span>](moreevents.md) <br/> |<span data-ttu-id="d95a3-118">Gibt an, ob weitere Ereignisse in der Warteschlange an den Client übermittelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d95a3-118">Indicates whether there are more events in the queue to be delivered to the client.</span></span>  <br/> |
|[<span data-ttu-id="d95a3-119">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="d95a3-119">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="d95a3-120">Stellt ein Ereignis dar, in dem ein Element oder ein Ordner kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="d95a3-120">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="d95a3-121">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="d95a3-121">CreatedEvent</span></span>](createdevent.md) <br/> |<span data-ttu-id="d95a3-122">Stellt ein Ereignis dar, in dem ein Element oder ein Ordner erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d95a3-122">Represents an event in which an item or folder is created.</span></span>  <br/> |
|[<span data-ttu-id="d95a3-123">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="d95a3-123">DeletedEvent</span></span>](deletedevent.md) <br/> |<span data-ttu-id="d95a3-124">Stellt ein Ereignis dar, in dem ein Element oder ein Ordner gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="d95a3-124">Represents an event in which an item or folder is deleted.</span></span>  <br/> |
|[<span data-ttu-id="d95a3-125">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="d95a3-125">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="d95a3-126">Stellt ein Ereignis dar, in dem ein Element oder ein Ordner geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d95a3-126">Represents an event in which an item or folder is modified.</span></span>  <br/> |
|[<span data-ttu-id="d95a3-127">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="d95a3-127">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="d95a3-128">Stellt ein Ereignis dar, in dem ein Element oder ein Ordner von einem übergeordneten Ordner in einen anderen übergeordneten Ordner verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="d95a3-128">Represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
|[<span data-ttu-id="d95a3-129">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="d95a3-129">NewMailEvent</span></span>](newmailevent.md) <br/> |<span data-ttu-id="d95a3-130">Stellt ein Ereignis dar, das durch ein neues e-Mail-Element in einem Postfach ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="d95a3-130">Represents an event that is triggered by a new mail item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d95a3-131">StatusEvent</span><span class="sxs-lookup"><span data-stu-id="d95a3-131">StatusEvent</span></span>](statusevent.md) <br/> |<span data-ttu-id="d95a3-132">Stellt eine Benachrichtigung dar, dass keine neue Aktivität im Postfach aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="d95a3-132">Represents a notification that no new activity has occurred in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d95a3-133">FreeBusyChangedEvent</span><span class="sxs-lookup"><span data-stu-id="d95a3-133">FreeBusyChangedEvent</span></span>](freebusychangedevent.md) <br/> |<span data-ttu-id="d95a3-134">Stellt ein Ereignis dar, in dem die Frei/Gebucht-Zeit eines Elements geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="d95a3-134">Represents an event in which an item's free/busy time has changed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d95a3-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d95a3-135">Parent elements</span></span>

|<span data-ttu-id="d95a3-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="d95a3-136">**Element**</span></span>|<span data-ttu-id="d95a3-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d95a3-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d95a3-138">GetEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d95a3-138">GetEventsResponseMessage</span></span>](geteventsresponsemessage.md) <br/> |<span data-ttu-id="d95a3-139">Enthält den Status und das Ergebnis einer einzelnen GetEvents-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d95a3-139">Contains the status and result of a single GetEvents request.</span></span>  <br/> |
|[<span data-ttu-id="d95a3-140">Sendnotificationresponsemessage zurück</span><span class="sxs-lookup"><span data-stu-id="d95a3-140">SendNotificationResponseMessage</span></span>](sendnotificationresponsemessage.md) <br/> |<span data-ttu-id="d95a3-141">Enthält den Status und das Ergebnis einer einzelnen SendNotification-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d95a3-141">Contains the status and result of a single SendNotification request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d95a3-142">Textwert</span><span class="sxs-lookup"><span data-stu-id="d95a3-142">Text value</span></span>

<span data-ttu-id="d95a3-143">Keine.</span><span class="sxs-lookup"><span data-stu-id="d95a3-143">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d95a3-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d95a3-144">Remarks</span></span>

<span data-ttu-id="d95a3-145">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d95a3-145">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d95a3-146">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d95a3-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d95a3-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="d95a3-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d95a3-148">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d95a3-148">Schema Name</span></span>  <br/> |<span data-ttu-id="d95a3-149">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d95a3-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="d95a3-150">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d95a3-150">Validation File</span></span>  <br/> |<span data-ttu-id="d95a3-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d95a3-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d95a3-152">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d95a3-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="d95a3-153">False</span><span class="sxs-lookup"><span data-stu-id="d95a3-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d95a3-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d95a3-154">See also</span></span>

- [<span data-ttu-id="d95a3-155">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="d95a3-155">Subscribe operation</span></span>](subscribe-operation.md) 
- [<span data-ttu-id="d95a3-156">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d95a3-156">GetEvents operation</span></span>](getevents-operation.md) 
- [<span data-ttu-id="d95a3-157">GetStreamingEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d95a3-157">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md) 
- [<span data-ttu-id="d95a3-158">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="d95a3-158">Unsubscribe operation</span></span>](unsubscribe-operation.md)

