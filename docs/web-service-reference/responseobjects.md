---
title: ResponseObjects
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseObjects
api_type:
- schema
ms.assetid: ad29e064-3f3d-4b7b-aa4c-9ec27326381d
description: Das ResponseObjects-Element enthält eine Auflistung aller Response-Objekte, die einem Element in der Exchange-Informationsspeicher zugeordnet sind.
ms.openlocfilehash: 675bfda4addb38535736efc0c790577ff4739108
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457438"
---
# <a name="responseobjects"></a><span data-ttu-id="e2c00-103">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="e2c00-103">ResponseObjects</span></span>

<span data-ttu-id="e2c00-104">Das **ResponseObjects** -Element enthält eine Auflistung aller Response-Objekte, die einem Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e2c00-104">The **ResponseObjects** element contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span> 
  
```XML
<ResponseObjects>
   <AcceptItem/>
   <TentativelyAcceptItem/>
   <DeclineItem/>
   <ReplyToItem/>
   <ForwardItem/>
   <ReplyAllToItem/>
   <CancelCalendarItem/>
   <RemoveItem/>
   <PostReplyItem/>
   <SuppressReadReceipt/>
   <AcceptSharingInvitation/>
</ResponseObjects>
```

 <span data-ttu-id="e2c00-105">**NonEmptyArrayOfResponseObjectsType**</span><span class="sxs-lookup"><span data-stu-id="e2c00-105">**NonEmptyArrayOfResponseObjectsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e2c00-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e2c00-106">Attributes and elements</span></span>

<span data-ttu-id="e2c00-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e2c00-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e2c00-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e2c00-108">Attributes</span></span>

<span data-ttu-id="e2c00-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e2c00-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e2c00-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e2c00-110">Child elements</span></span>

|<span data-ttu-id="e2c00-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e2c00-111">**Element**</span></span>|<span data-ttu-id="e2c00-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e2c00-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e2c00-113">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="e2c00-113">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="e2c00-114">Stellt eine Accept-Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="e2c00-114">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="e2c00-115">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="e2c00-115">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="e2c00-116">Stellt eine mit Vorbehalt Antworten auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="e2c00-116">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="e2c00-117">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="e2c00-117">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="e2c00-118">Stellt eine ablehnen Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="e2c00-118">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="e2c00-119">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="e2c00-119">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="e2c00-120">Enthält eine Antwort an den Ersteller eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="e2c00-120">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e2c00-121">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="e2c00-121">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="e2c00-122">Enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="e2c00-122">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="e2c00-123">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="e2c00-123">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="e2c00-124">Enthält eine Antwort an alle identifizierten Empfänger eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="e2c00-124">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e2c00-125">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="e2c00-125">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="e2c00-126">Stellt das Antwortobjekt dar, das zum Abbrechen einer Besprechung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e2c00-126">Represents the response object used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="e2c00-127">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="e2c00-127">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="e2c00-128">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="e2c00-128">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e2c00-129">PostReplyItem</span><span class="sxs-lookup"><span data-stu-id="e2c00-129">PostReplyItem</span></span>](postreplyitem.md) <br/> |<span data-ttu-id="e2c00-130">Enthält eine Antwort auf ein Post-Element.</span><span class="sxs-lookup"><span data-stu-id="e2c00-130">Contains a reply to a post item.</span></span> <span data-ttu-id="e2c00-131">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e2c00-131">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="e2c00-132">SuppressReadReceipt</span><span class="sxs-lookup"><span data-stu-id="e2c00-132">SuppressReadReceipt</span></span>](suppressreadreceipt.md) <br/> |<span data-ttu-id="e2c00-133">Wird verwendet, um Lese Bestätigungsanforderungen zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="e2c00-133">Used to suppress read receipt requests.</span></span>  <br/> |
|[<span data-ttu-id="e2c00-134">AcceptSharingInvitation</span><span class="sxs-lookup"><span data-stu-id="e2c00-134">AcceptSharingInvitation</span></span>](acceptsharinginvitation.md) <br/> |<span data-ttu-id="e2c00-135">Wird verwendet, um eine Einladung zu akzeptieren, die den Zugriff auf die Kalender-oder Kontaktdaten eines anderen Benutzers zulässt.</span><span class="sxs-lookup"><span data-stu-id="e2c00-135">Used to accept an invitation that allows access to another user's calendar or contacts data.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e2c00-136">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e2c00-136">Parent elements</span></span>

|<span data-ttu-id="e2c00-137">**Element**</span><span class="sxs-lookup"><span data-stu-id="e2c00-137">**Element**</span></span>|<span data-ttu-id="e2c00-138">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e2c00-138">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e2c00-139">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="e2c00-139">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="e2c00-140">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="e2c00-140">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="e2c00-141">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="e2c00-141">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="e2c00-142">Stellt ein Exchange-Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="e2c00-142">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="e2c00-143">DistributionList</span><span class="sxs-lookup"><span data-stu-id="e2c00-143">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="e2c00-144">Stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="e2c00-144">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="e2c00-145">Element</span><span class="sxs-lookup"><span data-stu-id="e2c00-145">Item</span></span>](item.md) <br/> |<span data-ttu-id="e2c00-146">Stellt ein Element im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="e2c00-146">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e2c00-147">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="e2c00-147">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="e2c00-148">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="e2c00-148">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e2c00-149">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="e2c00-149">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="e2c00-150">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="e2c00-150">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e2c00-151">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="e2c00-151">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="e2c00-152">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="e2c00-152">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e2c00-153">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="e2c00-153">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="e2c00-154">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="e2c00-154">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e2c00-155">Message</span><span class="sxs-lookup"><span data-stu-id="e2c00-155">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="e2c00-156">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="e2c00-156">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="e2c00-157">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="e2c00-157">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="e2c00-158">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="e2c00-158">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e2c00-159">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="e2c00-159">Task</span></span>](task.md) <br/> |<span data-ttu-id="e2c00-160">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="e2c00-160">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2c00-161">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2c00-161">Remarks</span></span>

<span data-ttu-id="e2c00-162">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="e2c00-162">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e2c00-163">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e2c00-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e2c00-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="e2c00-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e2c00-165">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e2c00-165">Schema Name</span></span>  <br/> |<span data-ttu-id="e2c00-166">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e2c00-166">Types schema</span></span>  <br/> |
|<span data-ttu-id="e2c00-167">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e2c00-167">Validation File</span></span>  <br/> |<span data-ttu-id="e2c00-168">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e2c00-168">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e2c00-169">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e2c00-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="e2c00-170">False</span><span class="sxs-lookup"><span data-stu-id="e2c00-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e2c00-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2c00-171">See also</span></span>



- [<span data-ttu-id="e2c00-172">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e2c00-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

