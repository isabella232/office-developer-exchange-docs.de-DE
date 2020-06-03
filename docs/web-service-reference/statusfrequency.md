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
description: Das StatusFrequency-Element stellt den maximalen Timeoutwert in Minuten dar, in dem Wiederholungsversuche vom Server versucht werden.
ms.openlocfilehash: db14ecfd54584188b3da16bb369db6c8089c70f4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468243"
---
# <a name="statusfrequency"></a><span data-ttu-id="ef732-103">StatusFrequency</span><span class="sxs-lookup"><span data-stu-id="ef732-103">StatusFrequency</span></span>

<span data-ttu-id="ef732-104">Das **StatusFrequency** -Element stellt den maximalen Timeoutwert in Minuten dar, in dem Wiederholungsversuche vom Server versucht werden.</span><span class="sxs-lookup"><span data-stu-id="ef732-104">The **StatusFrequency** element represents the maximum timeout value, in minutes, in which retries are attempted by the server.</span></span> 
  
[<span data-ttu-id="ef732-105">Abonnieren</span><span class="sxs-lookup"><span data-stu-id="ef732-105">Subscribe</span></span>](subscribe.md)
  
[<span data-ttu-id="ef732-106">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="ef732-106">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md)
  
[<span data-ttu-id="ef732-107">StatusFrequency</span><span class="sxs-lookup"><span data-stu-id="ef732-107">StatusFrequency</span></span>](statusfrequency.md)
  
```XML
<StatusFrequency/>
```

 <span data-ttu-id="ef732-108">**SubscriptionStatusFrequencyType**</span><span class="sxs-lookup"><span data-stu-id="ef732-108">**SubscriptionStatusFrequencyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ef732-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ef732-109">Attributes and elements</span></span>

<span data-ttu-id="ef732-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ef732-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef732-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="ef732-111">Attributes</span></span>

<span data-ttu-id="ef732-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="ef732-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ef732-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ef732-113">Child elements</span></span>

<span data-ttu-id="ef732-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="ef732-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ef732-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ef732-115">Parent elements</span></span>

|<span data-ttu-id="ef732-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="ef732-116">**Element**</span></span>|<span data-ttu-id="ef732-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ef732-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ef732-118">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="ef732-118">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="ef732-119">Stellt ein Abonnement für ein Push-basiertes Ereignis Benachrichtigungsabonnement dar.</span><span class="sxs-lookup"><span data-stu-id="ef732-119">Represents a subscription to a push-based event notification subscription.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ef732-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="ef732-120">Text value</span></span>

<span data-ttu-id="ef732-121">Ein Textwert, der eine ganze Zahl darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ef732-121">A text value that represents an integer is required if this element is used.</span></span> <span data-ttu-id="ef732-122">Die möglichen Werte für dieses Element sind 1 bis 1440, einschließlich.</span><span class="sxs-lookup"><span data-stu-id="ef732-122">The possible values for this element are 1 to 1440, inclusive.</span></span> <span data-ttu-id="ef732-123">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="ef732-123">This element is optional.</span></span> <span data-ttu-id="ef732-124">Der Standardwert beträgt 30 Minuten.</span><span class="sxs-lookup"><span data-stu-id="ef732-124">The default value is 30 minutes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ef732-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef732-125">Remarks</span></span>

<span data-ttu-id="ef732-126">Der **StatusFrequency** -Wert wird vom Server verwendet, um eine Push-Benachrichtigung zu wiederholen, wenn keine Antwort auf eine Push-Benachrichtigung oder einen Status-Ping vom Client empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="ef732-126">The **StatusFrequency** value is used by the server to retry a push notification when it does not receive a response to a push notification or status ping from the client.</span></span> <span data-ttu-id="ef732-127">Wenn der Server keine Antwort erhält, wird erneut versucht, die Benachrichtigung mehrmals zu senden, bevor das Senden der Benachrichtigung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="ef732-127">If the server does not receive a response, it retries sending the notification several times before it stops sending the notification.</span></span> <span data-ttu-id="ef732-128">In EWS beträgt das Standardintervall für Wiederholungen 30 Sekunden, und nachfolgende Wiederholungsversuche sind immer doppelt so lang wie beim letzten Wiederholungsintervall.</span><span class="sxs-lookup"><span data-stu-id="ef732-128">In EWS, the default retry interval is 30 seconds and subsequent retries are always double the time of the last retry interval.</span></span> <span data-ttu-id="ef732-129">Wiederholungszeiten sind nicht exakt, da Sie aufgrund anderer Lasten auf dem Server verzögert werden können.</span><span class="sxs-lookup"><span data-stu-id="ef732-129">Retry times are not exact as they can be delayed due to other loads on the server.</span></span> <span data-ttu-id="ef732-130">In der folgenden Tabelle wird gezeigt, wie die Wiederholungsintervalle in den 30 Minuten auftreten, die dem Standardwert **StatusFrequency** zugewiesen wurden (vorausgesetzt, der Server hat keine Verzögerungen auftreten).</span><span class="sxs-lookup"><span data-stu-id="ef732-130">The following table shows how the retry intervals occur in the 30 minutes allotted by the default **StatusFrequency** value (assuming the server did not encounter any delays).</span></span> 
  
|<span data-ttu-id="ef732-131">**Wiederholen**</span><span class="sxs-lookup"><span data-stu-id="ef732-131">**Retry**</span></span>|<span data-ttu-id="ef732-132">**Sekunden**</span><span class="sxs-lookup"><span data-stu-id="ef732-132">**Seconds**</span></span>|<span data-ttu-id="ef732-133">**Time**</span><span class="sxs-lookup"><span data-stu-id="ef732-133">**Time**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ef732-134">0</span><span class="sxs-lookup"><span data-stu-id="ef732-134">0</span></span>  <br/> |<span data-ttu-id="ef732-135">0</span><span class="sxs-lookup"><span data-stu-id="ef732-135">0</span></span>  <br/> |<span data-ttu-id="ef732-136">Erstsynchronisierung</span><span class="sxs-lookup"><span data-stu-id="ef732-136">Initial sync</span></span>  <br/> |
|<span data-ttu-id="ef732-137">1 </span><span class="sxs-lookup"><span data-stu-id="ef732-137">1</span></span>  <br/> |<span data-ttu-id="ef732-138">30</span><span class="sxs-lookup"><span data-stu-id="ef732-138">30</span></span>  <br/> |<span data-ttu-id="ef732-139">00:30</span><span class="sxs-lookup"><span data-stu-id="ef732-139">00:30</span></span>  <br/> |
|<span data-ttu-id="ef732-140">2</span><span class="sxs-lookup"><span data-stu-id="ef732-140">2</span></span>  <br/> |<span data-ttu-id="ef732-141">60</span><span class="sxs-lookup"><span data-stu-id="ef732-141">60</span></span>  <br/> |<span data-ttu-id="ef732-142">01:00</span><span class="sxs-lookup"><span data-stu-id="ef732-142">01:00</span></span>  <br/> |
|<span data-ttu-id="ef732-143">3</span><span class="sxs-lookup"><span data-stu-id="ef732-143">3</span></span>  <br/> |<span data-ttu-id="ef732-144">120</span><span class="sxs-lookup"><span data-stu-id="ef732-144">120</span></span>  <br/> |<span data-ttu-id="ef732-145">02:00</span><span class="sxs-lookup"><span data-stu-id="ef732-145">02:00</span></span>  <br/> |
|<span data-ttu-id="ef732-146">4 </span><span class="sxs-lookup"><span data-stu-id="ef732-146">4</span></span>  <br/> |<span data-ttu-id="ef732-147">240</span><span class="sxs-lookup"><span data-stu-id="ef732-147">240</span></span>  <br/> |<span data-ttu-id="ef732-148">04:00</span><span class="sxs-lookup"><span data-stu-id="ef732-148">04:00</span></span>  <br/> |
|<span data-ttu-id="ef732-149">5 </span><span class="sxs-lookup"><span data-stu-id="ef732-149">5</span></span>  <br/> |<span data-ttu-id="ef732-150">480</span><span class="sxs-lookup"><span data-stu-id="ef732-150">480</span></span>  <br/> |<span data-ttu-id="ef732-151">08:00</span><span class="sxs-lookup"><span data-stu-id="ef732-151">08:00</span></span>  <br/> |
|<span data-ttu-id="ef732-152">6 </span><span class="sxs-lookup"><span data-stu-id="ef732-152">6</span></span>  <br/> |<span data-ttu-id="ef732-153">960</span><span class="sxs-lookup"><span data-stu-id="ef732-153">960</span></span>  <br/> |<span data-ttu-id="ef732-154">16:00</span><span class="sxs-lookup"><span data-stu-id="ef732-154">16:00</span></span>  <br/> |
|<span data-ttu-id="ef732-155">7 </span><span class="sxs-lookup"><span data-stu-id="ef732-155">7</span></span>  <br/> |<span data-ttu-id="ef732-156">1920</span><span class="sxs-lookup"><span data-stu-id="ef732-156">1920</span></span>  <br/> |<span data-ttu-id="ef732-157">32:00- **StatusFrequency** Standardwert 30 überschritten, wiederholen nicht gesendet</span><span class="sxs-lookup"><span data-stu-id="ef732-157">32:00 - **StatusFrequency** default value of 30 exceeded, retry not sent</span></span>  <br/> |
   
<span data-ttu-id="ef732-158">Wenn der Client für einen Zeitraum, der das Doppelte der durch **StatusFrequency**angegebenen Zeitspanne überschreitet, keine Benachrichtigungen vom Server erhält, sollte der Client eine Aktion wie das erneute Erstellen des Abonnements durchführen.</span><span class="sxs-lookup"><span data-stu-id="ef732-158">If the client does not receive notification messages from the server for a period of time that exceeds twice the time specified by **StatusFrequency**, the client should take an action such as recreating the subscription.</span></span> 
  
<span data-ttu-id="ef732-159">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ef732-159">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef732-160">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ef732-160">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef732-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="ef732-161">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ef732-162">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ef732-162">Schema name</span></span>  <br/> |<span data-ttu-id="ef732-163">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ef732-163">Types schema</span></span>  <br/> |
|<span data-ttu-id="ef732-164">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ef732-164">Validation file</span></span>  <br/> |<span data-ttu-id="ef732-165">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ef732-165">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ef732-166">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ef732-166">Can be empty</span></span>  <br/> |<span data-ttu-id="ef732-167">False</span><span class="sxs-lookup"><span data-stu-id="ef732-167">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ef732-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef732-168">See also</span></span>



[<span data-ttu-id="ef732-169">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="ef732-169">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="ef732-170">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ef732-170">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="ef732-171">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="ef732-171">Unsubscribe operation</span></span>](unsubscribe-operation.md)
  
[<span data-ttu-id="ef732-172">Watermark</span><span class="sxs-lookup"><span data-stu-id="ef732-172">Watermark</span></span>](watermark.md)

