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
description: Das IsAllDayEvent-Element gibt an, ob ein Kalenderelement oder eine Besprechungsanfrage ein ganztägiges Ereignis darstellt.
ms.openlocfilehash: f0c975deecf96e94599a47ef2c33e54a7d1a80b9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526536"
---
# <a name="isalldayevent"></a><span data-ttu-id="3251c-103">IsAllDayEvent</span><span class="sxs-lookup"><span data-stu-id="3251c-103">IsAllDayEvent</span></span>

<span data-ttu-id="3251c-104">Das **IsAllDayEvent** -Element gibt an, ob ein Kalenderelement oder eine Besprechungsanfrage ein ganztägiges Ereignis darstellt.</span><span class="sxs-lookup"><span data-stu-id="3251c-104">The **IsAllDayEvent** element indicates whether a calendar item or meeting request represents an all-day event.</span></span> 
  
```xml
<IsAllDayEvent/>
```

 <span data-ttu-id="3251c-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="3251c-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3251c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3251c-106">Attributes and elements</span></span>

<span data-ttu-id="3251c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3251c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3251c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3251c-108">Attributes</span></span>

<span data-ttu-id="3251c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3251c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3251c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3251c-110">Child elements</span></span>

<span data-ttu-id="3251c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="3251c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3251c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3251c-112">Parent elements</span></span>

|<span data-ttu-id="3251c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3251c-113">**Element**</span></span>|<span data-ttu-id="3251c-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3251c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3251c-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="3251c-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="3251c-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="3251c-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="3251c-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="3251c-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="3251c-118">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="3251c-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3251c-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="3251c-119">Text value</span></span>

<span data-ttu-id="3251c-120">Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich, wenn dieses Element enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="3251c-120">A text value that represents a Boolean value is required if this element is included.</span></span> <span data-ttu-id="3251c-121">Der Wert **true** gibt an, dass das Element ein ganztägiges Ereignis darstellt.</span><span class="sxs-lookup"><span data-stu-id="3251c-121">A value of **true** indicates that the item represents an all-day event.</span></span> <span data-ttu-id="3251c-122">Der Wert **false** gibt an, dass das Element weniger als die Arbeitszeiten eines Benutzers umfasst.</span><span class="sxs-lookup"><span data-stu-id="3251c-122">A value of **false** indicates that the item spans less than a user's working hours.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3251c-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3251c-123">Remarks</span></span>

<span data-ttu-id="3251c-124">Ein ganztägiges Ereignis umfasst die Dauer der Arbeitsstunden, die für ein Postfach definiert ist.</span><span class="sxs-lookup"><span data-stu-id="3251c-124">An all-day event spans the duration of working hours that is defined for a mailbox.</span></span>
  
<span data-ttu-id="3251c-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="3251c-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3251c-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3251c-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3251c-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="3251c-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3251c-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3251c-128">Schema name</span></span>  <br/> |<span data-ttu-id="3251c-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3251c-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="3251c-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3251c-130">Validation file</span></span>  <br/> |<span data-ttu-id="3251c-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3251c-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3251c-132">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="3251c-132">Can be empty</span></span>  <br/> |<span data-ttu-id="3251c-133">False</span><span class="sxs-lookup"><span data-stu-id="3251c-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3251c-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3251c-134">See also</span></span>



- [<span data-ttu-id="3251c-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3251c-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

