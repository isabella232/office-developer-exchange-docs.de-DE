---
title: MeetingRequestWasSent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingRequestWasSent
api_type:
- schema
ms.assetid: 9192400a-8eef-4147-9f94-aa8ea91b41d8
description: Das MeetingRequestWasSent-Element gibt an, ob eine Besprechungsanfrage an den gewünschten Teilnehmer gesendet wurde.
ms.openlocfilehash: 0a87b1d773997e08ab96726375e4c8ce010faaf7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830438"
---
# <a name="meetingrequestwassent"></a><span data-ttu-id="c9add-103">MeetingRequestWasSent</span><span class="sxs-lookup"><span data-stu-id="c9add-103">MeetingRequestWasSent</span></span>

<span data-ttu-id="c9add-104">Das **MeetingRequestWasSent** -Element gibt an, ob eine Besprechungsanfrage an den gewünschten Teilnehmer gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c9add-104">The **MeetingRequestWasSent** element indicates whether a meeting request has been sent to requested attendees.</span></span> 
  
```xml
<MeetingRequestWasSent/>
```

 <span data-ttu-id="c9add-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c9add-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c9add-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c9add-106">Attributes and elements</span></span>

<span data-ttu-id="c9add-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c9add-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c9add-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c9add-108">Attributes</span></span>

<span data-ttu-id="c9add-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c9add-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c9add-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c9add-110">Child elements</span></span>

<span data-ttu-id="c9add-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="c9add-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c9add-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c9add-112">Parent elements</span></span>

|<span data-ttu-id="c9add-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c9add-113">**Element**</span></span>|<span data-ttu-id="c9add-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c9add-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c9add-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="c9add-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="c9add-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="c9add-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="c9add-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="c9add-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="c9add-118">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="c9add-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c9add-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="c9add-119">Text value</span></span>

<span data-ttu-id="c9add-120">Ein Textwert, der einen booleschen Wert darstellt ist erforderlich, wenn dieses Element enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="c9add-120">A text value that represents a Boolean value is required if this element is included.</span></span> <span data-ttu-id="c9add-121">Der Wert **true** gibt an, dass eine Besprechungsanfrage gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c9add-121">A value of **true** indicates that a meeting request was sent.</span></span> <span data-ttu-id="c9add-122">Der Wert **false** gibt an, dass eine Besprechungsanfrage nicht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c9add-122">A value of **false** indicates that a meeting request has not been sent.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c9add-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c9add-123">Remarks</span></span>

<span data-ttu-id="c9add-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="c9add-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c9add-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c9add-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c9add-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="c9add-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c9add-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c9add-127">Schema name</span></span>  <br/> |<span data-ttu-id="c9add-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c9add-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="c9add-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c9add-129">Validation file</span></span>  <br/> |<span data-ttu-id="c9add-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c9add-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c9add-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="c9add-131">Can be empty</span></span>  <br/> |<span data-ttu-id="c9add-132">False</span><span class="sxs-lookup"><span data-stu-id="c9add-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c9add-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9add-133">See also</span></span>



- [<span data-ttu-id="c9add-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c9add-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

