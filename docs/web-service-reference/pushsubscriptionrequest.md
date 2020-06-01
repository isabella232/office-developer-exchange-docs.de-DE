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
description: Das PushSubscriptionRequest-Element stellt ein Abonnement für ein Push-basiertes Ereignis Benachrichtigungsabonnement dar.
ms.openlocfilehash: dcdb767ed175468aa4ec940f3147c164e4707e40
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465513"
---
# <a name="pushsubscriptionrequest"></a><span data-ttu-id="67a89-103">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="67a89-103">PushSubscriptionRequest</span></span>

<span data-ttu-id="67a89-104">Das **PushSubscriptionRequest** -Element stellt ein Abonnement für ein Push-basiertes Ereignis Benachrichtigungsabonnement dar.</span><span class="sxs-lookup"><span data-stu-id="67a89-104">The **PushSubscriptionRequest** element represents a subscription to a push-based event notification subscription.</span></span> 
  
[<span data-ttu-id="67a89-105">Abonnieren</span><span class="sxs-lookup"><span data-stu-id="67a89-105">Subscribe</span></span>](subscribe.md)
  
[<span data-ttu-id="67a89-106">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="67a89-106">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md)
  
```XML
<PushSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
   <Watermark/>
   <StatusFrequency/>
   <URL/>
</PushSubscriptionRequest>
```

 <span data-ttu-id="67a89-107">**PushSubscriptionRequestType**</span><span class="sxs-lookup"><span data-stu-id="67a89-107">**PushSubscriptionRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="67a89-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="67a89-108">Attributes and elements</span></span>

<span data-ttu-id="67a89-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="67a89-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="67a89-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="67a89-110">Attributes</span></span>

|<span data-ttu-id="67a89-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="67a89-111">**Attribute**</span></span>|<span data-ttu-id="67a89-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="67a89-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="67a89-113">**SubscribeToAllFolders**</span><span class="sxs-lookup"><span data-stu-id="67a89-113">**SubscribeToAllFolders**</span></span> <br/> |<span data-ttu-id="67a89-114">Gibt an, ob alle verfügbaren Ordner abonniert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="67a89-114">Indicates whether to subscribe to all available folders.</span></span> <span data-ttu-id="67a89-115">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="67a89-115">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="67a89-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="67a89-116">Child elements</span></span>

|<span data-ttu-id="67a89-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="67a89-117">**Element**</span></span>|<span data-ttu-id="67a89-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="67a89-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="67a89-119">FolderIds</span><span class="sxs-lookup"><span data-stu-id="67a89-119">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="67a89-120">Enthält ein Array von Ordner Bezeichnern, die zum Identifizieren von zu überwachenden Ordnern für Ereignisbenachrichtigungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="67a89-120">Contains an array of folder identifiers that are used to identify folders to monitor for event notifications.</span></span>  <br/> |
|[<span data-ttu-id="67a89-121">EventTypes</span><span class="sxs-lookup"><span data-stu-id="67a89-121">EventTypes</span></span>](eventtypes.md) <br/> |<span data-ttu-id="67a89-122">Enthält eine Auflistung von Ereignisbenachrichtigungen, die zum Erstellen eines Abonnements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="67a89-122">Contains a collection of event notifications that are used to create a subscription.</span></span>  <br/> |
|[<span data-ttu-id="67a89-123">Watermark</span><span class="sxs-lookup"><span data-stu-id="67a89-123">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="67a89-124">Stellt eine Ereignis Textmarke in der Tabelle Post Fach Ereignisse dar.</span><span class="sxs-lookup"><span data-stu-id="67a89-124">Represents an event bookmark in the mailbox events table.</span></span> <span data-ttu-id="67a89-125">Dies wird verwendet, um ein Abonnement zu erstellen, das bei einem durch das Wasserzeichen dargestellten Ereignis beginnt.</span><span class="sxs-lookup"><span data-stu-id="67a89-125">This is used to create a subscription starting at an event represented by the watermark.</span></span> <span data-ttu-id="67a89-126">Wenn das Wasserzeichen aus einer subscribe-Anforderung nicht gefunden wird, wird eine Fehlerantwort an den Client zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="67a89-126">If the watermark from a Subscribe request is not found, an error response will be returned to the client.</span></span> <span data-ttu-id="67a89-127">Dies kann vorkommen, wenn das Wasserzeichen älter als 30 Tage ist oder wenn das Wasserzeichen nie im Postfach vorhanden war.</span><span class="sxs-lookup"><span data-stu-id="67a89-127">This may occur if the watermark is older than 30 days or if the watermark was never present in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="67a89-128">StatusFrequency</span><span class="sxs-lookup"><span data-stu-id="67a89-128">StatusFrequency</span></span>](statusfrequency.md) <br/> |<span data-ttu-id="67a89-129">Stellt die in Minuten angegebene Häufigkeit dar, bei der Benachrichtigungsmeldungen an den Client gesendet werden, wenn keine Ereignisse aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="67a89-129">Represents the frequency, specified in minutes, at which notification messages will be sent to the client when no events have occurred.</span></span>  <br/> |
|[<span data-ttu-id="67a89-130">URL</span><span class="sxs-lookup"><span data-stu-id="67a89-130">Url </span></span>](url-ex15websvcsotherref.md) <br/> |<span data-ttu-id="67a89-131">Stellt den Speicherort des Client-Webdiensts für Push-Benachrichtigungen dar.</span><span class="sxs-lookup"><span data-stu-id="67a89-131">Represents the location of the client Web service for push notifications.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="67a89-132">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="67a89-132">Parent elements</span></span>

|<span data-ttu-id="67a89-133">**Element**</span><span class="sxs-lookup"><span data-stu-id="67a89-133">**Element**</span></span>|<span data-ttu-id="67a89-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="67a89-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="67a89-135">Abonnieren</span><span class="sxs-lookup"><span data-stu-id="67a89-135">Subscribe</span></span>](subscribe.md) <br/> |<span data-ttu-id="67a89-136">Enthält die zum Erstellen von Abonnements verwendeten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="67a89-136">Contains the properties used to create subscriptions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="67a89-137">Textwert</span><span class="sxs-lookup"><span data-stu-id="67a89-137">Text value</span></span>

<span data-ttu-id="67a89-138">Keine.</span><span class="sxs-lookup"><span data-stu-id="67a89-138">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="67a89-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67a89-139">Remarks</span></span>

<span data-ttu-id="67a89-140">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="67a89-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="67a89-141">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="67a89-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67a89-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="67a89-142">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="67a89-143">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="67a89-143">Schema name</span></span>  <br/> |<span data-ttu-id="67a89-144">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="67a89-144">Messages schema</span></span>  <br/> |
|<span data-ttu-id="67a89-145">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="67a89-145">Validation file</span></span>  <br/> |<span data-ttu-id="67a89-146">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="67a89-146">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="67a89-147">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="67a89-147">Can be empty</span></span>  <br/> |<span data-ttu-id="67a89-148">False</span><span class="sxs-lookup"><span data-stu-id="67a89-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="67a89-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67a89-149">See also</span></span>



[<span data-ttu-id="67a89-150">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="67a89-150">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="67a89-151">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="67a89-151">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="67a89-152">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="67a89-152">Unsubscribe operation</span></span>](unsubscribe-operation.md)

