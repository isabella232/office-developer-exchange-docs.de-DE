---
title: IsPrivate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsPrivate
api_type:
- schema
ms.assetid: 1712bc94-9789-4507-8521-bde1be51e331
description: Das IsPrivate-Element gibt an, ob das Kalenderelement privat ist.
ms.openlocfilehash: 37c0357b3eab2314ee74e1c98287b3dc05a3bf26
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830095"
---
# <a name="isprivate"></a><span data-ttu-id="778d7-103">IsPrivate</span><span class="sxs-lookup"><span data-stu-id="778d7-103">IsPrivate</span></span>

<span data-ttu-id="778d7-104">Das **IsPrivate** -Element gibt an, ob das Kalenderelement privat ist.</span><span class="sxs-lookup"><span data-stu-id="778d7-104">The **IsPrivate** element indicates whether the calendar item is private.</span></span> 
  
[<span data-ttu-id="778d7-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="778d7-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="778d7-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="778d7-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="778d7-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="778d7-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="778d7-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="778d7-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="778d7-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="778d7-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="778d7-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="778d7-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="778d7-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="778d7-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
[<span data-ttu-id="778d7-112">IsPrivate</span><span class="sxs-lookup"><span data-stu-id="778d7-112">IsPrivate</span></span>](isprivate.md)
  
```xml
<IsPrivate>true or false</IsPrivate>
```

 <span data-ttu-id="778d7-113">**boolean**</span><span class="sxs-lookup"><span data-stu-id="778d7-113">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="778d7-114">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="778d7-114">Attributes and elements</span></span>

<span data-ttu-id="778d7-115">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="778d7-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="778d7-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="778d7-116">Attributes</span></span>

<span data-ttu-id="778d7-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="778d7-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="778d7-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="778d7-118">Child elements</span></span>

<span data-ttu-id="778d7-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="778d7-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="778d7-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="778d7-120">Parent elements</span></span>

|<span data-ttu-id="778d7-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="778d7-121">**Element**</span></span>|<span data-ttu-id="778d7-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="778d7-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="778d7-123">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="778d7-123">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="778d7-124">Zusätzliche Informationen zu einem Kalenderereignis.</span><span class="sxs-lookup"><span data-stu-id="778d7-124">Provides additional information about a calendar event.</span></span>  <br/> <span data-ttu-id="778d7-125">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="778d7-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]/CalendarEventDetails` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="778d7-126">Textwert</span><span class="sxs-lookup"><span data-stu-id="778d7-126">Text value</span></span>

<span data-ttu-id="778d7-127">Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="778d7-127">A text value that represents a Boolean value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="778d7-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="778d7-128">Remarks</span></span>

<span data-ttu-id="778d7-129">Wenn dieses Element verwendet wird, werden die anderen Elemente im [CalendarEventDetails](calendareventdetails.md) -Element nicht in der Antwort enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="778d7-129">If this element is used, the other elements in the [CalendarEventDetails](calendareventdetails.md) element will not be included in the response.</span></span> 
  
<span data-ttu-id="778d7-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="778d7-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="778d7-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="778d7-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="778d7-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="778d7-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="778d7-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="778d7-133">Schema Name</span></span>  <br/> |<span data-ttu-id="778d7-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="778d7-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="778d7-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="778d7-135">Validation File</span></span>  <br/> |<span data-ttu-id="778d7-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="778d7-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="778d7-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="778d7-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="778d7-138">False</span><span class="sxs-lookup"><span data-stu-id="778d7-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="778d7-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="778d7-139">See also</span></span>



[<span data-ttu-id="778d7-140">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="778d7-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="778d7-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="778d7-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="778d7-142">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="778d7-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

