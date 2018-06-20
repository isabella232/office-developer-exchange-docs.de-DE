---
title: ConflictingMeetingCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConflictingMeetingCount
api_type:
- schema
ms.assetid: 11f4d93a-b514-4a27-8d19-f4f0a35a185e
description: Das ConflictingMeetingCount-Element darstellt, die Anzahl der Besprechungen, die mit dem Kalenderelement in Konflikt stehen.
ms.openlocfilehash: ace800982c284cf65ff22d92c711197ee5ee1d06
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757594"
---
# <a name="conflictingmeetingcount"></a><span data-ttu-id="7e7df-103">ConflictingMeetingCount</span><span class="sxs-lookup"><span data-stu-id="7e7df-103">ConflictingMeetingCount</span></span>

<span data-ttu-id="7e7df-104">Das **ConflictingMeetingCount** -Element darstellt, die Anzahl der Besprechungen, die mit dem Kalenderelement in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="7e7df-104">The **ConflictingMeetingCount** element represents the number of meetings that conflict with the calendar item.</span></span> 
  
```xml
<ConflictingMeetingCount/>
```

 <span data-ttu-id="7e7df-105">**int**</span><span class="sxs-lookup"><span data-stu-id="7e7df-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7e7df-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7e7df-106">Attributes and elements</span></span>

<span data-ttu-id="7e7df-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7e7df-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7e7df-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7e7df-108">Attributes</span></span>

<span data-ttu-id="7e7df-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7e7df-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7e7df-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7e7df-110">Child elements</span></span>

<span data-ttu-id="7e7df-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="7e7df-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7e7df-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7e7df-112">Parent elements</span></span>

|<span data-ttu-id="7e7df-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7e7df-113">**Element**</span></span>|<span data-ttu-id="7e7df-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e7df-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7e7df-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="7e7df-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="7e7df-116">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="7e7df-116">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7e7df-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="7e7df-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="7e7df-118">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="7e7df-118">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7e7df-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="7e7df-119">Text value</span></span>

<span data-ttu-id="7e7df-120">Der Textwert stellt eine ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="7e7df-120">The text value represents an integer.</span></span> <span data-ttu-id="7e7df-121">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7e7df-121">This property is read-only.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7e7df-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7e7df-122">Remarks</span></span>

<span data-ttu-id="7e7df-123">Ein Kalenderelement gilt miteinander in Konflikt stehende Wenn es, mindestens im Webpart zur selben Zeit als eine andere Kalenderelement im gleichen Kalenderordner auftritt.</span><span class="sxs-lookup"><span data-stu-id="7e7df-123">A calendar item is considered conflicting if it occurs, at least in part, at the same time as another calendar item in the same calendar folder.</span></span> <span data-ttu-id="7e7df-124">Wenn ein Kalenderelement in einem Ordner Noncalendar ist, wird es mit Kalenderelementen in den Standardordner Kalender verglichen.</span><span class="sxs-lookup"><span data-stu-id="7e7df-124">If a calendar item is in a noncalendar folder, it is compared with calendar items in the default calendar folder.</span></span> <span data-ttu-id="7e7df-125">Besprechungsanfragen werden mit Kalenderelementen in den Standardordner Kalender verglichen.</span><span class="sxs-lookup"><span data-stu-id="7e7df-125">Meeting requests are compared with calendar items in the default calendar folder.</span></span>
  
<span data-ttu-id="7e7df-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="7e7df-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7e7df-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7e7df-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7e7df-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="7e7df-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7e7df-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7e7df-129">Schema name</span></span>  <br/> |<span data-ttu-id="7e7df-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7e7df-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="7e7df-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7e7df-131">Validation file</span></span>  <br/> |<span data-ttu-id="7e7df-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7e7df-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7e7df-133">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="7e7df-133">Can be empty</span></span>  <br/> |<span data-ttu-id="7e7df-134">False</span><span class="sxs-lookup"><span data-stu-id="7e7df-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7e7df-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e7df-135">See also</span></span>



- [<span data-ttu-id="7e7df-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7e7df-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

