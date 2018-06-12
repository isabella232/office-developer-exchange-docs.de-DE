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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757242"
---
# <a name="adjacentmeetingcount"></a><span data-ttu-id="20368-103">AdjacentMeetingCount</span><span class="sxs-lookup"><span data-stu-id="20368-103">AdjacentMeetingCount</span></span>

<span data-ttu-id="20368-104">Das Element **AdjacentMeetingCount** stellt die Gesamtzahl der Kalenderelemente, die an eine Besprechungszeit angrenzen.</span><span class="sxs-lookup"><span data-stu-id="20368-104">The **AdjacentMeetingCount** element represents the total number of calendar items that are adjacent to a meeting time.</span></span> 
  
```xml
<AdjacentMeetingCount/>
```

 <span data-ttu-id="20368-105">**Int**</span><span class="sxs-lookup"><span data-stu-id="20368-105">**Int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="20368-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="20368-106">Attributes and elements</span></span>

<span data-ttu-id="20368-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="20368-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="20368-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="20368-108">Attributes</span></span>

<span data-ttu-id="20368-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="20368-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="20368-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="20368-110">Child elements</span></span>

<span data-ttu-id="20368-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="20368-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="20368-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="20368-112">Parent elements</span></span>

|<span data-ttu-id="20368-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="20368-113">**Element**</span></span>|<span data-ttu-id="20368-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="20368-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="20368-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="20368-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="20368-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="20368-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="20368-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="20368-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="20368-118">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="20368-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="20368-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="20368-119">Text value</span></span>

<span data-ttu-id="20368-120">Ein Textwert, der eine ganze Zahl darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="20368-120">A text value that represents an integer is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="20368-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20368-121">Remarks</span></span>

<span data-ttu-id="20368-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="20368-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="20368-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="20368-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="20368-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="20368-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="20368-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="20368-125">Schema name</span></span>  <br/> |<span data-ttu-id="20368-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="20368-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="20368-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="20368-127">Validation file</span></span>  <br/> |<span data-ttu-id="20368-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="20368-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="20368-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="20368-129">Can be empty</span></span>  <br/> |<span data-ttu-id="20368-130">False</span><span class="sxs-lookup"><span data-stu-id="20368-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="20368-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20368-131">See also</span></span>

- [<span data-ttu-id="20368-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="20368-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

