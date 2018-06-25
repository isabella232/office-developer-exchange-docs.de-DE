---
title: Absender
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Sender
api_type:
- schema
ms.assetid: 26d1a46e-e1d3-44b8-a02d-fa6f83aa5cda
description: Das Absender-Element identifiziert den Absender eines Elements.
ms.openlocfilehash: a7b06543fadd7cf7ae05f7ae8f86122138e11076
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831323"
---
# <a name="sender"></a><span data-ttu-id="74178-103">Absender</span><span class="sxs-lookup"><span data-stu-id="74178-103">Sender</span></span>

<span data-ttu-id="74178-104">Das **Absender** -Element identifiziert den Absender eines Elements.</span><span class="sxs-lookup"><span data-stu-id="74178-104">The **Sender** element identifies the sender of an item.</span></span> 
  
```xml
<Sender>
   <Mailbox/>
</Sender>
```

 <span data-ttu-id="74178-105">**SingleRecipientType**</span><span class="sxs-lookup"><span data-stu-id="74178-105">**SingleRecipientType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="74178-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="74178-106">Attributes and elements</span></span>

<span data-ttu-id="74178-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="74178-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="74178-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="74178-108">Attributes</span></span>

<span data-ttu-id="74178-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="74178-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="74178-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="74178-110">Child elements</span></span>

|<span data-ttu-id="74178-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="74178-111">**Element**</span></span>|<span data-ttu-id="74178-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="74178-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="74178-113">Postfach</span><span class="sxs-lookup"><span data-stu-id="74178-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="74178-114">Identifiziert ein e-Mail-aktivierte Active Directory-Objekt, das den Absender identifiziert.</span><span class="sxs-lookup"><span data-stu-id="74178-114">Identifies a mail enabled Active Directory object that identifies the sender.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="74178-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="74178-115">Parent elements</span></span>

|<span data-ttu-id="74178-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="74178-116">**Element**</span></span>|<span data-ttu-id="74178-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="74178-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="74178-118">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="74178-118">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="74178-119">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="74178-119">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="74178-120">Message</span><span class="sxs-lookup"><span data-stu-id="74178-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="74178-121">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="74178-121">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="74178-122">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="74178-122">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="74178-123">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="74178-123">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="74178-124">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="74178-124">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="74178-125">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="74178-125">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="74178-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="74178-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="74178-127">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="74178-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="74178-128">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="74178-128">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="74178-129">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="74178-129">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="74178-130">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="74178-130">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="74178-131">Stellt eine Accept-Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="74178-131">Represents an accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="74178-132">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="74178-132">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="74178-133">Stellt eine Vorbehalt Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="74178-133">Represents a tentatively accepted reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="74178-134">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="74178-134">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="74178-135">Stellt eine ablehnen Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="74178-135">Represents a decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="74178-136">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="74178-136">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="74178-137">Enthält eine Antwort an den Ersteller eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="74178-137">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="74178-138">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="74178-138">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="74178-139">Enthält eine Antwort an alle identifizierten Empfänger eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="74178-139">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="74178-140">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="74178-140">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="74178-141">Enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="74178-141">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="74178-142">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="74178-142">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="74178-143">Verwendet, um eine Besprechung absagen Response-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="74178-143">Represents the response object used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="74178-144">PostItem-Objekt</span><span class="sxs-lookup"><span data-stu-id="74178-144">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="74178-145">Stellt ein Post-Element im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="74178-145">Represents a post item in the Exchange store.</span></span> <span data-ttu-id="74178-146">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="74178-146">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74178-147">Hinweise</span><span class="sxs-lookup"><span data-stu-id="74178-147">Remarks</span></span>

<span data-ttu-id="74178-148">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="74178-148">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="74178-149">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="74178-149">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="74178-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="74178-150">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="74178-151">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="74178-151">Schema Name</span></span>  <br/> |<span data-ttu-id="74178-152">Schematypen</span><span class="sxs-lookup"><span data-stu-id="74178-152">Types schema</span></span>  <br/> |
|<span data-ttu-id="74178-153">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="74178-153">Validation File</span></span>  <br/> |<span data-ttu-id="74178-154">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="74178-154">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="74178-155">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="74178-155">Can be Empty</span></span>  <br/> |<span data-ttu-id="74178-156">False</span><span class="sxs-lookup"><span data-stu-id="74178-156">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="74178-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74178-157">See also</span></span>



- [<span data-ttu-id="74178-158">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="74178-158">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

