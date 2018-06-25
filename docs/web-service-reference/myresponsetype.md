---
title: MyResponseType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MyResponseType
api_type:
- schema
ms.assetid: 9741b71d-a310-4520-81d5-3787a1ee630f
description: Das MyResponseType-Element enthält den Status des oder der Antwort auf ein Kalenderelement.
ms.openlocfilehash: 3be900ed6d2932699e3e83a0bca2918c016eb689
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830497"
---
# <a name="myresponsetype"></a><span data-ttu-id="b8fc1-103">MyResponseType</span><span class="sxs-lookup"><span data-stu-id="b8fc1-103">MyResponseType</span></span>

<span data-ttu-id="b8fc1-104">Das **MyResponseType** -Element enthält den Status des oder der Antwort auf ein Kalenderelement.</span><span class="sxs-lookup"><span data-stu-id="b8fc1-104">The **MyResponseType** element contains the status of or response to a calendar item.</span></span> 
  
```xml
<MyResponseType/>
```

 <span data-ttu-id="b8fc1-105">**ResponseTypeType**</span><span class="sxs-lookup"><span data-stu-id="b8fc1-105">**ResponseTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b8fc1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b8fc1-106">Attributes and elements</span></span>

<span data-ttu-id="b8fc1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b8fc1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b8fc1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b8fc1-108">Attributes</span></span>

<span data-ttu-id="b8fc1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b8fc1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b8fc1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b8fc1-110">Child elements</span></span>

<span data-ttu-id="b8fc1-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b8fc1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b8fc1-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b8fc1-112">Parent elements</span></span>

|<span data-ttu-id="b8fc1-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b8fc1-113">**Element**</span></span>|<span data-ttu-id="b8fc1-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b8fc1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8fc1-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="b8fc1-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="b8fc1-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="b8fc1-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="b8fc1-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="b8fc1-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="b8fc1-118">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="b8fc1-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b8fc1-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="b8fc1-119">Text value</span></span>

<span data-ttu-id="b8fc1-120">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b8fc1-120">A text value is required.</span></span> <span data-ttu-id="b8fc1-121">Es folgen die möglichen Textwerte für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="b8fc1-121">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="b8fc1-122">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="b8fc1-122">Unknown</span></span>
    
- <span data-ttu-id="b8fc1-123">Organisator</span><span class="sxs-lookup"><span data-stu-id="b8fc1-123">Organizer</span></span>
    
- <span data-ttu-id="b8fc1-124">Mit Vorbehalt</span><span class="sxs-lookup"><span data-stu-id="b8fc1-124">Tentative</span></span>
    
- <span data-ttu-id="b8fc1-125">Annehmen</span><span class="sxs-lookup"><span data-stu-id="b8fc1-125">Accept</span></span>
    
- <span data-ttu-id="b8fc1-126">Ablehnen</span><span class="sxs-lookup"><span data-stu-id="b8fc1-126">Decline</span></span>
    
- <span data-ttu-id="b8fc1-127">NoResponseReceived</span><span class="sxs-lookup"><span data-stu-id="b8fc1-127">NoResponseReceived</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b8fc1-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b8fc1-128">Remarks</span></span>

<span data-ttu-id="b8fc1-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="b8fc1-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b8fc1-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b8fc1-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b8fc1-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="b8fc1-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b8fc1-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b8fc1-132">Schema name</span></span>  <br/> |<span data-ttu-id="b8fc1-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b8fc1-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="b8fc1-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b8fc1-134">Validation file</span></span>  <br/> |<span data-ttu-id="b8fc1-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b8fc1-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b8fc1-136">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b8fc1-136">Can be empty</span></span>  <br/> |<span data-ttu-id="b8fc1-137">False</span><span class="sxs-lookup"><span data-stu-id="b8fc1-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b8fc1-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8fc1-138">See also</span></span>



- [<span data-ttu-id="b8fc1-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b8fc1-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

