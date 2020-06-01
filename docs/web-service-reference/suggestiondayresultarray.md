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
description: Das SuggestionDayResultArray-Element enthält ein Array von Besprechungs Vorschlägen nach Datum organisiert.
ms.openlocfilehash: 277d4cf71c31aba26cbff6f598eaa62769cae552
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457984"
---
# <a name="suggestiondayresultarray"></a><span data-ttu-id="6da41-103">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="6da41-103">SuggestionDayResultArray</span></span>

<span data-ttu-id="6da41-104">Das **SuggestionDayResultArray** -Element enthält ein Array von Besprechungs Vorschlägen nach Datum organisiert.</span><span class="sxs-lookup"><span data-stu-id="6da41-104">The **SuggestionDayResultArray** element contains an array of meeting suggestions organized by date.</span></span> 
  
[<span data-ttu-id="6da41-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="6da41-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="6da41-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="6da41-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="6da41-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="6da41-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
```xml
<SuggestionDayResultArray>
   <SuggestionDayResult>...</SuggestionDayResult>
</SuggestionDayResultArray>
```

 <span data-ttu-id="6da41-108">**ArrayOfSuggestionDayResult**</span><span class="sxs-lookup"><span data-stu-id="6da41-108">**ArrayOfSuggestionDayResult**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6da41-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6da41-109">Attributes and elements</span></span>

<span data-ttu-id="6da41-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6da41-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6da41-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="6da41-111">Attributes</span></span>

<span data-ttu-id="6da41-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="6da41-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6da41-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6da41-113">Child elements</span></span>

|<span data-ttu-id="6da41-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="6da41-114">**Element**</span></span>|<span data-ttu-id="6da41-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6da41-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6da41-116">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="6da41-116">SuggestionDayResult</span></span>](suggestiondayresult.md) <br/> |<span data-ttu-id="6da41-117">Stellt einen einzelnen Tag dar, der vorgeschlagene Besprechungszeiten enthält.</span><span class="sxs-lookup"><span data-stu-id="6da41-117">Represents a single day that contains suggested meeting times.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6da41-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6da41-118">Parent elements</span></span>

|<span data-ttu-id="6da41-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="6da41-119">**Element**</span></span>|<span data-ttu-id="6da41-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6da41-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6da41-121">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="6da41-121">SuggestionsResponse</span></span>](suggestionsresponse.md) <br/> |<span data-ttu-id="6da41-122">Enthält Antwortinformationen und Vorschlagsdaten für angeforderte Besprechungsvorschläge</span><span class="sxs-lookup"><span data-stu-id="6da41-122">Contains response information and suggestion data for requested meeting suggestions</span></span>  <br/> <span data-ttu-id="6da41-123">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="6da41-123">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6da41-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6da41-124">Remarks</span></span>

<span data-ttu-id="6da41-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="6da41-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6da41-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6da41-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6da41-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="6da41-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6da41-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6da41-128">Schema Name</span></span>  <br/> |<span data-ttu-id="6da41-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="6da41-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6da41-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6da41-130">Validation File</span></span>  <br/> |<span data-ttu-id="6da41-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6da41-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6da41-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6da41-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="6da41-133">False</span><span class="sxs-lookup"><span data-stu-id="6da41-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6da41-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6da41-134">See also</span></span>



[<span data-ttu-id="6da41-135">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6da41-135">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="6da41-136">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="6da41-136">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="6da41-137">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="6da41-137">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

