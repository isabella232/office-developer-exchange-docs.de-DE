---
title: ConferenceType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConferenceType
api_type:
- schema
ms.assetid: 6bcf6c18-2695-44b1-aabe-dadc52b2633a
description: Das ConferenceType-Element beschreibt die Art der Konferenzen, die mit einem Kalenderelement ausgeführt wird.
ms.openlocfilehash: d312420606c5e1914fe321ae7c7c512f0833199c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757590"
---
# <a name="conferencetype"></a><span data-ttu-id="d807c-103">ConferenceType</span><span class="sxs-lookup"><span data-stu-id="d807c-103">ConferenceType</span></span>

<span data-ttu-id="d807c-104">Das **ConferenceType** -Element beschreibt die Art der Konferenzen, die mit einem Kalenderelement ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d807c-104">The **ConferenceType** element describes the type of conferencing that is performed with a calendar item.</span></span> 
  
```xml
<ConferenceType/>
```

 <span data-ttu-id="d807c-105">**int**</span><span class="sxs-lookup"><span data-stu-id="d807c-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d807c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d807c-106">Attributes and elements</span></span>

<span data-ttu-id="d807c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d807c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d807c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d807c-108">Attributes</span></span>

<span data-ttu-id="d807c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d807c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d807c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d807c-110">Child elements</span></span>

<span data-ttu-id="d807c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d807c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d807c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d807c-112">Parent elements</span></span>

|<span data-ttu-id="d807c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d807c-113">**Element**</span></span>|<span data-ttu-id="d807c-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d807c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d807c-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="d807c-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="d807c-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="d807c-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="d807c-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="d807c-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="d807c-118">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="d807c-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d807c-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="d807c-119">Text value</span></span>

<span data-ttu-id="d807c-120">Ein Textwert, der eine ganze Zahl darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d807c-120">A text value that represents an integer value is required if this element is used.</span></span> <span data-ttu-id="d807c-121">Es folgen die möglichen Werte für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="d807c-121">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="d807c-122">0 = NetMeeting</span><span class="sxs-lookup"><span data-stu-id="d807c-122">0 = NetMeeting</span></span>
    
- <span data-ttu-id="d807c-123">1 = NetShow</span><span class="sxs-lookup"><span data-stu-id="d807c-123">1 = NetShow</span></span>
    
- <span data-ttu-id="d807c-124">2 = Chat</span><span class="sxs-lookup"><span data-stu-id="d807c-124">2 = Chat</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d807c-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d807c-125">Remarks</span></span>

<span data-ttu-id="d807c-126">**Meetingworkspaceurl (** Eigenschaft) kann für den Organisator Kalenderelement lesen geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d807c-126">The **MeetingWorkspaceUrl** property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="d807c-127">Es ist schreibgeschützt, für Besprechungsanfragen und für Elemente im Kalender des Teilnehmers.</span><span class="sxs-lookup"><span data-stu-id="d807c-127">It is read-only for meeting requests and for attendee's calendar items.</span></span> 
  
<span data-ttu-id="d807c-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d807c-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="d807c-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d807c-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d807c-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="d807c-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d807c-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d807c-131">Schema Name</span></span>  <br/> |<span data-ttu-id="d807c-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d807c-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="d807c-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d807c-133">Validation File</span></span>  <br/> |<span data-ttu-id="d807c-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d807c-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d807c-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d807c-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="d807c-136">False</span><span class="sxs-lookup"><span data-stu-id="d807c-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d807c-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d807c-137">See also</span></span>



- [<span data-ttu-id="d807c-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d807c-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

