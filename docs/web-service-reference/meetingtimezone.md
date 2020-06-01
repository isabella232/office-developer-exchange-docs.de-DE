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
description: Das MeetingTimeZone-Element stellt die Zeitzone des Speicherorts dar, an dem die Besprechung gehostet wird.
ms.openlocfilehash: aef4ac4e7571ded6920cbaf90e2895d421068f55
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465471"
---
# <a name="meetingtimezone"></a><span data-ttu-id="7af9b-103">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="7af9b-103">MeetingTimeZone</span></span>

<span data-ttu-id="7af9b-104">Das **MeetingTimeZone** -Element stellt die Zeitzone des Speicherorts dar, an dem die Besprechung gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="7af9b-104">The **MeetingTimeZone** element represents the time zone of the location where the meeting is hosted.</span></span> 
  
```xml
<MeetingTimeZone>
   <BaseOffset/>
   <Standard/>
   <Daylight/>
</MeetingTimeZone>
```

 <span data-ttu-id="7af9b-105">**Timezonetype**</span><span class="sxs-lookup"><span data-stu-id="7af9b-105">**TimeZoneType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7af9b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7af9b-106">Attributes and elements</span></span>

<span data-ttu-id="7af9b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7af9b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7af9b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7af9b-108">Attributes</span></span>

|<span data-ttu-id="7af9b-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7af9b-109">**Attribute**</span></span>|<span data-ttu-id="7af9b-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7af9b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7af9b-111">**TimeZoneName**</span><span class="sxs-lookup"><span data-stu-id="7af9b-111">**TimeZoneName**</span></span> <br/> |<span data-ttu-id="7af9b-112">Beschreibt den Namen der Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="7af9b-112">Describes the name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7af9b-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7af9b-113">Child elements</span></span>

|<span data-ttu-id="7af9b-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="7af9b-114">**Element**</span></span>|<span data-ttu-id="7af9b-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7af9b-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7af9b-116">BaseOffset</span><span class="sxs-lookup"><span data-stu-id="7af9b-116">BaseOffset</span></span>](baseoffset.md) <br/> |<span data-ttu-id="7af9b-117">Stellt den stündlichen Offset von UTC für die aktuelle Zeitzone dar.</span><span class="sxs-lookup"><span data-stu-id="7af9b-117">Represents the hourly offset from UTC for the current time zone.</span></span>  <br/> |
|[<span data-ttu-id="7af9b-118">Standard</span><span class="sxs-lookup"><span data-stu-id="7af9b-118">Standard</span></span>](standard.md) <br/> |<span data-ttu-id="7af9b-119">Stellt das Datum und die Uhrzeit dar, zu der sich die Zeit von Sommerzeit zu Standardzeit ändert.</span><span class="sxs-lookup"><span data-stu-id="7af9b-119">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
|[<span data-ttu-id="7af9b-120">Sommer</span><span class="sxs-lookup"><span data-stu-id="7af9b-120">Daylight</span></span>](daylight.md) <br/> |<span data-ttu-id="7af9b-121">Stellt das Datum und die Uhrzeit dar, zu der die Zeit von Standardzeit zu Sommerzeit wechselt.</span><span class="sxs-lookup"><span data-stu-id="7af9b-121">Represents the date and time when the time changes from standard time to daylight saving time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7af9b-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7af9b-122">Parent elements</span></span>

|<span data-ttu-id="7af9b-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="7af9b-123">**Element**</span></span>|<span data-ttu-id="7af9b-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7af9b-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7af9b-125">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="7af9b-125">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="7af9b-126">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="7af9b-126">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="7af9b-127">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="7af9b-127">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="7af9b-128">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="7af9b-128">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7af9b-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7af9b-129">Remarks</span></span>

<span data-ttu-id="7af9b-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="7af9b-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7af9b-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7af9b-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7af9b-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="7af9b-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7af9b-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7af9b-133">Schema Name</span></span>  <br/> |<span data-ttu-id="7af9b-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7af9b-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="7af9b-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7af9b-135">Validation File</span></span>  <br/> |<span data-ttu-id="7af9b-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7af9b-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7af9b-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7af9b-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="7af9b-138">False</span><span class="sxs-lookup"><span data-stu-id="7af9b-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7af9b-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7af9b-139">See also</span></span>



- [<span data-ttu-id="7af9b-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7af9b-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

