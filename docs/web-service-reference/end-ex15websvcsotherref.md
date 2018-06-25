---
title: Ende
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- End
api_type:
- schema
ms.assetid: 72329821-32ff-495d-b6e5-fdc011003c2e
description: Das Ende-Element darstellt, das Ende einer Dauer.
ms.openlocfilehash: 90eea4fc545fae083e5675225665e517b502ba6f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758226"
---
# <a name="end"></a><span data-ttu-id="ac581-103">Ende</span><span class="sxs-lookup"><span data-stu-id="ac581-103">End</span></span>

<span data-ttu-id="ac581-104">Das **Ende** -Element darstellt, das Ende einer Dauer.</span><span class="sxs-lookup"><span data-stu-id="ac581-104">The **End** element represents the end of a duration.</span></span> 
  
```xml
<End/>
```

 <span data-ttu-id="ac581-105">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="ac581-105">**DateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ac581-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ac581-106">Attributes and elements</span></span>

<span data-ttu-id="ac581-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ac581-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ac581-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ac581-108">Attributes</span></span>

<span data-ttu-id="ac581-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ac581-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ac581-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac581-110">Child elements</span></span>

<span data-ttu-id="ac581-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ac581-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ac581-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac581-112">Parent elements</span></span>

|<span data-ttu-id="ac581-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ac581-113">**Element**</span></span>|<span data-ttu-id="ac581-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ac581-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ac581-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="ac581-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="ac581-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="ac581-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="ac581-117">FirstOccurrence</span><span class="sxs-lookup"><span data-stu-id="ac581-117">FirstOccurrence</span></span>](firstoccurrence.md) <br/> |<span data-ttu-id="ac581-118">Stellt das erste Vorkommen eines sich wiederholenden Kalenderelements an.</span><span class="sxs-lookup"><span data-stu-id="ac581-118">Represents the first occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="ac581-119">LastOccurrence</span><span class="sxs-lookup"><span data-stu-id="ac581-119">LastOccurrence</span></span>](lastoccurrence.md) <br/> |<span data-ttu-id="ac581-120">Stellt das letzte Vorkommen eines sich wiederholenden Kalenderelements an.</span><span class="sxs-lookup"><span data-stu-id="ac581-120">Represents the last occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="ac581-121">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="ac581-121">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="ac581-122">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="ac581-122">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ac581-123">Vorkommen</span><span class="sxs-lookup"><span data-stu-id="ac581-123">Occurrence</span></span>](occurrence.md) <br/> |<span data-ttu-id="ac581-124">Stellt ein einzelnes geändertes Vorkommen des ein wiederkehrendes Kalenderelement.</span><span class="sxs-lookup"><span data-stu-id="ac581-124">Represents a single modified occurrence of a recurring calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ac581-125">Textwert</span><span class="sxs-lookup"><span data-stu-id="ac581-125">Text value</span></span>

<span data-ttu-id="ac581-126">Der Textwert stellt das Ende einer Dauer dar.</span><span class="sxs-lookup"><span data-stu-id="ac581-126">The text value represents the end of a duration.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ac581-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ac581-127">Remarks</span></span>

<span data-ttu-id="ac581-128">UpdateItem-Vorgang kann die Zeit [Start](start.md) und **End** eines Exchange-Speicher-Elements festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ac581-128">The UpdateItem operation can set the [Start](start.md) and **End** time of an Exchange store item.</span></span> <span data-ttu-id="ac581-129">In einer Anforderung UpdateItem können Sie [die Startzeit](start.md) festlegen, ohne dass auch **die Endzeit** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ac581-129">In an UpdateItem request, you can set the [Start](start.md) time without also setting the **End** time.</span></span> <span data-ttu-id="ac581-130">Dies kann einen Fehler verursachen, wenn [die Startzeit](start.md) **die Endzeit** liegt.</span><span class="sxs-lookup"><span data-stu-id="ac581-130">This can cause an error if the [Start](start.md) time is later than the **End** time.</span></span> <span data-ttu-id="ac581-131">Beachten Sie, dass Clientanwendungen Anpassungen an **die Endzeit** ausführen müssen, wenn [diese Startzeit](start.md) geändert wird, um die Dauer beibehalten.</span><span class="sxs-lookup"><span data-stu-id="ac581-131">Be aware that client applications must perform adjustments to the **End** time when that [Start](start.md) time is changed in order to preserve the duration.</span></span> 
  
 <span data-ttu-id="ac581-132">**Hinweis** Die Zeitzone Offset Informationen geht verloren, wenn die ** [Starten](start.md) und** Enddatum des wiederkehrenden master-Objekts nicht über ein Datum verfügen, das das erste Auftreten des ein wöchentliches Serienmuster gleich ist.</span><span class="sxs-lookup"><span data-stu-id="ac581-132">**Note** The time zone offset information is lost if the [Start](start.md) and **End** dates of the recurring master item do not have a date that is equal to the first occurrence of a weekly recurrence pattern.</span></span> 
  
<span data-ttu-id="ac581-133">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ac581-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ac581-134">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ac581-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac581-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac581-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ac581-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ac581-136">Schema Name</span></span>  <br/> |<span data-ttu-id="ac581-137">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ac581-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="ac581-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ac581-138">Validation File</span></span>  <br/> |<span data-ttu-id="ac581-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ac581-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ac581-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ac581-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="ac581-141">False</span><span class="sxs-lookup"><span data-stu-id="ac581-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ac581-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac581-142">See also</span></span>



[<span data-ttu-id="ac581-143">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="ac581-143">WeeklyRecurrence</span></span>](weeklyrecurrence.md)
  
 <span data-ttu-id="ac581-144">**End**</span><span class="sxs-lookup"><span data-stu-id="ac581-144">**End**</span></span>


- [<span data-ttu-id="ac581-145">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ac581-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

