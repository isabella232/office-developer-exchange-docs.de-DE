---
title: Zeitfenster
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
description: Das Zeitfenster-Element gibt die Zeitspanne für die Verfügbarkeit Benutzerinformationen abgefragt.
ms.openlocfilehash: 05858b4d62b72b3ff9904c90652bb1bff78ceb41
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839213"
---
# <a name="timewindow"></a><span data-ttu-id="2c302-103">Zeitfenster</span><span class="sxs-lookup"><span data-stu-id="2c302-103">TimeWindow</span></span>

<span data-ttu-id="2c302-104">Das **Zeitfenster** -Element gibt die Zeitspanne für die Verfügbarkeit Benutzerinformationen abgefragt.</span><span class="sxs-lookup"><span data-stu-id="2c302-104">The **TimeWindow** element identifies the time span queried for the user availability information.</span></span> 
  
[<span data-ttu-id="2c302-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="2c302-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="2c302-106">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="2c302-106">FreeBusyViewOptions</span></span>](freebusyviewoptions.md)
  
[<span data-ttu-id="2c302-107">Zeitfenster</span><span class="sxs-lookup"><span data-stu-id="2c302-107">TimeWindow</span></span>](timewindow.md)
  
```xml
<TimeWindow>
   <StartTime>dateTime</StartTime>
   <EndTime>dateTime</EndTime>
</TimeWindow>
```

 <span data-ttu-id="2c302-108">**Duration**</span><span class="sxs-lookup"><span data-stu-id="2c302-108">**Duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2c302-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2c302-109">Attributes and elements</span></span>

<span data-ttu-id="2c302-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2c302-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2c302-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="2c302-111">Attributes</span></span>

<span data-ttu-id="2c302-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="2c302-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2c302-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2c302-113">Child elements</span></span>

|<span data-ttu-id="2c302-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="2c302-114">**Element**</span></span>|<span data-ttu-id="2c302-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c302-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c302-116">StartTime</span><span class="sxs-lookup"><span data-stu-id="2c302-116">StartTime</span></span>](starttime.md) <br/> |<span data-ttu-id="2c302-117">Stellt den Anfang des einer bestimmten Zeitspanne für die Verfügbarkeit Benutzerinformationen abgefragt.</span><span class="sxs-lookup"><span data-stu-id="2c302-117">Represents the start of a time span queried for the user availability information.</span></span>  <br/> |
|[<span data-ttu-id="2c302-118">EndTime</span><span class="sxs-lookup"><span data-stu-id="2c302-118">EndTime</span></span>](endtime.md) <br/> |<span data-ttu-id="2c302-119">Stellt das Ende einer bestimmten Zeitspanne für die Verfügbarkeit Benutzerinformationen abgefragt.</span><span class="sxs-lookup"><span data-stu-id="2c302-119">Represents the end of a time span queried for the user availability information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2c302-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2c302-120">Parent elements</span></span>

|<span data-ttu-id="2c302-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="2c302-121">**Element**</span></span>|<span data-ttu-id="2c302-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c302-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c302-123">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="2c302-123">FreeBusyViewOptions</span></span>](freebusyviewoptions.md) <br/> |<span data-ttu-id="2c302-124">Gibt den Typ des Frei/Gebucht-Informationen in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2c302-124">Specifies the type of free/busy information returned in the response.</span></span>  <br/> <span data-ttu-id="2c302-125">Es folgt der XPath-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="2c302-125">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c302-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2c302-126">Remarks</span></span>

<span data-ttu-id="2c302-127">Der Höchstwert für diesen Zeitraum ist 42 Tage.</span><span class="sxs-lookup"><span data-stu-id="2c302-127">The maximum value for this time period is 42 days.</span></span> <span data-ttu-id="2c302-128">Dieser Höchstwert kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2c302-128">This maximum value can be modified.</span></span> <span data-ttu-id="2c302-129">Alle Anforderungen für Verfügbarkeitsinformationen für Benutzer außerhalb der Höchstwert gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="2c302-129">Any requests for user availability information beyond the maximum value will return an error.</span></span> <span data-ttu-id="2c302-130">Wenn keine Termine teilweise in die Zeitspanne, die durch die [Werte von StartTime](starttime.md) und [EndTime](endtime.md) Elemente definiert sind, ist in seiner Gesamtheit eines Termins enthalten.</span><span class="sxs-lookup"><span data-stu-id="2c302-130">If any appointments are partially in the time span defined by the [StartTime](starttime.md) and [EndTime](endtime.md) elements, that appointment is included in its entirety.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2c302-131">Das Schema, das dieses Element beschreibt befindet sich im Verzeichnis /EWS/ des Computers, auf dem Microsoft® Exchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="2c302-131">The schema that describes this element is located in the /EWS/ directory of the computer that is running Microsoft® Exchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="2c302-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2c302-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2c302-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="2c302-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2c302-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2c302-134">Schema Name</span></span>  <br/> |<span data-ttu-id="2c302-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="2c302-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="2c302-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2c302-136">Validation File</span></span>  <br/> |<span data-ttu-id="2c302-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2c302-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2c302-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2c302-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="2c302-139">False</span><span class="sxs-lookup"><span data-stu-id="2c302-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2c302-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c302-140">See also</span></span>



[<span data-ttu-id="2c302-141">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2c302-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="2c302-142">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="2c302-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

