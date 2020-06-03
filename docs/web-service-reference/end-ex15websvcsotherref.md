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
description: Das End-Element stellt das Ende einer Dauer dar.
ms.openlocfilehash: d36f555d2ac9c0c1d82053029720ec17a53f2d92
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456143"
---
# <a name="end"></a><span data-ttu-id="46121-103">Ende</span><span class="sxs-lookup"><span data-stu-id="46121-103">End</span></span>

<span data-ttu-id="46121-104">Das **End** -Element stellt das Ende einer Dauer dar.</span><span class="sxs-lookup"><span data-stu-id="46121-104">The **End** element represents the end of a duration.</span></span> 
  
```xml
<End/>
```

 <span data-ttu-id="46121-105">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="46121-105">**DateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="46121-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="46121-106">Attributes and elements</span></span>

<span data-ttu-id="46121-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="46121-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="46121-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="46121-108">Attributes</span></span>

<span data-ttu-id="46121-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="46121-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="46121-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="46121-110">Child elements</span></span>

<span data-ttu-id="46121-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="46121-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="46121-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="46121-112">Parent elements</span></span>

|<span data-ttu-id="46121-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="46121-113">**Element**</span></span>|<span data-ttu-id="46121-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="46121-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="46121-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="46121-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="46121-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="46121-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="46121-117">FirstOccurrence</span><span class="sxs-lookup"><span data-stu-id="46121-117">FirstOccurrence</span></span>](firstoccurrence.md) <br/> |<span data-ttu-id="46121-118">Stellt das erste Vorkommen eines wiederkehrenden Kalenderelements dar.</span><span class="sxs-lookup"><span data-stu-id="46121-118">Represents the first occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="46121-119">LastOccurrence</span><span class="sxs-lookup"><span data-stu-id="46121-119">LastOccurrence</span></span>](lastoccurrence.md) <br/> |<span data-ttu-id="46121-120">Stellt das letzte Vorkommen eines wiederkehrenden Kalenderelements dar.</span><span class="sxs-lookup"><span data-stu-id="46121-120">Represents the last occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="46121-121">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="46121-121">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="46121-122">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="46121-122">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="46121-123">Vorkommen</span><span class="sxs-lookup"><span data-stu-id="46121-123">Occurrence</span></span>](occurrence.md) <br/> |<span data-ttu-id="46121-124">Stellt ein einzelnes geändertes Vorkommen eines wiederkehrenden Kalenderelements dar.</span><span class="sxs-lookup"><span data-stu-id="46121-124">Represents a single modified occurrence of a recurring calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="46121-125">Textwert</span><span class="sxs-lookup"><span data-stu-id="46121-125">Text value</span></span>

<span data-ttu-id="46121-126">Der Wert Text stellt das Ende einer Dauer dar.</span><span class="sxs-lookup"><span data-stu-id="46121-126">The text value represents the end of a duration.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="46121-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46121-127">Remarks</span></span>

<span data-ttu-id="46121-128">Mit dem UpdateItem-Vorgang können die [Start](start.md) -und **Endzeit** eines Exchange-Informationsspeicher Elements festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="46121-128">The UpdateItem operation can set the [Start](start.md) and **End** time of an Exchange store item.</span></span> <span data-ttu-id="46121-129">In einer UpdateItem-Anforderung können Sie die [Startzeit](start.md) festlegen, ohne auch die **Endzeit** festzulegen.</span><span class="sxs-lookup"><span data-stu-id="46121-129">In an UpdateItem request, you can set the [Start](start.md) time without also setting the **End** time.</span></span> <span data-ttu-id="46121-130">Dies kann zu einem Fehler führen, wenn die [Startzeit](start.md) später als die **Endzeit** ist.</span><span class="sxs-lookup"><span data-stu-id="46121-130">This can cause an error if the [Start](start.md) time is later than the **End** time.</span></span> <span data-ttu-id="46121-131">Beachten Sie, dass Clientanwendungen Anpassungen an der **Endzeit** vornehmen müssen, wenn die [Startzeit](start.md) geändert wird, um die Dauer beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="46121-131">Be aware that client applications must perform adjustments to the **End** time when that [Start](start.md) time is changed in order to preserve the duration.</span></span> 
  
 <span data-ttu-id="46121-132">**Hinweis:** Die Zeitzonenoffset Informationen gehen verloren, wenn das [anfangs](start.md) -und Enddatum des **wiederkehrenden Haupt** Elements kein Datum aufweist, das dem ersten Vorkommen eines wöchentlichen Serienmusters entspricht.</span><span class="sxs-lookup"><span data-stu-id="46121-132">**Note** The time zone offset information is lost if the [Start](start.md) and **End** dates of the recurring master item do not have a date that is equal to the first occurrence of a weekly recurrence pattern.</span></span> 
  
<span data-ttu-id="46121-133">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="46121-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="46121-134">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="46121-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="46121-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="46121-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="46121-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="46121-136">Schema Name</span></span>  <br/> |<span data-ttu-id="46121-137">Schematypen</span><span class="sxs-lookup"><span data-stu-id="46121-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="46121-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="46121-138">Validation File</span></span>  <br/> |<span data-ttu-id="46121-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="46121-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="46121-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="46121-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="46121-141">False</span><span class="sxs-lookup"><span data-stu-id="46121-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="46121-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46121-142">See also</span></span>



[<span data-ttu-id="46121-143">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="46121-143">WeeklyRecurrence</span></span>](weeklyrecurrence.md)
  
 <span data-ttu-id="46121-144">**End**</span><span class="sxs-lookup"><span data-stu-id="46121-144">**End**</span></span>


- [<span data-ttu-id="46121-145">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="46121-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

