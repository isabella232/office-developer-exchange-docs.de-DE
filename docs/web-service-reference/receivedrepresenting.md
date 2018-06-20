---
title: ReceivedRepresenting
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReceivedRepresenting
api_type:
- schema
ms.assetid: 1157b042-6dce-4cdc-9700-e22b749da39f
description: Das ReceivedRepresenting-Element identifiziert den Prinzipal in einer Access Stellvertreter-Szenario.
ms.openlocfilehash: 1587fcae6975b986711e7223e50c60658833cc80
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830973"
---
# <a name="receivedrepresenting"></a><span data-ttu-id="ab965-103">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="ab965-103">ReceivedRepresenting</span></span>

<span data-ttu-id="ab965-104">Das **ReceivedRepresenting** -Element identifiziert den Prinzipal in einer Access Stellvertreter-Szenario.</span><span class="sxs-lookup"><span data-stu-id="ab965-104">The **ReceivedRepresenting** element identifies the principal in a delegate access scenario.</span></span> 
  
```xml
<ReceivedRepresenting>
   <Mailbox/>
</ReceivedRepresenting>
```

 <span data-ttu-id="ab965-105">**SingleRecipientType**</span><span class="sxs-lookup"><span data-stu-id="ab965-105">**SingleRecipientType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ab965-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ab965-106">Attributes and elements</span></span>

<span data-ttu-id="ab965-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ab965-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ab965-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ab965-108">Attributes</span></span>

<span data-ttu-id="ab965-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ab965-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ab965-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ab965-110">Child elements</span></span>

|<span data-ttu-id="ab965-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ab965-111">**Element**</span></span>|<span data-ttu-id="ab965-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ab965-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ab965-113">Postfach</span><span class="sxs-lookup"><span data-stu-id="ab965-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="ab965-114">Ein e-Mail-aktivierten Active Directory Directory Service-Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ab965-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ab965-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ab965-115">Parent elements</span></span>

|<span data-ttu-id="ab965-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="ab965-116">**Element**</span></span>|<span data-ttu-id="ab965-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ab965-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ab965-118">Message</span><span class="sxs-lookup"><span data-stu-id="ab965-118">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="ab965-119">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="ab965-119">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="ab965-120">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="ab965-120">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="ab965-121">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="ab965-121">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ab965-122">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="ab965-122">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="ab965-123">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="ab965-123">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ab965-124">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="ab965-124">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="ab965-125">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="ab965-125">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ab965-126">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="ab965-126">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="ab965-127">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="ab965-127">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ab965-128">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="ab965-128">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="ab965-129">Stellt eine Accept-Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="ab965-129">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="ab965-130">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="ab965-130">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="ab965-131">Stellt eine mit Vorbehalt Antworten auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="ab965-131">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="ab965-132">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="ab965-132">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="ab965-133">Stellt eine ablehnen Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="ab965-133">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="ab965-134">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="ab965-134">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="ab965-135">Enthält eine Antwort an den Ersteller eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="ab965-135">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ab965-136">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="ab965-136">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="ab965-137">Enthält eine Antwort an alle identifizierten Empfänger eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="ab965-137">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ab965-138">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="ab965-138">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="ab965-139">Enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="ab965-139">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="ab965-140">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="ab965-140">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="ab965-141">Stellt das Antwortobjekt, das Sie eine Besprechung absagen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ab965-141">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab965-142">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ab965-142">Remarks</span></span>

<span data-ttu-id="ab965-143">Das **ReceivedRepresenting** -Element wird zusammen mit den **von** verwendet und **ReceivedBy** Elemente in Access-Szenarien delegieren.</span><span class="sxs-lookup"><span data-stu-id="ab965-143">The **ReceivedRepresenting** element is used together with the **From** and **ReceivedBy** elements in delegate access scenarios.</span></span> <span data-ttu-id="ab965-144">Die folgende Tabelle enthält die Entitäten, die diese Elemente in einem Szenario mit Access Delegaten darstellen.</span><span class="sxs-lookup"><span data-stu-id="ab965-144">The following table lists the entities that these elements represent in a delegate access scenario.</span></span> 
  
<span data-ttu-id="ab965-145">**Elemente in einer Access Stellvertreter-Szenario**</span><span class="sxs-lookup"><span data-stu-id="ab965-145">**Elements in a delegate access scenario**</span></span>

|<span data-ttu-id="ab965-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="ab965-146">**Element**</span></span>|<span data-ttu-id="ab965-147">**Entität, die das Element darstellen.**</span><span class="sxs-lookup"><span data-stu-id="ab965-147">**Entity that the element represent**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ab965-148">Von</span><span class="sxs-lookup"><span data-stu-id="ab965-148">From</span></span>](from.md) <br/> |<span data-ttu-id="ab965-149">ThirdParty</span><span class="sxs-lookup"><span data-stu-id="ab965-149">ThirdParty</span></span>  <br/> |
|[<span data-ttu-id="ab965-150">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="ab965-150">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="ab965-151">Delegieren</span><span class="sxs-lookup"><span data-stu-id="ab965-151">Delegate</span></span>  <br/> |
|[<span data-ttu-id="ab965-152">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="ab965-152">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="ab965-153">Direktor</span><span class="sxs-lookup"><span data-stu-id="ab965-153">Principal</span></span>  <br/> |
   
<span data-ttu-id="ab965-154">In einem Szenario mit Access Delegaten Wenn eine ThirdParty einem Prinzipal eine Besprechungsanfrage sendet, die eine Stellvertretung hat sehen die Stellvertretung eine neue Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="ab965-154">In a delegate access scenario, if a ThirdParty sends a meeting request to a Principal who has a Delegate, the Delegate will see a new meeting request.</span></span> <span data-ttu-id="ab965-155">Diese Elemente aktivieren Delegaten zu unterscheiden, die direkt an diese gesendet werden und Nachrichten, die aufgrund einer Stellvertretung weiterleiten Regel an sie gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab965-155">These elements enable delegates to distinguish between messages that are sent directly to them and messages that are sent to them because of a delegate forwarding rule.</span></span>
  
<span data-ttu-id="ab965-156">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ab965-156">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ab965-157">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ab965-157">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ab965-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="ab965-158">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ab965-159">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ab965-159">Schema Name</span></span>  <br/> |<span data-ttu-id="ab965-160">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ab965-160">Types schema</span></span>  <br/> |
|<span data-ttu-id="ab965-161">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ab965-161">Validation File</span></span>  <br/> |<span data-ttu-id="ab965-162">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ab965-162">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ab965-163">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ab965-163">Can be Empty</span></span>  <br/> |<span data-ttu-id="ab965-164">False</span><span class="sxs-lookup"><span data-stu-id="ab965-164">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ab965-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab965-165">See also</span></span>



- [<span data-ttu-id="ab965-166">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ab965-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

