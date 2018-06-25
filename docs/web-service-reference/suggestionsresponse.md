---
title: SuggestionsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuggestionsResponse
api_type:
- schema
ms.assetid: d25ca143-f80c-4458-b669-346fda29a5a7
description: Das SuggestionsResponse-Element enthält Antwort Status Vorschlag und Daten für die angeforderte Besprechungsvorschläge.
ms.openlocfilehash: 614b58a1df8e340c6be468ccddd3b37537d32591
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839138"
---
# <a name="suggestionsresponse"></a><span data-ttu-id="af508-103">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="af508-103">SuggestionsResponse</span></span>

<span data-ttu-id="af508-104">Das **SuggestionsResponse** -Element enthält Antwort Status Vorschlag und Daten für die angeforderte Besprechungsvorschläge.</span><span class="sxs-lookup"><span data-stu-id="af508-104">The **SuggestionsResponse** element contains response status information and suggestion data for requested meeting suggestions.</span></span> 
  
[<span data-ttu-id="af508-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="af508-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="af508-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="af508-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
```xml
<SuggestionsResponse>
   <ResponseMessage>...</ResponseMessage>
   <SuggestionDayResultArray>...</SuggestionDayResultArray>
</SuggestionsResponse>
```

 <span data-ttu-id="af508-107">**SuggestionsResponseType**</span><span class="sxs-lookup"><span data-stu-id="af508-107">**SuggestionsResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="af508-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="af508-108">Attributes and elements</span></span>

<span data-ttu-id="af508-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="af508-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="af508-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="af508-110">Attributes</span></span>

<span data-ttu-id="af508-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="af508-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="af508-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="af508-112">Child elements</span></span>

|<span data-ttu-id="af508-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="af508-113">**Element**</span></span>|<span data-ttu-id="af508-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="af508-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af508-115">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="af508-115">ResponseMessage</span></span>](responsemessage.md) <br/> |<span data-ttu-id="af508-116">Enthält beschreibende Informationen über den Antwortstatus.</span><span class="sxs-lookup"><span data-stu-id="af508-116">Provides descriptive information about the response status.</span></span>  <br/> |
|[<span data-ttu-id="af508-117">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="af508-117">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md) <br/> |<span data-ttu-id="af508-118">Enthält ein Array von besprechungsvorschlägen nach Datum organisiert.</span><span class="sxs-lookup"><span data-stu-id="af508-118">Contains an array of meeting suggestions organized by date.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="af508-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="af508-119">Parent elements</span></span>

|<span data-ttu-id="af508-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="af508-120">**Element**</span></span>|<span data-ttu-id="af508-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="af508-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af508-122">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="af508-122">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md) <br/> |<span data-ttu-id="af508-123">Enthält Informationen zur Verfügbarkeit der angeforderten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="af508-123">Contains the requested users' availability information.</span></span>  <br/> <span data-ttu-id="af508-124">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="af508-124">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af508-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="af508-125">Remarks</span></span>

<span data-ttu-id="af508-126">Dieses Element ist nicht in einer Antwort GetUserAvailability enthalten, wenn [SuggestionsViewOptions](suggestionsviewoptions.md) nicht in der Besprechungsanfrage GetUserAvailability festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="af508-126">This element is not included in a GetUserAvailability response if [SuggestionsViewOptions](suggestionsviewoptions.md) is not set in the GetUserAvailability request message.</span></span> 
  
<span data-ttu-id="af508-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="af508-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="af508-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="af508-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="af508-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="af508-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="af508-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="af508-130">Schema Name</span></span>  <br/> |<span data-ttu-id="af508-131">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="af508-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="af508-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="af508-132">Validation File</span></span>  <br/> |<span data-ttu-id="af508-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="af508-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="af508-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="af508-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="af508-135">False</span><span class="sxs-lookup"><span data-stu-id="af508-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="af508-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af508-136">See also</span></span>



[<span data-ttu-id="af508-137">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="af508-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="af508-138">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="af508-138">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="af508-139">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="af508-139">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

