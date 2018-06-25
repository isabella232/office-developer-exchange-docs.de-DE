---
title: IsRecurring (CalendarEventDetails)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsRecurring
api_type:
- schema
ms.assetid: 42323940-0ccb-4a05-86e4-262bde5e41b0
description: IsRecurring-Element gibt an, ob das Kalenderereignis eine Instanz eines sich wiederholenden Kalenderelements oder ein einzelnes Kalenderelement ist.
ms.openlocfilehash: 87a168dc48bdd5ba2ea9398dd84f696e7729db44
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830103"
---
# <a name="isrecurring-calendareventdetails"></a><span data-ttu-id="fb848-103">IsRecurring (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="fb848-103">IsRecurring (CalendarEventDetails)</span></span>

<span data-ttu-id="fb848-104">**IsRecurring** -Element gibt an, ob das Kalenderereignis eine Instanz eines sich wiederholenden Kalenderelements oder ein einzelnes Kalenderelement ist.</span><span class="sxs-lookup"><span data-stu-id="fb848-104">The **IsRecurring** element indicates whether the calendar event is an instance of a recurring calendar item or a single calendar item.</span></span> 
  
[<span data-ttu-id="fb848-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="fb848-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="fb848-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="fb848-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="fb848-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="fb848-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="fb848-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="fb848-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="fb848-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="fb848-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="fb848-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="fb848-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="fb848-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="fb848-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
[<span data-ttu-id="fb848-112">IsRecurring (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="fb848-112">IsRecurring (CalendarEventDetails)</span></span>](isrecurring-calendareventdetails.md)
  
```xml
<IsRecurring>true or false</IsRecurring>
```

 <span data-ttu-id="fb848-113">**boolean**</span><span class="sxs-lookup"><span data-stu-id="fb848-113">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fb848-114">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fb848-114">Attributes and elements</span></span>

<span data-ttu-id="fb848-115">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fb848-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fb848-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="fb848-116">Attributes</span></span>

<span data-ttu-id="fb848-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="fb848-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fb848-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fb848-118">Child elements</span></span>

<span data-ttu-id="fb848-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="fb848-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fb848-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fb848-120">Parent elements</span></span>

|<span data-ttu-id="fb848-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="fb848-121">**Element**</span></span>|<span data-ttu-id="fb848-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fb848-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fb848-123">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="fb848-123">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="fb848-124">Zusätzliche Informationen zu einem Kalenderereignis.</span><span class="sxs-lookup"><span data-stu-id="fb848-124">Provides additional information about a calendar event.</span></span>  <br/> <span data-ttu-id="fb848-125">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="fb848-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]/CalendarEventDetails` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fb848-126">Textwert</span><span class="sxs-lookup"><span data-stu-id="fb848-126">Text value</span></span>

<span data-ttu-id="fb848-127">Ein Textwert ist erforderlich, wenn dieses Element in der Antwort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fb848-127">A text value is required if this element is returned in the response.</span></span> <span data-ttu-id="fb848-128">Dieses Element ist erforderlich, wenn das [CalendarEventDetails](calendareventdetails.md) -Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fb848-128">This element is required if the [CalendarEventDetails](calendareventdetails.md) element is used.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fb848-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fb848-129">Remarks</span></span>

<span data-ttu-id="fb848-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="fb848-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fb848-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="fb848-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fb848-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="fb848-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fb848-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fb848-133">Schema Name</span></span>  <br/> |<span data-ttu-id="fb848-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="fb848-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="fb848-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fb848-135">Validation File</span></span>  <br/> |<span data-ttu-id="fb848-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fb848-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fb848-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="fb848-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="fb848-138">False</span><span class="sxs-lookup"><span data-stu-id="fb848-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fb848-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb848-139">See also</span></span>



[<span data-ttu-id="fb848-140">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="fb848-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="fb848-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="fb848-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="fb848-142">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="fb848-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

