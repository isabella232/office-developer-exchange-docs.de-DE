---
title: DeclineItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeclineItem
api_type:
- schema
ms.assetid: 2d8d2389-924e-4d03-a324-35d56cf0d6b1
description: Das DeclineItem-Element stellt eine ablehnen Antwort auf eine Besprechungsanfrage.
ms.openlocfilehash: d7076708248bf1ddc0472b802e4de94a436dcde8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757893"
---
# <a name="declineitem"></a><span data-ttu-id="ddc02-103">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="ddc02-103">DeclineItem</span></span>

<span data-ttu-id="ddc02-104">Das **DeclineItem** -Element stellt eine ablehnen Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="ddc02-104">The **DeclineItem** element represents a Decline reply to a meeting request.</span></span> 
  
```xml
<DeclineItem>
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
</DeclineItem>
```

<span data-ttu-id="ddc02-105">**DeclineItemType**</span><span class="sxs-lookup"><span data-stu-id="ddc02-105">**DeclineItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ddc02-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ddc02-106">Attributes and elements</span></span>

<span data-ttu-id="ddc02-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ddc02-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ddc02-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ddc02-108">Attributes</span></span>

<span data-ttu-id="ddc02-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ddc02-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ddc02-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ddc02-110">Child elements</span></span>

|<span data-ttu-id="ddc02-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ddc02-111">**Element**</span></span>|<span data-ttu-id="ddc02-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ddc02-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ddc02-113">ItemClass</span><span class="sxs-lookup"><span data-stu-id="ddc02-113">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="ddc02-114">Die Nachrichtenklasse eines Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="ddc02-114">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="ddc02-115">Vertraulichkeit</span><span class="sxs-lookup"><span data-stu-id="ddc02-115">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="ddc02-116">Gibt die Vertraulichkeitsstufe eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="ddc02-116">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="ddc02-117">Body</span><span class="sxs-lookup"><span data-stu-id="ddc02-117">Body</span></span>](body.md) <br/> |<span data-ttu-id="ddc02-118">Stellt den tatsächlichen Textkörperinhalt einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="ddc02-118">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="ddc02-119">Anlagen</span><span class="sxs-lookup"><span data-stu-id="ddc02-119">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="ddc02-120">Enthält das Element oder die Datei, die ein Element in der Exchange-Informationsspeicher zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ddc02-120">Contains the item or file that is attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ddc02-121">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="ddc02-121">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="ddc02-122">Stellt den Internet Message Headernamen für einen angegebenen Header innerhalb der Kopfzeilen-Auflistung dar.</span><span class="sxs-lookup"><span data-stu-id="ddc02-122">Represents the Internet message header name for a given header within the headers collection.</span></span>  <br/> |
|[<span data-ttu-id="ddc02-123">Absender</span><span class="sxs-lookup"><span data-stu-id="ddc02-123">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="ddc02-124">Bezeichnet den Absender eines Elements.</span><span class="sxs-lookup"><span data-stu-id="ddc02-124">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="ddc02-125">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="ddc02-125">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="ddc02-126">Enthält eine Reihe von Empfänger eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="ddc02-126">Contains a set of recipients of an item.</span></span> <span data-ttu-id="ddc02-127">Dies sind die primären Empfänger eines Elements.</span><span class="sxs-lookup"><span data-stu-id="ddc02-127">These are the primary recipients of an item.</span></span>  <br/> |
|[<span data-ttu-id="ddc02-128">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="ddc02-128">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="ddc02-129">Stellt eine Auflistung der Empfänger dar, die eine Kopie der Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="ddc02-129">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="ddc02-130">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="ddc02-130">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="ddc02-131">Stellt eine Auflistung der Empfänger dar, die eine Blindkopie (Bcc) einer E-Mail erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="ddc02-131">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="ddc02-132">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="ddc02-132">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="ddc02-133">Gibt an, ob der Absender eines Elements eine lesebestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="ddc02-133">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="ddc02-134">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="ddc02-134">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="ddc02-135">Gibt an, ob der Absender eines Elements eine Empfangsbestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="ddc02-135">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="ddc02-136">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="ddc02-136">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="ddc02-137">Identifiziert das Element auf dem im Response-Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="ddc02-137">Identifies the item to which the response object refers.</span></span>  <br/> |
|[<span data-ttu-id="ddc02-138">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="ddc02-138">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="ddc02-139">Identifiziert den Delegaten in eine Access Stellvertreter-Szenario.</span><span class="sxs-lookup"><span data-stu-id="ddc02-139">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="ddc02-140">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ddc02-140">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="ddc02-141">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="ddc02-141">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="ddc02-142">Identifiziert den Prinzipal in einer Access Stellvertreter-Szenario.</span><span class="sxs-lookup"><span data-stu-id="ddc02-142">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="ddc02-143">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ddc02-143">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="ddc02-144">ProposedStart</span><span class="sxs-lookup"><span data-stu-id="ddc02-144">ProposedStart</span></span>](proposedstart.md) <br/> |<span data-ttu-id="ddc02-145">Gibt die vorgeschlagenen Anfangszeit der Besprechung an.</span><span class="sxs-lookup"><span data-stu-id="ddc02-145">Specifies the proposed start time of the meeting.</span></span>  <br/> |
|[<span data-ttu-id="ddc02-146">ProposedEnd</span><span class="sxs-lookup"><span data-stu-id="ddc02-146">ProposedEnd</span></span>](proposedend.md) <br/> |<span data-ttu-id="ddc02-147">Gibt die vorgeschlagenen Endzeit der Besprechung an.</span><span class="sxs-lookup"><span data-stu-id="ddc02-147">Specifies the proposed end time of the meeting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ddc02-148">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ddc02-148">Parent elements</span></span>

|<span data-ttu-id="ddc02-149">**Element**</span><span class="sxs-lookup"><span data-stu-id="ddc02-149">**Element**</span></span>|<span data-ttu-id="ddc02-150">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ddc02-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ddc02-151">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="ddc02-151">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> | <span data-ttu-id="ddc02-152">Werden alle Elemente, die an eine Besprechungszeit angrenzen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ddc02-152">Describes all items that are adjacent to a meeting time.</span></span><br/><br/><span data-ttu-id="ddc02-153">Im folgenden sind einige der XPath-Ausdrücke auf dieses Element:</span><span class="sxs-lookup"><span data-stu-id="ddc02-153">The following are some of the XPath expressions to this element:</span></span><br/><br/>`/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[<span data-ttu-id="ddc02-154">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="ddc02-154">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> | <span data-ttu-id="ddc02-155">Beschreibt alle Elemente, die mit einem bestimmten Zeitpunkt treffen in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="ddc02-155">Describes all items that conflict with a meeting time.</span></span><br/><br/><span data-ttu-id="ddc02-156">Im folgenden sind einige der XPath-Ausdrücke auf dieses Element:</span><span class="sxs-lookup"><span data-stu-id="ddc02-156">The following are some of the XPath expressions to this element:</span></span><br/><br/>`/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[<span data-ttu-id="ddc02-157">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="ddc02-157">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="ddc02-158">Enthält eine Auflistung aller Antwort-Objekte, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ddc02-158">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ddc02-159">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="ddc02-159">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="ddc02-160">Enthält ein Array von Elementen im Ordner zu erstellen, die durch das Element [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="ddc02-160">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ddc02-161">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ddc02-161">Remarks</span></span>

<span data-ttu-id="ddc02-162">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Exchange-Servers, der die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ddc02-162">The schema that describes this element is located in the EWS virtual directory of the Exchange server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ddc02-163">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ddc02-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ddc02-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="ddc02-164">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ddc02-165">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ddc02-165">Schema Name</span></span>  <br/> |<span data-ttu-id="ddc02-166">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ddc02-166">Types schema</span></span>  <br/> |
|<span data-ttu-id="ddc02-167">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ddc02-167">Validation File</span></span>  <br/> |<span data-ttu-id="ddc02-168">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ddc02-168">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ddc02-169">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ddc02-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="ddc02-170">False</span><span class="sxs-lookup"><span data-stu-id="ddc02-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ddc02-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ddc02-171">See also</span></span>

- [<span data-ttu-id="ddc02-172">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ddc02-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

