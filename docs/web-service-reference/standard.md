---
title: Standard
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Standard
api_type:
- schema
ms.assetid: d598f0a6-e296-423f-8ce5-3da57cfd8189
description: Das Standard-Element darstellt, Datum und Uhrzeit, wann die Zeit von Sommerzeit zu Normalzeit wechselt.
ms.openlocfilehash: 1c9be4cf35773583078bc8e16ddf44433d3ad98c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831536"
---
# <a name="standard"></a><span data-ttu-id="dfe79-103">Standard</span><span class="sxs-lookup"><span data-stu-id="dfe79-103">Standard</span></span>

<span data-ttu-id="dfe79-104">Das **Standard** -Element darstellt, Datum und Uhrzeit, wann die Zeit von Sommerzeit zu Normalzeit wechselt.</span><span class="sxs-lookup"><span data-stu-id="dfe79-104">The **Standard** element represents the date and time when the time changes from daylight saving time to standard time.</span></span> 
  
```xml
<Standard TimeZoneName="">
   <Offset/>
   <RelativeYearlyRecurrence/>
   <Time/>
</Standard>
```

 <span data-ttu-id="dfe79-105">**TimeChangeType**</span><span class="sxs-lookup"><span data-stu-id="dfe79-105">**TimeChangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dfe79-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="dfe79-106">Attributes and elements</span></span>

<span data-ttu-id="dfe79-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="dfe79-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dfe79-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="dfe79-108">Attributes</span></span>

|<span data-ttu-id="dfe79-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="dfe79-109">**Attribute**</span></span>|<span data-ttu-id="dfe79-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dfe79-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dfe79-111">**TimeZoneName**</span><span class="sxs-lookup"><span data-stu-id="dfe79-111">**TimeZoneName**</span></span> <br/> |<span data-ttu-id="dfe79-112">Beschreibt den Namen der Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="dfe79-112">Describes the name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="dfe79-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dfe79-113">Child elements</span></span>

|<span data-ttu-id="dfe79-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="dfe79-114">**Element**</span></span>|<span data-ttu-id="dfe79-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dfe79-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dfe79-116">Offset</span><span class="sxs-lookup"><span data-stu-id="dfe79-116">Offset</span></span>](offset.md) <br/> |<span data-ttu-id="dfe79-117">Beschreibt die [BaseOffset](baseoffset.md)-Offset.</span><span class="sxs-lookup"><span data-stu-id="dfe79-117">Describes the offset from the [BaseOffset](baseoffset.md).</span></span> <span data-ttu-id="dfe79-118">Zusammen mit dem **BaseOffset** -Element identifiziert das **Offset** -Element an, ob die Zeit Standardzeit oder Sommerzeit.</span><span class="sxs-lookup"><span data-stu-id="dfe79-118">Together with the **BaseOffset** element, the **Offset** element identifies whether the time is standard time or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="dfe79-119">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="dfe79-119">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="dfe79-120">Ein relative jährliches Serienmuster beschrieben für eine Zeitzone Übergangsdatum.</span><span class="sxs-lookup"><span data-stu-id="dfe79-120">Describes a relative yearly recurrence pattern for a time zone transition date.</span></span>  <br/> |
|[<span data-ttu-id="dfe79-121">AbsoluteDate</span><span class="sxs-lookup"><span data-stu-id="dfe79-121">AbsoluteDate</span></span>](absolutedate.md) <br/> |<span data-ttu-id="dfe79-122">Stellt dar, wenn die Zeit von Standardzeit oder Sommerzeit geändert wird.</span><span class="sxs-lookup"><span data-stu-id="dfe79-122">Represents the date when the time changes from standard time or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="dfe79-123">Zeit (TimeChangeType)</span><span class="sxs-lookup"><span data-stu-id="dfe79-123">Time (TimeChangeType)</span></span>](time-timechangetype.md) <br/> |<span data-ttu-id="dfe79-124">Beschreibt, wenn die Zeit zwischen Standardzeit und Sommerzeit geändert wird.</span><span class="sxs-lookup"><span data-stu-id="dfe79-124">Describes the time when the time changes between standard time and daylight saving time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dfe79-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dfe79-125">Parent elements</span></span>

|<span data-ttu-id="dfe79-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="dfe79-126">**Element**</span></span>|<span data-ttu-id="dfe79-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dfe79-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dfe79-128">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="dfe79-128">MeetingTimeZone</span></span>](meetingtimezone.md) <br/> |<span data-ttu-id="dfe79-129">Stellt die Zeitzone des Speicherorts, in die Besprechung gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="dfe79-129">Represents the time zone of the location where the meeting is hosted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dfe79-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dfe79-130">Remarks</span></span>

<span data-ttu-id="dfe79-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="dfe79-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dfe79-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="dfe79-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dfe79-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="dfe79-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dfe79-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="dfe79-134">Schema Name</span></span>  <br/> |<span data-ttu-id="dfe79-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="dfe79-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="dfe79-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="dfe79-136">Validation File</span></span>  <br/> |<span data-ttu-id="dfe79-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="dfe79-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dfe79-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="dfe79-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="dfe79-139">False</span><span class="sxs-lookup"><span data-stu-id="dfe79-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dfe79-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dfe79-140">See also</span></span>



- [<span data-ttu-id="dfe79-141">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="dfe79-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

