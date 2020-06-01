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
description: Das DeclineItem-Element stellt eine Ablehnungs Antwort auf eine Besprechungsanfrage dar.
ms.openlocfilehash: a3fb2b62ea2fa895a664034d2150f46a3099f6c1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457431"
---
# <a name="declineitem"></a><span data-ttu-id="b42ea-103">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="b42ea-103">DeclineItem</span></span>

<span data-ttu-id="b42ea-104">Das **DeclineItem** -Element stellt eine Ablehnungs Antwort auf eine Besprechungsanfrage dar.</span><span class="sxs-lookup"><span data-stu-id="b42ea-104">The **DeclineItem** element represents a Decline reply to a meeting request.</span></span> 
  
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

<span data-ttu-id="b42ea-105">**DeclineItemType**</span><span class="sxs-lookup"><span data-stu-id="b42ea-105">**DeclineItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="b42ea-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b42ea-106">Attributes and elements</span></span>

<span data-ttu-id="b42ea-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b42ea-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b42ea-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b42ea-108">Attributes</span></span>

<span data-ttu-id="b42ea-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b42ea-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b42ea-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b42ea-110">Child elements</span></span>

|<span data-ttu-id="b42ea-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b42ea-111">**Element**</span></span>|<span data-ttu-id="b42ea-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b42ea-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b42ea-113">ItemClass</span><span class="sxs-lookup"><span data-stu-id="b42ea-113">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="b42ea-114">Stellt die Nachrichtenklasse eines Elements dar.</span><span class="sxs-lookup"><span data-stu-id="b42ea-114">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="b42ea-115">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="b42ea-115">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="b42ea-116">Gibt die Empfindlichkeitsstufe eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="b42ea-116">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="b42ea-117">Body</span><span class="sxs-lookup"><span data-stu-id="b42ea-117">Body</span></span>](body.md) <br/> |<span data-ttu-id="b42ea-118">Stellt den tatsächlichen Textinhalt einer Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="b42ea-118">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="b42ea-119">Anlagen</span><span class="sxs-lookup"><span data-stu-id="b42ea-119">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="b42ea-120">Enthält das Element oder die Datei, das an ein Element in der Exchange-Informationsspeicher angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="b42ea-120">Contains the item or file that is attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b42ea-121">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="b42ea-121">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="b42ea-122">Stellt den Namen des Internet Nachrichtenkopfs für eine bestimmte Kopfzeile in der Headers-Auflistung dar.</span><span class="sxs-lookup"><span data-stu-id="b42ea-122">Represents the Internet message header name for a given header within the headers collection.</span></span>  <br/> |
|[<span data-ttu-id="b42ea-123">Absender</span><span class="sxs-lookup"><span data-stu-id="b42ea-123">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="b42ea-124">Bezeichnet den Absender eines Elements.</span><span class="sxs-lookup"><span data-stu-id="b42ea-124">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="b42ea-125">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="b42ea-125">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="b42ea-126">Enthält eine Gruppe von Empfängern eines Elements.</span><span class="sxs-lookup"><span data-stu-id="b42ea-126">Contains a set of recipients of an item.</span></span> <span data-ttu-id="b42ea-127">Dies sind die primären Empfänger eines Elements.</span><span class="sxs-lookup"><span data-stu-id="b42ea-127">These are the primary recipients of an item.</span></span>  <br/> |
|[<span data-ttu-id="b42ea-128">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="b42ea-128">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="b42ea-129">Stellt eine Auflistung der Empfänger dar, die eine Kopie der Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="b42ea-129">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="b42ea-130">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="b42ea-130">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="b42ea-131">Stellt eine Auflistung der Empfänger dar, die eine Blindkopie (Bcc) einer E-Mail erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="b42ea-131">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="b42ea-132">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="b42ea-132">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="b42ea-133">Gibt an, ob der Absender eines Elements eine Lesebestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="b42ea-133">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="b42ea-134">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="b42ea-134">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="b42ea-135">Gibt an, ob der Absender eines Elements eine Zustellungsbestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="b42ea-135">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="b42ea-136">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="b42ea-136">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="b42ea-137">Gibt das Element an, auf das das Response-Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="b42ea-137">Identifies the item to which the response object refers.</span></span>  <br/> |
|[<span data-ttu-id="b42ea-138">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="b42ea-138">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="b42ea-139">Identifiziert die Stellvertretung in einem Stellvertretungs-Zugriffs Szenario.</span><span class="sxs-lookup"><span data-stu-id="b42ea-139">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="b42ea-140">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b42ea-140">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="b42ea-141">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="b42ea-141">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="b42ea-142">Identifiziert den Prinzipal in einem Stellvertretungs-Zugriffs Szenario.</span><span class="sxs-lookup"><span data-stu-id="b42ea-142">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="b42ea-143">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b42ea-143">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="b42ea-144">ProposedStart</span><span class="sxs-lookup"><span data-stu-id="b42ea-144">ProposedStart</span></span>](proposedstart.md) <br/> |<span data-ttu-id="b42ea-145">Gibt die vorgeschlagene Anfangszeit der Besprechung an.</span><span class="sxs-lookup"><span data-stu-id="b42ea-145">Specifies the proposed start time of the meeting.</span></span>  <br/> |
|[<span data-ttu-id="b42ea-146">ProposedEnd</span><span class="sxs-lookup"><span data-stu-id="b42ea-146">ProposedEnd</span></span>](proposedend.md) <br/> |<span data-ttu-id="b42ea-147">Gibt die vorgeschlagene Endzeit der Besprechung an.</span><span class="sxs-lookup"><span data-stu-id="b42ea-147">Specifies the proposed end time of the meeting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b42ea-148">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b42ea-148">Parent elements</span></span>

|<span data-ttu-id="b42ea-149">**Element**</span><span class="sxs-lookup"><span data-stu-id="b42ea-149">**Element**</span></span>|<span data-ttu-id="b42ea-150">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b42ea-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b42ea-151">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="b42ea-151">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> | <span data-ttu-id="b42ea-152">Beschreibt alle Elemente, die an eine Besprechungszeit angrenzen.</span><span class="sxs-lookup"><span data-stu-id="b42ea-152">Describes all items that are adjacent to a meeting time.</span></span><br/><br/><span data-ttu-id="b42ea-153">Im folgenden finden Sie einige der XPath-Ausdrücke für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="b42ea-153">The following are some of the XPath expressions to this element:</span></span><br/><br/>`/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[<span data-ttu-id="b42ea-154">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="b42ea-154">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> | <span data-ttu-id="b42ea-155">Beschreibt alle Elemente, die mit einer Besprechungszeit in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="b42ea-155">Describes all items that conflict with a meeting time.</span></span><br/><br/><span data-ttu-id="b42ea-156">Im folgenden finden Sie einige der XPath-Ausdrücke für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="b42ea-156">The following are some of the XPath expressions to this element:</span></span><br/><br/>`/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[<span data-ttu-id="b42ea-157">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="b42ea-157">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="b42ea-158">Enthält eine Auflistung aller Response-Objekte, die einem Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b42ea-158">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b42ea-159">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="b42ea-159">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="b42ea-160">Enthält ein Array von Elementen, die in dem Ordner erstellt werden sollen, der durch das [parentfolderid (TargetFolderIdType)-](parentfolderid-targetfolderidtype.md) Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="b42ea-160">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b42ea-161">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b42ea-161">Remarks</span></span>

<span data-ttu-id="b42ea-162">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Exchange-Servers, auf dem die Client Zugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b42ea-162">The schema that describes this element is located in the EWS virtual directory of the Exchange server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b42ea-163">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b42ea-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b42ea-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="b42ea-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b42ea-165">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b42ea-165">Schema Name</span></span>  <br/> |<span data-ttu-id="b42ea-166">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b42ea-166">Types schema</span></span>  <br/> |
|<span data-ttu-id="b42ea-167">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b42ea-167">Validation File</span></span>  <br/> |<span data-ttu-id="b42ea-168">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b42ea-168">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b42ea-169">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b42ea-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="b42ea-170">False</span><span class="sxs-lookup"><span data-stu-id="b42ea-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b42ea-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b42ea-171">See also</span></span>

- [<span data-ttu-id="b42ea-172">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b42ea-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

