---
title: Meldung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Message
api_type:
- schema
ms.assetid: 2400b33c-43b2-4fc2-b6fb-275a99e0e810
description: Das Message-Element stellt eine Microsoft Exchange e-Mail-Nachricht dar.
ms.openlocfilehash: 510e97572e54f0ea0cb65fc7c75910e69cc0651f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467781"
---
# <a name="message"></a><span data-ttu-id="06893-103">Meldung</span><span class="sxs-lookup"><span data-stu-id="06893-103">Message</span></span>

<span data-ttu-id="06893-104">Das **Message** -Element stellt eine Microsoft Exchange e-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="06893-104">The **Message** element represents a Microsoft Exchange e-mail message.</span></span> 
  
```xml
<Message>
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
   <EffectiveRights/>
   <ReceivedBy/>
   <ReceivedRepresenting/>
   <LastModifiedName/>
   <LastModifiedTime/>
   <IsAssociated/>
   <WebClientReadFormQueryString/>
   <WebClientEditFormQueryString/>
   <ConversationId/>
   <UniqueBody/>
   <ReminderMessageData/>
</Message>
```

 <span data-ttu-id="06893-105">**MessageType**</span><span class="sxs-lookup"><span data-stu-id="06893-105">**MessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="06893-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="06893-106">Attributes and elements</span></span>

<span data-ttu-id="06893-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="06893-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="06893-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="06893-108">Attributes</span></span>

<span data-ttu-id="06893-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="06893-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="06893-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="06893-110">Child elements</span></span>

|<span data-ttu-id="06893-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="06893-111">**Element**</span></span>|<span data-ttu-id="06893-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="06893-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="06893-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="06893-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="06893-114">Enthält den systemeigenen Multipurpose Internet Mail Extensions (MIME) Stream eines Objekts, das im base64Binary-Format dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="06893-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="06893-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="06893-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="06893-116">Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="06893-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="06893-117">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="06893-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="06893-118">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="06893-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="06893-119">Stellt den Bezeichner des übergeordneten Ordners dar, der das Element oder den Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="06893-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="06893-120">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="06893-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="06893-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="06893-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="06893-122">Stellt die Nachrichtenklasse eines Elements dar.</span><span class="sxs-lookup"><span data-stu-id="06893-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="06893-123">Betreff</span><span class="sxs-lookup"><span data-stu-id="06893-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="06893-124">Stellt den Betreff für Exchange-Informationsspeicher Elemente und Response-Objekte dar.</span><span class="sxs-lookup"><span data-stu-id="06893-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="06893-125">Der Betreff ist auf 255 Zeichen limitiert.</span><span class="sxs-lookup"><span data-stu-id="06893-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="06893-126">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="06893-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="06893-127">Gibt die Empfindlichkeitsstufe eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="06893-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="06893-128">Body</span><span class="sxs-lookup"><span data-stu-id="06893-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="06893-129">Stellt den tatsächlichen Textinhalt einer Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="06893-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="06893-130">Anlagen</span><span class="sxs-lookup"><span data-stu-id="06893-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="06893-131">Enthält die Elemente oder Dateien, die an ein Element im Exchange-Informationsspeicher angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="06893-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="06893-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="06893-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="06893-133">Stellt das Datum und die Uhrzeit dar, zu denen ein Element in einem Postfach empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="06893-133">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="06893-134">Größe</span><span class="sxs-lookup"><span data-stu-id="06893-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="06893-135">Stellt die Größe eines Elements in Bytes dar.</span><span class="sxs-lookup"><span data-stu-id="06893-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="06893-136">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="06893-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="06893-137">Kategorien</span><span class="sxs-lookup"><span data-stu-id="06893-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="06893-138">Stellt eine Auflistung von Zeichenfolgen dar, die ermitteln, zu welchen Kategorien ein Element im Postfach gehört.</span><span class="sxs-lookup"><span data-stu-id="06893-138">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="06893-139">Importance</span><span class="sxs-lookup"><span data-stu-id="06893-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="06893-140">Beschreibt die Wichtigkeit eines Elements.</span><span class="sxs-lookup"><span data-stu-id="06893-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="06893-141">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="06893-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="06893-142">Stellt den Bezeichner des Elements dar, zu dem dieses Element eine Antwort ist.</span><span class="sxs-lookup"><span data-stu-id="06893-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="06893-143">Issubmitted</span><span class="sxs-lookup"><span data-stu-id="06893-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="06893-144">Gibt an, ob ein Element an den Standardordner Postausgang übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="06893-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="06893-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="06893-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="06893-146">Stellt dar, ob ein Element noch nicht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="06893-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="06893-147">Isfromme</span><span class="sxs-lookup"><span data-stu-id="06893-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="06893-148">Gibt an, ob ein Benutzer ein Element an sich selbst gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="06893-148">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="06893-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="06893-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="06893-150">Gibt an, ob das Element zuvor gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="06893-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="06893-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="06893-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="06893-152">Gibt an, ob das Element geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="06893-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="06893-153">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="06893-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="06893-154">Stellt die Auflistung aller Internet Nachrichtenkopfzeilen dar, die in einem Element in einem Postfach enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="06893-154">Represents the collection of all Internet message headers that are contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="06893-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="06893-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="06893-156">Stellt das Datum und die Uhrzeit dar, zu denen ein Element in einem Postfach gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="06893-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="06893-157">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="06893-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="06893-158">Stellt das Datum und die Uhrzeit dar, zu der ein bestimmtes Element im Postfach erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="06893-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="06893-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="06893-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="06893-160">Enthält eine Auflistung aller Response-Objekte, die einem Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="06893-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="06893-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="06893-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="06893-162">Stellt das Datum und die Uhrzeit des Eintretens des Ereignisses dar.</span><span class="sxs-lookup"><span data-stu-id="06893-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="06893-163">Dies wird vom [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) -Element verwendet, um zu bestimmen, wann die Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="06893-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="06893-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="06893-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="06893-165">Gibt an, ob für ein Element im Exchange-Informationsspeicher eine Erinnerung festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="06893-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="06893-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="06893-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="06893-167">Stellt die Anzahl von Minuten vor einem Ereignis dar, wenn eine Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="06893-167">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="06893-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="06893-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="06893-169">Stellt die Anzeigezeichenfolge dar, die für den Inhalt der CC-Zeile verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="06893-169">Represents the display string that is used for the contents of the CC line.</span></span> <span data-ttu-id="06893-170">Dies ist die verkettete Zeichenfolge aller Anzeigenamen des CC-Empfängers.</span><span class="sxs-lookup"><span data-stu-id="06893-170">This is the concatenated string of all CC recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="06893-171">Displayto ursprünglicher</span><span class="sxs-lookup"><span data-stu-id="06893-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="06893-172">Stellt die Anzeigezeichenfolge dar, die für den Inhalt des Felds an verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="06893-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="06893-173">Dies ist die verkettete Zeichenfolge aller in Empfänger Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="06893-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="06893-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="06893-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="06893-175">Stellt eine Eigenschaft dar, die auf **true** festgelegt ist, wenn ein Element mindestens eine sichtbare Anlage aufweist.</span><span class="sxs-lookup"><span data-stu-id="06893-175">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="06893-176">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="06893-176">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="06893-177">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="06893-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="06893-178">Erweiterte Eigenschaften für Ordner und Elemente identifiziert.</span><span class="sxs-lookup"><span data-stu-id="06893-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="06893-179">Kultur</span><span class="sxs-lookup"><span data-stu-id="06893-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="06893-180">Stellt die Kultur für ein bestimmtes Element in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="06893-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="06893-181">Absender</span><span class="sxs-lookup"><span data-stu-id="06893-181">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="06893-182">Bezeichnet den Absender eines Elements.</span><span class="sxs-lookup"><span data-stu-id="06893-182">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="06893-183">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="06893-183">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="06893-184">Enthält eine Gruppe von Empfängern einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="06893-184">Contains a set of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="06893-185">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="06893-185">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="06893-186">Stellt eine Auflistung der Empfänger dar, die eine Kopie der Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="06893-186">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="06893-187">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="06893-187">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="06893-188">Stellt eine Auflistung von Empfängern dar, die eine Blindkopie (BCC) einer e-Mail-Nachricht erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="06893-188">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="06893-189">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="06893-189">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="06893-190">Gibt an, ob der Absender eines Elements eine Lesebestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="06893-190">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="06893-191">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="06893-191">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="06893-192">Gibt an, ob der Absender eines Elements eine Zustellungsbestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="06893-192">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="06893-193">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="06893-193">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="06893-194">Enthält eine binäre ID, die den Thread darstellt, zu dem diese Nachricht gehört.</span><span class="sxs-lookup"><span data-stu-id="06893-194">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="06893-195">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="06893-195">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="06893-196">Stellt den Konversationsbezeichner dar.</span><span class="sxs-lookup"><span data-stu-id="06893-196">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="06893-197">Von</span><span class="sxs-lookup"><span data-stu-id="06893-197">From</span></span>](from.md) <br/> |<span data-ttu-id="06893-198">Stellt den Adressat dar, der die Nachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="06893-198">Represents the addressee from whom the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="06893-199">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="06893-199">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="06893-200">Stellt die Internet Nachrichten-ID eines Elements dar.</span><span class="sxs-lookup"><span data-stu-id="06893-200">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="06893-201">IsRead</span><span class="sxs-lookup"><span data-stu-id="06893-201">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="06893-202">Gibt an, ob eine Nachricht gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="06893-202">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="06893-203">IsResponseRequested</span><span class="sxs-lookup"><span data-stu-id="06893-203">IsResponseRequested</span></span>](isresponserequested.md) <br/> |<span data-ttu-id="06893-204">Gibt an, ob eine Antwort auf eine e-Mail-Nachricht angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="06893-204">Indicates whether a response to an e-mail message is requested.</span></span>  <br/> |
|[<span data-ttu-id="06893-205">References</span><span class="sxs-lookup"><span data-stu-id="06893-205">References</span></span>](references.md) <br/> |<span data-ttu-id="06893-206">Stellt den Usenet-Header dar, der zum Korrelieren von Antworten mit ihren ursprünglichen Nachrichten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="06893-206">Represents the Usenet header that is used to correlate replies with their original messages.</span></span>  <br/> |
|[<span data-ttu-id="06893-207">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="06893-207">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="06893-208">Gibt eine Reihe von Adressen an, an die Antworten gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="06893-208">Identifies a set of addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="06893-209">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="06893-209">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="06893-210">Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner.</span><span class="sxs-lookup"><span data-stu-id="06893-210">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="06893-211">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="06893-211">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="06893-212">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="06893-212">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="06893-213">Identifiziert die Stellvertretung in einem Stellvertretungs-Zugriffs Szenario.</span><span class="sxs-lookup"><span data-stu-id="06893-213">Identifies the delegate in a delegate access scenario.</span></span>  <br/> |
|[<span data-ttu-id="06893-214">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="06893-214">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="06893-215">Identifiziert den Prinzipal in einem Stellvertretungs-Zugriffs Szenario.</span><span class="sxs-lookup"><span data-stu-id="06893-215">Identifies the principal in a delegate access scenario.</span></span>  <br/> |
|[<span data-ttu-id="06893-216">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="06893-216">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="06893-217">Enthält den Anzeigenamen des letzten Benutzers, der ein Element ändern soll.</span><span class="sxs-lookup"><span data-stu-id="06893-217">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="06893-218">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="06893-218">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="06893-219">Gibt an, wann ein Element zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="06893-219">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="06893-220">Isassociated</span><span class="sxs-lookup"><span data-stu-id="06893-220">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="06893-221">Gibt an, ob das Element einem Ordner zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="06893-221">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="06893-222">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="06893-222">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="06893-223">Stellt eine URL dar, die mit dem Microsoft Office Outlook Web App-Endpunkt verkettet werden soll, um ein Element in Outlook Web App zu lesen.</span><span class="sxs-lookup"><span data-stu-id="06893-223">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="06893-224">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="06893-224">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="06893-225">Stellt eine URL dar, die mit dem Outlook Web App-Endpunkt verkettet werden soll, um ein Element in Outlook Web App zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="06893-225">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="06893-226">ConversationId</span><span class="sxs-lookup"><span data-stu-id="06893-226">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="06893-227">Enthält den Bezeichner eines Elements oder einer Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="06893-227">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="06893-228">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="06893-228">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="06893-229">Stellt ein HTML-Fragment oder nur-Text dar, der den eindeutigen Textkörper dieser Unterhaltung darstellt.</span><span class="sxs-lookup"><span data-stu-id="06893-229">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="06893-230">ReminderMessageData</span><span class="sxs-lookup"><span data-stu-id="06893-230">ReminderMessageData</span></span>](remindermessagedata.md) <br/> |<span data-ttu-id="06893-231">Enthält die Daten für eine Erinnerungsnachricht.</span><span class="sxs-lookup"><span data-stu-id="06893-231">Contains the data for a reminder message.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="06893-232">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="06893-232">Parent elements</span></span>

|<span data-ttu-id="06893-233">**Element**</span><span class="sxs-lookup"><span data-stu-id="06893-233">**Element**</span></span>|<span data-ttu-id="06893-234">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="06893-234">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="06893-235">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="06893-235">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="06893-236">Beschreibt alle Kalenderelemente, die an eine Besprechungszeit angrenzen.</span><span class="sxs-lookup"><span data-stu-id="06893-236">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="06893-237">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="06893-237">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="06893-238">Identifiziert Daten, die während einer [UpdateItem Operation](updateitem-operation.md) an eine einzelne Eigenschaft eines Elements angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="06893-238">Identifies data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="06893-239">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="06893-239">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="06893-240">Identifiziert alle Elemente, die mit einer Besprechungszeit in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="06893-240">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="06893-241">Erstellen (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="06893-241">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="06893-242">Identifiziert ein einzelnes Element, das im lokalen Clientspeicher erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="06893-242">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="06893-243">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="06893-243">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="06893-244">Stellt ein Exchange-Element dar, das an ein anderes Exchange-Element angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="06893-244">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="06893-245">Items</span><span class="sxs-lookup"><span data-stu-id="06893-245">Items</span></span>](items.md) <br/> |<span data-ttu-id="06893-246">Enthält ein Array von Elementen.</span><span class="sxs-lookup"><span data-stu-id="06893-246">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="06893-247">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="06893-247">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="06893-248">Enthält ein Array von Elementen, die in dem Ordner erstellt werden sollen, der durch das [parentfolderid (TargetFolderIdType)-](parentfolderid-targetfolderidtype.md) Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="06893-248">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="06893-249">SetItemField</span><span class="sxs-lookup"><span data-stu-id="06893-249">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="06893-250">Stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einer [UpdateItem Operation](updateitem-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="06893-250">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="06893-251">Update (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="06893-251">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="06893-252">Identifiziert ein einzelnes Element, das im lokalen Clientspeicher aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="06893-252">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="06893-253">Textwert</span><span class="sxs-lookup"><span data-stu-id="06893-253">Text value</span></span>

<span data-ttu-id="06893-254">Keine.</span><span class="sxs-lookup"><span data-stu-id="06893-254">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="06893-255">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06893-255">Remarks</span></span>

<span data-ttu-id="06893-256">Ein weiteres **Nachrichten** Element, [Message (Availability)](message-availability.md) wird von den Verfügbarkeits Vorgängen verwendet, um OOF-Nachrichten zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="06893-256">Another **Message** element, [Message (Availability)](message-availability.md) is used by the Availability operations to return OOF messages.</span></span> 
  
<span data-ttu-id="06893-257">[Nachrichten](message-ex15websvcsotherref.md) Elemente stellen e-Mail-Nachrichten und alle anderen Elemente dar, die nicht stark vom Exchange-Webdienste Schema typisiert sind.</span><span class="sxs-lookup"><span data-stu-id="06893-257">[Message](message-ex15websvcsotherref.md) elements represent e-mail messages and all other items that are not strongly typed by the Exchange Web Services (EWS) schema.</span></span> <span data-ttu-id="06893-258">Elemente wie IPM.Sharing- und IPM.InfoPath-Elemente werden als **Message**-Elemente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="06893-258">Items such as IPM.Sharing and IPM.InfoPath are returned as **Message** elements.</span></span> <span data-ttu-id="06893-259">Exchange 2010 gibt nicht das Basis **Element** Element in Antworten zurück.</span><span class="sxs-lookup"><span data-stu-id="06893-259">Exchange 2010 does not return the base **Item** element in responses.</span></span> 
  
<span data-ttu-id="06893-260">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="06893-260">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="06893-261">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="06893-261">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="06893-262">Namespace</span><span class="sxs-lookup"><span data-stu-id="06893-262">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="06893-263">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="06893-263">Schema Name</span></span>  <br/> |<span data-ttu-id="06893-264">Schematypen</span><span class="sxs-lookup"><span data-stu-id="06893-264">Types schema</span></span>  <br/> |
|<span data-ttu-id="06893-265">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="06893-265">Validation File</span></span>  <br/> |<span data-ttu-id="06893-266">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="06893-266">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="06893-267">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="06893-267">Can be Empty</span></span>  <br/> |<span data-ttu-id="06893-268">False</span><span class="sxs-lookup"><span data-stu-id="06893-268">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="06893-269">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06893-269">See also</span></span>



- [<span data-ttu-id="06893-270">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="06893-270">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

