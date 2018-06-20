---
title: TentativelyAcceptItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TentativelyAcceptItem
api_type:
- schema
ms.assetid: ce6f50ef-ad8a-47e4-915a-487b2ef7a2e0
description: Eine mit Vorbehalt Antworten auf eine Besprechungsanfrage TentativelyAcceptItem-Element darstellt.
ms.openlocfilehash: 203028aae2ec972e36209b2a97420e83d61ddd81
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839183"
---
# <a name="tentativelyacceptitem"></a><span data-ttu-id="b979b-103">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="b979b-103">TentativelyAcceptItem</span></span>

<span data-ttu-id="b979b-104">Eine mit Vorbehalt Antworten auf eine Besprechungsanfrage **TentativelyAcceptItem** -Element darstellt.</span><span class="sxs-lookup"><span data-stu-id="b979b-104">The **TentativelyAcceptItem** element represents a Tentative reply to a meeting request.</span></span> 
  
```xml
<TentativelyAcceptItem>
   <ItemClass/>
   <Sensitivity/>
   <Body/>
   <Attachments/>
   <InternetMessageHeaders/>
   <Sender/>
   <ToRecipients/>
   <CcRecipients/>
   <BccRecipients/>
   <IsReadReceiptRequested/>
   <IsDeliveryReceiptRequested/>
   <ReferenceItemId/>
   <ReceivedBy/>
   <ReceivedRepresenting/>
   <ProposedStart/>
   <ProposedEnd/>
</TentativelyAcceptItem>
```

 <span data-ttu-id="b979b-105">**TentativelyAcceptItemType**</span><span class="sxs-lookup"><span data-stu-id="b979b-105">**TentativelyAcceptItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b979b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b979b-106">Attributes and elements</span></span>

<span data-ttu-id="b979b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b979b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b979b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b979b-108">Attributes</span></span>

<span data-ttu-id="b979b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b979b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b979b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b979b-110">Child elements</span></span>

|<span data-ttu-id="b979b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b979b-111">**Element**</span></span>|<span data-ttu-id="b979b-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b979b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b979b-113">ItemClass</span><span class="sxs-lookup"><span data-stu-id="b979b-113">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="b979b-114">Die Nachrichtenklasse eines Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="b979b-114">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="b979b-115">Vertraulichkeit</span><span class="sxs-lookup"><span data-stu-id="b979b-115">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="b979b-116">Identifiziert die Vertraulichkeit eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="b979b-116">Identifies the sensitivity of an item.</span></span>  <br/> |
|[<span data-ttu-id="b979b-117">Body</span><span class="sxs-lookup"><span data-stu-id="b979b-117">Body</span></span>](body.md) <br/> |<span data-ttu-id="b979b-118">Stellt den tatsächlichen Textkörperinhalt einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b979b-118">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="b979b-119">Anlagen</span><span class="sxs-lookup"><span data-stu-id="b979b-119">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="b979b-120">Enthält das Element oder die Datei, die ein Element in der Exchange-Informationsspeicher zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b979b-120">Contains the item or file that is attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b979b-121">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="b979b-121">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="b979b-122">Stellt den Internet Message Headernamen für einen angegebenen Header innerhalb der Kopfzeilen-Auflistung dar.</span><span class="sxs-lookup"><span data-stu-id="b979b-122">Represents the Internet message header name for a given header within the headers collection.</span></span>  <br/> |
|[<span data-ttu-id="b979b-123">Absender</span><span class="sxs-lookup"><span data-stu-id="b979b-123">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="b979b-124">Bezeichnet den Absender eines Elements.</span><span class="sxs-lookup"><span data-stu-id="b979b-124">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="b979b-125">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="b979b-125">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="b979b-126">Enthält eine Reihe von Empfänger eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="b979b-126">Contains a set of recipients of an item.</span></span> <span data-ttu-id="b979b-127">Dies sind die primären Empfänger eines Elements.</span><span class="sxs-lookup"><span data-stu-id="b979b-127">These are the primary recipients of an item.</span></span>  <br/> |
|[<span data-ttu-id="b979b-128">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="b979b-128">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="b979b-129">Stellt eine Auflistung der Empfänger dar, die eine Kopie der Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="b979b-129">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="b979b-130">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="b979b-130">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="b979b-131">Stellt eine Auflistung der Empfänger dar, die eine Blindkopie (Bcc) einer E-Mail erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="b979b-131">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="b979b-132">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="b979b-132">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="b979b-133">Gibt an, ob der Absender eines Elements eine lesebestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="b979b-133">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="b979b-134">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="b979b-134">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="b979b-135">Gibt an, ob der Absender eines Elements eine Empfangsbestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="b979b-135">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="b979b-136">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="b979b-136">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="b979b-137">Identifiziert das Element auf dem im Response-Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="b979b-137">Identifies the item to which the response object refers.</span></span>  <br/> |
|[<span data-ttu-id="b979b-138">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="b979b-138">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="b979b-139">Identifiziert den Delegaten in eine Access Stellvertreter-Szenario.</span><span class="sxs-lookup"><span data-stu-id="b979b-139">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="b979b-140">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b979b-140">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="b979b-141">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="b979b-141">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="b979b-142">Identifiziert den Prinzipal in einer Access Stellvertreter-Szenario.</span><span class="sxs-lookup"><span data-stu-id="b979b-142">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="b979b-143">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b979b-143">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="b979b-144">ProposedStart</span><span class="sxs-lookup"><span data-stu-id="b979b-144">ProposedStart</span></span>](proposedstart.md) <br/> |<span data-ttu-id="b979b-145">Gibt die vorgeschlagenen Anfangszeit der Besprechungsanfrage an.</span><span class="sxs-lookup"><span data-stu-id="b979b-145">Specifies the proposed start time of the meeting request.</span></span>  <br/> |
|[<span data-ttu-id="b979b-146">ProposedEnd</span><span class="sxs-lookup"><span data-stu-id="b979b-146">ProposedEnd</span></span>](proposedend.md) <br/> |<span data-ttu-id="b979b-147">Gibt die vorgeschlagenen Endzeit der Besprechungsanfrage an.</span><span class="sxs-lookup"><span data-stu-id="b979b-147">Specifies the proposed end time of the meeting request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b979b-148">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b979b-148">Parent elements</span></span>

|<span data-ttu-id="b979b-149">**Element**</span><span class="sxs-lookup"><span data-stu-id="b979b-149">**Element**</span></span>|<span data-ttu-id="b979b-150">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b979b-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b979b-151">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="b979b-151">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> | <span data-ttu-id="b979b-152">Werden alle Elemente, die an eine Besprechungszeit angrenzen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b979b-152">Describes all items that are adjacent to a meeting time.</span></span>  <br/> <br/> <span data-ttu-id="b979b-153">Im folgenden sind einige der XPath-Ausdrücke auf dieses Element:</span><span class="sxs-lookup"><span data-stu-id="b979b-153">The following are some of the XPath expressions to this element:</span></span>  <br/><br/>  `/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[<span data-ttu-id="b979b-154">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="b979b-154">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> | <span data-ttu-id="b979b-155">Beschreibt alle Elemente, die mit einem bestimmten Zeitpunkt treffen in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="b979b-155">Describes all items that conflict with a meeting time.</span></span> <br/> <br/>  <span data-ttu-id="b979b-156">Im folgenden sind einige der XPath-Ausdrücke auf dieses Element:</span><span class="sxs-lookup"><span data-stu-id="b979b-156">The following are some of the XPath expressions to this element:</span></span> <br/> <br/>  `/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[<span data-ttu-id="b979b-157">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="b979b-157">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="b979b-158">Enthält eine Auflistung aller Antwort-Objekte, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b979b-158">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b979b-159">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="b979b-159">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="b979b-160">Enthält ein Array von Elementen, die in den Ordner vom [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) -Element zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b979b-160">Contains an array of items to create in the folder identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b979b-161">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b979b-161">Remarks</span></span>

<span data-ttu-id="b979b-162">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="b979b-162">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b979b-163">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b979b-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b979b-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="b979b-164">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b979b-165">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b979b-165">Schema Name</span></span>  <br/> |<span data-ttu-id="b979b-166">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b979b-166">Types schema</span></span>  <br/> |
|<span data-ttu-id="b979b-167">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b979b-167">Validation File</span></span>  <br/> |<span data-ttu-id="b979b-168">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b979b-168">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b979b-169">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b979b-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="b979b-170">False</span><span class="sxs-lookup"><span data-stu-id="b979b-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b979b-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b979b-171">See also</span></span>

- [<span data-ttu-id="b979b-172">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b979b-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

