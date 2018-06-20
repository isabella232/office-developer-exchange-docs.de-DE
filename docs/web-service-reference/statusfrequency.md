---
title: StatusFrequency
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StatusFrequency
api_type:
- schema
ms.assetid: 917474e2-a426-4166-b825-53783a41dad4
description: Das StatusFrequency-Element stellt den Timeoutwert maximale in Minuten ein, in denen Wiederholungsversuche vom Server versucht werden.
ms.openlocfilehash: 402f8978c0ec6b377dfa020f23595c8954509a07
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831589"
---
# <a name="statusfrequency"></a><span data-ttu-id="4e34f-103">StatusFrequency</span><span class="sxs-lookup"><span data-stu-id="4e34f-103">StatusFrequency</span></span>

<span data-ttu-id="4e34f-104">Das **StatusFrequency** -Element stellt den Timeoutwert maximale in Minuten ein, in denen Wiederholungsversuche vom Server versucht werden.</span><span class="sxs-lookup"><span data-stu-id="4e34f-104">The **StatusFrequency** element represents the maximum timeout value, in minutes, in which retries are attempted by the server.</span></span> 
  
[<span data-ttu-id="4e34f-105">Abonnieren</span><span class="sxs-lookup"><span data-stu-id="4e34f-105">Subscribe</span></span>](subscribe.md)
  
[<span data-ttu-id="4e34f-106">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="4e34f-106">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md)
  
[<span data-ttu-id="4e34f-107">StatusFrequency</span><span class="sxs-lookup"><span data-stu-id="4e34f-107">StatusFrequency</span></span>](statusfrequency.md)
  
```XML
<StatusFrequency/>
```

 <span data-ttu-id="4e34f-108">**SubscriptionStatusFrequencyType**</span><span class="sxs-lookup"><span data-stu-id="4e34f-108">**SubscriptionStatusFrequencyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4e34f-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4e34f-109">Attributes and elements</span></span>

<span data-ttu-id="4e34f-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4e34f-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4e34f-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="4e34f-111">Attributes</span></span>

<span data-ttu-id="4e34f-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="4e34f-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4e34f-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4e34f-113">Child elements</span></span>

<span data-ttu-id="4e34f-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="4e34f-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4e34f-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4e34f-115">Parent elements</span></span>

|<span data-ttu-id="4e34f-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="4e34f-116">**Element**</span></span>|<span data-ttu-id="4e34f-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4e34f-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4e34f-118">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="4e34f-118">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="4e34f-119">Stellt ein Abonnement für ein Benachrichtigungsabonnement Push-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="4e34f-119">Represents a subscription to a push-based event notification subscription.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4e34f-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="4e34f-120">Text value</span></span>

<span data-ttu-id="4e34f-121">Ein Textwert, der eine ganze Zahl darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4e34f-121">A text value that represents an integer is required if this element is used.</span></span> <span data-ttu-id="4e34f-122">Die möglichen Werte für dieses Element sind 1 bis 1440, inklusive.</span><span class="sxs-lookup"><span data-stu-id="4e34f-122">The possible values for this element are 1 to 1440, inclusive.</span></span> <span data-ttu-id="4e34f-123">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="4e34f-123">This element is optional.</span></span> <span data-ttu-id="4e34f-124">Der Standardwert ist 30 Minuten.</span><span class="sxs-lookup"><span data-stu-id="4e34f-124">The default value is 30 minutes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4e34f-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4e34f-125">Remarks</span></span>

<span data-ttu-id="4e34f-126">Der Wert **StatusFrequency** wird vom Server verwendet, eine Push-Benachrichtigung zu wiederholen, wenn eine Antwort auf eine Push-Benachrichtigung oder Status Ping vom Client nicht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="4e34f-126">The **StatusFrequency** value is used by the server to retry a push notification when it does not receive a response to a push notification or status ping from the client.</span></span> <span data-ttu-id="4e34f-127">Wenn der Server keine Antwort erhalten, versucht er senden die Benachrichtigung mehrmals, bevor es beendet, das die Benachrichtigung gesendet.</span><span class="sxs-lookup"><span data-stu-id="4e34f-127">If the server does not receive a response, it retries sending the notification several times before it stops sending the notification.</span></span> <span data-ttu-id="4e34f-128">In der Exchange-Webdienste das Standard-Wiederholungsintervall beträgt 30 Sekunden und nachfolgende Wiederholungsversuche sind immer double der Zeitpunkt der letzten Wiederholungsintervall.</span><span class="sxs-lookup"><span data-stu-id="4e34f-128">In EWS, the default retry interval is 30 seconds and subsequent retries are always double the time of the last retry interval.</span></span> <span data-ttu-id="4e34f-129">Wie oft wiederholen sind nicht genau, wie sie andere Lasten auf dem Server aufgrund von verzögert werden können.</span><span class="sxs-lookup"><span data-stu-id="4e34f-129">Retry times are not exact as they can be delayed due to other loads on the server.</span></span> <span data-ttu-id="4e34f-130">In der folgenden Tabelle veranschaulicht, wie die Wiederholungsversuchen treten in der 30 Minuten Projektzuordnungstermin vom **StatusFrequency** Standardwert (vorausgesetzt, dass der Server keine Verzögerungen auftreten).</span><span class="sxs-lookup"><span data-stu-id="4e34f-130">The following table shows how the retry intervals occur in the 30 minutes allotted by the default **StatusFrequency** value (assuming the server did not encounter any delays).</span></span> 
  
|<span data-ttu-id="4e34f-131">**Wiederholen**</span><span class="sxs-lookup"><span data-stu-id="4e34f-131">**Retry**</span></span>|<span data-ttu-id="4e34f-132">**Sekunden**</span><span class="sxs-lookup"><span data-stu-id="4e34f-132">**Seconds**</span></span>|<span data-ttu-id="4e34f-133">**Time**</span><span class="sxs-lookup"><span data-stu-id="4e34f-133">**Time**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4e34f-134">0</span><span class="sxs-lookup"><span data-stu-id="4e34f-134">0</span></span>  <br/> |<span data-ttu-id="4e34f-135">0</span><span class="sxs-lookup"><span data-stu-id="4e34f-135">0</span></span>  <br/> |<span data-ttu-id="4e34f-136">Ersten Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="4e34f-136">Initial sync</span></span>  <br/> |
|<span data-ttu-id="4e34f-137">1</span><span class="sxs-lookup"><span data-stu-id="4e34f-137">1</span></span>  <br/> |<span data-ttu-id="4e34f-138">30</span><span class="sxs-lookup"><span data-stu-id="4e34f-138">30</span></span>  <br/> |<span data-ttu-id="4e34f-139">00:30</span><span class="sxs-lookup"><span data-stu-id="4e34f-139">00:30</span></span>  <br/> |
|<span data-ttu-id="4e34f-140">2</span><span class="sxs-lookup"><span data-stu-id="4e34f-140">2</span></span>  <br/> |<span data-ttu-id="4e34f-141">60</span><span class="sxs-lookup"><span data-stu-id="4e34f-141">60</span></span>  <br/> |<span data-ttu-id="4e34f-142">01:00</span><span class="sxs-lookup"><span data-stu-id="4e34f-142">01:00</span></span>  <br/> |
|<span data-ttu-id="4e34f-143">3</span><span class="sxs-lookup"><span data-stu-id="4e34f-143">3</span></span>  <br/> |<span data-ttu-id="4e34f-144">120</span><span class="sxs-lookup"><span data-stu-id="4e34f-144">120</span></span>  <br/> |<span data-ttu-id="4e34f-145">02:00</span><span class="sxs-lookup"><span data-stu-id="4e34f-145">02:00</span></span>  <br/> |
|<span data-ttu-id="4e34f-146">4</span><span class="sxs-lookup"><span data-stu-id="4e34f-146">4</span></span>  <br/> |<span data-ttu-id="4e34f-147">240</span><span class="sxs-lookup"><span data-stu-id="4e34f-147">240</span></span>  <br/> |<span data-ttu-id="4e34f-148">04:00</span><span class="sxs-lookup"><span data-stu-id="4e34f-148">04:00</span></span>  <br/> |
|<span data-ttu-id="4e34f-149">5</span><span class="sxs-lookup"><span data-stu-id="4e34f-149">5</span></span>  <br/> |<span data-ttu-id="4e34f-150">480</span><span class="sxs-lookup"><span data-stu-id="4e34f-150">480</span></span>  <br/> |<span data-ttu-id="4e34f-151">08:00</span><span class="sxs-lookup"><span data-stu-id="4e34f-151">08:00</span></span>  <br/> |
|<span data-ttu-id="4e34f-152">6</span><span class="sxs-lookup"><span data-stu-id="4e34f-152">6</span></span>  <br/> |<span data-ttu-id="4e34f-153">960</span><span class="sxs-lookup"><span data-stu-id="4e34f-153">960</span></span>  <br/> |<span data-ttu-id="4e34f-154">16:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="4e34f-154">16:00</span></span>  <br/> |
|<span data-ttu-id="4e34f-155">7</span><span class="sxs-lookup"><span data-stu-id="4e34f-155">7</span></span>  <br/> |<span data-ttu-id="4e34f-156">1920</span><span class="sxs-lookup"><span data-stu-id="4e34f-156">1920</span></span>  <br/> |<span data-ttu-id="4e34f-157">32:00 - **StatusFrequency** Standardwert 30 überschritten, wiederholen Sie den Vorgang nicht gesendet</span><span class="sxs-lookup"><span data-stu-id="4e34f-157">32:00 - **StatusFrequency** default value of 30 exceeded, retry not sent</span></span>  <br/> |
   
<span data-ttu-id="4e34f-158">Erhält der Client keine Benachrichtigungsnachrichten vom Server für eine bestimmte Zeitspanne, die zweimal die Zeit, die durch **StatusFrequency**angegebenen überschreitet, sollte der Client eine Aktion wie das Abonnement Neuerstellen verwenden.</span><span class="sxs-lookup"><span data-stu-id="4e34f-158">If the client does not receive notification messages from the server for a period of time that exceeds twice the time specified by **StatusFrequency**, the client should take an action such as recreating the subscription.</span></span> 
  
<span data-ttu-id="4e34f-159">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4e34f-159">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4e34f-160">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4e34f-160">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4e34f-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="4e34f-161">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4e34f-162">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4e34f-162">Schema name</span></span>  <br/> |<span data-ttu-id="4e34f-163">Schematypen</span><span class="sxs-lookup"><span data-stu-id="4e34f-163">Types schema</span></span>  <br/> |
|<span data-ttu-id="4e34f-164">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4e34f-164">Validation file</span></span>  <br/> |<span data-ttu-id="4e34f-165">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4e34f-165">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4e34f-166">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="4e34f-166">Can be empty</span></span>  <br/> |<span data-ttu-id="4e34f-167">False</span><span class="sxs-lookup"><span data-stu-id="4e34f-167">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4e34f-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e34f-168">See also</span></span>



[<span data-ttu-id="4e34f-169">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="4e34f-169">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="4e34f-170">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4e34f-170">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="4e34f-171">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="4e34f-171">Unsubscribe operation</span></span>](unsubscribe-operation.md)
  
[<span data-ttu-id="4e34f-172">Wasserzeichen</span><span class="sxs-lookup"><span data-stu-id="4e34f-172">Watermark</span></span>](watermark.md)

