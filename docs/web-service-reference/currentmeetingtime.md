---
title: CurrentMeetingTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CurrentMeetingTime
api_type:
- schema
ms.assetid: 1ff68154-24b5-465a-a31c-3d3bab0d491e
description: Das Element CurrentMeetingTime stellt die Anfangszeit der eine Besprechung, die Sie mit einer von einem Besprechungsteilnehmer vorgeschlagenen Besprechungszeit aktualisieren möchten.
ms.openlocfilehash: 88adbe566270d759986e9b55afd4827c0513ca43
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757824"
---
# <a name="currentmeetingtime"></a><span data-ttu-id="484dd-103">CurrentMeetingTime</span><span class="sxs-lookup"><span data-stu-id="484dd-103">CurrentMeetingTime</span></span>

<span data-ttu-id="484dd-104">Das Element **CurrentMeetingTime** stellt die Anfangszeit der eine Besprechung, die Sie mit einer von einem Besprechungsteilnehmer vorgeschlagenen Besprechungszeit aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="484dd-104">The **CurrentMeetingTime** element represents the start time of a meeting that you want to update with a meeting time proposed by a meeting attendee.</span></span> 
  
[<span data-ttu-id="484dd-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="484dd-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="484dd-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="484dd-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
[<span data-ttu-id="484dd-107">CurrentMeetingTime</span><span class="sxs-lookup"><span data-stu-id="484dd-107">CurrentMeetingTime</span></span>](currentmeetingtime.md)
  
```xml
<CurrentMeetingTime>...</CurrentMeetingTime>
```

 <span data-ttu-id="484dd-108">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="484dd-108">**DateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="484dd-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="484dd-109">Attributes and elements</span></span>

<span data-ttu-id="484dd-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="484dd-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="484dd-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="484dd-111">Attributes</span></span>

<span data-ttu-id="484dd-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="484dd-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="484dd-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="484dd-113">Child elements</span></span>

<span data-ttu-id="484dd-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="484dd-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="484dd-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="484dd-115">Parent elements</span></span>

|<span data-ttu-id="484dd-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="484dd-116">**Element**</span></span>|<span data-ttu-id="484dd-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="484dd-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="484dd-118">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="484dd-118">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="484dd-119">Enthält die Optionen zum Abrufen von Besprechungsinformationen Vorschlag.</span><span class="sxs-lookup"><span data-stu-id="484dd-119">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="484dd-120">Es folgt der XPath-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="484dd-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="484dd-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="484dd-121">Remarks</span></span>

<span data-ttu-id="484dd-122">Dieses Element ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="484dd-122">This element is not required.</span></span>
  
> [!NOTE]
> <span data-ttu-id="484dd-123">Das Schema, das dieses Element beschreibt befindet sich im Verzeichnis /EWS/ des Computers, auf dem MicrosoftExchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="484dd-123">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="484dd-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="484dd-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="484dd-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="484dd-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="484dd-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="484dd-126">Schema Name</span></span>  <br/> |<span data-ttu-id="484dd-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="484dd-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="484dd-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="484dd-128">Validation File</span></span>  <br/> |<span data-ttu-id="484dd-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="484dd-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="484dd-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="484dd-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="484dd-131">False</span><span class="sxs-lookup"><span data-stu-id="484dd-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="484dd-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="484dd-132">See also</span></span>



[<span data-ttu-id="484dd-133">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="484dd-133">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="484dd-134">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="484dd-134">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

