---
title: TimeOffset
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
description: Das TimeOffset-Element stellt Offset der von der koordinierten Weltzeit (UTC) für den Übergang zur Zeitzone dar.
ms.openlocfilehash: 46b1b2c8eec9bae871b4dafe43036e9d725075ae
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839189"
---
# <a name="timeoffset"></a><span data-ttu-id="26a32-103">TimeOffset</span><span class="sxs-lookup"><span data-stu-id="26a32-103">TimeOffset</span></span>

<span data-ttu-id="26a32-104">Das **TimeOffset** -Element stellt Offset der von der koordinierten Weltzeit (UTC) für den Übergang zur Zeitzone dar.</span><span class="sxs-lookup"><span data-stu-id="26a32-104">The **TimeOffset** element represents the time offset from Coordinated Universal Time (UTC) for the time zone transition.</span></span> 
  
```XML
<TimeOffset/>
```

 <span data-ttu-id="26a32-105">**duration**</span><span class="sxs-lookup"><span data-stu-id="26a32-105">**duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="26a32-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="26a32-106">Attributes and elements</span></span>

<span data-ttu-id="26a32-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="26a32-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="26a32-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="26a32-108">Attributes</span></span>

<span data-ttu-id="26a32-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="26a32-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="26a32-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="26a32-110">Child elements</span></span>

<span data-ttu-id="26a32-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="26a32-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="26a32-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="26a32-112">Parent elements</span></span>

|<span data-ttu-id="26a32-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="26a32-113">**Element**</span></span>|<span data-ttu-id="26a32-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="26a32-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26a32-115">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="26a32-115">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="26a32-116">Stellt einen Zeitzone Übergang dar, der einem bestimmten Datum pro Jahr auftritt.</span><span class="sxs-lookup"><span data-stu-id="26a32-116">Represents a time zone transition that occurs on a specific date each year.</span></span>  <br/> |
|[<span data-ttu-id="26a32-117">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="26a32-117">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="26a32-118">Stellt einen Zeitzone Übergang dar, bei dem gleichen Tag pro Jahr auftritt.</span><span class="sxs-lookup"><span data-stu-id="26a32-118">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="26a32-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="26a32-119">Text value</span></span>

<span data-ttu-id="26a32-120">Der Textwert der **TimeOffset** -Element wird eine Dauer, die UTC-Zeitoffset für den Übergang zur Zeitzone angibt.</span><span class="sxs-lookup"><span data-stu-id="26a32-120">The text value of the **TimeOffset** element is a duration that specifies the time offset from UTC for the time zone transition.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="26a32-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="26a32-121">Remarks</span></span>

<span data-ttu-id="26a32-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="26a32-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="26a32-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="26a32-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26a32-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="26a32-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="26a32-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="26a32-125">Schema Name</span></span>  <br/> |<span data-ttu-id="26a32-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="26a32-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="26a32-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="26a32-127">Validation File</span></span>  <br/> |<span data-ttu-id="26a32-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="26a32-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="26a32-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="26a32-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="26a32-130">False</span><span class="sxs-lookup"><span data-stu-id="26a32-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="26a32-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26a32-131">See also</span></span>



- [<span data-ttu-id="26a32-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="26a32-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

