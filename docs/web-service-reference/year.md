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
description: Das Year-Element wird verwendet, um eine Zeitzone zu definieren, die sich je nach Jahr ändert. Dieses Element ist optional. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: cc83f9b2137f151f3f8ef0ceaf603ec036989961
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465170"
---
# <a name="year"></a><span data-ttu-id="e00d0-105">Jahr</span><span class="sxs-lookup"><span data-stu-id="e00d0-105">Year</span></span>

<span data-ttu-id="e00d0-106">Das **year** -Element wird verwendet, um eine Zeitzone zu definieren, die sich je nach Jahr ändert.</span><span class="sxs-lookup"><span data-stu-id="e00d0-106">The **Year** element is used to define a time zone that changes depending on the year.</span></span> <span data-ttu-id="e00d0-107">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="e00d0-107">This element is optional.</span></span> <span data-ttu-id="e00d0-108">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e00d0-108">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<Year/>
```

<span data-ttu-id="e00d0-109">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e00d0-109">**string**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="e00d0-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e00d0-110">Attributes and elements</span></span>

<span data-ttu-id="e00d0-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e00d0-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e00d0-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="e00d0-112">Attributes</span></span>

<span data-ttu-id="e00d0-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="e00d0-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e00d0-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e00d0-114">Child elements</span></span>

<span data-ttu-id="e00d0-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="e00d0-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e00d0-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e00d0-116">Parent elements</span></span>

|<span data-ttu-id="e00d0-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="e00d0-117">**Element**</span></span>|<span data-ttu-id="e00d0-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e00d0-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e00d0-119">Standard Time</span><span class="sxs-lookup"><span data-stu-id="e00d0-119">StandardTime</span></span>](standardtime.md) <br/> |<span data-ttu-id="e00d0-120">Stellt einen Offset von der Zeit relativ zur koordinierten Weltzeit (Coordinated Universal Time, UTC) dar, die durch das [Bias-Element (UTC)](bias-utc.md) dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e00d0-120">Represents an offset from the time relative to Coordinated Universal Time (UTC) that is represented by the [Bias (UTC)](bias-utc.md) element.</span></span>  <br/> |
|[<span data-ttu-id="e00d0-121">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="e00d0-121">DaylightTime</span></span>](daylighttime.md) <br/> |<span data-ttu-id="e00d0-122">Stellt einen Offset von der Zeit relativ zur koordinierten Weltzeit (Coordinated Universal Time, UTC) dar, die durch das [Bias-Element (UTC)](bias-utc.md) in Regionen dargestellt wird, in denen die Sommerzeit eingehaltenwird.</span><span class="sxs-lookup"><span data-stu-id="e00d0-122">Represents an offset from the time relative to Coordinated Universal Time (UTC) that is represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e00d0-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="e00d0-123">Text value</span></span>

<span data-ttu-id="e00d0-124">Das Year-Element akzeptiert eine Zeichenfolge, die ein Jahr darstellt.</span><span class="sxs-lookup"><span data-stu-id="e00d0-124">The Year element accepts a string that represents a year.</span></span> <span data-ttu-id="e00d0-125">Das Jahr Format ist YYYY.</span><span class="sxs-lookup"><span data-stu-id="e00d0-125">The year format is YYYY.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e00d0-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e00d0-126">Remarks</span></span>

<span data-ttu-id="e00d0-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="e00d0-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e00d0-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e00d0-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e00d0-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="e00d0-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e00d0-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e00d0-130">Schema Name</span></span>  <br/> |<span data-ttu-id="e00d0-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e00d0-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="e00d0-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e00d0-132">Validation File</span></span>  <br/> |<span data-ttu-id="e00d0-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e00d0-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e00d0-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e00d0-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="e00d0-135">False</span><span class="sxs-lookup"><span data-stu-id="e00d0-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e00d0-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e00d0-136">See also</span></span>

- [<span data-ttu-id="e00d0-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e00d0-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

