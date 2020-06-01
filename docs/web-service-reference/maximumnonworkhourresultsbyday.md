---
title: MaximumNonWorkHourResultsByDay
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MaximumNonWorkHourResultsByDay
api_type:
- schema
ms.assetid: 9fb7314d-779c-4b1f-9d7c-b5cb092ed134
description: Das MaximumNonWorkHourResultsByDay-Element gibt die Anzahl der vorgeschlagenen Ergebnisse für Besprechungszeiten außerhalb regulärer Arbeitsstunden pro Tag an.
ms.openlocfilehash: 410d6bd84838d979af6bc53ca47f445ae55a09e6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465499"
---
# <a name="maximumnonworkhourresultsbyday"></a><span data-ttu-id="0e137-103">MaximumNonWorkHourResultsByDay</span><span class="sxs-lookup"><span data-stu-id="0e137-103">MaximumNonWorkHourResultsByDay</span></span>

<span data-ttu-id="0e137-104">Das **MaximumNonWorkHourResultsByDay** -Element gibt die Anzahl der vorgeschlagenen Ergebnisse für Besprechungszeiten außerhalb regulärer Arbeitsstunden pro Tag an.</span><span class="sxs-lookup"><span data-stu-id="0e137-104">The **MaximumNonWorkHourResultsByDay** element specifies the number of suggested results for meeting times outside regular working hours per day.</span></span> 
  
[<span data-ttu-id="0e137-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="0e137-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="0e137-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="0e137-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
[<span data-ttu-id="0e137-107">MaximumNonWorkHourResultsByDay</span><span class="sxs-lookup"><span data-stu-id="0e137-107">MaximumNonWorkHourResultsByDay</span></span>](maximumnonworkhourresultsbyday.md)
  
```xml
<MaximumNonWorkHourResultsByDay>...</MaximumNonWorkHourResultsByDay>
```

 <span data-ttu-id="0e137-108">**int**</span><span class="sxs-lookup"><span data-stu-id="0e137-108">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0e137-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0e137-109">Attributes and elements</span></span>

<span data-ttu-id="0e137-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0e137-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0e137-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="0e137-111">Attributes</span></span>

<span data-ttu-id="0e137-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="0e137-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0e137-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0e137-113">Child elements</span></span>

<span data-ttu-id="0e137-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="0e137-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0e137-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0e137-115">Parent elements</span></span>

|<span data-ttu-id="0e137-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="0e137-116">**Element**</span></span>|<span data-ttu-id="0e137-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0e137-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0e137-118">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="0e137-118">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="0e137-119">Enthält die Optionen zum Abrufen von Informationen zu Besprechungs Vorschlägen.</span><span class="sxs-lookup"><span data-stu-id="0e137-119">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="0e137-120">Es folgt der XPath für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="0e137-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0e137-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="0e137-121">Text value</span></span>

<span data-ttu-id="0e137-122">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0e137-122">A text value is required.</span></span> <span data-ttu-id="0e137-123">Der Wert Text stellt eine ganze Zahl dar.</span><span class="sxs-lookup"><span data-stu-id="0e137-123">The text value represents an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0e137-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e137-124">Remarks</span></span>

<span data-ttu-id="0e137-125">Dieses Element ist erforderlich, wenn das [SuggestionsViewOptions](suggestionsviewoptions.md) -Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0e137-125">This element is required if the [SuggestionsViewOptions](suggestionsviewoptions.md) element is used.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0e137-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="0e137-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="0e137-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="0e137-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0e137-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="0e137-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0e137-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0e137-129">Schema Name</span></span>  <br/> |<span data-ttu-id="0e137-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="0e137-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="0e137-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0e137-131">Validation File</span></span>  <br/> |<span data-ttu-id="0e137-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0e137-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0e137-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0e137-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="0e137-134">False</span><span class="sxs-lookup"><span data-stu-id="0e137-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0e137-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e137-135">See also</span></span>



[<span data-ttu-id="0e137-136">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0e137-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="0e137-137">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="0e137-137">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

