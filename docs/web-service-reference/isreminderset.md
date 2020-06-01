---
title: Reminder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsReminderSet
api_type:
- schema
ms.assetid: 6aea4cb7-ca14-4949-8e7f-660b565f6556
description: Das Reminder-Element gibt an, ob für das Calendar-Ereignis eine Erinnerung festgelegt wurde.
ms.openlocfilehash: e2f5fa072b549bdaf636a15313e7dfe72172f768
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460337"
---
# <a name="isreminderset"></a><span data-ttu-id="39362-103">Reminder</span><span class="sxs-lookup"><span data-stu-id="39362-103">IsReminderSet</span></span>

<span data-ttu-id="39362-104">Das **Reminder** -Element gibt an, ob für das Calendar-Ereignis eine Erinnerung festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="39362-104">The **IsReminderSet** element indicates whether a reminder has been set for the calendar event.</span></span> 
  
[<span data-ttu-id="39362-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="39362-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="39362-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="39362-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="39362-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="39362-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="39362-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="39362-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="39362-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="39362-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="39362-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="39362-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="39362-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="39362-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
[<span data-ttu-id="39362-112">Reminder</span><span class="sxs-lookup"><span data-stu-id="39362-112">IsReminderSet</span></span>](isreminderset.md)
  
```xml
<IsReminderSet>true or false</IsReminderSet>
```

 <span data-ttu-id="39362-113">**boolean**</span><span class="sxs-lookup"><span data-stu-id="39362-113">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="39362-114">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="39362-114">Attributes and elements</span></span>

<span data-ttu-id="39362-115">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="39362-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="39362-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="39362-116">Attributes</span></span>

<span data-ttu-id="39362-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="39362-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="39362-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="39362-118">Child elements</span></span>

<span data-ttu-id="39362-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="39362-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="39362-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="39362-120">Parent elements</span></span>

|<span data-ttu-id="39362-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="39362-121">**Element**</span></span>|<span data-ttu-id="39362-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="39362-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39362-123">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="39362-123">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="39362-124">Enthält zusätzliche Informationen zu einem Kalenderereignis.</span><span class="sxs-lookup"><span data-stu-id="39362-124">Provides additional information about a calendar event.</span></span>  <br/> <span data-ttu-id="39362-125">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="39362-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]/CalendarEventDetails` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="39362-126">Textwert</span><span class="sxs-lookup"><span data-stu-id="39362-126">Text value</span></span>

<span data-ttu-id="39362-127">Ein Textwert ist erforderlich, wenn dieses Element in der Antwort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="39362-127">A text value is required if this element is returned in the response.</span></span> <span data-ttu-id="39362-128">Dieses Element ist erforderlich, wenn das [CalendarEventDetails](calendareventdetails.md) -Element verwendet wird, es sei denn, das [IsPrivate](isprivate.md) -Element auf **true**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="39362-128">This element is required if the [CalendarEventDetails](calendareventdetails.md) element is used unless the [IsPrivate](isprivate.md) element is set to **true**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="39362-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39362-129">Remarks</span></span>

<span data-ttu-id="39362-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="39362-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="39362-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="39362-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="39362-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="39362-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="39362-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="39362-133">Schema Name</span></span>  <br/> |<span data-ttu-id="39362-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="39362-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="39362-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="39362-135">Validation File</span></span>  <br/> |<span data-ttu-id="39362-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="39362-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="39362-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="39362-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="39362-138">False</span><span class="sxs-lookup"><span data-stu-id="39362-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="39362-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39362-139">See also</span></span>



[<span data-ttu-id="39362-140">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="39362-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="39362-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="39362-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="39362-142">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="39362-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

