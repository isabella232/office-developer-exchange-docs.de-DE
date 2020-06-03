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
description: Das StartTime-Element stellt den Anfang einer Zeitspanne dar.
ms.openlocfilehash: 16bee698b65dc512a709e2af9ddfe8629347fee3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458565"
---
# <a name="starttime"></a><span data-ttu-id="ee7c7-103">StartTime</span><span class="sxs-lookup"><span data-stu-id="ee7c7-103">StartTime</span></span>

<span data-ttu-id="ee7c7-104">Das **StartTime-Element stellt** den Anfang einer Zeitspanne dar.</span><span class="sxs-lookup"><span data-stu-id="ee7c7-104">The **StartTime** element represents the start of a time span.</span></span> 
  
```xml
<StartTime/
```

<span data-ttu-id="ee7c7-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="ee7c7-105">**dateTime**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ee7c7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ee7c7-106">Attributes and elements</span></span>

<span data-ttu-id="ee7c7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ee7c7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ee7c7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ee7c7-108">Attributes</span></span>

<span data-ttu-id="ee7c7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ee7c7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ee7c7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ee7c7-110">Child elements</span></span>

<span data-ttu-id="ee7c7-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ee7c7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ee7c7-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ee7c7-112">Parent elements</span></span>

|<span data-ttu-id="ee7c7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ee7c7-113">**Element**</span></span>|<span data-ttu-id="ee7c7-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ee7c7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ee7c7-115">TimeWindow</span><span class="sxs-lookup"><span data-stu-id="ee7c7-115">TimeWindow</span></span>](timewindow.md) <br/> |<span data-ttu-id="ee7c7-116">Gibt den Zeitraum an, der für die Informationen zur Benutzerverfügbarkeit abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="ee7c7-116">Identifies the time span queried for the user availability information.</span></span>  <br/><br/> <span data-ttu-id="ee7c7-117">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="ee7c7-117">The following is the XPath expression to this element:</span></span>  <br/><br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions/TimeWindow` <br/> |
|[<span data-ttu-id="ee7c7-118">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="ee7c7-118">DetailedSuggestionsWindow</span></span>](detailedsuggestionswindow.md) <br/> |<span data-ttu-id="ee7c7-119">Gibt den Zeitraum an, der nach detaillierten Informationen zu vorgeschlagenen Besprechungszeiten abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="ee7c7-119">Identifies the time span that is queried for detailed information about suggested meeting times.</span></span>  <br/><br/> <span data-ttu-id="ee7c7-120">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="ee7c7-120">The following is the XPath expression to this element:</span></span> <br/> <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow` <br/> |
|[<span data-ttu-id="ee7c7-121">Dauer (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="ee7c7-121">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> | <span data-ttu-id="ee7c7-122">Gibt die Dauer an, für die der Abwesenheit (Out of Office, OOF) Status aktiviert ist, wenn das [OofState](oofstate.md) -Element auf **Scheduled**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ee7c7-122">Specifies the duration for which the Out of Office (OOF) status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.</span></span>  <br/><br/>  <span data-ttu-id="ee7c7-123">Im folgenden sind die möglichen XPath-Ausdrücke für dieses Element angegeben:</span><span class="sxs-lookup"><span data-stu-id="ee7c7-123">The following are the possible XPath expressions to this element:</span></span> <br/> <br/>  `/SetUserOofSettingsRequest/UserOofSettings/Duration` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/Duration` <br/> |
|[<span data-ttu-id="ee7c7-124">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="ee7c7-124">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="ee7c7-125">Stellt ein eindeutiges Kalenderelement vorkommen dar.</span><span class="sxs-lookup"><span data-stu-id="ee7c7-125">Represents a unique calendar item occurrence.</span></span> <span data-ttu-id="ee7c7-126">Dies wird für Verfügbarkeitsabfragen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ee7c7-126">This is used for Availability inquiries.</span></span> <span data-ttu-id="ee7c7-127">Das **StartTime** -Element ist im **CalendarEvent** -Element erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ee7c7-127">The **StartTime** element is required in the **CalendarEvent** element.</span></span> <span data-ttu-id="ee7c7-128">Das **StartTime** -Element im **CalendarEvent** -Element ist für den **CalendarEvent** -Typ eindeutig, obwohl es dieselben Facet-Werte enthält, die die **StartTime** -Elemente im **Duration** -Typ enthalten.</span><span class="sxs-lookup"><span data-stu-id="ee7c7-128">The **StartTime** element in the **CalendarEvent** element is unique to the **CalendarEvent** type although it contains the same facet values that the **StartTime** elements in the **Duration** type contain.</span></span>  <br/><br/> <span data-ttu-id="ee7c7-129">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="ee7c7-129">The following is the XPath expression to this element:</span></span>  <br/> <br/> `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ee7c7-130">Textwert</span><span class="sxs-lookup"><span data-stu-id="ee7c7-130">Text value</span></span>

<span data-ttu-id="ee7c7-131">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ee7c7-131">A text value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ee7c7-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ee7c7-132">Remarks</span></span>

<span data-ttu-id="ee7c7-133">Das [EndTime](endtime.md) -Element stellt das Ende der Zeitspanne dar.</span><span class="sxs-lookup"><span data-stu-id="ee7c7-133">The [EndTime](endtime.md) element represents the end of the time span.</span></span> 
  
<span data-ttu-id="ee7c7-134">Das Schema enthält viele [StartTime](starttime.md) -Elemente.</span><span class="sxs-lookup"><span data-stu-id="ee7c7-134">The schema includes many [StartTime](starttime.md) elements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ee7c7-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ee7c7-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="ee7c7-136">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ee7c7-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ee7c7-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="ee7c7-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ee7c7-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ee7c7-138">Schema Name</span></span>  <br/> |<span data-ttu-id="ee7c7-139">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ee7c7-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="ee7c7-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ee7c7-140">Validation File</span></span>  <br/> |<span data-ttu-id="ee7c7-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ee7c7-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ee7c7-142">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ee7c7-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="ee7c7-143">False</span><span class="sxs-lookup"><span data-stu-id="ee7c7-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ee7c7-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee7c7-144">See also</span></span>

- [<span data-ttu-id="ee7c7-145">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ee7c7-145">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="ee7c7-146">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="ee7c7-146">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

