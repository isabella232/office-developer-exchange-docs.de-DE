---
title: DayQuality
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DayQuality
api_type:
- schema
ms.assetid: cd0eb239-6e7f-4a5a-b245-659f170550b7
description: Das DayQuality-Element stellt die Qualität des Tages für das enthalten von Qualität vorgeschlagene Besprechungszeiten.
ms.openlocfilehash: 41cc8313dccb1a5172fefc167e6ed90a21109ec5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455114"
---
# <a name="dayquality"></a><span data-ttu-id="de64c-103">DayQuality</span><span class="sxs-lookup"><span data-stu-id="de64c-103">DayQuality</span></span>

<span data-ttu-id="de64c-104">Das **DayQuality** -Element stellt die Qualität des Tages für das enthalten von Qualität vorgeschlagene Besprechungszeiten.</span><span class="sxs-lookup"><span data-stu-id="de64c-104">The **DayQuality** element represents the quality of the day for containing quality suggested meeting times.</span></span> 
  
- [<span data-ttu-id="de64c-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="de64c-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)  
- [<span data-ttu-id="de64c-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="de64c-106">SuggestionsResponse</span></span>](suggestionsresponse.md) 
- [<span data-ttu-id="de64c-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="de64c-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)  
- [<span data-ttu-id="de64c-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="de64c-108">SuggestionDayResult</span></span>](suggestiondayresult.md) 
- [<span data-ttu-id="de64c-109">DayQuality</span><span class="sxs-lookup"><span data-stu-id="de64c-109">DayQuality</span></span>](dayquality.md)
  
```xml
<DayQuality>Excellent or Good or Fair or Poor</DayQuality>
```

<span data-ttu-id="de64c-110">**SuggestionQuality**</span><span class="sxs-lookup"><span data-stu-id="de64c-110">**SuggestionQuality**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="de64c-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="de64c-111">Attributes and elements</span></span>

<span data-ttu-id="de64c-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="de64c-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="de64c-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="de64c-113">Attributes</span></span>

<span data-ttu-id="de64c-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="de64c-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="de64c-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="de64c-115">Child elements</span></span>

<span data-ttu-id="de64c-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="de64c-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="de64c-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="de64c-117">Parent elements</span></span>

|<span data-ttu-id="de64c-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="de64c-118">**Element**</span></span>|<span data-ttu-id="de64c-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="de64c-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de64c-120">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="de64c-120">SuggestionDayResult</span></span>](suggestiondayresult.md) <br/> |<span data-ttu-id="de64c-121">Stellt einen einzelnen Tag dar, der vorgeschlagene Besprechungszeiten enthält.</span><span class="sxs-lookup"><span data-stu-id="de64c-121">Represents a single day that contains suggested meeting times.</span></span>  <br/><br/><span data-ttu-id="de64c-122">Im folgenden finden Sie den XPath 2,0-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="de64c-122">The following is the XPath 2.0 expression to this element:</span></span><br/><br/>`/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="de64c-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="de64c-123">Text value</span></span>

<span data-ttu-id="de64c-124">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="de64c-124">A text value is required.</span></span> <span data-ttu-id="de64c-125">Im folgenden sind die möglichen Werte für dieses Element angegeben:</span><span class="sxs-lookup"><span data-stu-id="de64c-125">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="de64c-126">**Hervorragend**</span><span class="sxs-lookup"><span data-stu-id="de64c-126">**Excellent**</span></span>   
- <span data-ttu-id="de64c-127">**Gut**</span><span class="sxs-lookup"><span data-stu-id="de64c-127">**Good**</span></span>    
- <span data-ttu-id="de64c-128">**Messe**</span><span class="sxs-lookup"><span data-stu-id="de64c-128">**Fair**</span></span>    
- <span data-ttu-id="de64c-129">**mangelhaft**</span><span class="sxs-lookup"><span data-stu-id="de64c-129">**Poor**</span></span>
    
## <a name="remarks"></a><span data-ttu-id="de64c-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de64c-130">Remarks</span></span>

<span data-ttu-id="de64c-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="de64c-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="de64c-132">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="de64c-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="de64c-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="de64c-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="de64c-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="de64c-134">Schema Name</span></span>  <br/> |<span data-ttu-id="de64c-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="de64c-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="de64c-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="de64c-136">Validation File</span></span>  <br/> |<span data-ttu-id="de64c-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="de64c-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="de64c-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="de64c-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="de64c-139">False</span><span class="sxs-lookup"><span data-stu-id="de64c-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="de64c-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de64c-140">See also</span></span>

- [<span data-ttu-id="de64c-141">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="de64c-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)  
- [<span data-ttu-id="de64c-142">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="de64c-142">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="de64c-143">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="de64c-143">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

