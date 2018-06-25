---
title: DetailedSuggestionsWindow
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DetailedSuggestionsWindow
api_type:
- schema
ms.assetid: 7b348d63-6a7d-45f4-9562-5c42243d63a5
description: Das DetailedSuggestionsWindow-Element gibt die Zeitspanne, die ausführliche Informationen zum vorgeschlagenen Besprechungszeiten abgefragt wird.
ms.openlocfilehash: 8a3af0178d0c96b50f4dd641716a9f7a7be8f7a2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757966"
---
# <a name="detailedsuggestionswindow"></a><span data-ttu-id="6dc11-103">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="6dc11-103">DetailedSuggestionsWindow</span></span>

<span data-ttu-id="6dc11-104">Das **DetailedSuggestionsWindow** -Element gibt die Zeitspanne, die ausführliche Informationen zum vorgeschlagenen Besprechungszeiten abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="6dc11-104">The **DetailedSuggestionsWindow** element identifies the time span that is queried for detailed information about suggested meeting times.</span></span> 
  
- [<span data-ttu-id="6dc11-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="6dc11-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) 
- [<span data-ttu-id="6dc11-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="6dc11-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) 
- [<span data-ttu-id="6dc11-107">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="6dc11-107">DetailedSuggestionsWindow</span></span>](detailedsuggestionswindow.md)
  
```xml
<DetailedSuggestionsWindow>
   <StartTime>...</StartTime>
   <EndTime>...</EndTime>
</DetailedSuggestionsWindow>
```

 <span data-ttu-id="6dc11-108">**Duration**</span><span class="sxs-lookup"><span data-stu-id="6dc11-108">**Duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6dc11-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6dc11-109">Attributes and elements</span></span>

<span data-ttu-id="6dc11-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6dc11-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6dc11-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="6dc11-111">Attributes</span></span>

<span data-ttu-id="6dc11-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="6dc11-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6dc11-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6dc11-113">Child elements</span></span>

|<span data-ttu-id="6dc11-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="6dc11-114">**Element**</span></span>|<span data-ttu-id="6dc11-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6dc11-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6dc11-116">StartTime</span><span class="sxs-lookup"><span data-stu-id="6dc11-116">StartTime</span></span>](starttime.md) <br/> |<span data-ttu-id="6dc11-117">Stellt den Anfang des Zeitraums ausführliche Informationen zum vorgeschlagenen Besprechungszeiten abgefragt.</span><span class="sxs-lookup"><span data-stu-id="6dc11-117">Represents the start of the time span queried for detailed information about suggested meeting times.</span></span>  <br/> |
|[<span data-ttu-id="6dc11-118">EndTime</span><span class="sxs-lookup"><span data-stu-id="6dc11-118">EndTime</span></span>](endtime.md) <br/> |<span data-ttu-id="6dc11-119">Stellt das Ende des Zeitraums ausführliche Informationen zum vorgeschlagenen Besprechungszeiten abgefragt.</span><span class="sxs-lookup"><span data-stu-id="6dc11-119">Represents the end of the time span queried for detailed information about suggested meeting times.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6dc11-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6dc11-120">Parent elements</span></span>

|<span data-ttu-id="6dc11-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="6dc11-121">**Element**</span></span>|<span data-ttu-id="6dc11-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6dc11-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6dc11-123">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="6dc11-123">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="6dc11-124">Enthält die Optionen zum Abrufen von Besprechungsinformationen Vorschlag.</span><span class="sxs-lookup"><span data-stu-id="6dc11-124">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="6dc11-125">Es folgt der XPath-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="6dc11-125">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6dc11-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6dc11-126">Remarks</span></span>

<span data-ttu-id="6dc11-127">Dieses Element ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6dc11-127">This element is not required.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6dc11-128">Das Schema, das dieses Element beschreibt befindet sich im Verzeichnis /EWS/ des Computers, auf dem MicrosoftExchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6dc11-128">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="6dc11-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6dc11-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6dc11-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="6dc11-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6dc11-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6dc11-131">Schema Name</span></span>  <br/> |<span data-ttu-id="6dc11-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6dc11-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="6dc11-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6dc11-133">Validation File</span></span>  <br/> |<span data-ttu-id="6dc11-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6dc11-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6dc11-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6dc11-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="6dc11-136">False</span><span class="sxs-lookup"><span data-stu-id="6dc11-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6dc11-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6dc11-137">See also</span></span>

- [<span data-ttu-id="6dc11-138">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6dc11-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="6dc11-139">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="6dc11-139">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

