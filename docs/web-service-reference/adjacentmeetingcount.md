---
title: AdjacentMeetingCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AdjacentMeetingCount
api_type:
- schema
ms.assetid: 35045024-f6e1-47d1-89be-f100b7b4f3c7
description: Das Element AdjacentMeetingCount stellt die Gesamtzahl der Kalenderelemente, die an eine Besprechungszeit angrenzen.
ms.openlocfilehash: a00468bec392498745fe778b627259a79d6027bf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757242"
---
# <a name="adjacentmeetingcount"></a><span data-ttu-id="db11d-103">AdjacentMeetingCount</span><span class="sxs-lookup"><span data-stu-id="db11d-103">AdjacentMeetingCount</span></span>

<span data-ttu-id="db11d-104">Das Element **AdjacentMeetingCount** stellt die Gesamtzahl der Kalenderelemente, die an eine Besprechungszeit angrenzen.</span><span class="sxs-lookup"><span data-stu-id="db11d-104">The **AdjacentMeetingCount** element represents the total number of calendar items that are adjacent to a meeting time.</span></span> 
  
```xml
<AdjacentMeetingCount/>
```

 <span data-ttu-id="db11d-105">**Int**</span><span class="sxs-lookup"><span data-stu-id="db11d-105">**Int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="db11d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="db11d-106">Attributes and elements</span></span>

<span data-ttu-id="db11d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="db11d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="db11d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="db11d-108">Attributes</span></span>

<span data-ttu-id="db11d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="db11d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="db11d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="db11d-110">Child elements</span></span>

<span data-ttu-id="db11d-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="db11d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="db11d-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="db11d-112">Parent elements</span></span>

|<span data-ttu-id="db11d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="db11d-113">**Element**</span></span>|<span data-ttu-id="db11d-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="db11d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="db11d-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="db11d-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="db11d-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="db11d-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="db11d-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="db11d-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="db11d-118">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="db11d-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="db11d-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="db11d-119">Text value</span></span>

<span data-ttu-id="db11d-120">Ein Textwert, der eine ganze Zahl darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="db11d-120">A text value that represents an integer is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="db11d-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="db11d-121">Remarks</span></span>

<span data-ttu-id="db11d-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="db11d-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="db11d-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="db11d-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="db11d-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="db11d-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="db11d-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="db11d-125">Schema name</span></span>  <br/> |<span data-ttu-id="db11d-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="db11d-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="db11d-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="db11d-127">Validation file</span></span>  <br/> |<span data-ttu-id="db11d-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="db11d-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="db11d-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="db11d-129">Can be empty</span></span>  <br/> |<span data-ttu-id="db11d-130">False</span><span class="sxs-lookup"><span data-stu-id="db11d-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="db11d-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db11d-131">See also</span></span>

- [<span data-ttu-id="db11d-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="db11d-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

