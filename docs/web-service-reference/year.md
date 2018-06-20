---
title: Jahr
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Year
api_type:
- schema
ms.assetid: 93bf2847-53fa-496c-9a1e-dc9a9ffd0b9f
description: Das Jahr-Element wird verwendet, um eine Zeitzone definiert, die sich je nach dem Jahr ändern. Dieses Element ist optional. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 95d75f9c6166fc26e86534346fb07292a7fb3dcd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839565"
---
# <a name="year"></a><span data-ttu-id="be6bb-105">Jahr</span><span class="sxs-lookup"><span data-stu-id="be6bb-105">Year</span></span>

<span data-ttu-id="be6bb-106">Das **Jahr** -Element wird verwendet, um eine Zeitzone definiert, die sich je nach dem Jahr ändern.</span><span class="sxs-lookup"><span data-stu-id="be6bb-106">The **Year** element is used to define a time zone that changes depending on the year.</span></span> <span data-ttu-id="be6bb-107">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="be6bb-107">This element is optional.</span></span> <span data-ttu-id="be6bb-108">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="be6bb-108">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<Year/>
```

<span data-ttu-id="be6bb-109">**string**</span><span class="sxs-lookup"><span data-stu-id="be6bb-109">**string**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="be6bb-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="be6bb-110">Attributes and elements</span></span>

<span data-ttu-id="be6bb-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="be6bb-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="be6bb-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="be6bb-112">Attributes</span></span>

<span data-ttu-id="be6bb-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="be6bb-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="be6bb-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="be6bb-114">Child elements</span></span>

<span data-ttu-id="be6bb-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="be6bb-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="be6bb-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="be6bb-116">Parent elements</span></span>

|<span data-ttu-id="be6bb-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="be6bb-117">**Element**</span></span>|<span data-ttu-id="be6bb-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="be6bb-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="be6bb-119">StandardTime</span><span class="sxs-lookup"><span data-stu-id="be6bb-119">StandardTime</span></span>](standardtime.md) <br/> |<span data-ttu-id="be6bb-120">Stellt einen Abstand von dem Zeitpunkt relativ zur koordinierten Weltzeit (UTC), die durch die [Verschiebung (UTC)](bias-utc.md) Element dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="be6bb-120">Represents an offset from the time relative to Coordinated Universal Time (UTC) that is represented by the [Bias (UTC)](bias-utc.md) element.</span></span>  <br/> |
|[<span data-ttu-id="be6bb-121">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="be6bb-121">DaylightTime</span></span>](daylighttime.md) <br/> |<span data-ttu-id="be6bb-122">Stellt einen Abstand von dem Zeitpunkt relativ zur koordinierten Weltzeit (UTC), die durch die [Verschiebung (UTC)](bias-utc.md) Element Regionen dargestellt wird, in dem Sommerzeit beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="be6bb-122">Represents an offset from the time relative to Coordinated Universal Time (UTC) that is represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="be6bb-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="be6bb-123">Text value</span></span>

<span data-ttu-id="be6bb-124">Das Jahr-Element akzeptiert eine Zeichenfolge, die ein Jahr darstellt.</span><span class="sxs-lookup"><span data-stu-id="be6bb-124">The Year element accepts a string that represents a year.</span></span> <span data-ttu-id="be6bb-125">Das Jahresformat ist YYYY.</span><span class="sxs-lookup"><span data-stu-id="be6bb-125">The year format is YYYY.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="be6bb-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="be6bb-126">Remarks</span></span>

<span data-ttu-id="be6bb-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="be6bb-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="be6bb-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="be6bb-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="be6bb-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="be6bb-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="be6bb-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="be6bb-130">Schema Name</span></span>  <br/> |<span data-ttu-id="be6bb-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="be6bb-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="be6bb-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="be6bb-132">Validation File</span></span>  <br/> |<span data-ttu-id="be6bb-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="be6bb-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="be6bb-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="be6bb-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="be6bb-135">False</span><span class="sxs-lookup"><span data-stu-id="be6bb-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="be6bb-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be6bb-136">See also</span></span>

- [<span data-ttu-id="be6bb-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="be6bb-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

