---
title: RequiredAttendees
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RequiredAttendees
api_type:
- schema
ms.assetid: 422f8d44-b0eb-49ca-af0f-0e22b54c78d2
description: RequiredAttendees-Element stellt Teilnehmer, die erforderlich sind, an einer Besprechung teilnehmen.
ms.openlocfilehash: 9630be828f459808b61602448a4675aac07b0106
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831149"
---
# <a name="requiredattendees"></a><span data-ttu-id="fbe27-103">RequiredAttendees</span><span class="sxs-lookup"><span data-stu-id="fbe27-103">RequiredAttendees</span></span>

<span data-ttu-id="fbe27-104">**RequiredAttendees** -Element stellt Teilnehmer, die erforderlich sind, an einer Besprechung teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="fbe27-104">The **RequiredAttendees** element represents attendees that are required to attend a meeting.</span></span> 
  
```xml
<RequiredAttendees>
   <Attendee/>
</RequiredAttendees>
```

 <span data-ttu-id="fbe27-105">**NonEmptyArrayOfAttendeesType**</span><span class="sxs-lookup"><span data-stu-id="fbe27-105">**NonEmptyArrayOfAttendeesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fbe27-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fbe27-106">Attributes and elements</span></span>

<span data-ttu-id="fbe27-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fbe27-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fbe27-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="fbe27-108">Attributes</span></span>

<span data-ttu-id="fbe27-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="fbe27-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fbe27-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fbe27-110">Child elements</span></span>

|<span data-ttu-id="fbe27-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="fbe27-111">**Element**</span></span>|<span data-ttu-id="fbe27-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fbe27-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fbe27-113">Attendee</span><span class="sxs-lookup"><span data-stu-id="fbe27-113">Attendee</span></span>](attendee.md) <br/> |<span data-ttu-id="fbe27-114">Stellt Teilnehmer und Ressourcen für eine Besprechung.</span><span class="sxs-lookup"><span data-stu-id="fbe27-114">Represents attendees and resources for a meeting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fbe27-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fbe27-115">Parent elements</span></span>

|<span data-ttu-id="fbe27-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="fbe27-116">**Element**</span></span>|<span data-ttu-id="fbe27-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fbe27-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fbe27-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="fbe27-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="fbe27-119">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="fbe27-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="fbe27-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="fbe27-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="fbe27-121">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="fbe27-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fbe27-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fbe27-122">Remarks</span></span>

<span data-ttu-id="fbe27-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="fbe27-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fbe27-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="fbe27-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fbe27-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="fbe27-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fbe27-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fbe27-126">Schema name</span></span>  <br/> |<span data-ttu-id="fbe27-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="fbe27-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="fbe27-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fbe27-128">Validation file</span></span>  <br/> |<span data-ttu-id="fbe27-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fbe27-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fbe27-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="fbe27-130">Can be empty</span></span>  <br/> |<span data-ttu-id="fbe27-131">False</span><span class="sxs-lookup"><span data-stu-id="fbe27-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fbe27-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbe27-132">See also</span></span>



- [<span data-ttu-id="fbe27-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="fbe27-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

