---
title: Watermark
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Watermark
api_type:
- schema
ms.assetid: e1545046-94f9-4ac7-af1c-ea81dfb6822c
description: Das Wasserzeichen-Element stellt eine Ereignis Textmarke in der Post Fach Ereigniswarteschlange dar.
ms.openlocfilehash: a717196101fea698b0b8c66f92a3d420fda9a421
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459763"
---
# <a name="watermark"></a><span data-ttu-id="0b477-103">Watermark</span><span class="sxs-lookup"><span data-stu-id="0b477-103">Watermark</span></span>

<span data-ttu-id="0b477-104">Das **Wasserzeichen** -Element stellt eine Ereignis Textmarke in der Post Fach Ereigniswarteschlange dar.</span><span class="sxs-lookup"><span data-stu-id="0b477-104">The **Watermark** element represents an event bookmark in the mailbox event queue.</span></span> 
  
```xml
<Watermark/>
```

 <span data-ttu-id="0b477-105">**Watermarktype**</span><span class="sxs-lookup"><span data-stu-id="0b477-105">**WatermarkType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0b477-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0b477-106">Attributes and elements</span></span>

<span data-ttu-id="0b477-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0b477-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0b477-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0b477-108">Attributes</span></span>

<span data-ttu-id="0b477-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="0b477-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0b477-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0b477-110">Child elements</span></span>

<span data-ttu-id="0b477-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="0b477-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0b477-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0b477-112">Parent elements</span></span>

|<span data-ttu-id="0b477-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0b477-113">**Element**</span></span>|<span data-ttu-id="0b477-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0b477-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0b477-115">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="0b477-115">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="0b477-116">Stellt ein Abonnement für ein Pull-basiertes Ereignis Benachrichtigungsabonnement dar.</span><span class="sxs-lookup"><span data-stu-id="0b477-116">Represents a subscription to a pull-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="0b477-117">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="0b477-117">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="0b477-118">Stellt ein Abonnement für ein Push-basiertes Ereignis Benachrichtigungsabonnement dar.</span><span class="sxs-lookup"><span data-stu-id="0b477-118">Represents a subscription to a push-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="0b477-119">GetEvents</span><span class="sxs-lookup"><span data-stu-id="0b477-119">GetEvents</span></span>](getevents.md) <br/> |<span data-ttu-id="0b477-120">Stellt den Vorgang dar, der von Pull-Clients zum Anfordern von Benachrichtigungen vom Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0b477-120">Represents the operation used by pull clients to request notifications from the server.</span></span>  <br/> |
|[<span data-ttu-id="0b477-121">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="0b477-121">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="0b477-122">Stellt ein Ereignis dar, in dem ein Element oder ein Ordner kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="0b477-122">Represents an event where an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="0b477-123">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="0b477-123">CreatedEvent</span></span>](createdevent.md) <br/> |<span data-ttu-id="0b477-124">Stellt ein Ereignis dar, in dem ein Element oder ein Ordner erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0b477-124">Represents an event where an item or folder is created.</span></span>  <br/> |
|[<span data-ttu-id="0b477-125">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="0b477-125">DeletedEvent</span></span>](deletedevent.md) <br/> |<span data-ttu-id="0b477-126">Stellt ein Ereignis dar, bei dem ein Element oder ein Ordner gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="0b477-126">Represents an event where an item or folder is deleted.</span></span>  <br/> |
|[<span data-ttu-id="0b477-127">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="0b477-127">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="0b477-128">Stellt ein Ereignis dar, in dem ein Element oder ein Ordner geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0b477-128">Represents an event where an item or folder is modified.</span></span>  <br/> |
|[<span data-ttu-id="0b477-129">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="0b477-129">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="0b477-130">Stellt ein Ereignis dar, bei dem ein Element oder ein Ordner von einem übergeordneten Ordner in einen anderen übergeordneten Ordner verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="0b477-130">Represents an event where an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
|[<span data-ttu-id="0b477-131">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="0b477-131">NewMailEvent</span></span>](newmailevent.md) <br/> |<span data-ttu-id="0b477-132">Stellt ein Ereignis dar, das durch ein neues e-Mail-Element in einem Postfach ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="0b477-132">Represents an event triggered by a new mail item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="0b477-133">StatusEvent</span><span class="sxs-lookup"><span data-stu-id="0b477-133">StatusEvent</span></span>](statusevent.md) <br/> |<span data-ttu-id="0b477-134">Stellt eine Benachrichtigung dar, dass keine neue Aktivität im Postfach aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="0b477-134">Represents a notification that no new activity has occurred in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="0b477-135">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0b477-135">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md) <br/> |<span data-ttu-id="0b477-136">Enthält den Status und das Ergebnis einer subscribe-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="0b477-136">Contains the status and result of a Subscribe request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0b477-137">Textwert</span><span class="sxs-lookup"><span data-stu-id="0b477-137">Text value</span></span>

<span data-ttu-id="0b477-138">Je nachdem, wie dieses Element verwendet wird, ist möglicherweise ein Textwert erforderlich oder optional.</span><span class="sxs-lookup"><span data-stu-id="0b477-138">A text value may be required or optional depending on how this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0b477-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b477-139">Remarks</span></span>

<span data-ttu-id="0b477-140">Wenn eine subscribe-Anforderung ein Wasserzeichen enthält, wird das Abonnement aus dem Wasserzeichen vorwärts erstellt.</span><span class="sxs-lookup"><span data-stu-id="0b477-140">If a Subscribe request contains a watermark, the subscription is created from the watermark forward.</span></span> <span data-ttu-id="0b477-141">Wenn die Subscribe-Anforderung ein Wasserzeichen enthält, das in der Tabelle Post Fach Ereignisse nicht gefunden wird, `ErrorInvalidWatermark` wird ein Fehler an die Clientanwendung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0b477-141">If the Subscribe request contains a watermark that is not found in the mailbox events table, an  `ErrorInvalidWatermark` error is returned to the client application.</span></span> <span data-ttu-id="0b477-142">Dies kann vorkommen, wenn das Wasserzeichen zu alt ist und aus dem 30-Tage-Fenster der Ereignistabelle entfernt wurde oder wenn das Wasserzeichen in der Ereignistabelle nicht immer vorhanden war.</span><span class="sxs-lookup"><span data-stu-id="0b477-142">This may occur if the watermark is too old and has been removed from the 30 day window of the events table or if the watermark was not ever present in the events table.</span></span> <span data-ttu-id="0b477-143">Dies kann beispielsweise der Fall sein, wenn ein Wasserzeichen aus einem anderen Abonnement für ein Postfach in einer anderen Datenbank abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0b477-143">This can happen, for example, if a watermark is obtained from a different subscription for a mailbox in a different database.</span></span> 
  
<span data-ttu-id="0b477-144">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="0b477-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0b477-145">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="0b477-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0b477-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="0b477-146">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0b477-147">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0b477-147">Schema name</span></span>  <br/> |<span data-ttu-id="0b477-148">Schematypen</span><span class="sxs-lookup"><span data-stu-id="0b477-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="0b477-149">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0b477-149">Validation file</span></span>  <br/> |<span data-ttu-id="0b477-150">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0b477-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0b477-151">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="0b477-151">Can be empty</span></span>  <br/> |<span data-ttu-id="0b477-152">False</span><span class="sxs-lookup"><span data-stu-id="0b477-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0b477-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b477-153">See also</span></span>



[<span data-ttu-id="0b477-154">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="0b477-154">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="0b477-155">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0b477-155">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="0b477-156">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="0b477-156">Unsubscribe operation</span></span>](unsubscribe-operation.md)

