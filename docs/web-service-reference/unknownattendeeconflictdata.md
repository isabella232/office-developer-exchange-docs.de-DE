---
title: UnknownAttendeeConflictData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnknownAttendeeConflictData
api_type:
- schema
ms.assetid: 70e41268-c231-4587-9d23-e46927fe5272
description: Das UnknownAttendeeConflictData-Element stellt einen nicht auflösbaren Teilnehmer oder einen Teilnehmer dar, der kein Benutzer, eine Verteilerliste oder ein Kontakt ist.
ms.openlocfilehash: b4362e0117e3939c21342a1ab8079d95512aec79
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459868"
---
# <a name="unknownattendeeconflictdata"></a><span data-ttu-id="07166-103">UnknownAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="07166-103">UnknownAttendeeConflictData</span></span>

<span data-ttu-id="07166-104">Das **UnknownAttendeeConflictData** -Element stellt einen nicht auflösbaren Teilnehmer oder einen Teilnehmer dar, der kein Benutzer, eine Verteilerliste oder ein Kontakt ist.</span><span class="sxs-lookup"><span data-stu-id="07166-104">The **UnknownAttendeeConflictData** element represents an unresolvable attendee or an attendee that is not a user, distribution list, or contact.</span></span> 
  
[<span data-ttu-id="07166-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="07166-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="07166-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="07166-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="07166-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="07166-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="07166-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="07166-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="07166-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="07166-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="07166-110">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="07166-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="07166-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="07166-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="07166-112">UnknownAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="07166-112">UnknownAttendeeConflictData</span></span>](unknownattendeeconflictdata.md)
  
```xml
<UnknownAttendeeConflictData/>
```

 <span data-ttu-id="07166-113">**UnknownAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="07166-113">**UnknownAttendeeConflictData**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="07166-114">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="07166-114">Attributes and elements</span></span>

<span data-ttu-id="07166-115">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="07166-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="07166-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="07166-116">Attributes</span></span>

<span data-ttu-id="07166-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="07166-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="07166-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="07166-118">Child elements</span></span>

<span data-ttu-id="07166-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="07166-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="07166-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="07166-120">Parent elements</span></span>

|<span data-ttu-id="07166-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="07166-121">**Element**</span></span>|<span data-ttu-id="07166-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="07166-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07166-123">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="07166-123">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="07166-124">Enthält ein Array von Konfliktdaten für abgefragte Teilnehmer, die im [GetUserAvailability-Vorgang](getuseravailability-operation.md)identifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="07166-124">Contains an array of conflict data for queried attendees identified in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span>  <br/> <span data-ttu-id="07166-125">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="07166-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07166-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07166-126">Remarks</span></span>

<span data-ttu-id="07166-127">Ein Teilnehmer ist unbekannt, wenn er nicht für ein Active Directory Verzeichnisdienstobjekt aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="07166-127">An attendee is unknown if it cannot be resolved against an Active Directory directory service object.</span></span> <span data-ttu-id="07166-128">Ein Teilnehmer ist nicht aufgelöst, wenn er nicht als Benutzer, Gruppe oder Kontakt festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="07166-128">An attendee is unresolved if it cannot be determined to be a user, group, or contact.</span></span> <span data-ttu-id="07166-129">Beispielsweise wird ein Teilnehmer nicht aufgelöst, wenn es sich um einen e-Mail-aktivierten Öffentlichen Ordner handelt.</span><span class="sxs-lookup"><span data-stu-id="07166-129">For example, an attendee will not be resolved if it is a mail-enabled public folder.</span></span>
  
<span data-ttu-id="07166-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="07166-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="07166-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="07166-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="07166-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="07166-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="07166-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="07166-133">Schema Name</span></span>  <br/> |<span data-ttu-id="07166-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="07166-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="07166-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="07166-135">Validation File</span></span>  <br/> |<span data-ttu-id="07166-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="07166-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="07166-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="07166-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="07166-138">False</span><span class="sxs-lookup"><span data-stu-id="07166-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="07166-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07166-139">See also</span></span>



[<span data-ttu-id="07166-140">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="07166-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="07166-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="07166-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="07166-142">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="07166-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

