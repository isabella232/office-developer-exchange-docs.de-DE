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
description: Das Standard-Element stellt das Datum und die Uhrzeit dar, zu der sich die Zeit von Sommerzeit zu Standardzeit ändert.
ms.openlocfilehash: 1214a1debb53c9a31ca7c92a0c9e5c0722960d75
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467564"
---
# <a name="standard"></a><span data-ttu-id="10e50-103">Standard</span><span class="sxs-lookup"><span data-stu-id="10e50-103">Standard</span></span>

<span data-ttu-id="10e50-104">Das **Standard** -Element stellt das Datum und die Uhrzeit dar, zu der sich die Zeit von Sommerzeit zu Standardzeit ändert.</span><span class="sxs-lookup"><span data-stu-id="10e50-104">The **Standard** element represents the date and time when the time changes from daylight saving time to standard time.</span></span> 
  
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

<span data-ttu-id="10e50-105">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="10e50-105">**TimeChangeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="10e50-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="10e50-106">Attributes and elements</span></span>

<span data-ttu-id="10e50-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="10e50-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="10e50-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="10e50-108">Attributes</span></span>

|<span data-ttu-id="10e50-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="10e50-109">**Attribute**</span></span>|<span data-ttu-id="10e50-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="10e50-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="10e50-111">**TimeZoneName**</span><span class="sxs-lookup"><span data-stu-id="10e50-111">**TimeZoneName**</span></span> <br/> |<span data-ttu-id="10e50-112">Beschreibt den Namen der Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="10e50-112">Describes the name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="10e50-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="10e50-113">Child elements</span></span>

|<span data-ttu-id="10e50-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="10e50-114">**Element**</span></span>|<span data-ttu-id="10e50-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="10e50-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="10e50-116">Offset</span><span class="sxs-lookup"><span data-stu-id="10e50-116">Offset</span></span>](offset.md) <br/> |<span data-ttu-id="10e50-117">Beschreibt den Offset aus dem [BaseOffset](baseoffset.md).</span><span class="sxs-lookup"><span data-stu-id="10e50-117">Describes the offset from the [BaseOffset](baseoffset.md).</span></span> <span data-ttu-id="10e50-118">Zusammen mit dem **BaseOffset** -Element gibt das **Offset** -Element an, ob es sich um Standardzeit oder Sommerzeit handelt.</span><span class="sxs-lookup"><span data-stu-id="10e50-118">Together with the **BaseOffset** element, the **Offset** element identifies whether the time is standard time or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="10e50-119">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="10e50-119">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="10e50-120">Beschreibt ein relatives jährliches Serienmuster für das übergangsdatum einer Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="10e50-120">Describes a relative yearly recurrence pattern for a time zone transition date.</span></span>  <br/> |
|[<span data-ttu-id="10e50-121">AbsoluteDate</span><span class="sxs-lookup"><span data-stu-id="10e50-121">AbsoluteDate</span></span>](absolutedate.md) <br/> |<span data-ttu-id="10e50-122">Stellt das Datum dar, an dem sich die Zeit zwischen Standardzeit oder Sommerzeit ändert.</span><span class="sxs-lookup"><span data-stu-id="10e50-122">Represents the date when the time changes from standard time or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="10e50-123">Zeit (Time ChangeType)</span><span class="sxs-lookup"><span data-stu-id="10e50-123">Time (TimeChangeType)</span></span>](time-timechangetype.md) <br/> |<span data-ttu-id="10e50-124">Beschreibt die Zeit, zu der sich die Zeit zwischen Standardzeit und Sommerzeit ändert.</span><span class="sxs-lookup"><span data-stu-id="10e50-124">Describes the time when the time changes between standard time and daylight saving time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="10e50-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="10e50-125">Parent elements</span></span>

|<span data-ttu-id="10e50-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="10e50-126">**Element**</span></span>|<span data-ttu-id="10e50-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="10e50-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="10e50-128">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="10e50-128">MeetingTimeZone</span></span>](meetingtimezone.md) <br/> |<span data-ttu-id="10e50-129">Stellt die Zeitzone des Speicherorts dar, an dem die Besprechung gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="10e50-129">Represents the time zone of the location where the meeting is hosted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10e50-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10e50-130">Remarks</span></span>

<span data-ttu-id="10e50-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="10e50-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="10e50-132">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="10e50-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="10e50-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="10e50-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="10e50-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="10e50-134">Schema Name</span></span>  <br/> |<span data-ttu-id="10e50-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="10e50-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="10e50-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="10e50-136">Validation File</span></span>  <br/> |<span data-ttu-id="10e50-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="10e50-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="10e50-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="10e50-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="10e50-139">False</span><span class="sxs-lookup"><span data-stu-id="10e50-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="10e50-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10e50-140">See also</span></span>

- [<span data-ttu-id="10e50-141">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="10e50-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

