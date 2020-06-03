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
description: Das MeetingDurationInMinutes-Element gibt die Dauer der Besprechung an, die vorgeschlagen werden soll.
ms.openlocfilehash: b41e234be40c2ad8b28047ae2e812edfd66af644
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467487"
---
# <a name="meetingdurationinminutes"></a><span data-ttu-id="e086b-103">MeetingDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="e086b-103">MeetingDurationInMinutes</span></span>

<span data-ttu-id="e086b-104">Das **MeetingDurationInMinutes** -Element gibt die Dauer der Besprechung an, die vorgeschlagen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e086b-104">The **MeetingDurationInMinutes** element specifies the duration of the meeting to be suggested.</span></span> 
  
[<span data-ttu-id="e086b-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="e086b-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="e086b-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="e086b-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
[<span data-ttu-id="e086b-107">MeetingDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="e086b-107">MeetingDurationInMinutes</span></span>](meetingdurationinminutes.md)
  
```xml
<MeetingDurationInMinutes>...</MeetingDurationInMinutes>
```

 <span data-ttu-id="e086b-108">**int**</span><span class="sxs-lookup"><span data-stu-id="e086b-108">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e086b-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e086b-109">Attributes and elements</span></span>

<span data-ttu-id="e086b-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e086b-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e086b-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="e086b-111">Attributes</span></span>

<span data-ttu-id="e086b-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="e086b-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e086b-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e086b-113">Child elements</span></span>

<span data-ttu-id="e086b-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="e086b-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e086b-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e086b-115">Parent elements</span></span>

|<span data-ttu-id="e086b-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="e086b-116">**Element**</span></span>|<span data-ttu-id="e086b-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e086b-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e086b-118">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="e086b-118">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="e086b-119">Enthält die Optionen zum Abrufen von Informationen zu Besprechungs Vorschlägen.</span><span class="sxs-lookup"><span data-stu-id="e086b-119">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="e086b-120">Es folgt der XPath für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="e086b-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e086b-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="e086b-121">Text value</span></span>

<span data-ttu-id="e086b-122">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e086b-122">A text value is required.</span></span> <span data-ttu-id="e086b-123">Der Wert Text stellt eine ganze Zahl dar.</span><span class="sxs-lookup"><span data-stu-id="e086b-123">The text value represents an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e086b-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e086b-124">Remarks</span></span>

<span data-ttu-id="e086b-125">Dieses Element ist erforderlich, wenn das [SuggestionsViewOptions](suggestionsviewoptions.md) -Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e086b-125">This element is required if the [SuggestionsViewOptions](suggestionsviewoptions.md) element is used.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e086b-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="e086b-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="e086b-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e086b-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e086b-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="e086b-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e086b-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e086b-129">Schema Name</span></span>  <br/> |<span data-ttu-id="e086b-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e086b-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="e086b-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e086b-131">Validation File</span></span>  <br/> |<span data-ttu-id="e086b-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e086b-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e086b-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e086b-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="e086b-134">False</span><span class="sxs-lookup"><span data-stu-id="e086b-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e086b-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e086b-135">See also</span></span>



[<span data-ttu-id="e086b-136">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e086b-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="e086b-137">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="e086b-137">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

