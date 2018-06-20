---
title: MeetingDurationInMinutes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingDurationInMinutes
api_type:
- schema
ms.assetid: bb86b275-9c29-4daf-8196-8d505b87a4f4
description: Das MeetingDurationInMinutes-Element gibt die Dauer der Besprechung, die vorgeschlagen werden.
ms.openlocfilehash: 2ff60b69fb352c2ac7316f1ca231bb04da67ead2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830433"
---
# <a name="meetingdurationinminutes"></a><span data-ttu-id="1c55d-103">MeetingDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="1c55d-103">MeetingDurationInMinutes</span></span>

<span data-ttu-id="1c55d-104">Das **MeetingDurationInMinutes** -Element gibt die Dauer der Besprechung, die vorgeschlagen werden.</span><span class="sxs-lookup"><span data-stu-id="1c55d-104">The **MeetingDurationInMinutes** element specifies the duration of the meeting to be suggested.</span></span> 
  
[<span data-ttu-id="1c55d-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="1c55d-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="1c55d-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="1c55d-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
[<span data-ttu-id="1c55d-107">MeetingDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="1c55d-107">MeetingDurationInMinutes</span></span>](meetingdurationinminutes.md)
  
```xml
<MeetingDurationInMinutes>...</MeetingDurationInMinutes>
```

 <span data-ttu-id="1c55d-108">**int**</span><span class="sxs-lookup"><span data-stu-id="1c55d-108">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1c55d-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1c55d-109">Attributes and elements</span></span>

<span data-ttu-id="1c55d-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1c55d-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1c55d-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="1c55d-111">Attributes</span></span>

<span data-ttu-id="1c55d-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="1c55d-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1c55d-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1c55d-113">Child elements</span></span>

<span data-ttu-id="1c55d-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="1c55d-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1c55d-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1c55d-115">Parent elements</span></span>

|<span data-ttu-id="1c55d-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="1c55d-116">**Element**</span></span>|<span data-ttu-id="1c55d-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1c55d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1c55d-118">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="1c55d-118">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="1c55d-119">Enthält die Optionen zum Abrufen von Besprechungsinformationen Vorschlag.</span><span class="sxs-lookup"><span data-stu-id="1c55d-119">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="1c55d-120">Es folgt der XPath-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="1c55d-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1c55d-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="1c55d-121">Text value</span></span>

<span data-ttu-id="1c55d-122">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1c55d-122">A text value is required.</span></span> <span data-ttu-id="1c55d-123">Der Textwert stellt eine ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="1c55d-123">The text value represents an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1c55d-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1c55d-124">Remarks</span></span>

<span data-ttu-id="1c55d-125">Dieses Element ist erforderlich, wenn das [SuggestionsViewOptions](suggestionsviewoptions.md) -Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1c55d-125">This element is required if the [SuggestionsViewOptions](suggestionsviewoptions.md) element is used.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1c55d-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="1c55d-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="1c55d-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1c55d-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1c55d-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="1c55d-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1c55d-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1c55d-129">Schema Name</span></span>  <br/> |<span data-ttu-id="1c55d-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1c55d-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="1c55d-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1c55d-131">Validation File</span></span>  <br/> |<span data-ttu-id="1c55d-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1c55d-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1c55d-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1c55d-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="1c55d-134">False</span><span class="sxs-lookup"><span data-stu-id="1c55d-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1c55d-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c55d-135">See also</span></span>



[<span data-ttu-id="1c55d-136">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1c55d-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="1c55d-137">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="1c55d-137">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

