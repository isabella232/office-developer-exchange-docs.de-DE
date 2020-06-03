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
description: Das InternetMessageHeaders-Element enthält eine Auflistung einiger der Internet Nachrichtenkopfzeilen, die in einem Element in einem Postfach enthalten sind. Verwenden Sie die PR_TRANSPORT_MESSAGE_HEADERS-Eigenschaft, um die gesamte Auflistung von Internet Nachrichtenkopfzeilen abzurufen. Weitere Informationen zu EWS und Internet Nachrichtenkopfzeilen, unterkauf-Internet Nachrichtenkopfzeilen in EWS, MIME und die fehlenden Internet Nachrichtenkopfzeilen.
ms.openlocfilehash: 4719050c02590e021b29173c234466de3fdc58a4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467326"
---
# <a name="internetmessageheaders"></a><span data-ttu-id="785f2-105">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="785f2-105">InternetMessageHeaders</span></span>

<span data-ttu-id="785f2-106">Das **InternetMessageHeaders** -Element enthält eine Auflistung einiger der Internet Nachrichtenkopfzeilen, die in einem Element in einem Postfach enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="785f2-106">The **InternetMessageHeaders** element contains a collection of some of the Internet message headers that are contained in an item in a mailbox.</span></span> <span data-ttu-id="785f2-107">Verwenden Sie die **PR_TRANSPORT_MESSAGE_HEADERS** -Eigenschaft, um die gesamte Auflistung von Internet Nachrichtenkopfzeilen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="785f2-107">To get the entire collection of Internet message headers, use the **PR_TRANSPORT_MESSAGE_HEADERS** property.</span></span> <span data-ttu-id="785f2-108">Weitere Informationen zu EWS und Internet Nachrichtenkopfzeilen finden Sie unter "Getting Internet Message Headers" in [EWS, MIME und den fehlenden Internet Nachrichten](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx)Kopfzeilen.</span><span class="sxs-lookup"><span data-stu-id="785f2-108">For more information about EWS and Internet message headers, see "Getting Internet message headers" in [EWS, MIME, and the missing Internet message headers](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx).</span></span>
  
```XML
<InternetMessageHeaders>
   <InternetMessageHeader/>
</InternetMessageHeaders>
```

 <span data-ttu-id="785f2-109">**NonEmptyArrayOfInternetHeadersType**</span><span class="sxs-lookup"><span data-stu-id="785f2-109">**NonEmptyArrayOfInternetHeadersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="785f2-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="785f2-110">Attributes and elements</span></span>

<span data-ttu-id="785f2-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="785f2-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="785f2-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="785f2-112">Attributes</span></span>

<span data-ttu-id="785f2-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="785f2-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="785f2-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="785f2-114">Child elements</span></span>

|<span data-ttu-id="785f2-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="785f2-115">**Element**</span></span>|<span data-ttu-id="785f2-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="785f2-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="785f2-117">InternetMessageHeader</span><span class="sxs-lookup"><span data-stu-id="785f2-117">InternetMessageHeader</span></span>](internetmessageheader.md) <br/> |<span data-ttu-id="785f2-118">Stellt den Internet Nachrichtenkopf für eine angegebene Kopfzeile in der Headers-Auflistung dar.</span><span class="sxs-lookup"><span data-stu-id="785f2-118">Represents the Internet message header for a given header within the headers collection.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="785f2-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="785f2-119">Parent elements</span></span>

|<span data-ttu-id="785f2-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="785f2-120">**Element**</span></span>|<span data-ttu-id="785f2-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="785f2-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="785f2-122">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="785f2-122">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="785f2-123">Stellt eine Accept-Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="785f2-123">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="785f2-124">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="785f2-124">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="785f2-125">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="785f2-125">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="785f2-126">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="785f2-126">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="785f2-127">Stellt ein Exchange-Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="785f2-127">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="785f2-128">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="785f2-128">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="785f2-129">Stellt eine ablehnen Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="785f2-129">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="785f2-130">DistributionList</span><span class="sxs-lookup"><span data-stu-id="785f2-130">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="785f2-131">Stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="785f2-131">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="785f2-132">Element</span><span class="sxs-lookup"><span data-stu-id="785f2-132">Item</span></span>](item.md) <br/> |<span data-ttu-id="785f2-133">Stellt ein Element im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="785f2-133">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="785f2-134">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="785f2-134">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="785f2-135">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="785f2-135">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="785f2-136">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="785f2-136">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="785f2-137">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="785f2-137">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="785f2-138">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="785f2-138">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="785f2-139">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="785f2-139">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="785f2-140">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="785f2-140">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="785f2-141">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="785f2-141">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="785f2-142">Message</span><span class="sxs-lookup"><span data-stu-id="785f2-142">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="785f2-143">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="785f2-143">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="785f2-144">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="785f2-144">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="785f2-145">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="785f2-145">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="785f2-146">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="785f2-146">Task</span></span>](task.md) <br/> |<span data-ttu-id="785f2-147">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="785f2-147">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="785f2-148">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="785f2-148">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="785f2-149">Stellt eine Vorbehalt Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="785f2-149">Represents a tentatively accepted reply to a meeting request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="785f2-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="785f2-150">Remarks</span></span>

<span data-ttu-id="785f2-151">Im folgenden finden Sie die verwaltete EWS-API erweiterte Eigenschaftsdefinition für die **PR_TRANSPORT_MESSAGE_HEADERS** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="785f2-151">The following is the EWS Managed API extended property definition for the **PR_TRANSPORT_MESSAGE_HEADERS** property.</span></span> 
  
```cs
ExtendedPropertyDefinition transportMsgHdr = new ExtendedPropertyDefinition(0x007D, MapiPropertyType.String);
```

<span data-ttu-id="785f2-152">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="785f2-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="785f2-153">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="785f2-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="785f2-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="785f2-154">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="785f2-155">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="785f2-155">Schema Name</span></span>  <br/> |<span data-ttu-id="785f2-156">Schematypen</span><span class="sxs-lookup"><span data-stu-id="785f2-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="785f2-157">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="785f2-157">Validation File</span></span>  <br/> |<span data-ttu-id="785f2-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="785f2-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="785f2-159">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="785f2-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="785f2-160">False</span><span class="sxs-lookup"><span data-stu-id="785f2-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="785f2-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="785f2-161">See also</span></span>



- [<span data-ttu-id="785f2-162">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="785f2-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="785f2-163">EWS, MIME und die fehlenden Nachrichtenkopfzeilen</span><span class="sxs-lookup"><span data-stu-id="785f2-163">EWS, MIME, and the missing Internet message headers</span></span>](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx)

