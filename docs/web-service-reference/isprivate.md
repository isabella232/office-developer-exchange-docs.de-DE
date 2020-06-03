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
ms.openlocfilehash: c36c659414700439436cd2ca903e443164c1473b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457802"
---
# <a name="isprivate"></a><span data-ttu-id="00a7d-103">IsPrivate</span><span class="sxs-lookup"><span data-stu-id="00a7d-103">IsPrivate</span></span>

<span data-ttu-id="00a7d-104">Das **IsPrivate** -Element gibt an, ob das Kalenderelement privat ist.</span><span class="sxs-lookup"><span data-stu-id="00a7d-104">The **IsPrivate** element indicates whether the calendar item is private.</span></span> 
  
[<span data-ttu-id="00a7d-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="00a7d-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="00a7d-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="00a7d-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="00a7d-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="00a7d-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="00a7d-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="00a7d-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="00a7d-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="00a7d-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="00a7d-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="00a7d-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="00a7d-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="00a7d-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
[<span data-ttu-id="00a7d-112">IsPrivate</span><span class="sxs-lookup"><span data-stu-id="00a7d-112">IsPrivate</span></span>](isprivate.md)
  
```xml
<IsPrivate>true or false</IsPrivate>
```

 <span data-ttu-id="00a7d-113">**boolean**</span><span class="sxs-lookup"><span data-stu-id="00a7d-113">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="00a7d-114">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="00a7d-114">Attributes and elements</span></span>

<span data-ttu-id="00a7d-115">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="00a7d-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="00a7d-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="00a7d-116">Attributes</span></span>

<span data-ttu-id="00a7d-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="00a7d-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="00a7d-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="00a7d-118">Child elements</span></span>

<span data-ttu-id="00a7d-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="00a7d-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="00a7d-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="00a7d-120">Parent elements</span></span>

|<span data-ttu-id="00a7d-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="00a7d-121">**Element**</span></span>|<span data-ttu-id="00a7d-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="00a7d-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="00a7d-123">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="00a7d-123">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="00a7d-124">Enthält zusätzliche Informationen zu einem Kalenderereignis.</span><span class="sxs-lookup"><span data-stu-id="00a7d-124">Provides additional information about a calendar event.</span></span>  <br/> <span data-ttu-id="00a7d-125">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="00a7d-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]/CalendarEventDetails` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="00a7d-126">Textwert</span><span class="sxs-lookup"><span data-stu-id="00a7d-126">Text value</span></span>

<span data-ttu-id="00a7d-127">Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="00a7d-127">A text value that represents a Boolean value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="00a7d-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00a7d-128">Remarks</span></span>

<span data-ttu-id="00a7d-129">Wenn dieses Element verwendet wird, werden die anderen Elemente im [CalendarEventDetails](calendareventdetails.md) -Element in der Antwort nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="00a7d-129">If this element is used, the other elements in the [CalendarEventDetails](calendareventdetails.md) element will not be included in the response.</span></span> 
  
<span data-ttu-id="00a7d-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="00a7d-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="00a7d-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="00a7d-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="00a7d-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="00a7d-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="00a7d-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="00a7d-133">Schema Name</span></span>  <br/> |<span data-ttu-id="00a7d-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="00a7d-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="00a7d-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="00a7d-135">Validation File</span></span>  <br/> |<span data-ttu-id="00a7d-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="00a7d-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="00a7d-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="00a7d-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="00a7d-138">False</span><span class="sxs-lookup"><span data-stu-id="00a7d-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="00a7d-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00a7d-139">See also</span></span>



[<span data-ttu-id="00a7d-140">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="00a7d-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="00a7d-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="00a7d-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="00a7d-142">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="00a7d-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

