---
title: Von
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- From
api_type:
- schema
ms.assetid: 5a52d644-3677-4049-874c-12bd5c3080dc
description: Das From-Element darstellt, die Adresse an, von der die Nachricht gesendet wurde.
ms.openlocfilehash: 39c8c8ef84ff445e8f44ebb9f2285ccfc42353a7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758554"
---
# <a name="from"></a><span data-ttu-id="8f7f4-103">Von</span><span class="sxs-lookup"><span data-stu-id="8f7f4-103">From</span></span>

<span data-ttu-id="8f7f4-104">Das Element **aus** stellt die Adresse an, von der die Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-104">The **From** element represents the address from which the message was sent.</span></span> 
  
```xml
<From>
   <Mailbox/>
</From>
```

 <span data-ttu-id="8f7f4-105">**SingleRecipientType**</span><span class="sxs-lookup"><span data-stu-id="8f7f4-105">**SingleRecipientType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8f7f4-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8f7f4-106">Attributes and elements</span></span>

<span data-ttu-id="8f7f4-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8f7f4-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8f7f4-108">Attributes</span></span>

<span data-ttu-id="8f7f4-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8f7f4-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8f7f4-110">Child elements</span></span>

|<span data-ttu-id="8f7f4-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="8f7f4-111">**Element**</span></span>|<span data-ttu-id="8f7f4-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8f7f4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8f7f4-113">Postfach</span><span class="sxs-lookup"><span data-stu-id="8f7f4-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="8f7f4-114">Ein e-Mail-aktivierten Active Directory Directory Service-Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8f7f4-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8f7f4-115">Parent elements</span></span>

|<span data-ttu-id="8f7f4-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="8f7f4-116">**Element**</span></span>|<span data-ttu-id="8f7f4-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8f7f4-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8f7f4-118">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="8f7f4-118">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="8f7f4-119">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-119">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8f7f4-120">Message</span><span class="sxs-lookup"><span data-stu-id="8f7f4-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="8f7f4-121">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-121">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="8f7f4-122">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="8f7f4-122">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="8f7f4-123">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-123">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8f7f4-124">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="8f7f4-124">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="8f7f4-125">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-125">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8f7f4-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="8f7f4-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="8f7f4-127">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8f7f4-128">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="8f7f4-128">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="8f7f4-129">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-129">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8f7f4-130">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="8f7f4-130">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="8f7f4-131">Stellt eine Accept-Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-131">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="8f7f4-132">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="8f7f4-132">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="8f7f4-133">Stellt eine mit Vorbehalt Antworten auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-133">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="8f7f4-134">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="8f7f4-134">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="8f7f4-135">Stellt eine ablehnen Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-135">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="8f7f4-136">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="8f7f4-136">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="8f7f4-137">Enthält eine Antwort an den Ersteller eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-137">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8f7f4-138">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="8f7f4-138">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="8f7f4-139">Enthält eine Antwort an alle identifizierten Empfänger eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-139">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8f7f4-140">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="8f7f4-140">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="8f7f4-141">Enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-141">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="8f7f4-142">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="8f7f4-142">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="8f7f4-143">Stellt das Antwortobjekt, das Sie eine Besprechung absagen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-143">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="8f7f4-144">PostItem-Objekt</span><span class="sxs-lookup"><span data-stu-id="8f7f4-144">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="8f7f4-145">Stellt ein Post-Element im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-145">Represents a post item in the Exchange store.</span></span> <span data-ttu-id="8f7f4-146">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-146">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8f7f4-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f7f4-147">Remarks</span></span>

<span data-ttu-id="8f7f4-148">Dieses Element wird für "Senden im Auftrag von" e-Mail-Nachrichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-148">This element is used for "send on behalf of" e-mails.</span></span>
  
<span data-ttu-id="8f7f4-149">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="8f7f4-149">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8f7f4-150">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8f7f4-150">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8f7f4-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="8f7f4-151">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8f7f4-152">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8f7f4-152">Schema Name</span></span>  <br/> |<span data-ttu-id="8f7f4-153">Schematypen</span><span class="sxs-lookup"><span data-stu-id="8f7f4-153">Types schema</span></span>  <br/> |
|<span data-ttu-id="8f7f4-154">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8f7f4-154">Validation File</span></span>  <br/> |<span data-ttu-id="8f7f4-155">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8f7f4-155">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8f7f4-156">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8f7f4-156">Can be Empty</span></span>  <br/> |<span data-ttu-id="8f7f4-157">False</span><span class="sxs-lookup"><span data-stu-id="8f7f4-157">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8f7f4-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f7f4-158">See also</span></span>



- [<span data-ttu-id="8f7f4-159">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8f7f4-159">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

