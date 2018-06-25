---
title: LastOccurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- LastOccurrence
api_type:
- schema
ms.assetid: c9ef0fcb-4265-4e60-9986-fff0f211d00b
description: Das LastOccurrence-Element darstellt, das letzte Vorkommen eines sich wiederholenden Kalenderelements.
ms.openlocfilehash: 2c8fdfc0005e86c9dda84a48ae1d3692b5134ca8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830209"
---
# <a name="lastoccurrence"></a><span data-ttu-id="d6138-103">LastOccurrence</span><span class="sxs-lookup"><span data-stu-id="d6138-103">LastOccurrence</span></span>

<span data-ttu-id="d6138-104">Das **LastOccurrence** -Element darstellt, das letzte Vorkommen eines sich wiederholenden Kalenderelements.</span><span class="sxs-lookup"><span data-stu-id="d6138-104">The **LastOccurrence** element represents the last occurrence of a recurring calendar item.</span></span> 
  
```xml
<LastOccurrence>
   <ItemId/>
   <Start/>
   <End/>
   <OriginalStart/>
</LastOccurrence>
```

 <span data-ttu-id="d6138-105">**OccurrenceInfoType**</span><span class="sxs-lookup"><span data-stu-id="d6138-105">**OccurrenceInfoType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d6138-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d6138-106">Attributes and elements</span></span>

<span data-ttu-id="d6138-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d6138-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d6138-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d6138-108">Attributes</span></span>

<span data-ttu-id="d6138-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d6138-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d6138-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d6138-110">Child elements</span></span>

|<span data-ttu-id="d6138-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d6138-111">**Element**</span></span>|<span data-ttu-id="d6138-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6138-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d6138-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="d6138-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="d6138-114">Den eindeutigen Bezeichner und ein Änderungsprotokoll Schlüssel des das letzte Vorkommen eines sich wiederholenden Kalenderelements enthält.</span><span class="sxs-lookup"><span data-stu-id="d6138-114">Contains the unique identifier and change key of the last occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="d6138-115">Start</span><span class="sxs-lookup"><span data-stu-id="d6138-115">Start</span></span>](start.md) <br/> |<span data-ttu-id="d6138-116">Stellt die Anfangszeit der das letzte Vorkommen eines sich wiederholenden Kalenderelements an.</span><span class="sxs-lookup"><span data-stu-id="d6138-116">Represents the start time of the last occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="d6138-117">Ende</span><span class="sxs-lookup"><span data-stu-id="d6138-117">End </span></span>](end-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d6138-118">Stellt die Endzeit der das letzte Vorkommen eines sich wiederholenden Kalenderelements an.</span><span class="sxs-lookup"><span data-stu-id="d6138-118">Represents the end time of the last occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="d6138-119">OriginalStart</span><span class="sxs-lookup"><span data-stu-id="d6138-119">OriginalStart</span></span>](originalstart.md) <br/> |<span data-ttu-id="d6138-120">Stellt die ursprünglichen Anfangszeit der das letzte Vorkommen eines sich wiederholenden Kalenderelements an.</span><span class="sxs-lookup"><span data-stu-id="d6138-120">Represents the original start time of the last occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d6138-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d6138-121">Parent elements</span></span>

|<span data-ttu-id="d6138-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="d6138-122">**Element**</span></span>|<span data-ttu-id="d6138-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6138-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d6138-124">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="d6138-124">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="d6138-125">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="d6138-125">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="d6138-126">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="d6138-126">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="d6138-127">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="d6138-127">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6138-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d6138-128">Remarks</span></span>

<span data-ttu-id="d6138-129">Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den Wert RecurringMaster hat.</span><span class="sxs-lookup"><span data-stu-id="d6138-129">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span> 
  
<span data-ttu-id="d6138-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d6138-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d6138-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d6138-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d6138-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="d6138-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d6138-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d6138-133">Schema name</span></span>  <br/> |<span data-ttu-id="d6138-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d6138-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="d6138-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d6138-135">Validation file</span></span>  <br/> |<span data-ttu-id="d6138-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d6138-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d6138-137">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d6138-137">Can be empty</span></span>  <br/> |<span data-ttu-id="d6138-138">False</span><span class="sxs-lookup"><span data-stu-id="d6138-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d6138-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6138-139">See also</span></span>



- [<span data-ttu-id="d6138-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d6138-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
  
[<span data-ttu-id="d6138-141">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="d6138-141">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

