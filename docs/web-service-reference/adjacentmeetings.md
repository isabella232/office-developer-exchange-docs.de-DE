---
title: AdjacentMeetings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AdjacentMeetings
api_type:
- schema
ms.assetid: 50a9c381-9166-476e-8421-29e51b94499b
description: Das AdjacentMeetings-Element identifiziert alle Kalenderelemente, die an eine Besprechungszeit angrenzen.
ms.openlocfilehash: 9ab818f4f67c32c01101cc595ccb92424a872ef0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757244"
---
# <a name="adjacentmeetings"></a><span data-ttu-id="7a081-103">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="7a081-103">AdjacentMeetings</span></span>

<span data-ttu-id="7a081-104">Das **AdjacentMeetings** -Element identifiziert alle Kalenderelemente, die an eine Besprechungszeit angrenzen.</span><span class="sxs-lookup"><span data-stu-id="7a081-104">The **AdjacentMeetings** element identifies all calendar items that are adjacent to a meeting time.</span></span> 
  
```xml
<AdjacentMeetings>
   <CalendarItem/>
</AdjacentMeetings>
```

 <span data-ttu-id="7a081-105">**NonEmptyArrayOfAllItemsType**</span><span class="sxs-lookup"><span data-stu-id="7a081-105">**NonEmptyArrayOfAllItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7a081-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7a081-106">Attributes and elements</span></span>

<span data-ttu-id="7a081-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7a081-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7a081-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7a081-108">Attributes</span></span>

<span data-ttu-id="7a081-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7a081-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7a081-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7a081-110">Child elements</span></span>

|<span data-ttu-id="7a081-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="7a081-111">**Element**</span></span>|<span data-ttu-id="7a081-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7a081-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a081-113">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="7a081-113">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="7a081-114">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="7a081-114">Represents an Exchange calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7a081-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7a081-115">Parent elements</span></span>

|<span data-ttu-id="7a081-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="7a081-116">**Element**</span></span>|<span data-ttu-id="7a081-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7a081-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a081-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="7a081-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="7a081-119">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="7a081-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="7a081-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="7a081-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="7a081-121">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="7a081-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a081-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7a081-122">Remarks</span></span>

<span data-ttu-id="7a081-123">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7a081-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7a081-124">Obwohl weitere untergeordnete Elemente pro das Schema gültig sind, ist das [CalendarItem](calendaritem.md) -Element das einzige untergeordnete Element, bei dem Exchange-Webdienste (EWS) innerhalb des Elements **AdjacentMeetings** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7a081-124">Although additional child elements are valid per the schema, the [CalendarItem](calendaritem.md) element is the only child element that Exchange Web Services (EWS) will return within the **AdjacentMeetings** element.</span></span> <span data-ttu-id="7a081-125">In diesem Thema wird keine untergeordneten Elemente aufgelistet, die dem Schema gültig sind, aber nicht von EWS zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7a081-125">This topic does not list child elements that are valid per the schema but will not be returned by EWS.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="7a081-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7a081-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7a081-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="7a081-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7a081-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7a081-128">Schema Name</span></span>  <br/> |<span data-ttu-id="7a081-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7a081-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="7a081-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7a081-130">Validation File</span></span>  <br/> |<span data-ttu-id="7a081-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7a081-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7a081-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7a081-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="7a081-133">False</span><span class="sxs-lookup"><span data-stu-id="7a081-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7a081-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a081-134">See also</span></span>

- [<span data-ttu-id="7a081-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7a081-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

