---
title: SuggestionDayResultArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuggestionDayResultArray
api_type:
- schema
ms.assetid: eeba9eff-5eca-4002-b5a5-8fb794feaba1
description: Das SuggestionDayResultArray-Element enthält ein Array von besprechungsvorschlägen nach Datum organisiert.
ms.openlocfilehash: c208104356606a5d9961461ad8743a772d2410d8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839137"
---
# <a name="suggestiondayresultarray"></a><span data-ttu-id="082b3-103">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="082b3-103">SuggestionDayResultArray</span></span>

<span data-ttu-id="082b3-104">Das **SuggestionDayResultArray** -Element enthält ein Array von besprechungsvorschlägen nach Datum organisiert.</span><span class="sxs-lookup"><span data-stu-id="082b3-104">The **SuggestionDayResultArray** element contains an array of meeting suggestions organized by date.</span></span> 
  
[<span data-ttu-id="082b3-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="082b3-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="082b3-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="082b3-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="082b3-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="082b3-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
```xml
<SuggestionDayResultArray>
   <SuggestionDayResult>...</SuggestionDayResult>
</SuggestionDayResultArray>
```

 <span data-ttu-id="082b3-108">**ArrayOfSuggestionDayResult**</span><span class="sxs-lookup"><span data-stu-id="082b3-108">**ArrayOfSuggestionDayResult**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="082b3-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="082b3-109">Attributes and elements</span></span>

<span data-ttu-id="082b3-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="082b3-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="082b3-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="082b3-111">Attributes</span></span>

<span data-ttu-id="082b3-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="082b3-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="082b3-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="082b3-113">Child elements</span></span>

|<span data-ttu-id="082b3-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="082b3-114">**Element**</span></span>|<span data-ttu-id="082b3-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="082b3-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="082b3-116">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="082b3-116">SuggestionDayResult</span></span>](suggestiondayresult.md) <br/> |<span data-ttu-id="082b3-117">Stellt einen einzelnen Tag, der Zeiten der vorgeschlagenen Besprechung enthält.</span><span class="sxs-lookup"><span data-stu-id="082b3-117">Represents a single day that contains suggested meeting times.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="082b3-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="082b3-118">Parent elements</span></span>

|<span data-ttu-id="082b3-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="082b3-119">**Element**</span></span>|<span data-ttu-id="082b3-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="082b3-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="082b3-121">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="082b3-121">SuggestionsResponse</span></span>](suggestionsresponse.md) <br/> |<span data-ttu-id="082b3-122">Für angefordert Besprechungsvorschläge enthält Antwort und Vorschlag Daten</span><span class="sxs-lookup"><span data-stu-id="082b3-122">Contains response information and suggestion data for requested meeting suggestions</span></span>  <br/> <span data-ttu-id="082b3-123">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="082b3-123">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="082b3-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="082b3-124">Remarks</span></span>

<span data-ttu-id="082b3-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="082b3-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="082b3-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="082b3-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="082b3-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="082b3-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="082b3-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="082b3-128">Schema Name</span></span>  <br/> |<span data-ttu-id="082b3-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="082b3-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="082b3-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="082b3-130">Validation File</span></span>  <br/> |<span data-ttu-id="082b3-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="082b3-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="082b3-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="082b3-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="082b3-133">False</span><span class="sxs-lookup"><span data-stu-id="082b3-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="082b3-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="082b3-134">See also</span></span>



[<span data-ttu-id="082b3-135">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="082b3-135">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="082b3-136">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="082b3-136">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="082b3-137">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="082b3-137">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

