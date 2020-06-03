---
title: TimeWindow
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeWindow
api_type:
- schema
ms.assetid: 49c79266-353a-4036-a8e2-8a4660d0d8ea
description: Das Window-Element gibt die Zeitspanne an, die für die Informationen zur Benutzerverfügbarkeit abgefragt wird.
ms.openlocfilehash: 5c66614520f9d616687d67ad609b3d55d9cf6571
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458929"
---
# <a name="timewindow"></a><span data-ttu-id="3dd98-103">TimeWindow</span><span class="sxs-lookup"><span data-stu-id="3dd98-103">TimeWindow</span></span>

<span data-ttu-id="3dd98-104">Das **Window** -Element gibt die Zeitspanne an, die für die Informationen zur Benutzerverfügbarkeit abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="3dd98-104">The **TimeWindow** element identifies the time span queried for the user availability information.</span></span> 
  
[<span data-ttu-id="3dd98-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="3dd98-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="3dd98-106">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="3dd98-106">FreeBusyViewOptions</span></span>](freebusyviewoptions.md)
  
[<span data-ttu-id="3dd98-107">TimeWindow</span><span class="sxs-lookup"><span data-stu-id="3dd98-107">TimeWindow</span></span>](timewindow.md)
  
```xml
<TimeWindow>
   <StartTime>dateTime</StartTime>
   <EndTime>dateTime</EndTime>
</TimeWindow>
```

 <span data-ttu-id="3dd98-108">**Duration**</span><span class="sxs-lookup"><span data-stu-id="3dd98-108">**Duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3dd98-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3dd98-109">Attributes and elements</span></span>

<span data-ttu-id="3dd98-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3dd98-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3dd98-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="3dd98-111">Attributes</span></span>

<span data-ttu-id="3dd98-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="3dd98-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3dd98-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3dd98-113">Child elements</span></span>

|<span data-ttu-id="3dd98-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="3dd98-114">**Element**</span></span>|<span data-ttu-id="3dd98-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3dd98-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3dd98-116">StartTime</span><span class="sxs-lookup"><span data-stu-id="3dd98-116">StartTime</span></span>](starttime.md) <br/> |<span data-ttu-id="3dd98-117">Stellt den Beginn einer Zeitspanne dar, die für die Informationen zur Benutzerverfügbarkeit abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="3dd98-117">Represents the start of a time span queried for the user availability information.</span></span>  <br/> |
|[<span data-ttu-id="3dd98-118">EndTime</span><span class="sxs-lookup"><span data-stu-id="3dd98-118">EndTime</span></span>](endtime.md) <br/> |<span data-ttu-id="3dd98-119">Stellt das Ende einer Zeitspanne dar, die für die Informationen zur Benutzerverfügbarkeit abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="3dd98-119">Represents the end of a time span queried for the user availability information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3dd98-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3dd98-120">Parent elements</span></span>

|<span data-ttu-id="3dd98-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="3dd98-121">**Element**</span></span>|<span data-ttu-id="3dd98-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3dd98-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3dd98-123">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="3dd98-123">FreeBusyViewOptions</span></span>](freebusyviewoptions.md) <br/> |<span data-ttu-id="3dd98-124">Gibt den Typ der Frei/Gebucht-Informationen an, die in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3dd98-124">Specifies the type of free/busy information returned in the response.</span></span>  <br/> <span data-ttu-id="3dd98-125">Es folgt der XPath für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="3dd98-125">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3dd98-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3dd98-126">Remarks</span></span>

<span data-ttu-id="3dd98-127">Der maximale Wert für diesen Zeitraum beträgt 42 Tage.</span><span class="sxs-lookup"><span data-stu-id="3dd98-127">The maximum value for this time period is 42 days.</span></span> <span data-ttu-id="3dd98-128">Dieser Maximalwert kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3dd98-128">This maximum value can be modified.</span></span> <span data-ttu-id="3dd98-129">Bei Anforderungen für Benutzer Verfügbarkeitsinformationen, die über den Maximalwert hinausgehen, wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3dd98-129">Any requests for user availability information beyond the maximum value will return an error.</span></span> <span data-ttu-id="3dd98-130">Wenn Termine teilweise in der von den Elementen "StartTime" [und "](starttime.md) [EndTime](endtime.md) " definierten Zeitspanne liegen, ist dieser Termin vollständig enthalten.</span><span class="sxs-lookup"><span data-stu-id="3dd98-130">If any appointments are partially in the time span defined by the [StartTime](starttime.md) and [EndTime](endtime.md) elements, that appointment is included in its entirety.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3dd98-131">Das Schema, das dieses Element beschreibt, befindet sich im/EWS/"aus-Verzeichnis des Computers, auf dem Microsoft® Exchange Server 2007 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3dd98-131">The schema that describes this element is located in the /EWS/ directory of the computer that is running Microsoft® Exchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="3dd98-132">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3dd98-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3dd98-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="3dd98-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3dd98-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3dd98-134">Schema Name</span></span>  <br/> |<span data-ttu-id="3dd98-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3dd98-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="3dd98-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3dd98-136">Validation File</span></span>  <br/> |<span data-ttu-id="3dd98-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3dd98-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3dd98-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3dd98-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="3dd98-139">False</span><span class="sxs-lookup"><span data-stu-id="3dd98-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3dd98-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3dd98-140">See also</span></span>



[<span data-ttu-id="3dd98-141">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3dd98-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="3dd98-142">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="3dd98-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

