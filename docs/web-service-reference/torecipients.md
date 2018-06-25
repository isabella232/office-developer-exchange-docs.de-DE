---
title: ToRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ToRecipients
api_type:
- schema
ms.assetid: 72dc3be8-30bb-4ae1-acf4-fb94ff490631
description: Das ToRecipients -Element enthält ein Array von Empfänger eines Elements. Dies sind die primären Empfänger eines Elements.
ms.openlocfilehash: 2913705cad52c041809769fe58efc3d616f40462
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839239"
---
# <a name="torecipients"></a><span data-ttu-id="cc750-104">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="cc750-104">ToRecipients</span></span>

<span data-ttu-id="cc750-p102">Das **ToRecipients** -Element enthält ein Array von Empfänger eines Elements. Dies sind die primären Empfänger eines Elements.</span><span class="sxs-lookup"><span data-stu-id="cc750-p102">The **ToRecipients** element contains an array of recipients of an item. These are the primary recipients of an item.</span></span> 
  
```xml
<ToRecipients>
   <Mailbox/>
</ToRecipients>
```

 <span data-ttu-id="cc750-107">**ArrayOfRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="cc750-107">**ArrayOfRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cc750-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cc750-108">Attributes and elements</span></span>

<span data-ttu-id="cc750-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cc750-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cc750-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="cc750-110">Attributes</span></span>

<span data-ttu-id="cc750-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="cc750-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cc750-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cc750-112">Child elements</span></span>

|<span data-ttu-id="cc750-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="cc750-113">**Element**</span></span>|<span data-ttu-id="cc750-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cc750-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cc750-115">Postfach</span><span class="sxs-lookup"><span data-stu-id="cc750-115">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="cc750-116">Ein e-Mail-aktivierten Active Directory Directory Service-Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cc750-116">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cc750-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cc750-117">Parent elements</span></span>

|<span data-ttu-id="cc750-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="cc750-118">**Element**</span></span>|<span data-ttu-id="cc750-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cc750-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cc750-120">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="cc750-120">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="cc750-121">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="cc750-121">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="cc750-122">Message</span><span class="sxs-lookup"><span data-stu-id="cc750-122">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="cc750-123">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="cc750-123">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="cc750-124">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="cc750-124">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="cc750-125">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="cc750-125">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="cc750-126">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="cc750-126">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="cc750-127">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="cc750-127">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="cc750-128">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="cc750-128">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="cc750-129">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="cc750-129">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="cc750-130">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="cc750-130">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="cc750-131">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="cc750-131">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="cc750-132">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="cc750-132">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="cc750-133">Stellt eine Accept-Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="cc750-133">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="cc750-134">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="cc750-134">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="cc750-135">Stellt eine mit Vorbehalt Antworten auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="cc750-135">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="cc750-136">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="cc750-136">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="cc750-137">Stellt eine ablehnen Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="cc750-137">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="cc750-138">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="cc750-138">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="cc750-139">Enthält eine Antwort an den Ersteller eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="cc750-139">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="cc750-140">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="cc750-140">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="cc750-141">Enthält eine Antwort an alle identifizierten Empfänger eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="cc750-141">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="cc750-142">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="cc750-142">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="cc750-143">Enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="cc750-143">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="cc750-144">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="cc750-144">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="cc750-145">Stellt das Antwortobjekt, das Sie eine Besprechung absagen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cc750-145">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc750-146">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cc750-146">Remarks</span></span>

<span data-ttu-id="cc750-p103">Sie können nicht **ToRecipients** mithilfe einer Anforderung FindItem abrufen. Verwenden Sie eine Anforderung GetItem, um die **ToRecipients**abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cc750-p103">You cannot get **ToRecipients** by using a FindItem request. Use a GetItem request to get the **ToRecipients**.</span></span>
  
<span data-ttu-id="cc750-149">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="cc750-149">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cc750-150">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="cc750-150">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cc750-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="cc750-151">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cc750-152">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cc750-152">Schema Name</span></span>  <br/> |<span data-ttu-id="cc750-153">Schematypen</span><span class="sxs-lookup"><span data-stu-id="cc750-153">Types schema</span></span>  <br/> |
|<span data-ttu-id="cc750-154">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cc750-154">Validation File</span></span>  <br/> |<span data-ttu-id="cc750-155">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cc750-155">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cc750-156">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="cc750-156">Can be Empty</span></span>  <br/> |<span data-ttu-id="cc750-157">False</span><span class="sxs-lookup"><span data-stu-id="cc750-157">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cc750-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc750-158">See also</span></span>



- [<span data-ttu-id="cc750-159">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="cc750-159">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

