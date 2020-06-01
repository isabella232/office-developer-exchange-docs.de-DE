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
description: Das SuggestionsResponse-Element enthält Antwortstatus Informationen und Vorschlagsdaten für angeforderte Besprechungsvorschläge.
ms.openlocfilehash: cba344f3f97777580c2cc6d296f110f20b550063
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466654"
---
# <a name="suggestionsresponse"></a><span data-ttu-id="e64ef-103">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="e64ef-103">SuggestionsResponse</span></span>

<span data-ttu-id="e64ef-104">Das **SuggestionsResponse** -Element enthält Antwortstatus Informationen und Vorschlagsdaten für angeforderte Besprechungsvorschläge.</span><span class="sxs-lookup"><span data-stu-id="e64ef-104">The **SuggestionsResponse** element contains response status information and suggestion data for requested meeting suggestions.</span></span> 
  
[<span data-ttu-id="e64ef-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="e64ef-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="e64ef-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="e64ef-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
```xml
<SuggestionsResponse>
   <ResponseMessage>...</ResponseMessage>
   <SuggestionDayResultArray>...</SuggestionDayResultArray>
</SuggestionsResponse>
```

 <span data-ttu-id="e64ef-107">**SuggestionsResponseType**</span><span class="sxs-lookup"><span data-stu-id="e64ef-107">**SuggestionsResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e64ef-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e64ef-108">Attributes and elements</span></span>

<span data-ttu-id="e64ef-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e64ef-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e64ef-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="e64ef-110">Attributes</span></span>

<span data-ttu-id="e64ef-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="e64ef-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e64ef-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e64ef-112">Child elements</span></span>

|<span data-ttu-id="e64ef-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e64ef-113">**Element**</span></span>|<span data-ttu-id="e64ef-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e64ef-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e64ef-115">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e64ef-115">ResponseMessage</span></span>](responsemessage.md) <br/> |<span data-ttu-id="e64ef-116">Enthält beschreibende Informationen zum Antwortstatus.</span><span class="sxs-lookup"><span data-stu-id="e64ef-116">Provides descriptive information about the response status.</span></span>  <br/> |
|[<span data-ttu-id="e64ef-117">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="e64ef-117">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md) <br/> |<span data-ttu-id="e64ef-118">Enthält ein Array von Besprechungs Vorschlägen nach Datum organisiert.</span><span class="sxs-lookup"><span data-stu-id="e64ef-118">Contains an array of meeting suggestions organized by date.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e64ef-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e64ef-119">Parent elements</span></span>

|<span data-ttu-id="e64ef-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="e64ef-120">**Element**</span></span>|<span data-ttu-id="e64ef-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e64ef-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e64ef-122">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="e64ef-122">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md) <br/> |<span data-ttu-id="e64ef-123">Enthält die Verfügbarkeitsinformationen der angeforderten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="e64ef-123">Contains the requested users' availability information.</span></span>  <br/> <span data-ttu-id="e64ef-124">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="e64ef-124">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e64ef-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e64ef-125">Remarks</span></span>

<span data-ttu-id="e64ef-126">Dieses Element ist nicht in einer GetUserAvailability-Antwort enthalten, wenn [SuggestionsViewOptions](suggestionsviewoptions.md) nicht in der GetUserAvailability-Anforderungsnachricht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e64ef-126">This element is not included in a GetUserAvailability response if [SuggestionsViewOptions](suggestionsviewoptions.md) is not set in the GetUserAvailability request message.</span></span> 
  
<span data-ttu-id="e64ef-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="e64ef-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e64ef-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e64ef-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e64ef-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="e64ef-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e64ef-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e64ef-130">Schema Name</span></span>  <br/> |<span data-ttu-id="e64ef-131">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="e64ef-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e64ef-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e64ef-132">Validation File</span></span>  <br/> |<span data-ttu-id="e64ef-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="e64ef-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e64ef-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e64ef-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="e64ef-135">False</span><span class="sxs-lookup"><span data-stu-id="e64ef-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e64ef-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e64ef-136">See also</span></span>



[<span data-ttu-id="e64ef-137">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e64ef-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="e64ef-138">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="e64ef-138">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="e64ef-139">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="e64ef-139">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

