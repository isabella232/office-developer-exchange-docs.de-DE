---
title: InternetMessageHeaders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InternetMessageHeaders
api_type:
- schema
ms.assetid: 4dcf8671-96df-4a2d-9836-7e8e3a67e0db
description: Das InternetMessageHeaders-Element enthält eine Auflistung einiger Internet-Nachrichtenkopfzeilen, die in einem Element in einem Postfach enthalten sind. Wenn Sie die gesamte Auflistung der Internetkopfzeilen Nachricht erhalten möchten, verwenden Sie die PR_TRANSPORT_MESSAGE_HEADERS-Eigenschaft. Weitere Informationen zu EWS und Internet Nachrichtenkopfzeilen, SeeGetting Internet Message Headersin EWS, MIME und fehlenden Internetkopfzeilen Nachricht.
ms.openlocfilehash: 2da529a8a3532cebb2791b285b7673c962a2a656
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829954"
---
# <a name="internetmessageheaders"></a><span data-ttu-id="37d01-105">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="37d01-105">InternetMessageHeaders</span></span>

<span data-ttu-id="37d01-106">Das **InternetMessageHeaders** -Element enthält eine Auflistung einiger Internet-Nachrichtenkopfzeilen, die in einem Element in einem Postfach enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="37d01-106">The **InternetMessageHeaders** element contains a collection of some of the Internet message headers that are contained in an item in a mailbox.</span></span> <span data-ttu-id="37d01-107">Wenn Sie die gesamte Auflistung der Internetkopfzeilen Nachricht erhalten möchten, verwenden Sie die **PR_TRANSPORT_MESSAGE_HEADERS** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="37d01-107">To get the entire collection of Internet message headers, use the **PR_TRANSPORT_MESSAGE_HEADERS** property.</span></span> <span data-ttu-id="37d01-108">Weitere Informationen zu EWS und Internet Nachrichtenkopfzeilen finden Sie unter "Erste Internet-Kopfzeilen" im [EWS, MIME, und die fehlenden Internet Nachrichtenkopfzeilen](http://msdn.microsoft.com/en-us/library/exchange/hh545614%28v=exchg.140%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="37d01-108">For more information about EWS and Internet message headers, see "Getting Internet message headers" in [EWS, MIME, and the missing Internet message headers](http://msdn.microsoft.com/en-us/library/exchange/hh545614%28v=exchg.140%29.aspx).</span></span>
  
```XML
<InternetMessageHeaders>
   <InternetMessageHeader/>
</InternetMessageHeaders>
```

 <span data-ttu-id="37d01-109">**NonEmptyArrayOfInternetHeadersType**</span><span class="sxs-lookup"><span data-stu-id="37d01-109">**NonEmptyArrayOfInternetHeadersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="37d01-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="37d01-110">Attributes and elements</span></span>

<span data-ttu-id="37d01-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="37d01-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="37d01-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="37d01-112">Attributes</span></span>

<span data-ttu-id="37d01-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="37d01-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="37d01-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="37d01-114">Child elements</span></span>

|<span data-ttu-id="37d01-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="37d01-115">**Element**</span></span>|<span data-ttu-id="37d01-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="37d01-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="37d01-117">InternetMessageHeader</span><span class="sxs-lookup"><span data-stu-id="37d01-117">InternetMessageHeader</span></span>](internetmessageheader.md) <br/> |<span data-ttu-id="37d01-118">Internet-Nachrichtenkopfzeile für einen angegebenen Header innerhalb der Kopfzeilen-Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="37d01-118">Represents the Internet message header for a given header within the headers collection.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="37d01-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="37d01-119">Parent elements</span></span>

|<span data-ttu-id="37d01-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="37d01-120">**Element**</span></span>|<span data-ttu-id="37d01-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="37d01-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="37d01-122">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="37d01-122">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="37d01-123">Stellt eine Accept-Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="37d01-123">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="37d01-124">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="37d01-124">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="37d01-125">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="37d01-125">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="37d01-126">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="37d01-126">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="37d01-127">Stellt ein Exchange-Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="37d01-127">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="37d01-128">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="37d01-128">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="37d01-129">Stellt eine ablehnen Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="37d01-129">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="37d01-130">DistributionList</span><span class="sxs-lookup"><span data-stu-id="37d01-130">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="37d01-131">Stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="37d01-131">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="37d01-132">Element</span><span class="sxs-lookup"><span data-stu-id="37d01-132">Item</span></span>](item.md) <br/> |<span data-ttu-id="37d01-133">Stellt ein Element im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="37d01-133">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="37d01-134">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="37d01-134">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="37d01-135">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="37d01-135">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="37d01-136">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="37d01-136">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="37d01-137">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="37d01-137">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="37d01-138">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="37d01-138">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="37d01-139">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="37d01-139">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="37d01-140">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="37d01-140">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="37d01-141">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="37d01-141">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="37d01-142">Message</span><span class="sxs-lookup"><span data-stu-id="37d01-142">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="37d01-143">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="37d01-143">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="37d01-144">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="37d01-144">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="37d01-145">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="37d01-145">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="37d01-146">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="37d01-146">Task</span></span>](task.md) <br/> |<span data-ttu-id="37d01-147">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="37d01-147">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="37d01-148">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="37d01-148">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="37d01-149">Stellt eine Vorbehalt Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="37d01-149">Represents a tentatively accepted reply to a meeting request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37d01-150">Hinweise</span><span class="sxs-lookup"><span data-stu-id="37d01-150">Remarks</span></span>

<span data-ttu-id="37d01-151">Es folgt die EWS Managed API erweiterten Eigenschaftendefinition für die Eigenschaft **PR_TRANSPORT_MESSAGE_HEADERS** .</span><span class="sxs-lookup"><span data-stu-id="37d01-151">The following is the EWS Managed API extended property definition for the **PR_TRANSPORT_MESSAGE_HEADERS** property.</span></span> 
  
```cs
ExtendedPropertyDefinition transportMsgHdr = new ExtendedPropertyDefinition(0x007D, MapiPropertyType.String);
```

<span data-ttu-id="37d01-152">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="37d01-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="37d01-153">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="37d01-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="37d01-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="37d01-154">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="37d01-155">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="37d01-155">Schema Name</span></span>  <br/> |<span data-ttu-id="37d01-156">Schematypen</span><span class="sxs-lookup"><span data-stu-id="37d01-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="37d01-157">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="37d01-157">Validation File</span></span>  <br/> |<span data-ttu-id="37d01-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="37d01-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="37d01-159">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="37d01-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="37d01-160">False</span><span class="sxs-lookup"><span data-stu-id="37d01-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="37d01-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37d01-161">See also</span></span>



- [<span data-ttu-id="37d01-162">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="37d01-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="37d01-163">EWS, MIME und die fehlenden Nachrichtenkopfzeilen</span><span class="sxs-lookup"><span data-stu-id="37d01-163">EWS, MIME, and the missing Internet message headers</span></span>](http://msdn.microsoft.com/en-us/library/exchange/hh545614%28v=exchg.140%29.aspx)

