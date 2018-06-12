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
description: Das ResponseObjects-Element enthält eine Auflistung aller Antwort-Objekte, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.
ms.openlocfilehash: b1d95063439f5089665d2aad97d747665caef0ca
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831197"
---
# <a name="responseobjects"></a><span data-ttu-id="191ba-103">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="191ba-103">ResponseObjects</span></span>

<span data-ttu-id="191ba-104">Das **ResponseObjects** -Element enthält eine Auflistung aller Antwort-Objekte, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="191ba-104">The **ResponseObjects** element contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span> 
  
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

 <span data-ttu-id="191ba-105">**NonEmptyArrayOfResponseObjectsType**</span><span class="sxs-lookup"><span data-stu-id="191ba-105">**NonEmptyArrayOfResponseObjectsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="191ba-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="191ba-106">Attributes and elements</span></span>

<span data-ttu-id="191ba-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="191ba-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="191ba-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="191ba-108">Attributes</span></span>

<span data-ttu-id="191ba-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="191ba-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="191ba-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="191ba-110">Child elements</span></span>

|<span data-ttu-id="191ba-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="191ba-111">**Element**</span></span>|<span data-ttu-id="191ba-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="191ba-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="191ba-113">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="191ba-113">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="191ba-114">Stellt eine Accept-Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="191ba-114">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="191ba-115">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="191ba-115">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="191ba-116">Stellt eine mit Vorbehalt Antworten auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="191ba-116">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="191ba-117">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="191ba-117">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="191ba-118">Stellt eine ablehnen Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="191ba-118">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="191ba-119">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="191ba-119">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="191ba-120">Enthält eine Antwort an den Ersteller eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="191ba-120">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="191ba-121">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="191ba-121">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="191ba-122">Enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="191ba-122">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="191ba-123">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="191ba-123">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="191ba-124">Enthält eine Antwort an alle identifizierten Empfänger eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="191ba-124">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="191ba-125">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="191ba-125">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="191ba-126">Verwendet, um eine Besprechung absagen Response-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="191ba-126">Represents the response object used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="191ba-127">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="191ba-127">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="191ba-128">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="191ba-128">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="191ba-129">PostReplyItem</span><span class="sxs-lookup"><span data-stu-id="191ba-129">PostReplyItem</span></span>](postreplyitem.md) <br/> |<span data-ttu-id="191ba-130">Eine Antwort auf eine Post-Element enthält.</span><span class="sxs-lookup"><span data-stu-id="191ba-130">Contains a reply to a post item.</span></span> <span data-ttu-id="191ba-131">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="191ba-131">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="191ba-132">SuppressReadReceipt</span><span class="sxs-lookup"><span data-stu-id="191ba-132">SuppressReadReceipt</span></span>](suppressreadreceipt.md) <br/> |<span data-ttu-id="191ba-133">Verwendet, um lesebestätigung Anfragen zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="191ba-133">Used to suppress read receipt requests.</span></span>  <br/> |
|[<span data-ttu-id="191ba-134">AcceptSharingInvitation</span><span class="sxs-lookup"><span data-stu-id="191ba-134">AcceptSharingInvitation</span></span>](acceptsharinginvitation.md) <br/> |<span data-ttu-id="191ba-135">Verwendet, um eine Einladung annehmen, die Zugriff auf einen anderen Benutzer Kalender oder Kontaktdaten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="191ba-135">Used to accept an invitation that allows access to another user's calendar or contacts data.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="191ba-136">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="191ba-136">Parent elements</span></span>

|<span data-ttu-id="191ba-137">**Element**</span><span class="sxs-lookup"><span data-stu-id="191ba-137">**Element**</span></span>|<span data-ttu-id="191ba-138">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="191ba-138">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="191ba-139">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="191ba-139">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="191ba-140">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="191ba-140">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="191ba-141">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="191ba-141">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="191ba-142">Stellt ein Exchange-Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="191ba-142">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="191ba-143">DistributionList</span><span class="sxs-lookup"><span data-stu-id="191ba-143">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="191ba-144">Stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="191ba-144">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="191ba-145">Element</span><span class="sxs-lookup"><span data-stu-id="191ba-145">Item</span></span>](item.md) <br/> |<span data-ttu-id="191ba-146">Stellt ein Element im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="191ba-146">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="191ba-147">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="191ba-147">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="191ba-148">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="191ba-148">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="191ba-149">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="191ba-149">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="191ba-150">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="191ba-150">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="191ba-151">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="191ba-151">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="191ba-152">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="191ba-152">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="191ba-153">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="191ba-153">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="191ba-154">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="191ba-154">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="191ba-155">Message</span><span class="sxs-lookup"><span data-stu-id="191ba-155">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="191ba-156">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="191ba-156">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="191ba-157">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="191ba-157">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="191ba-158">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="191ba-158">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="191ba-159">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="191ba-159">Task</span></span>](task.md) <br/> |<span data-ttu-id="191ba-160">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="191ba-160">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="191ba-161">Hinweise</span><span class="sxs-lookup"><span data-stu-id="191ba-161">Remarks</span></span>

<span data-ttu-id="191ba-162">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="191ba-162">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="191ba-163">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="191ba-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="191ba-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="191ba-164">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="191ba-165">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="191ba-165">Schema Name</span></span>  <br/> |<span data-ttu-id="191ba-166">Schematypen</span><span class="sxs-lookup"><span data-stu-id="191ba-166">Types schema</span></span>  <br/> |
|<span data-ttu-id="191ba-167">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="191ba-167">Validation File</span></span>  <br/> |<span data-ttu-id="191ba-168">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="191ba-168">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="191ba-169">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="191ba-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="191ba-170">False</span><span class="sxs-lookup"><span data-stu-id="191ba-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="191ba-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="191ba-171">See also</span></span>



- [<span data-ttu-id="191ba-172">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="191ba-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

