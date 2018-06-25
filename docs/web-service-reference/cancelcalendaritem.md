---
title: CancelCalendarItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CancelCalendarItem
api_type:
- schema
ms.assetid: a2046402-a176-44d5-b4b3-adb696581935
description: Das CancelCalendarItem-Element darstellt, das Antwortobjekt, das Sie eine Besprechung absagen verwendet wird.
ms.openlocfilehash: 262f60db33abac36156b069dc85e1fccb3522d5b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757548"
---
# <a name="cancelcalendaritem"></a><span data-ttu-id="f6009-103">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="f6009-103">CancelCalendarItem</span></span>

<span data-ttu-id="f6009-104">Das **CancelCalendarItem** -Element darstellt, das Antwortobjekt, das Sie eine Besprechung absagen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f6009-104">The **CancelCalendarItem** element represents the response object that is used to cancel a meeting.</span></span> 
  
```xml
<CancelCalendarItem>
   <Subject/>
   <Body/>
   <ToRecipients/>
   <CcRecipients/>
   <BccRecipients/>
   <IsReadReceiptRequested/>
   <IsDeliveryReceiptRequested/>
   <ReferenceItemId/>
   <NewBodyContent/>
   <ReceivedBy/>
   <ReceivedRepresenting/>
</CancelCalendarItem>
```

 <span data-ttu-id="f6009-105">**CancelCalendarItemType**</span><span class="sxs-lookup"><span data-stu-id="f6009-105">**CancelCalendarItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f6009-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f6009-106">Attributes and elements</span></span>

<span data-ttu-id="f6009-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f6009-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f6009-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f6009-108">Attributes</span></span>

<span data-ttu-id="f6009-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f6009-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f6009-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f6009-110">Child elements</span></span>

|<span data-ttu-id="f6009-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f6009-111">**Element**</span></span>|<span data-ttu-id="f6009-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f6009-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f6009-113">Betreff</span><span class="sxs-lookup"><span data-stu-id="f6009-113">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="f6009-114">Die Subject-Eigenschaft der Exchange-Speicher-Elemente darstellt.</span><span class="sxs-lookup"><span data-stu-id="f6009-114">Represents the subject property of Exchange store items.</span></span>  <br/> |
|[<span data-ttu-id="f6009-115">Body</span><span class="sxs-lookup"><span data-stu-id="f6009-115">Body</span></span>](body.md) <br/> |<span data-ttu-id="f6009-116">Von **CancelCalendarItem**verwendet nicht.</span><span class="sxs-lookup"><span data-stu-id="f6009-116">Not used by **CancelCalendarItem**.</span></span> <span data-ttu-id="f6009-117">Verwenden Sie die [NewBodyContent](newbodycontent.md) -Eigenschaft, um den Textkörperinhalt festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f6009-117">Use the [NewBodyContent](newbodycontent.md) property to set the body content.</span></span>  <br/> |
|[<span data-ttu-id="f6009-118">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="f6009-118">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="f6009-119">Enthält eine Reihe von Empfänger eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="f6009-119">Contains a set of recipients of an item.</span></span> <span data-ttu-id="f6009-120">Dies sind die primären Empfänger eines Elements.</span><span class="sxs-lookup"><span data-stu-id="f6009-120">These are the primary recipients of an item.</span></span>  <br/> |
|[<span data-ttu-id="f6009-121">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="f6009-121">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="f6009-122">Stellt eine Auflistung der Empfänger dar, die eine Kopie der Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="f6009-122">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="f6009-123">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="f6009-123">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="f6009-124">Stellt eine Auflistung der Empfänger dar, die eine Blindkopie (Bcc) einer E-Mail erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="f6009-124">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="f6009-125">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="f6009-125">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="f6009-126">Gibt an, ob der Absender eines Elements eine lesebestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="f6009-126">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="f6009-127">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="f6009-127">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="f6009-128">Gibt an, ob der Absender eines Elements eine Empfangsbestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="f6009-128">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="f6009-129">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="f6009-129">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="f6009-130">Identifiziert das Element auf dem im Response-Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="f6009-130">Identifies the item to which the response object refers.</span></span>  <br/> |
|[<span data-ttu-id="f6009-131">NewBodyContent</span><span class="sxs-lookup"><span data-stu-id="f6009-131">NewBodyContent</span></span>](newbodycontent.md) <br/> |<span data-ttu-id="f6009-132">Stellt den neuen Textkörperinhalt einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="f6009-132">Represents the new body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="f6009-133">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="f6009-133">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="f6009-134">Identifiziert den Delegaten in eine Access Stellvertreter-Szenario.</span><span class="sxs-lookup"><span data-stu-id="f6009-134">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="f6009-135">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f6009-135">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="f6009-136">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="f6009-136">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="f6009-137">Identifiziert den Prinzipal in einer Access Stellvertreter-Szenario.</span><span class="sxs-lookup"><span data-stu-id="f6009-137">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="f6009-138">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f6009-138">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f6009-139">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f6009-139">Parent elements</span></span>

|<span data-ttu-id="f6009-140">**Element**</span><span class="sxs-lookup"><span data-stu-id="f6009-140">**Element**</span></span>|<span data-ttu-id="f6009-141">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f6009-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f6009-142">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="f6009-142">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> | <span data-ttu-id="f6009-143">Werden alle Elemente, die an eine Besprechungszeit angrenzen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f6009-143">Describes all items that are adjacent to a meeting time.</span></span><br/><br/> <span data-ttu-id="f6009-144">Im folgenden sind einige der XPath-Ausdrücke auf dieses Element:</span><span class="sxs-lookup"><span data-stu-id="f6009-144">The following are some of the XPath expressions to this element:</span></span><br/><br/>`/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[<span data-ttu-id="f6009-145">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="f6009-145">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> | <span data-ttu-id="f6009-146">Beschreibt alle Elemente, die mit einem bestimmten Zeitpunkt treffen in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="f6009-146">Describes all items that conflict with a meeting time.</span></span><br/><br/><span data-ttu-id="f6009-147">Im folgenden sind einige der XPath-Ausdrücke auf dieses Element:</span><span class="sxs-lookup"><span data-stu-id="f6009-147">The following are some of the XPath expressions to this element:</span></span><br/><br/>`/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[<span data-ttu-id="f6009-148">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="f6009-148">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="f6009-149">Enthält eine Auflistung aller Antwort-Objekte, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f6009-149">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f6009-150">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="f6009-150">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="f6009-151">Enthält ein Array von Elementen, die in den Ordner vom [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) -Element zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f6009-151">Contains an array of items to create in the folder identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6009-152">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f6009-152">Remarks</span></span>

<span data-ttu-id="f6009-153">Das **CancelCalendarItem** -Element wird nur von der Organisator angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f6009-153">The **CancelCalendarItem** element is only viewed by the organizer.</span></span> <span data-ttu-id="f6009-154">Dies gilt nur für Kalenderelement des Organisierer vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f6009-154">It only applies to the organizer's calendar item.</span></span> 
  
<span data-ttu-id="f6009-155">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="f6009-155">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f6009-156">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f6009-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f6009-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="f6009-157">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f6009-158">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f6009-158">Schema Name</span></span>  <br/> |<span data-ttu-id="f6009-159">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f6009-159">Types schema</span></span>  <br/> |
|<span data-ttu-id="f6009-160">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f6009-160">Validation File</span></span>  <br/> |<span data-ttu-id="f6009-161">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f6009-161">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f6009-162">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f6009-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="f6009-163">False</span><span class="sxs-lookup"><span data-stu-id="f6009-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f6009-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6009-164">See also</span></span>

- [<span data-ttu-id="f6009-165">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f6009-165">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

