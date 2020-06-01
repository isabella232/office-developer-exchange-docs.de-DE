---
title: Ismeeting (CalendarEventDetails)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsMeeting
api_type:
- schema
ms.assetid: dd6900e4-e4a3-471a-909d-7240ebec501b
description: Das ismeeting-Element gibt an, ob es sich bei dem Kalenderereignis um eine Besprechung oder einen Termin handelt.
ms.openlocfilehash: b75dfba203177d6451f3847bf8d1f68014612e1c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465996"
---
# <a name="ismeeting-calendareventdetails"></a><span data-ttu-id="1f3da-103">Ismeeting (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="1f3da-103">IsMeeting (CalendarEventDetails)</span></span>

<span data-ttu-id="1f3da-104">Das **ismeeting** -Element gibt an, ob es sich bei dem Kalenderereignis um eine Besprechung oder einen Termin handelt.</span><span class="sxs-lookup"><span data-stu-id="1f3da-104">The **IsMeeting** element indicates whether the calendar event is a meeting or an appointment.</span></span> 
  
[<span data-ttu-id="1f3da-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="1f3da-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="1f3da-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="1f3da-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="1f3da-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="1f3da-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="1f3da-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="1f3da-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="1f3da-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="1f3da-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="1f3da-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="1f3da-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="1f3da-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="1f3da-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
[<span data-ttu-id="1f3da-112">Ismeeting (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="1f3da-112">IsMeeting (CalendarEventDetails)</span></span>](ismeeting-calendareventdetails.md)
  
```xml
<IsMeeting>true or false</IsMeeting>
```

 <span data-ttu-id="1f3da-113">**boolean**</span><span class="sxs-lookup"><span data-stu-id="1f3da-113">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1f3da-114">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1f3da-114">Attributes and elements</span></span>

<span data-ttu-id="1f3da-115">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1f3da-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1f3da-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="1f3da-116">Attributes</span></span>

<span data-ttu-id="1f3da-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="1f3da-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1f3da-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1f3da-118">Child elements</span></span>

<span data-ttu-id="1f3da-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="1f3da-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1f3da-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1f3da-120">Parent elements</span></span>

|<span data-ttu-id="1f3da-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="1f3da-121">**Element**</span></span>|<span data-ttu-id="1f3da-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1f3da-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1f3da-123">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="1f3da-123">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="1f3da-124">Enthält zusätzliche Informationen für ein Calendar-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1f3da-124">Provides additional information for a calendar event.</span></span>  <br/> <span data-ttu-id="1f3da-125">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="1f3da-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]/CalendarEventDetails` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1f3da-126">Textwert</span><span class="sxs-lookup"><span data-stu-id="1f3da-126">Text value</span></span>

<span data-ttu-id="1f3da-127">Ein Textwert ist erforderlich, wenn dieses Element in der Antwort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1f3da-127">A text value is required if this element is returned in the response.</span></span> <span data-ttu-id="1f3da-128">Dieses Element ist erforderlich, wenn das [CalendarEventDetails](calendareventdetails.md) -Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1f3da-128">This element is required if the [CalendarEventDetails](calendareventdetails.md) element is used.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1f3da-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f3da-129">Remarks</span></span>

<span data-ttu-id="1f3da-130">Der Unterschied zwischen einer Besprechung und einem Termin besteht darin, dass es sich bei einer Besprechung um ein Kalenderelement handelt, das Teilnehmer enthält. ein Termin ist ein Kalenderelement, das keine Teilnehmer enthält.</span><span class="sxs-lookup"><span data-stu-id="1f3da-130">The difference between a meeting and an appointment is that a meeting is a calendar item that includes attendees; an appointment is a calendar item that does not include attendees.</span></span>
  
<span data-ttu-id="1f3da-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="1f3da-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1f3da-132">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1f3da-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1f3da-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="1f3da-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1f3da-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1f3da-134">Schema Name</span></span>  <br/> |<span data-ttu-id="1f3da-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1f3da-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="1f3da-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1f3da-136">Validation File</span></span>  <br/> |<span data-ttu-id="1f3da-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1f3da-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1f3da-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1f3da-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="1f3da-139">False</span><span class="sxs-lookup"><span data-stu-id="1f3da-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1f3da-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f3da-140">See also</span></span>



[<span data-ttu-id="1f3da-141">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1f3da-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="1f3da-142">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="1f3da-142">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="1f3da-143">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="1f3da-143">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

