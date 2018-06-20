---
title: Wasserzeichen
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
description: Das Wasserzeichen-Element stellt ein Lesezeichen Ereignis in der Ereigniswarteschlange Postfach.
ms.openlocfilehash: 1867aa781bc24f5eb3bdb4648fa494a2a7ea396a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839511"
---
# <a name="watermark"></a><span data-ttu-id="a9c65-103">Wasserzeichen</span><span class="sxs-lookup"><span data-stu-id="a9c65-103">Watermark</span></span>

<span data-ttu-id="a9c65-104">Das **Wasserzeichen** -Element stellt ein Lesezeichen Ereignis in der Ereigniswarteschlange Postfach.</span><span class="sxs-lookup"><span data-stu-id="a9c65-104">The **Watermark** element represents an event bookmark in the mailbox event queue.</span></span> 
  
```xml
<Watermark/>
```

 <span data-ttu-id="a9c65-105">**WatermarkType**</span><span class="sxs-lookup"><span data-stu-id="a9c65-105">**WatermarkType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a9c65-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a9c65-106">Attributes and elements</span></span>

<span data-ttu-id="a9c65-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a9c65-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a9c65-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a9c65-108">Attributes</span></span>

<span data-ttu-id="a9c65-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a9c65-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a9c65-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a9c65-110">Child elements</span></span>

<span data-ttu-id="a9c65-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="a9c65-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a9c65-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a9c65-112">Parent elements</span></span>

|<span data-ttu-id="a9c65-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a9c65-113">**Element**</span></span>|<span data-ttu-id="a9c65-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a9c65-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9c65-115">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="a9c65-115">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="a9c65-116">Stellt ein Abonnement für ein Benachrichtigungsabonnement Pull-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a9c65-116">Represents a subscription to a pull-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="a9c65-117">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="a9c65-117">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="a9c65-118">Stellt ein Abonnement für ein Benachrichtigungsabonnement Push-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a9c65-118">Represents a subscription to a push-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="a9c65-119">GetEvents</span><span class="sxs-lookup"><span data-stu-id="a9c65-119">GetEvents</span></span>](getevents.md) <br/> |<span data-ttu-id="a9c65-120">Stellt die Operation auf Anforderung-Benachrichtigungen vom Server von Pull-Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a9c65-120">Represents the operation used by pull clients to request notifications from the server.</span></span>  <br/> |
|[<span data-ttu-id="a9c65-121">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="a9c65-121">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="a9c65-122">Stellt ein Ereignis eines Elements oder Ordners, in dem kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="a9c65-122">Represents an event where an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="a9c65-123">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="a9c65-123">CreatedEvent</span></span>](createdevent.md) <br/> |<span data-ttu-id="a9c65-124">Stellt ein Ereignis eines Elements oder Ordners, in dem erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a9c65-124">Represents an event where an item or folder is created.</span></span>  <br/> |
|[<span data-ttu-id="a9c65-125">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="a9c65-125">DeletedEvent</span></span>](deletedevent.md) <br/> |<span data-ttu-id="a9c65-126">Stellt ein Ereignis, bei denen eines Elements oder Ordners gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="a9c65-126">Represents an event where an item or folder is deleted.</span></span>  <br/> |
|[<span data-ttu-id="a9c65-127">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="a9c65-127">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="a9c65-128">Stellt ein Ereignis, bei denen eines Elements oder Ordners geändert wird.</span><span class="sxs-lookup"><span data-stu-id="a9c65-128">Represents an event where an item or folder is modified.</span></span>  <br/> |
|[<span data-ttu-id="a9c65-129">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="a9c65-129">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="a9c65-130">Stellt ein Ereignis, auf dem eines Elements oder Ordners aus einem übergeordneten Ordner in einen anderen übergeordneten Ordner verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="a9c65-130">Represents an event where an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
|[<span data-ttu-id="a9c65-131">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="a9c65-131">NewMailEvent</span></span>](newmailevent.md) <br/> |<span data-ttu-id="a9c65-132">Stellt ein Ereignis ausgelöst, indem eine neue e-Mail-Element in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="a9c65-132">Represents an event triggered by a new mail item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a9c65-133">StatusEvent</span><span class="sxs-lookup"><span data-stu-id="a9c65-133">StatusEvent</span></span>](statusevent.md) <br/> |<span data-ttu-id="a9c65-134">Stellt eine Benachrichtigung, dass keine neue Aktivität im Postfach aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="a9c65-134">Represents a notification that no new activity has occurred in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a9c65-135">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a9c65-135">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md) <br/> |<span data-ttu-id="a9c65-136">Enthält den Status und das Ergebnis einer Subscribe-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a9c65-136">Contains the status and result of a Subscribe request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a9c65-137">Textwert</span><span class="sxs-lookup"><span data-stu-id="a9c65-137">Text value</span></span>

<span data-ttu-id="a9c65-138">Ein Textwert möglicherweise erforderlich oder optional je nach dieses Elements Verwendung.</span><span class="sxs-lookup"><span data-stu-id="a9c65-138">A text value may be required or optional depending on how this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a9c65-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a9c65-139">Remarks</span></span>

<span data-ttu-id="a9c65-140">Wenn die Subscribe-Anforderung ein Wasserzeichen enthält, wird das Abonnement aus der Wasserzeichen vorwärts erstellt.</span><span class="sxs-lookup"><span data-stu-id="a9c65-140">If a Subscribe request contains a watermark, the subscription is created from the watermark forward.</span></span> <span data-ttu-id="a9c65-141">Wenn die Subscribe-Anforderung ein Wasserzeichen enthält, die in der Tabelle Ereignisse Postfach nicht gefunden werden kann ein `ErrorInvalidWatermark` Fehler an die Clientanwendung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a9c65-141">If the Subscribe request contains a watermark that is not found in the mailbox events table, an  `ErrorInvalidWatermark` error is returned to the client application.</span></span> <span data-ttu-id="a9c65-142">Dies kann auftreten, wenn das Wasserzeichen veraltet ist und wurde aus der Ereignistabelle das 30-Tage-Fenster entfernt oder wenn das Wasserzeichen jemals nicht wurde in der Ereignistabelle.</span><span class="sxs-lookup"><span data-stu-id="a9c65-142">This may occur if the watermark is too old and has been removed from the 30 day window of the events table or if the watermark was not ever present in the events table.</span></span> <span data-ttu-id="a9c65-143">Dies kann beispielsweise auftreten, wenn ein Wasserzeichen aus ein anderes Abonnement für ein Postfach in einer anderen Datenbank abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a9c65-143">This can happen, for example, if a watermark is obtained from a different subscription for a mailbox in a different database.</span></span> 
  
<span data-ttu-id="a9c65-144">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="a9c65-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a9c65-145">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a9c65-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a9c65-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="a9c65-146">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a9c65-147">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a9c65-147">Schema name</span></span>  <br/> |<span data-ttu-id="a9c65-148">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a9c65-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="a9c65-149">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a9c65-149">Validation file</span></span>  <br/> |<span data-ttu-id="a9c65-150">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a9c65-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a9c65-151">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a9c65-151">Can be empty</span></span>  <br/> |<span data-ttu-id="a9c65-152">False</span><span class="sxs-lookup"><span data-stu-id="a9c65-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a9c65-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9c65-153">See also</span></span>



[<span data-ttu-id="a9c65-154">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="a9c65-154">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="a9c65-155">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a9c65-155">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="a9c65-156">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="a9c65-156">Unsubscribe operation</span></span>](unsubscribe-operation.md)

