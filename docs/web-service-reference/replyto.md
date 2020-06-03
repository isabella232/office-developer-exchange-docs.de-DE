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
description: Das ReplyTo-Element identifiziert ein Array von Adressen, an die Antworten gesendet werden sollen.
ms.openlocfilehash: 08f9edce76fd01111922a2a07d1a63e288a0c1ee
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468327"
---
# <a name="replyto"></a><span data-ttu-id="147ee-103">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="147ee-103">ReplyTo</span></span>

<span data-ttu-id="147ee-104">Das **ReplyTo** -Element identifiziert ein Array von Adressen, an die Antworten gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="147ee-104">The **ReplyTo** element identifies an array of addresses to which replies should be sent.</span></span> 
  
```xml
<ReplyTo>
   <Mailbox/>
</ReplyTo>
```

 <span data-ttu-id="147ee-105">**ArrayOfRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="147ee-105">**ArrayOfRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="147ee-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="147ee-106">Attributes and elements</span></span>

<span data-ttu-id="147ee-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="147ee-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="147ee-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="147ee-108">Attributes</span></span>

<span data-ttu-id="147ee-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="147ee-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="147ee-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="147ee-110">Child elements</span></span>

|<span data-ttu-id="147ee-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="147ee-111">**Element**</span></span>|<span data-ttu-id="147ee-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="147ee-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="147ee-113">Postfach</span><span class="sxs-lookup"><span data-stu-id="147ee-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="147ee-114">Identifiziert ein e-Mail-aktiviertes Active Directory Verzeichnisdienstobjekt, an das eine Antwort gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="147ee-114">Identifies a mail-enabled Active Directory directory service object to which a reply is sent.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="147ee-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="147ee-115">Parent elements</span></span>

|<span data-ttu-id="147ee-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="147ee-116">**Element**</span></span>|<span data-ttu-id="147ee-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="147ee-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="147ee-118">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="147ee-118">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="147ee-119">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="147ee-119">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="147ee-120">Message</span><span class="sxs-lookup"><span data-stu-id="147ee-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="147ee-121">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="147ee-121">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="147ee-122">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="147ee-122">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="147ee-123">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="147ee-123">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="147ee-124">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="147ee-124">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="147ee-125">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="147ee-125">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="147ee-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="147ee-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="147ee-127">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="147ee-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="147ee-128">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="147ee-128">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="147ee-129">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="147ee-129">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="147ee-130">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="147ee-130">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="147ee-131">Stellt eine Accept-Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="147ee-131">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="147ee-132">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="147ee-132">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="147ee-133">Stellt eine mit Vorbehalt Antworten auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="147ee-133">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="147ee-134">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="147ee-134">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="147ee-135">Stellt eine ablehnen Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="147ee-135">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="147ee-136">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="147ee-136">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="147ee-137">Enthält eine Antwort an den Ersteller eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="147ee-137">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="147ee-138">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="147ee-138">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="147ee-139">Enthält eine Antwort an alle identifizierten Empfänger eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="147ee-139">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="147ee-140">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="147ee-140">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="147ee-141">Enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="147ee-141">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="147ee-142">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="147ee-142">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="147ee-143">Stellt das Antwortobjekt, das Sie eine Besprechung absagen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="147ee-143">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="147ee-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="147ee-144">Remarks</span></span>

<span data-ttu-id="147ee-145">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="147ee-145">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="147ee-146">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="147ee-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="147ee-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="147ee-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="147ee-148">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="147ee-148">Schema Name</span></span>  <br/> |<span data-ttu-id="147ee-149">Schematypen</span><span class="sxs-lookup"><span data-stu-id="147ee-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="147ee-150">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="147ee-150">Validation File</span></span>  <br/> |<span data-ttu-id="147ee-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="147ee-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="147ee-152">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="147ee-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="147ee-153">False</span><span class="sxs-lookup"><span data-stu-id="147ee-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="147ee-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="147ee-154">See also</span></span>



- [<span data-ttu-id="147ee-155">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="147ee-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

