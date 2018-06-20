---
title: PushSubscriptionRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PushSubscriptionRequest
api_type:
- schema
ms.assetid: 70caa0ca-40a1-421f-b4e6-0658f22d0b8e
description: Das PushSubscriptionRequest-Element stellt ein Abonnement für ein Benachrichtigungsabonnement Push-Ereignis.
ms.openlocfilehash: 34717d37b8e5bb50c927e57088299fbcb18a2514
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830929"
---
# <a name="pushsubscriptionrequest"></a><span data-ttu-id="76358-103">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="76358-103">PushSubscriptionRequest</span></span>

<span data-ttu-id="76358-104">Das **PushSubscriptionRequest** -Element stellt ein Abonnement für ein Benachrichtigungsabonnement Push-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="76358-104">The **PushSubscriptionRequest** element represents a subscription to a push-based event notification subscription.</span></span> 
  
[<span data-ttu-id="76358-105">Abonnieren</span><span class="sxs-lookup"><span data-stu-id="76358-105">Subscribe</span></span>](subscribe.md)
  
[<span data-ttu-id="76358-106">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="76358-106">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md)
  
```XML
<PushSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
   <Watermark/>
   <StatusFrequency/>
   <URL/>
</PushSubscriptionRequest>
```

 <span data-ttu-id="76358-107">**PushSubscriptionRequestType**</span><span class="sxs-lookup"><span data-stu-id="76358-107">**PushSubscriptionRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="76358-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="76358-108">Attributes and elements</span></span>

<span data-ttu-id="76358-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="76358-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="76358-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="76358-110">Attributes</span></span>

|<span data-ttu-id="76358-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="76358-111">**Attribute**</span></span>|<span data-ttu-id="76358-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="76358-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="76358-113">**SubscribeToAllFolders**</span><span class="sxs-lookup"><span data-stu-id="76358-113">**SubscribeToAllFolders**</span></span> <br/> |<span data-ttu-id="76358-114">Gibt an, ob, um alle verfügbaren Ordner zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="76358-114">Indicates whether to subscribe to all available folders.</span></span> <span data-ttu-id="76358-115">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="76358-115">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="76358-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="76358-116">Child elements</span></span>

|<span data-ttu-id="76358-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="76358-117">**Element**</span></span>|<span data-ttu-id="76358-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="76358-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="76358-119">FolderIds</span><span class="sxs-lookup"><span data-stu-id="76358-119">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="76358-120">Enthält ein Array von Bezeichnern für Ordner, die zum Identifizieren von Ordnern zum Überwachen von ereignisbenachrichtigungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76358-120">Contains an array of folder identifiers that are used to identify folders to monitor for event notifications.</span></span>  <br/> |
|[<span data-ttu-id="76358-121">EventTypes</span><span class="sxs-lookup"><span data-stu-id="76358-121">EventTypes</span></span>](eventtypes.md) <br/> |<span data-ttu-id="76358-122">Enthält eine Auflistung von ereignisbenachrichtigungen, die zum Erstellen eines Abonnements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76358-122">Contains a collection of event notifications that are used to create a subscription.</span></span>  <br/> |
|[<span data-ttu-id="76358-123">Wasserzeichen</span><span class="sxs-lookup"><span data-stu-id="76358-123">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="76358-124">Stellt eine Textmarke Ereignis in der Tabelle der Postfach-Ereignisse dar.</span><span class="sxs-lookup"><span data-stu-id="76358-124">Represents an event bookmark in the mailbox events table.</span></span> <span data-ttu-id="76358-125">Hiermit wird ein Ereignis, dargestellt durch das Wasserzeichen beginnend-Abonnement zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="76358-125">This is used to create a subscription starting at an event represented by the watermark.</span></span> <span data-ttu-id="76358-126">Wenn das Wasserzeichen aus die Subscribe-Anforderung nicht gefunden wird, wird eine Fehlerantwort an den Client zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="76358-126">If the watermark from a Subscribe request is not found, an error response will be returned to the client.</span></span> <span data-ttu-id="76358-127">Dies kann vorkommen, wenn das Wasserzeichen älter als 30 Tage oder ist wenn das Wasserzeichen nie im Postfach vorhanden war.</span><span class="sxs-lookup"><span data-stu-id="76358-127">This may occur if the watermark is older than 30 days or if the watermark was never present in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="76358-128">StatusFrequency</span><span class="sxs-lookup"><span data-stu-id="76358-128">StatusFrequency</span></span>](statusfrequency.md) <br/> |<span data-ttu-id="76358-129">Stellt die Häufigkeit in Minuten ein, an welche, die Benachrichtigung Nachrichten an den Client gesendet werden, wenn keine Ereignisse eingetreten angegeben.</span><span class="sxs-lookup"><span data-stu-id="76358-129">Represents the frequency, specified in minutes, at which notification messages will be sent to the client when no events have occurred.</span></span>  <br/> |
|[<span data-ttu-id="76358-130">URL</span><span class="sxs-lookup"><span data-stu-id="76358-130">Url </span></span>](url-ex15websvcsotherref.md) <br/> |<span data-ttu-id="76358-131">Stellt den Speicherort des Webdiensts für Pushbenachrichtigungen-Clients.</span><span class="sxs-lookup"><span data-stu-id="76358-131">Represents the location of the client Web service for push notifications.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="76358-132">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="76358-132">Parent elements</span></span>

|<span data-ttu-id="76358-133">**Element**</span><span class="sxs-lookup"><span data-stu-id="76358-133">**Element**</span></span>|<span data-ttu-id="76358-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="76358-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="76358-135">Abonnieren</span><span class="sxs-lookup"><span data-stu-id="76358-135">Subscribe</span></span>](subscribe.md) <br/> |<span data-ttu-id="76358-136">Enthält die Eigenschaften, die zum Erstellen von Abonnements verwendet.</span><span class="sxs-lookup"><span data-stu-id="76358-136">Contains the properties used to create subscriptions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="76358-137">Textwert</span><span class="sxs-lookup"><span data-stu-id="76358-137">Text value</span></span>

<span data-ttu-id="76358-138">Keine.</span><span class="sxs-lookup"><span data-stu-id="76358-138">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="76358-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="76358-139">Remarks</span></span>

<span data-ttu-id="76358-140">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="76358-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="76358-141">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="76358-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="76358-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="76358-142">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="76358-143">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="76358-143">Schema name</span></span>  <br/> |<span data-ttu-id="76358-144">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="76358-144">Messages schema</span></span>  <br/> |
|<span data-ttu-id="76358-145">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="76358-145">Validation file</span></span>  <br/> |<span data-ttu-id="76358-146">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="76358-146">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="76358-147">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="76358-147">Can be empty</span></span>  <br/> |<span data-ttu-id="76358-148">False</span><span class="sxs-lookup"><span data-stu-id="76358-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="76358-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76358-149">See also</span></span>



[<span data-ttu-id="76358-150">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="76358-150">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="76358-151">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="76358-151">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="76358-152">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="76358-152">Unsubscribe operation</span></span>](unsubscribe-operation.md)

