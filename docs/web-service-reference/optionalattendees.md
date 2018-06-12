---
title: OptionalAttendees
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OptionalAttendees
api_type:
- schema
ms.assetid: e7c80c4d-3794-45e9-986f-6a8a687df0a4
description: OptionalAttendees-Element stellt Teilnehmer, die nicht erforderlich sind, an einer Besprechung teilnehmen.
ms.openlocfilehash: d5d994f7e85a47b14ab47f58fb73533cf961f7e6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830658"
---
# <a name="optionalattendees"></a><span data-ttu-id="9e25c-103">OptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="9e25c-103">OptionalAttendees</span></span>

<span data-ttu-id="9e25c-104">**OptionalAttendees** -Element stellt Teilnehmer, die nicht erforderlich sind, an einer Besprechung teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="9e25c-104">The **OptionalAttendees** element represents attendees who are not required to attend a meeting.</span></span> 
  
```xml
<OptionalAttendees>
   <Attendee/>
</OptionalAttendees>
```

 <span data-ttu-id="9e25c-105">**NonEmptyArrayOfAttendeesType**</span><span class="sxs-lookup"><span data-stu-id="9e25c-105">**NonEmptyArrayOfAttendeesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9e25c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9e25c-106">Attributes and elements</span></span>

<span data-ttu-id="9e25c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9e25c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9e25c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9e25c-108">Attributes</span></span>

<span data-ttu-id="9e25c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9e25c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9e25c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9e25c-110">Child elements</span></span>

|<span data-ttu-id="9e25c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="9e25c-111">**Element**</span></span>|<span data-ttu-id="9e25c-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9e25c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e25c-113">Attendee</span><span class="sxs-lookup"><span data-stu-id="9e25c-113">Attendee</span></span>](attendee.md) <br/> |<span data-ttu-id="9e25c-114">Stellt Teilnehmer und Ressourcen für eine Besprechung.</span><span class="sxs-lookup"><span data-stu-id="9e25c-114">Represents attendees and resources for a meeting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9e25c-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9e25c-115">Parent elements</span></span>

|<span data-ttu-id="9e25c-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="9e25c-116">**Element**</span></span>|<span data-ttu-id="9e25c-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9e25c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e25c-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="9e25c-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="9e25c-119">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="9e25c-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="9e25c-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="9e25c-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="9e25c-121">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="9e25c-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9e25c-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e25c-122">Remarks</span></span>

<span data-ttu-id="9e25c-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="9e25c-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9e25c-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9e25c-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9e25c-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="9e25c-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9e25c-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9e25c-126">Schema name</span></span>  <br/> |<span data-ttu-id="9e25c-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9e25c-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="9e25c-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9e25c-128">Validation file</span></span>  <br/> |<span data-ttu-id="9e25c-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9e25c-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9e25c-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="9e25c-130">Can be empty</span></span>  <br/> |<span data-ttu-id="9e25c-131">False</span><span class="sxs-lookup"><span data-stu-id="9e25c-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9e25c-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e25c-132">See also</span></span>



- [<span data-ttu-id="9e25c-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9e25c-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

