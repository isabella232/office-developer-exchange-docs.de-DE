---
title: ParentFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ParentFolderId
api_type:
- schema
ms.assetid: 258f4b1f-367e-4c7d-9c29-eb775a2398c7
description: Das parentfolderid-Element stellt den Bezeichner des übergeordneten Ordners dar, der das Element oder den Ordner enthält.
ms.openlocfilehash: 3bad638aa21019472df8f487f1e065d2e725e750
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465751"
---
# <a name="parentfolderid"></a><span data-ttu-id="3e1b6-103">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="3e1b6-103">ParentFolderId</span></span>

<span data-ttu-id="3e1b6-104">Das **parentfolderid** -Element stellt den Bezeichner des übergeordneten Ordners dar, der das Element oder den Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-104">The **ParentFolderId** element represents the identifier of the parent folder that contains the item or folder.</span></span> 
  
```XML
<ParentFolderId Id="" ChangeKey=""/>
```

<span data-ttu-id="3e1b6-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="3e1b6-105">**FolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="3e1b6-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3e1b6-106">Attributes and elements</span></span>

<span data-ttu-id="3e1b6-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3e1b6-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3e1b6-108">Attributes</span></span>

|<span data-ttu-id="3e1b6-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="3e1b6-109">**Attribute**</span></span>|<span data-ttu-id="3e1b6-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3e1b6-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3e1b6-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="3e1b6-111">**Id**</span></span> <br/> |<span data-ttu-id="3e1b6-112">Enthält eine Zeichenfolge, die einen Ordner im Exchange-Informationsspeicher identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="3e1b6-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="3e1b6-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="3e1b6-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="3e1b6-115">Enthält eine Zeichenfolge, die eine Version eines Ordners identifiziert, die durch das **ID-** Attribut identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-115">Contains a string that identifies a version of a folder that is identified by the **Id** attribute.</span></span> <span data-ttu-id="3e1b6-116">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-116">This attribute is optional.</span></span> <span data-ttu-id="3e1b6-117">Verwenden Sie dieses Attribut, um sicherzustellen, dass die richtige Version eines Ordners verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3e1b6-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3e1b6-118">Child elements</span></span>

<span data-ttu-id="3e1b6-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3e1b6-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3e1b6-120">Parent elements</span></span>

|<span data-ttu-id="3e1b6-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="3e1b6-121">**Element**</span></span>|<span data-ttu-id="3e1b6-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3e1b6-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3e1b6-123">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="3e1b6-123">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="3e1b6-124">Stellt einen Kalenderordner in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-124">Represents a calendar folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-125">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="3e1b6-125">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="3e1b6-126">Stellt ein Kalenderelement in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-126">Represents a calendar item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-127">Kontakt</span><span class="sxs-lookup"><span data-stu-id="3e1b6-127">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="3e1b6-128">Stellt ein Kontaktelement in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-128">Represents a contact item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-129">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="3e1b6-129">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="3e1b6-130">Stellt einen Ordner Kontakte in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-130">Represents a contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-131">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="3e1b6-131">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="3e1b6-132">Stellt ein Ereignis dar, in dem ein Element oder ein Ordner kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-132">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-133">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="3e1b6-133">CreatedEvent</span></span>](createdevent.md) <br/> |<span data-ttu-id="3e1b6-134">Stellt ein Ereignis dar, in dem ein Element oder ein Ordner erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-134">Represents an event in which an item or folder is created.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-135">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="3e1b6-135">DeletedEvent</span></span>](deletedevent.md) <br/> |<span data-ttu-id="3e1b6-136">Stellt ein Ereignis dar, in dem ein Element oder ein Ordner gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-136">Represents an event in which an item or folder is deleted.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-137">DistributionList</span><span class="sxs-lookup"><span data-stu-id="3e1b6-137">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="3e1b6-138">Stellt eine private Verteilerliste in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-138">Represents a private distribution list in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-139">Folder</span><span class="sxs-lookup"><span data-stu-id="3e1b6-139">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="3e1b6-140">Stellt einen Ordner in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-140">Represents a folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-141">Element</span><span class="sxs-lookup"><span data-stu-id="3e1b6-141">Item</span></span>](item.md) <br/> |<span data-ttu-id="3e1b6-142">Stellt ein generisches Exchange-Element dar.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-142">Represents a generic Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-143">Element (UploadItemType)</span><span class="sxs-lookup"><span data-stu-id="3e1b6-143">Item (UploadItemType)</span></span>](item-uploaditemtype.md) <br/> |<span data-ttu-id="3e1b6-144">Stellt ein einzelnes Element dar, das in ein Postfach hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-144">Represents a single item to upload into a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-145">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="3e1b6-145">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="3e1b6-146">Stellt eine Besprechungsabsage in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-146">Represents a meeting cancellation in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-147">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="3e1b6-147">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="3e1b6-148">Stellt eine Besprechungsnachricht in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-148">Represents a meeting message in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-149">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="3e1b6-149">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="3e1b6-150">Stellt eine Besprechungsanfrage in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-150">Represents a meeting request in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-151">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="3e1b6-151">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="3e1b6-152">Stellt eine Besprechungsantwort in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-152">Represents a meeting response in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-153">Nachricht</span><span class="sxs-lookup"><span data-stu-id="3e1b6-153">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="3e1b6-154">Stellt eine e-Mail-Nachricht in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-154">Represents an e-mail message in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-155">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="3e1b6-155">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="3e1b6-156">Stellt ein Ereignis dar, in dem ein Element oder ein Ordner geändert wird.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-156">Represents an event in which an item or folder is modified.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-157">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="3e1b6-157">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="3e1b6-158">Stellt ein Ereignis dar, in dem ein Element oder ein Ordner von einem übergeordneten Ordner in einen anderen übergeordneten Ordner verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-158">Represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-159">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="3e1b6-159">NewMailEvent</span></span>](newmailevent.md) <br/> |<span data-ttu-id="3e1b6-160">Stellt ein Ereignis dar, das durch ein neues e-Mail-Element in einem Postfach ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-160">Represents an event that is triggered by a new mail item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-161">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="3e1b6-161">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="3e1b6-162">Stellt eine Accept-Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-162">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-163">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="3e1b6-163">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="3e1b6-164">Stellt eine mit Vorbehalt Antworten auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-164">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-165">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="3e1b6-165">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="3e1b6-166">Stellt eine ablehnen Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-166">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-167">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="3e1b6-167">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="3e1b6-168">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-168">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-169">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="3e1b6-169">Task</span></span>](task.md) <br/> |<span data-ttu-id="3e1b6-170">Stellt ein Aufgabenelement in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-170">Represents a task item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-171">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="3e1b6-171">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="3e1b6-172">Enthält eine Antwort an den Ersteller eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-172">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-173">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="3e1b6-173">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="3e1b6-174">Enthält eine Antwort an alle identifizierten Empfänger eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-174">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-175">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="3e1b6-175">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="3e1b6-176">Enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-176">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-177">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="3e1b6-177">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="3e1b6-178">Stellt das Antwortobjekt, das Sie eine Besprechung absagen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-178">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-179">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="3e1b6-179">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="3e1b6-180">Stellt einen Aufgabenordner in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-180">Represents a task folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="3e1b6-181">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="3e1b6-181">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="3e1b6-182">Stellt einen Suchordner in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-182">Represents a search folder in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e1b6-183">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e1b6-183">Remarks</span></span>

<span data-ttu-id="3e1b6-184">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="3e1b6-184">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3e1b6-185">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3e1b6-185">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3e1b6-186">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e1b6-186">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3e1b6-187">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3e1b6-187">Schema Name</span></span>  <br/> |<span data-ttu-id="3e1b6-188">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3e1b6-188">Types schema</span></span>  <br/> |
|<span data-ttu-id="3e1b6-189">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3e1b6-189">Validation File</span></span>  <br/> |<span data-ttu-id="3e1b6-190">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3e1b6-190">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3e1b6-191">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3e1b6-191">Can be Empty</span></span>  <br/> |<span data-ttu-id="3e1b6-192">False</span><span class="sxs-lookup"><span data-stu-id="3e1b6-192">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3e1b6-193">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e1b6-193">See also</span></span>

- [<span data-ttu-id="3e1b6-194">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3e1b6-194">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

