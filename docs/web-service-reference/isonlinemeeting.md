---
title: IsOnlineMeeting
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsOnlineMeeting
api_type:
- schema
ms.assetid: c29df676-0f3a-4694-a42f-522c6d16872f
description: Das IsOnlineMeeting-Element gibt an, ob die Besprechung Online ist.
ms.openlocfilehash: d2d60c8a51ad7e03c33b57709d9173e79d162268
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460400"
---
# <a name="isonlinemeeting"></a><span data-ttu-id="28c21-103">IsOnlineMeeting</span><span class="sxs-lookup"><span data-stu-id="28c21-103">IsOnlineMeeting</span></span>

<span data-ttu-id="28c21-104">Das **IsOnlineMeeting** -Element gibt an, ob die Besprechung Online ist.</span><span class="sxs-lookup"><span data-stu-id="28c21-104">The **IsOnlineMeeting** element indicates whether the meeting is online.</span></span> 
  
```xml
<IsOnlineMeeting/>
```

 <span data-ttu-id="28c21-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="28c21-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="28c21-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="28c21-106">Attributes and elements</span></span>

<span data-ttu-id="28c21-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="28c21-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="28c21-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="28c21-108">Attributes</span></span>

<span data-ttu-id="28c21-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="28c21-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="28c21-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="28c21-110">Child elements</span></span>

<span data-ttu-id="28c21-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="28c21-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="28c21-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="28c21-112">Parent elements</span></span>

|<span data-ttu-id="28c21-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="28c21-113">**Element**</span></span>|<span data-ttu-id="28c21-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="28c21-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28c21-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="28c21-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="28c21-116">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="28c21-116">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="28c21-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="28c21-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="28c21-118">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="28c21-118">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="28c21-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="28c21-119">Text value</span></span>

<span data-ttu-id="28c21-120">Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="28c21-120">A text value that represents a Boolean value is required if this element is used.</span></span> <span data-ttu-id="28c21-121">Der Wert **true** gibt an, dass die Besprechung Online ist.</span><span class="sxs-lookup"><span data-stu-id="28c21-121">A value of **true** indicates that the meeting is online.</span></span> <span data-ttu-id="28c21-122">Der Wert **false** gibt an, dass die Besprechung nicht online ist.</span><span class="sxs-lookup"><span data-stu-id="28c21-122">A value of **false** indicates that the meeting is not online.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="28c21-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28c21-123">Remarks</span></span>

<span data-ttu-id="28c21-124">Die IsOnlineMeeting-Eigenschaft ist für das Kalenderelement des Organisators schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="28c21-124">The IsOnlineMeeting property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="28c21-125">Er ist schreibgeschützt für Besprechungsanfragen und für die Kalenderelemente von Teilnehmern.</span><span class="sxs-lookup"><span data-stu-id="28c21-125">It is read-only for meeting requests and for attendees' calendar items.</span></span>
  
<span data-ttu-id="28c21-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange 2007 ausgeführt wird, auf dem die Client Zugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="28c21-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="28c21-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="28c21-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28c21-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="28c21-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="28c21-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="28c21-129">Schema name</span></span>  <br/> |<span data-ttu-id="28c21-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="28c21-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="28c21-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="28c21-131">Validation file</span></span>  <br/> |<span data-ttu-id="28c21-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="28c21-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="28c21-133">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="28c21-133">Can be empty</span></span>  <br/> |<span data-ttu-id="28c21-134">False</span><span class="sxs-lookup"><span data-stu-id="28c21-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="28c21-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28c21-135">See also</span></span>



- [<span data-ttu-id="28c21-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="28c21-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

