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
description: Das FirstOccurrence-Element stellt das erste Vorkommen eines wiederkehrenden Kalenderelements dar.
ms.openlocfilehash: 22ee9018df1e89a3783c4dfb56aaf065b2c8ea6c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466297"
---
# <a name="firstoccurrence"></a><span data-ttu-id="3bab6-103">FirstOccurrence</span><span class="sxs-lookup"><span data-stu-id="3bab6-103">FirstOccurrence</span></span>

<span data-ttu-id="3bab6-104">Das **FirstOccurrence** -Element stellt das erste Vorkommen eines wiederkehrenden Kalenderelements dar.</span><span class="sxs-lookup"><span data-stu-id="3bab6-104">The **FirstOccurrence** element represents the first occurrence of a recurring calendar item.</span></span> 
  
```xml
<FirstOccurrence>
   <ItemId/>
   <Start/>
   <End/>
   <OriginalStart/>
</FirstOccurrence>
```

 <span data-ttu-id="3bab6-105">**OccurrenceInfoType**</span><span class="sxs-lookup"><span data-stu-id="3bab6-105">**OccurrenceInfoType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3bab6-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3bab6-106">Attributes and elements</span></span>

<span data-ttu-id="3bab6-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3bab6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3bab6-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3bab6-108">Attributes</span></span>

<span data-ttu-id="3bab6-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3bab6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3bab6-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3bab6-110">Child elements</span></span>

|<span data-ttu-id="3bab6-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3bab6-111">**Element**</span></span>|<span data-ttu-id="3bab6-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3bab6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3bab6-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="3bab6-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="3bab6-114">Enthält den eindeutigen Bezeichner und den Änderungsschlüssel des ersten Vorkommens eines wiederkehrenden Kalenderelements.</span><span class="sxs-lookup"><span data-stu-id="3bab6-114">Contains the unique identifier and change key of the first occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="3bab6-115">Start</span><span class="sxs-lookup"><span data-stu-id="3bab6-115">Start</span></span>](start.md) <br/> |<span data-ttu-id="3bab6-116">Stellt die Startzeit des ersten Auftretens eines wiederkehrenden Kalenderelements dar.</span><span class="sxs-lookup"><span data-stu-id="3bab6-116">Represents the start time of the first occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="3bab6-117">End</span><span class="sxs-lookup"><span data-stu-id="3bab6-117">End </span></span>](end-ex15websvcsotherref.md) <br/> |<span data-ttu-id="3bab6-118">Stellt die Endzeit des ersten Vorkommens eines wiederkehrenden Kalenderelements dar.</span><span class="sxs-lookup"><span data-stu-id="3bab6-118">Represents the end time of the first occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="3bab6-119">OriginalStart</span><span class="sxs-lookup"><span data-stu-id="3bab6-119">OriginalStart</span></span>](originalstart.md) <br/> |<span data-ttu-id="3bab6-120">Stellt die ursprüngliche Startzeit des ersten Vorkommens eines wiederkehrenden Kalenderelements dar.</span><span class="sxs-lookup"><span data-stu-id="3bab6-120">Represents the original start time of the first occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3bab6-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3bab6-121">Parent elements</span></span>

|<span data-ttu-id="3bab6-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="3bab6-122">**Element**</span></span>|<span data-ttu-id="3bab6-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3bab6-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3bab6-124">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="3bab6-124">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="3bab6-125">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="3bab6-125">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="3bab6-126">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="3bab6-126">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="3bab6-127">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="3bab6-127">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3bab6-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3bab6-128">Remarks</span></span>

<span data-ttu-id="3bab6-129">Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den RecurringMaster-Wert aufweist.</span><span class="sxs-lookup"><span data-stu-id="3bab6-129">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span> 
  
<span data-ttu-id="3bab6-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="3bab6-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3bab6-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3bab6-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3bab6-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="3bab6-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3bab6-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3bab6-133">Schema name</span></span>  <br/> |<span data-ttu-id="3bab6-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3bab6-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="3bab6-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3bab6-135">Validation file</span></span>  <br/> |<span data-ttu-id="3bab6-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3bab6-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3bab6-137">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="3bab6-137">Can be empty</span></span>  <br/> |<span data-ttu-id="3bab6-138">False</span><span class="sxs-lookup"><span data-stu-id="3bab6-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3bab6-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3bab6-139">See also</span></span>



- [<span data-ttu-id="3bab6-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3bab6-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
  
[<span data-ttu-id="3bab6-141">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="3bab6-141">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

