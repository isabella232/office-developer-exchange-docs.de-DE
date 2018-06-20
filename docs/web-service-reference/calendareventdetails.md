---
title: CalendarEventDetails
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarEventDetails
api_type:
- schema
ms.assetid: 2dca0192-b91b-4154-aa09-84da74e875e9
description: Das Element CalendarEventDetails enthält zusätzliche Informationen zu einem Kalenderereignis.
ms.openlocfilehash: 8df4f3ed4f66c7dcba00e1f0c5b0c383075da0a0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757523"
---
# <a name="calendareventdetails"></a><span data-ttu-id="c4311-103">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="c4311-103">CalendarEventDetails</span></span>

<span data-ttu-id="c4311-104">Das Element **CalendarEventDetails** enthält zusätzliche Informationen zu einem Kalenderereignis.</span><span class="sxs-lookup"><span data-stu-id="c4311-104">The **CalendarEventDetails** element provides additional information about a calendar event.</span></span> 
  
[<span data-ttu-id="c4311-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="c4311-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="c4311-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="c4311-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="c4311-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="c4311-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="c4311-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="c4311-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="c4311-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="c4311-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="c4311-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="c4311-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="c4311-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="c4311-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
```xml
<CalendarEventDetails>
   <ID/>
   <Subject/>
   <Location/>
   <IsMeeting/>
   <IsRecurring/>
   <IsException/>
   <IsReminderSet/>
   <IsPrivate/>
</CalendarEventDetails>
```

 <span data-ttu-id="c4311-112">**CalendarEventDetails**</span><span class="sxs-lookup"><span data-stu-id="c4311-112">**CalendarEventDetails**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c4311-113">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c4311-113">Attributes and elements</span></span>

<span data-ttu-id="c4311-114">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c4311-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c4311-115">Attribute</span><span class="sxs-lookup"><span data-stu-id="c4311-115">Attributes</span></span>

<span data-ttu-id="c4311-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="c4311-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c4311-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c4311-117">Child elements</span></span>

|<span data-ttu-id="c4311-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="c4311-118">**Element**</span></span>|<span data-ttu-id="c4311-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c4311-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4311-120">ID</span><span class="sxs-lookup"><span data-stu-id="c4311-120">ID</span></span>](id.md) <br/> |<span data-ttu-id="c4311-121">Stellt die Eintrags-ID des Kalenderelements an.</span><span class="sxs-lookup"><span data-stu-id="c4311-121">Represents the entry ID of the calendar item.</span></span>  <br/> |
|[<span data-ttu-id="c4311-122">Betreff (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="c4311-122">Subject (CalendarEventDetails)</span></span>](subject-calendareventdetails.md) <br/> |<span data-ttu-id="c4311-123">Stellt den Betreff des Kalenderelements an.</span><span class="sxs-lookup"><span data-stu-id="c4311-123">Represents the subject of the calendar item.</span></span>  <br/> |
|[<span data-ttu-id="c4311-124">Speicherort (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="c4311-124">Location (CalendarEventDetails)</span></span>](location-calendareventdetails.md) <br/> |<span data-ttu-id="c4311-125">Stellt die Position des Kalenderelements.</span><span class="sxs-lookup"><span data-stu-id="c4311-125">Represents the location field of the calendar item.</span></span>  <br/> |
|[<span data-ttu-id="c4311-126">IsMeeting (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="c4311-126">IsMeeting (CalendarEventDetails)</span></span>](ismeeting-calendareventdetails.md) <br/> |<span data-ttu-id="c4311-127">Gibt an, ob das Kalenderereignis gehört zu einer Besprechung oder eines Termins.</span><span class="sxs-lookup"><span data-stu-id="c4311-127">Indicates whether the calendar event is a meeting or an appointment.</span></span>  <br/> |
|[<span data-ttu-id="c4311-128">IsRecurring (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="c4311-128">IsRecurring (CalendarEventDetails)</span></span>](isrecurring-calendareventdetails.md) <br/> |<span data-ttu-id="c4311-129">Gibt an, ob das Kalenderereignis eine Instanz eines sich wiederholenden Kalenderelements oder ein einzelnes Kalenderelement ist.</span><span class="sxs-lookup"><span data-stu-id="c4311-129">Indicates whether the calendar event is an instance of a recurring calendar item or a single calendar item.</span></span>  <br/> |
|[<span data-ttu-id="c4311-130">IsException</span><span class="sxs-lookup"><span data-stu-id="c4311-130">IsException</span></span>](isexception.md) <br/> |<span data-ttu-id="c4311-131">Gibt an, ob eine Instanz eines sich wiederholenden Kalenderelements aus der Master-Shapes geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c4311-131">Indicates whether an instance of a recurring calendar item is changed from the master.</span></span>  <br/> |
|[<span data-ttu-id="c4311-132">IsReminderSet</span><span class="sxs-lookup"><span data-stu-id="c4311-132">IsReminderSet</span></span>](isreminderset.md) <br/> |<span data-ttu-id="c4311-133">Gibt an, ob eine Erinnerung für das Ereignis festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="c4311-133">Indicates whether a reminder has been set for the calendar event.</span></span>  <br/> |
|[<span data-ttu-id="c4311-134">IsPrivate</span><span class="sxs-lookup"><span data-stu-id="c4311-134">IsPrivate</span></span>](isprivate.md) <br/> |<span data-ttu-id="c4311-135">Gibt an, ob das Kalenderelement privat ist.</span><span class="sxs-lookup"><span data-stu-id="c4311-135">Indicates whether the calendar item is private.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c4311-136">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c4311-136">Parent elements</span></span>

|<span data-ttu-id="c4311-137">**Element**</span><span class="sxs-lookup"><span data-stu-id="c4311-137">**Element**</span></span>|<span data-ttu-id="c4311-138">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c4311-138">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4311-139">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="c4311-139">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="c4311-140">Stellt eine einzelne Kalender Element vorkommen.</span><span class="sxs-lookup"><span data-stu-id="c4311-140">Represents a unique calendar item occurrence.</span></span>  <br/> <span data-ttu-id="c4311-141">Es folgt der 2.0 XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="c4311-141">The following is the XPath 2.0 expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4311-142">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c4311-142">Remarks</span></span>

<span data-ttu-id="c4311-143">All die untergeordneten Elemente sind in der Reihenfolge aufgeführt, in denen sie anfallen.</span><span class="sxs-lookup"><span data-stu-id="c4311-143">All the child elements are listed in the sequence in which they occur.</span></span> 
  
<span data-ttu-id="c4311-144">Wenn das Element [IsPrivate](isprivate.md) auf **true**festgelegt ist, werden alle anderen Elemente im [CalendarEventDetails](calendareventdetails.md) -Element nicht in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c4311-144">If the [IsPrivate](isprivate.md) element is **true**, all the other elements in the [CalendarEventDetails](calendareventdetails.md) element are not returned in the response.</span></span> 
  
<span data-ttu-id="c4311-145">GetUserAvailability-Vorgang gibt keine Anrufer detaillierte Informationen zurück, wenn der Aufrufer Lesezugriff auf Kalender des Zielbenutzers verfügt.</span><span class="sxs-lookup"><span data-stu-id="c4311-145">The GetUserAvailability operation does not return detailed caller information unless the caller has read access on the target user's calendar.</span></span> <span data-ttu-id="c4311-146">Sie können mithilfe der Exchange-Verwaltungsshell Zugriffsberechtigungen festlegen.</span><span class="sxs-lookup"><span data-stu-id="c4311-146">You can set access permissions by using the Exchange Management Shell.</span></span>
  
<span data-ttu-id="c4311-147">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="c4311-147">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c4311-148">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c4311-148">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4311-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="c4311-149">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c4311-150">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c4311-150">Schema Name</span></span>  <br/> |<span data-ttu-id="c4311-151">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c4311-151">Types schema</span></span>  <br/> |
|<span data-ttu-id="c4311-152">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c4311-152">Validation File</span></span>  <br/> |<span data-ttu-id="c4311-153">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c4311-153">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c4311-154">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c4311-154">Can be Empty</span></span>  <br/> |<span data-ttu-id="c4311-155">False</span><span class="sxs-lookup"><span data-stu-id="c4311-155">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c4311-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4311-156">See also</span></span>



[<span data-ttu-id="c4311-157">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c4311-157">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="c4311-158">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="c4311-158">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="c4311-159">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="c4311-159">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

