---
title: PostReplyItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PostReplyItem
api_type:
- schema
ms.assetid: e5d93d63-0a3b-470f-9a94-2d57284c6745
description: Das PostReplyItem-Element enthält eine Antwort auf ein Post-Element. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 4104e79449acc6e358b729cf2de769d28dac52bd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461681"
---
# <a name="postreplyitem"></a><span data-ttu-id="ccf3f-104">PostReplyItem</span><span class="sxs-lookup"><span data-stu-id="ccf3f-104">PostReplyItem</span></span>

<span data-ttu-id="ccf3f-105">Das **PostReplyItem** -Element enthält eine Antwort auf ein Post-Element.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-105">The **PostReplyItem** element contains a reply to a post item.</span></span> <span data-ttu-id="ccf3f-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<PostReplyItem>
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
   <NewBodyContent/>
</PostReplyItem>
```

 <span data-ttu-id="ccf3f-107">**PostReplyItemType**</span><span class="sxs-lookup"><span data-stu-id="ccf3f-107">**PostReplyItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ccf3f-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ccf3f-108">Attributes and elements</span></span>

<span data-ttu-id="ccf3f-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ccf3f-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="ccf3f-110">Attributes</span></span>

<span data-ttu-id="ccf3f-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ccf3f-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ccf3f-112">Child elements</span></span>

|<span data-ttu-id="ccf3f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ccf3f-113">**Element**</span></span>|<span data-ttu-id="ccf3f-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ccf3f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ccf3f-115">MimeContent</span><span class="sxs-lookup"><span data-stu-id="ccf3f-115">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="ccf3f-116">Enthält den systemeigenen Multipurpose Internet Mail Extensions (MIME) Stream eines Objekts, das im base64Binary-Format dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-116">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="ccf3f-117">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="ccf3f-118">Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-118">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="ccf3f-119">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-119">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-120">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="ccf3f-120">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="ccf3f-121">Stellt den Bezeichner des übergeordneten Ordners dar, der das Element oder den Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-121">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="ccf3f-122">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-122">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-123">ItemClass</span><span class="sxs-lookup"><span data-stu-id="ccf3f-123">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="ccf3f-124">Stellt die Nachrichtenklasse eines Elements dar.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-124">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-125">Betreff</span><span class="sxs-lookup"><span data-stu-id="ccf3f-125">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="ccf3f-126">Stellt den Betreff für Exchange-Informationsspeicher Elemente und Response-Objekte dar.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-126">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="ccf3f-127">Der Betreff ist auf 255 Zeichen limitiert.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-127">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-128">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="ccf3f-128">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="ccf3f-129">Gibt die Empfindlichkeitsstufe eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-129">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-130">Body</span><span class="sxs-lookup"><span data-stu-id="ccf3f-130">Body</span></span>](body.md) <br/> |<span data-ttu-id="ccf3f-131">Stellt den tatsächlichen Textinhalt einer Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-131">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-132">Anlagen</span><span class="sxs-lookup"><span data-stu-id="ccf3f-132">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="ccf3f-133">Enthält die Elemente oder Dateien, die an ein Element im Exchange-Informationsspeicher angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-133">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-134">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="ccf3f-134">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="ccf3f-135">Stellt das Datum und die Uhrzeit dar, zu denen ein Element in einem Postfach empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-135">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-136">Größe</span><span class="sxs-lookup"><span data-stu-id="ccf3f-136">Size</span></span>](size.md) <br/> |<span data-ttu-id="ccf3f-137">Stellt die Größe eines Elements in Bytes dar.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-137">Represents the size in bytes of an item.</span></span> <span data-ttu-id="ccf3f-138">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-138">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-139">Kategorien</span><span class="sxs-lookup"><span data-stu-id="ccf3f-139">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="ccf3f-140">Stellt eine Auflistung von Zeichenfolgen dar, die Kategorien identifizieren, zu denen ein Element im Postfach gehört.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-140">Represents a collection of strings that identify categories to which an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-141">Importance</span><span class="sxs-lookup"><span data-stu-id="ccf3f-141">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="ccf3f-142">Beschreibt die Wichtigkeit eines Elements.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-142">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-143">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="ccf3f-143">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="ccf3f-144">Stellt den Bezeichner des Elements dar, zu dem dieses Element eine Antwort ist.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-144">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-145">Issubmitted</span><span class="sxs-lookup"><span data-stu-id="ccf3f-145">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="ccf3f-146">Gibt an, ob ein Element an den Standardordner Postausgang übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-146">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-147">IsDraft</span><span class="sxs-lookup"><span data-stu-id="ccf3f-147">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="ccf3f-148">Stellt dar, ob ein Element noch nicht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-148">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-149">Isfromme</span><span class="sxs-lookup"><span data-stu-id="ccf3f-149">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="ccf3f-150">Gibt an, ob ein Benutzer ein Element an sich selbst gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-150">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-151">IsResend</span><span class="sxs-lookup"><span data-stu-id="ccf3f-151">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="ccf3f-152">Gibt an, ob das Element zuvor gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-152">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-153">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="ccf3f-153">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="ccf3f-154">Gibt an, ob das Element geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-154">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-155">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="ccf3f-155">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="ccf3f-156">Stellt die Auflistung aller Internet Nachrichtenkopfzeilen dar, die in einem Element in einem Postfach enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-156">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-157">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="ccf3f-157">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="ccf3f-158">Stellt das Datum und die Uhrzeit dar, zu denen ein Element in einem Postfach gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-158">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-159">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="ccf3f-159">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="ccf3f-160">Stellt das Datum und die Uhrzeit dar, zu der ein bestimmtes Element im Postfach erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-160">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-161">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="ccf3f-161">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="ccf3f-162">Enthält eine Auflistung aller Response-Objekte, die einem Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-162">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-163">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="ccf3f-163">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="ccf3f-164">Stellt das Datum und die Uhrzeit des Eintretens des Ereignisses dar.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-164">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="ccf3f-165">Dies wird vom [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) -Element verwendet, um zu bestimmen, wann die Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-165">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-166">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="ccf3f-166">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="ccf3f-167">Gibt an, ob für ein Element im Exchange-Informationsspeicher eine Erinnerung festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-167">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-168">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="ccf3f-168">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="ccf3f-169">Stellt die Anzahl von Minuten vor einem Ereignis dar, wenn eine Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-169">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-170">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="ccf3f-170">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="ccf3f-171">Stellt die Anzeigezeichenfolge dar, die für den Inhalt der CC-Zeile verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-171">Represents the display string that is used for the contents of the Cc line.</span></span> <span data-ttu-id="ccf3f-172">Dies ist die verkettete Zeichenfolge aller Anzeigenamen des CC-Empfängers.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-172">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-173">Displayto ursprünglicher</span><span class="sxs-lookup"><span data-stu-id="ccf3f-173">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="ccf3f-174">Stellt die Anzeigezeichenfolge dar, die für den Inhalt des Felds an verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-174">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="ccf3f-175">Dies ist die verkettete Zeichenfolge aller in Empfänger Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-175">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-176">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="ccf3f-176">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="ccf3f-177">Stellt eine Eigenschaft dar, die auf **true** festgelegt ist, wenn ein Element eine Anlage aufweist.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-177">Represents a property that is set to **true** if an item has an attachment.</span></span> <span data-ttu-id="ccf3f-178">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-178">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-179">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="ccf3f-179">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="ccf3f-180">Erweiterte Eigenschaften für Ordner und Elemente identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-180">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-181">Kultur</span><span class="sxs-lookup"><span data-stu-id="ccf3f-181">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="ccf3f-182">Stellt die Kultur für ein bestimmtes Element in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-182">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-183">Absender</span><span class="sxs-lookup"><span data-stu-id="ccf3f-183">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="ccf3f-184">Bezeichnet den Absender eines Elements.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-184">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-185">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="ccf3f-185">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="ccf3f-186">Enthält eine Gruppe von Empfängern einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-186">Contains a set of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-187">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="ccf3f-187">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="ccf3f-188">Stellt eine Auflistung der Empfänger dar, die eine Kopie der Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-188">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-189">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="ccf3f-189">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="ccf3f-190">Stellt eine Auflistung der Empfänger dar, die eine Blindkopie (Bcc) einer E-Mail erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-190">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-191">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="ccf3f-191">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="ccf3f-192">Gibt an, ob der Absender eines Elements eine Lesebestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-192">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-193">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="ccf3f-193">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="ccf3f-194">Gibt an, ob der Absender eines Elements eine Zustellungsbestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-194">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-195">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="ccf3f-195">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="ccf3f-196">Enthält eine binäre ID, die den Thread darstellt, zu dem diese Nachricht gehört.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-196">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-197">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="ccf3f-197">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="ccf3f-198">Stellt den Konversationsbezeichner dar.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-198">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-199">From</span><span class="sxs-lookup"><span data-stu-id="ccf3f-199">From</span></span>](from.md) <br/> |<span data-ttu-id="ccf3f-200">Stellt die Adresse dar, von der die Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-200">Represents the address from which the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-201">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="ccf3f-201">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="ccf3f-202">Stellt die Internet Nachrichten-ID eines Elements dar.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-202">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-203">IsRead</span><span class="sxs-lookup"><span data-stu-id="ccf3f-203">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="ccf3f-204">Gibt an, ob eine Nachricht gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-204">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-205">IsResponseRequested</span><span class="sxs-lookup"><span data-stu-id="ccf3f-205">IsResponseRequested</span></span>](isresponserequested.md) <br/> |<span data-ttu-id="ccf3f-206">Gibt an, ob eine Antwort auf eine e-Mail-Nachricht angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-206">Indicates whether a response to an e-mail message is requested.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-207">References</span><span class="sxs-lookup"><span data-stu-id="ccf3f-207">References</span></span>](references.md) <br/> |<span data-ttu-id="ccf3f-208">Stellt den Usenet-Header dar, der verwendet wird, um Antworten mit ihren ursprünglichen Nachrichten zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-208">Represents the Usenet header that is used to associate replies with their original messages.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-209">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="ccf3f-209">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="ccf3f-210">Gibt eine Reihe von Adressen an, an die Antworten gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-210">Identifies a set of addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-211">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="ccf3f-211">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="ccf3f-212">Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-212">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="ccf3f-213">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-213">This element is read-only.</span></span> <span data-ttu-id="ccf3f-214">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-214">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-215">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="ccf3f-215">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="ccf3f-216">Identifiziert die Stellvertretung in einem Stellvertretungs-Zugriffs Szenario.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-216">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="ccf3f-217">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-217">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-218">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="ccf3f-218">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="ccf3f-219">Identifiziert den Prinzipal in einem Stellvertretungs-Zugriffs Szenario.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-219">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="ccf3f-220">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-220">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-221">NewBodyContent</span><span class="sxs-lookup"><span data-stu-id="ccf3f-221">NewBodyContent</span></span>](newbodycontent.md) <br/> |<span data-ttu-id="ccf3f-222">Stellt den neuen Textkörper Inhalt eines Beitrags Elements dar.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-222">Represents the new body content of a post item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ccf3f-223">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ccf3f-223">Parent elements</span></span>

|<span data-ttu-id="ccf3f-224">**Element**</span><span class="sxs-lookup"><span data-stu-id="ccf3f-224">**Element**</span></span>|<span data-ttu-id="ccf3f-225">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ccf3f-225">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ccf3f-226">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="ccf3f-226">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="ccf3f-227">Beschreibt alle Elemente, die an eine Besprechungszeit angrenzen.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-227">Describes all items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-228">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="ccf3f-228">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="ccf3f-229">Beschreibt alle Elemente, die mit einer Besprechungszeit in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-229">Describes all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-230">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="ccf3f-230">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="ccf3f-231">Enthält eine Auflistung aller Response-Objekte, die einem Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-231">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ccf3f-232">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="ccf3f-232">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="ccf3f-233">Enthält ein Array von Elementen, die in dem Ordner erstellt werden sollen, der durch das [parentfolderid (TargetFolderIdType)-](parentfolderid-targetfolderidtype.md) Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-233">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ccf3f-234">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ccf3f-234">Remarks</span></span>

<span data-ttu-id="ccf3f-235">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ccf3f-235">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ccf3f-236">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ccf3f-236">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ccf3f-237">Namespace</span><span class="sxs-lookup"><span data-stu-id="ccf3f-237">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ccf3f-238">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ccf3f-238">Schema Name</span></span>  <br/> |<span data-ttu-id="ccf3f-239">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ccf3f-239">Types schema</span></span>  <br/> |
|<span data-ttu-id="ccf3f-240">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ccf3f-240">Validation File</span></span>  <br/> |<span data-ttu-id="ccf3f-241">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ccf3f-241">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ccf3f-242">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ccf3f-242">Can be Empty</span></span>  <br/> |<span data-ttu-id="ccf3f-243">False</span><span class="sxs-lookup"><span data-stu-id="ccf3f-243">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ccf3f-244">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ccf3f-244">See also</span></span>



- [<span data-ttu-id="ccf3f-245">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ccf3f-245">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

