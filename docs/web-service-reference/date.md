---
title: Date
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Date
api_type:
- schema
ms.assetid: 2f6bc090-fff4-45b1-8d7e-8fd6e060cce2
description: Das Date-Element darstellt, das Datum, das die Zeiten vorgeschlagenen Besprechung enthält.
ms.openlocfilehash: 98dc9d6c599222c819b2c9ed1bacd05758ae1655
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757853"
---
# <a name="date"></a><span data-ttu-id="39baa-103">Date</span><span class="sxs-lookup"><span data-stu-id="39baa-103">Date</span></span>

<span data-ttu-id="39baa-104">Das **Date** -Element darstellt, das Datum, das die Zeiten vorgeschlagenen Besprechung enthält.</span><span class="sxs-lookup"><span data-stu-id="39baa-104">The **Date** element represents the date that contains the suggested meeting times.</span></span> 
  
- [<span data-ttu-id="39baa-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="39baa-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md) 
- [<span data-ttu-id="39baa-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="39baa-106">SuggestionsResponse</span></span>](suggestionsresponse.md) 
- [<span data-ttu-id="39baa-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="39baa-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)  
- [<span data-ttu-id="39baa-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="39baa-108">SuggestionDayResult</span></span>](suggestiondayresult.md)  
- [<span data-ttu-id="39baa-109">Date</span><span class="sxs-lookup"><span data-stu-id="39baa-109">Date</span></span>](date.md)
  
```xml
<Date>...</Date>
```

<span data-ttu-id="39baa-110">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="39baa-110">**dateTime**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="39baa-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="39baa-111">Attributes and elements</span></span>

<span data-ttu-id="39baa-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="39baa-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="39baa-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="39baa-113">Attributes</span></span>

<span data-ttu-id="39baa-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="39baa-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="39baa-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="39baa-115">Child elements</span></span>

<span data-ttu-id="39baa-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="39baa-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="39baa-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="39baa-117">Parent elements</span></span>

|<span data-ttu-id="39baa-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="39baa-118">**Element**</span></span>|<span data-ttu-id="39baa-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="39baa-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39baa-120">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="39baa-120">SuggestionDayResult</span></span>](suggestiondayresult.md) <br/> |<span data-ttu-id="39baa-121">Stellt einen einzelnen Tag, der Zeiten der vorgeschlagenen Besprechung enthält.</span><span class="sxs-lookup"><span data-stu-id="39baa-121">Represents a single day that contains suggested meeting times.</span></span>  <br/><br/><span data-ttu-id="39baa-122">Es folgt der 2.0 XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="39baa-122">The following is the XPath 2.0 expression to this element:</span></span><br/><br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="39baa-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="39baa-123">Text value</span></span>

<span data-ttu-id="39baa-124">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="39baa-124">A text value is required.</span></span> <span data-ttu-id="39baa-125">Überprüfen Sie die World Wide Web Consortium (W3C) Schema Datatype Empfehlungen für das Format für den primitiven DateTime-Datentyp.</span><span class="sxs-lookup"><span data-stu-id="39baa-125">Review the World Wide Web Consortium (W3C) schema datatype recommendations for the format of the dateTime primitive datatype.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="39baa-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="39baa-126">Remarks</span></span>

<span data-ttu-id="39baa-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="39baa-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="39baa-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="39baa-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="39baa-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="39baa-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="39baa-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="39baa-130">Schema Name</span></span>  <br/> |<span data-ttu-id="39baa-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="39baa-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="39baa-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="39baa-132">Validation File</span></span>  <br/> |<span data-ttu-id="39baa-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="39baa-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="39baa-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="39baa-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="39baa-135">False</span><span class="sxs-lookup"><span data-stu-id="39baa-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="39baa-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39baa-136">See also</span></span>

- [<span data-ttu-id="39baa-137">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="39baa-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md) 
- [<span data-ttu-id="39baa-138">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="39baa-138">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="39baa-139">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="39baa-139">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

