---
title: StartTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StartTime
api_type:
- schema
ms.assetid: 1fac7937-7a06-4d66-9d2a-14423bcb3b37
description: Das StartTime-Element stellt den Anfang des einer bestimmten Zeitspanne.
ms.openlocfilehash: 4346797d755bb6e577e1cacb8bec656a7562bf1f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831560"
---
# <a name="starttime"></a><span data-ttu-id="c38dc-103">StartTime</span><span class="sxs-lookup"><span data-stu-id="c38dc-103">StartTime</span></span>

<span data-ttu-id="c38dc-104">Das **StartTime** -Element stellt den Anfang des einer bestimmten Zeitspanne.</span><span class="sxs-lookup"><span data-stu-id="c38dc-104">The **StartTime** element represents the start of a time span.</span></span> 
  
```xml
<StartTime/
```

<span data-ttu-id="c38dc-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="c38dc-105">**dateTime**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c38dc-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c38dc-106">Attributes and elements</span></span>

<span data-ttu-id="c38dc-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c38dc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c38dc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c38dc-108">Attributes</span></span>

<span data-ttu-id="c38dc-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c38dc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c38dc-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c38dc-110">Child elements</span></span>

<span data-ttu-id="c38dc-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="c38dc-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c38dc-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c38dc-112">Parent elements</span></span>

|<span data-ttu-id="c38dc-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c38dc-113">**Element**</span></span>|<span data-ttu-id="c38dc-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c38dc-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c38dc-115">Zeitfenster</span><span class="sxs-lookup"><span data-stu-id="c38dc-115">TimeWindow</span></span>](timewindow.md) <br/> |<span data-ttu-id="c38dc-116">Gibt die Zeitspanne für die Verfügbarkeit Benutzerinformationen abgefragt.</span><span class="sxs-lookup"><span data-stu-id="c38dc-116">Identifies the time span queried for the user availability information.</span></span>  <br/><br/> <span data-ttu-id="c38dc-117">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="c38dc-117">The following is the XPath expression to this element:</span></span>  <br/><br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions/TimeWindow` <br/> |
|[<span data-ttu-id="c38dc-118">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="c38dc-118">DetailedSuggestionsWindow</span></span>](detailedsuggestionswindow.md) <br/> |<span data-ttu-id="c38dc-119">Gibt die Zeitspanne, die ausführliche Informationen zum vorgeschlagenen Besprechungszeiten abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="c38dc-119">Identifies the time span that is queried for detailed information about suggested meeting times.</span></span>  <br/><br/> <span data-ttu-id="c38dc-120">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="c38dc-120">The following is the XPath expression to this element:</span></span> <br/> <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow` <br/> |
|[<span data-ttu-id="c38dc-121">Dauer (' UserOofSettings ')</span><span class="sxs-lookup"><span data-stu-id="c38dc-121">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> | <span data-ttu-id="c38dc-122">Gibt die Dauer, für die der Status von Office (OOF) aktiviert ist, wenn das Element [OofState](oofstate.md) auf **Geplante Tasks**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c38dc-122">Specifies the duration for which the Out of Office (OOF) status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.</span></span>  <br/><br/>  <span data-ttu-id="c38dc-123">Im folgenden sind die möglichen XPath-Ausdrücke auf dieses Element:</span><span class="sxs-lookup"><span data-stu-id="c38dc-123">The following are the possible XPath expressions to this element:</span></span> <br/> <br/>  `/SetUserOofSettingsRequest/UserOofSettings/Duration` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/Duration` <br/> |
|[<span data-ttu-id="c38dc-124">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="c38dc-124">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="c38dc-125">Stellt eine einzelne Kalender Element vorkommen.</span><span class="sxs-lookup"><span data-stu-id="c38dc-125">Represents a unique calendar item occurrence.</span></span> <span data-ttu-id="c38dc-126">Dies ist für Verfügbarkeit Abfragen verwendet.</span><span class="sxs-lookup"><span data-stu-id="c38dc-126">This is used for Availability inquiries.</span></span> <span data-ttu-id="c38dc-127">Das **Werte von StartTime** -Element ist im **CalendarEvent** -Element erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c38dc-127">The **StartTime** element is required in the **CalendarEvent** element.</span></span> <span data-ttu-id="c38dc-128">Das **Werte von StartTime** -Element im **CalendarEvent** -Element ist eindeutig den **CalendarEvent** -Typ, obwohl es Facetten dieselben Werte enthält, die die **Werte von StartTime** -Elemente in der **Dauer** Typ enthalten.</span><span class="sxs-lookup"><span data-stu-id="c38dc-128">The **StartTime** element in the **CalendarEvent** element is unique to the **CalendarEvent** type although it contains the same facet values that the **StartTime** elements in the **Duration** type contain.</span></span>  <br/><br/> <span data-ttu-id="c38dc-129">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="c38dc-129">The following is the XPath expression to this element:</span></span>  <br/> <br/> `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c38dc-130">Textwert</span><span class="sxs-lookup"><span data-stu-id="c38dc-130">Text value</span></span>

<span data-ttu-id="c38dc-131">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c38dc-131">A text value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c38dc-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c38dc-132">Remarks</span></span>

<span data-ttu-id="c38dc-133">Das [EndTime](endtime.md) -Element darstellt, das Ende des Zeitraums.</span><span class="sxs-lookup"><span data-stu-id="c38dc-133">The [EndTime](endtime.md) element represents the end of the time span.</span></span> 
  
<span data-ttu-id="c38dc-134">Das Schema enthält viele [StartTime](starttime.md) Elemente.</span><span class="sxs-lookup"><span data-stu-id="c38dc-134">The schema includes many [StartTime](starttime.md) elements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c38dc-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="c38dc-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="c38dc-136">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c38dc-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c38dc-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="c38dc-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c38dc-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c38dc-138">Schema Name</span></span>  <br/> |<span data-ttu-id="c38dc-139">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c38dc-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="c38dc-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c38dc-140">Validation File</span></span>  <br/> |<span data-ttu-id="c38dc-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c38dc-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c38dc-142">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c38dc-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="c38dc-143">False</span><span class="sxs-lookup"><span data-stu-id="c38dc-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c38dc-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c38dc-144">See also</span></span>

- [<span data-ttu-id="c38dc-145">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c38dc-145">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="c38dc-146">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="c38dc-146">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

