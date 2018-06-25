---
title: Punkt
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Period
api_type:
- schema
ms.assetid: 2f9cf6af-c531-4d7d-90c9-1a1db504d890
description: Period-Element definiert die Namen sowie die Uhrzeitoffset und eindeutiger Bezeichner für eine bestimmte Phase der Zeitzone.
ms.openlocfilehash: 3b5d5877e6d9baffdfe536a0feec3b25b6d2883f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830726"
---
# <a name="period"></a><span data-ttu-id="aee93-103">Punkt</span><span class="sxs-lookup"><span data-stu-id="aee93-103">Period</span></span>

<span data-ttu-id="aee93-104">**Period** -Element definiert die Namen sowie die Uhrzeitoffset und eindeutiger Bezeichner für eine bestimmte Phase der Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="aee93-104">The **Period** element defines the name, time offset, and unique identifier for a specific stage of the time zone.</span></span> 
  
```xml
<Period Bias="" Name="" Id=""/>
```

 <span data-ttu-id="aee93-105">**PeriodType**</span><span class="sxs-lookup"><span data-stu-id="aee93-105">**PeriodType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aee93-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="aee93-106">Attributes and elements</span></span>

<span data-ttu-id="aee93-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="aee93-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aee93-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="aee93-108">Attributes</span></span>

|<span data-ttu-id="aee93-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="aee93-109">**Attribute**</span></span>|<span data-ttu-id="aee93-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aee93-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="aee93-111">Bias</span><span class="sxs-lookup"><span data-stu-id="aee93-111">Bias</span></span>  <br/> |<span data-ttu-id="aee93-112">Ein Duration-Wert, der den Uhrzeit-Offset für den Zeitraum von koordinierte Weltzeit (UTC) darstellt.</span><span class="sxs-lookup"><span data-stu-id="aee93-112">An xs:duration value that represents the time offset from Coordinated Universal Time (UTC) for the period.</span></span>  <br/> |
|<span data-ttu-id="aee93-113">Name</span><span class="sxs-lookup"><span data-stu-id="aee93-113">Name</span></span>  <br/> |<span data-ttu-id="aee93-114">Ein String-Wert, der den beschreibenden Namen des Zeitraums darstellt.</span><span class="sxs-lookup"><span data-stu-id="aee93-114">A string value that represents the descriptive name of the period.</span></span>  <br/> |
|<span data-ttu-id="aee93-115">Id</span><span class="sxs-lookup"><span data-stu-id="aee93-115">Id</span></span>  <br/> |<span data-ttu-id="aee93-116">Ein String-Wert, der den Bezeichner für den Zeitraum darstellt.</span><span class="sxs-lookup"><span data-stu-id="aee93-116">A string value that represents the identifier for the period.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="aee93-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aee93-117">Child elements</span></span>

<span data-ttu-id="aee93-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="aee93-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="aee93-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aee93-119">Parent elements</span></span>

|<span data-ttu-id="aee93-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="aee93-120">**Element**</span></span>|<span data-ttu-id="aee93-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aee93-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aee93-122">Perioden</span><span class="sxs-lookup"><span data-stu-id="aee93-122">Periods</span></span>](periods.md) <br/> |<span data-ttu-id="aee93-123">Stellt ein Array von Zeiträumen, mit die den Uhrzeit-Offset in verschiedenen Phasen der Zeitzone definiert.</span><span class="sxs-lookup"><span data-stu-id="aee93-123">Represents an array of periods that define the time offset at different stages of the time zone.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="aee93-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="aee93-124">Text value</span></span>

<span data-ttu-id="aee93-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="aee93-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aee93-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aee93-126">Remarks</span></span>

<span data-ttu-id="aee93-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="aee93-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aee93-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="aee93-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aee93-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="aee93-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="aee93-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="aee93-130">Schema Name</span></span>  <br/> |<span data-ttu-id="aee93-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="aee93-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="aee93-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="aee93-132">Validation File</span></span>  <br/> |<span data-ttu-id="aee93-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="aee93-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="aee93-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="aee93-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="aee93-135">False</span><span class="sxs-lookup"><span data-stu-id="aee93-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aee93-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aee93-136">See also</span></span>



- [<span data-ttu-id="aee93-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="aee93-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

