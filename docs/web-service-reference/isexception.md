---
title: IsException
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsException
api_type:
- schema
ms.assetid: e7bd8ae2-2643-411e-ae08-358bac445800
description: Das IsException-Element gibt an, ob das Master-Shape eine Instanz eines sich wiederholenden Kalenderelements geändert wird.
ms.openlocfilehash: bb884110fd3642bebbc03504aef369f9e0412714
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830009"
---
# <a name="isexception"></a><span data-ttu-id="54f82-103">IsException</span><span class="sxs-lookup"><span data-stu-id="54f82-103">IsException</span></span>

<span data-ttu-id="54f82-104">Das **IsException** -Element gibt an, ob das Master-Shape eine Instanz eines sich wiederholenden Kalenderelements geändert wird.</span><span class="sxs-lookup"><span data-stu-id="54f82-104">The **IsException** element indicates whether an instance of a recurring calendar item is changed from the master.</span></span> 
  
[<span data-ttu-id="54f82-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="54f82-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="54f82-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="54f82-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="54f82-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="54f82-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="54f82-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="54f82-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="54f82-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="54f82-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="54f82-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="54f82-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="54f82-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="54f82-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
[<span data-ttu-id="54f82-112">IsException</span><span class="sxs-lookup"><span data-stu-id="54f82-112">IsException</span></span>](isexception.md)
  
```xml
<IsException/>
```

 <span data-ttu-id="54f82-113">**boolean**</span><span class="sxs-lookup"><span data-stu-id="54f82-113">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="54f82-114">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="54f82-114">Attributes and elements</span></span>

<span data-ttu-id="54f82-115">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="54f82-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="54f82-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="54f82-116">Attributes</span></span>

<span data-ttu-id="54f82-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="54f82-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="54f82-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="54f82-118">Child elements</span></span>

<span data-ttu-id="54f82-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="54f82-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="54f82-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="54f82-120">Parent elements</span></span>

|<span data-ttu-id="54f82-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="54f82-121">**Element**</span></span>|<span data-ttu-id="54f82-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="54f82-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="54f82-123">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="54f82-123">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="54f82-124">Zusätzliche Informationen zu einem Kalenderereignis.</span><span class="sxs-lookup"><span data-stu-id="54f82-124">Provides additional information about a calendar event.</span></span>  <br/> <span data-ttu-id="54f82-125">Es folgt der 2.0 XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="54f82-125">The following is the XPath 2.0 expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]/CalendarEventDetails` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="54f82-126">Textwert</span><span class="sxs-lookup"><span data-stu-id="54f82-126">Text value</span></span>

<span data-ttu-id="54f82-127">Ein Textwert ist erforderlich, wenn dieses Element in der Antwort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="54f82-127">A text value is required if this element is returned in the response.</span></span> <span data-ttu-id="54f82-128">Dieses Element ist erforderlich, wenn das [CalendarEventDetails](calendareventdetails.md) -Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="54f82-128">This element is required if the [CalendarEventDetails](calendareventdetails.md) element is used.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="54f82-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="54f82-129">Remarks</span></span>

<span data-ttu-id="54f82-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="54f82-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="54f82-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="54f82-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="54f82-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="54f82-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="54f82-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="54f82-133">Schema Name</span></span>  <br/> |<span data-ttu-id="54f82-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="54f82-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="54f82-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="54f82-135">Validation File</span></span>  <br/> |<span data-ttu-id="54f82-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="54f82-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="54f82-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="54f82-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="54f82-138">False</span><span class="sxs-lookup"><span data-stu-id="54f82-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="54f82-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54f82-139">See also</span></span>



[<span data-ttu-id="54f82-140">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="54f82-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="54f82-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="54f82-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="54f82-142">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="54f82-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

