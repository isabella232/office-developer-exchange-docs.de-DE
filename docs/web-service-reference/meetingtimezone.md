---
title: MeetingTimeZone
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingTimeZone
api_type:
- schema
ms.assetid: 413b47d9-8126-462c-9a4f-4e771a5e8889
description: Das MeetingTimeZone-Element darstellt, die Zeitzone des Speicherorts, in die Besprechung gehostet wird.
ms.openlocfilehash: ce014ac6d8841e451927a94049cb4e8860886fdf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830440"
---
# <a name="meetingtimezone"></a><span data-ttu-id="3f9c2-103">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="3f9c2-103">MeetingTimeZone</span></span>

<span data-ttu-id="3f9c2-104">Das **MeetingTimeZone** -Element darstellt, die Zeitzone des Speicherorts, in die Besprechung gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="3f9c2-104">The **MeetingTimeZone** element represents the time zone of the location where the meeting is hosted.</span></span> 
  
```xml
<MeetingTimeZone>
   <BaseOffset/>
   <Standard/>
   <Daylight/>
</MeetingTimeZone>
```

 <span data-ttu-id="3f9c2-105">**TimeZoneType**</span><span class="sxs-lookup"><span data-stu-id="3f9c2-105">**TimeZoneType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3f9c2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3f9c2-106">Attributes and elements</span></span>

<span data-ttu-id="3f9c2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3f9c2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3f9c2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3f9c2-108">Attributes</span></span>

|<span data-ttu-id="3f9c2-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="3f9c2-109">**Attribute**</span></span>|<span data-ttu-id="3f9c2-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3f9c2-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3f9c2-111">**TimeZoneName**</span><span class="sxs-lookup"><span data-stu-id="3f9c2-111">**TimeZoneName**</span></span> <br/> |<span data-ttu-id="3f9c2-112">Beschreibt den Namen der Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="3f9c2-112">Describes the name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3f9c2-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3f9c2-113">Child elements</span></span>

|<span data-ttu-id="3f9c2-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="3f9c2-114">**Element**</span></span>|<span data-ttu-id="3f9c2-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3f9c2-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3f9c2-116">BaseOffset</span><span class="sxs-lookup"><span data-stu-id="3f9c2-116">BaseOffset</span></span>](baseoffset.md) <br/> |<span data-ttu-id="3f9c2-117">Stellt die stündlich offset von UTC für die aktuelle Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="3f9c2-117">Represents the hourly offset from UTC for the current time zone.</span></span>  <br/> |
|[<span data-ttu-id="3f9c2-118">Standard</span><span class="sxs-lookup"><span data-stu-id="3f9c2-118">Standard</span></span>](standard.md) <br/> |<span data-ttu-id="3f9c2-119">Das Datum und Zeitpunkt der Änderung die Zeit von Sommerzeit auf Normalzeit darstellt.</span><span class="sxs-lookup"><span data-stu-id="3f9c2-119">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
|[<span data-ttu-id="3f9c2-120">Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="3f9c2-120">Daylight</span></span>](daylight.md) <br/> |<span data-ttu-id="3f9c2-121">Das Datum und Zeitpunkt der Änderung die Zeit von Normalzeit auf Sommerzeit darstellt.</span><span class="sxs-lookup"><span data-stu-id="3f9c2-121">Represents the date and time when the time changes from standard time to daylight saving time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3f9c2-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3f9c2-122">Parent elements</span></span>

|<span data-ttu-id="3f9c2-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="3f9c2-123">**Element**</span></span>|<span data-ttu-id="3f9c2-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3f9c2-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3f9c2-125">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="3f9c2-125">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="3f9c2-126">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="3f9c2-126">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="3f9c2-127">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="3f9c2-127">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="3f9c2-128">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="3f9c2-128">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f9c2-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3f9c2-129">Remarks</span></span>

<span data-ttu-id="3f9c2-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="3f9c2-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3f9c2-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3f9c2-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3f9c2-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="3f9c2-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3f9c2-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3f9c2-133">Schema Name</span></span>  <br/> |<span data-ttu-id="3f9c2-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3f9c2-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="3f9c2-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3f9c2-135">Validation File</span></span>  <br/> |<span data-ttu-id="3f9c2-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3f9c2-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3f9c2-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3f9c2-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="3f9c2-138">False</span><span class="sxs-lookup"><span data-stu-id="3f9c2-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3f9c2-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f9c2-139">See also</span></span>



- [<span data-ttu-id="3f9c2-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3f9c2-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

