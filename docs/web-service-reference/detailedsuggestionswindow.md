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
description: Das DetailedSuggestionsWindow-Element gibt die Zeitspanne an, die nach detaillierten Informationen zu vorgeschlagenen Besprechungszeiten abgefragt wird.
ms.openlocfilehash: 45d582f2642c0e3d8f6330b09946230c8842618d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467844"
---
# <a name="detailedsuggestionswindow"></a><span data-ttu-id="c786a-103">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="c786a-103">DetailedSuggestionsWindow</span></span>

<span data-ttu-id="c786a-104">Das **DetailedSuggestionsWindow** -Element gibt die Zeitspanne an, die nach detaillierten Informationen zu vorgeschlagenen Besprechungszeiten abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="c786a-104">The **DetailedSuggestionsWindow** element identifies the time span that is queried for detailed information about suggested meeting times.</span></span> 
  
- [<span data-ttu-id="c786a-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="c786a-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) 
- [<span data-ttu-id="c786a-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="c786a-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) 
- [<span data-ttu-id="c786a-107">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="c786a-107">DetailedSuggestionsWindow</span></span>](detailedsuggestionswindow.md)
  
```xml
<DetailedSuggestionsWindow>
   <StartTime>...</StartTime>
   <EndTime>...</EndTime>
</DetailedSuggestionsWindow>
```

 <span data-ttu-id="c786a-108">**Duration**</span><span class="sxs-lookup"><span data-stu-id="c786a-108">**Duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c786a-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c786a-109">Attributes and elements</span></span>

<span data-ttu-id="c786a-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c786a-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c786a-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="c786a-111">Attributes</span></span>

<span data-ttu-id="c786a-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="c786a-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c786a-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c786a-113">Child elements</span></span>

|<span data-ttu-id="c786a-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="c786a-114">**Element**</span></span>|<span data-ttu-id="c786a-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c786a-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c786a-116">StartTime</span><span class="sxs-lookup"><span data-stu-id="c786a-116">StartTime</span></span>](starttime.md) <br/> |<span data-ttu-id="c786a-117">Stellt den Anfang der abgefragten Zeitspanne dar, um detaillierte Informationen zu vorgeschlagenen Besprechungszeiten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c786a-117">Represents the start of the time span queried for detailed information about suggested meeting times.</span></span>  <br/> |
|[<span data-ttu-id="c786a-118">EndTime</span><span class="sxs-lookup"><span data-stu-id="c786a-118">EndTime</span></span>](endtime.md) <br/> |<span data-ttu-id="c786a-119">Stellt das Ende der abgefragten Zeitspanne dar, um detaillierte Informationen zu vorgeschlagenen Besprechungszeiten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c786a-119">Represents the end of the time span queried for detailed information about suggested meeting times.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c786a-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c786a-120">Parent elements</span></span>

|<span data-ttu-id="c786a-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="c786a-121">**Element**</span></span>|<span data-ttu-id="c786a-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c786a-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c786a-123">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="c786a-123">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="c786a-124">Enthält die Optionen zum Abrufen von Informationen zu Besprechungs Vorschlägen.</span><span class="sxs-lookup"><span data-stu-id="c786a-124">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="c786a-125">Es folgt der XPath für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="c786a-125">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c786a-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c786a-126">Remarks</span></span>

<span data-ttu-id="c786a-127">Dieses Element ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c786a-127">This element is not required.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c786a-128">Das Schema, das dieses Element beschreibt, befindet sich im Verzeichnis/EWS/"aus des Computers mit Microsoft Exchange Server 2007, auf dem die Client Zugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="c786a-128">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="c786a-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c786a-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c786a-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="c786a-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c786a-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c786a-131">Schema Name</span></span>  <br/> |<span data-ttu-id="c786a-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c786a-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="c786a-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c786a-133">Validation File</span></span>  <br/> |<span data-ttu-id="c786a-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c786a-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c786a-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c786a-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="c786a-136">False</span><span class="sxs-lookup"><span data-stu-id="c786a-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c786a-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c786a-137">See also</span></span>

- [<span data-ttu-id="c786a-138">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c786a-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="c786a-139">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="c786a-139">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

