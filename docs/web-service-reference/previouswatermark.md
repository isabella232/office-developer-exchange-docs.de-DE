---
title: PreviousWatermark
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PreviousWatermark
api_type:
- schema
ms.assetid: 474f4f7c-47da-47d4-8126-230012172fb5
description: Das PreviousWatermark-Element darstellt, das Wasserzeichen des neuesten Ereignisses, das an den Client für das Abonnement erfolgreich übermittelt wurde.
ms.openlocfilehash: 93c6f90d0866ae13618391b8544ab593fe33922b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830886"
---
# <a name="previouswatermark"></a><span data-ttu-id="82678-103">PreviousWatermark</span><span class="sxs-lookup"><span data-stu-id="82678-103">PreviousWatermark</span></span>

<span data-ttu-id="82678-104">Das **PreviousWatermark** -Element darstellt, das Wasserzeichen des neuesten Ereignisses, das an den Client für das Abonnement erfolgreich übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="82678-104">The **PreviousWatermark** element represents the watermark of the latest event that was successfully communicated to the client for the subscription.</span></span> 
  
```xml
<PreviousWatermark/>
```

 <span data-ttu-id="82678-105">**WatermarkType**</span><span class="sxs-lookup"><span data-stu-id="82678-105">**WatermarkType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="82678-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="82678-106">Attributes and elements</span></span>

<span data-ttu-id="82678-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="82678-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="82678-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="82678-108">Attributes</span></span>

<span data-ttu-id="82678-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="82678-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="82678-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="82678-110">Child elements</span></span>

<span data-ttu-id="82678-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="82678-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="82678-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="82678-112">Parent elements</span></span>

|<span data-ttu-id="82678-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="82678-113">**Element**</span></span>|<span data-ttu-id="82678-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="82678-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="82678-115">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="82678-115">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="82678-116">Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="82678-116">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="82678-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="82678-117">Text value</span></span>

<span data-ttu-id="82678-118">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="82678-118">A text value is required.</span></span> <span data-ttu-id="82678-119">Der Textwert stellt das neuesten Wasserzeichen.</span><span class="sxs-lookup"><span data-stu-id="82678-119">The text value represents the latest watermark.</span></span> <span data-ttu-id="82678-120">Der Textwert darf nicht auf eine leere Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="82678-120">The text value cannot be an empty string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="82678-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="82678-121">Remarks</span></span>

<span data-ttu-id="82678-122">Die **PreviousWatermark** -Eigenschaft ist hilfreich, den Client bei der Bestimmung der letzten erfolgreichen benachrichtigungs.</span><span class="sxs-lookup"><span data-stu-id="82678-122">The **PreviousWatermark** property is useful to the client in determining the last successful notification.</span></span> <span data-ttu-id="82678-123">Beispielsweise kann, wenn ein Abonnement verfügt über drei Ereignisse mit Wasserzeichen 1, 2 und 3, und die nächste Benachrichtigung mit dem Wert **PreviousWatermark** 3 gesendet wird, der Client dieser Wert auf den Wasserzeichen-Wert, der die letzte Benachrichtigung empfangen vergleichen.</span><span class="sxs-lookup"><span data-stu-id="82678-123">For example, if a subscription has three events with watermarks 1, 2, and 3, and the next notification is sent with a **PreviousWatermark** value of 3, the client can compare this value to the Watermark value of the last notification received.</span></span> <span data-ttu-id="82678-124">Dies ermöglicht dem Client um sicherzustellen, dass die Kontinuität von Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="82678-124">This enables the client to ensure the continuity of events.</span></span> 
  
<span data-ttu-id="82678-125">Für Push-Clients wird der **PreviousWatermark** auf das lokale, mithilfe der clientseitigen letzte bekannte Wasserzeichen verglichen.</span><span class="sxs-lookup"><span data-stu-id="82678-125">For push clients, the **PreviousWatermark** is compared to the local, client-side last known watermark.</span></span> <span data-ttu-id="82678-126">Wenn die Werte unterschiedlich sind, wird der Client eine ereignisbenachrichtigung verpasst hat und sollte ein Abonnement mit den neuesten lokalen Wasserzeichen wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="82678-126">If the values are different, the client has missed an event notification and should reestablish a subscription by using the latest local watermark.</span></span> <span data-ttu-id="82678-127">Beispielsweise wenn ein Push-Client drei Ereignisse für ein Abonnement mit Wasserzeichen 1, 2 und 3 empfängt und die nächste Benachrichtigung mit dem Wert **PreviousWatermark** 5 stammen, der Client verpasst hat mindestens eine Benachrichtigung und sollten ein neues Abonnement erstellen, übergeben einen 3 das Wasserzeichen.</span><span class="sxs-lookup"><span data-stu-id="82678-127">For example, if a push client receives three events for a subscription with watermarks 1, 2, and 3, and the next notification comes with a **PreviousWatermark** value of 5, the client has missed at least one notification and should create a new subscription, passing a 3 as the watermark.</span></span> 
  
<span data-ttu-id="82678-128">Bei einem Pull-Client wird der Wert der **PreviousWatermark** der vom Client in den Anruf GetEvents enthalten [Wasserzeichen](watermark.md) identisch sein.</span><span class="sxs-lookup"><span data-stu-id="82678-128">In the case of a pull client, the value of **PreviousWatermark** will be the same as the [Watermark](watermark.md) included by the client in the GetEvents call.</span></span> 
  
<span data-ttu-id="82678-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="82678-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="82678-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="82678-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="82678-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="82678-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="82678-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="82678-132">Schema Name</span></span>  <br/> |<span data-ttu-id="82678-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="82678-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="82678-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="82678-134">Validation File</span></span>  <br/> |<span data-ttu-id="82678-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="82678-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="82678-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="82678-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="82678-137">False</span><span class="sxs-lookup"><span data-stu-id="82678-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="82678-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82678-138">See also</span></span>



[<span data-ttu-id="82678-139">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="82678-139">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="82678-140">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="82678-140">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="82678-141">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="82678-141">Unsubscribe operation</span></span>](unsubscribe-operation.md)

