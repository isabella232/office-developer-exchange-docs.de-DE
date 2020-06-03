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
description: Das RequiredAttendees-Element stellt Teilnehmer dar, die für die Teilnahme an einer Besprechung erforderlich sind.
ms.openlocfilehash: a67800687f24dc323c3d80e4166ca9dd34dfc4fc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468292"
---
# <a name="requiredattendees"></a><span data-ttu-id="3069e-103">RequiredAttendees</span><span class="sxs-lookup"><span data-stu-id="3069e-103">RequiredAttendees</span></span>

<span data-ttu-id="3069e-104">Das **RequiredAttendees** -Element stellt Teilnehmer dar, die für die Teilnahme an einer Besprechung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="3069e-104">The **RequiredAttendees** element represents attendees that are required to attend a meeting.</span></span> 
  
```xml
<RequiredAttendees>
   <Attendee/>
</RequiredAttendees>
```

 <span data-ttu-id="3069e-105">**NonEmptyArrayOfAttendeesType**</span><span class="sxs-lookup"><span data-stu-id="3069e-105">**NonEmptyArrayOfAttendeesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3069e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3069e-106">Attributes and elements</span></span>

<span data-ttu-id="3069e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3069e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3069e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3069e-108">Attributes</span></span>

<span data-ttu-id="3069e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3069e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3069e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3069e-110">Child elements</span></span>

|<span data-ttu-id="3069e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3069e-111">**Element**</span></span>|<span data-ttu-id="3069e-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3069e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3069e-113">Teilnehmer</span><span class="sxs-lookup"><span data-stu-id="3069e-113">Attendee</span></span>](attendee.md) <br/> |<span data-ttu-id="3069e-114">Stellt Teilnehmer und Ressourcen für eine Besprechung dar.</span><span class="sxs-lookup"><span data-stu-id="3069e-114">Represents attendees and resources for a meeting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3069e-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3069e-115">Parent elements</span></span>

|<span data-ttu-id="3069e-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="3069e-116">**Element**</span></span>|<span data-ttu-id="3069e-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3069e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3069e-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="3069e-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="3069e-119">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="3069e-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="3069e-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="3069e-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="3069e-121">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="3069e-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3069e-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3069e-122">Remarks</span></span>

<span data-ttu-id="3069e-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="3069e-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3069e-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3069e-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3069e-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="3069e-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3069e-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3069e-126">Schema name</span></span>  <br/> |<span data-ttu-id="3069e-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3069e-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="3069e-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3069e-128">Validation file</span></span>  <br/> |<span data-ttu-id="3069e-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3069e-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3069e-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="3069e-130">Can be empty</span></span>  <br/> |<span data-ttu-id="3069e-131">False</span><span class="sxs-lookup"><span data-stu-id="3069e-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3069e-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3069e-132">See also</span></span>



- [<span data-ttu-id="3069e-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3069e-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

