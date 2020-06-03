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
description: Das period-Element definiert den Namen, den Zeit Offset und den eindeutigen Bezeichner für eine bestimmte Phase der Zeitzone.
ms.openlocfilehash: a7c36a9de01fd0484a7df75de3b5525992ef7ee7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459721"
---
# <a name="period"></a><span data-ttu-id="c1cb0-103">Punkt</span><span class="sxs-lookup"><span data-stu-id="c1cb0-103">Period</span></span>

<span data-ttu-id="c1cb0-104">Das **Period** -Element definiert den Namen, den Zeit Offset und den eindeutigen Bezeichner für eine bestimmte Phase der Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="c1cb0-104">The **Period** element defines the name, time offset, and unique identifier for a specific stage of the time zone.</span></span> 
  
```xml
<Period Bias="" Name="" Id=""/>
```

 <span data-ttu-id="c1cb0-105">**Periodtype**</span><span class="sxs-lookup"><span data-stu-id="c1cb0-105">**PeriodType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c1cb0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c1cb0-106">Attributes and elements</span></span>

<span data-ttu-id="c1cb0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c1cb0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1cb0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c1cb0-108">Attributes</span></span>

|<span data-ttu-id="c1cb0-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c1cb0-109">**Attribute**</span></span>|<span data-ttu-id="c1cb0-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1cb0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c1cb0-111">Bias</span><span class="sxs-lookup"><span data-stu-id="c1cb0-111">Bias</span></span>  <br/> |<span data-ttu-id="c1cb0-112">Ein xs: Duration-Wert, der den Zeit Offset der koordinierten Weltzeit (Coordinated Universal Time, UTC) für den Zeitraum darstellt.</span><span class="sxs-lookup"><span data-stu-id="c1cb0-112">An xs:duration value that represents the time offset from Coordinated Universal Time (UTC) for the period.</span></span>  <br/> |
|<span data-ttu-id="c1cb0-113">Name</span><span class="sxs-lookup"><span data-stu-id="c1cb0-113">Name</span></span>  <br/> |<span data-ttu-id="c1cb0-114">Ein String-Wert, der den beschreibenden Namen des Zeitraums darstellt.</span><span class="sxs-lookup"><span data-stu-id="c1cb0-114">A string value that represents the descriptive name of the period.</span></span>  <br/> |
|<span data-ttu-id="c1cb0-115">Id</span><span class="sxs-lookup"><span data-stu-id="c1cb0-115">Id</span></span>  <br/> |<span data-ttu-id="c1cb0-116">Ein String-Wert, der den Bezeichner für den Zeitraum darstellt.</span><span class="sxs-lookup"><span data-stu-id="c1cb0-116">A string value that represents the identifier for the period.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c1cb0-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1cb0-117">Child elements</span></span>

<span data-ttu-id="c1cb0-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="c1cb0-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c1cb0-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1cb0-119">Parent elements</span></span>

|<span data-ttu-id="c1cb0-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="c1cb0-120">**Element**</span></span>|<span data-ttu-id="c1cb0-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1cb0-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1cb0-122">Zeiten</span><span class="sxs-lookup"><span data-stu-id="c1cb0-122">Periods</span></span>](periods.md) <br/> |<span data-ttu-id="c1cb0-123">Stellt ein Array von Punkten dar, die den Zeit Offset in unterschiedlichen Phasen der Zeitzone definieren.</span><span class="sxs-lookup"><span data-stu-id="c1cb0-123">Represents an array of periods that define the time offset at different stages of the time zone.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c1cb0-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="c1cb0-124">Text value</span></span>

<span data-ttu-id="c1cb0-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="c1cb0-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c1cb0-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1cb0-126">Remarks</span></span>

<span data-ttu-id="c1cb0-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c1cb0-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1cb0-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c1cb0-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1cb0-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1cb0-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c1cb0-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c1cb0-130">Schema Name</span></span>  <br/> |<span data-ttu-id="c1cb0-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c1cb0-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="c1cb0-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c1cb0-132">Validation File</span></span>  <br/> |<span data-ttu-id="c1cb0-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c1cb0-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c1cb0-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c1cb0-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="c1cb0-135">False</span><span class="sxs-lookup"><span data-stu-id="c1cb0-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1cb0-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1cb0-136">See also</span></span>



- [<span data-ttu-id="c1cb0-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c1cb0-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

