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
ms.openlocfilehash: 7c89095e24af799df22a848be06a0fd65d53be7f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463580"
---
# <a name="adjacentmeetings"></a><span data-ttu-id="1f142-103">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="1f142-103">AdjacentMeetings</span></span>

<span data-ttu-id="1f142-104">Das **AdjacentMeetings** -Element identifiziert alle Kalenderelemente, die an eine Besprechungszeit angrenzen.</span><span class="sxs-lookup"><span data-stu-id="1f142-104">The **AdjacentMeetings** element identifies all calendar items that are adjacent to a meeting time.</span></span> 
  
```xml
<AdjacentMeetings>
   <CalendarItem/>
</AdjacentMeetings>
```

 <span data-ttu-id="1f142-105">**NonEmptyArrayOfAllItemsType**</span><span class="sxs-lookup"><span data-stu-id="1f142-105">**NonEmptyArrayOfAllItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1f142-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1f142-106">Attributes and elements</span></span>

<span data-ttu-id="1f142-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1f142-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1f142-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1f142-108">Attributes</span></span>

<span data-ttu-id="1f142-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1f142-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1f142-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1f142-110">Child elements</span></span>

|<span data-ttu-id="1f142-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1f142-111">**Element**</span></span>|<span data-ttu-id="1f142-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1f142-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1f142-113">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="1f142-113">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="1f142-114">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="1f142-114">Represents an Exchange calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1f142-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1f142-115">Parent elements</span></span>

|<span data-ttu-id="1f142-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="1f142-116">**Element**</span></span>|<span data-ttu-id="1f142-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1f142-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1f142-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="1f142-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="1f142-119">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="1f142-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="1f142-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="1f142-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="1f142-121">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="1f142-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f142-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f142-122">Remarks</span></span>

<span data-ttu-id="1f142-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1f142-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="1f142-124">Obwohl zusätzliche untergeordnete Elemente pro Schema gültig sind, ist das [CalendarItem](calendaritem.md) -Element das einzige untergeordnete Element, das Exchange-Webdienste innerhalb des **AdjacentMeetings** -Elements zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1f142-124">Although additional child elements are valid per the schema, the [CalendarItem](calendaritem.md) element is the only child element that Exchange Web Services (EWS) will return within the **AdjacentMeetings** element.</span></span> <span data-ttu-id="1f142-125">In diesem Thema werden keine untergeordneten Elemente aufgeführt, die für das Schema gültig sind, aber nicht von EWS zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1f142-125">This topic does not list child elements that are valid per the schema but will not be returned by EWS.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="1f142-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1f142-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1f142-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="1f142-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1f142-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1f142-128">Schema Name</span></span>  <br/> |<span data-ttu-id="1f142-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1f142-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="1f142-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1f142-130">Validation File</span></span>  <br/> |<span data-ttu-id="1f142-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1f142-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1f142-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1f142-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="1f142-133">False</span><span class="sxs-lookup"><span data-stu-id="1f142-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1f142-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f142-134">See also</span></span>

- [<span data-ttu-id="1f142-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1f142-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

