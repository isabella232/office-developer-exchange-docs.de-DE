---
title: AcceptItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AcceptItem
api_type:
- schema
ms.assetid: 05a15431-77e1-411a-a16b-5481d364d3cc
description: Das AcceptItem-Element stellt eine Annahme Antwort auf eine Besprechungsanfrage dar.
ms.openlocfilehash: 6f2197e9df8a095aec545e1a09a761f7e8e432d3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461716"
---
# <a name="acceptitem"></a><span data-ttu-id="e83d1-103">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="e83d1-103">AcceptItem</span></span>

<span data-ttu-id="e83d1-104">Das **AcceptItem** -Element stellt eine Annahme Antwort auf eine Besprechungsanfrage dar.</span><span class="sxs-lookup"><span data-stu-id="e83d1-104">The **AcceptItem** element represents an Accept reply to a meeting request.</span></span> 
  
```xml
<AcceptItem>
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
</AcceptItem>
```

 <span data-ttu-id="e83d1-105">**AcceptItemType**</span><span class="sxs-lookup"><span data-stu-id="e83d1-105">**AcceptItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e83d1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e83d1-106">Attributes and elements</span></span>

<span data-ttu-id="e83d1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e83d1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e83d1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e83d1-108">Attributes</span></span>

<span data-ttu-id="e83d1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e83d1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e83d1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e83d1-110">Child elements</span></span>

|<span data-ttu-id="e83d1-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e83d1-111">**Element**</span></span>|<span data-ttu-id="e83d1-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e83d1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e83d1-113">ItemClass</span><span class="sxs-lookup"><span data-stu-id="e83d1-113">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="e83d1-114">Stellt die Nachrichtenklasse eines Elements dar.</span><span class="sxs-lookup"><span data-stu-id="e83d1-114">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="e83d1-115">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="e83d1-115">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="e83d1-116">Gibt die Empfindlichkeitsstufe eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="e83d1-116">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="e83d1-117">Body</span><span class="sxs-lookup"><span data-stu-id="e83d1-117">Body</span></span>](body.md) <br/> |<span data-ttu-id="e83d1-118">Stellt den tatsächlichen Textinhalt einer Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="e83d1-118">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="e83d1-119">Anlagen</span><span class="sxs-lookup"><span data-stu-id="e83d1-119">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="e83d1-120">Enthält das Element oder die Datei, das an ein Element in der Exchange-Informationsspeicher angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="e83d1-120">Contains the item or file that is attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e83d1-121">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="e83d1-121">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="e83d1-122">Stellt den Namen des Internet Nachrichtenkopfs für eine bestimmte Kopfzeile in der Headers-Auflistung dar.</span><span class="sxs-lookup"><span data-stu-id="e83d1-122">Represents the Internet message header name for a given header within the headers collection.</span></span>  <br/> |
|[<span data-ttu-id="e83d1-123">Absender</span><span class="sxs-lookup"><span data-stu-id="e83d1-123">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="e83d1-124">Bezeichnet den Absender eines Elements.</span><span class="sxs-lookup"><span data-stu-id="e83d1-124">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="e83d1-125">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="e83d1-125">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="e83d1-126">Enthält eine Gruppe von Empfängern eines Elements.</span><span class="sxs-lookup"><span data-stu-id="e83d1-126">Contains a set of recipients of an item.</span></span> <span data-ttu-id="e83d1-127">Dies sind die primären Empfänger eines Elements.</span><span class="sxs-lookup"><span data-stu-id="e83d1-127">These are the primary recipients of an item.</span></span>  <br/> |
|[<span data-ttu-id="e83d1-128">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="e83d1-128">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="e83d1-129">Stellt eine Auflistung der Empfänger dar, die eine Kopie der Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="e83d1-129">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="e83d1-130">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="e83d1-130">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="e83d1-131">Stellt eine Auflistung der Empfänger dar, die eine Blindkopie (Bcc) einer E-Mail erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="e83d1-131">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="e83d1-132">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="e83d1-132">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="e83d1-133">Gibt an, ob der Absender eines Elements eine Lesebestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="e83d1-133">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="e83d1-134">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="e83d1-134">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="e83d1-135">Gibt an, ob der Absender eines Elements eine Zustellungsbestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="e83d1-135">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="e83d1-136">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="e83d1-136">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="e83d1-137">Gibt das Element an, auf das das Response-Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="e83d1-137">Identifies the item to which the response object refers.</span></span>  <br/> |
|[<span data-ttu-id="e83d1-138">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="e83d1-138">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="e83d1-139">Identifiziert die Stellvertretung in einem Stellvertretungs-Zugriffs Szenario.</span><span class="sxs-lookup"><span data-stu-id="e83d1-139">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="e83d1-140">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e83d1-140">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="e83d1-141">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="e83d1-141">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="e83d1-142">Identifiziert den Prinzipal in einem Stellvertretungs-Zugriffs Szenario.</span><span class="sxs-lookup"><span data-stu-id="e83d1-142">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="e83d1-143">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e83d1-143">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="e83d1-144">ProposedStart</span><span class="sxs-lookup"><span data-stu-id="e83d1-144">ProposedStart</span></span>](proposedstart.md) <br/> |<span data-ttu-id="e83d1-145">Gibt die vorgeschlagene Anfangszeit der Besprechung an.</span><span class="sxs-lookup"><span data-stu-id="e83d1-145">Specifies the proposed start time of the meeting.</span></span>  <br/> |
|[<span data-ttu-id="e83d1-146">ProposedEnd</span><span class="sxs-lookup"><span data-stu-id="e83d1-146">ProposedEnd</span></span>](proposedend.md) <br/> |<span data-ttu-id="e83d1-147">Gibt die vorgeschlagene Endzeit der Besprechung an.</span><span class="sxs-lookup"><span data-stu-id="e83d1-147">Specifies the proposed end time of the meeting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e83d1-148">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e83d1-148">Parent elements</span></span>

|<span data-ttu-id="e83d1-149">**Element**</span><span class="sxs-lookup"><span data-stu-id="e83d1-149">**Element**</span></span>|<span data-ttu-id="e83d1-150">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e83d1-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e83d1-151">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="e83d1-151">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> | <span data-ttu-id="e83d1-152">Beschreibt alle Elemente, die an eine Besprechungszeit angrenzen.</span><span class="sxs-lookup"><span data-stu-id="e83d1-152">Describes all items that are adjacent to a meeting time.</span></span><br/><br/>  <span data-ttu-id="e83d1-153">Im folgenden finden Sie einige der XPath-Ausdrücke für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="e83d1-153">The following are some of the XPath expressions to this element:</span></span><br/><br/>  `/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[<span data-ttu-id="e83d1-154">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="e83d1-154">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> | <span data-ttu-id="e83d1-155">Beschreibt alle Elemente, die mit einer Besprechungszeit in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="e83d1-155">Describes all items that conflict with a meeting time.</span></span><br/><br/>  <span data-ttu-id="e83d1-156">Im folgenden finden Sie einige der XPath-Ausdrücke für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="e83d1-156">The following are some of the XPath expressions to this element:</span></span><br/><br/>  `/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[<span data-ttu-id="e83d1-157">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="e83d1-157">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="e83d1-158">Enthält eine Auflistung aller Response-Objekte, die einem Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e83d1-158">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e83d1-159">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="e83d1-159">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="e83d1-160">Enthält ein Array von Elementen, die in dem durch das [parentfolderid (TargetFolderIdType)-](parentfolderid-targetfolderidtype.md) Element identifizierten Ordner erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e83d1-160">Contains an array of items to create in the folder identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e83d1-161">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e83d1-161">Remarks</span></span>

<span data-ttu-id="e83d1-162">Das Schema, das dieses Element beschreibt, befindet sich im EWS-Verzeichnis des Exchange-Servers, auf dem die Client Zugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="e83d1-162">The schema that describes this element is located in the EWS directory of the Exchange server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e83d1-163">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e83d1-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e83d1-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="e83d1-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e83d1-165">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e83d1-165">Schema Name</span></span>  <br/> |<span data-ttu-id="e83d1-166">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e83d1-166">Types schema</span></span>  <br/> |
|<span data-ttu-id="e83d1-167">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e83d1-167">Validation File</span></span>  <br/> |<span data-ttu-id="e83d1-168">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e83d1-168">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e83d1-169">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e83d1-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="e83d1-170">False</span><span class="sxs-lookup"><span data-stu-id="e83d1-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e83d1-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e83d1-171">See also</span></span>

- [<span data-ttu-id="e83d1-172">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e83d1-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

