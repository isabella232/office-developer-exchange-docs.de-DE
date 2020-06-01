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
description: Das CancelCalendarItem-Element stellt das Response-Objekt dar, das zum Abbrechen einer Besprechung verwendet wird.
ms.openlocfilehash: 45ad76d19bd43e2081aa9b9eb63547e091014803
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462255"
---
# <a name="cancelcalendaritem"></a><span data-ttu-id="d3dee-103">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="d3dee-103">CancelCalendarItem</span></span>

<span data-ttu-id="d3dee-104">Das **CancelCalendarItem** -Element stellt das Response-Objekt dar, das zum Abbrechen einer Besprechung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d3dee-104">The **CancelCalendarItem** element represents the response object that is used to cancel a meeting.</span></span> 
  
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

 <span data-ttu-id="d3dee-105">**CancelCalendarItemType**</span><span class="sxs-lookup"><span data-stu-id="d3dee-105">**CancelCalendarItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d3dee-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d3dee-106">Attributes and elements</span></span>

<span data-ttu-id="d3dee-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d3dee-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d3dee-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d3dee-108">Attributes</span></span>

<span data-ttu-id="d3dee-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d3dee-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d3dee-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d3dee-110">Child elements</span></span>

|<span data-ttu-id="d3dee-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d3dee-111">**Element**</span></span>|<span data-ttu-id="d3dee-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d3dee-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d3dee-113">Betreff</span><span class="sxs-lookup"><span data-stu-id="d3dee-113">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="d3dee-114">Stellt die Subject-Eigenschaft Exchange-Informationsspeicher Elemente dar.</span><span class="sxs-lookup"><span data-stu-id="d3dee-114">Represents the subject property of Exchange store items.</span></span>  <br/> |
|[<span data-ttu-id="d3dee-115">Body</span><span class="sxs-lookup"><span data-stu-id="d3dee-115">Body</span></span>](body.md) <br/> |<span data-ttu-id="d3dee-116">Wird nicht von **CancelCalendarItem**verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3dee-116">Not used by **CancelCalendarItem**.</span></span> <span data-ttu-id="d3dee-117">Verwenden Sie die [NewBodyContent](newbodycontent.md) -Eigenschaft, um den Textkörper Inhalt festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d3dee-117">Use the [NewBodyContent](newbodycontent.md) property to set the body content.</span></span>  <br/> |
|[<span data-ttu-id="d3dee-118">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="d3dee-118">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="d3dee-119">Enthält eine Gruppe von Empfängern eines Elements.</span><span class="sxs-lookup"><span data-stu-id="d3dee-119">Contains a set of recipients of an item.</span></span> <span data-ttu-id="d3dee-120">Dies sind die primären Empfänger eines Elements.</span><span class="sxs-lookup"><span data-stu-id="d3dee-120">These are the primary recipients of an item.</span></span>  <br/> |
|[<span data-ttu-id="d3dee-121">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="d3dee-121">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="d3dee-122">Stellt eine Auflistung der Empfänger dar, die eine Kopie der Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="d3dee-122">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="d3dee-123">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="d3dee-123">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="d3dee-124">Stellt eine Auflistung der Empfänger dar, die eine Blindkopie (Bcc) einer E-Mail erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="d3dee-124">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="d3dee-125">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="d3dee-125">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="d3dee-126">Gibt an, ob der Absender eines Elements eine Lesebestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="d3dee-126">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="d3dee-127">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="d3dee-127">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="d3dee-128">Gibt an, ob der Absender eines Elements eine Zustellungsbestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="d3dee-128">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="d3dee-129">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="d3dee-129">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="d3dee-130">Gibt das Element an, auf das das Response-Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="d3dee-130">Identifies the item to which the response object refers.</span></span>  <br/> |
|[<span data-ttu-id="d3dee-131">NewBodyContent</span><span class="sxs-lookup"><span data-stu-id="d3dee-131">NewBodyContent</span></span>](newbodycontent.md) <br/> |<span data-ttu-id="d3dee-132">Stellt den neuen Textkörper Inhalt einer Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="d3dee-132">Represents the new body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="d3dee-133">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="d3dee-133">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="d3dee-134">Identifiziert die Stellvertretung in einem Stellvertretungs-Zugriffs Szenario.</span><span class="sxs-lookup"><span data-stu-id="d3dee-134">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="d3dee-135">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d3dee-135">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="d3dee-136">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="d3dee-136">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="d3dee-137">Identifiziert den Prinzipal in einem Stellvertretungs-Zugriffs Szenario.</span><span class="sxs-lookup"><span data-stu-id="d3dee-137">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="d3dee-138">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d3dee-138">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d3dee-139">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d3dee-139">Parent elements</span></span>

|<span data-ttu-id="d3dee-140">**Element**</span><span class="sxs-lookup"><span data-stu-id="d3dee-140">**Element**</span></span>|<span data-ttu-id="d3dee-141">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d3dee-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d3dee-142">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="d3dee-142">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> | <span data-ttu-id="d3dee-143">Beschreibt alle Elemente, die an eine Besprechungszeit angrenzen.</span><span class="sxs-lookup"><span data-stu-id="d3dee-143">Describes all items that are adjacent to a meeting time.</span></span><br/><br/> <span data-ttu-id="d3dee-144">Im folgenden finden Sie einige der XPath-Ausdrücke für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="d3dee-144">The following are some of the XPath expressions to this element:</span></span><br/><br/>`/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[<span data-ttu-id="d3dee-145">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="d3dee-145">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> | <span data-ttu-id="d3dee-146">Beschreibt alle Elemente, die mit einer Besprechungszeit in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="d3dee-146">Describes all items that conflict with a meeting time.</span></span><br/><br/><span data-ttu-id="d3dee-147">Im folgenden finden Sie einige der XPath-Ausdrücke für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="d3dee-147">The following are some of the XPath expressions to this element:</span></span><br/><br/>`/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[<span data-ttu-id="d3dee-148">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="d3dee-148">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="d3dee-149">Enthält eine Auflistung aller Response-Objekte, die einem Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d3dee-149">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d3dee-150">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="d3dee-150">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="d3dee-151">Enthält ein Array von Elementen, die in dem durch das [parentfolderid (TargetFolderIdType)-](parentfolderid-targetfolderidtype.md) Element identifizierten Ordner erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d3dee-151">Contains an array of items to create in the folder identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3dee-152">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3dee-152">Remarks</span></span>

<span data-ttu-id="d3dee-153">Das **CancelCalendarItem** -Element wird nur vom Organisator angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d3dee-153">The **CancelCalendarItem** element is only viewed by the organizer.</span></span> <span data-ttu-id="d3dee-154">Sie gilt nur für das Kalenderelement des Organisators.</span><span class="sxs-lookup"><span data-stu-id="d3dee-154">It only applies to the organizer's calendar item.</span></span> 
  
<span data-ttu-id="d3dee-155">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d3dee-155">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d3dee-156">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d3dee-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d3dee-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="d3dee-157">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d3dee-158">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d3dee-158">Schema Name</span></span>  <br/> |<span data-ttu-id="d3dee-159">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d3dee-159">Types schema</span></span>  <br/> |
|<span data-ttu-id="d3dee-160">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d3dee-160">Validation File</span></span>  <br/> |<span data-ttu-id="d3dee-161">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d3dee-161">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d3dee-162">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d3dee-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="d3dee-163">False</span><span class="sxs-lookup"><span data-stu-id="d3dee-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d3dee-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3dee-164">See also</span></span>

- [<span data-ttu-id="d3dee-165">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d3dee-165">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

