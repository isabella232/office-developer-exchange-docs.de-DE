---
title: BusyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BusyType
api_type:
- schema
ms.assetid: 26d4fae0-8c78-4705-b5e8-d6033712c41e
description: Das BusyType-Element darstellt, den Frei/Gebucht-Status für ein Ereignis im Kalender festgelegt.
ms.openlocfilehash: 6484bc70c6a05084e5d2bc1738b575fbebe4c132
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757519"
---
# <a name="busytype"></a><span data-ttu-id="b0e3a-103">BusyType</span><span class="sxs-lookup"><span data-stu-id="b0e3a-103">BusyType</span></span>

<span data-ttu-id="b0e3a-104">Das **BusyType** -Element darstellt, den Frei/Gebucht-Status für ein Ereignis im Kalender festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b0e3a-104">The **BusyType** element represents the free/busy status set for a calendar event.</span></span> 
  
```xml
<BusyType>Free or Tentative or Busy or OOF or NoData</BusyType>
```

 <span data-ttu-id="b0e3a-105">**BusyType**</span><span class="sxs-lookup"><span data-stu-id="b0e3a-105">**BusyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b0e3a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b0e3a-106">Attributes and elements</span></span>

<span data-ttu-id="b0e3a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b0e3a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b0e3a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b0e3a-108">Attributes</span></span>

<span data-ttu-id="b0e3a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b0e3a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b0e3a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b0e3a-110">Child elements</span></span>

<span data-ttu-id="b0e3a-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b0e3a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b0e3a-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b0e3a-112">Parent elements</span></span>

|<span data-ttu-id="b0e3a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b0e3a-113">**Element**</span></span>|<span data-ttu-id="b0e3a-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b0e3a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b0e3a-115">IndividualAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="b0e3a-115">IndividualAttendeeConflictData</span></span>](individualattendeeconflictdata.md) <br/> |<span data-ttu-id="b0e3a-116">Enthält eines Benutzers oder Kontakts Frei/Gebucht-Status für ein Zeitfenster, das zur selben Zeit als die Uhrzeit der vorgeschlagenen Besprechung auftritt.</span><span class="sxs-lookup"><span data-stu-id="b0e3a-116">Contains a user's or contact's free/busy status for a time window that occurs at the same time as the suggested meeting time.</span></span>  <br/> <span data-ttu-id="b0e3a-117">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="b0e3a-117">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/IndividualAttendeeConflictData` <br/> |
|[<span data-ttu-id="b0e3a-118">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="b0e3a-118">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="b0e3a-119">Stellt eine einzelne Kalender Element vorkommen.</span><span class="sxs-lookup"><span data-stu-id="b0e3a-119">Represents a unique calendar item occurrence.</span></span>  <br/> <span data-ttu-id="b0e3a-120">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="b0e3a-120">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b0e3a-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="b0e3a-121">Text value</span></span>

<span data-ttu-id="b0e3a-122">Es wird ein Textwert für dieses Element erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b0e3a-122">A text value is required for this element.</span></span> <span data-ttu-id="b0e3a-123">Der Wert ist eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b0e3a-123">The value is a string type.</span></span> <span data-ttu-id="b0e3a-124">Es folgen die möglichen Werte für das [BusyType](busytype.md) -Element:</span><span class="sxs-lookup"><span data-stu-id="b0e3a-124">The following are the possible values for the [BusyType](busytype.md) element:</span></span> 
  
- <span data-ttu-id="b0e3a-125">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="b0e3a-125">Free</span></span>
    
- <span data-ttu-id="b0e3a-126">Mit Vorbehalt</span><span class="sxs-lookup"><span data-stu-id="b0e3a-126">Tentative</span></span>
    
- <span data-ttu-id="b0e3a-127">Gebucht</span><span class="sxs-lookup"><span data-stu-id="b0e3a-127">Busy</span></span>
    
- <span data-ttu-id="b0e3a-128">ABWESEND</span><span class="sxs-lookup"><span data-stu-id="b0e3a-128">OOF</span></span>
    
- <span data-ttu-id="b0e3a-129">NoData</span><span class="sxs-lookup"><span data-stu-id="b0e3a-129">NoData</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b0e3a-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b0e3a-130">Remarks</span></span>

<span data-ttu-id="b0e3a-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="b0e3a-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b0e3a-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b0e3a-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b0e3a-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="b0e3a-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b0e3a-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b0e3a-134">Schema Name</span></span>  <br/> |<span data-ttu-id="b0e3a-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b0e3a-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="b0e3a-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b0e3a-136">Validation File</span></span>  <br/> |<span data-ttu-id="b0e3a-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b0e3a-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b0e3a-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b0e3a-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="b0e3a-139">False</span><span class="sxs-lookup"><span data-stu-id="b0e3a-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b0e3a-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0e3a-140">See also</span></span>



[<span data-ttu-id="b0e3a-141">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b0e3a-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="b0e3a-142">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="b0e3a-142">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="b0e3a-143">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="b0e3a-143">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

