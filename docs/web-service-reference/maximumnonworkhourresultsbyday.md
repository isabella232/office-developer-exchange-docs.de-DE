---
title: "' MaximumNonWorkHourResultsByDay '"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MaximumNonWorkHourResultsByDay
api_type:
- schema
ms.assetid: 9fb7314d-779c-4b1f-9d7c-b5cb092ed134
description: Das Element ' MaximumNonWorkHourResultsByDay ' gibt die Anzahl der vorgeschlagenen Ergebnisse für Besprechungszeiten außerhalb der regulären Arbeitszeit pro Tag an.
ms.openlocfilehash: f931dcaabda222e1579a0a4c0e0e6e49d88c6342
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830382"
---
# <a name="maximumnonworkhourresultsbyday"></a><span data-ttu-id="060f3-103">' MaximumNonWorkHourResultsByDay '</span><span class="sxs-lookup"><span data-stu-id="060f3-103">MaximumNonWorkHourResultsByDay</span></span>

<span data-ttu-id="060f3-104">Das Element **' MaximumNonWorkHourResultsByDay '** gibt die Anzahl der vorgeschlagenen Ergebnisse für Besprechungszeiten außerhalb der regulären Arbeitszeit pro Tag an.</span><span class="sxs-lookup"><span data-stu-id="060f3-104">The **MaximumNonWorkHourResultsByDay** element specifies the number of suggested results for meeting times outside regular working hours per day.</span></span> 
  
[<span data-ttu-id="060f3-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="060f3-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="060f3-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="060f3-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
[<span data-ttu-id="060f3-107">' MaximumNonWorkHourResultsByDay '</span><span class="sxs-lookup"><span data-stu-id="060f3-107">MaximumNonWorkHourResultsByDay</span></span>](maximumnonworkhourresultsbyday.md)
  
```xml
<MaximumNonWorkHourResultsByDay>...</MaximumNonWorkHourResultsByDay>
```

 <span data-ttu-id="060f3-108">**int**</span><span class="sxs-lookup"><span data-stu-id="060f3-108">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="060f3-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="060f3-109">Attributes and elements</span></span>

<span data-ttu-id="060f3-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="060f3-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="060f3-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="060f3-111">Attributes</span></span>

<span data-ttu-id="060f3-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="060f3-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="060f3-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="060f3-113">Child elements</span></span>

<span data-ttu-id="060f3-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="060f3-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="060f3-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="060f3-115">Parent elements</span></span>

|<span data-ttu-id="060f3-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="060f3-116">**Element**</span></span>|<span data-ttu-id="060f3-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="060f3-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="060f3-118">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="060f3-118">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="060f3-119">Enthält die Optionen zum Abrufen von Besprechungsinformationen Vorschlag.</span><span class="sxs-lookup"><span data-stu-id="060f3-119">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="060f3-120">Es folgt der XPath-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="060f3-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="060f3-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="060f3-121">Text value</span></span>

<span data-ttu-id="060f3-122">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="060f3-122">A text value is required.</span></span> <span data-ttu-id="060f3-123">Der Textwert stellt eine ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="060f3-123">The text value represents an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="060f3-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="060f3-124">Remarks</span></span>

<span data-ttu-id="060f3-125">Dieses Element ist erforderlich, wenn das [SuggestionsViewOptions](suggestionsviewoptions.md) -Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="060f3-125">This element is required if the [SuggestionsViewOptions](suggestionsviewoptions.md) element is used.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="060f3-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="060f3-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="060f3-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="060f3-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="060f3-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="060f3-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="060f3-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="060f3-129">Schema Name</span></span>  <br/> |<span data-ttu-id="060f3-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="060f3-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="060f3-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="060f3-131">Validation File</span></span>  <br/> |<span data-ttu-id="060f3-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="060f3-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="060f3-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="060f3-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="060f3-134">False</span><span class="sxs-lookup"><span data-stu-id="060f3-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="060f3-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="060f3-135">See also</span></span>



[<span data-ttu-id="060f3-136">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="060f3-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="060f3-137">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="060f3-137">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

