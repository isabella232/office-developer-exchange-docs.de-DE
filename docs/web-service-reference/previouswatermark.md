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
description: Das PreviousWatermark-Element stellt das Wasserzeichen des letzten Ereignisses dar, das erfolgreich an den Client für das Abonnement kommuniziert wurde.
ms.openlocfilehash: 1b26a645a5ec6dbbd2874b118f968866aadc32af
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461653"
---
# <a name="previouswatermark"></a><span data-ttu-id="50a9b-103">PreviousWatermark</span><span class="sxs-lookup"><span data-stu-id="50a9b-103">PreviousWatermark</span></span>

<span data-ttu-id="50a9b-104">Das **PreviousWatermark** -Element stellt das Wasserzeichen des letzten Ereignisses dar, das erfolgreich an den Client für das Abonnement kommuniziert wurde.</span><span class="sxs-lookup"><span data-stu-id="50a9b-104">The **PreviousWatermark** element represents the watermark of the latest event that was successfully communicated to the client for the subscription.</span></span> 
  
```xml
<PreviousWatermark/>
```

 <span data-ttu-id="50a9b-105">**Watermarktype**</span><span class="sxs-lookup"><span data-stu-id="50a9b-105">**WatermarkType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="50a9b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="50a9b-106">Attributes and elements</span></span>

<span data-ttu-id="50a9b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="50a9b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="50a9b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="50a9b-108">Attributes</span></span>

<span data-ttu-id="50a9b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="50a9b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="50a9b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="50a9b-110">Child elements</span></span>

<span data-ttu-id="50a9b-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="50a9b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="50a9b-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="50a9b-112">Parent elements</span></span>

|<span data-ttu-id="50a9b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="50a9b-113">**Element**</span></span>|<span data-ttu-id="50a9b-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="50a9b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="50a9b-115">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="50a9b-115">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="50a9b-116">Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="50a9b-116">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="50a9b-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="50a9b-117">Text value</span></span>

<span data-ttu-id="50a9b-118">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="50a9b-118">A text value is required.</span></span> <span data-ttu-id="50a9b-119">Der Wert Text stellt das neueste Wasserzeichen dar.</span><span class="sxs-lookup"><span data-stu-id="50a9b-119">The text value represents the latest watermark.</span></span> <span data-ttu-id="50a9b-120">Der Textwert darf keine leere Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="50a9b-120">The text value cannot be an empty string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="50a9b-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50a9b-121">Remarks</span></span>

<span data-ttu-id="50a9b-122">Die **PreviousWatermark** -Eigenschaft ist hilfreich für den Client beim Bestimmen der letzten erfolgreichen Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="50a9b-122">The **PreviousWatermark** property is useful to the client in determining the last successful notification.</span></span> <span data-ttu-id="50a9b-123">Wenn ein Abonnement beispielsweise drei Ereignisse mit Wasserzeichen 1, 2 und 3 aufweist und die nächste Benachrichtigung mit dem **PreviousWatermark** -Wert 3 gesendet wird, kann der Client diesen Wert mit dem Wasserzeichen Wert der letzten empfangenen Benachrichtigung vergleichen.</span><span class="sxs-lookup"><span data-stu-id="50a9b-123">For example, if a subscription has three events with watermarks 1, 2, and 3, and the next notification is sent with a **PreviousWatermark** value of 3, the client can compare this value to the Watermark value of the last notification received.</span></span> <span data-ttu-id="50a9b-124">Auf diese Weise kann der Client die Kontinuität von Ereignissen sicherstellen.</span><span class="sxs-lookup"><span data-stu-id="50a9b-124">This enables the client to ensure the continuity of events.</span></span> 
  
<span data-ttu-id="50a9b-125">Bei Push-Clients wird das **PreviousWatermark** mit dem lokalen, clientseitigen letzten bekannten Wasserzeichen verglichen.</span><span class="sxs-lookup"><span data-stu-id="50a9b-125">For push clients, the **PreviousWatermark** is compared to the local, client-side last known watermark.</span></span> <span data-ttu-id="50a9b-126">Wenn die Werte unterschiedlich sind, hat der Client eine Ereignisbenachrichtigung verpasst und sollte ein Abonnement mit dem neuesten lokalen Wasserzeichen wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="50a9b-126">If the values are different, the client has missed an event notification and should reestablish a subscription by using the latest local watermark.</span></span> <span data-ttu-id="50a9b-127">Wenn beispielsweise ein Push-Client drei Ereignisse für ein Abonnement mit Wasserzeichen 1, 2 und 3 erhält und die nächste Benachrichtigung mit einem **PreviousWatermark** -Wert von 5 geliefert wird, hat der Client mindestens eine Benachrichtigung verpasst und sollte ein neues Abonnement erstellen, wobei ein 3 als Wasserzeichen übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="50a9b-127">For example, if a push client receives three events for a subscription with watermarks 1, 2, and 3, and the next notification comes with a **PreviousWatermark** value of 5, the client has missed at least one notification and should create a new subscription, passing a 3 as the watermark.</span></span> 
  
<span data-ttu-id="50a9b-128">Im Fall eines Pull-Clients ist der Wert von **PreviousWatermark** identisch mit dem [Wasserzeichen](watermark.md) , das vom Client im GetEvents-Aufruf enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="50a9b-128">In the case of a pull client, the value of **PreviousWatermark** will be the same as the [Watermark](watermark.md) included by the client in the GetEvents call.</span></span> 
  
<span data-ttu-id="50a9b-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="50a9b-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="50a9b-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="50a9b-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="50a9b-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="50a9b-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="50a9b-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="50a9b-132">Schema Name</span></span>  <br/> |<span data-ttu-id="50a9b-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="50a9b-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="50a9b-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="50a9b-134">Validation File</span></span>  <br/> |<span data-ttu-id="50a9b-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="50a9b-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="50a9b-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="50a9b-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="50a9b-137">False</span><span class="sxs-lookup"><span data-stu-id="50a9b-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="50a9b-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50a9b-138">See also</span></span>



[<span data-ttu-id="50a9b-139">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="50a9b-139">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="50a9b-140">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="50a9b-140">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="50a9b-141">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="50a9b-141">Unsubscribe operation</span></span>](unsubscribe-operation.md)

