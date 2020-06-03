---
title: MeetingResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingResponse
api_type:
- schema
ms.assetid: 9f798e79-dafd-4d4d-9967-95fd8e5c0502
description: Das MeetingResponse-Element stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.
ms.openlocfilehash: ff999a671c0321586fbc2adae6cbb5c1ad117ebf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467697"
---
# <a name="meetingresponse"></a><span data-ttu-id="d313d-103">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="d313d-103">MeetingResponse</span></span>

<span data-ttu-id="d313d-104">Das **MeetingResponse** -Element stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="d313d-104">The **MeetingResponse** element represents a meeting response in the Exchange store.</span></span> 
  
```xml
<MeetingResponse>
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
   <EffectiveRights/>
   <ReceivedBy/>
   <ReceivedRepresenting/>
</MeetingResponse>
```

 <span data-ttu-id="d313d-105">**MeetingResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="d313d-105">**MeetingResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d313d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d313d-106">Attributes and elements</span></span>

<span data-ttu-id="d313d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d313d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d313d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d313d-108">Attributes</span></span>

<span data-ttu-id="d313d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d313d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d313d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d313d-110">Child elements</span></span>

|<span data-ttu-id="d313d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d313d-111">**Element**</span></span>|<span data-ttu-id="d313d-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d313d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d313d-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="d313d-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="d313d-114">Enthält den systemeigenen MIME-Stream eines Objekts, das im base64Binary-Format dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d313d-114">Contains the native MIME stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="d313d-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="d313d-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="d313d-116">Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="d313d-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="d313d-117">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d313d-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d313d-118">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="d313d-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="d313d-119">Stellt den Bezeichner des übergeordneten Ordners dar, der das Element oder den Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="d313d-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="d313d-120">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d313d-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d313d-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="d313d-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="d313d-122">Stellt die Nachrichtenklasse eines Elements dar.</span><span class="sxs-lookup"><span data-stu-id="d313d-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="d313d-123">Betreff</span><span class="sxs-lookup"><span data-stu-id="d313d-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="d313d-124">Stellt den Betreff für Exchange-Informationsspeicher Elemente und Response-Objekte dar.</span><span class="sxs-lookup"><span data-stu-id="d313d-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="d313d-125">Der Betreff ist auf 255 Zeichen limitiert.</span><span class="sxs-lookup"><span data-stu-id="d313d-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="d313d-126">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="d313d-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="d313d-127">Gibt die Empfindlichkeitsstufe eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="d313d-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="d313d-128">Body</span><span class="sxs-lookup"><span data-stu-id="d313d-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="d313d-129">Stellt den tatsächlichen Textinhalt einer Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="d313d-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="d313d-130">Anlagen</span><span class="sxs-lookup"><span data-stu-id="d313d-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d313d-131">Enthält die Elemente oder Dateien, die an ein Element im Exchange-Informationsspeicher angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="d313d-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d313d-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="d313d-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="d313d-133">Stellt die Daten und die Zeit dar, die ein Element in einem Postfach empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="d313d-133">Represents the data and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="d313d-134">Größe</span><span class="sxs-lookup"><span data-stu-id="d313d-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="d313d-135">Stellt die Größe eines Elements in Bytes dar.</span><span class="sxs-lookup"><span data-stu-id="d313d-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="d313d-136">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d313d-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d313d-137">Kategorien</span><span class="sxs-lookup"><span data-stu-id="d313d-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d313d-138">Stellt eine Auflistung von Zeichenfolgen dar, die ermitteln, zu welchen Kategorien ein Element im Postfach gehört.</span><span class="sxs-lookup"><span data-stu-id="d313d-138">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="d313d-139">Importance</span><span class="sxs-lookup"><span data-stu-id="d313d-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="d313d-140">Beschreibt die Wichtigkeit eines Elements.</span><span class="sxs-lookup"><span data-stu-id="d313d-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="d313d-141">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="d313d-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="d313d-142">Stellt den Bezeichner des Elements dar, zu dem dieses Element eine Antwort ist.</span><span class="sxs-lookup"><span data-stu-id="d313d-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="d313d-143">Issubmitted</span><span class="sxs-lookup"><span data-stu-id="d313d-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="d313d-144">Gibt an, ob ein Element an den Standardordner Postausgang übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="d313d-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="d313d-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="d313d-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="d313d-146">Stellt dar, ob ein Element noch nicht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d313d-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="d313d-147">Isfromme</span><span class="sxs-lookup"><span data-stu-id="d313d-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="d313d-148">Gibt an, ob ein Benutzer ein Element an sich selbst gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="d313d-148">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="d313d-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="d313d-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="d313d-150">Gibt an, ob das Element zuvor gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d313d-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="d313d-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="d313d-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="d313d-152">Gibt an, ob das Element geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="d313d-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="d313d-153">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="d313d-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="d313d-154">Stellt die Auflistung aller Internet Nachrichtenkopfzeilen dar, die in einem Element in einem Postfach enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d313d-154">Represents the collection of all Internet message headers that are contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d313d-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="d313d-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="d313d-156">Stellt das Datum und die Uhrzeit dar, zu denen ein Element in einem Postfach gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d313d-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="d313d-157">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="d313d-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="d313d-158">Stellt das Datum und die Uhrzeit dar, zu der ein bestimmtes Element im Postfach erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d313d-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="d313d-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="d313d-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="d313d-160">Enthält eine Auflistung aller Response-Objekte, die einem Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d313d-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d313d-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="d313d-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="d313d-162">Stellt das Datum und die Uhrzeit des Eintretens des Ereignisses dar.</span><span class="sxs-lookup"><span data-stu-id="d313d-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="d313d-163">Dies wird vom [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) -Element verwendet, um zu bestimmen, wann die Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d313d-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="d313d-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="d313d-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="d313d-165">Gibt an, ob für ein Element im Exchange-Informationsspeicher eine Erinnerung festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="d313d-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d313d-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="d313d-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="d313d-167">Stellt die Anzahl von Minuten vor einem Ereignis dar, wenn eine Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d313d-167">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="d313d-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="d313d-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="d313d-169">Stellt die Anzeigezeichenfolge dar, die für den Inhalt des Felds CC verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d313d-169">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="d313d-170">Dies ist die verkettete Zeichenfolge aller Anzeigenamen des CC-Empfängers.</span><span class="sxs-lookup"><span data-stu-id="d313d-170">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="d313d-171">Displayto ursprünglicher</span><span class="sxs-lookup"><span data-stu-id="d313d-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="d313d-172">Stellt die Anzeigezeichenfolge dar, die für den Inhalt des Felds an verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d313d-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="d313d-173">Dies ist die verkettete Zeichenfolge aller in Empfänger Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="d313d-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="d313d-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="d313d-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="d313d-175">Stellt eine Eigenschaft dar, die auf **true** festgelegt ist, wenn ein Element mindestens eine sichtbare Anlage aufweist.</span><span class="sxs-lookup"><span data-stu-id="d313d-175">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="d313d-176">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d313d-176">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d313d-177">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="d313d-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="d313d-178">Erweiterte Eigenschaften für Ordner und Elemente identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d313d-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="d313d-179">Kultur</span><span class="sxs-lookup"><span data-stu-id="d313d-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="d313d-180">Stellt die Kultur für ein bestimmtes Element in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="d313d-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d313d-181">Absender</span><span class="sxs-lookup"><span data-stu-id="d313d-181">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="d313d-182">Bezeichnet den Absender eines Elements.</span><span class="sxs-lookup"><span data-stu-id="d313d-182">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="d313d-183">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="d313d-183">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="d313d-184">Enthält eine Gruppe von Empfängern einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d313d-184">Contains a set of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="d313d-185">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="d313d-185">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="d313d-186">Stellt eine Auflistung der Empfänger dar, die eine Kopie der Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="d313d-186">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="d313d-187">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="d313d-187">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="d313d-188">Stellt eine Auflistung der Empfänger dar, die eine Blindkopie (Bcc) einer E-Mail erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="d313d-188">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="d313d-189">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="d313d-189">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="d313d-190">Gibt an, ob der Absender eines Elements eine Lesebestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="d313d-190">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="d313d-191">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="d313d-191">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="d313d-192">Gibt an, ob der Absender eines Elements eine Zustellungsbestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="d313d-192">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="d313d-193">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="d313d-193">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="d313d-194">Enthält eine binäre ID, die den Thread darstellt, zu dem diese Nachricht gehört.</span><span class="sxs-lookup"><span data-stu-id="d313d-194">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="d313d-195">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="d313d-195">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="d313d-196">Stellt den Konversationsbezeichner dar.</span><span class="sxs-lookup"><span data-stu-id="d313d-196">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="d313d-197">Von</span><span class="sxs-lookup"><span data-stu-id="d313d-197">From</span></span>](from.md) <br/> |<span data-ttu-id="d313d-198">Stellt den Adressat dar, der die Nachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="d313d-198">Represents the addressee from whom the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="d313d-199">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="d313d-199">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="d313d-200">Stellt die Internet Nachrichten-ID eines Elements dar.</span><span class="sxs-lookup"><span data-stu-id="d313d-200">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="d313d-201">IsRead</span><span class="sxs-lookup"><span data-stu-id="d313d-201">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="d313d-202">Gibt an, ob eine Nachricht gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="d313d-202">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="d313d-203">IsResponseRequested</span><span class="sxs-lookup"><span data-stu-id="d313d-203">IsResponseRequested</span></span>](isresponserequested.md) <br/> |<span data-ttu-id="d313d-204">Gibt an, ob eine Antwort auf eine e-Mail-Nachricht angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="d313d-204">Indicates whether a response to an e-mail message is requested.</span></span>  <br/> |
|[<span data-ttu-id="d313d-205">References</span><span class="sxs-lookup"><span data-stu-id="d313d-205">References</span></span>](references.md) <br/> |<span data-ttu-id="d313d-206">Stellt den Usenet-Header dar, der zum Korrelieren von Antworten mit ihren ursprünglichen Nachrichten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d313d-206">Represents the Usenet header that is used to correlate replies with their original messages.</span></span>  <br/> |
|[<span data-ttu-id="d313d-207">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="d313d-207">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="d313d-208">Gibt eine Reihe von Adressen an, an die Antworten gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d313d-208">Identifies a set of addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="d313d-209">AssociatedCalendarItemId</span><span class="sxs-lookup"><span data-stu-id="d313d-209">AssociatedCalendarItemId</span></span>](associatedcalendaritemid.md) <br/> |<span data-ttu-id="d313d-210">Stellt das Kalenderelement dar, das einem [MeetingMessage](meetingmessage.md)zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d313d-210">Represents the calendar item that is associated with a [MeetingMessage](meetingmessage.md).</span></span>  <br/> |
|[<span data-ttu-id="d313d-211">Isdelegated wurde</span><span class="sxs-lookup"><span data-stu-id="d313d-211">IsDelegated</span></span>](isdelegated.md) <br/> |<span data-ttu-id="d313d-212">Gibt an, ob eine Besprechung von einem Konto mit Stellvertretungszugriff verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="d313d-212">Indicates whether a meeting was handled by an account with delegate access.</span></span>  <br/> |
|[<span data-ttu-id="d313d-213">IsOutOfDate</span><span class="sxs-lookup"><span data-stu-id="d313d-213">IsOutOfDate</span></span>](isoutofdate.md) <br/> |<span data-ttu-id="d313d-214">Gibt an, ob eine Besprechungsnachricht veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="d313d-214">Indicates whether a meeting message is out-of-date.</span></span>  <br/> |
|[<span data-ttu-id="d313d-215">HasBeenProcessed</span><span class="sxs-lookup"><span data-stu-id="d313d-215">HasBeenProcessed</span></span>](hasbeenprocessed.md) <br/> |<span data-ttu-id="d313d-216">Gibt an, ob ein Besprechungsnachrichten Element verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="d313d-216">Indicates whether a meeting message item has been processed.</span></span>  <br/> |
|[<span data-ttu-id="d313d-217">ResponseType</span><span class="sxs-lookup"><span data-stu-id="d313d-217">ResponseType</span></span>](responsetype.md) <br/> |<span data-ttu-id="d313d-218">Stellt den Typ der Empfängerantwort dar, die für eine Besprechung empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="d313d-218">Represents the type of recipient response that is received for a meeting.</span></span>  <br/> |
|[<span data-ttu-id="d313d-219">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="d313d-219">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="d313d-220">Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner.</span><span class="sxs-lookup"><span data-stu-id="d313d-220">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="d313d-221">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d313d-221">This element is read-only.</span></span> <span data-ttu-id="d313d-222">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d313d-222">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="d313d-223">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="d313d-223">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="d313d-224">Identifiziert die Stellvertretung in einem Stellvertretungs-Zugriffs Szenario.</span><span class="sxs-lookup"><span data-stu-id="d313d-224">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="d313d-225">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d313d-225">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="d313d-226">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="d313d-226">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="d313d-227">Identifiziert den Prinzipal in einem Stellvertretungs-Zugriffs Szenario.</span><span class="sxs-lookup"><span data-stu-id="d313d-227">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="d313d-228">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d313d-228">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="d313d-229">UID</span><span class="sxs-lookup"><span data-stu-id="d313d-229">UID</span></span>](uid.md) <br/> |<span data-ttu-id="d313d-230">Identifiziert ein Kalenderelement.</span><span class="sxs-lookup"><span data-stu-id="d313d-230">Identifies a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="d313d-231">Wiederholungs-Nr</span><span class="sxs-lookup"><span data-stu-id="d313d-231">RecurrenceId</span></span>](recurrenceid.md) <br/> |<span data-ttu-id="d313d-232">Wird verwendet, um eine bestimmte Instanz eines wiederkehrenden Kalenderelements zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d313d-232">Used to identify a specific instance of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="d313d-233">DateTimeStamp</span><span class="sxs-lookup"><span data-stu-id="d313d-233">DateTimeStamp</span></span>](datetimestamp.md) <br/> |<span data-ttu-id="d313d-234">Gibt das Datum und die Uhrzeit der Erstellung einer Instanz eines iCalendar-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="d313d-234">Indicates the date and time that an instance of an iCalendar object was created.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d313d-235">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d313d-235">Parent elements</span></span>

|<span data-ttu-id="d313d-236">**Element**</span><span class="sxs-lookup"><span data-stu-id="d313d-236">**Element**</span></span>|<span data-ttu-id="d313d-237">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d313d-237">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d313d-238">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="d313d-238">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="d313d-239">Identifiziert alle Kalenderelemente, die an eine Besprechungszeit angrenzen.</span><span class="sxs-lookup"><span data-stu-id="d313d-239">Identifies all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="d313d-240">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="d313d-240">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="d313d-241">Identifiziert Daten, die während einer [UpdateItem Operation](updateitem-operation.md) an eine einzelne Eigenschaft eines Elements angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d313d-241">Identifies data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="d313d-242">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="d313d-242">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="d313d-243">Identifiziert alle Elemente, die mit einer Besprechungszeit in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="d313d-243">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="d313d-244">Erstellen (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="d313d-244">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="d313d-245">Identifiziert ein einzelnes Element, das im lokalen Clientspeicher erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d313d-245">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="d313d-246">Elemente</span><span class="sxs-lookup"><span data-stu-id="d313d-246">Items</span></span>](items.md) <br/> |<span data-ttu-id="d313d-247">Enthält ein Array von Elementen.</span><span class="sxs-lookup"><span data-stu-id="d313d-247">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="d313d-248">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="d313d-248">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="d313d-249">Enthält ein Array von Elementen, die erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d313d-249">Contains an array of items to create.</span></span>  <br/> |
|[<span data-ttu-id="d313d-250">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="d313d-250">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="d313d-251">Stellt ein Exchange-Element dar, das an ein anderes Exchange-Element angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="d313d-251">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="d313d-252">SetItemField</span><span class="sxs-lookup"><span data-stu-id="d313d-252">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="d313d-253">Stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einer [UpdateItem Operation](updateitem-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="d313d-253">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="d313d-254">Update (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="d313d-254">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="d313d-255">Identifiziert ein einzelnes Element, das im lokalen Clientspeicher aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d313d-255">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d313d-256">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d313d-256">Remarks</span></span>

<span data-ttu-id="d313d-257">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d313d-257">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d313d-258">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d313d-258">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d313d-259">Namespace</span><span class="sxs-lookup"><span data-stu-id="d313d-259">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d313d-260">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d313d-260">Schema Name</span></span>  <br/> |<span data-ttu-id="d313d-261">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d313d-261">Types schema</span></span>  <br/> |
|<span data-ttu-id="d313d-262">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d313d-262">Validation File</span></span>  <br/> |<span data-ttu-id="d313d-263">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d313d-263">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d313d-264">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d313d-264">Can be Empty</span></span>  <br/> |<span data-ttu-id="d313d-265">False</span><span class="sxs-lookup"><span data-stu-id="d313d-265">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d313d-266">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d313d-266">See also</span></span>



- [<span data-ttu-id="d313d-267">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d313d-267">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

