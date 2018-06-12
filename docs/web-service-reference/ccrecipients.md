---
title: CcRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CcRecipients
api_type:
- schema
ms.assetid: 5c20ec3a-0bee-4e67-b220-586ed0d601c9
description: Das Element CcRecipients stellt eine Sammlung von Empfängern, die eine Kopie der Nachricht erhalten.
ms.openlocfilehash: 0afe19cfae49dbf48c685296a83ab1330b631d04
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757556"
---
# <a name="ccrecipients"></a><span data-ttu-id="e98b4-103">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="e98b4-103">CcRecipients</span></span>

<span data-ttu-id="e98b4-104">Das Element **CcRecipients** stellt eine Sammlung von Empfängern, die eine Kopie der Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="e98b4-104">The **CcRecipients** element represents a collection of recipients that will receive a copy of the message.</span></span> 
  
```xml
<CcRecipients>
   <Mailbox/>
</CcRecipients>
```

 <span data-ttu-id="e98b4-105">**ArrayOfRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="e98b4-105">**ArrayOfRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e98b4-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e98b4-106">Attributes and elements</span></span>

<span data-ttu-id="e98b4-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e98b4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e98b4-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e98b4-108">Attributes</span></span>

<span data-ttu-id="e98b4-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e98b4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e98b4-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e98b4-110">Child elements</span></span>

|<span data-ttu-id="e98b4-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e98b4-111">**Element**</span></span>|<span data-ttu-id="e98b4-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e98b4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e98b4-113">Postfach</span><span class="sxs-lookup"><span data-stu-id="e98b4-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="e98b4-114">Ein e-Mail-aktivierten Active Directory Directory Service-Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e98b4-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e98b4-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e98b4-115">Parent elements</span></span>

|<span data-ttu-id="e98b4-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="e98b4-116">**Element**</span></span>|<span data-ttu-id="e98b4-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e98b4-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e98b4-118">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="e98b4-118">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="e98b4-119">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="e98b4-119">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e98b4-120">Message</span><span class="sxs-lookup"><span data-stu-id="e98b4-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="e98b4-121">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="e98b4-121">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="e98b4-122">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="e98b4-122">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="e98b4-123">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="e98b4-123">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e98b4-124">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="e98b4-124">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="e98b4-125">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="e98b4-125">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e98b4-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="e98b4-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="e98b4-127">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="e98b4-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e98b4-128">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="e98b4-128">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="e98b4-129">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="e98b4-129">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e98b4-130">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="e98b4-130">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="e98b4-131">Stellt eine Accept-Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="e98b4-131">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="e98b4-132">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="e98b4-132">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="e98b4-133">Stellt eine mit Vorbehalt Antworten auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="e98b4-133">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="e98b4-134">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="e98b4-134">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="e98b4-135">Stellt eine ablehnen Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="e98b4-135">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="e98b4-136">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="e98b4-136">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="e98b4-137">Enthält eine Antwort an den Ersteller eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="e98b4-137">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e98b4-138">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="e98b4-138">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="e98b4-139">Enthält eine Antwort an alle identifizierten Empfänger eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="e98b4-139">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e98b4-140">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="e98b4-140">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="e98b4-141">Enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="e98b4-141">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="e98b4-142">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="e98b4-142">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="e98b4-143">Stellt das Antwortobjekt, das Sie eine Besprechung absagen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e98b4-143">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e98b4-144">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e98b4-144">Remarks</span></span>

<span data-ttu-id="e98b4-p101">Sie können nicht **CcRecipients** mithilfe einer Anforderung FindItem abrufen. Verwenden Sie eine Anforderung GetItem **CcRecipients**abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e98b4-p101">You cannot get **CcRecipients** by using a FindItem request. Use a GetItem request to get **CcRecipients**.</span></span>
  
<span data-ttu-id="e98b4-147">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="e98b4-147">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e98b4-148">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e98b4-148">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e98b4-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="e98b4-149">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e98b4-150">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e98b4-150">Schema Name</span></span>  <br/> |<span data-ttu-id="e98b4-151">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e98b4-151">Types schema</span></span>  <br/> |
|<span data-ttu-id="e98b4-152">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e98b4-152">Validation File</span></span>  <br/> |<span data-ttu-id="e98b4-153">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e98b4-153">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e98b4-154">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e98b4-154">Can be Empty</span></span>  <br/> |<span data-ttu-id="e98b4-155">False</span><span class="sxs-lookup"><span data-stu-id="e98b4-155">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e98b4-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e98b4-156">See also</span></span>



- [<span data-ttu-id="e98b4-157">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e98b4-157">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

