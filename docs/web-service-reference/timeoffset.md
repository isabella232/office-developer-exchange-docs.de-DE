---
title: Offset
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeOffset
api_type:
- schema
ms.assetid: b70bf498-cc3a-4fa6-8236-514acb973b33
description: Das Time Offset-Element stellt den Zeitversatz zwischen der koordinierten Weltzeit (Coordinated Universal Time, UTC) für den Zeitzonenübergang dar.
ms.openlocfilehash: 8cfd43477f0548227204da9ebc6d7e9307786845
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460288"
---
# <a name="timeoffset"></a><span data-ttu-id="14492-103">Offset</span><span class="sxs-lookup"><span data-stu-id="14492-103">TimeOffset</span></span>

<span data-ttu-id="14492-104">Das Time **Offset** -Element stellt den Zeitversatz zwischen der koordinierten Weltzeit (Coordinated Universal Time, UTC) für den Zeitzonenübergang dar.</span><span class="sxs-lookup"><span data-stu-id="14492-104">The **TimeOffset** element represents the time offset from Coordinated Universal Time (UTC) for the time zone transition.</span></span> 
  
```XML
<TimeOffset/>
```

 <span data-ttu-id="14492-105">**duration**</span><span class="sxs-lookup"><span data-stu-id="14492-105">**duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="14492-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="14492-106">Attributes and elements</span></span>

<span data-ttu-id="14492-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="14492-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="14492-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="14492-108">Attributes</span></span>

<span data-ttu-id="14492-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="14492-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="14492-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="14492-110">Child elements</span></span>

<span data-ttu-id="14492-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="14492-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="14492-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="14492-112">Parent elements</span></span>

|<span data-ttu-id="14492-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="14492-113">**Element**</span></span>|<span data-ttu-id="14492-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="14492-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="14492-115">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="14492-115">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="14492-116">Stellt einen Zeitzonenübergang dar, der jedes Jahr an einem bestimmten Datum auftritt.</span><span class="sxs-lookup"><span data-stu-id="14492-116">Represents a time zone transition that occurs on a specific date each year.</span></span>  <br/> |
|[<span data-ttu-id="14492-117">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="14492-117">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="14492-118">Stellt einen Zeitzonenübergang dar, der an demselben Tag jedes Jahr erfolgt.</span><span class="sxs-lookup"><span data-stu-id="14492-118">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="14492-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="14492-119">Text value</span></span>

<span data-ttu-id="14492-120">Der Textwert des Time **Offset** -Elements ist eine Dauer, die den Zeitversatz von UTC für den Zeitzonenübergang angibt.</span><span class="sxs-lookup"><span data-stu-id="14492-120">The text value of the **TimeOffset** element is a duration that specifies the time offset from UTC for the time zone transition.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="14492-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14492-121">Remarks</span></span>

<span data-ttu-id="14492-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="14492-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="14492-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="14492-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="14492-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="14492-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="14492-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="14492-125">Schema Name</span></span>  <br/> |<span data-ttu-id="14492-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="14492-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="14492-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="14492-127">Validation File</span></span>  <br/> |<span data-ttu-id="14492-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="14492-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="14492-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="14492-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="14492-130">False</span><span class="sxs-lookup"><span data-stu-id="14492-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="14492-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14492-131">See also</span></span>



- [<span data-ttu-id="14492-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="14492-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

