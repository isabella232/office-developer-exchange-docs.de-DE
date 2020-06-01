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
description: Das CurrentMeetingTime-Element stellt die Startzeit einer Besprechung dar, die Sie mit einer Besprechungszeit aktualisieren möchten, die von einem Besprechungsteilnehmer vorgeschlagen wurde.
ms.openlocfilehash: e79616fd735cbf6410e85450bd75c1276923f171
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458775"
---
# <a name="currentmeetingtime"></a><span data-ttu-id="58bc1-103">CurrentMeetingTime</span><span class="sxs-lookup"><span data-stu-id="58bc1-103">CurrentMeetingTime</span></span>

<span data-ttu-id="58bc1-104">Das **CurrentMeetingTime** -Element stellt die Startzeit einer Besprechung dar, die Sie mit einer Besprechungszeit aktualisieren möchten, die von einem Besprechungsteilnehmer vorgeschlagen wurde.</span><span class="sxs-lookup"><span data-stu-id="58bc1-104">The **CurrentMeetingTime** element represents the start time of a meeting that you want to update with a meeting time proposed by a meeting attendee.</span></span> 
  
[<span data-ttu-id="58bc1-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="58bc1-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="58bc1-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="58bc1-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
[<span data-ttu-id="58bc1-107">CurrentMeetingTime</span><span class="sxs-lookup"><span data-stu-id="58bc1-107">CurrentMeetingTime</span></span>](currentmeetingtime.md)
  
```xml
<CurrentMeetingTime>...</CurrentMeetingTime>
```

 <span data-ttu-id="58bc1-108">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="58bc1-108">**DateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="58bc1-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="58bc1-109">Attributes and elements</span></span>

<span data-ttu-id="58bc1-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="58bc1-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="58bc1-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="58bc1-111">Attributes</span></span>

<span data-ttu-id="58bc1-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="58bc1-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="58bc1-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="58bc1-113">Child elements</span></span>

<span data-ttu-id="58bc1-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="58bc1-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="58bc1-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="58bc1-115">Parent elements</span></span>

|<span data-ttu-id="58bc1-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="58bc1-116">**Element**</span></span>|<span data-ttu-id="58bc1-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="58bc1-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="58bc1-118">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="58bc1-118">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="58bc1-119">Enthält die Optionen zum Abrufen von Informationen zu Besprechungs Vorschlägen.</span><span class="sxs-lookup"><span data-stu-id="58bc1-119">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="58bc1-120">Es folgt der XPath für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="58bc1-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58bc1-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58bc1-121">Remarks</span></span>

<span data-ttu-id="58bc1-122">Dieses Element ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="58bc1-122">This element is not required.</span></span>
  
> [!NOTE]
> <span data-ttu-id="58bc1-123">Das Schema, das dieses Element beschreibt, befindet sich im Verzeichnis/EWS/"aus des Computers mit Microsoft Exchange Server 2007, auf dem die Client Zugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="58bc1-123">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="58bc1-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="58bc1-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="58bc1-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="58bc1-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="58bc1-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="58bc1-126">Schema Name</span></span>  <br/> |<span data-ttu-id="58bc1-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="58bc1-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="58bc1-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="58bc1-128">Validation File</span></span>  <br/> |<span data-ttu-id="58bc1-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="58bc1-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="58bc1-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="58bc1-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="58bc1-131">False</span><span class="sxs-lookup"><span data-stu-id="58bc1-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="58bc1-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58bc1-132">See also</span></span>



[<span data-ttu-id="58bc1-133">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="58bc1-133">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="58bc1-134">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="58bc1-134">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

