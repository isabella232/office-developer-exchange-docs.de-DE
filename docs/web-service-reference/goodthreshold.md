---
title: GoodThreshold
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GoodThreshold
api_type:
- schema
ms.assetid: 68f607f5-7271-46a6-8ffc-91878185a683
description: Das GoodThreshold-Element gibt den Prozentsatz der Teilnehmer, die den Zeitraum an, öffnen Sie in der Reihenfolge für den Zeitraum als eine gute Vorgeschlagene Besprechungszeit qualifizieren benötigen.
ms.openlocfilehash: 8044cb2b52cb572fad8731253dffa34de9d097fa
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829746"
---
# <a name="goodthreshold"></a><span data-ttu-id="d39fe-103">GoodThreshold</span><span class="sxs-lookup"><span data-stu-id="d39fe-103">GoodThreshold</span></span>

<span data-ttu-id="d39fe-104">Das **GoodThreshold** -Element gibt den Prozentsatz der Teilnehmer, die den Zeitraum an, öffnen Sie in der Reihenfolge für den Zeitraum als eine gute Vorgeschlagene Besprechungszeit qualifizieren benötigen.</span><span class="sxs-lookup"><span data-stu-id="d39fe-104">The **GoodThreshold** element specifies the percentage of attendees that must have the time period open in order for the time period to qualify as a Good suggested meeting time.</span></span> 
  
[<span data-ttu-id="d39fe-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="d39fe-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="d39fe-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="d39fe-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
[<span data-ttu-id="d39fe-107">GoodThreshold</span><span class="sxs-lookup"><span data-stu-id="d39fe-107">GoodThreshold</span></span>](goodthreshold.md)
  
```xml
<GoodThreshold>...</GoodThreshold>
```

 <span data-ttu-id="d39fe-108">**int**</span><span class="sxs-lookup"><span data-stu-id="d39fe-108">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d39fe-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d39fe-109">Attributes and elements</span></span>

<span data-ttu-id="d39fe-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d39fe-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d39fe-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="d39fe-111">Attributes</span></span>

<span data-ttu-id="d39fe-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="d39fe-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d39fe-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d39fe-113">Child elements</span></span>

<span data-ttu-id="d39fe-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="d39fe-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d39fe-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d39fe-115">Parent elements</span></span>

|<span data-ttu-id="d39fe-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="d39fe-116">**Element**</span></span>|<span data-ttu-id="d39fe-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d39fe-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d39fe-118">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="d39fe-118">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="d39fe-119">Enthält die Optionen zum Abrufen von Besprechungsinformationen Vorschlag.</span><span class="sxs-lookup"><span data-stu-id="d39fe-119">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="d39fe-120">Es folgt der XPath-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="d39fe-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d39fe-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="d39fe-121">Text value</span></span>

<span data-ttu-id="d39fe-122">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d39fe-122">A text value is required.</span></span> <span data-ttu-id="d39fe-123">Die erwartete ganzzahligen Werte liegen zwischen 0 und 50.</span><span class="sxs-lookup"><span data-stu-id="d39fe-123">The expected integer values are between 0 and 50.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d39fe-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d39fe-124">Remarks</span></span>

<span data-ttu-id="d39fe-125">Dieses Element ist erforderlich, wenn das [SuggestionsViewOptions](suggestionsviewoptions.md) -Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d39fe-125">This element is required if the [SuggestionsViewOptions](suggestionsviewoptions.md) element is used.</span></span> <span data-ttu-id="d39fe-126">Das Element **GoodThreshold** bestimmt auch an, welche Besprechungen Fair berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="d39fe-126">The **GoodThreshold** element also determines what meetings are considered Fair.</span></span> <span data-ttu-id="d39fe-127">Es, die der Prozentsatz der Teilnehmer mit Konflikten handelt es sich um kleiner als der Schwellenwert gute und höher als 50 Prozent der vorgeschlagenen Besprechungszeit als Fair qualifiziert.</span><span class="sxs-lookup"><span data-stu-id="d39fe-127">It the percentage of attendees with conflicts is less than the Good Threshold and higher than 50 percent, the suggested meeting time qualifies as Fair.</span></span> <span data-ttu-id="d39fe-128">Schwellenwert für die gute plus 50 entspricht den Prozentsatz, der den Schwellenwert für die gut/Fair definiert.</span><span class="sxs-lookup"><span data-stu-id="d39fe-128">The Good Threshold plus 50 equals the percentage that defines the Good/Fair threshold.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d39fe-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d39fe-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="d39fe-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d39fe-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d39fe-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="d39fe-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d39fe-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d39fe-132">Schema Name</span></span>  <br/> |<span data-ttu-id="d39fe-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d39fe-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="d39fe-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d39fe-134">Validation File</span></span>  <br/> |<span data-ttu-id="d39fe-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d39fe-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d39fe-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d39fe-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="d39fe-137">False</span><span class="sxs-lookup"><span data-stu-id="d39fe-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d39fe-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d39fe-138">See also</span></span>



[<span data-ttu-id="d39fe-139">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d39fe-139">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="d39fe-140">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="d39fe-140">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

