---
title: Perioden
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Periods
api_type:
- schema
ms.assetid: 7920d81d-abba-4232-8bfe-49267b6c9a36
description: Perioden-Element stellt ein Array von Zeiträumen, mit die den Uhrzeit-Offset in verschiedenen Phasen der Zeitzone definiert.
ms.openlocfilehash: f2f9cf7c724b453d2b1975fcf72c55bc02caa54b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830729"
---
# <a name="periods"></a><span data-ttu-id="31b69-103">Perioden</span><span class="sxs-lookup"><span data-stu-id="31b69-103">Periods</span></span>

<span data-ttu-id="31b69-104">**Perioden** -Element stellt ein Array von Zeiträumen, mit die den Uhrzeit-Offset in verschiedenen Phasen der Zeitzone definiert.</span><span class="sxs-lookup"><span data-stu-id="31b69-104">The **Periods** element represents an array of periods that define the time offset at different stages of the time zone.</span></span> 
  
```xml
<Periods>
   <Period/>
</Periods>
```

 <span data-ttu-id="31b69-105">**NonEmptyArrayOfPeriodsType**</span><span class="sxs-lookup"><span data-stu-id="31b69-105">**NonEmptyArrayOfPeriodsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="31b69-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="31b69-106">Attributes and elements</span></span>

<span data-ttu-id="31b69-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="31b69-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="31b69-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="31b69-108">Attributes</span></span>

<span data-ttu-id="31b69-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="31b69-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="31b69-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="31b69-110">Child elements</span></span>

|<span data-ttu-id="31b69-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="31b69-111">**Element**</span></span>|<span data-ttu-id="31b69-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="31b69-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31b69-113">Period</span><span class="sxs-lookup"><span data-stu-id="31b69-113">Period</span></span>](period.md) <br/> |<span data-ttu-id="31b69-114">Definiert die Namen sowie die Uhrzeitoffset und eindeutiger Bezeichner für eine bestimmte Phase der Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="31b69-114">Defines the name, time offset, and unique identifier for a specific stage of the time zone.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="31b69-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="31b69-115">Parent elements</span></span>

|<span data-ttu-id="31b69-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="31b69-116">**Element**</span></span>|<span data-ttu-id="31b69-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="31b69-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31b69-118">StartTimeZone-Zeitzone</span><span class="sxs-lookup"><span data-stu-id="31b69-118">StartTimeZone</span></span>](starttimezone.md) <br/> |<span data-ttu-id="31b69-119">Definiert die Zeitzone für die Startzeit eines [CalendarItem](calendaritem.md) oder [MeetingRequest](meetingrequest.md).</span><span class="sxs-lookup"><span data-stu-id="31b69-119">Defines the time zone for the start time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="31b69-120">EndTimeZone</span><span class="sxs-lookup"><span data-stu-id="31b69-120">EndTimeZone</span></span>](endtimezone.md) <br/> |<span data-ttu-id="31b69-121">Definiert die Zeitzone für die Endzeit eines [CalendarItem](calendaritem.md) oder [MeetingRequest](meetingrequest.md).</span><span class="sxs-lookup"><span data-stu-id="31b69-121">Defines the time zone for the end time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="31b69-122">Zeitzonendefinition</span><span class="sxs-lookup"><span data-stu-id="31b69-122">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="31b69-123">Definiert eine Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="31b69-123">Defines a time zone.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31b69-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="31b69-124">Remarks</span></span>

<span data-ttu-id="31b69-125">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="31b69-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="31b69-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="31b69-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31b69-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="31b69-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="31b69-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="31b69-128">Schema Name</span></span>  <br/> |<span data-ttu-id="31b69-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="31b69-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="31b69-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="31b69-130">Validation File</span></span>  <br/> |<span data-ttu-id="31b69-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="31b69-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="31b69-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="31b69-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="31b69-133">False</span><span class="sxs-lookup"><span data-stu-id="31b69-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="31b69-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31b69-134">See also</span></span>



- [<span data-ttu-id="31b69-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="31b69-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

