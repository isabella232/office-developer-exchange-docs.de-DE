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
description: Das from-Element stellt die Adresse dar, von der die Nachricht gesendet wurde.
ms.openlocfilehash: c0d655731677e56cc02c7c029264ffc96f0a18c2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459553"
---
# <a name="from"></a><span data-ttu-id="07cdd-103">Von</span><span class="sxs-lookup"><span data-stu-id="07cdd-103">From</span></span>

<span data-ttu-id="07cdd-104">Das **from** -Element stellt die Adresse dar, von der die Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="07cdd-104">The **From** element represents the address from which the message was sent.</span></span> 
  
```xml
<From>
   <Mailbox/>
</From>
```

 <span data-ttu-id="07cdd-105">**SingleRecipientType**</span><span class="sxs-lookup"><span data-stu-id="07cdd-105">**SingleRecipientType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="07cdd-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="07cdd-106">Attributes and elements</span></span>

<span data-ttu-id="07cdd-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="07cdd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="07cdd-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="07cdd-108">Attributes</span></span>

<span data-ttu-id="07cdd-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="07cdd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="07cdd-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="07cdd-110">Child elements</span></span>

|<span data-ttu-id="07cdd-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="07cdd-111">**Element**</span></span>|<span data-ttu-id="07cdd-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="07cdd-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07cdd-113">Postfach</span><span class="sxs-lookup"><span data-stu-id="07cdd-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="07cdd-114">Ein e-Mail-aktivierten Active Directory Directory Service-Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="07cdd-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="07cdd-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="07cdd-115">Parent elements</span></span>

|<span data-ttu-id="07cdd-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="07cdd-116">**Element**</span></span>|<span data-ttu-id="07cdd-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="07cdd-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07cdd-118">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="07cdd-118">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="07cdd-119">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="07cdd-119">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="07cdd-120">Message</span><span class="sxs-lookup"><span data-stu-id="07cdd-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="07cdd-121">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="07cdd-121">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="07cdd-122">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="07cdd-122">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="07cdd-123">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="07cdd-123">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="07cdd-124">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="07cdd-124">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="07cdd-125">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="07cdd-125">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="07cdd-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="07cdd-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="07cdd-127">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="07cdd-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="07cdd-128">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="07cdd-128">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="07cdd-129">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="07cdd-129">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="07cdd-130">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="07cdd-130">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="07cdd-131">Stellt eine Accept-Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="07cdd-131">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="07cdd-132">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="07cdd-132">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="07cdd-133">Stellt eine mit Vorbehalt Antworten auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="07cdd-133">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="07cdd-134">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="07cdd-134">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="07cdd-135">Stellt eine ablehnen Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="07cdd-135">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="07cdd-136">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="07cdd-136">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="07cdd-137">Enthält eine Antwort an den Ersteller eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="07cdd-137">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="07cdd-138">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="07cdd-138">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="07cdd-139">Enthält eine Antwort an alle identifizierten Empfänger eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="07cdd-139">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="07cdd-140">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="07cdd-140">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="07cdd-141">Enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="07cdd-141">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="07cdd-142">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="07cdd-142">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="07cdd-143">Stellt das Antwortobjekt, das Sie eine Besprechung absagen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="07cdd-143">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="07cdd-144">PostItem</span><span class="sxs-lookup"><span data-stu-id="07cdd-144">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="07cdd-145">Stellt ein Post-Element im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="07cdd-145">Represents a post item in the Exchange store.</span></span> <span data-ttu-id="07cdd-146">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="07cdd-146">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07cdd-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07cdd-147">Remarks</span></span>

<span data-ttu-id="07cdd-148">Dieses Element wird für e-Mails vom "Senden im Auftrag von" verwendet.</span><span class="sxs-lookup"><span data-stu-id="07cdd-148">This element is used for "send on behalf of" e-mails.</span></span>
  
<span data-ttu-id="07cdd-149">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="07cdd-149">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="07cdd-150">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="07cdd-150">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="07cdd-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="07cdd-151">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="07cdd-152">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="07cdd-152">Schema Name</span></span>  <br/> |<span data-ttu-id="07cdd-153">Schematypen</span><span class="sxs-lookup"><span data-stu-id="07cdd-153">Types schema</span></span>  <br/> |
|<span data-ttu-id="07cdd-154">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="07cdd-154">Validation File</span></span>  <br/> |<span data-ttu-id="07cdd-155">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="07cdd-155">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="07cdd-156">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="07cdd-156">Can be Empty</span></span>  <br/> |<span data-ttu-id="07cdd-157">False</span><span class="sxs-lookup"><span data-stu-id="07cdd-157">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="07cdd-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07cdd-158">See also</span></span>



- [<span data-ttu-id="07cdd-159">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="07cdd-159">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

