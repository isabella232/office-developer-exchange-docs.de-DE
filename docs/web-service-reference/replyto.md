---
title: ReplyTo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReplyTo
api_type:
- schema
ms.assetid: 6b6ae792-e2c4-4aa0-95cb-b49b446f1e08
description: Das ReplyTo-Element gibt einen Array von Adressen, die an die Antworten gesendet werden soll.
ms.openlocfilehash: 0ceb4f5edb75bbfe52a7a7156da3c2a328bea346
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831115"
---
# <a name="replyto"></a><span data-ttu-id="ae57a-103">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="ae57a-103">ReplyTo</span></span>

<span data-ttu-id="ae57a-104">Das **ReplyTo** -Element gibt einen Array von Adressen, die an die Antworten gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ae57a-104">The **ReplyTo** element identifies an array of addresses to which replies should be sent.</span></span> 
  
```xml
<ReplyTo>
   <Mailbox/>
</ReplyTo>
```

 <span data-ttu-id="ae57a-105">**ArrayOfRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="ae57a-105">**ArrayOfRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ae57a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ae57a-106">Attributes and elements</span></span>

<span data-ttu-id="ae57a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ae57a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ae57a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ae57a-108">Attributes</span></span>

<span data-ttu-id="ae57a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ae57a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ae57a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ae57a-110">Child elements</span></span>

|<span data-ttu-id="ae57a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ae57a-111">**Element**</span></span>|<span data-ttu-id="ae57a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ae57a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae57a-113">Postfach</span><span class="sxs-lookup"><span data-stu-id="ae57a-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="ae57a-114">Identifiziert eine e-Mail-aktivierte Active Directory Directory Service-Objekt an die eine Antwort gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="ae57a-114">Identifies a mail-enabled Active Directory directory service object to which a reply is sent.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ae57a-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ae57a-115">Parent elements</span></span>

|<span data-ttu-id="ae57a-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="ae57a-116">**Element**</span></span>|<span data-ttu-id="ae57a-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ae57a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae57a-118">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="ae57a-118">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="ae57a-119">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="ae57a-119">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ae57a-120">Message</span><span class="sxs-lookup"><span data-stu-id="ae57a-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="ae57a-121">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="ae57a-121">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="ae57a-122">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="ae57a-122">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="ae57a-123">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="ae57a-123">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ae57a-124">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="ae57a-124">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="ae57a-125">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="ae57a-125">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ae57a-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="ae57a-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="ae57a-127">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="ae57a-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ae57a-128">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="ae57a-128">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="ae57a-129">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="ae57a-129">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ae57a-130">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="ae57a-130">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="ae57a-131">Stellt eine Accept-Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="ae57a-131">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="ae57a-132">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="ae57a-132">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="ae57a-133">Stellt eine mit Vorbehalt Antworten auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="ae57a-133">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="ae57a-134">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="ae57a-134">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="ae57a-135">Stellt eine ablehnen Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="ae57a-135">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="ae57a-136">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="ae57a-136">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="ae57a-137">Enthält eine Antwort an den Ersteller eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="ae57a-137">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ae57a-138">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="ae57a-138">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="ae57a-139">Enthält eine Antwort an alle identifizierten Empfänger eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="ae57a-139">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ae57a-140">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="ae57a-140">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="ae57a-141">Enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="ae57a-141">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="ae57a-142">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="ae57a-142">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="ae57a-143">Stellt das Antwortobjekt, das Sie eine Besprechung absagen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ae57a-143">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae57a-144">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ae57a-144">Remarks</span></span>

<span data-ttu-id="ae57a-145">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ae57a-145">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ae57a-146">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ae57a-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae57a-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="ae57a-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ae57a-148">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ae57a-148">Schema Name</span></span>  <br/> |<span data-ttu-id="ae57a-149">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ae57a-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="ae57a-150">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ae57a-150">Validation File</span></span>  <br/> |<span data-ttu-id="ae57a-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ae57a-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ae57a-152">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ae57a-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="ae57a-153">False</span><span class="sxs-lookup"><span data-stu-id="ae57a-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ae57a-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae57a-154">See also</span></span>



- [<span data-ttu-id="ae57a-155">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ae57a-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

