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
description: Das FirstDayOfWeek-Element gibt den ersten Tag der Woche an.
ms.openlocfilehash: 1b4aee8e1ce2548cd6b0047623b0bcda47ad316b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530972"
---
# <a name="firstdayofweek"></a><span data-ttu-id="efc63-103">FirstDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="efc63-103">FirstDayOfWeek</span></span>

<span data-ttu-id="efc63-104">Das **FirstDayOfWeek** -Element gibt den ersten Tag der Woche an.</span><span class="sxs-lookup"><span data-stu-id="efc63-104">The **FirstDayOfWeek** element specifies the first day of the week.</span></span> 
  
```XML
<FirstDayOfWeek> Sunday | Monday | Tuesday | Wednesday | Thursday | Friday | Saturday</FirstDayOfWeek>
```

 <span data-ttu-id="efc63-105">**Dayofweektype**</span><span class="sxs-lookup"><span data-stu-id="efc63-105">**DayOfWeekType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="efc63-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="efc63-106">Attributes and elements</span></span>

<span data-ttu-id="efc63-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="efc63-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="efc63-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="efc63-108">Attributes</span></span>

<span data-ttu-id="efc63-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="efc63-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="efc63-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="efc63-110">Child elements</span></span>

<span data-ttu-id="efc63-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="efc63-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="efc63-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="efc63-112">Parent elements</span></span>

|<span data-ttu-id="efc63-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="efc63-113">**Element**</span></span>|<span data-ttu-id="efc63-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="efc63-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="efc63-115">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="efc63-115">WeeklyRecurrence</span></span>](weeklyrecurrence.md) <br/> |<span data-ttu-id="efc63-116">Beschreibt ein wöchentliches Serienmuster.</span><span class="sxs-lookup"><span data-stu-id="efc63-116">Describes a weekly recurrence pattern.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="efc63-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="efc63-117">Text value</span></span>

<span data-ttu-id="efc63-118">Der Textwert des **FirstDayOfWeek** -Elements gibt an, welcher Wochentag als erster Tag der Woche verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="efc63-118">The text value of the **FirstDayOfWeek** element indicates which day of the week is used as the first day of the week.</span></span> <span data-ttu-id="efc63-119">Im folgenden sind die möglichen Text Werte zu finden:</span><span class="sxs-lookup"><span data-stu-id="efc63-119">The following are the possible text values:</span></span> 
  
- <span data-ttu-id="efc63-120">Sonntag</span><span class="sxs-lookup"><span data-stu-id="efc63-120">Sunday</span></span>
    
- <span data-ttu-id="efc63-121">Montag</span><span class="sxs-lookup"><span data-stu-id="efc63-121">Monday</span></span>
    
- <span data-ttu-id="efc63-122">Dienstag</span><span class="sxs-lookup"><span data-stu-id="efc63-122">Tuesday</span></span>
    
- <span data-ttu-id="efc63-123">Mittwoch</span><span class="sxs-lookup"><span data-stu-id="efc63-123">Wednesday</span></span>
    
- <span data-ttu-id="efc63-124">Donnerstag</span><span class="sxs-lookup"><span data-stu-id="efc63-124">Thursday</span></span>
    
- <span data-ttu-id="efc63-125">Freitag</span><span class="sxs-lookup"><span data-stu-id="efc63-125">Friday</span></span>
    
- <span data-ttu-id="efc63-126">Samstag</span><span class="sxs-lookup"><span data-stu-id="efc63-126">Saturday</span></span>
    
## <a name="remarks"></a><span data-ttu-id="efc63-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="efc63-127">Remarks</span></span>

<span data-ttu-id="efc63-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="efc63-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="efc63-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="efc63-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="efc63-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="efc63-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="efc63-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="efc63-131">Schema Name</span></span>  <br/> |<span data-ttu-id="efc63-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="efc63-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="efc63-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="efc63-133">Validation File</span></span>  <br/> |<span data-ttu-id="efc63-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="efc63-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="efc63-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="efc63-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="efc63-136">False</span><span class="sxs-lookup"><span data-stu-id="efc63-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="efc63-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="efc63-137">See also</span></span>



- [<span data-ttu-id="efc63-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="efc63-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

