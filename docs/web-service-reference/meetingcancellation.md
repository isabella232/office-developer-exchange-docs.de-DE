---
title: MeetingCancellation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingCancellation
api_type:
- schema
ms.assetid: a9c61f7f-2ecd-4b21-9dce-24d9f61aeeea
description: Das MeetingCancellation-Element stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.
ms.openlocfilehash: b0fca0a2dcbdf8685f7b9fb2197db1c3123d54b1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "44467529"
---
# <a name="meetingcancellation"></a><span data-ttu-id="d4c35-103">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="d4c35-103">MeetingCancellation</span></span>

<span data-ttu-id="d4c35-104">Das **MeetingCancellation** -Element stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="d4c35-104">The **MeetingCancellation** element represents a meeting cancellation in the Exchange store.</span></span> 
  
```xml
<MeetingCancellation>
   <MimeContent/>
   <ItemId/>
   <ParentFolderId/>
   <ItemClass/>
   <Subject/>
   <Sensitivity/>
   <Body/>
   <Attachments/>
   <DateTimeReceived/>
   <Size/>
   <Categories/>
   <Importance/>
   <InReplyTo/>
   <IsSubmitted/>
   <IsDraft/>
   <IsFromMe/>
   <IsResend/>
   <IsUnmodified/>
   <InternetMessageHeaders/>
   <DateTimeSent/>
   <DateTimeCreated/>
   <ResponseObjects/>
   <ReminderDueBy/>
   <ReminderIsSet/>
   <ReminderMinutesBeforeStart/>
   <DisplayCc/>
   <DisplayTo/>
   <HasAttachments/>
   <ExtendedProperty/>
   <Culture/>
   <EffectiveRights/>
   <LastModifiedName/>
   <LastModifiedTime/>
   <IsAssociated/>
   <WebClientReadFormQueryString/>
   <WebClientEditFormQueryString/>
   <ConversationId/>
   <UniqueBody/>
   <Sender/>
   <ToRecipients/>
   <CcRecipients/>
   <BccRecipients/>
   <IsReadReceiptRequested/>
   <IsDeliveryReceiptRequested/>
   <ConversationIndex/>
   <ConversationTopic/>
   <From/>
   <InternetMessageId/>
   <IsRead/>
   <IsResponseRequested/>
   <References/>
   <ReplyTo/>
   <AssociatedCalendarItemId/>
   <IsDelegated/>
   <IsOutOfDate/>
   <HasBeenProcessed/>
   <ResponseType/>
</MeetingCancellation>
```

 <span data-ttu-id="d4c35-105">**MeetingCancellationMessageType**</span><span class="sxs-lookup"><span data-stu-id="d4c35-105">**MeetingCancellationMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d4c35-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d4c35-106">Attributes and elements</span></span>

<span data-ttu-id="d4c35-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d4c35-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d4c35-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d4c35-108">Attributes</span></span>

<span data-ttu-id="d4c35-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d4c35-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d4c35-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d4c35-110">Child elements</span></span>

|<span data-ttu-id="d4c35-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d4c35-111">**Element**</span></span>|<span data-ttu-id="d4c35-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d4c35-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d4c35-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="d4c35-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="d4c35-114">Enthält den systemeigenen MIME-Stream eines Objekts, das im base64Binary-Format dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d4c35-114">Contains the native MIME stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="d4c35-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="d4c35-116">Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="d4c35-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="d4c35-117">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d4c35-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-118">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="d4c35-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="d4c35-119">Stellt den Bezeichner des übergeordneten Ordners dar, der das Element oder den Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="d4c35-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="d4c35-120">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d4c35-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="d4c35-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="d4c35-122">Stellt die Nachrichtenklasse eines Elements dar.</span><span class="sxs-lookup"><span data-stu-id="d4c35-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-123">Betreff</span><span class="sxs-lookup"><span data-stu-id="d4c35-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="d4c35-124">Stellt den Betreff für Exchange-Informationsspeicher Elemente und Response-Objekte dar.</span><span class="sxs-lookup"><span data-stu-id="d4c35-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="d4c35-125">Der Betreff ist auf 255 Zeichen limitiert.</span><span class="sxs-lookup"><span data-stu-id="d4c35-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-126">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="d4c35-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="d4c35-127">Gibt die Empfindlichkeitsstufe eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="d4c35-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-128">Body</span><span class="sxs-lookup"><span data-stu-id="d4c35-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="d4c35-129">Stellt den tatsächlichen Textinhalt einer Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="d4c35-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-130">Anlagen</span><span class="sxs-lookup"><span data-stu-id="d4c35-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d4c35-131">Enthält die Elemente oder Dateien, die an ein Element im Exchange-Informationsspeicher angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="d4c35-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="d4c35-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="d4c35-133">Stellt das Datum und die Uhrzeit dar, zu denen ein Element in einem Postfach empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="d4c35-133">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-134">Größe</span><span class="sxs-lookup"><span data-stu-id="d4c35-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="d4c35-135">Stellt die Größe eines Elements in Bytes dar.</span><span class="sxs-lookup"><span data-stu-id="d4c35-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="d4c35-136">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d4c35-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-137">Kategorien</span><span class="sxs-lookup"><span data-stu-id="d4c35-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d4c35-138">Stellt eine Auflistung von Zeichenfolgen dar, die ermitteln, zu welchen Kategorien ein Element im Postfach gehört.</span><span class="sxs-lookup"><span data-stu-id="d4c35-138">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-139">Importance</span><span class="sxs-lookup"><span data-stu-id="d4c35-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="d4c35-140">Beschreibt die Wichtigkeit eines Elements.</span><span class="sxs-lookup"><span data-stu-id="d4c35-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-141">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="d4c35-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="d4c35-142">Stellt den Bezeichner des Elements dar, zu dem dieses Element eine Antwort ist.</span><span class="sxs-lookup"><span data-stu-id="d4c35-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-143">Issubmitted</span><span class="sxs-lookup"><span data-stu-id="d4c35-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="d4c35-144">Gibt an, ob ein Element an den Standardordner Postausgang übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="d4c35-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="d4c35-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="d4c35-146">Stellt dar, ob ein Element noch nicht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d4c35-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-147">Isfromme</span><span class="sxs-lookup"><span data-stu-id="d4c35-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="d4c35-148">Gibt an, ob ein Benutzer ein Element an sich selbst gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="d4c35-148">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="d4c35-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="d4c35-150">Gibt an, ob das Element zuvor gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d4c35-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="d4c35-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="d4c35-152">Gibt an, ob das Element geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="d4c35-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-153">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="d4c35-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="d4c35-154">Stellt die Auflistung aller Internet Nachrichtenkopfzeilen dar, die in einem Element in einem Postfach enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d4c35-154">Represents the collection of all Internet message headers that are contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="d4c35-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="d4c35-156">Stellt das Datum und die Uhrzeit dar, zu denen ein Element in einem Postfach gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d4c35-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-157">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="d4c35-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="d4c35-158">Stellt das Datum und die Uhrzeit dar, zu der ein bestimmtes Element im Postfach erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d4c35-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="d4c35-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="d4c35-160">Enthält eine Auflistung aller Response-Objekte, die einem Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d4c35-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="d4c35-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="d4c35-162">Stellt das Datum und die Uhrzeit des Eintretens des Ereignisses dar.</span><span class="sxs-lookup"><span data-stu-id="d4c35-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="d4c35-163">Dies wird vom [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) -Element verwendet, um zu bestimmen, wann die Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d4c35-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="d4c35-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="d4c35-165">Gibt an, ob für ein Element im Exchange-Informationsspeicher eine Erinnerung festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="d4c35-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="d4c35-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="d4c35-167">Gibt die Anzahl von Minuten vor einem Ereignis an, das eine Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d4c35-167">Represents the number of minutes before an event that a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="d4c35-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="d4c35-169">Stellt die Anzeigezeichenfolge dar, die für den Inhalt des Felds CC verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d4c35-169">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="d4c35-170">Dies ist die verkettete Zeichenfolge aller Anzeigenamen des CC-Empfängers.</span><span class="sxs-lookup"><span data-stu-id="d4c35-170">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-171">Displayto ursprünglicher</span><span class="sxs-lookup"><span data-stu-id="d4c35-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="d4c35-172">Stellt die Anzeigezeichenfolge dar, die für den Inhalt des Felds an verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d4c35-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="d4c35-173">Dies ist die verkettete Zeichenfolge aller in Empfänger Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="d4c35-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="d4c35-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="d4c35-175">Stellt eine Eigenschaft dar, die auf **true** festgelegt ist, wenn ein Element mindestens eine sichtbare Anlage aufweist.</span><span class="sxs-lookup"><span data-stu-id="d4c35-175">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="d4c35-176">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d4c35-176">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-177">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="d4c35-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="d4c35-178">Erweiterte Eigenschaften für Ordner und Elemente identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d4c35-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-179">Kultur</span><span class="sxs-lookup"><span data-stu-id="d4c35-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="d4c35-180">Stellt die Kultur für ein bestimmtes Element in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="d4c35-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-181">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="d4c35-181">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="d4c35-182">Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner.</span><span class="sxs-lookup"><span data-stu-id="d4c35-182">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="d4c35-183">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d4c35-183">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-184">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="d4c35-184">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="d4c35-185">Enthält den Anzeigenamen des letzten Benutzers, der ein Element ändern soll.</span><span class="sxs-lookup"><span data-stu-id="d4c35-185">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-186">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="d4c35-186">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="d4c35-187">Gibt an, wann ein Element zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="d4c35-187">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-188">Isassociated</span><span class="sxs-lookup"><span data-stu-id="d4c35-188">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="d4c35-189">Gibt an, ob das Element einem Ordner zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d4c35-189">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-190">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="d4c35-190">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="d4c35-191">Stellt eine URL dar, die mit dem Microsoft Office Outlook Web App-Endpunkt verkettet werden soll, um ein Element in Outlook Web App zu lesen.</span><span class="sxs-lookup"><span data-stu-id="d4c35-191">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-192">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="d4c35-192">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="d4c35-193">Stellt eine URL dar, die mit dem Outlook Web App-Endpunkt verkettet werden soll, um ein Element in Outlook Web App zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="d4c35-193">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-194">ConversationId</span><span class="sxs-lookup"><span data-stu-id="d4c35-194">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="d4c35-195">Enthält den Bezeichner eines Elements oder einer Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="d4c35-195">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-196">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="d4c35-196">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="d4c35-197">Stellt ein HTML-Fragment oder nur-Text dar, der den eindeutigen Textkörper dieser Unterhaltung darstellt.</span><span class="sxs-lookup"><span data-stu-id="d4c35-197">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-198">Absender</span><span class="sxs-lookup"><span data-stu-id="d4c35-198">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="d4c35-199">Bezeichnet den Absender eines Elements.</span><span class="sxs-lookup"><span data-stu-id="d4c35-199">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-200">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="d4c35-200">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="d4c35-201">Enthält eine Gruppe von Empfängern einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d4c35-201">Contains a set of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-202">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="d4c35-202">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="d4c35-203">Stellt eine Auflistung der Empfänger dar, die eine Kopie der Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="d4c35-203">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-204">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="d4c35-204">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="d4c35-205">Stellt eine Auflistung der Empfänger dar, die eine Blindkopie (Bcc) einer E-Mail erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="d4c35-205">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-206">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="d4c35-206">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="d4c35-207">Gibt an, ob der Absender eines Elements eine Lesebestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="d4c35-207">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-208">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="d4c35-208">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="d4c35-209">Gibt an, ob der Absender eines Elements eine Zustellungsbestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="d4c35-209">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-210">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="d4c35-210">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="d4c35-211">Enthält eine binäre ID, die den Thread darstellt, zu dem diese Nachricht gehört.</span><span class="sxs-lookup"><span data-stu-id="d4c35-211">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-212">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="d4c35-212">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="d4c35-213">Stellt den Konversationsbezeichner dar.</span><span class="sxs-lookup"><span data-stu-id="d4c35-213">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-214">Von</span><span class="sxs-lookup"><span data-stu-id="d4c35-214">From</span></span>](from.md) <br/> |<span data-ttu-id="d4c35-215">Stellt den Adressat dar, der die Nachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="d4c35-215">Represents the addressee from whom the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-216">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="d4c35-216">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="d4c35-217">Stellt die Internet Nachrichten-ID eines Elements dar.</span><span class="sxs-lookup"><span data-stu-id="d4c35-217">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-218">IsRead</span><span class="sxs-lookup"><span data-stu-id="d4c35-218">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="d4c35-219">Gibt an, ob eine Nachricht gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="d4c35-219">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-220">IsResponseRequested</span><span class="sxs-lookup"><span data-stu-id="d4c35-220">IsResponseRequested</span></span>](isresponserequested.md) <br/> |<span data-ttu-id="d4c35-221">Gibt an, ob eine Antwort auf eine e-Mail-Nachricht angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="d4c35-221">Indicates whether a response to an e-mail message is requested.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-222">References</span><span class="sxs-lookup"><span data-stu-id="d4c35-222">References</span></span>](references.md) <br/> |<span data-ttu-id="d4c35-223">Stellt den Usenet-Header dar, der zum Korrelieren von Antworten mit ihren ursprünglichen Nachrichten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d4c35-223">Represents the Usenet header that is used to correlate replies with their original messages.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-224">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="d4c35-224">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="d4c35-225">Gibt eine Reihe von Adressen an, an die Antworten gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d4c35-225">Identifies a set of addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-226">AssociatedCalendarItemId</span><span class="sxs-lookup"><span data-stu-id="d4c35-226">AssociatedCalendarItemId</span></span>](associatedcalendaritemid.md) <br/> |<span data-ttu-id="d4c35-227">Stellt das Kalenderelement dar, das einem [MeetingMessage](meetingmessage.md)zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d4c35-227">Represents the calendar item that is associated with a [MeetingMessage](meetingmessage.md).</span></span>  <br/> |
|[<span data-ttu-id="d4c35-228">Isdelegated wurde</span><span class="sxs-lookup"><span data-stu-id="d4c35-228">IsDelegated</span></span>](isdelegated.md) <br/> |<span data-ttu-id="d4c35-229">Gibt an, ob eine Besprechung von einem Konto mit Stellvertretungszugriff verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="d4c35-229">Indicates whether a meeting was handled by an account with delegate access.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-230">IsOutOfDate</span><span class="sxs-lookup"><span data-stu-id="d4c35-230">IsOutOfDate</span></span>](isoutofdate.md) <br/> |<span data-ttu-id="d4c35-231">Gibt an, ob eine Besprechungsnachricht veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="d4c35-231">Indicates whether a meeting message is out-of-date.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-232">HasBeenProcessed</span><span class="sxs-lookup"><span data-stu-id="d4c35-232">HasBeenProcessed</span></span>](hasbeenprocessed.md) <br/> |<span data-ttu-id="d4c35-233">Gibt an, ob ein Besprechungsnachrichten Element verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="d4c35-233">Indicates whether a meeting message item has been processed.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-234">ResponseType</span><span class="sxs-lookup"><span data-stu-id="d4c35-234">ResponseType</span></span>](responsetype.md) <br/> |<span data-ttu-id="d4c35-235">Stellt den Typ der Empfängerantwort dar, die für eine Besprechung empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="d4c35-235">Represents the type of recipient response received for a meeting.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-236">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="d4c35-236">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="d4c35-237">Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner.</span><span class="sxs-lookup"><span data-stu-id="d4c35-237">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="d4c35-238">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d4c35-238">This element is read-only.</span></span> <span data-ttu-id="d4c35-239">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d4c35-239">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="d4c35-240">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="d4c35-240">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="d4c35-241">Identifiziert die Stellvertretung in einem Stellvertretungs-Zugriffs Szenario.</span><span class="sxs-lookup"><span data-stu-id="d4c35-241">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="d4c35-242">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d4c35-242">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-243">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="d4c35-243">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="d4c35-244">Identifiziert den Prinzipal in einem Stellvertretungs-Zugriffs Szenario.</span><span class="sxs-lookup"><span data-stu-id="d4c35-244">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="d4c35-245">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d4c35-245">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-246">UID</span><span class="sxs-lookup"><span data-stu-id="d4c35-246">UID</span></span>](uid.md) <br/> |<span data-ttu-id="d4c35-247">Identifiziert ein Kalenderelement.</span><span class="sxs-lookup"><span data-stu-id="d4c35-247">Identifies a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-248">Wiederholungs-Nr</span><span class="sxs-lookup"><span data-stu-id="d4c35-248">RecurrenceId</span></span>](recurrenceid.md) <br/> |<span data-ttu-id="d4c35-249">Wird verwendet, um eine bestimmte Instanz eines wiederkehrenden Kalenderelements zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d4c35-249">Used to identify a specific instance of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-250">DateTimeStamp</span><span class="sxs-lookup"><span data-stu-id="d4c35-250">DateTimeStamp</span></span>](datetimestamp.md) <br/> |<span data-ttu-id="d4c35-251">Gibt das Datum und die Uhrzeit der Erstellung einer Instanz eines iCalendar-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="d4c35-251">Indicates the date and time that an instance of an iCalendar object was created.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d4c35-252">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d4c35-252">Parent elements</span></span>

|<span data-ttu-id="d4c35-253">**Element**</span><span class="sxs-lookup"><span data-stu-id="d4c35-253">**Element**</span></span>|<span data-ttu-id="d4c35-254">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d4c35-254">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d4c35-255">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="d4c35-255">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="d4c35-256">Identifiziert alle Kalenderelemente, die an eine Besprechungszeit angrenzen.</span><span class="sxs-lookup"><span data-stu-id="d4c35-256">Identifies all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-257">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="d4c35-257">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="d4c35-258">Identifiziert Daten, die während einer [UpdateItem Operation](updateitem-operation.md) an eine einzelne Eigenschaft eines Elements angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d4c35-258">Identifies data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="d4c35-259">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="d4c35-259">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="d4c35-260">Identifiziert alle Elemente, die mit einer Besprechungszeit in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="d4c35-260">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-261">Erstellen (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="d4c35-261">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="d4c35-262">Identifiziert ein einzelnes Element, das im lokalen Clientspeicher erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4c35-262">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-263">Items</span><span class="sxs-lookup"><span data-stu-id="d4c35-263">Items</span></span>](items.md) <br/> |<span data-ttu-id="d4c35-264">Enthält ein Array von Elementen.</span><span class="sxs-lookup"><span data-stu-id="d4c35-264">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-265">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="d4c35-265">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="d4c35-266">Enthält ein Array von Elementen, die erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d4c35-266">Contains an array of items to create.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-267">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="d4c35-267">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="d4c35-268">Stellt ein Exchange-Element dar, das an ein anderes Exchange-Element angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="d4c35-268">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="d4c35-269">SetItemField</span><span class="sxs-lookup"><span data-stu-id="d4c35-269">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="d4c35-270">Stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einer [UpdateItem Operation](updateitem-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="d4c35-270">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="d4c35-271">Update (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="d4c35-271">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="d4c35-272">Identifiziert ein einzelnes Element, das im lokalen Clientspeicher aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4c35-272">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d4c35-273">Textwert</span><span class="sxs-lookup"><span data-stu-id="d4c35-273">Text value</span></span>

<span data-ttu-id="d4c35-274">Keine.</span><span class="sxs-lookup"><span data-stu-id="d4c35-274">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d4c35-275">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4c35-275">Remarks</span></span>

<span data-ttu-id="d4c35-276">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d4c35-276">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d4c35-277">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d4c35-277">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d4c35-278">Namespace</span><span class="sxs-lookup"><span data-stu-id="d4c35-278">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d4c35-279">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d4c35-279">Schema Name</span></span>  <br/> |<span data-ttu-id="d4c35-280">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d4c35-280">Types schema</span></span>  <br/> |
|<span data-ttu-id="d4c35-281">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d4c35-281">Validation File</span></span>  <br/> |<span data-ttu-id="d4c35-282">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d4c35-282">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d4c35-283">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d4c35-283">Can be Empty</span></span>  <br/> |<span data-ttu-id="d4c35-284">False</span><span class="sxs-lookup"><span data-stu-id="d4c35-284">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d4c35-285">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4c35-285">See also</span></span>



- [<span data-ttu-id="d4c35-286">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d4c35-286">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

