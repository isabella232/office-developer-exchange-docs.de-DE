---
title: EndTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EndTime
api_type:
- schema
ms.assetid: 82e4ef4f-a557-4044-b9b7-d91622f4ac55
description: Das EndTime-Element darstellt, das Ende einer bestimmten Zeitspanne.
ms.openlocfilehash: 7d3d186618a7bcc05ad82532e13e03d2e67a0e40
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758254"
---
# <a name="endtime"></a><span data-ttu-id="13692-103">EndTime</span><span class="sxs-lookup"><span data-stu-id="13692-103">EndTime</span></span>

<span data-ttu-id="13692-104">Das **EndTime** -Element darstellt, das Ende einer bestimmten Zeitspanne.</span><span class="sxs-lookup"><span data-stu-id="13692-104">The **EndTime** element represents the end of a time span.</span></span> 
  
```xml
<EndTime>dateTime</EndTime>
```

 <span data-ttu-id="13692-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="13692-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="13692-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="13692-106">Attributes and elements</span></span>

<span data-ttu-id="13692-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="13692-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="13692-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="13692-108">Attributes</span></span>

<span data-ttu-id="13692-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="13692-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="13692-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="13692-110">Child elements</span></span>

<span data-ttu-id="13692-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="13692-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="13692-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="13692-112">Parent elements</span></span>

|<span data-ttu-id="13692-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="13692-113">**Element**</span></span>|<span data-ttu-id="13692-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="13692-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="13692-115">Zeitfenster</span><span class="sxs-lookup"><span data-stu-id="13692-115">TimeWindow</span></span>](timewindow.md) <br/> |<span data-ttu-id="13692-116">Gibt die Zeitspanne für die Verfügbarkeit Benutzerinformationen abgefragt.</span><span class="sxs-lookup"><span data-stu-id="13692-116">Identifies the time span queried for the user availability information.</span></span><br/><br/> <span data-ttu-id="13692-117">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="13692-117">The following is the XPath expression to this element:</span></span><br/><br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions/TimeWindow` <br/> |
|[<span data-ttu-id="13692-118">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="13692-118">DetailedSuggestionsWindow</span></span>](detailedsuggestionswindow.md) <br/> |<span data-ttu-id="13692-119">Gibt die Zeitspanne, die ausführliche Informationen zum vorgeschlagenen Besprechungszeiten abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="13692-119">Identifies the time span that is queried for detailed information about suggested meeting times.</span></span><br/><br/> <span data-ttu-id="13692-120">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="13692-120">The following is the XPath expression to this element:</span></span><br/><br/>  <span data-ttu-id="13692-121">`/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow`.</span><span class="sxs-lookup"><span data-stu-id="13692-121"></span></span>  <br/> |
|[<span data-ttu-id="13692-122">Dauer (' UserOofSettings ')</span><span class="sxs-lookup"><span data-stu-id="13692-122">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> | <span data-ttu-id="13692-123">Gibt die Dauer, für die der Status von Office (OOF) aktiviert ist, wenn das Element [OofState](oofstate.md) auf **Geplante Tasks**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="13692-123">Specifies the duration for which the Out of Office (OOF) status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.</span></span>  <br/><br/>  <span data-ttu-id="13692-124">Im folgenden sind die möglichen XPath-Ausdrücke auf dieses Element:</span><span class="sxs-lookup"><span data-stu-id="13692-124">The following are the possible XPath expressions to this element:</span></span><br/><br/>  `/SetUserOofSettingsRequest/UserOofSettings/Duration` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/Duration` <br/> |
|[<span data-ttu-id="13692-125">Vorkommen</span><span class="sxs-lookup"><span data-stu-id="13692-125">Occurrence</span></span>](occurrence.md) <br/> |<span data-ttu-id="13692-126">Stellt ein einzelnes geändertes Vorkommen des ein wiederkehrendes Kalenderelement.</span><span class="sxs-lookup"><span data-stu-id="13692-126">Represents a single modified occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="13692-127">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="13692-127">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="13692-128">Stellt eine einzelne Kalender Element vorkommen.</span><span class="sxs-lookup"><span data-stu-id="13692-128">Represents a unique calendar item occurrence.</span></span> <span data-ttu-id="13692-129">Dies ist für Verfügbarkeit Abfragen verwendet.</span><span class="sxs-lookup"><span data-stu-id="13692-129">This is used for Availability inquiries.</span></span> <span data-ttu-id="13692-130">Das **EndTime** -Element ist im **CalendarEvent** -Element erforderlich.</span><span class="sxs-lookup"><span data-stu-id="13692-130">The **EndTime** element is required in the **CalendarEvent** element.</span></span> <span data-ttu-id="13692-131">Das **EndTime** -Element im **CalendarEvent** -Element ist für den Typ **CalendarEvent** eindeutig.</span><span class="sxs-lookup"><span data-stu-id="13692-131">The **EndTime** element in the **CalendarEvent** element is unique to the **CalendarEvent** type.</span></span><br/><br/> <span data-ttu-id="13692-132">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="13692-132">The following is the XPath expression to this element:</span></span><br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="13692-133">Textwert</span><span class="sxs-lookup"><span data-stu-id="13692-133">Text value</span></span>

<span data-ttu-id="13692-134">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="13692-134">A text value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="13692-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="13692-135">Remarks</span></span>

<span data-ttu-id="13692-136">Das [StartTime](starttime.md) -Element darstellt, das Ende einer bestimmten Zeitspanne.</span><span class="sxs-lookup"><span data-stu-id="13692-136">The [StartTime](starttime.md) element represents the beginning of a time span.</span></span> 
  
<span data-ttu-id="13692-137">Die Endzeit darstellt der Client-Zeit.</span><span class="sxs-lookup"><span data-stu-id="13692-137">The end time represents the client's time.</span></span>
  
<span data-ttu-id="13692-138">Das Schema enthält viele [EndTime](endtime.md) Elemente.</span><span class="sxs-lookup"><span data-stu-id="13692-138">The schema includes many [EndTime](endtime.md) elements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="13692-139">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="13692-139">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="13692-140">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="13692-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13692-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="13692-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="13692-142">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="13692-142">Schema Name</span></span>  <br/> |<span data-ttu-id="13692-143">Schematypen</span><span class="sxs-lookup"><span data-stu-id="13692-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="13692-144">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="13692-144">Validation File</span></span>  <br/> |<span data-ttu-id="13692-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="13692-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="13692-146">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="13692-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="13692-147">False</span><span class="sxs-lookup"><span data-stu-id="13692-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="13692-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13692-148">See also</span></span>

- [<span data-ttu-id="13692-149">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="13692-149">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="13692-150">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="13692-150">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

