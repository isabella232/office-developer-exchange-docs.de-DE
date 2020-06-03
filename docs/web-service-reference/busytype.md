---
title: Busytype
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
description: Das busytype-Element stellt den Frei/Gebucht-Status für ein Calendar-Ereignis fest.
ms.openlocfilehash: 7c2d18c21156a8603d3caeeb796a56c5d8afcba5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459083"
---
# <a name="busytype"></a><span data-ttu-id="3b04c-103">Busytype</span><span class="sxs-lookup"><span data-stu-id="3b04c-103">BusyType</span></span>

<span data-ttu-id="3b04c-104">Das **busytype** -Element stellt den Frei/Gebucht-Status für ein Calendar-Ereignis fest.</span><span class="sxs-lookup"><span data-stu-id="3b04c-104">The **BusyType** element represents the free/busy status set for a calendar event.</span></span> 
  
```xml
<BusyType>Free or Tentative or Busy or OOF or NoData</BusyType>
```

 <span data-ttu-id="3b04c-105">**Busytype**</span><span class="sxs-lookup"><span data-stu-id="3b04c-105">**BusyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3b04c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3b04c-106">Attributes and elements</span></span>

<span data-ttu-id="3b04c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3b04c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3b04c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3b04c-108">Attributes</span></span>

<span data-ttu-id="3b04c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3b04c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3b04c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3b04c-110">Child elements</span></span>

<span data-ttu-id="3b04c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="3b04c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3b04c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3b04c-112">Parent elements</span></span>

|<span data-ttu-id="3b04c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3b04c-113">**Element**</span></span>|<span data-ttu-id="3b04c-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3b04c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b04c-115">IndividualAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="3b04c-115">IndividualAttendeeConflictData</span></span>](individualattendeeconflictdata.md) <br/> |<span data-ttu-id="3b04c-116">Enthält den Frei/Gebucht-Status eines Benutzers oder Kontakts für ein Zeitfenster, das gleichzeitig mit der vorgeschlagenen Besprechungszeit auftritt.</span><span class="sxs-lookup"><span data-stu-id="3b04c-116">Contains a user's or contact's free/busy status for a time window that occurs at the same time as the suggested meeting time.</span></span>  <br/> <span data-ttu-id="3b04c-117">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="3b04c-117">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/IndividualAttendeeConflictData` <br/> |
|[<span data-ttu-id="3b04c-118">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="3b04c-118">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="3b04c-119">Stellt ein eindeutiges Kalenderelement vorkommen dar.</span><span class="sxs-lookup"><span data-stu-id="3b04c-119">Represents a unique calendar item occurrence.</span></span>  <br/> <span data-ttu-id="3b04c-120">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="3b04c-120">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3b04c-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="3b04c-121">Text value</span></span>

<span data-ttu-id="3b04c-122">Für dieses Element ist ein Textwert erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3b04c-122">A text value is required for this element.</span></span> <span data-ttu-id="3b04c-123">Der Wert ist ein String-Typ.</span><span class="sxs-lookup"><span data-stu-id="3b04c-123">The value is a string type.</span></span> <span data-ttu-id="3b04c-124">Im folgenden sind die möglichen Werte für das [busytype](busytype.md) -Element angegeben:</span><span class="sxs-lookup"><span data-stu-id="3b04c-124">The following are the possible values for the [BusyType](busytype.md) element:</span></span> 
  
- <span data-ttu-id="3b04c-125">Frei</span><span class="sxs-lookup"><span data-stu-id="3b04c-125">Free</span></span>
    
- <span data-ttu-id="3b04c-126">Vorläufige</span><span class="sxs-lookup"><span data-stu-id="3b04c-126">Tentative</span></span>
    
- <span data-ttu-id="3b04c-127">Gebucht</span><span class="sxs-lookup"><span data-stu-id="3b04c-127">Busy</span></span>
    
- <span data-ttu-id="3b04c-128">Abwesenheits</span><span class="sxs-lookup"><span data-stu-id="3b04c-128">OOF</span></span>
    
- <span data-ttu-id="3b04c-129">NoData</span><span class="sxs-lookup"><span data-stu-id="3b04c-129">NoData</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3b04c-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b04c-130">Remarks</span></span>

<span data-ttu-id="3b04c-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="3b04c-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3b04c-132">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3b04c-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3b04c-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="3b04c-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3b04c-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3b04c-134">Schema Name</span></span>  <br/> |<span data-ttu-id="3b04c-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3b04c-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="3b04c-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3b04c-136">Validation File</span></span>  <br/> |<span data-ttu-id="3b04c-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3b04c-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3b04c-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3b04c-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="3b04c-139">False</span><span class="sxs-lookup"><span data-stu-id="3b04c-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b04c-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b04c-140">See also</span></span>



[<span data-ttu-id="3b04c-141">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3b04c-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="3b04c-142">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="3b04c-142">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="3b04c-143">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="3b04c-143">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

