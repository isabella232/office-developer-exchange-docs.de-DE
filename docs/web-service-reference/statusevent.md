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
description: Das StatusEvent-Element stellt eine Benachrichtigung dar, dass keine neue Aktivität im Postfach aufgetreten ist.
ms.openlocfilehash: 8158a47937a810be2ea22346384b4e61da56ac48
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468257"
---
# <a name="statusevent"></a><span data-ttu-id="bd8b5-103">StatusEvent</span><span class="sxs-lookup"><span data-stu-id="bd8b5-103">StatusEvent</span></span>

<span data-ttu-id="bd8b5-104">Das **StatusEvent** -Element stellt eine Benachrichtigung dar, dass keine neue Aktivität im Postfach aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="bd8b5-104">The **StatusEvent** element represents a notification that no new activity has occurred in the mailbox.</span></span> 
  
```xml
<StatusEvent>
   <Watermark/>
</StatusEvent>
```

 <span data-ttu-id="bd8b5-105">**BaseNotificationEventType**</span><span class="sxs-lookup"><span data-stu-id="bd8b5-105">**BaseNotificationEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bd8b5-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bd8b5-106">Attributes and elements</span></span>

<span data-ttu-id="bd8b5-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bd8b5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bd8b5-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="bd8b5-108">Attributes</span></span>

<span data-ttu-id="bd8b5-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="bd8b5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bd8b5-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bd8b5-110">Child elements</span></span>

|<span data-ttu-id="bd8b5-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="bd8b5-111">**Element**</span></span>|<span data-ttu-id="bd8b5-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bd8b5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bd8b5-113">Watermark</span><span class="sxs-lookup"><span data-stu-id="bd8b5-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="bd8b5-114">Stellt das letzte gültige Wasserzeichen für ein Abonnement dar.</span><span class="sxs-lookup"><span data-stu-id="bd8b5-114">Represents the last valid watermark for a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bd8b5-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bd8b5-115">Parent elements</span></span>

|<span data-ttu-id="bd8b5-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="bd8b5-116">**Element**</span></span>|<span data-ttu-id="bd8b5-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bd8b5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bd8b5-118">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="bd8b5-118">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="bd8b5-119">Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="bd8b5-119">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd8b5-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd8b5-120">Remarks</span></span>

<span data-ttu-id="bd8b5-121">Das **StatusEvent** -Element wird aus einem der folgenden Gründe in einer Benachrichtigung zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="bd8b5-121">The **StatusEvent** element is returned in a notification for one of the following reasons:</span></span> 
  
- <span data-ttu-id="bd8b5-122">Ein Pull-Client gibt eine GetEvents-Anforderung für ein Abonnement aus, das über keine Aktivität verfügt.</span><span class="sxs-lookup"><span data-stu-id="bd8b5-122">A pull client issues a GetEvents request on a subscription that has no activity.</span></span>
    
- <span data-ttu-id="bd8b5-123">Ein Push-Client hat keine Ereignisse in der Warteschlange, wenn die [StatusFrequency](statusfrequency.md) erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="bd8b5-123">A push client has no events in the queue when the [StatusFrequency](statusfrequency.md) has been reached.</span></span> 
    
<span data-ttu-id="bd8b5-124">Das **StatusEvent**-[Wasserzeichen](watermark.md) wird von einer Clientanwendung auf die gleiche Weise wie die anderen Wasserzeichen von Ereignistypen verwendet.</span><span class="sxs-lookup"><span data-stu-id="bd8b5-124">The **StatusEvent**[Watermark](watermark.md) is used by a client application in the same manner as the other event type watermarks.</span></span> <span data-ttu-id="bd8b5-125">Das Wasserzeichen für das **StatusEvent** ist jedoch nicht identisch mit den Wasserzeichen, die für andere Ereignisse verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bd8b5-125">However, the watermark for the **StatusEvent** is not the same as the watermarks used for other events.</span></span> <span data-ttu-id="bd8b5-126">Beispielsweise hat ein Abonnement Ereignisse mit Wasserzeichen 1, 2 und 3, und diese Ereignisse wurden in einer Benachrichtigung erfolgreich kommuniziert.</span><span class="sxs-lookup"><span data-stu-id="bd8b5-126">For example, a subscription has events with watermarks 1, 2, and 3 and those events have been successfully communicated in a notification.</span></span> <span data-ttu-id="bd8b5-127">Ein Zeitraum der Inaktivität tritt auf, und es wird eine **GetEvents** -Anforderung gesendet.</span><span class="sxs-lookup"><span data-stu-id="bd8b5-127">A period of inactivity occurs and a **GetEvents** request is sent.</span></span> <span data-ttu-id="bd8b5-128">Der Client Zugriffsserver (CAS) gibt ein Status Ereignis zurück und enthält das letzte Wasserzeichen, 3, als [PreviousWatermark](previouswatermark.md) und das aktuelle [Wasserzeichen](watermark.md).</span><span class="sxs-lookup"><span data-stu-id="bd8b5-128">The Client Access server (CAS) returns a status event and includes the last watermark, 3, as both the [PreviousWatermark](previouswatermark.md) and the current [Watermark](watermark.md).</span></span>
  
<span data-ttu-id="bd8b5-129">Das Wasserzeichen wird nicht in allen Fällen gleich bleiben.</span><span class="sxs-lookup"><span data-stu-id="bd8b5-129">The watermark will not remain the same in all cases.</span></span> <span data-ttu-id="bd8b5-130">Ereigniseinträge werden für 30 Tage beibehalten.</span><span class="sxs-lookup"><span data-stu-id="bd8b5-130">Event entries are maintained for 30 days.</span></span> <span data-ttu-id="bd8b5-131">Um ein aktives Abonnement beizubehalten, werden die Wasserzeichen für Abonnement Warteschlangen von der Zertifizierungsstellen regelmäßig aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="bd8b5-131">To maintain an active subscription, the CAS periodically updates the watermarks for subscription queues.</span></span> <span data-ttu-id="bd8b5-132">Die aktualisierten Wasserzeichen werden an Clients gesendet, um ein aktives Abonnement beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="bd8b5-132">The updated watermarks are sent to clients to maintain an active subscription.</span></span>
  
<span data-ttu-id="bd8b5-133">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="bd8b5-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bd8b5-134">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="bd8b5-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bd8b5-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="bd8b5-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bd8b5-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bd8b5-136">Schema name</span></span>  <br/> |<span data-ttu-id="bd8b5-137">Schematypen</span><span class="sxs-lookup"><span data-stu-id="bd8b5-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="bd8b5-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bd8b5-138">Validation file</span></span>  <br/> |<span data-ttu-id="bd8b5-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bd8b5-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bd8b5-140">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="bd8b5-140">Can be empty</span></span>  <br/> |<span data-ttu-id="bd8b5-141">False</span><span class="sxs-lookup"><span data-stu-id="bd8b5-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bd8b5-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd8b5-142">See also</span></span>



[<span data-ttu-id="bd8b5-143">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="bd8b5-143">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="bd8b5-144">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="bd8b5-144">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="bd8b5-145">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="bd8b5-145">Unsubscribe operation</span></span>](unsubscribe-operation.md)

