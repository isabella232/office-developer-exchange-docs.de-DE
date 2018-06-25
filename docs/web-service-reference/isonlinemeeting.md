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
description: IsOnlineMeeting-Element gibt an, ob die Besprechung online ist.
ms.openlocfilehash: 5a56b0b9828d6f6bec83fc0ad0f8f9579b471a72
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830061"
---
# <a name="isonlinemeeting"></a><span data-ttu-id="aa396-103">IsOnlineMeeting</span><span class="sxs-lookup"><span data-stu-id="aa396-103">IsOnlineMeeting</span></span>

<span data-ttu-id="aa396-104">**IsOnlineMeeting** -Element gibt an, ob die Besprechung online ist.</span><span class="sxs-lookup"><span data-stu-id="aa396-104">The **IsOnlineMeeting** element indicates whether the meeting is online.</span></span> 
  
```xml
<IsOnlineMeeting/>
```

 <span data-ttu-id="aa396-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="aa396-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aa396-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="aa396-106">Attributes and elements</span></span>

<span data-ttu-id="aa396-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="aa396-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aa396-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="aa396-108">Attributes</span></span>

<span data-ttu-id="aa396-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="aa396-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aa396-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aa396-110">Child elements</span></span>

<span data-ttu-id="aa396-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="aa396-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="aa396-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aa396-112">Parent elements</span></span>

|<span data-ttu-id="aa396-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="aa396-113">**Element**</span></span>|<span data-ttu-id="aa396-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aa396-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aa396-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="aa396-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="aa396-116">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="aa396-116">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="aa396-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="aa396-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="aa396-118">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="aa396-118">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="aa396-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="aa396-119">Text value</span></span>

<span data-ttu-id="aa396-120">Ein Textwert, der einen booleschen Wert darstellt ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aa396-120">A text value that represents a Boolean value is required if this element is used.</span></span> <span data-ttu-id="aa396-121">Der Wert **true** gibt an, dass die Besprechung online ist.</span><span class="sxs-lookup"><span data-stu-id="aa396-121">A value of **true** indicates that the meeting is online.</span></span> <span data-ttu-id="aa396-122">Der Wert **false** gibt an, dass die Besprechung nicht online ist.</span><span class="sxs-lookup"><span data-stu-id="aa396-122">A value of **false** indicates that the meeting is not online.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="aa396-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aa396-123">Remarks</span></span>

<span data-ttu-id="aa396-124">Die IsOnlineMeeting-Eigenschaft kann für den Organisator Kalenderelement lesen geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="aa396-124">The IsOnlineMeeting property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="aa396-125">Es ist schreibgeschützt, für Besprechungsanfragen und Kalenderelemente Teilnehmer.</span><span class="sxs-lookup"><span data-stu-id="aa396-125">It is read-only for meeting requests and for attendees' calendar items.</span></span>
  
<span data-ttu-id="aa396-126">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem MicrosoftExchange 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="aa396-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aa396-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="aa396-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa396-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="aa396-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="aa396-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="aa396-129">Schema name</span></span>  <br/> |<span data-ttu-id="aa396-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="aa396-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="aa396-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="aa396-131">Validation file</span></span>  <br/> |<span data-ttu-id="aa396-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="aa396-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="aa396-133">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="aa396-133">Can be empty</span></span>  <br/> |<span data-ttu-id="aa396-134">False</span><span class="sxs-lookup"><span data-stu-id="aa396-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aa396-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa396-135">See also</span></span>



- [<span data-ttu-id="aa396-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="aa396-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

