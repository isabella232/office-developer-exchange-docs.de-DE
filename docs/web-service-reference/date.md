---
title: Datum
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
description: Das Date-Element stellt das Datum dar, das die vorgeschlagenen Besprechungszeiten enthält.
ms.openlocfilehash: bcc152ed6aba94907189b5579b998815be45db16
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44443788"
---
# <a name="date"></a><span data-ttu-id="9d500-103">Datum</span><span class="sxs-lookup"><span data-stu-id="9d500-103">Date</span></span>

<span data-ttu-id="9d500-104">Das **Date** -Element stellt das Datum dar, das die vorgeschlagenen Besprechungszeiten enthält.</span><span class="sxs-lookup"><span data-stu-id="9d500-104">The **Date** element represents the date that contains the suggested meeting times.</span></span> 
  
- [<span data-ttu-id="9d500-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="9d500-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md) 
- [<span data-ttu-id="9d500-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="9d500-106">SuggestionsResponse</span></span>](suggestionsresponse.md) 
- [<span data-ttu-id="9d500-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="9d500-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)  
- [<span data-ttu-id="9d500-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="9d500-108">SuggestionDayResult</span></span>](suggestiondayresult.md)  
- [<span data-ttu-id="9d500-109">Date</span><span class="sxs-lookup"><span data-stu-id="9d500-109">Date</span></span>](date.md)
  
```xml
<Date>...</Date>
```

<span data-ttu-id="9d500-110">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="9d500-110">**dateTime**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="9d500-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9d500-111">Attributes and elements</span></span>

<span data-ttu-id="9d500-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9d500-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9d500-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="9d500-113">Attributes</span></span>

<span data-ttu-id="9d500-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="9d500-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9d500-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9d500-115">Child elements</span></span>

<span data-ttu-id="9d500-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="9d500-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9d500-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9d500-117">Parent elements</span></span>

|<span data-ttu-id="9d500-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="9d500-118">**Element**</span></span>|<span data-ttu-id="9d500-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d500-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9d500-120">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="9d500-120">SuggestionDayResult</span></span>](suggestiondayresult.md) <br/> |<span data-ttu-id="9d500-121">Stellt einen einzelnen Tag dar, der vorgeschlagene Besprechungszeiten enthält.</span><span class="sxs-lookup"><span data-stu-id="9d500-121">Represents a single day that contains suggested meeting times.</span></span>  <br/><br/><span data-ttu-id="9d500-122">Im folgenden finden Sie den XPath 2,0-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="9d500-122">The following is the XPath 2.0 expression to this element:</span></span><br/><br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9d500-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="9d500-123">Text value</span></span>

<span data-ttu-id="9d500-124">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9d500-124">A text value is required.</span></span> <span data-ttu-id="9d500-125">Lesen Sie die Empfehlungen des W3C (World Wide webconsortium)-Schemas für das Format des primitiven datetime-Datentyps.</span><span class="sxs-lookup"><span data-stu-id="9d500-125">Review the World Wide Web Consortium (W3C) schema datatype recommendations for the format of the dateTime primitive datatype.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9d500-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d500-126">Remarks</span></span>

<span data-ttu-id="9d500-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="9d500-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9d500-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="9d500-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d500-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d500-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9d500-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9d500-130">Schema Name</span></span>  <br/> |<span data-ttu-id="9d500-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9d500-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="9d500-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9d500-132">Validation File</span></span>  <br/> |<span data-ttu-id="9d500-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9d500-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9d500-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9d500-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="9d500-135">False</span><span class="sxs-lookup"><span data-stu-id="9d500-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9d500-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d500-136">See also</span></span>

- [<span data-ttu-id="9d500-137">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9d500-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md) 
- [<span data-ttu-id="9d500-138">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="9d500-138">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="9d500-139">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="9d500-139">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

