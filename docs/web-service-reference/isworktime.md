---
title: Isworkzeit
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsWorkTime
api_type:
- schema
ms.assetid: 5243dd19-3593-4a81-bb2d-90496e04cb98
description: Das iswork Time-Element stellt dar, ob die vorgeschlagene Besprechungszeit während der geplanten Arbeitsstunden auftritt.
ms.openlocfilehash: a3f3c73d585bee6f73863e2be64eea245be674f4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467578"
---
# <a name="isworktime"></a><span data-ttu-id="92bd2-103">Isworkzeit</span><span class="sxs-lookup"><span data-stu-id="92bd2-103">IsWorkTime</span></span>

<span data-ttu-id="92bd2-104">Das **iswork** Time-Element stellt dar, ob die vorgeschlagene Besprechungszeit während der geplanten Arbeitsstunden auftritt.</span><span class="sxs-lookup"><span data-stu-id="92bd2-104">The **IsWorkTime** element represents whether the suggested meeting time occurs during scheduled work hours.</span></span> 
  
[<span data-ttu-id="92bd2-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="92bd2-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="92bd2-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="92bd2-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="92bd2-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="92bd2-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="92bd2-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="92bd2-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="92bd2-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="92bd2-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="92bd2-110">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="92bd2-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="92bd2-111">Isworkzeit</span><span class="sxs-lookup"><span data-stu-id="92bd2-111">IsWorkTime</span></span>](isworktime.md)
  
```xml
<IsWorkTime>true or false</IsWorkTime>
```

 <span data-ttu-id="92bd2-112">**boolean**</span><span class="sxs-lookup"><span data-stu-id="92bd2-112">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="92bd2-113">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="92bd2-113">Attributes and elements</span></span>

<span data-ttu-id="92bd2-114">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="92bd2-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="92bd2-115">Attribute</span><span class="sxs-lookup"><span data-stu-id="92bd2-115">Attributes</span></span>

<span data-ttu-id="92bd2-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="92bd2-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="92bd2-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="92bd2-117">Child elements</span></span>

<span data-ttu-id="92bd2-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="92bd2-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="92bd2-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="92bd2-119">Parent elements</span></span>

|<span data-ttu-id="92bd2-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="92bd2-120">**Element**</span></span>|<span data-ttu-id="92bd2-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="92bd2-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="92bd2-122">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="92bd2-122">Suggestion</span></span>](suggestion.md) <br/> |<span data-ttu-id="92bd2-123">Stellt einen einzelnen Besprechungszeit Vorschlag dar.</span><span class="sxs-lookup"><span data-stu-id="92bd2-123">Represents a single meeting time suggestion.</span></span>  <br/> <span data-ttu-id="92bd2-124">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="92bd2-124">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="92bd2-125">Textwert</span><span class="sxs-lookup"><span data-stu-id="92bd2-125">Text value</span></span>

<span data-ttu-id="92bd2-126">Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="92bd2-126">A text value that represents a Boolean value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="92bd2-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92bd2-127">Remarks</span></span>

<span data-ttu-id="92bd2-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="92bd2-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="92bd2-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="92bd2-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92bd2-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="92bd2-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="92bd2-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="92bd2-131">Schema Name</span></span>  <br/> |<span data-ttu-id="92bd2-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="92bd2-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="92bd2-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="92bd2-133">Validation File</span></span>  <br/> |<span data-ttu-id="92bd2-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="92bd2-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="92bd2-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="92bd2-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="92bd2-136">False</span><span class="sxs-lookup"><span data-stu-id="92bd2-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="92bd2-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92bd2-137">See also</span></span>



[<span data-ttu-id="92bd2-138">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="92bd2-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="92bd2-139">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="92bd2-139">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="92bd2-140">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="92bd2-140">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

