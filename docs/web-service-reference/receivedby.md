---
title: ReceivedBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReceivedBy
api_type:
- schema
ms.assetid: ac84c9c5-d2fe-4b6f-bf4d-0444131d835b
description: Das ReceivedBy-Element identifiziert die Stellvertretung in einem Stellvertretungs-Zugriffs Szenario.
ms.openlocfilehash: 7cee996c15e81f77d71f42e052b14b1d21772ba1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468250"
---
# <a name="receivedby"></a><span data-ttu-id="7159a-103">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="7159a-103">ReceivedBy</span></span>

<span data-ttu-id="7159a-104">Das **ReceivedBy** -Element identifiziert die Stellvertretung in einem Stellvertretungs-Zugriffs Szenario.</span><span class="sxs-lookup"><span data-stu-id="7159a-104">The **ReceivedBy** element identifies the delegate in a delegate access scenario.</span></span> 
  
```xml
<ReceivedBy>
   <Mailbox/>
</ReceivedBy>
```

 <span data-ttu-id="7159a-105">**SingleRecipientType**</span><span class="sxs-lookup"><span data-stu-id="7159a-105">**SingleRecipientType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7159a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7159a-106">Attributes and elements</span></span>

<span data-ttu-id="7159a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7159a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7159a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7159a-108">Attributes</span></span>

<span data-ttu-id="7159a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7159a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7159a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7159a-110">Child elements</span></span>

|<span data-ttu-id="7159a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="7159a-111">**Element**</span></span>|<span data-ttu-id="7159a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7159a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7159a-113">Postfach</span><span class="sxs-lookup"><span data-stu-id="7159a-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="7159a-114">Ein e-Mail-aktivierten Active Directory Directory Service-Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7159a-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7159a-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7159a-115">Parent elements</span></span>

|<span data-ttu-id="7159a-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="7159a-116">**Element**</span></span>|<span data-ttu-id="7159a-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7159a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7159a-118">Message</span><span class="sxs-lookup"><span data-stu-id="7159a-118">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="7159a-119">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="7159a-119">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="7159a-120">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="7159a-120">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="7159a-121">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="7159a-121">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7159a-122">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="7159a-122">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="7159a-123">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="7159a-123">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7159a-124">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="7159a-124">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="7159a-125">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="7159a-125">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7159a-126">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="7159a-126">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="7159a-127">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="7159a-127">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7159a-128">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="7159a-128">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="7159a-129">Stellt eine Accept-Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="7159a-129">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="7159a-130">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="7159a-130">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="7159a-131">Stellt eine mit Vorbehalt Antworten auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="7159a-131">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="7159a-132">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="7159a-132">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="7159a-133">Stellt eine ablehnen Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="7159a-133">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="7159a-134">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="7159a-134">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="7159a-135">Enthält eine Antwort an den Ersteller eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="7159a-135">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7159a-136">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="7159a-136">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="7159a-137">Enthält eine Antwort an alle identifizierten Empfänger eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="7159a-137">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7159a-138">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="7159a-138">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="7159a-139">Enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="7159a-139">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="7159a-140">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="7159a-140">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="7159a-141">Stellt das Antwortobjekt, das Sie eine Besprechung absagen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7159a-141">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7159a-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7159a-142">Remarks</span></span>

<span data-ttu-id="7159a-143">Das **ReceivedRepresenting** -Element wird zusammen mit den **from** -und **ReceivedBy** -Elementen in Stellvertretungs-Zugriffsszenarien verwendet.</span><span class="sxs-lookup"><span data-stu-id="7159a-143">The **ReceivedRepresenting** element is used together with the **From** and **ReceivedBy** elements in delegate access scenarios.</span></span> <span data-ttu-id="7159a-144">In der folgenden Tabelle sind die Entitäten aufgeführt, die diese Elemente in einem Stellvertretungs-Zugriffs Szenario darstellen.</span><span class="sxs-lookup"><span data-stu-id="7159a-144">The following table lists the entities that these elements represent in a delegate access scenario.</span></span> 
  
<span data-ttu-id="7159a-145">**Elemente in einem Szenario mit Stellvertretungszugriff**</span><span class="sxs-lookup"><span data-stu-id="7159a-145">**Elements in a delegate access scenario**</span></span>

|<span data-ttu-id="7159a-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="7159a-146">**Element**</span></span>|<span data-ttu-id="7159a-147">**Entität, die das Element darstellt**</span><span class="sxs-lookup"><span data-stu-id="7159a-147">**Entity that the element represent**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7159a-148">From</span><span class="sxs-lookup"><span data-stu-id="7159a-148">From</span></span>](from.md) <br/> |<span data-ttu-id="7159a-149">ThirdParty</span><span class="sxs-lookup"><span data-stu-id="7159a-149">ThirdParty</span></span>  <br/> |
|[<span data-ttu-id="7159a-150">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="7159a-150">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="7159a-151">Stellvertretung</span><span class="sxs-lookup"><span data-stu-id="7159a-151">Delegate</span></span>  <br/> |
|[<span data-ttu-id="7159a-152">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="7159a-152">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="7159a-153">Principal</span><span class="sxs-lookup"><span data-stu-id="7159a-153">Principal</span></span>  <br/> |
   
<span data-ttu-id="7159a-154">Wenn ein thirdparty in einem Stellvertretungs-Zugriffs Szenario eine Besprechungsanfrage an einen Prinzipal sendet, der über eine Stellvertretung verfügt, wird der Stellvertretung eine neue Besprechungsanfrage angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7159a-154">In a delegate access scenario, if a ThirdParty sends a meeting request to a Principal who has a Delegate, the Delegate will see a new meeting request.</span></span> <span data-ttu-id="7159a-155">Diese Elemente ermöglichen Delegaten, zwischen Nachrichten zu unterscheiden, die direkt an Sie gesendet werden, und Nachrichten, die aufgrund einer Weiterleitungsregel für Delegaten an Sie gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="7159a-155">These elements enable delegates to distinguish between messages that are sent directly to them and messages that are sent to them because of a delegate forwarding rule.</span></span>
  
<span data-ttu-id="7159a-156">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7159a-156">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7159a-157">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7159a-157">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7159a-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="7159a-158">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7159a-159">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7159a-159">Schema Name</span></span>  <br/> |<span data-ttu-id="7159a-160">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7159a-160">Types schema</span></span>  <br/> |
|<span data-ttu-id="7159a-161">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7159a-161">Validation File</span></span>  <br/> |<span data-ttu-id="7159a-162">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7159a-162">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7159a-163">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7159a-163">Can be Empty</span></span>  <br/> |<span data-ttu-id="7159a-164">False</span><span class="sxs-lookup"><span data-stu-id="7159a-164">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7159a-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7159a-165">See also</span></span>



- [<span data-ttu-id="7159a-166">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7159a-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

