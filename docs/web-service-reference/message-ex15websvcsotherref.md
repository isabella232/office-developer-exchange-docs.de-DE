---
title: Nachricht
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
description: Message-Elements darstellt, eine E-mail-Nachricht von Microsoft Exchange.
ms.openlocfilehash: 388b944cfa16899cb2376320882f5087396d7b82
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830474"
---
# <a name="message"></a><span data-ttu-id="19888-103">Nachricht</span><span class="sxs-lookup"><span data-stu-id="19888-103">Message</span></span>

<span data-ttu-id="19888-104">**Message** -Elements darstellt, eine E-mail-Nachricht von Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="19888-104">The **Message** element represents a Microsoft Exchange e-mail message.</span></span> 
  
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

 <span data-ttu-id="19888-105">**MessageType**</span><span class="sxs-lookup"><span data-stu-id="19888-105">**MessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="19888-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="19888-106">Attributes and elements</span></span>

<span data-ttu-id="19888-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="19888-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="19888-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="19888-108">Attributes</span></span>

<span data-ttu-id="19888-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="19888-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="19888-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="19888-110">Child elements</span></span>

|<span data-ttu-id="19888-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="19888-111">**Element**</span></span>|<span data-ttu-id="19888-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="19888-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="19888-113">' MimeContent '</span><span class="sxs-lookup"><span data-stu-id="19888-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="19888-114">Enthält den systemeigene Multipurpose Internet Mail Extensions (MIME) Stream eines Objekts, das im Format base64Binary dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="19888-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="19888-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="19888-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="19888-116">Enthält den eindeutigen Bezeichner und Ändern eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="19888-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="19888-117">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="19888-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="19888-118">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="19888-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="19888-119">Stellt den Bezeichner des übergeordneten Ordners, der das Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="19888-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="19888-120">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="19888-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="19888-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="19888-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="19888-122">Die Nachrichtenklasse eines Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="19888-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="19888-123">Betreff</span><span class="sxs-lookup"><span data-stu-id="19888-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="19888-124">Der Betreff den Exchange-Speicherelemente und Antwortobjekte darstellt.</span><span class="sxs-lookup"><span data-stu-id="19888-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="19888-125">Der Betreff ist auf 255 Zeichen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="19888-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="19888-126">Vertraulichkeit</span><span class="sxs-lookup"><span data-stu-id="19888-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="19888-127">Gibt die Vertraulichkeitsstufe eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="19888-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="19888-128">Body</span><span class="sxs-lookup"><span data-stu-id="19888-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="19888-129">Stellt den tatsächlichen Textkörperinhalt einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="19888-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="19888-130">Anlagen</span><span class="sxs-lookup"><span data-stu-id="19888-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="19888-131">Enthält die Elemente oder Dateien, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="19888-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="19888-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="19888-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="19888-133">Stellt das Datum und die Uhrzeit, die ein Element in einem Postfach empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="19888-133">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="19888-134">Size</span><span class="sxs-lookup"><span data-stu-id="19888-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="19888-135">Die Größe in Bytes eines Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="19888-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="19888-136">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="19888-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="19888-137">Kategorien</span><span class="sxs-lookup"><span data-stu-id="19888-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="19888-138">Stellt eine Auflistung von Zeichenfolgen, die identifizieren, welche, die Kategorien ein Elements im Postfach gehört.</span><span class="sxs-lookup"><span data-stu-id="19888-138">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="19888-139">Importance</span><span class="sxs-lookup"><span data-stu-id="19888-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="19888-140">Beschreibt die Bedeutung eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="19888-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="19888-141">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="19888-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="19888-142">Stellt den Bezeichner des Elements, der dieses Element eine Antwort ist.</span><span class="sxs-lookup"><span data-stu-id="19888-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="19888-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="19888-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="19888-144">Gibt an, ob ein Element in den Standardordner Postausgang gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="19888-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="19888-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="19888-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="19888-146">Stellt dar, ob ein Element noch nicht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="19888-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="19888-147">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="19888-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="19888-148">Gibt an, ob ein Benutzer ein Element an sich gesendet.</span><span class="sxs-lookup"><span data-stu-id="19888-148">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="19888-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="19888-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="19888-150">Gibt an, ob das Element zuvor gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="19888-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="19888-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="19888-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="19888-152">Gibt an, ob das Element geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="19888-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="19888-153">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="19888-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="19888-154">Stellt die Auflistung aller Internet Message Header, die innerhalb eines Elements in einem Postfach enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="19888-154">Represents the collection of all Internet message headers that are contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="19888-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="19888-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="19888-156">Stellt das Datum und die Uhrzeit, die ein Element in einem Postfach gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="19888-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="19888-157">"Datetimecreated"</span><span class="sxs-lookup"><span data-stu-id="19888-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="19888-158">Stellt das Datum und die Uhrzeit, die ein bestimmtes Element im Postfach erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="19888-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="19888-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="19888-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="19888-160">Enthält eine Auflistung aller Antwort-Objekte, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="19888-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="19888-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="19888-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="19888-162">Stellt das Datum und die Uhrzeit bei des Ereignisses eintreten.</span><span class="sxs-lookup"><span data-stu-id="19888-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="19888-163">Dies wird durch die [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) -Element verwendet, um zu bestimmen, wann die Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="19888-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="19888-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="19888-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="19888-165">Gibt an, ob eine Erinnerung für ein Element in der Exchange-Informationsspeicher festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="19888-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="19888-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="19888-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="19888-167">Stellt die Anzahl der Minuten, bevor ein Ereignis, wenn eine Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="19888-167">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="19888-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="19888-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="19888-169">Stellt die Zeichenfolge, die für den Inhalt der CC-Zeile verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="19888-169">Represents the display string that is used for the contents of the CC line.</span></span> <span data-ttu-id="19888-170">Dies ist die verkettete Zeichenfolge alle Anzeigenamen der CC-Empfänger.</span><span class="sxs-lookup"><span data-stu-id="19888-170">This is the concatenated string of all CC recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="19888-171">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="19888-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="19888-172">Stellt die Zeichenfolge, die für den Inhalt des im Feld an verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="19888-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="19888-173">Dies ist die verkettete Zeichenfolge aller in Empfänger Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="19888-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="19888-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="19888-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="19888-175">Stellt eine Eigenschaft, die auf **true** festgelegt ist, wenn ein Element mindestens eine Anlage sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="19888-175">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="19888-176">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="19888-176">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="19888-177">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="19888-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="19888-178">Erweiterte Eigenschaften für Ordner und Elemente identifiziert.</span><span class="sxs-lookup"><span data-stu-id="19888-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="19888-179">Kultur</span><span class="sxs-lookup"><span data-stu-id="19888-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="19888-180">Stellt die Kultur für ein bestimmtes Element in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="19888-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="19888-181">Absender</span><span class="sxs-lookup"><span data-stu-id="19888-181">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="19888-182">Bezeichnet den Absender eines Elements.</span><span class="sxs-lookup"><span data-stu-id="19888-182">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="19888-183">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="19888-183">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="19888-184">Enthält einen Satz an Empfänger einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="19888-184">Contains a set of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="19888-185">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="19888-185">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="19888-186">Stellt eine Auflistung der Empfänger dar, die eine Kopie der Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="19888-186">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="19888-187">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="19888-187">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="19888-188">Stellt eine Auflistung der Empfänger, die eine Blindkopie (Bcc) einer e-Mail-Nachricht empfangen.</span><span class="sxs-lookup"><span data-stu-id="19888-188">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="19888-189">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="19888-189">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="19888-190">Gibt an, ob der Absender eines Elements eine lesebestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="19888-190">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="19888-191">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="19888-191">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="19888-192">Gibt an, ob der Absender eines Elements eine Empfangsbestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="19888-192">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="19888-193">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="19888-193">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="19888-194">Enthält eine binäre Kennung, die den Thread darstellt, zu dem diese Nachricht gehört.</span><span class="sxs-lookup"><span data-stu-id="19888-194">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="19888-195">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="19888-195">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="19888-196">Den Bezeichner für die Unterhaltung darstellt.</span><span class="sxs-lookup"><span data-stu-id="19888-196">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="19888-197">Von</span><span class="sxs-lookup"><span data-stu-id="19888-197">From</span></span>](from.md) <br/> |<span data-ttu-id="19888-198">Stellt den Adressat dar, der die Nachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="19888-198">Represents the addressee from whom the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="19888-199">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="19888-199">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="19888-200">Die Internetnachricht-ID eines Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="19888-200">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="19888-201">IsRead</span><span class="sxs-lookup"><span data-stu-id="19888-201">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="19888-202">Gibt an, ob eine Nachricht gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="19888-202">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="19888-203">IsResponseRequested</span><span class="sxs-lookup"><span data-stu-id="19888-203">IsResponseRequested</span></span>](isresponserequested.md) <br/> |<span data-ttu-id="19888-204">Gibt an, ob eine Antwort auf eine E-mail-Nachricht angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="19888-204">Indicates whether a response to an e-mail message is requested.</span></span>  <br/> |
|[<span data-ttu-id="19888-205">Referenzen</span><span class="sxs-lookup"><span data-stu-id="19888-205">References</span></span>](references.md) <br/> |<span data-ttu-id="19888-206">Stellt den Usenet-Header, der zum Korrelieren Antworten mit ihrer ursprünglichen Nachrichten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="19888-206">Represents the Usenet header that is used to correlate replies with their original messages.</span></span>  <br/> |
|[<span data-ttu-id="19888-207">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="19888-207">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="19888-208">Identifiziert eine Reihe von Adressen, die an die Antworten gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="19888-208">Identifies a set of addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="19888-209">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="19888-209">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="19888-210">Der Client Rechte basierend auf den berechtigungseinstellungen für das Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="19888-210">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="19888-211">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="19888-211">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="19888-212">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="19888-212">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="19888-213">Identifiziert den Delegaten in eine Access Stellvertreter-Szenario.</span><span class="sxs-lookup"><span data-stu-id="19888-213">Identifies the delegate in a delegate access scenario.</span></span>  <br/> |
|[<span data-ttu-id="19888-214">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="19888-214">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="19888-215">Identifiziert den Prinzipal in einer Access Stellvertreter-Szenario.</span><span class="sxs-lookup"><span data-stu-id="19888-215">Identifies the principal in a delegate access scenario.</span></span>  <br/> |
|[<span data-ttu-id="19888-216">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="19888-216">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="19888-217">Enthält den Anzeigenamen des Benutzers auf ein Element zu ändern.</span><span class="sxs-lookup"><span data-stu-id="19888-217">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="19888-218">ZuletztGeändertUm</span><span class="sxs-lookup"><span data-stu-id="19888-218">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="19888-219">Gibt an, wann ein Element zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="19888-219">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="19888-220">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="19888-220">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="19888-221">Gibt an, ob das Element einem Ordner zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="19888-221">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="19888-222">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="19888-222">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="19888-223">Stellt eine URL zu verketten an den Microsoft Office Outlook Web App-Endpunkt ein Elements in Outlook Web App zu lesen.</span><span class="sxs-lookup"><span data-stu-id="19888-223">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="19888-224">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="19888-224">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="19888-225">Stellt eine URL an den Endpunkt Outlook Web App so bearbeiten Sie ein Element in Outlook Web App verketten.</span><span class="sxs-lookup"><span data-stu-id="19888-225">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="19888-226">ConversationId</span><span class="sxs-lookup"><span data-stu-id="19888-226">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="19888-227">Enthält die ID eines Elements oder einer Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="19888-227">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="19888-228">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="19888-228">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="19888-229">Stellt ein HTML-Fragment oder nur-Text, der den eindeutigen Text an dieser Unterhaltung darstellt.</span><span class="sxs-lookup"><span data-stu-id="19888-229">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="19888-230">ReminderMessageData</span><span class="sxs-lookup"><span data-stu-id="19888-230">ReminderMessageData</span></span>](remindermessagedata.md) <br/> |<span data-ttu-id="19888-231">Enthält die Daten für eine Erinnerungsnachricht.</span><span class="sxs-lookup"><span data-stu-id="19888-231">Contains the data for a reminder message.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="19888-232">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="19888-232">Parent elements</span></span>

|<span data-ttu-id="19888-233">**Element**</span><span class="sxs-lookup"><span data-stu-id="19888-233">**Element**</span></span>|<span data-ttu-id="19888-234">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="19888-234">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="19888-235">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="19888-235">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="19888-236">Werden alle Kalenderelemente, die an eine Besprechungszeit angrenzen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="19888-236">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="19888-237">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="19888-237">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="19888-238">Identifiziert Daten, die während einer [UpdateItem Operation](updateitem-operation.md) an eine einzelne Eigenschaft eines Elements angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="19888-238">Identifies data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="19888-239">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="19888-239">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="19888-240">Identifiziert alle Elemente, die mit einem bestimmten Zeitpunkt treffen Konflikt.</span><span class="sxs-lookup"><span data-stu-id="19888-240">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="19888-241">Erstellen (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="19888-241">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="19888-242">Gibt ein einzelnes Element in der lokalen Client-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="19888-242">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="19888-243">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="19888-243">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="19888-244">Stellt ein Exchange-Element, das mit einem anderen Exchange-Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="19888-244">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="19888-245">Elemente</span><span class="sxs-lookup"><span data-stu-id="19888-245">Items</span></span>](items.md) <br/> |<span data-ttu-id="19888-246">Enthält ein Array von Elementen an.</span><span class="sxs-lookup"><span data-stu-id="19888-246">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="19888-247">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="19888-247">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="19888-248">Enthält ein Array von Elementen im Ordner zu erstellen, die durch das Element [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="19888-248">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="19888-249">SetItemField</span><span class="sxs-lookup"><span data-stu-id="19888-249">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="19888-250">Stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einer [UpdateItem Operation](updateitem-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="19888-250">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="19888-251">Update (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="19888-251">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="19888-252">Gibt ein einzelnes Element in den Speicher des lokalen Client aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="19888-252">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="19888-253">Textwert</span><span class="sxs-lookup"><span data-stu-id="19888-253">Text value</span></span>

<span data-ttu-id="19888-254">Keine.</span><span class="sxs-lookup"><span data-stu-id="19888-254">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="19888-255">Hinweise</span><span class="sxs-lookup"><span data-stu-id="19888-255">Remarks</span></span>

<span data-ttu-id="19888-256">Eine andere **Nachricht** -Element, [Nachricht (Verfügbarkeit)](message-availability.md) wird von der Verfügbarkeit Vorgänge zum OOF-Nachrichten zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="19888-256">Another **Message** element, [Message (Availability)](message-availability.md) is used by the Availability operations to return OOF messages.</span></span> 
  
<span data-ttu-id="19888-257">[Nachrichtenelemente](message-ex15websvcsotherref.md) darstellen, E-mail-Nachrichten und andere Elemente, die vom Exchange-Webdienste (EWS) Schema nicht stark typisiert sind.</span><span class="sxs-lookup"><span data-stu-id="19888-257">[Message](message-ex15websvcsotherref.md) elements represent e-mail messages and all other items that are not strongly typed by the Exchange Web Services (EWS) schema.</span></span> <span data-ttu-id="19888-258">Elemente wie IPM.Sharing- und IPM.InfoPath-Elemente werden als **Message**-Elemente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="19888-258">Items such as IPM.Sharing and IPM.InfoPath are returned as **Message** elements.</span></span> <span data-ttu-id="19888-259">Exchange 2010 werden keine das Basiselement **Element** in Antworten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="19888-259">Exchange 2010 does not return the base **Item** element in responses.</span></span> 
  
<span data-ttu-id="19888-260">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="19888-260">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="19888-261">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="19888-261">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19888-262">Namespace</span><span class="sxs-lookup"><span data-stu-id="19888-262">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="19888-263">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="19888-263">Schema Name</span></span>  <br/> |<span data-ttu-id="19888-264">Schematypen</span><span class="sxs-lookup"><span data-stu-id="19888-264">Types schema</span></span>  <br/> |
|<span data-ttu-id="19888-265">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="19888-265">Validation File</span></span>  <br/> |<span data-ttu-id="19888-266">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="19888-266">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="19888-267">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="19888-267">Can be Empty</span></span>  <br/> |<span data-ttu-id="19888-268">False</span><span class="sxs-lookup"><span data-stu-id="19888-268">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="19888-269">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19888-269">See also</span></span>



- [<span data-ttu-id="19888-270">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="19888-270">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

