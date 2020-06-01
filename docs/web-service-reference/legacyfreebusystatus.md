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
description: Das LegacyFreeBusyStatus-Element stellt den Frei/Gebucht-Status des Kalenderelements dar.
ms.openlocfilehash: ecbcae0862c9c02c0a4a61012816e4c2c6ea07b7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463230"
---
# <a name="legacyfreebusystatus"></a><span data-ttu-id="f969a-103">LegacyFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="f969a-103">LegacyFreeBusyStatus</span></span>

<span data-ttu-id="f969a-104">Das **LegacyFreeBusyStatus** -Element stellt den Frei/Gebucht-Status des Kalenderelements dar.</span><span class="sxs-lookup"><span data-stu-id="f969a-104">The **LegacyFreeBusyStatus** element represents the free/busy status of the calendar item.</span></span> 
  
```xml
<LegacyFreeBusyStatus/>
```

<span data-ttu-id="f969a-105">**LegacyFreeBusyType**</span><span class="sxs-lookup"><span data-stu-id="f969a-105">**LegacyFreeBusyType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f969a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f969a-106">Attributes and elements</span></span>

<span data-ttu-id="f969a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f969a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f969a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f969a-108">Attributes</span></span>

<span data-ttu-id="f969a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f969a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f969a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f969a-110">Child elements</span></span>

<span data-ttu-id="f969a-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="f969a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f969a-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f969a-112">Parent elements</span></span>

|<span data-ttu-id="f969a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f969a-113">**Element**</span></span>|<span data-ttu-id="f969a-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f969a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f969a-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="f969a-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="f969a-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="f969a-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="f969a-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="f969a-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="f969a-118">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="f969a-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f969a-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="f969a-119">Text value</span></span>

<span data-ttu-id="f969a-120">Für dieses Element ist ein Textwert erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f969a-120">A text value is required for this element.</span></span> <span data-ttu-id="f969a-121">Im folgenden sind die möglichen Text Werte für dieses Element angegeben:</span><span class="sxs-lookup"><span data-stu-id="f969a-121">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="f969a-122">Frei</span><span class="sxs-lookup"><span data-stu-id="f969a-122">Free</span></span> 
- <span data-ttu-id="f969a-123">Vorläufige</span><span class="sxs-lookup"><span data-stu-id="f969a-123">Tentative</span></span>
- <span data-ttu-id="f969a-124">Gebucht</span><span class="sxs-lookup"><span data-stu-id="f969a-124">Busy</span></span>
- <span data-ttu-id="f969a-125">Abwesenheits</span><span class="sxs-lookup"><span data-stu-id="f969a-125">OOF</span></span>
- <span data-ttu-id="f969a-126">WorkingElsewhere</span><span class="sxs-lookup"><span data-stu-id="f969a-126">WorkingElsewhere</span></span>
- <span data-ttu-id="f969a-127">NoData</span><span class="sxs-lookup"><span data-stu-id="f969a-127">NoData</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f969a-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f969a-128">Remarks</span></span>

<span data-ttu-id="f969a-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="f969a-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f969a-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f969a-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f969a-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="f969a-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f969a-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f969a-132">Schema name</span></span>  <br/> |<span data-ttu-id="f969a-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f969a-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="f969a-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f969a-134">Validation file</span></span>  <br/> |<span data-ttu-id="f969a-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f969a-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f969a-136">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f969a-136">Can be empty</span></span>  <br/> |<span data-ttu-id="f969a-137">False</span><span class="sxs-lookup"><span data-stu-id="f969a-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f969a-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f969a-138">See also</span></span>

- [<span data-ttu-id="f969a-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f969a-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

