---
title: StreamingSubscriptionRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StreamingSubscriptionRequest
api_type:
- schema
ms.assetid: d18f3b60-ebb6-4133-b895-a6ec8942d039
description: Das StreamingSubscriptionRequest-Element stellt ein Abonnement für eine streaming Benachrichtigungsabonnement Ereignis dar.
ms.openlocfilehash: 088ec3b8048d70803b4837548ca918c0005d91bb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831601"
---
# <a name="streamingsubscriptionrequest"></a><span data-ttu-id="c209c-103">StreamingSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="c209c-103">StreamingSubscriptionRequest</span></span>

<span data-ttu-id="c209c-104">Das **StreamingSubscriptionRequest** -Element stellt ein Abonnement für eine streaming Benachrichtigungsabonnement Ereignis dar.</span><span class="sxs-lookup"><span data-stu-id="c209c-104">The **StreamingSubscriptionRequest** element represents a subscription to a streaming event notification subscription.</span></span> 
  
[<span data-ttu-id="c209c-105">Abonnieren</span><span class="sxs-lookup"><span data-stu-id="c209c-105">Subscribe</span></span>](subscribe.md)
  
[<span data-ttu-id="c209c-106">StreamingSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="c209c-106">StreamingSubscriptionRequest</span></span>](streamingsubscriptionrequest.md)
  
```xml
<StreamingSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
</StreamingSubscriptionRequest>
```

 <span data-ttu-id="c209c-107">**StreamingSubscriptionRequest**</span><span class="sxs-lookup"><span data-stu-id="c209c-107">**StreamingSubscriptionRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c209c-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c209c-108">Attributes and elements</span></span>

<span data-ttu-id="c209c-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c209c-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c209c-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="c209c-110">Attributes</span></span>

|<span data-ttu-id="c209c-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c209c-111">**Attribute**</span></span>|<span data-ttu-id="c209c-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c209c-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c209c-113">**SubscribeToAllFolders**</span><span class="sxs-lookup"><span data-stu-id="c209c-113">**SubscribeToAllFolders**</span></span> <br/> |<span data-ttu-id="c209c-114">Gibt an, ob der Server werden alle Ordner im Postfach des Benutzers abonnieren.</span><span class="sxs-lookup"><span data-stu-id="c209c-114">Indicates whether the server will subscribe to all folders in the user's mailbox.</span></span> <span data-ttu-id="c209c-115">Der Wert **true** gibt an, dass der Server abonnieren soll.</span><span class="sxs-lookup"><span data-stu-id="c209c-115">A value of **true** indicates that the server will subscribe.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c209c-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c209c-116">Child elements</span></span>

|<span data-ttu-id="c209c-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="c209c-117">**Element**</span></span>|<span data-ttu-id="c209c-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c209c-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c209c-119">FolderIds</span><span class="sxs-lookup"><span data-stu-id="c209c-119">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="c209c-120">Enthält ein Array von Bezeichnern für Ordner, die zum Identifizieren von Ordnern zum Überwachen von ereignisbenachrichtigungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c209c-120">Contains an array of folder identifiers that are used to identify folders to monitor for event notifications.</span></span>  <br/> |
|[<span data-ttu-id="c209c-121">EventTypes</span><span class="sxs-lookup"><span data-stu-id="c209c-121">EventTypes</span></span>](eventtypes.md) <br/> |<span data-ttu-id="c209c-122">Enthält eine Auflistung von ereignisbenachrichtigungen, die zum Erstellen eines Abonnements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c209c-122">Contains a collection of event notifications that are used to create a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c209c-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c209c-123">Parent elements</span></span>

|<span data-ttu-id="c209c-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="c209c-124">**Element**</span></span>|<span data-ttu-id="c209c-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c209c-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c209c-126">Abonnieren</span><span class="sxs-lookup"><span data-stu-id="c209c-126">Subscribe</span></span>](subscribe.md) <br/> |<span data-ttu-id="c209c-127">Enthält die Eigenschaften, die zum Erstellen von Abonnements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c209c-127">Contains the properties that are used to create subscriptions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c209c-128">Textwert</span><span class="sxs-lookup"><span data-stu-id="c209c-128">Text value</span></span>

<span data-ttu-id="c209c-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="c209c-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c209c-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c209c-130">Remarks</span></span>

<span data-ttu-id="c209c-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c209c-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c209c-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c209c-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c209c-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="c209c-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c209c-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c209c-134">Schema name</span></span>  <br/> |<span data-ttu-id="c209c-135">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="c209c-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c209c-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c209c-136">Validation file</span></span>  <br/> |<span data-ttu-id="c209c-137">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c209c-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c209c-138">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="c209c-138">Can be empty</span></span>  <br/> |<span data-ttu-id="c209c-139">False</span><span class="sxs-lookup"><span data-stu-id="c209c-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c209c-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c209c-140">See also</span></span>



[<span data-ttu-id="c209c-141">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="c209c-141">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="c209c-142">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c209c-142">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="c209c-143">GetStreamingEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c209c-143">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="c209c-144">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="c209c-144">Unsubscribe operation</span></span>](unsubscribe-operation.md)

