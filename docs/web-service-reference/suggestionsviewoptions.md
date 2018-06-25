---
title: SuggestionsViewOptions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuggestionsViewOptions
api_type:
- schema
ms.assetid: bb04ae38-e62d-4a69-a479-8ff326ca726e
description: Das SuggestionsViewOptions-Element enthält die Optionen zum Abrufen von Besprechungsinformationen Vorschlag.
ms.openlocfilehash: 09ff317ae0b2ebf1eadc89dc3bb1cf5b3ae19dcb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839139"
---
# <a name="suggestionsviewoptions"></a><span data-ttu-id="81662-103">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="81662-103">SuggestionsViewOptions</span></span>

<span data-ttu-id="81662-104">Das **SuggestionsViewOptions** -Element enthält die Optionen zum Abrufen von Besprechungsinformationen Vorschlag.</span><span class="sxs-lookup"><span data-stu-id="81662-104">The **SuggestionsViewOptions** element contains the options for obtaining meeting suggestion information.</span></span> 
  
[<span data-ttu-id="81662-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="81662-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="81662-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="81662-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
```xml
<SuggestionsViewOptions>
   <GoodThreshold>...</GoodThreshold>
   <MaximumResultsByDay>...</MaximumResultsByDay>
   <MaximumNonWorkingHourResultsByDay>...</MaximumNonWorkingHourResultsByDay>
   <MeetingDurationInMinutes>...</MeetingDurationInMinutes>
   <MinimumSuggestionQuality>...</MinimumSuggestionQuality>
   <SuggestionIntervalInMinutes>...</SuggestionIntervalInMinutes>
   <DetailedSuggestionsWindow>...</DetailedSuggestionsWindow>
   <CurrentMeetingTime>...</CurrentMeetingTime>
   <GlobalObjectId>...</GlobalObjectId>
</SuggestionsViewOptions>
```

 <span data-ttu-id="81662-107">**SuggestionsViewOptionsType**</span><span class="sxs-lookup"><span data-stu-id="81662-107">**SuggestionsViewOptionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="81662-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="81662-108">Attributes and elements</span></span>

<span data-ttu-id="81662-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="81662-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="81662-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="81662-110">Attributes</span></span>

<span data-ttu-id="81662-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="81662-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="81662-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="81662-112">Child elements</span></span>

|<span data-ttu-id="81662-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="81662-113">**Element**</span></span>|<span data-ttu-id="81662-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="81662-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="81662-115">GoodThreshold</span><span class="sxs-lookup"><span data-stu-id="81662-115">GoodThreshold</span></span>](goodthreshold.md) <br/> |<span data-ttu-id="81662-116">Gibt den Prozentsatz der Teilnehmer, die den Zeitraum an, für den Zeitraum als eine gute Vorgeschlagene Besprechungszeit qualifizieren öffnen benötigen.</span><span class="sxs-lookup"><span data-stu-id="81662-116">Specifies the percentage of attendees that must have the time period open for the time period to qualify as a good suggested meeting time.</span></span>  <br/> |
|[<span data-ttu-id="81662-117">' MaximumResultsByDay '</span><span class="sxs-lookup"><span data-stu-id="81662-117">MaximumResultsByDay</span></span>](maximumresultsbyday.md) <br/> |<span data-ttu-id="81662-118">Gibt die Anzahl der vorgeschlagenen Besprechung pro Tag in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="81662-118">Specifies the number of suggested meeting times per day returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="81662-119">' MaximumNonWorkHourResultsByDay '</span><span class="sxs-lookup"><span data-stu-id="81662-119">MaximumNonWorkHourResultsByDay</span></span>](maximumnonworkhourresultsbyday.md) <br/> |<span data-ttu-id="81662-120">Gibt die Anzahl der vorgeschlagenen Ergebnisse für Besprechungszeiten außerhalb der regulären Arbeitszeit pro Tag.</span><span class="sxs-lookup"><span data-stu-id="81662-120">Specifies the number of suggested results for meeting times outside regular working hours per day.</span></span>  <br/> |
|[<span data-ttu-id="81662-121">MeetingDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="81662-121">MeetingDurationInMinutes</span></span>](meetingdurationinminutes.md) <br/> |<span data-ttu-id="81662-122">Gibt die Länge der Besprechung, die vorgeschlagen werden.</span><span class="sxs-lookup"><span data-stu-id="81662-122">Specifies the length of the meeting to be suggested.</span></span>  <br/> |
|[<span data-ttu-id="81662-123">MinimumSuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="81662-123">MinimumSuggestionQuality</span></span>](minimumsuggestionquality.md) <br/> |<span data-ttu-id="81662-124">Gibt die Qualität der Besprechungsvorschläge in der Antwort zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="81662-124">Specifies the quality of meeting suggestions to be returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="81662-125">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="81662-125">DetailedSuggestionsWindow</span></span>](detailedsuggestionswindow.md) <br/> |<span data-ttu-id="81662-126">Gibt die Zeitspanne, die ausführliche Informationen zum vorgeschlagenen Besprechungszeiten abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="81662-126">Identifies the time span that is queried for detailed information about suggested meeting times.</span></span>  <br/> |
|[<span data-ttu-id="81662-127">CurrentMeetingTime</span><span class="sxs-lookup"><span data-stu-id="81662-127">CurrentMeetingTime</span></span>](currentmeetingtime.md) <br/> |<span data-ttu-id="81662-128">Stellt die Anfangszeit der eine Besprechung, die Sie mit der vorgeschlagenen Besprechung aktualisieren möchten Zeit Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="81662-128">Represents the start time of a meeting that you want to update with the suggested meeting time results.</span></span>  <br/> |
|[<span data-ttu-id="81662-129">GlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="81662-129">GlobalObjectId</span></span>](globalobjectid.md) <br/> |<span data-ttu-id="81662-130">Dieses Element wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="81662-130">This element is not used.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="81662-131">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="81662-131">Parent elements</span></span>

|<span data-ttu-id="81662-132">**Element**</span><span class="sxs-lookup"><span data-stu-id="81662-132">**Element**</span></span>|<span data-ttu-id="81662-133">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="81662-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="81662-134">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="81662-134">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) <br/> |<span data-ttu-id="81662-135">Enthält die Argumente, die zum Abrufen von Informationen zur Verfügbarkeit der Benutzer verwendet.</span><span class="sxs-lookup"><span data-stu-id="81662-135">Contains the arguments used to obtain user availability information.</span></span> <span data-ttu-id="81662-136">Dies ist eine Stammelements.</span><span class="sxs-lookup"><span data-stu-id="81662-136">This is a root element.</span></span>  <br/> <span data-ttu-id="81662-137">Es folgt der XPath-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="81662-137">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81662-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="81662-138">Remarks</span></span>

<span data-ttu-id="81662-139">Dieses Element ist nicht erforderlich, und kann nur einmal auftreten, wenn verwendet.</span><span class="sxs-lookup"><span data-stu-id="81662-139">This element is not required and can only occur once if used.</span></span> <span data-ttu-id="81662-140">Dieser Wert kann null sein, wenn der Wert des Elements [FreeBusyViewOptions](freebusyviewoptions.md) nicht null ist.</span><span class="sxs-lookup"><span data-stu-id="81662-140">This value can be null if the value of the [FreeBusyViewOptions](freebusyviewoptions.md) element is not null.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="81662-141">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="81662-141">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="81662-142">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="81662-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="81662-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="81662-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="81662-144">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="81662-144">Schema Name</span></span>  <br/> |<span data-ttu-id="81662-145">Schematypen</span><span class="sxs-lookup"><span data-stu-id="81662-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="81662-146">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="81662-146">Validation File</span></span>  <br/> |<span data-ttu-id="81662-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="81662-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="81662-148">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="81662-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="81662-149">False</span><span class="sxs-lookup"><span data-stu-id="81662-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="81662-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81662-150">See also</span></span>



[<span data-ttu-id="81662-151">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="81662-151">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="81662-152">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="81662-152">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

