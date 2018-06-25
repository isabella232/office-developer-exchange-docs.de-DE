---
title: BccRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BccRecipients
api_type:
- schema
ms.assetid: c4e05168-d36b-4740-a526-4b7da53553c1
description: Das Element BccRecipients stellt eine Auflistung der Empfänger, die eine Blindkopie (Bcc) einer e-Mail-Nachricht empfangen.
ms.openlocfilehash: 858fe74c32cb7d1ed624888c06bba4ffe09d489e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757437"
---
# <a name="bccrecipients"></a><span data-ttu-id="d1261-103">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="d1261-103">BccRecipients</span></span>

<span data-ttu-id="d1261-104">Das Element **BccRecipients** stellt eine Auflistung der Empfänger, die eine Blindkopie (Bcc) einer e-Mail-Nachricht empfangen.</span><span class="sxs-lookup"><span data-stu-id="d1261-104">The **BccRecipients** element represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail message.</span></span> 
  
```xml
<BccRecipients>
   <Mailbox/>
</BccRecipients>
```

 <span data-ttu-id="d1261-105">**ArrayOfRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="d1261-105">**ArrayOfRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d1261-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d1261-106">Attributes and elements</span></span>

<span data-ttu-id="d1261-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d1261-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d1261-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d1261-108">Attributes</span></span>

<span data-ttu-id="d1261-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d1261-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d1261-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d1261-110">Child elements</span></span>

|<span data-ttu-id="d1261-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d1261-111">**Element**</span></span>|<span data-ttu-id="d1261-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d1261-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d1261-113">Postfach</span><span class="sxs-lookup"><span data-stu-id="d1261-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="d1261-114">Ein e-Mail-aktivierten Active Directory Directory Service-Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d1261-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d1261-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d1261-115">Parent elements</span></span>

|<span data-ttu-id="d1261-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="d1261-116">**Element**</span></span>|<span data-ttu-id="d1261-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d1261-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d1261-118">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="d1261-118">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="d1261-119">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="d1261-119">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d1261-120">Message</span><span class="sxs-lookup"><span data-stu-id="d1261-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d1261-121">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="d1261-121">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="d1261-122">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="d1261-122">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="d1261-123">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="d1261-123">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d1261-124">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="d1261-124">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="d1261-125">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="d1261-125">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d1261-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="d1261-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="d1261-127">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="d1261-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d1261-128">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="d1261-128">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="d1261-129">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="d1261-129">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d1261-130">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="d1261-130">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="d1261-131">Stellt eine Accept-Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="d1261-131">Represents an accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="d1261-132">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="d1261-132">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="d1261-133">Stellt eine Vorbehalt Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="d1261-133">Represents a tentatively accepted reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="d1261-134">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="d1261-134">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="d1261-135">Stellt eine ablehnen Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="d1261-135">Represents a decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="d1261-136">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="d1261-136">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="d1261-137">Enthält eine Antwort an den Ersteller eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="d1261-137">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d1261-138">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="d1261-138">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="d1261-139">Enthält eine Antwort an alle identifizierten Empfänger eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="d1261-139">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d1261-140">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="d1261-140">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="d1261-141">Enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="d1261-141">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="d1261-142">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="d1261-142">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="d1261-143">Stellt das Antwortobjekt, das Sie eine Besprechung absagen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d1261-143">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1261-144">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d1261-144">Remarks</span></span>

<span data-ttu-id="d1261-p101">Sie können nicht **BccRecipients** mithilfe einer Anforderung FindItem abrufen. Verwenden Sie eine Anforderung GetItem **BccRecipients**abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d1261-p101">You cannot get **BccRecipients** by using a FindItem request. Use a GetItem request to get **BccRecipients**.</span></span>
  
<span data-ttu-id="d1261-147">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d1261-147">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d1261-148">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d1261-148">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1261-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="d1261-149">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d1261-150">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d1261-150">Schema Name</span></span>  <br/> |<span data-ttu-id="d1261-151">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d1261-151">Types schema</span></span>  <br/> |
|<span data-ttu-id="d1261-152">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d1261-152">Validation File</span></span>  <br/> |<span data-ttu-id="d1261-153">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d1261-153">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d1261-154">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d1261-154">Can be Empty</span></span>  <br/> |<span data-ttu-id="d1261-155">False</span><span class="sxs-lookup"><span data-stu-id="d1261-155">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d1261-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1261-156">See also</span></span>



- [<span data-ttu-id="d1261-157">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d1261-157">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

