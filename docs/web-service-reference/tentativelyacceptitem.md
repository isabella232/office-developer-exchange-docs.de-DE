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
description: Das TentativelyAcceptItem-Element stellt eine vorläufige Antwort auf eine Besprechungsanfrage dar.
ms.openlocfilehash: 6d20ec2964c41dcbb786b1209b4597999e025609
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459497"
---
# <a name="tentativelyacceptitem"></a><span data-ttu-id="751b1-103">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="751b1-103">TentativelyAcceptItem</span></span>

<span data-ttu-id="751b1-104">Das **TentativelyAcceptItem** -Element stellt eine vorläufige Antwort auf eine Besprechungsanfrage dar.</span><span class="sxs-lookup"><span data-stu-id="751b1-104">The **TentativelyAcceptItem** element represents a Tentative reply to a meeting request.</span></span> 
  
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

 <span data-ttu-id="751b1-105">**TentativelyAcceptItemType**</span><span class="sxs-lookup"><span data-stu-id="751b1-105">**TentativelyAcceptItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="751b1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="751b1-106">Attributes and elements</span></span>

<span data-ttu-id="751b1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="751b1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="751b1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="751b1-108">Attributes</span></span>

<span data-ttu-id="751b1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="751b1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="751b1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="751b1-110">Child elements</span></span>

|<span data-ttu-id="751b1-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="751b1-111">**Element**</span></span>|<span data-ttu-id="751b1-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="751b1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="751b1-113">ItemClass</span><span class="sxs-lookup"><span data-stu-id="751b1-113">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="751b1-114">Stellt die Nachrichtenklasse eines Elements dar.</span><span class="sxs-lookup"><span data-stu-id="751b1-114">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="751b1-115">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="751b1-115">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="751b1-116">Gibt die Empfindlichkeit eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="751b1-116">Identifies the sensitivity of an item.</span></span>  <br/> |
|[<span data-ttu-id="751b1-117">Body</span><span class="sxs-lookup"><span data-stu-id="751b1-117">Body</span></span>](body.md) <br/> |<span data-ttu-id="751b1-118">Stellt den tatsächlichen Textinhalt einer Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="751b1-118">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="751b1-119">Anlagen</span><span class="sxs-lookup"><span data-stu-id="751b1-119">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="751b1-120">Enthält das Element oder die Datei, das an ein Element in der Exchange-Informationsspeicher angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="751b1-120">Contains the item or file that is attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="751b1-121">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="751b1-121">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="751b1-122">Stellt den Namen des Internet Nachrichtenkopfs für eine bestimmte Kopfzeile in der Headers-Auflistung dar.</span><span class="sxs-lookup"><span data-stu-id="751b1-122">Represents the Internet message header name for a given header within the headers collection.</span></span>  <br/> |
|[<span data-ttu-id="751b1-123">Absender</span><span class="sxs-lookup"><span data-stu-id="751b1-123">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="751b1-124">Bezeichnet den Absender eines Elements.</span><span class="sxs-lookup"><span data-stu-id="751b1-124">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="751b1-125">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="751b1-125">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="751b1-126">Enthält eine Gruppe von Empfängern eines Elements.</span><span class="sxs-lookup"><span data-stu-id="751b1-126">Contains a set of recipients of an item.</span></span> <span data-ttu-id="751b1-127">Dies sind die primären Empfänger eines Elements.</span><span class="sxs-lookup"><span data-stu-id="751b1-127">These are the primary recipients of an item.</span></span>  <br/> |
|[<span data-ttu-id="751b1-128">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="751b1-128">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="751b1-129">Stellt eine Auflistung der Empfänger dar, die eine Kopie der Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="751b1-129">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="751b1-130">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="751b1-130">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="751b1-131">Stellt eine Auflistung der Empfänger dar, die eine Blindkopie (Bcc) einer E-Mail erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="751b1-131">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="751b1-132">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="751b1-132">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="751b1-133">Gibt an, ob der Absender eines Elements eine Lesebestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="751b1-133">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="751b1-134">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="751b1-134">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="751b1-135">Gibt an, ob der Absender eines Elements eine Zustellungsbestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="751b1-135">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="751b1-136">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="751b1-136">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="751b1-137">Gibt das Element an, auf das das Response-Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="751b1-137">Identifies the item to which the response object refers.</span></span>  <br/> |
|[<span data-ttu-id="751b1-138">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="751b1-138">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="751b1-139">Identifiziert die Stellvertretung in einem Stellvertretungs-Zugriffs Szenario.</span><span class="sxs-lookup"><span data-stu-id="751b1-139">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="751b1-140">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="751b1-140">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="751b1-141">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="751b1-141">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="751b1-142">Identifiziert den Prinzipal in einem Stellvertretungs-Zugriffs Szenario.</span><span class="sxs-lookup"><span data-stu-id="751b1-142">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="751b1-143">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="751b1-143">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="751b1-144">ProposedStart</span><span class="sxs-lookup"><span data-stu-id="751b1-144">ProposedStart</span></span>](proposedstart.md) <br/> |<span data-ttu-id="751b1-145">Gibt die vorgeschlagene Startzeit der Besprechungsanfrage an.</span><span class="sxs-lookup"><span data-stu-id="751b1-145">Specifies the proposed start time of the meeting request.</span></span>  <br/> |
|[<span data-ttu-id="751b1-146">ProposedEnd</span><span class="sxs-lookup"><span data-stu-id="751b1-146">ProposedEnd</span></span>](proposedend.md) <br/> |<span data-ttu-id="751b1-147">Gibt die vorgeschlagene Endzeit der Besprechungsanfrage an.</span><span class="sxs-lookup"><span data-stu-id="751b1-147">Specifies the proposed end time of the meeting request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="751b1-148">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="751b1-148">Parent elements</span></span>

|<span data-ttu-id="751b1-149">**Element**</span><span class="sxs-lookup"><span data-stu-id="751b1-149">**Element**</span></span>|<span data-ttu-id="751b1-150">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="751b1-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="751b1-151">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="751b1-151">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> | <span data-ttu-id="751b1-152">Beschreibt alle Elemente, die an eine Besprechungszeit angrenzen.</span><span class="sxs-lookup"><span data-stu-id="751b1-152">Describes all items that are adjacent to a meeting time.</span></span>  <br/> <br/> <span data-ttu-id="751b1-153">Im folgenden finden Sie einige der XPath-Ausdrücke für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="751b1-153">The following are some of the XPath expressions to this element:</span></span>  <br/><br/>  `/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[<span data-ttu-id="751b1-154">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="751b1-154">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> | <span data-ttu-id="751b1-155">Beschreibt alle Elemente, die mit einer Besprechungszeit in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="751b1-155">Describes all items that conflict with a meeting time.</span></span> <br/> <br/>  <span data-ttu-id="751b1-156">Im folgenden finden Sie einige der XPath-Ausdrücke für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="751b1-156">The following are some of the XPath expressions to this element:</span></span> <br/> <br/>  `/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[<span data-ttu-id="751b1-157">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="751b1-157">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="751b1-158">Enthält eine Auflistung aller Response-Objekte, die einem Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="751b1-158">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="751b1-159">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="751b1-159">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="751b1-160">Enthält ein Array von Elementen, die in dem durch das [parentfolderid (TargetFolderIdType)-](parentfolderid-targetfolderidtype.md) Element identifizierten Ordner erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="751b1-160">Contains an array of items to create in the folder identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="751b1-161">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="751b1-161">Remarks</span></span>

<span data-ttu-id="751b1-162">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="751b1-162">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="751b1-163">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="751b1-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="751b1-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="751b1-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="751b1-165">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="751b1-165">Schema Name</span></span>  <br/> |<span data-ttu-id="751b1-166">Schematypen</span><span class="sxs-lookup"><span data-stu-id="751b1-166">Types schema</span></span>  <br/> |
|<span data-ttu-id="751b1-167">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="751b1-167">Validation File</span></span>  <br/> |<span data-ttu-id="751b1-168">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="751b1-168">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="751b1-169">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="751b1-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="751b1-170">False</span><span class="sxs-lookup"><span data-stu-id="751b1-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="751b1-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="751b1-171">See also</span></span>

- [<span data-ttu-id="751b1-172">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="751b1-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

