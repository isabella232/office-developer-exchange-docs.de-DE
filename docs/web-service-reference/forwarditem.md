---
title: ForwardItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ForwardItem
api_type:
- schema
ms.assetid: 97786086-8b91-4471-8af8-d21e8d66de87
description: Das ForwardItem-Element enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.
ms.openlocfilehash: 8a82ff28ad1d0dc965a3284c1d0eac9b2fa38301
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758526"
---
# <a name="forwarditem"></a><span data-ttu-id="c61cf-103">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="c61cf-103">ForwardItem</span></span>

<span data-ttu-id="c61cf-104">Das **ForwardItem** -Element enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="c61cf-104">The **ForwardItem** element contains an Exchange store item to forward to recipients.</span></span> 
  
```xml
<ForwardItem>
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
</ForwardItem>
```

<span data-ttu-id="c61cf-105">**ForwardItemType**</span><span class="sxs-lookup"><span data-stu-id="c61cf-105">**ForwardItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c61cf-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c61cf-106">Attributes and elements</span></span>

<span data-ttu-id="c61cf-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c61cf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c61cf-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c61cf-108">Attributes</span></span>

<span data-ttu-id="c61cf-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c61cf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c61cf-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c61cf-110">Child elements</span></span>

|<span data-ttu-id="c61cf-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c61cf-111">**Element**</span></span>|<span data-ttu-id="c61cf-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c61cf-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c61cf-113">Betreff</span><span class="sxs-lookup"><span data-stu-id="c61cf-113">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="c61cf-114">Die Subject-Eigenschaft der Exchange-Speicher-Elemente darstellt.</span><span class="sxs-lookup"><span data-stu-id="c61cf-114">Represents the subject property of Exchange store items.</span></span>  <br/> |
|[<span data-ttu-id="c61cf-115">Body</span><span class="sxs-lookup"><span data-stu-id="c61cf-115">Body</span></span>](body.md) <br/> |<span data-ttu-id="c61cf-116">Stellt den tatsächlichen Textkörperinhalt einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c61cf-116">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="c61cf-117">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="c61cf-117">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="c61cf-118">Enthält eine Reihe von Empfänger eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="c61cf-118">Contains a set of recipients of an item.</span></span> <span data-ttu-id="c61cf-119">Dies sind die primären Empfänger eines Elements.</span><span class="sxs-lookup"><span data-stu-id="c61cf-119">These are the primary recipients of an item.</span></span>  <br/> |
|[<span data-ttu-id="c61cf-120">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="c61cf-120">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="c61cf-121">Stellt eine Auflistung der Empfänger dar, die eine Kopie der Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="c61cf-121">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="c61cf-122">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="c61cf-122">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="c61cf-123">Stellt eine Auflistung der Empfänger dar, die eine Blindkopie (Bcc) einer E-Mail erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="c61cf-123">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="c61cf-124">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="c61cf-124">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="c61cf-125">Gibt an, ob der Absender eines Elements eine lesebestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="c61cf-125">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="c61cf-126">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="c61cf-126">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="c61cf-127">Gibt an, ob der Absender eines Elements eine Empfangsbestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="c61cf-127">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="c61cf-128">Von</span><span class="sxs-lookup"><span data-stu-id="c61cf-128">From</span></span>](from.md) <br/> |<span data-ttu-id="c61cf-129">Stellt die Adresse an, von der die Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c61cf-129">Represents the address from which the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="c61cf-130">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="c61cf-130">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="c61cf-131">Identifiziert das Element auf dem im Response-Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="c61cf-131">Identifies the item to which the response object refers.</span></span>  <br/> |
|[<span data-ttu-id="c61cf-132">NewBodyContent</span><span class="sxs-lookup"><span data-stu-id="c61cf-132">NewBodyContent</span></span>](newbodycontent.md) <br/> |<span data-ttu-id="c61cf-133">Stellt den neuen Textkörperinhalt einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c61cf-133">Represents the new body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="c61cf-134">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="c61cf-134">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="c61cf-135">Identifiziert den Delegaten in eine Access Stellvertreter-Szenario.</span><span class="sxs-lookup"><span data-stu-id="c61cf-135">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="c61cf-136">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c61cf-136">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="c61cf-137">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="c61cf-137">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="c61cf-138">Identifiziert den Prinzipal in einer Access Stellvertreter-Szenario.</span><span class="sxs-lookup"><span data-stu-id="c61cf-138">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="c61cf-139">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c61cf-139">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c61cf-140">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c61cf-140">Parent elements</span></span>

|<span data-ttu-id="c61cf-141">**Element**</span><span class="sxs-lookup"><span data-stu-id="c61cf-141">**Element**</span></span>|<span data-ttu-id="c61cf-142">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c61cf-142">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c61cf-143">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="c61cf-143">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> | <span data-ttu-id="c61cf-144">Werden alle Elemente, die an eine Besprechungszeit angrenzen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c61cf-144">Describes all items that are adjacent to a meeting time.</span></span>  <br/><br/>  <span data-ttu-id="c61cf-145">Im folgenden sind einige der XPath-Ausdrücke auf dieses Element:</span><span class="sxs-lookup"><span data-stu-id="c61cf-145">The following are some of the XPath expressions to this element:</span></span> <br/> <br/>  `/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[<span data-ttu-id="c61cf-146">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="c61cf-146">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> | <span data-ttu-id="c61cf-147">Beschreibt alle Elemente, die mit einem bestimmten Zeitpunkt treffen in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="c61cf-147">Describes all items that conflict with a meeting time.</span></span>  <br/><br/>  <span data-ttu-id="c61cf-148">Im folgenden sind einige der XPath-Ausdrücke auf dieses Element:</span><span class="sxs-lookup"><span data-stu-id="c61cf-148">The following are some of the XPath expressions to this element:</span></span> <br/> <br/>  `/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[<span data-ttu-id="c61cf-149">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="c61cf-149">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="c61cf-150">Enthält eine Auflistung aller Antwort-Objekte, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c61cf-150">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c61cf-151">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="c61cf-151">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="c61cf-152">Enthält ein Array von Elementen im Ordner zu erstellen, die durch das Element [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="c61cf-152">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c61cf-153">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c61cf-153">Remarks</span></span>

<span data-ttu-id="c61cf-154">Das Element [von](from.md) sollte die e-Mail-Adresse des Prinzipals festgelegt werden, wenn ein Element von einer Stellvertretung weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="c61cf-154">The [From](from.md) element should be set to the e-mail address of the principal if an item is forwarded by a delegate.</span></span> <span data-ttu-id="c61cf-155">Wenn die Eigenschaft [aus](from.md) die Stellvertretung nicht festlegt, erscheint das Element direkt aus der Stellvertretung Postfach gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="c61cf-155">If the delegate does not set the [From](from.md) property, the item will appear to have been sent directly from the delegate's mailbox.</span></span> 
  
<span data-ttu-id="c61cf-156">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="c61cf-156">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c61cf-157">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c61cf-157">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c61cf-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="c61cf-158">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c61cf-159">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c61cf-159">Schema Name</span></span>  <br/> |<span data-ttu-id="c61cf-160">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c61cf-160">Types schema</span></span>  <br/> |
|<span data-ttu-id="c61cf-161">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c61cf-161">Validation File</span></span>  <br/> |<span data-ttu-id="c61cf-162">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c61cf-162">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c61cf-163">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c61cf-163">Can be Empty</span></span>  <br/> |<span data-ttu-id="c61cf-164">False</span><span class="sxs-lookup"><span data-stu-id="c61cf-164">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c61cf-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c61cf-165">See also</span></span>

- [<span data-ttu-id="c61cf-166">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c61cf-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

