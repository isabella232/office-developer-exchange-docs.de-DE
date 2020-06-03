---
title: Wiederholungs-Nr
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecurrenceId
api_type:
- schema
ms.assetid: 9ef3569d-ee56-4b22-b008-609fb3337da7
description: Das Serien-Element wird verwendet, um eine bestimmte Instanz eines wiederkehrenden Kalenderelements zu identifizieren.
ms.openlocfilehash: 58a379f2cffa7ff37181e93ad1c45c9752e84f1d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461611"
---
# <a name="recurrenceid"></a><span data-ttu-id="38065-103">Wiederholungs-Nr</span><span class="sxs-lookup"><span data-stu-id="38065-103">RecurrenceId</span></span>

<span data-ttu-id="38065-104">Das **Serien** -Element wird verwendet, um eine bestimmte Instanz eines wiederkehrenden Kalenderelements zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="38065-104">The **RecurrenceId** element is used to identify a specific instance of a recurring calendar item.</span></span> 
  
```xml
<RecurrenceId/>
```

 <span data-ttu-id="38065-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="38065-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="38065-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="38065-106">Attributes and elements</span></span>

<span data-ttu-id="38065-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="38065-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="38065-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="38065-108">Attributes</span></span>

<span data-ttu-id="38065-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="38065-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="38065-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="38065-110">Child elements</span></span>

<span data-ttu-id="38065-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="38065-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="38065-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="38065-112">Parent elements</span></span>

|<span data-ttu-id="38065-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="38065-113">**Element**</span></span>|<span data-ttu-id="38065-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="38065-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="38065-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="38065-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="38065-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="38065-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="38065-117">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="38065-117">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="38065-118">Stellt eine Besprechungsnachricht dar.</span><span class="sxs-lookup"><span data-stu-id="38065-118">Represents a meeting message.</span></span>  <br/> |
|[<span data-ttu-id="38065-119">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="38065-119">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="38065-120">Stellt eine Besprechungsanfrage dar.</span><span class="sxs-lookup"><span data-stu-id="38065-120">Represents a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="38065-121">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="38065-121">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="38065-122">Stellt eine Besprechungsantwort dar.</span><span class="sxs-lookup"><span data-stu-id="38065-122">Represents a meeting response.</span></span>  <br/> |
|[<span data-ttu-id="38065-123">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="38065-123">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="38065-124">Stellt einen Besprechungs Abbruch dar.</span><span class="sxs-lookup"><span data-stu-id="38065-124">Represents a meeting cancellation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="38065-125">Textwert</span><span class="sxs-lookup"><span data-stu-id="38065-125">Text value</span></span>

<span data-ttu-id="38065-126">Der Wert Text stellt einen Datum/Uhrzeit-Wert dar, der ein Kalender vorkommen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="38065-126">The text value represents a date/time value that identifies a calendar occurrence.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="38065-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38065-127">Remarks</span></span>

<span data-ttu-id="38065-128">Diese Eigenschaft wird zusammen mit der [UID](uid.md) -Eigenschaft verwendet, um eine bestimmte Instanz eines wiederkehrenden Kalenderelements zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="38065-128">This property is used with the [UID](uid.md) property to identify a specific instance of a recurring calendar item.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="38065-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="38065-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="38065-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="38065-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="38065-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="38065-131">Schema Name</span></span>  <br/> |<span data-ttu-id="38065-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="38065-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="38065-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="38065-133">Validation File</span></span>  <br/> |<span data-ttu-id="38065-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="38065-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="38065-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="38065-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="38065-136">False</span><span class="sxs-lookup"><span data-stu-id="38065-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="38065-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38065-137">See also</span></span>



- [<span data-ttu-id="38065-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="38065-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

