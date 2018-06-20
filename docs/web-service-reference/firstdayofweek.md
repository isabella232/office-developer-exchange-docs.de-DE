---
title: FirstDayOfWeek
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FirstDayOfWeek
api_type:
- schema
ms.assetid: d6cf1bd3-a19b-4d5f-9e25-8e337a4939e0
description: Das FirstDayOfWeek-Element gibt den ersten Tag der Woche.
ms.openlocfilehash: 99858d17213d077ce7c51ad1c746588f2f3939a7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758486"
---
# <a name="firstdayofweek"></a><span data-ttu-id="ad196-103">FirstDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="ad196-103">FirstDayOfWeek</span></span>

<span data-ttu-id="ad196-104">Das **FirstDayOfWeek** -Element gibt den ersten Tag der Woche.</span><span class="sxs-lookup"><span data-stu-id="ad196-104">The **FirstDayOfWeek** element specifies the first day of the week.</span></span> 
  
```XML
<FirstDayOfWeek> Sunday | Monday | Tuesday | Wednesday | Thursday | Friday | Saturday</FirstDayOfWeek>
```

 <span data-ttu-id="ad196-105">**DayOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="ad196-105">**DayOfWeekType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ad196-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ad196-106">Attributes and elements</span></span>

<span data-ttu-id="ad196-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ad196-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ad196-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ad196-108">Attributes</span></span>

<span data-ttu-id="ad196-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ad196-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ad196-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ad196-110">Child elements</span></span>

<span data-ttu-id="ad196-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ad196-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ad196-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ad196-112">Parent elements</span></span>

|<span data-ttu-id="ad196-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ad196-113">**Element**</span></span>|<span data-ttu-id="ad196-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad196-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ad196-115">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="ad196-115">WeeklyRecurrence</span></span>](weeklyrecurrence.md) <br/> |<span data-ttu-id="ad196-116">Beschreibt ein wöchentliches Serienmuster.</span><span class="sxs-lookup"><span data-stu-id="ad196-116">Describes a weekly recurrence pattern.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ad196-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="ad196-117">Text value</span></span>

<span data-ttu-id="ad196-118">Der Textwert der **FirstDayOfWeek** -Element gibt an, welche den Wochentag als der erste Tag der Woche verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ad196-118">The text value of the **FirstDayOfWeek** element indicates which day of the week is used as the first day of the week.</span></span> <span data-ttu-id="ad196-119">Im folgenden sind die möglichen Textwerte:</span><span class="sxs-lookup"><span data-stu-id="ad196-119">The following are the possible text values:</span></span> 
  
- <span data-ttu-id="ad196-120">Sonntag</span><span class="sxs-lookup"><span data-stu-id="ad196-120">Sunday</span></span>
    
- <span data-ttu-id="ad196-121">Montag</span><span class="sxs-lookup"><span data-stu-id="ad196-121">Monday</span></span>
    
- <span data-ttu-id="ad196-122">Dienstag</span><span class="sxs-lookup"><span data-stu-id="ad196-122">Tuesday</span></span>
    
- <span data-ttu-id="ad196-123">Mittwoch</span><span class="sxs-lookup"><span data-stu-id="ad196-123">Wednesday</span></span>
    
- <span data-ttu-id="ad196-124">Donnerstag</span><span class="sxs-lookup"><span data-stu-id="ad196-124">Thursday</span></span>
    
- <span data-ttu-id="ad196-125">Freitag</span><span class="sxs-lookup"><span data-stu-id="ad196-125">Friday</span></span>
    
- <span data-ttu-id="ad196-126">Samstag</span><span class="sxs-lookup"><span data-stu-id="ad196-126">Saturday</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ad196-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ad196-127">Remarks</span></span>

<span data-ttu-id="ad196-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ad196-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ad196-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ad196-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad196-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="ad196-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ad196-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ad196-131">Schema Name</span></span>  <br/> |<span data-ttu-id="ad196-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ad196-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="ad196-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ad196-133">Validation File</span></span>  <br/> |<span data-ttu-id="ad196-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ad196-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ad196-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ad196-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="ad196-136">False</span><span class="sxs-lookup"><span data-stu-id="ad196-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ad196-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad196-137">See also</span></span>



- [<span data-ttu-id="ad196-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ad196-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

