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
description: Das GoodThreshold-Element gibt den Prozentsatz der Teilnehmer an, für die der Zeitraum geöffnet sein muss, damit der Zeitraum als gute vorgeschlagene Besprechungszeit qualifiziert wird.
ms.openlocfilehash: 34ea433ad7315d61df8cf8e22bae1166d3210af3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457312"
---
# <a name="goodthreshold"></a><span data-ttu-id="4542a-103">GoodThreshold</span><span class="sxs-lookup"><span data-stu-id="4542a-103">GoodThreshold</span></span>

<span data-ttu-id="4542a-104">Das **GoodThreshold** -Element gibt den Prozentsatz der Teilnehmer an, für die der Zeitraum geöffnet sein muss, damit der Zeitraum als gute vorgeschlagene Besprechungszeit qualifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="4542a-104">The **GoodThreshold** element specifies the percentage of attendees that must have the time period open in order for the time period to qualify as a Good suggested meeting time.</span></span> 
  
[<span data-ttu-id="4542a-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="4542a-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="4542a-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="4542a-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
[<span data-ttu-id="4542a-107">GoodThreshold</span><span class="sxs-lookup"><span data-stu-id="4542a-107">GoodThreshold</span></span>](goodthreshold.md)
  
```xml
<GoodThreshold>...</GoodThreshold>
```

 <span data-ttu-id="4542a-108">**int**</span><span class="sxs-lookup"><span data-stu-id="4542a-108">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4542a-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4542a-109">Attributes and elements</span></span>

<span data-ttu-id="4542a-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4542a-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4542a-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="4542a-111">Attributes</span></span>

<span data-ttu-id="4542a-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="4542a-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4542a-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4542a-113">Child elements</span></span>

<span data-ttu-id="4542a-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="4542a-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4542a-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4542a-115">Parent elements</span></span>

|<span data-ttu-id="4542a-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="4542a-116">**Element**</span></span>|<span data-ttu-id="4542a-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4542a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4542a-118">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="4542a-118">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="4542a-119">Enthält die Optionen zum Abrufen von Informationen zu Besprechungs Vorschlägen.</span><span class="sxs-lookup"><span data-stu-id="4542a-119">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="4542a-120">Es folgt der XPath für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="4542a-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4542a-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="4542a-121">Text value</span></span>

<span data-ttu-id="4542a-122">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4542a-122">A text value is required.</span></span> <span data-ttu-id="4542a-123">Die erwarteten ganzzahligen Werte liegen zwischen 0 und 50.</span><span class="sxs-lookup"><span data-stu-id="4542a-123">The expected integer values are between 0 and 50.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4542a-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4542a-124">Remarks</span></span>

<span data-ttu-id="4542a-125">Dieses Element ist erforderlich, wenn das [SuggestionsViewOptions](suggestionsviewoptions.md) -Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4542a-125">This element is required if the [SuggestionsViewOptions](suggestionsviewoptions.md) element is used.</span></span> <span data-ttu-id="4542a-126">Das **GoodThreshold** -Element bestimmt auch, welche Besprechungen als angemessen betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="4542a-126">The **GoodThreshold** element also determines what meetings are considered Fair.</span></span> <span data-ttu-id="4542a-127">IT der Prozentsatz der Teilnehmer mit Konflikten ist kleiner als der gute Schwellenwert und höher als 50 Prozent, die vorgeschlagene Besprechungszeit gilt als fair.</span><span class="sxs-lookup"><span data-stu-id="4542a-127">It the percentage of attendees with conflicts is less than the Good Threshold and higher than 50 percent, the suggested meeting time qualifies as Fair.</span></span> <span data-ttu-id="4542a-128">Der gute Schwellenwert plus 50 entspricht dem Prozentsatz, der den Wert "Good/Fair" definiert.</span><span class="sxs-lookup"><span data-stu-id="4542a-128">The Good Threshold plus 50 equals the percentage that defines the Good/Fair threshold.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4542a-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="4542a-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="4542a-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4542a-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4542a-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="4542a-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4542a-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4542a-132">Schema Name</span></span>  <br/> |<span data-ttu-id="4542a-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="4542a-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="4542a-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4542a-134">Validation File</span></span>  <br/> |<span data-ttu-id="4542a-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4542a-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4542a-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4542a-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="4542a-137">False</span><span class="sxs-lookup"><span data-stu-id="4542a-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4542a-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4542a-138">See also</span></span>



[<span data-ttu-id="4542a-139">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4542a-139">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="4542a-140">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="4542a-140">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

