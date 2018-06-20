---
title: FirstOccurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FirstOccurrence
api_type:
- schema
ms.assetid: d6748860-ce0d-4d2e-b7e4-9ed834f1e45a
description: Das FirstOccurrence-Element darstellt, das erste Auftreten des ein wiederkehrendes Kalenderelement.
ms.openlocfilehash: e5244e74bdd5a4b8e22c6e63811db53b46fa353a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758490"
---
# <a name="firstoccurrence"></a><span data-ttu-id="e5924-103">FirstOccurrence</span><span class="sxs-lookup"><span data-stu-id="e5924-103">FirstOccurrence</span></span>

<span data-ttu-id="e5924-104">Das **FirstOccurrence** -Element darstellt, das erste Auftreten des ein wiederkehrendes Kalenderelement.</span><span class="sxs-lookup"><span data-stu-id="e5924-104">The **FirstOccurrence** element represents the first occurrence of a recurring calendar item.</span></span> 
  
```xml
<FirstOccurrence>
   <ItemId/>
   <Start/>
   <End/>
   <OriginalStart/>
</FirstOccurrence>
```

 <span data-ttu-id="e5924-105">**OccurrenceInfoType**</span><span class="sxs-lookup"><span data-stu-id="e5924-105">**OccurrenceInfoType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e5924-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e5924-106">Attributes and elements</span></span>

<span data-ttu-id="e5924-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e5924-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e5924-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e5924-108">Attributes</span></span>

<span data-ttu-id="e5924-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e5924-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e5924-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e5924-110">Child elements</span></span>

|<span data-ttu-id="e5924-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e5924-111">**Element**</span></span>|<span data-ttu-id="e5924-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e5924-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e5924-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="e5924-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="e5924-114">Den eindeutigen Bezeichner und ein Änderungsprotokoll Schlüssel des ersten Vorkommens einer wiederkehrenden Kalenderelement enthält.</span><span class="sxs-lookup"><span data-stu-id="e5924-114">Contains the unique identifier and change key of the first occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="e5924-115">Start</span><span class="sxs-lookup"><span data-stu-id="e5924-115">Start</span></span>](start.md) <br/> |<span data-ttu-id="e5924-116">Stellt die Anfangszeit des ersten Vorkommens einer wiederkehrenden Kalenderelement.</span><span class="sxs-lookup"><span data-stu-id="e5924-116">Represents the start time of the first occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="e5924-117">Ende</span><span class="sxs-lookup"><span data-stu-id="e5924-117">End </span></span>](end-ex15websvcsotherref.md) <br/> |<span data-ttu-id="e5924-118">Die Endzeit des ersten Vorkommens einer wiederkehrenden Kalenderelement darstellt.</span><span class="sxs-lookup"><span data-stu-id="e5924-118">Represents the end time of the first occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="e5924-119">OriginalStart</span><span class="sxs-lookup"><span data-stu-id="e5924-119">OriginalStart</span></span>](originalstart.md) <br/> |<span data-ttu-id="e5924-120">Stellt die ursprünglichen Startzeit des ersten Vorkommens einer wiederkehrenden Kalenderelement.</span><span class="sxs-lookup"><span data-stu-id="e5924-120">Represents the original start time of the first occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e5924-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e5924-121">Parent elements</span></span>

|<span data-ttu-id="e5924-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="e5924-122">**Element**</span></span>|<span data-ttu-id="e5924-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e5924-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e5924-124">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="e5924-124">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="e5924-125">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="e5924-125">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="e5924-126">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="e5924-126">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="e5924-127">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="e5924-127">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5924-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e5924-128">Remarks</span></span>

<span data-ttu-id="e5924-129">Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den Wert RecurringMaster hat.</span><span class="sxs-lookup"><span data-stu-id="e5924-129">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span> 
  
<span data-ttu-id="e5924-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="e5924-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e5924-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e5924-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e5924-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="e5924-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e5924-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e5924-133">Schema name</span></span>  <br/> |<span data-ttu-id="e5924-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e5924-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="e5924-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e5924-135">Validation file</span></span>  <br/> |<span data-ttu-id="e5924-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e5924-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e5924-137">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="e5924-137">Can be empty</span></span>  <br/> |<span data-ttu-id="e5924-138">False</span><span class="sxs-lookup"><span data-stu-id="e5924-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e5924-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5924-139">See also</span></span>



- [<span data-ttu-id="e5924-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e5924-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
  
[<span data-ttu-id="e5924-141">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="e5924-141">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

