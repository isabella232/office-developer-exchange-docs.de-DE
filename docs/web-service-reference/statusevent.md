---
title: StatusEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StatusEvent
api_type:
- schema
ms.assetid: d3901818-2640-4bed-aad8-21a61aee62a1
description: Das Element StatusEvent stellt eine Benachrichtigung, dass keine neue Aktivität im Postfach aufgetreten ist.
ms.openlocfilehash: e214918f9795e9e29061d4aac72ab144d2b24267
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831592"
---
# <a name="statusevent"></a><span data-ttu-id="24c9b-103">StatusEvent</span><span class="sxs-lookup"><span data-stu-id="24c9b-103">StatusEvent</span></span>

<span data-ttu-id="24c9b-104">Das Element **StatusEvent** stellt eine Benachrichtigung, dass keine neue Aktivität im Postfach aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="24c9b-104">The **StatusEvent** element represents a notification that no new activity has occurred in the mailbox.</span></span> 
  
```xml
<StatusEvent>
   <Watermark/>
</StatusEvent>
```

 <span data-ttu-id="24c9b-105">**BaseNotificationEventType**</span><span class="sxs-lookup"><span data-stu-id="24c9b-105">**BaseNotificationEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="24c9b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="24c9b-106">Attributes and elements</span></span>

<span data-ttu-id="24c9b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="24c9b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="24c9b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="24c9b-108">Attributes</span></span>

<span data-ttu-id="24c9b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="24c9b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="24c9b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="24c9b-110">Child elements</span></span>

|<span data-ttu-id="24c9b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="24c9b-111">**Element**</span></span>|<span data-ttu-id="24c9b-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="24c9b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="24c9b-113">Wasserzeichen</span><span class="sxs-lookup"><span data-stu-id="24c9b-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="24c9b-114">Stellt das letzte gültige Wasserzeichen für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="24c9b-114">Represents the last valid watermark for a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="24c9b-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="24c9b-115">Parent elements</span></span>

|<span data-ttu-id="24c9b-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="24c9b-116">**Element**</span></span>|<span data-ttu-id="24c9b-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="24c9b-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="24c9b-118">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="24c9b-118">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="24c9b-119">Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="24c9b-119">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24c9b-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="24c9b-120">Remarks</span></span>

<span data-ttu-id="24c9b-121">Das **StatusEvent** -Element wird in einer Benachrichtigung für einen der folgenden Gründe zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="24c9b-121">The **StatusEvent** element is returned in a notification for one of the following reasons:</span></span> 
  
- <span data-ttu-id="24c9b-122">Ein Pull-Client sendet eine Anforderung GetEvents auf einem Abonnement, das keine Aktivität verfügt.</span><span class="sxs-lookup"><span data-stu-id="24c9b-122">A pull client issues a GetEvents request on a subscription that has no activity.</span></span>
    
- <span data-ttu-id="24c9b-123">Ein Push-Client hat keine Ereignisse in der Warteschlange, wenn die [StatusFrequency](statusfrequency.md) erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="24c9b-123">A push client has no events in the queue when the [StatusFrequency](statusfrequency.md) has been reached.</span></span> 
    
<span data-ttu-id="24c9b-124">Das **StatusEvent**[Wasserzeichen](watermark.md) wird von einer Clientanwendung in die gleiche Weise wie das Ereignis Typ Wasserzeichen verwendet.</span><span class="sxs-lookup"><span data-stu-id="24c9b-124">The **StatusEvent**[Watermark](watermark.md) is used by a client application in the same manner as the other event type watermarks.</span></span> <span data-ttu-id="24c9b-125">Das Wasserzeichen für die **StatusEvent** ist jedoch nicht identisch mit der Wasserzeichen für andere Ereignisse verwendet.</span><span class="sxs-lookup"><span data-stu-id="24c9b-125">However, the watermark for the **StatusEvent** is not the same as the watermarks used for other events.</span></span> <span data-ttu-id="24c9b-126">Angenommen, haben ein Abonnement von Ereignissen mit Wasserzeichen 1 aufweist, 2 und 3 und die Ereignisse, die erfolgreich in einer Benachrichtigung mitgeteilt wurden.</span><span class="sxs-lookup"><span data-stu-id="24c9b-126">For example, a subscription has events with watermarks 1, 2, and 3 and those events have been successfully communicated in a notification.</span></span> <span data-ttu-id="24c9b-127">Tritt auf ein Zeitraum der Inaktivität, und eine Anforderung **GetEvents** gesendet.</span><span class="sxs-lookup"><span data-stu-id="24c9b-127">A period of inactivity occurs and a **GetEvents** request is sent.</span></span> <span data-ttu-id="24c9b-128">Der Clientzugriffsserver (CAS) liefert ein Statusereignis und das letzte Wasserzeichen, 3, als die [PreviousWatermark](previouswatermark.md) und das aktuelle [Wasserzeichen](watermark.md).</span><span class="sxs-lookup"><span data-stu-id="24c9b-128">The Client Access server (CAS) returns a status event and includes the last watermark, 3, as both the [PreviousWatermark](previouswatermark.md) and the current [Watermark](watermark.md).</span></span>
  
<span data-ttu-id="24c9b-129">Das Wasserzeichen wird nicht in allen Fällen unverändert.</span><span class="sxs-lookup"><span data-stu-id="24c9b-129">The watermark will not remain the same in all cases.</span></span> <span data-ttu-id="24c9b-130">Einträge werden für 30 Tage beibehalten.</span><span class="sxs-lookup"><span data-stu-id="24c9b-130">Event entries are maintained for 30 days.</span></span> <span data-ttu-id="24c9b-131">Um ein aktives Abonnement zu gewährleisten, aktualisiert die CAS in regelmäßigen Abständen die Wasserzeichen für Abonnementwarteschlangen.</span><span class="sxs-lookup"><span data-stu-id="24c9b-131">To maintain an active subscription, the CAS periodically updates the watermarks for subscription queues.</span></span> <span data-ttu-id="24c9b-132">Die aktualisierten Wasserzeichen sind an Clients gesendet, um ein aktives Abonnement verwalten.</span><span class="sxs-lookup"><span data-stu-id="24c9b-132">The updated watermarks are sent to clients to maintain an active subscription.</span></span>
  
<span data-ttu-id="24c9b-133">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="24c9b-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="24c9b-134">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="24c9b-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="24c9b-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="24c9b-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="24c9b-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="24c9b-136">Schema name</span></span>  <br/> |<span data-ttu-id="24c9b-137">Schematypen</span><span class="sxs-lookup"><span data-stu-id="24c9b-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="24c9b-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="24c9b-138">Validation file</span></span>  <br/> |<span data-ttu-id="24c9b-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="24c9b-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="24c9b-140">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="24c9b-140">Can be empty</span></span>  <br/> |<span data-ttu-id="24c9b-141">False</span><span class="sxs-lookup"><span data-stu-id="24c9b-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="24c9b-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24c9b-142">See also</span></span>



[<span data-ttu-id="24c9b-143">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="24c9b-143">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="24c9b-144">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="24c9b-144">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="24c9b-145">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="24c9b-145">Unsubscribe operation</span></span>](unsubscribe-operation.md)

