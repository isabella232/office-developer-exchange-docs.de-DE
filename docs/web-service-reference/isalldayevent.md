---
title: IsAllDayEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsAllDayEvent
api_type:
- schema
ms.assetid: 29140a64-9d7a-4a14-a10d-c98197c9831b
description: Das IsAllDayEvent-Element gibt an, ob ein Kalender-Elements oder einer Besprechungsanfrage ein ganztägiges Ereignis darstellt.
ms.openlocfilehash: 81cf1e7d8338275540f264de7cbf194005e7770c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829983"
---
# <a name="isalldayevent"></a><span data-ttu-id="a38b8-103">IsAllDayEvent</span><span class="sxs-lookup"><span data-stu-id="a38b8-103">IsAllDayEvent</span></span>

<span data-ttu-id="a38b8-104">Das **IsAllDayEvent** -Element gibt an, ob ein Kalender-Elements oder einer Besprechungsanfrage ein ganztägiges Ereignis darstellt.</span><span class="sxs-lookup"><span data-stu-id="a38b8-104">The **IsAllDayEvent** element indicates whether a calendar item or meeting request represents an all-day event.</span></span> 
  
```xml
<IsAllDayEvent/>
```

 <span data-ttu-id="a38b8-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a38b8-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a38b8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a38b8-106">Attributes and elements</span></span>

<span data-ttu-id="a38b8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a38b8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a38b8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a38b8-108">Attributes</span></span>

<span data-ttu-id="a38b8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a38b8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a38b8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a38b8-110">Child elements</span></span>

<span data-ttu-id="a38b8-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="a38b8-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a38b8-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a38b8-112">Parent elements</span></span>

|<span data-ttu-id="a38b8-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a38b8-113">**Element**</span></span>|<span data-ttu-id="a38b8-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a38b8-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a38b8-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="a38b8-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="a38b8-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="a38b8-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="a38b8-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="a38b8-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="a38b8-118">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="a38b8-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a38b8-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="a38b8-119">Text value</span></span>

<span data-ttu-id="a38b8-120">Ein Textwert, der einen booleschen Wert darstellt ist erforderlich, wenn dieses Element enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="a38b8-120">A text value that represents a Boolean value is required if this element is included.</span></span> <span data-ttu-id="a38b8-121">Der Wert **true** gibt an, dass das Element ein ganztägiges Ereignis darstellt.</span><span class="sxs-lookup"><span data-stu-id="a38b8-121">A value of **true** indicates that the item represents an all-day event.</span></span> <span data-ttu-id="a38b8-122">Der Wert **false** gibt an, dass das Element kleiner als Arbeitsstunden des Benutzers umfasst.</span><span class="sxs-lookup"><span data-stu-id="a38b8-122">A value of **false** indicates that the item spans less than a user's working hours.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a38b8-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a38b8-123">Remarks</span></span>

<span data-ttu-id="a38b8-124">Ein ganztägiges Ereignis erstreckt sich über die Dauer der Arbeitsstunden, die definiert ist für ein Postfach aus.</span><span class="sxs-lookup"><span data-stu-id="a38b8-124">An all-day event spans the duration of working hours that is defined for a mailbox.</span></span>
  
<span data-ttu-id="a38b8-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="a38b8-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a38b8-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a38b8-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a38b8-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="a38b8-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a38b8-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a38b8-128">Schema name</span></span>  <br/> |<span data-ttu-id="a38b8-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a38b8-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="a38b8-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a38b8-130">Validation file</span></span>  <br/> |<span data-ttu-id="a38b8-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a38b8-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a38b8-132">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a38b8-132">Can be empty</span></span>  <br/> |<span data-ttu-id="a38b8-133">False</span><span class="sxs-lookup"><span data-stu-id="a38b8-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a38b8-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a38b8-134">See also</span></span>



- [<span data-ttu-id="a38b8-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a38b8-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

