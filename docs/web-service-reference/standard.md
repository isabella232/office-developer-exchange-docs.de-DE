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
ms.openlocfilehash: c121e959f243d982cfe50ed6b4ef39a82dae2cc8
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353434"
---
# <a name="standard"></a><span data-ttu-id="c30c4-103">Standard</span><span class="sxs-lookup"><span data-stu-id="c30c4-103">Standard</span></span>

<span data-ttu-id="c30c4-104">Das **Standard** -Element darstellt, Datum und Uhrzeit, wann die Zeit von Sommerzeit zu Normalzeit wechselt.</span><span class="sxs-lookup"><span data-stu-id="c30c4-104">The **Standard** element represents the date and time when the time changes from daylight saving time to standard time.</span></span> 
  
```xml
<Standard TimeZoneName="">
   <Offset/>
   <RelativeYearlyRecurrence/>
   <Time/>
</Standard>
```

```xml
<Standard TimeZoneName="">
   <Offset/>
   <AbsoluteDate/>
   <Time/>
</Standard>
```

<span data-ttu-id="c30c4-105">**TimeChangeType**</span><span class="sxs-lookup"><span data-stu-id="c30c4-105">**TimeChangeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c30c4-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c30c4-106">Attributes and elements</span></span>

<span data-ttu-id="c30c4-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c30c4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c30c4-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c30c4-108">Attributes</span></span>

|<span data-ttu-id="c30c4-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c30c4-109">**Attribute**</span></span>|<span data-ttu-id="c30c4-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c30c4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c30c4-111">**TimeZoneName**</span><span class="sxs-lookup"><span data-stu-id="c30c4-111">**TimeZoneName**</span></span> <br/> |<span data-ttu-id="c30c4-112">Beschreibt den Namen der Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="c30c4-112">Describes the name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c30c4-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c30c4-113">Child elements</span></span>

|<span data-ttu-id="c30c4-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="c30c4-114">**Element**</span></span>|<span data-ttu-id="c30c4-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c30c4-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c30c4-116">Offset</span><span class="sxs-lookup"><span data-stu-id="c30c4-116">Offset</span></span>](offset.md) <br/> |<span data-ttu-id="c30c4-117">Beschreibt die [BaseOffset](baseoffset.md)-Offset.</span><span class="sxs-lookup"><span data-stu-id="c30c4-117">Describes the offset from the [BaseOffset](baseoffset.md).</span></span> <span data-ttu-id="c30c4-118">Zusammen mit dem **BaseOffset** -Element identifiziert das **Offset** -Element an, ob die Zeit Standardzeit oder Sommerzeit.</span><span class="sxs-lookup"><span data-stu-id="c30c4-118">Together with the **BaseOffset** element, the **Offset** element identifies whether the time is standard time or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="c30c4-119">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="c30c4-119">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="c30c4-120">Ein relative jährliches Serienmuster beschrieben für eine Zeitzone Übergangsdatum.</span><span class="sxs-lookup"><span data-stu-id="c30c4-120">Describes a relative yearly recurrence pattern for a time zone transition date.</span></span>  <br/> |
|[<span data-ttu-id="c30c4-121">AbsoluteDate</span><span class="sxs-lookup"><span data-stu-id="c30c4-121">AbsoluteDate</span></span>](absolutedate.md) <br/> |<span data-ttu-id="c30c4-122">Stellt dar, wenn die Zeit von Standardzeit oder Sommerzeit geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c30c4-122">Represents the date when the time changes from standard time or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="c30c4-123">Zeit (TimeChangeType)</span><span class="sxs-lookup"><span data-stu-id="c30c4-123">Time (TimeChangeType)</span></span>](time-timechangetype.md) <br/> |<span data-ttu-id="c30c4-124">Beschreibt, wenn die Zeit zwischen Standardzeit und Sommerzeit geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c30c4-124">Describes the time when the time changes between standard time and daylight saving time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c30c4-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c30c4-125">Parent elements</span></span>

|<span data-ttu-id="c30c4-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="c30c4-126">**Element**</span></span>|<span data-ttu-id="c30c4-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c30c4-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c30c4-128">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="c30c4-128">MeetingTimeZone</span></span>](meetingtimezone.md) <br/> |<span data-ttu-id="c30c4-129">Stellt die Zeitzone des Speicherorts, in die Besprechung gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="c30c4-129">Represents the time zone of the location where the meeting is hosted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c30c4-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c30c4-130">Remarks</span></span>

<span data-ttu-id="c30c4-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="c30c4-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c30c4-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c30c4-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c30c4-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="c30c4-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c30c4-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c30c4-134">Schema Name</span></span>  <br/> |<span data-ttu-id="c30c4-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c30c4-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="c30c4-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c30c4-136">Validation File</span></span>  <br/> |<span data-ttu-id="c30c4-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c30c4-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c30c4-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c30c4-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="c30c4-139">False</span><span class="sxs-lookup"><span data-stu-id="c30c4-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c30c4-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c30c4-140">See also</span></span>

- [<span data-ttu-id="c30c4-141">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c30c4-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

