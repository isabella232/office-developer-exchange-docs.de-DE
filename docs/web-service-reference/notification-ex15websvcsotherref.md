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
ms.openlocfilehash: 942ec18521fc484a7a3aa1385fb54f480ce9d11f
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354351"
---
# <a name="notification"></a><span data-ttu-id="88886-103">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="88886-103">Notification</span></span>

<span data-ttu-id="88886-104">Das Element **Benachrichtigung** enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="88886-104">The **Notification** element contains information about the subscription and the events that have occurred since the last notification.</span></span> 
  
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

<span data-ttu-id="88886-105">**NotificationType**</span><span class="sxs-lookup"><span data-stu-id="88886-105">**NotificationType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="88886-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="88886-106">Attributes and elements</span></span>

<span data-ttu-id="88886-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="88886-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="88886-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="88886-108">Attributes</span></span>

<span data-ttu-id="88886-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="88886-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="88886-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="88886-110">Child elements</span></span>

|<span data-ttu-id="88886-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="88886-111">**Element**</span></span>|<span data-ttu-id="88886-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="88886-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="88886-113">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="88886-113">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="88886-114">Stellt den Bezeichner für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="88886-114">Represents the identifier for a subscription.</span></span>  <br/> |
|[<span data-ttu-id="88886-115">PreviousWatermark</span><span class="sxs-lookup"><span data-stu-id="88886-115">PreviousWatermark</span></span>](previouswatermark.md) <br/> |<span data-ttu-id="88886-116">Stellt das Wasserzeichen des letzten Ereignisses, die erfolgreich übermittelt wurde an den Client für das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="88886-116">Represents the watermark of the latest event that was successfully communicated to the client for the subscription.</span></span>  <br/> |
|[<span data-ttu-id="88886-117">MoreEvents</span><span class="sxs-lookup"><span data-stu-id="88886-117">MoreEvents</span></span>](moreevents.md) <br/> |<span data-ttu-id="88886-118">Gibt an, ob es sind mehr Ereignisse in der Warteschlange an den Client übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="88886-118">Indicates whether there are more events in the queue to be delivered to the client.</span></span>  <br/> |
|[<span data-ttu-id="88886-119">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="88886-119">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="88886-120">Stellt ein Ereignis in der eines Elements oder Ordners kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="88886-120">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="88886-121">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="88886-121">CreatedEvent</span></span>](createdevent.md) <br/> |<span data-ttu-id="88886-122">Stellt ein Ereignis in der eines Elements oder Ordners erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="88886-122">Represents an event in which an item or folder is created.</span></span>  <br/> |
|[<span data-ttu-id="88886-123">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="88886-123">DeletedEvent</span></span>](deletedevent.md) <br/> |<span data-ttu-id="88886-124">Stellt ein Ereignis in der eines Elements oder Ordners gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="88886-124">Represents an event in which an item or folder is deleted.</span></span>  <br/> |
|[<span data-ttu-id="88886-125">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="88886-125">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="88886-126">Stellt ein Ereignis in der eines Elements oder Ordners geändert wird.</span><span class="sxs-lookup"><span data-stu-id="88886-126">Represents an event in which an item or folder is modified.</span></span>  <br/> |
|[<span data-ttu-id="88886-127">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="88886-127">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="88886-128">Stellt ein Ereignis in der eines Elements oder Ordners von einem übergeordneten Ordner in einer anderen übergeordneten Ordner verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="88886-128">Represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
|[<span data-ttu-id="88886-129">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="88886-129">NewMailEvent</span></span>](newmailevent.md) <br/> |<span data-ttu-id="88886-130">Stellt ein Ereignis, das durch eine neue e-Mail-Element in einem Postfach ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="88886-130">Represents an event that is triggered by a new mail item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="88886-131">StatusEvent</span><span class="sxs-lookup"><span data-stu-id="88886-131">StatusEvent</span></span>](statusevent.md) <br/> |<span data-ttu-id="88886-132">Stellt eine Benachrichtigung, dass keine neue Aktivität im Postfach aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="88886-132">Represents a notification that no new activity has occurred in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="88886-133">FreeBusyChangedEvent</span><span class="sxs-lookup"><span data-stu-id="88886-133">FreeBusyChangedEvent</span></span>](freebusychangedevent.md) <br/> |<span data-ttu-id="88886-134">Stellt ein Ereignis in der Frei/Gebucht-Zeit eines Elements geändert hat.</span><span class="sxs-lookup"><span data-stu-id="88886-134">Represents an event in which an item's free/busy time has changed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="88886-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="88886-135">Parent elements</span></span>

|<span data-ttu-id="88886-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="88886-136">**Element**</span></span>|<span data-ttu-id="88886-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="88886-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="88886-138">GetEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="88886-138">GetEventsResponseMessage</span></span>](geteventsresponsemessage.md) <br/> |<span data-ttu-id="88886-139">Enthält den Status und das Ergebnis einer GetEvents Anforderung.</span><span class="sxs-lookup"><span data-stu-id="88886-139">Contains the status and result of a single GetEvents request.</span></span>  <br/> |
|[<span data-ttu-id="88886-140">SendNotificationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="88886-140">SendNotificationResponseMessage</span></span>](sendnotificationresponsemessage.md) <br/> |<span data-ttu-id="88886-141">Enthält den Status und das Ergebnis einer SendNotification Anforderung.</span><span class="sxs-lookup"><span data-stu-id="88886-141">Contains the status and result of a single SendNotification request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="88886-142">Textwert</span><span class="sxs-lookup"><span data-stu-id="88886-142">Text value</span></span>

<span data-ttu-id="88886-143">Keine.</span><span class="sxs-lookup"><span data-stu-id="88886-143">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="88886-144">Hinweise</span><span class="sxs-lookup"><span data-stu-id="88886-144">Remarks</span></span>

<span data-ttu-id="88886-145">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="88886-145">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="88886-146">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="88886-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88886-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="88886-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="88886-148">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="88886-148">Schema Name</span></span>  <br/> |<span data-ttu-id="88886-149">Schematypen</span><span class="sxs-lookup"><span data-stu-id="88886-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="88886-150">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="88886-150">Validation File</span></span>  <br/> |<span data-ttu-id="88886-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="88886-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="88886-152">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="88886-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="88886-153">False</span><span class="sxs-lookup"><span data-stu-id="88886-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="88886-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88886-154">See also</span></span>

- [<span data-ttu-id="88886-155">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="88886-155">Subscribe operation</span></span>](subscribe-operation.md) 
- [<span data-ttu-id="88886-156">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="88886-156">GetEvents operation</span></span>](getevents-operation.md) 
- [<span data-ttu-id="88886-157">GetStreamingEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="88886-157">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md) 
- [<span data-ttu-id="88886-158">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="88886-158">Unsubscribe operation</span></span>](unsubscribe-operation.md)

