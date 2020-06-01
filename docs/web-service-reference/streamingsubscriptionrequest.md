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
description: Das StreamingSubscriptionRequest-Element stellt ein Abonnement für ein Streaming-Ereignis Benachrichtigungsabonnement dar.
ms.openlocfilehash: b469ba7598420189c1db0e2fe676a279390eb6bf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468229"
---
# <a name="streamingsubscriptionrequest"></a><span data-ttu-id="0939a-103">StreamingSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="0939a-103">StreamingSubscriptionRequest</span></span>

<span data-ttu-id="0939a-104">Das **StreamingSubscriptionRequest** -Element stellt ein Abonnement für ein Streaming-Ereignis Benachrichtigungsabonnement dar.</span><span class="sxs-lookup"><span data-stu-id="0939a-104">The **StreamingSubscriptionRequest** element represents a subscription to a streaming event notification subscription.</span></span> 
  
[<span data-ttu-id="0939a-105">Abonnieren</span><span class="sxs-lookup"><span data-stu-id="0939a-105">Subscribe</span></span>](subscribe.md)
  
[<span data-ttu-id="0939a-106">StreamingSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="0939a-106">StreamingSubscriptionRequest</span></span>](streamingsubscriptionrequest.md)
  
```xml
<StreamingSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
</StreamingSubscriptionRequest>
```

 <span data-ttu-id="0939a-107">**StreamingSubscriptionRequest**</span><span class="sxs-lookup"><span data-stu-id="0939a-107">**StreamingSubscriptionRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0939a-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0939a-108">Attributes and elements</span></span>

<span data-ttu-id="0939a-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0939a-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0939a-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="0939a-110">Attributes</span></span>

|<span data-ttu-id="0939a-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0939a-111">**Attribute**</span></span>|<span data-ttu-id="0939a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0939a-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0939a-113">**SubscribeToAllFolders**</span><span class="sxs-lookup"><span data-stu-id="0939a-113">**SubscribeToAllFolders**</span></span> <br/> |<span data-ttu-id="0939a-114">Gibt an, ob der Server für alle Ordner im Postfach des Benutzers abonniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0939a-114">Indicates whether the server will subscribe to all folders in the user's mailbox.</span></span> <span data-ttu-id="0939a-115">Der Wert **true** gibt an, dass der Server abonniert wird.</span><span class="sxs-lookup"><span data-stu-id="0939a-115">A value of **true** indicates that the server will subscribe.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0939a-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0939a-116">Child elements</span></span>

|<span data-ttu-id="0939a-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="0939a-117">**Element**</span></span>|<span data-ttu-id="0939a-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0939a-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0939a-119">FolderIds</span><span class="sxs-lookup"><span data-stu-id="0939a-119">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="0939a-120">Enthält ein Array von Ordner Bezeichnern, die zum Identifizieren von zu überwachenden Ordnern für Ereignisbenachrichtigungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0939a-120">Contains an array of folder identifiers that are used to identify folders to monitor for event notifications.</span></span>  <br/> |
|[<span data-ttu-id="0939a-121">EventTypes</span><span class="sxs-lookup"><span data-stu-id="0939a-121">EventTypes</span></span>](eventtypes.md) <br/> |<span data-ttu-id="0939a-122">Enthält eine Auflistung von Ereignisbenachrichtigungen, die zum Erstellen eines Abonnements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0939a-122">Contains a collection of event notifications that are used to create a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0939a-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0939a-123">Parent elements</span></span>

|<span data-ttu-id="0939a-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="0939a-124">**Element**</span></span>|<span data-ttu-id="0939a-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0939a-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0939a-126">Abonnieren</span><span class="sxs-lookup"><span data-stu-id="0939a-126">Subscribe</span></span>](subscribe.md) <br/> |<span data-ttu-id="0939a-127">Enthält die Eigenschaften, die zum Erstellen von Abonnements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0939a-127">Contains the properties that are used to create subscriptions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0939a-128">Textwert</span><span class="sxs-lookup"><span data-stu-id="0939a-128">Text value</span></span>

<span data-ttu-id="0939a-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="0939a-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0939a-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0939a-130">Remarks</span></span>

<span data-ttu-id="0939a-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0939a-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0939a-132">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="0939a-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0939a-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="0939a-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0939a-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0939a-134">Schema name</span></span>  <br/> |<span data-ttu-id="0939a-135">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="0939a-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0939a-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0939a-136">Validation file</span></span>  <br/> |<span data-ttu-id="0939a-137">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="0939a-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0939a-138">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="0939a-138">Can be empty</span></span>  <br/> |<span data-ttu-id="0939a-139">False</span><span class="sxs-lookup"><span data-stu-id="0939a-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0939a-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0939a-140">See also</span></span>



[<span data-ttu-id="0939a-141">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="0939a-141">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="0939a-142">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0939a-142">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="0939a-143">GetStreamingEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0939a-143">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="0939a-144">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="0939a-144">Unsubscribe operation</span></span>](unsubscribe-operation.md)

