---
title: LegacyFreeBusyStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- LegacyFreeBusyStatus
api_type:
- schema
ms.assetid: ee5f3046-b79f-4f68-9455-1a688cee2745
description: Das LegacyFreeBusyStatus-Element darstellt, den Frei/Gebucht-Status des Kalenderelements.
ms.openlocfilehash: 681d7256dbef09c6c43d33ea1fc92b5d05e73a41
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830247"
---
# <a name="legacyfreebusystatus"></a><span data-ttu-id="ba3dd-103">LegacyFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="ba3dd-103">LegacyFreeBusyStatus</span></span>

<span data-ttu-id="ba3dd-104">Das **LegacyFreeBusyStatus** -Element darstellt, den Frei/Gebucht-Status des Kalenderelements.</span><span class="sxs-lookup"><span data-stu-id="ba3dd-104">The **LegacyFreeBusyStatus** element represents the free/busy status of the calendar item.</span></span> 
  
```xml
<LegacyFreeBusyStatus/>
```

<span data-ttu-id="ba3dd-105">**LegacyFreeBusyType**</span><span class="sxs-lookup"><span data-stu-id="ba3dd-105">**LegacyFreeBusyType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ba3dd-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ba3dd-106">Attributes and elements</span></span>

<span data-ttu-id="ba3dd-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ba3dd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba3dd-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ba3dd-108">Attributes</span></span>

<span data-ttu-id="ba3dd-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ba3dd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ba3dd-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ba3dd-110">Child elements</span></span>

<span data-ttu-id="ba3dd-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ba3dd-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ba3dd-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ba3dd-112">Parent elements</span></span>

|<span data-ttu-id="ba3dd-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ba3dd-113">**Element**</span></span>|<span data-ttu-id="ba3dd-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ba3dd-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba3dd-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="ba3dd-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="ba3dd-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="ba3dd-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="ba3dd-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="ba3dd-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="ba3dd-118">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="ba3dd-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ba3dd-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="ba3dd-119">Text value</span></span>

<span data-ttu-id="ba3dd-120">Es wird ein Textwert für dieses Element erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ba3dd-120">A text value is required for this element.</span></span> <span data-ttu-id="ba3dd-121">Es folgen die möglichen Textwerte für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="ba3dd-121">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="ba3dd-122">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="ba3dd-122">Free</span></span> 
- <span data-ttu-id="ba3dd-123">Mit Vorbehalt</span><span class="sxs-lookup"><span data-stu-id="ba3dd-123">Tentative</span></span>
- <span data-ttu-id="ba3dd-124">Gebucht</span><span class="sxs-lookup"><span data-stu-id="ba3dd-124">Busy</span></span>
- <span data-ttu-id="ba3dd-125">ABWESEND</span><span class="sxs-lookup"><span data-stu-id="ba3dd-125">OOF</span></span>
- <span data-ttu-id="ba3dd-126">WorkingElsewhere</span><span class="sxs-lookup"><span data-stu-id="ba3dd-126">WorkingElsewhere</span></span>
- <span data-ttu-id="ba3dd-127">NoData</span><span class="sxs-lookup"><span data-stu-id="ba3dd-127">NoData</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ba3dd-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba3dd-128">Remarks</span></span>

<span data-ttu-id="ba3dd-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ba3dd-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ba3dd-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ba3dd-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba3dd-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="ba3dd-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ba3dd-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ba3dd-132">Schema name</span></span>  <br/> |<span data-ttu-id="ba3dd-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ba3dd-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="ba3dd-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ba3dd-134">Validation file</span></span>  <br/> |<span data-ttu-id="ba3dd-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ba3dd-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ba3dd-136">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ba3dd-136">Can be empty</span></span>  <br/> |<span data-ttu-id="ba3dd-137">False</span><span class="sxs-lookup"><span data-stu-id="ba3dd-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba3dd-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba3dd-138">See also</span></span>

- [<span data-ttu-id="ba3dd-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ba3dd-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

