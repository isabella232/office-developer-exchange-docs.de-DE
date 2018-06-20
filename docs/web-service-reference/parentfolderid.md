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
description: Das ParentFolderId-Element stellt den Bezeichner des übergeordneten Ordners, der das Element oder Ordner enthält.
ms.openlocfilehash: 3f60e8adb62fbf464a58af4169fbcd83910877cc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830687"
---
# <a name="parentfolderid"></a><span data-ttu-id="e5eb3-103">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="e5eb3-103">ParentFolderId</span></span>

<span data-ttu-id="e5eb3-104">Das **ParentFolderId** -Element stellt den Bezeichner des übergeordneten Ordners, der das Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-104">The **ParentFolderId** element represents the identifier of the parent folder that contains the item or folder.</span></span> 
  
```XML
<ParentFolderId Id="" ChangeKey=""/>
```

<span data-ttu-id="e5eb3-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="e5eb3-105">**FolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="e5eb3-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e5eb3-106">Attributes and elements</span></span>

<span data-ttu-id="e5eb3-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e5eb3-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e5eb3-108">Attributes</span></span>

|<span data-ttu-id="e5eb3-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e5eb3-109">**Attribute**</span></span>|<span data-ttu-id="e5eb3-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e5eb3-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e5eb3-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="e5eb3-111">**Id**</span></span> <br/> |<span data-ttu-id="e5eb3-112">Enthält eine Zeichenfolge, die einen Ordner im Exchange-Speicher identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="e5eb3-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="e5eb3-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="e5eb3-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="e5eb3-115">Enthält eine Zeichenfolge, die eine Version eines Ordners identifiziert, die von dem **Id** -Attribut angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-115">Contains a string that identifies a version of a folder that is identified by the **Id** attribute.</span></span> <span data-ttu-id="e5eb3-116">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-116">This attribute is optional.</span></span> <span data-ttu-id="e5eb3-117">Verwenden Sie dieses Attribut, um sicherzustellen, dass die richtige Version eines Ordners verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e5eb3-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e5eb3-118">Child elements</span></span>

<span data-ttu-id="e5eb3-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e5eb3-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e5eb3-120">Parent elements</span></span>

|<span data-ttu-id="e5eb3-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="e5eb3-121">**Element**</span></span>|<span data-ttu-id="e5eb3-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e5eb3-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e5eb3-123">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="e5eb3-123">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="e5eb3-124">Stellt einen Kalenderordner in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-124">Represents a calendar folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-125">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="e5eb3-125">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="e5eb3-126">Stellt ein Kalenderelement in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-126">Represents a calendar item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-127">Contact</span><span class="sxs-lookup"><span data-stu-id="e5eb3-127">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="e5eb3-128">Stellt ein Kontaktelement in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-128">Represents a contact item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-129">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="e5eb3-129">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="e5eb3-130">Stellt einen Kontakteordner in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-130">Represents a contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-131">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="e5eb3-131">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="e5eb3-132">Stellt ein Ereignis in der eines Elements oder Ordners kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-132">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-133">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="e5eb3-133">CreatedEvent</span></span>](createdevent.md) <br/> |<span data-ttu-id="e5eb3-134">Stellt ein Ereignis in der eines Elements oder Ordners erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-134">Represents an event in which an item or folder is created.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-135">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="e5eb3-135">DeletedEvent</span></span>](deletedevent.md) <br/> |<span data-ttu-id="e5eb3-136">Stellt ein Ereignis in der eines Elements oder Ordners gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-136">Represents an event in which an item or folder is deleted.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-137">DistributionList</span><span class="sxs-lookup"><span data-stu-id="e5eb3-137">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="e5eb3-138">Stellt eine private Verteilerliste in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-138">Represents a private distribution list in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-139">Folder</span><span class="sxs-lookup"><span data-stu-id="e5eb3-139">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="e5eb3-140">Stellt einen Ordner in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-140">Represents a folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-141">Element</span><span class="sxs-lookup"><span data-stu-id="e5eb3-141">Item</span></span>](item.md) <br/> |<span data-ttu-id="e5eb3-142">Stellt ein generisches Exchange-Element.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-142">Represents a generic Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-143">Item (UploadItemType)</span><span class="sxs-lookup"><span data-stu-id="e5eb3-143">Item (UploadItemType)</span></span>](item-uploaditemtype.md) <br/> |<span data-ttu-id="e5eb3-144">Stellt ein einzelnes Element in einem Postfach hochladen.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-144">Represents a single item to upload into a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-145">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="e5eb3-145">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="e5eb3-146">Stellt einen Besprechungsabsage in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-146">Represents a meeting cancellation in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-147">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="e5eb3-147">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="e5eb3-148">Stellt eine Besprechungsnachricht in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-148">Represents a meeting message in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-149">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="e5eb3-149">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="e5eb3-150">Stellt eine Besprechungsanfrage in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-150">Represents a meeting request in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-151">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="e5eb3-151">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="e5eb3-152">Stellt eine Antwort auf Besprechungsanfrage in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-152">Represents a meeting response in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-153">Message</span><span class="sxs-lookup"><span data-stu-id="e5eb3-153">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="e5eb3-154">Stellt eine e-Mail-Nachricht in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-154">Represents an e-mail message in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-155">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="e5eb3-155">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="e5eb3-156">Stellt ein Ereignis in der eines Elements oder Ordners geändert wird.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-156">Represents an event in which an item or folder is modified.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-157">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="e5eb3-157">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="e5eb3-158">Stellt ein Ereignis in der eines Elements oder Ordners von einem übergeordneten Ordner in einer anderen übergeordneten Ordner verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-158">Represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-159">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="e5eb3-159">NewMailEvent</span></span>](newmailevent.md) <br/> |<span data-ttu-id="e5eb3-160">Stellt ein Ereignis, das durch eine neue e-Mail-Element in einem Postfach ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-160">Represents an event that is triggered by a new mail item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-161">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="e5eb3-161">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="e5eb3-162">Stellt eine Accept-Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-162">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-163">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="e5eb3-163">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="e5eb3-164">Stellt eine mit Vorbehalt Antworten auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-164">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-165">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="e5eb3-165">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="e5eb3-166">Stellt eine ablehnen Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-166">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-167">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="e5eb3-167">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="e5eb3-168">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-168">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-169">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="e5eb3-169">Task</span></span>](task.md) <br/> |<span data-ttu-id="e5eb3-170">Stellt ein Aufgabenelement in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-170">Represents a task item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-171">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="e5eb3-171">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="e5eb3-172">Enthält eine Antwort an den Ersteller eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-172">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-173">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="e5eb3-173">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="e5eb3-174">Enthält eine Antwort an alle identifizierten Empfänger eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-174">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-175">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="e5eb3-175">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="e5eb3-176">Enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-176">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-177">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="e5eb3-177">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="e5eb3-178">Stellt das Antwortobjekt, das Sie eine Besprechung absagen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-178">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-179">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="e5eb3-179">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="e5eb3-180">Stellt einen Ordner in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-180">Represents a task folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e5eb3-181">"SearchFolder"</span><span class="sxs-lookup"><span data-stu-id="e5eb3-181">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="e5eb3-182">Stellt einen Suchordner in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-182">Represents a search folder in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5eb3-183">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e5eb3-183">Remarks</span></span>

<span data-ttu-id="e5eb3-184">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-184">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e5eb3-185">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e5eb3-185">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e5eb3-186">Namespace</span><span class="sxs-lookup"><span data-stu-id="e5eb3-186">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e5eb3-187">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e5eb3-187">Schema Name</span></span>  <br/> |<span data-ttu-id="e5eb3-188">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e5eb3-188">Types schema</span></span>  <br/> |
|<span data-ttu-id="e5eb3-189">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e5eb3-189">Validation File</span></span>  <br/> |<span data-ttu-id="e5eb3-190">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e5eb3-190">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e5eb3-191">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e5eb3-191">Can be Empty</span></span>  <br/> |<span data-ttu-id="e5eb3-192">False</span><span class="sxs-lookup"><span data-stu-id="e5eb3-192">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e5eb3-193">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5eb3-193">See also</span></span>

- [<span data-ttu-id="e5eb3-194">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e5eb3-194">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

