---
title: ReplyToItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReplyToItem
api_type:
- schema
ms.assetid: 35ee751a-41c0-4216-ad8b-78f7ada43a2f
description: Das ReplyToItem-Element enthält eine Antwort an den Absender eines Elements in der Exchange-Informationsspeicher.
ms.openlocfilehash: fc40335dc73327820c0b39cafa07168d1f27851d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529854"
---
# <a name="replytoitem"></a><span data-ttu-id="3fda0-103">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="3fda0-103">ReplyToItem</span></span>

<span data-ttu-id="3fda0-104">Das **ReplyToItem** -Element enthält eine Antwort an den Absender eines Elements in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="3fda0-104">The **ReplyToItem** element contains a reply to the sender of an item in the Exchange store.</span></span> 
  
```xml
<ReplyToItem>
   <Subject/>
   <Body/>
   <ToRecipients/>
   <CcRecipients/>
   <BccRecipients/>
   <IsReadReceiptRequested/>
   <IsDeliveryReceiptRequested/>
   <From/>
   <ReferenceItemId/>
   <NewBodyContent/>
   <ReceivedBy/>
   <ReceivedRepresenting/>
</ReplyToItem>
```

<span data-ttu-id="3fda0-105">**ReplyToItemType**</span><span class="sxs-lookup"><span data-stu-id="3fda0-105">**ReplyToItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="3fda0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3fda0-106">Attributes and elements</span></span>

<span data-ttu-id="3fda0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3fda0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3fda0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3fda0-108">Attributes</span></span>

<span data-ttu-id="3fda0-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3fda0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3fda0-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3fda0-110">Child elements</span></span>

|<span data-ttu-id="3fda0-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3fda0-111">**Element**</span></span>|<span data-ttu-id="3fda0-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3fda0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3fda0-113">Betreff</span><span class="sxs-lookup"><span data-stu-id="3fda0-113">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="3fda0-114">Stellt die Subject-Eigenschaft Exchange-Informationsspeicher Elemente dar.</span><span class="sxs-lookup"><span data-stu-id="3fda0-114">Represents the subject property of Exchange store items.</span></span>  <br/> |
|[<span data-ttu-id="3fda0-115">Body</span><span class="sxs-lookup"><span data-stu-id="3fda0-115">Body</span></span>](body.md) <br/> |<span data-ttu-id="3fda0-116">Stellt den tatsächlichen Textinhalt einer Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="3fda0-116">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="3fda0-117">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="3fda0-117">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="3fda0-118">Enthält eine Reihe von Benutzern eines Elements.</span><span class="sxs-lookup"><span data-stu-id="3fda0-118">Contains an array of recipients of an item.</span></span> <span data-ttu-id="3fda0-119">Dies sind die primären Empfänger eines Elements.</span><span class="sxs-lookup"><span data-stu-id="3fda0-119">These are the primary recipients of an item.</span></span>  <br/> |
|[<span data-ttu-id="3fda0-120">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="3fda0-120">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="3fda0-121">Stellt eine Auflistung der Empfänger dar, die eine Kopie der Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="3fda0-121">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="3fda0-122">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="3fda0-122">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="3fda0-123">Stellt eine Auflistung von Empfängern dar, die eine Blindkopie (BCC) einer e-Mail-Nachricht erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="3fda0-123">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="3fda0-124">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="3fda0-124">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="3fda0-125">Gibt an, ob der Absender eines Elements eine Lesebestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="3fda0-125">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="3fda0-126">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="3fda0-126">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="3fda0-127">Gibt an, ob der Absender eines Elements eine Zustellungsbestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="3fda0-127">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="3fda0-128">From</span><span class="sxs-lookup"><span data-stu-id="3fda0-128">From</span></span>](from.md) <br/> |<span data-ttu-id="3fda0-129">Stellt die Adresse dar, von der die Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="3fda0-129">Represents the address from which the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="3fda0-130">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="3fda0-130">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="3fda0-131">Gibt das Element an, auf das das Response-Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="3fda0-131">Identifies the item to which the response object refers.</span></span>  <br/> |
|[<span data-ttu-id="3fda0-132">NewBodyContent</span><span class="sxs-lookup"><span data-stu-id="3fda0-132">NewBodyContent</span></span>](newbodycontent.md) <br/> |<span data-ttu-id="3fda0-133">Stellt den neuen Textkörper Inhalt einer Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="3fda0-133">Represents the new body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="3fda0-134">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="3fda0-134">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="3fda0-135">Identifiziert die Stellvertretung in einem Stellvertretungs-Zugriffs Szenario.</span><span class="sxs-lookup"><span data-stu-id="3fda0-135">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="3fda0-136">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3fda0-136">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="3fda0-137">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="3fda0-137">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="3fda0-138">Identifiziert den Prinzipal in einem Stellvertretungs-Zugriffs Szenario.</span><span class="sxs-lookup"><span data-stu-id="3fda0-138">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="3fda0-139">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3fda0-139">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3fda0-140">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3fda0-140">Parent elements</span></span>

|<span data-ttu-id="3fda0-141">**Element**</span><span class="sxs-lookup"><span data-stu-id="3fda0-141">**Element**</span></span>|<span data-ttu-id="3fda0-142">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3fda0-142">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3fda0-143">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="3fda0-143">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> | <span data-ttu-id="3fda0-144">Beschreibt alle Elemente, die an eine Besprechungszeit angrenzen.</span><span class="sxs-lookup"><span data-stu-id="3fda0-144">Describes all items that are adjacent to a meeting time.</span></span> <br/> <br/>  <span data-ttu-id="3fda0-145">Im folgenden finden Sie einige der XPath-Ausdrücke für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="3fda0-145">The following are some of the XPath expressions to this element:</span></span> <br/> <br/>  `/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[<span data-ttu-id="3fda0-146">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="3fda0-146">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> | <span data-ttu-id="3fda0-147">Beschreibt alle Elemente, die mit einer Besprechungszeit in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="3fda0-147">Describes all items that conflict with a meeting time.</span></span> <br/> <br/>  <span data-ttu-id="3fda0-148">Im folgenden finden Sie einige der XPath-Ausdrücke für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="3fda0-148">The following are some of the XPath expressions to this element:</span></span> <br/> <br/>  `/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[<span data-ttu-id="3fda0-149">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="3fda0-149">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="3fda0-150">Enthält eine Auflistung aller Response-Objekte, die einem Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3fda0-150">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3fda0-151">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="3fda0-151">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="3fda0-152">Enthält ein Array von Elementen, die in dem Ordner erstellt werden sollen, der durch das [parentfolderid (TargetFolderIdType)-](parentfolderid-targetfolderidtype.md) Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="3fda0-152">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3fda0-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3fda0-153">Remarks</span></span>

<span data-ttu-id="3fda0-154">Das [from](from.md) -Element sollte auf die e-Mail-Adresse des Prinzipals festgelegt werden, wenn es sich bei einem Element um eine Antwort von einer Stellvertretung handelt.</span><span class="sxs-lookup"><span data-stu-id="3fda0-154">The [From](from.md) element should be set to the e-mail address of the principal if an item is a reply by a delegate.</span></span> <span data-ttu-id="3fda0-155">Wenn die Stellvertretung die [from](from.md) -Eigenschaft nicht festgelegt hat, wird das Element scheinbar direkt aus dem Postfach des Stellvertreters gesendet.</span><span class="sxs-lookup"><span data-stu-id="3fda0-155">If the delegate does not set the [From](from.md) property, the item will appear to have been sent directly from the delegate's mailbox.</span></span> 
  
<span data-ttu-id="3fda0-156">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="3fda0-156">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3fda0-157">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3fda0-157">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3fda0-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="3fda0-158">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3fda0-159">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3fda0-159">Schema Name</span></span>  <br/> |<span data-ttu-id="3fda0-160">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3fda0-160">Types schema</span></span>  <br/> |
|<span data-ttu-id="3fda0-161">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3fda0-161">Validation File</span></span>  <br/> |<span data-ttu-id="3fda0-162">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3fda0-162">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3fda0-163">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3fda0-163">Can be Empty</span></span>  <br/> |<span data-ttu-id="3fda0-164">False</span><span class="sxs-lookup"><span data-stu-id="3fda0-164">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3fda0-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3fda0-165">See also</span></span>

- [<span data-ttu-id="3fda0-166">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3fda0-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

