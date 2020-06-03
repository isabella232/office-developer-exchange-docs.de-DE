---
title: Zeiten
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
description: Das Periods-Element stellt ein Array von Punkten dar, die den Zeit Offset in unterschiedlichen Phasen der Zeitzone definieren.
ms.openlocfilehash: 773457a6e4c0237eaeaf23109a7022427cc7dd0d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467774"
---
# <a name="periods"></a><span data-ttu-id="fa035-103">Zeiten</span><span class="sxs-lookup"><span data-stu-id="fa035-103">Periods</span></span>

<span data-ttu-id="fa035-104">Das **Periods** -Element stellt ein Array von Punkten dar, die den Zeit Offset in unterschiedlichen Phasen der Zeitzone definieren.</span><span class="sxs-lookup"><span data-stu-id="fa035-104">The **Periods** element represents an array of periods that define the time offset at different stages of the time zone.</span></span> 
  
```xml
<Periods>
   <Period/>
</Periods>
```

 <span data-ttu-id="fa035-105">**NonEmptyArrayOfPeriodsType**</span><span class="sxs-lookup"><span data-stu-id="fa035-105">**NonEmptyArrayOfPeriodsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fa035-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fa035-106">Attributes and elements</span></span>

<span data-ttu-id="fa035-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fa035-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa035-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="fa035-108">Attributes</span></span>

<span data-ttu-id="fa035-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="fa035-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fa035-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fa035-110">Child elements</span></span>

|<span data-ttu-id="fa035-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="fa035-111">**Element**</span></span>|<span data-ttu-id="fa035-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fa035-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa035-113">Period</span><span class="sxs-lookup"><span data-stu-id="fa035-113">Period</span></span>](period.md) <br/> |<span data-ttu-id="fa035-114">Definiert den Namen, den Zeit Offset und den eindeutigen Bezeichner für eine bestimmte Phase der Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="fa035-114">Defines the name, time offset, and unique identifier for a specific stage of the time zone.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fa035-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fa035-115">Parent elements</span></span>

|<span data-ttu-id="fa035-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="fa035-116">**Element**</span></span>|<span data-ttu-id="fa035-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fa035-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa035-118">StartTimeZone</span><span class="sxs-lookup"><span data-stu-id="fa035-118">StartTimeZone</span></span>](starttimezone.md) <br/> |<span data-ttu-id="fa035-119">Definiert die Zeitzone für die Startzeit einer [CalendarItem](calendaritem.md) -oder [MeetingRequest](meetingrequest.md)-Start Zeit.</span><span class="sxs-lookup"><span data-stu-id="fa035-119">Defines the time zone for the start time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="fa035-120">EndTimeZone</span><span class="sxs-lookup"><span data-stu-id="fa035-120">EndTimeZone</span></span>](endtimezone.md) <br/> |<span data-ttu-id="fa035-121">Definiert die Zeitzone für die Endzeit einer [CalendarItem](calendaritem.md) -oder [MeetingRequest](meetingrequest.md)-Datei.</span><span class="sxs-lookup"><span data-stu-id="fa035-121">Defines the time zone for the end time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="fa035-122">TimeZoneDefinition</span><span class="sxs-lookup"><span data-stu-id="fa035-122">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="fa035-123">Definiert eine Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="fa035-123">Defines a time zone.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa035-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa035-124">Remarks</span></span>

<span data-ttu-id="fa035-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="fa035-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fa035-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="fa035-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa035-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="fa035-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fa035-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fa035-128">Schema Name</span></span>  <br/> |<span data-ttu-id="fa035-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="fa035-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="fa035-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fa035-130">Validation File</span></span>  <br/> |<span data-ttu-id="fa035-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fa035-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fa035-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="fa035-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="fa035-133">False</span><span class="sxs-lookup"><span data-stu-id="fa035-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fa035-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa035-134">See also</span></span>



- [<span data-ttu-id="fa035-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="fa035-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

