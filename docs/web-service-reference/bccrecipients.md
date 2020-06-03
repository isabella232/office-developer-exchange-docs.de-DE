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
ms.openlocfilehash: 96070415c6d92a893f6c560884d9d191c7d5f15b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529504"
---
# <a name="bccrecipients"></a><span data-ttu-id="822fb-103">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="822fb-103">BccRecipients</span></span>

<span data-ttu-id="822fb-104">Das Element **BccRecipients** stellt eine Auflistung der Empfänger, die eine Blindkopie (Bcc) einer e-Mail-Nachricht empfangen.</span><span class="sxs-lookup"><span data-stu-id="822fb-104">The **BccRecipients** element represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail message.</span></span> 
  
```xml
<BccRecipients>
   <Mailbox/>
</BccRecipients>
```

 <span data-ttu-id="822fb-105">**ArrayOfRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="822fb-105">**ArrayOfRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="822fb-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="822fb-106">Attributes and elements</span></span>

<span data-ttu-id="822fb-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="822fb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="822fb-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="822fb-108">Attributes</span></span>

<span data-ttu-id="822fb-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="822fb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="822fb-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="822fb-110">Child elements</span></span>

|<span data-ttu-id="822fb-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="822fb-111">**Element**</span></span>|<span data-ttu-id="822fb-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="822fb-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="822fb-113">Postfach</span><span class="sxs-lookup"><span data-stu-id="822fb-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="822fb-114">Ein e-Mail-aktivierten Active Directory Directory Service-Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="822fb-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="822fb-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="822fb-115">Parent elements</span></span>

|<span data-ttu-id="822fb-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="822fb-116">**Element**</span></span>|<span data-ttu-id="822fb-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="822fb-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="822fb-118">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="822fb-118">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="822fb-119">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="822fb-119">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="822fb-120">Message</span><span class="sxs-lookup"><span data-stu-id="822fb-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="822fb-121">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="822fb-121">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="822fb-122">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="822fb-122">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="822fb-123">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="822fb-123">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="822fb-124">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="822fb-124">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="822fb-125">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="822fb-125">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="822fb-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="822fb-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="822fb-127">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="822fb-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="822fb-128">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="822fb-128">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="822fb-129">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="822fb-129">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="822fb-130">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="822fb-130">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="822fb-131">Stellt eine Accept-Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="822fb-131">Represents an accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="822fb-132">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="822fb-132">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="822fb-133">Stellt eine Vorbehalt Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="822fb-133">Represents a tentatively accepted reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="822fb-134">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="822fb-134">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="822fb-135">Stellt eine ablehnen Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="822fb-135">Represents a decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="822fb-136">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="822fb-136">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="822fb-137">Enthält eine Antwort an den Ersteller eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="822fb-137">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="822fb-138">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="822fb-138">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="822fb-139">Enthält eine Antwort an alle identifizierten Empfänger eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="822fb-139">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="822fb-140">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="822fb-140">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="822fb-141">Enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="822fb-141">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="822fb-142">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="822fb-142">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="822fb-143">Stellt das Antwortobjekt, das Sie eine Besprechung absagen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="822fb-143">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="822fb-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="822fb-144">Remarks</span></span>

<span data-ttu-id="822fb-p101">Sie können nicht **BccRecipients** mithilfe einer Anforderung FindItem abrufen. Verwenden Sie eine Anforderung GetItem **BccRecipients**abgerufen.</span><span class="sxs-lookup"><span data-stu-id="822fb-p101">You cannot get **BccRecipients** by using a FindItem request. Use a GetItem request to get **BccRecipients**.</span></span>
  
<span data-ttu-id="822fb-147">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="822fb-147">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="822fb-148">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="822fb-148">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="822fb-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="822fb-149">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="822fb-150">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="822fb-150">Schema Name</span></span>  <br/> |<span data-ttu-id="822fb-151">Schematypen</span><span class="sxs-lookup"><span data-stu-id="822fb-151">Types schema</span></span>  <br/> |
|<span data-ttu-id="822fb-152">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="822fb-152">Validation File</span></span>  <br/> |<span data-ttu-id="822fb-153">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="822fb-153">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="822fb-154">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="822fb-154">Can be Empty</span></span>  <br/> |<span data-ttu-id="822fb-155">False</span><span class="sxs-lookup"><span data-stu-id="822fb-155">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="822fb-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="822fb-156">See also</span></span>



- [<span data-ttu-id="822fb-157">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="822fb-157">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

