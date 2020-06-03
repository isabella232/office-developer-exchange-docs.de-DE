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
description: Das ConflictingMeetingCount-Element stellt die Anzahl der Besprechungen dar, die mit dem Kalenderelement in Konflikt stehen.
ms.openlocfilehash: d53245e1b5d1f0182b28b15bf55ba9742bbb2a07
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463860"
---
# <a name="conflictingmeetingcount"></a><span data-ttu-id="5f4a1-103">ConflictingMeetingCount</span><span class="sxs-lookup"><span data-stu-id="5f4a1-103">ConflictingMeetingCount</span></span>

<span data-ttu-id="5f4a1-104">Das **ConflictingMeetingCount** -Element stellt die Anzahl der Besprechungen dar, die mit dem Kalenderelement in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="5f4a1-104">The **ConflictingMeetingCount** element represents the number of meetings that conflict with the calendar item.</span></span> 
  
```xml
<ConflictingMeetingCount/>
```

 <span data-ttu-id="5f4a1-105">**int**</span><span class="sxs-lookup"><span data-stu-id="5f4a1-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5f4a1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5f4a1-106">Attributes and elements</span></span>

<span data-ttu-id="5f4a1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5f4a1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5f4a1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5f4a1-108">Attributes</span></span>

<span data-ttu-id="5f4a1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5f4a1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5f4a1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5f4a1-110">Child elements</span></span>

<span data-ttu-id="5f4a1-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="5f4a1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5f4a1-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5f4a1-112">Parent elements</span></span>

|<span data-ttu-id="5f4a1-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5f4a1-113">**Element**</span></span>|<span data-ttu-id="5f4a1-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5f4a1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f4a1-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="5f4a1-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="5f4a1-116">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="5f4a1-116">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5f4a1-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="5f4a1-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="5f4a1-118">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="5f4a1-118">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5f4a1-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="5f4a1-119">Text value</span></span>

<span data-ttu-id="5f4a1-120">Der Wert Text stellt eine ganze Zahl dar.</span><span class="sxs-lookup"><span data-stu-id="5f4a1-120">The text value represents an integer.</span></span> <span data-ttu-id="5f4a1-121">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="5f4a1-121">This property is read-only.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5f4a1-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f4a1-122">Remarks</span></span>

<span data-ttu-id="5f4a1-123">Ein Kalenderelement wird als widersprüchlich betrachtet, wenn es, zumindest teilweise, gleichzeitig mit einem anderen Kalenderelement in demselben Kalenderordner auftritt.</span><span class="sxs-lookup"><span data-stu-id="5f4a1-123">A calendar item is considered conflicting if it occurs, at least in part, at the same time as another calendar item in the same calendar folder.</span></span> <span data-ttu-id="5f4a1-124">Wenn sich ein Kalenderelement in einem nicht-Kalender-Ordner befindet, wird es mit Kalenderelementen im Standardkalenderordner verglichen.</span><span class="sxs-lookup"><span data-stu-id="5f4a1-124">If a calendar item is in a noncalendar folder, it is compared with calendar items in the default calendar folder.</span></span> <span data-ttu-id="5f4a1-125">Besprechungsanfragen werden mit Kalenderelementen im Standardkalenderordner verglichen.</span><span class="sxs-lookup"><span data-stu-id="5f4a1-125">Meeting requests are compared with calendar items in the default calendar folder.</span></span>
  
<span data-ttu-id="5f4a1-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="5f4a1-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5f4a1-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="5f4a1-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5f4a1-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="5f4a1-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5f4a1-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5f4a1-129">Schema name</span></span>  <br/> |<span data-ttu-id="5f4a1-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5f4a1-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="5f4a1-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5f4a1-131">Validation file</span></span>  <br/> |<span data-ttu-id="5f4a1-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5f4a1-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5f4a1-133">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="5f4a1-133">Can be empty</span></span>  <br/> |<span data-ttu-id="5f4a1-134">False</span><span class="sxs-lookup"><span data-stu-id="5f4a1-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5f4a1-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f4a1-135">See also</span></span>



- [<span data-ttu-id="5f4a1-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5f4a1-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

