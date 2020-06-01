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
description: Das CalendarEventDetails-Element stellt zusätzliche Informationen zu einem Calendar-Ereignis bereit.
ms.openlocfilehash: 3e1dbba00bce4a1fdc53f3330527764c516890ab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459069"
---
# <a name="calendareventdetails"></a><span data-ttu-id="f871f-103">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="f871f-103">CalendarEventDetails</span></span>

<span data-ttu-id="f871f-104">Das **CalendarEventDetails** -Element stellt zusätzliche Informationen zu einem Calendar-Ereignis bereit.</span><span class="sxs-lookup"><span data-stu-id="f871f-104">The **CalendarEventDetails** element provides additional information about a calendar event.</span></span> 
  
[<span data-ttu-id="f871f-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="f871f-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="f871f-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="f871f-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="f871f-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="f871f-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="f871f-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="f871f-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="f871f-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="f871f-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="f871f-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="f871f-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="f871f-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="f871f-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
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

 <span data-ttu-id="f871f-112">**CalendarEventDetails**</span><span class="sxs-lookup"><span data-stu-id="f871f-112">**CalendarEventDetails**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f871f-113">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f871f-113">Attributes and elements</span></span>

<span data-ttu-id="f871f-114">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f871f-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f871f-115">Attribute</span><span class="sxs-lookup"><span data-stu-id="f871f-115">Attributes</span></span>

<span data-ttu-id="f871f-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="f871f-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f871f-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f871f-117">Child elements</span></span>

|<span data-ttu-id="f871f-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="f871f-118">**Element**</span></span>|<span data-ttu-id="f871f-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f871f-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f871f-120">ID</span><span class="sxs-lookup"><span data-stu-id="f871f-120">ID</span></span>](id.md) <br/> |<span data-ttu-id="f871f-121">Stellt die Eintrags-ID des Kalenderelements dar.</span><span class="sxs-lookup"><span data-stu-id="f871f-121">Represents the entry ID of the calendar item.</span></span>  <br/> |
|[<span data-ttu-id="f871f-122">Betreff (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="f871f-122">Subject (CalendarEventDetails)</span></span>](subject-calendareventdetails.md) <br/> |<span data-ttu-id="f871f-123">Stellt den Betreff des Kalenderelements dar.</span><span class="sxs-lookup"><span data-stu-id="f871f-123">Represents the subject of the calendar item.</span></span>  <br/> |
|[<span data-ttu-id="f871f-124">Speicherort (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="f871f-124">Location (CalendarEventDetails)</span></span>](location-calendareventdetails.md) <br/> |<span data-ttu-id="f871f-125">Stellt das Feld Location des Kalenderelements dar.</span><span class="sxs-lookup"><span data-stu-id="f871f-125">Represents the location field of the calendar item.</span></span>  <br/> |
|[<span data-ttu-id="f871f-126">Ismeeting (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="f871f-126">IsMeeting (CalendarEventDetails)</span></span>](ismeeting-calendareventdetails.md) <br/> |<span data-ttu-id="f871f-127">Gibt an, ob es sich bei dem Kalenderereignis um eine Besprechung oder einen Termin handelt.</span><span class="sxs-lookup"><span data-stu-id="f871f-127">Indicates whether the calendar event is a meeting or an appointment.</span></span>  <br/> |
|[<span data-ttu-id="f871f-128">Iswiederkehr (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="f871f-128">IsRecurring (CalendarEventDetails)</span></span>](isrecurring-calendareventdetails.md) <br/> |<span data-ttu-id="f871f-129">Gibt an, ob das Kalenderereignis eine Instanz eines wiederkehrenden Kalenderelements oder eines einzelnen Kalenderelements ist.</span><span class="sxs-lookup"><span data-stu-id="f871f-129">Indicates whether the calendar event is an instance of a recurring calendar item or a single calendar item.</span></span>  <br/> |
|[<span data-ttu-id="f871f-130">Isexception</span><span class="sxs-lookup"><span data-stu-id="f871f-130">IsException</span></span>](isexception.md) <br/> |<span data-ttu-id="f871f-131">Gibt an, ob eine Instanz eines wiederkehrenden Kalenderelements aus dem Master geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f871f-131">Indicates whether an instance of a recurring calendar item is changed from the master.</span></span>  <br/> |
|[<span data-ttu-id="f871f-132">Reminder</span><span class="sxs-lookup"><span data-stu-id="f871f-132">IsReminderSet</span></span>](isreminderset.md) <br/> |<span data-ttu-id="f871f-133">Gibt an, ob für das Calendar-Ereignis eine Erinnerung festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="f871f-133">Indicates whether a reminder has been set for the calendar event.</span></span>  <br/> |
|[<span data-ttu-id="f871f-134">IsPrivate</span><span class="sxs-lookup"><span data-stu-id="f871f-134">IsPrivate</span></span>](isprivate.md) <br/> |<span data-ttu-id="f871f-135">Gibt an, ob das Kalenderelement privat ist.</span><span class="sxs-lookup"><span data-stu-id="f871f-135">Indicates whether the calendar item is private.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f871f-136">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f871f-136">Parent elements</span></span>

|<span data-ttu-id="f871f-137">**Element**</span><span class="sxs-lookup"><span data-stu-id="f871f-137">**Element**</span></span>|<span data-ttu-id="f871f-138">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f871f-138">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f871f-139">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="f871f-139">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="f871f-140">Stellt ein eindeutiges Kalenderelement vorkommen dar.</span><span class="sxs-lookup"><span data-stu-id="f871f-140">Represents a unique calendar item occurrence.</span></span>  <br/> <span data-ttu-id="f871f-141">Im folgenden finden Sie den XPath 2,0-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="f871f-141">The following is the XPath 2.0 expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f871f-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f871f-142">Remarks</span></span>

<span data-ttu-id="f871f-143">Alle untergeordneten Elemente werden in der Reihenfolge aufgeführt, in der Sie auftreten.</span><span class="sxs-lookup"><span data-stu-id="f871f-143">All the child elements are listed in the sequence in which they occur.</span></span> 
  
<span data-ttu-id="f871f-144">Wenn das [IsPrivate](isprivate.md) -Element auf **true**festgelegt ist, werden alle anderen Elemente im [CalendarEventDetails](calendareventdetails.md) -Element nicht in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f871f-144">If the [IsPrivate](isprivate.md) element is **true**, all the other elements in the [CalendarEventDetails](calendareventdetails.md) element are not returned in the response.</span></span> 
  
<span data-ttu-id="f871f-145">Der GetUserAvailability-Vorgang gibt keine detaillierten Anrufer-Informationen zurück, es sei denn, der Aufrufer verfügt über Lesezugriff auf den Kalender des Zielbenutzers.</span><span class="sxs-lookup"><span data-stu-id="f871f-145">The GetUserAvailability operation does not return detailed caller information unless the caller has read access on the target user's calendar.</span></span> <span data-ttu-id="f871f-146">Sie können Zugriffsberechtigungen mithilfe der Exchange-Verwaltungsshell festlegen.</span><span class="sxs-lookup"><span data-stu-id="f871f-146">You can set access permissions by using the Exchange Management Shell.</span></span>
  
<span data-ttu-id="f871f-147">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="f871f-147">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f871f-148">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f871f-148">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f871f-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="f871f-149">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f871f-150">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f871f-150">Schema Name</span></span>  <br/> |<span data-ttu-id="f871f-151">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f871f-151">Types schema</span></span>  <br/> |
|<span data-ttu-id="f871f-152">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f871f-152">Validation File</span></span>  <br/> |<span data-ttu-id="f871f-153">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f871f-153">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f871f-154">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f871f-154">Can be Empty</span></span>  <br/> |<span data-ttu-id="f871f-155">False</span><span class="sxs-lookup"><span data-stu-id="f871f-155">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f871f-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f871f-156">See also</span></span>



[<span data-ttu-id="f871f-157">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f871f-157">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="f871f-158">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="f871f-158">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="f871f-159">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="f871f-159">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

