---
title: Tag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Day
api_type:
- schema
ms.assetid: d3b2dc66-486a-41d1-bff3-606f0bf92715
description: Das Day-Element stellt den Tag des Monats auf der erfolgt der Übergang zur Zeitzone.
ms.openlocfilehash: 01d1bf7833a89c0bb9a2b1af95ec8dfc627336d9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757872"
---
# <a name="day"></a><span data-ttu-id="c2d20-103">Tag</span><span class="sxs-lookup"><span data-stu-id="c2d20-103">Day</span></span>

<span data-ttu-id="c2d20-104">Das **Day** -Element stellt den Tag des Monats auf der erfolgt der Übergang zur Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="c2d20-104">The **Day** element represents the day of the month on which the time zone transition occurs.</span></span> 
  
```xml
<Day/>
```

<span data-ttu-id="c2d20-105">**int**</span><span class="sxs-lookup"><span data-stu-id="c2d20-105">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c2d20-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c2d20-106">Attributes and elements</span></span>

<span data-ttu-id="c2d20-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c2d20-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c2d20-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c2d20-108">Attributes</span></span>

<span data-ttu-id="c2d20-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c2d20-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c2d20-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c2d20-110">Child elements</span></span>

<span data-ttu-id="c2d20-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="c2d20-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c2d20-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c2d20-112">Parent elements</span></span>

|<span data-ttu-id="c2d20-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c2d20-113">**Element**</span></span>|<span data-ttu-id="c2d20-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c2d20-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c2d20-115">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="c2d20-115">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="c2d20-116">Stellt einen Zeitzone Übergang dar, der einem bestimmten Datum pro Jahr auftritt.</span><span class="sxs-lookup"><span data-stu-id="c2d20-116">Represents a time zone transition that occurs on a specific date each year.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c2d20-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="c2d20-117">Text value</span></span>

<span data-ttu-id="c2d20-118">Der Textwert der **Day** -Element ist eine ganze Zahl, die den Tag des Monats darstellt, auf dem der Übergang zur Zeitzone auftritt.</span><span class="sxs-lookup"><span data-stu-id="c2d20-118">The text value of the **Day** element is an integer that represents the day of the month on which the time zone transition occurs.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c2d20-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c2d20-119">Remarks</span></span>

<span data-ttu-id="c2d20-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c2d20-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c2d20-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c2d20-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c2d20-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="c2d20-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c2d20-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c2d20-123">Schema Name</span></span>  <br/> |<span data-ttu-id="c2d20-124">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c2d20-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="c2d20-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c2d20-125">Validation File</span></span>  <br/> |<span data-ttu-id="c2d20-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c2d20-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c2d20-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c2d20-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="c2d20-128">False</span><span class="sxs-lookup"><span data-stu-id="c2d20-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c2d20-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2d20-129">See also</span></span>

- [<span data-ttu-id="c2d20-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c2d20-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

