---
title: Sommerzeit
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Daylight
api_type:
- schema
ms.assetid: ea400839-fba8-4a5e-a5d1-9b677afc0ff9
description: Das Sommerzeit-Element darstellt, Datum und Uhrzeit, wann die Zeit von Normalzeit zu Sommerzeit wechselt.
ms.openlocfilehash: cdb6ed305f1d77a73b952f8c659991f3b2a8df7a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757873"
---
# <a name="daylight"></a><span data-ttu-id="95d14-103">Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="95d14-103">Daylight</span></span>

<span data-ttu-id="95d14-104">Das **Sommerzeit** -Element darstellt, Datum und Uhrzeit, wann die Zeit von Normalzeit zu Sommerzeit wechselt.</span><span class="sxs-lookup"><span data-stu-id="95d14-104">The **Daylight** element represents the date and time when the time changes from standard time to daylight saving time.</span></span> 
  
```xml
<Daylight TimeZoneName="">
   <Offset/>
   <RelativeYearlyRecurrence/>
   <Time/>
</Daylight>
```

```xml
<Daylight TimeZoneName="">
   <Offset/>
   <AbsoluteDate/>
   <Time/>
</Daylight>
```

<span data-ttu-id="95d14-105">**TimeChangeType**</span><span class="sxs-lookup"><span data-stu-id="95d14-105">**TimeChangeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="95d14-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="95d14-106">Attributes and elements</span></span>

<span data-ttu-id="95d14-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="95d14-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="95d14-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="95d14-108">Attributes</span></span>

|<span data-ttu-id="95d14-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="95d14-109">**Attribute**</span></span>|<span data-ttu-id="95d14-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="95d14-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="95d14-111">**TimeZoneName**</span><span class="sxs-lookup"><span data-stu-id="95d14-111">**TimeZoneName**</span></span> <br/> |<span data-ttu-id="95d14-112">Beschreibt den Namen der Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="95d14-112">Describes the name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="95d14-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="95d14-113">Child elements</span></span>

|<span data-ttu-id="95d14-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="95d14-114">**Element**</span></span>|<span data-ttu-id="95d14-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="95d14-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95d14-116">Offset</span><span class="sxs-lookup"><span data-stu-id="95d14-116">Offset</span></span>](offset.md) <br/> |<span data-ttu-id="95d14-117">Beschreibt die [BaseOffset](baseoffset.md)-Offset.</span><span class="sxs-lookup"><span data-stu-id="95d14-117">Describes the offset from the [BaseOffset](baseoffset.md).</span></span> <span data-ttu-id="95d14-118">Die offset zusätzlich zu diesen Offset Base identifiziert das Zeitformat an, entsprechend gibt an, ob es eine Standard- oder Sommerzeit.</span><span class="sxs-lookup"><span data-stu-id="95d14-118">The base offset in addition to this offset identifies the time according to whether it is standard or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="95d14-119">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="95d14-119">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="95d14-120">Beschreibt ein relative jährliches Serienmuster für eine Zeitzone Übergang Datumsformat an.</span><span class="sxs-lookup"><span data-stu-id="95d14-120">Describes a relative yearly recurrence pattern for a time zone transition date pattern.</span></span>  <br/> |
|[<span data-ttu-id="95d14-121">AbsoluteDate</span><span class="sxs-lookup"><span data-stu-id="95d14-121">AbsoluteDate</span></span>](absolutedate.md) <br/> |<span data-ttu-id="95d14-122">Stellt dar, wenn die Zeit von Standard- oder Sommerzeit geändert wird.</span><span class="sxs-lookup"><span data-stu-id="95d14-122">Represents the date when the time changes from standard or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="95d14-123">Zeit (TimeChangeType)</span><span class="sxs-lookup"><span data-stu-id="95d14-123">Time (TimeChangeType)</span></span>](time-timechangetype.md) <br/> |<span data-ttu-id="95d14-124">Beschreibt, wenn die Zeit zwischen Standardzeit und Sommerzeit geändert wird.</span><span class="sxs-lookup"><span data-stu-id="95d14-124">Describes the time when the time changes between standard time and daylight saving time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="95d14-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="95d14-125">Parent elements</span></span>

|<span data-ttu-id="95d14-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="95d14-126">**Element**</span></span>|<span data-ttu-id="95d14-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="95d14-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95d14-128">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="95d14-128">MeetingTimeZone</span></span>](meetingtimezone.md) <br/> |<span data-ttu-id="95d14-129">Stellt die Zeitzone des Speicherorts, in die Besprechung gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="95d14-129">Represents the time zone of the location where the meeting is hosted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95d14-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="95d14-130">Remarks</span></span>

<span data-ttu-id="95d14-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="95d14-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="95d14-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="95d14-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95d14-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="95d14-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="95d14-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="95d14-134">Schema Name</span></span>  <br/> |<span data-ttu-id="95d14-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="95d14-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="95d14-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="95d14-136">Validation File</span></span>  <br/> |<span data-ttu-id="95d14-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="95d14-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="95d14-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="95d14-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="95d14-139">False</span><span class="sxs-lookup"><span data-stu-id="95d14-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="95d14-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95d14-140">See also</span></span>

- [<span data-ttu-id="95d14-141">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="95d14-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

