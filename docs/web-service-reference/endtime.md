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
description: Das EndTime-Element stellt das Ende einer Zeitspanne dar.
ms.openlocfilehash: 5a30b32ecfeafe582cd07dd662aacb0a960257c9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462992"
---
# <a name="endtime"></a><span data-ttu-id="47bd2-103">EndTime</span><span class="sxs-lookup"><span data-stu-id="47bd2-103">EndTime</span></span>

<span data-ttu-id="47bd2-104">Das **EndTime** -Element stellt das Ende einer Zeitspanne dar.</span><span class="sxs-lookup"><span data-stu-id="47bd2-104">The **EndTime** element represents the end of a time span.</span></span> 
  
```xml
<EndTime>dateTime</EndTime>
```

 <span data-ttu-id="47bd2-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="47bd2-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="47bd2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="47bd2-106">Attributes and elements</span></span>

<span data-ttu-id="47bd2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="47bd2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="47bd2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="47bd2-108">Attributes</span></span>

<span data-ttu-id="47bd2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="47bd2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="47bd2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="47bd2-110">Child elements</span></span>

<span data-ttu-id="47bd2-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="47bd2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="47bd2-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="47bd2-112">Parent elements</span></span>

|<span data-ttu-id="47bd2-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="47bd2-113">**Element**</span></span>|<span data-ttu-id="47bd2-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="47bd2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="47bd2-115">TimeWindow</span><span class="sxs-lookup"><span data-stu-id="47bd2-115">TimeWindow</span></span>](timewindow.md) <br/> |<span data-ttu-id="47bd2-116">Gibt den Zeitraum an, der für die Informationen zur Benutzerverfügbarkeit abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="47bd2-116">Identifies the time span queried for the user availability information.</span></span><br/><br/> <span data-ttu-id="47bd2-117">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="47bd2-117">The following is the XPath expression to this element:</span></span><br/><br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions/TimeWindow` <br/> |
|[<span data-ttu-id="47bd2-118">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="47bd2-118">DetailedSuggestionsWindow</span></span>](detailedsuggestionswindow.md) <br/> |<span data-ttu-id="47bd2-119">Gibt den Zeitraum an, der nach detaillierten Informationen zu vorgeschlagenen Besprechungszeiten abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="47bd2-119">Identifies the time span that is queried for detailed information about suggested meeting times.</span></span><br/><br/> <span data-ttu-id="47bd2-120">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="47bd2-120">The following is the XPath expression to this element:</span></span><br/><br/>  <span data-ttu-id="47bd2-121">`/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow`.</span><span class="sxs-lookup"><span data-stu-id="47bd2-121">`/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow`.</span></span>  <br/> |
|[<span data-ttu-id="47bd2-122">Dauer (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="47bd2-122">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> | <span data-ttu-id="47bd2-123">Gibt die Dauer an, für die der Abwesenheit (Out of Office, OOF) Status aktiviert ist, wenn das [OofState](oofstate.md) -Element auf **Scheduled**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="47bd2-123">Specifies the duration for which the Out of Office (OOF) status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.</span></span>  <br/><br/>  <span data-ttu-id="47bd2-124">Im folgenden sind die möglichen XPath-Ausdrücke für dieses Element angegeben:</span><span class="sxs-lookup"><span data-stu-id="47bd2-124">The following are the possible XPath expressions to this element:</span></span><br/><br/>  `/SetUserOofSettingsRequest/UserOofSettings/Duration` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/Duration` <br/> |
|[<span data-ttu-id="47bd2-125">Vorkommen</span><span class="sxs-lookup"><span data-stu-id="47bd2-125">Occurrence</span></span>](occurrence.md) <br/> |<span data-ttu-id="47bd2-126">Stellt ein einzelnes geändertes Vorkommen eines wiederkehrenden Kalenderelements dar.</span><span class="sxs-lookup"><span data-stu-id="47bd2-126">Represents a single modified occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="47bd2-127">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="47bd2-127">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="47bd2-128">Stellt ein eindeutiges Kalenderelement vorkommen dar.</span><span class="sxs-lookup"><span data-stu-id="47bd2-128">Represents a unique calendar item occurrence.</span></span> <span data-ttu-id="47bd2-129">Dies wird für Verfügbarkeitsabfragen verwendet.</span><span class="sxs-lookup"><span data-stu-id="47bd2-129">This is used for Availability inquiries.</span></span> <span data-ttu-id="47bd2-130">Das **EndTime** -Element ist im **CalendarEvent** -Element erforderlich.</span><span class="sxs-lookup"><span data-stu-id="47bd2-130">The **EndTime** element is required in the **CalendarEvent** element.</span></span> <span data-ttu-id="47bd2-131">Das **EndTime** -Element im **CalendarEvent** -Element ist für den **CalendarEvent** -Typ eindeutig.</span><span class="sxs-lookup"><span data-stu-id="47bd2-131">The **EndTime** element in the **CalendarEvent** element is unique to the **CalendarEvent** type.</span></span><br/><br/> <span data-ttu-id="47bd2-132">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="47bd2-132">The following is the XPath expression to this element:</span></span><br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="47bd2-133">Textwert</span><span class="sxs-lookup"><span data-stu-id="47bd2-133">Text value</span></span>

<span data-ttu-id="47bd2-134">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="47bd2-134">A text value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="47bd2-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47bd2-135">Remarks</span></span>

<span data-ttu-id="47bd2-136">Das [StartTime-Element stellt](starttime.md) den Anfang einer Zeitspanne dar.</span><span class="sxs-lookup"><span data-stu-id="47bd2-136">The [StartTime](starttime.md) element represents the beginning of a time span.</span></span> 
  
<span data-ttu-id="47bd2-137">Die Endzeit stellt die Zeit des Clients dar.</span><span class="sxs-lookup"><span data-stu-id="47bd2-137">The end time represents the client's time.</span></span>
  
<span data-ttu-id="47bd2-138">Das Schema enthält viele [EndTime](endtime.md) -Elemente.</span><span class="sxs-lookup"><span data-stu-id="47bd2-138">The schema includes many [EndTime](endtime.md) elements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="47bd2-139">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="47bd2-139">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="47bd2-140">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="47bd2-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="47bd2-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="47bd2-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="47bd2-142">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="47bd2-142">Schema Name</span></span>  <br/> |<span data-ttu-id="47bd2-143">Schematypen</span><span class="sxs-lookup"><span data-stu-id="47bd2-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="47bd2-144">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="47bd2-144">Validation File</span></span>  <br/> |<span data-ttu-id="47bd2-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="47bd2-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="47bd2-146">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="47bd2-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="47bd2-147">False</span><span class="sxs-lookup"><span data-stu-id="47bd2-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="47bd2-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47bd2-148">See also</span></span>

- [<span data-ttu-id="47bd2-149">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="47bd2-149">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="47bd2-150">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="47bd2-150">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

