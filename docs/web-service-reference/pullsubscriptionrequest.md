---
title: PullSubscriptionRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PullSubscriptionRequest
api_type:
- schema
ms.assetid: 145c5cc7-a894-4f0b-a6ea-358cddfb5c33
description: Das PullSubscriptionRequest-Element stellt ein Abonnement für ein Benachrichtigungsabonnement Pull-Ereignis.
ms.openlocfilehash: 5f757bf1f79f7e2a00fb886db50e6ea0eaed1a4a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830932"
---
# <a name="pullsubscriptionrequest"></a><span data-ttu-id="f07ed-103">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="f07ed-103">PullSubscriptionRequest</span></span>

<span data-ttu-id="f07ed-104">Das **PullSubscriptionRequest** -Element stellt ein Abonnement für ein Benachrichtigungsabonnement Pull-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f07ed-104">The **PullSubscriptionRequest** element represents a subscription to a pull-based event notification subscription.</span></span> 
  
[<span data-ttu-id="f07ed-105">Abonnieren</span><span class="sxs-lookup"><span data-stu-id="f07ed-105">Subscribe</span></span>](subscribe.md)
  
[<span data-ttu-id="f07ed-106">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="f07ed-106">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md)
  
```XML
<PullSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
   <Watermark/>
   <Timeout/>
</PullSubscriptionRequest>
```

 <span data-ttu-id="f07ed-107">**PullSubscriptionRequestType**</span><span class="sxs-lookup"><span data-stu-id="f07ed-107">**PullSubscriptionRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f07ed-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f07ed-108">Attributes and elements</span></span>

<span data-ttu-id="f07ed-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f07ed-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f07ed-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="f07ed-110">Attributes</span></span>

|<span data-ttu-id="f07ed-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f07ed-111">**Attribute**</span></span>|<span data-ttu-id="f07ed-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f07ed-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f07ed-113">**SubscribeToAllFolders**</span><span class="sxs-lookup"><span data-stu-id="f07ed-113">**SubscribeToAllFolders**</span></span> <br/> |<span data-ttu-id="f07ed-114">Gibt an, ob, um alle verfügbaren Ordner zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="f07ed-114">Indicates whether to subscribe to all available folders.</span></span> <span data-ttu-id="f07ed-115">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="f07ed-115">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f07ed-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f07ed-116">Child elements</span></span>

|<span data-ttu-id="f07ed-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="f07ed-117">**Element**</span></span>|<span data-ttu-id="f07ed-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f07ed-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f07ed-119">FolderIds</span><span class="sxs-lookup"><span data-stu-id="f07ed-119">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="f07ed-120">Enthält ein Array von Bezeichnern für Ordner, die zum Identifizieren von Ordnern zum Überwachen von ereignisbenachrichtigungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f07ed-120">Contains an array of folder identifiers that are used to identify folders to monitor for event notifications.</span></span>  <br/> |
|[<span data-ttu-id="f07ed-121">EventTypes</span><span class="sxs-lookup"><span data-stu-id="f07ed-121">EventTypes</span></span>](eventtypes.md) <br/> |<span data-ttu-id="f07ed-122">Enthält eine Auflistung von ereignisbenachrichtigungen, die zum Erstellen eines Abonnements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f07ed-122">Contains a collection of event notifications that are used to create a subscription.</span></span>  <br/> |
|[<span data-ttu-id="f07ed-123">Wasserzeichen</span><span class="sxs-lookup"><span data-stu-id="f07ed-123">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="f07ed-124">Stellt eine Textmarke Ereignis in der Tabelle der Postfach-Ereignisse dar.</span><span class="sxs-lookup"><span data-stu-id="f07ed-124">Represents an event bookmark in the mailbox events table.</span></span> <span data-ttu-id="f07ed-125">Hiermit wird ein Abonnement, die beginnt am ein Ereignis zu erstellen, die durch das Wasserzeichen dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f07ed-125">This is used to create a subscription that starts at an event that is represented by the watermark.</span></span> <span data-ttu-id="f07ed-126">Wenn das Wasserzeichen aus die Subscribe-Anforderung nicht gefunden wird, wird eine Fehlerantwort an den Client zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="f07ed-126">If the watermark from a Subscribe request is not found, an error response will be returned to the client.</span></span> <span data-ttu-id="f07ed-127">Dieser Fehler kann auftreten, wenn das Wasserzeichen älter als 30 Tage oder ist wenn das Wasserzeichen nie im Postfach vorhanden war.</span><span class="sxs-lookup"><span data-stu-id="f07ed-127">This error may occur if the watermark is older than 30 days or if the watermark was never present in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="f07ed-128">Timeout</span><span class="sxs-lookup"><span data-stu-id="f07ed-128">Timeout</span></span>](timeout.md) <br/> |<span data-ttu-id="f07ed-129">Stellt die Dauer in Minuten, die das Abonnement ohne GetEvents Anforderung vom Client im Leerlauf sein kann.</span><span class="sxs-lookup"><span data-stu-id="f07ed-129">Represents the duration, in minutes, that the subscription can remain idle without a GetEvents request from the client.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f07ed-130">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f07ed-130">Parent elements</span></span>

|<span data-ttu-id="f07ed-131">**Element**</span><span class="sxs-lookup"><span data-stu-id="f07ed-131">**Element**</span></span>|<span data-ttu-id="f07ed-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f07ed-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f07ed-133">Abonnieren</span><span class="sxs-lookup"><span data-stu-id="f07ed-133">Subscribe</span></span>](subscribe.md) <br/> |<span data-ttu-id="f07ed-134">Enthält die Eigenschaften, die zum Erstellen von Abonnements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f07ed-134">Contains the properties that are used to create subscriptions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f07ed-135">Textwert</span><span class="sxs-lookup"><span data-stu-id="f07ed-135">Text value</span></span>

<span data-ttu-id="f07ed-136">Keine.</span><span class="sxs-lookup"><span data-stu-id="f07ed-136">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f07ed-137">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f07ed-137">Remarks</span></span>

<span data-ttu-id="f07ed-138">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f07ed-138">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f07ed-139">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f07ed-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f07ed-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="f07ed-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f07ed-141">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f07ed-141">Schema name</span></span>  <br/> |<span data-ttu-id="f07ed-142">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="f07ed-142">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f07ed-143">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f07ed-143">Validation file</span></span>  <br/> |<span data-ttu-id="f07ed-144">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f07ed-144">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f07ed-145">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f07ed-145">Can be empty</span></span>  <br/> |<span data-ttu-id="f07ed-146">False</span><span class="sxs-lookup"><span data-stu-id="f07ed-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f07ed-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f07ed-147">See also</span></span>



[<span data-ttu-id="f07ed-148">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="f07ed-148">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md)
  
[<span data-ttu-id="f07ed-149">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="f07ed-149">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="f07ed-150">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f07ed-150">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="f07ed-151">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="f07ed-151">Unsubscribe operation</span></span>](unsubscribe-operation.md)


- [<span data-ttu-id="f07ed-152">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f07ed-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

