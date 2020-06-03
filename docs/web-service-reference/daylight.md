---
title: Sommer
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
description: Das Tageslicht-Element stellt das Datum und die Uhrzeit dar, zu der die Zeit von Standardzeit zu Sommerzeit wechselt.
ms.openlocfilehash: bf2041cb4677f837ddb5b399041f1c19a7b5f577
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457459"
---
# <a name="daylight"></a><span data-ttu-id="c15ba-103">Sommer</span><span class="sxs-lookup"><span data-stu-id="c15ba-103">Daylight</span></span>

<span data-ttu-id="c15ba-104">Das **Tageslicht** -Element stellt das Datum und die Uhrzeit dar, zu der die Zeit von Standardzeit zu Sommerzeit wechselt.</span><span class="sxs-lookup"><span data-stu-id="c15ba-104">The **Daylight** element represents the date and time when the time changes from standard time to daylight saving time.</span></span> 
  
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

<span data-ttu-id="c15ba-105">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="c15ba-105">**TimeChangeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c15ba-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c15ba-106">Attributes and elements</span></span>

<span data-ttu-id="c15ba-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c15ba-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c15ba-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c15ba-108">Attributes</span></span>

|<span data-ttu-id="c15ba-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c15ba-109">**Attribute**</span></span>|<span data-ttu-id="c15ba-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c15ba-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c15ba-111">**TimeZoneName**</span><span class="sxs-lookup"><span data-stu-id="c15ba-111">**TimeZoneName**</span></span> <br/> |<span data-ttu-id="c15ba-112">Beschreibt den Namen der Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="c15ba-112">Describes the name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c15ba-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c15ba-113">Child elements</span></span>

|<span data-ttu-id="c15ba-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="c15ba-114">**Element**</span></span>|<span data-ttu-id="c15ba-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c15ba-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c15ba-116">Offset</span><span class="sxs-lookup"><span data-stu-id="c15ba-116">Offset</span></span>](offset.md) <br/> |<span data-ttu-id="c15ba-117">Beschreibt den Offset aus dem [BaseOffset](baseoffset.md).</span><span class="sxs-lookup"><span data-stu-id="c15ba-117">Describes the offset from the [BaseOffset](baseoffset.md).</span></span> <span data-ttu-id="c15ba-118">Der Basis Offset zusätzlich zu diesem Offset gibt die Zeit entsprechend der Standard-oder Sommerzeit an.</span><span class="sxs-lookup"><span data-stu-id="c15ba-118">The base offset in addition to this offset identifies the time according to whether it is standard or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="c15ba-119">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="c15ba-119">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="c15ba-120">Beschreibt ein relatives jährliches Serienmuster für ein Zeit Zonen Übergangs-Datumsmuster.</span><span class="sxs-lookup"><span data-stu-id="c15ba-120">Describes a relative yearly recurrence pattern for a time zone transition date pattern.</span></span>  <br/> |
|[<span data-ttu-id="c15ba-121">AbsoluteDate</span><span class="sxs-lookup"><span data-stu-id="c15ba-121">AbsoluteDate</span></span>](absolutedate.md) <br/> |<span data-ttu-id="c15ba-122">Stellt das Datum dar, an dem sich die Zeit von der Standard-oder Sommerzeit ändert.</span><span class="sxs-lookup"><span data-stu-id="c15ba-122">Represents the date when the time changes from standard or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="c15ba-123">Zeit (Time ChangeType)</span><span class="sxs-lookup"><span data-stu-id="c15ba-123">Time (TimeChangeType)</span></span>](time-timechangetype.md) <br/> |<span data-ttu-id="c15ba-124">Beschreibt die Zeit, zu der sich die Zeit zwischen Standardzeit und Sommerzeit ändert.</span><span class="sxs-lookup"><span data-stu-id="c15ba-124">Describes the time when the time changes between standard time and daylight saving time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c15ba-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c15ba-125">Parent elements</span></span>

|<span data-ttu-id="c15ba-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="c15ba-126">**Element**</span></span>|<span data-ttu-id="c15ba-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c15ba-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c15ba-128">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="c15ba-128">MeetingTimeZone</span></span>](meetingtimezone.md) <br/> |<span data-ttu-id="c15ba-129">Stellt die Zeitzone des Speicherorts dar, an dem die Besprechung gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="c15ba-129">Represents the time zone of the location where the meeting is hosted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c15ba-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c15ba-130">Remarks</span></span>

<span data-ttu-id="c15ba-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="c15ba-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c15ba-132">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c15ba-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c15ba-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="c15ba-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c15ba-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c15ba-134">Schema Name</span></span>  <br/> |<span data-ttu-id="c15ba-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c15ba-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="c15ba-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c15ba-136">Validation File</span></span>  <br/> |<span data-ttu-id="c15ba-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c15ba-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c15ba-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c15ba-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="c15ba-139">False</span><span class="sxs-lookup"><span data-stu-id="c15ba-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c15ba-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c15ba-140">See also</span></span>

- [<span data-ttu-id="c15ba-141">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c15ba-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

