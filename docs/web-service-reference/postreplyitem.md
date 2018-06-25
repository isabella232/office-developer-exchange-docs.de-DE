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
description: Das PostReplyItem-Element enthält eine Antwort auf eine Post-Element. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 70a0d6a7c670d0f16a55e66e7ef329331a04a5f8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830868"
---
# <a name="postreplyitem"></a><span data-ttu-id="0918b-104">PostReplyItem</span><span class="sxs-lookup"><span data-stu-id="0918b-104">PostReplyItem</span></span>

<span data-ttu-id="0918b-105">Das **PostReplyItem** -Element enthält eine Antwort auf eine Post-Element.</span><span class="sxs-lookup"><span data-stu-id="0918b-105">The **PostReplyItem** element contains a reply to a post item.</span></span> <span data-ttu-id="0918b-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0918b-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
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

 <span data-ttu-id="0918b-107">**PostReplyItemType**</span><span class="sxs-lookup"><span data-stu-id="0918b-107">**PostReplyItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0918b-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0918b-108">Attributes and elements</span></span>

<span data-ttu-id="0918b-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0918b-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0918b-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="0918b-110">Attributes</span></span>

<span data-ttu-id="0918b-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="0918b-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0918b-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0918b-112">Child elements</span></span>

|<span data-ttu-id="0918b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0918b-113">**Element**</span></span>|<span data-ttu-id="0918b-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0918b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0918b-115">' MimeContent '</span><span class="sxs-lookup"><span data-stu-id="0918b-115">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="0918b-116">Enthält den systemeigene Multipurpose Internet Mail Extensions (MIME) Stream eines Objekts, das im Format base64Binary dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="0918b-116">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="0918b-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="0918b-117">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="0918b-118">Enthält den eindeutigen Bezeichner und Ändern eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="0918b-118">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="0918b-119">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0918b-119">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="0918b-120">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="0918b-120">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="0918b-121">Stellt den Bezeichner des übergeordneten Ordners, der das Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="0918b-121">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="0918b-122">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0918b-122">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="0918b-123">ItemClass</span><span class="sxs-lookup"><span data-stu-id="0918b-123">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="0918b-124">Die Nachrichtenklasse eines Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="0918b-124">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="0918b-125">Betreff</span><span class="sxs-lookup"><span data-stu-id="0918b-125">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="0918b-126">Der Betreff den Exchange-Speicherelemente und Antwortobjekte darstellt.</span><span class="sxs-lookup"><span data-stu-id="0918b-126">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="0918b-127">Der Betreff ist auf 255 Zeichen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="0918b-127">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="0918b-128">Vertraulichkeit</span><span class="sxs-lookup"><span data-stu-id="0918b-128">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="0918b-129">Gibt die Vertraulichkeitsstufe eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="0918b-129">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="0918b-130">Body</span><span class="sxs-lookup"><span data-stu-id="0918b-130">Body</span></span>](body.md) <br/> |<span data-ttu-id="0918b-131">Stellt den tatsächlichen Textkörperinhalt einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="0918b-131">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="0918b-132">Anlagen</span><span class="sxs-lookup"><span data-stu-id="0918b-132">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="0918b-133">Enthält die Elemente oder Dateien, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0918b-133">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0918b-134">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="0918b-134">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="0918b-135">Stellt das Datum und die Uhrzeit, die ein Element in einem Postfach empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="0918b-135">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="0918b-136">Size</span><span class="sxs-lookup"><span data-stu-id="0918b-136">Size</span></span>](size.md) <br/> |<span data-ttu-id="0918b-137">Die Größe in Bytes eines Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="0918b-137">Represents the size in bytes of an item.</span></span> <span data-ttu-id="0918b-138">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0918b-138">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="0918b-139">Kategorien</span><span class="sxs-lookup"><span data-stu-id="0918b-139">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="0918b-140">Stellt eine Auflistung von Zeichenfolgen, die Kategorien zu identifizieren, zu denen ein Element im Postfach gehört.</span><span class="sxs-lookup"><span data-stu-id="0918b-140">Represents a collection of strings that identify categories to which an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="0918b-141">Importance</span><span class="sxs-lookup"><span data-stu-id="0918b-141">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="0918b-142">Beschreibt die Bedeutung eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="0918b-142">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="0918b-143">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="0918b-143">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="0918b-144">Stellt den Bezeichner des Elements, der dieses Element eine Antwort ist.</span><span class="sxs-lookup"><span data-stu-id="0918b-144">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="0918b-145">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="0918b-145">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="0918b-146">Gibt an, ob ein Element in den Standardordner Postausgang gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="0918b-146">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="0918b-147">IsDraft</span><span class="sxs-lookup"><span data-stu-id="0918b-147">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="0918b-148">Stellt dar, ob ein Element noch nicht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="0918b-148">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="0918b-149">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="0918b-149">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="0918b-150">Gibt an, ob ein Benutzer ein Element an sich gesendet.</span><span class="sxs-lookup"><span data-stu-id="0918b-150">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="0918b-151">IsResend</span><span class="sxs-lookup"><span data-stu-id="0918b-151">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="0918b-152">Gibt an, ob das Element zuvor gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="0918b-152">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="0918b-153">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="0918b-153">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="0918b-154">Gibt an, ob das Element geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="0918b-154">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="0918b-155">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="0918b-155">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="0918b-156">Stellt die Auflistung aller Internet Message Header, die in einem Element in einem Postfach enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="0918b-156">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="0918b-157">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="0918b-157">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="0918b-158">Stellt das Datum und die Uhrzeit, die ein Element in einem Postfach gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="0918b-158">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="0918b-159">"Datetimecreated"</span><span class="sxs-lookup"><span data-stu-id="0918b-159">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="0918b-160">Stellt das Datum und die Uhrzeit, die ein bestimmtes Element im Postfach erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0918b-160">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="0918b-161">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="0918b-161">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="0918b-162">Enthält eine Auflistung aller Antwort-Objekte, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0918b-162">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0918b-163">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="0918b-163">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="0918b-164">Stellt das Datum und die Uhrzeit bei des Ereignisses eintreten.</span><span class="sxs-lookup"><span data-stu-id="0918b-164">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="0918b-165">Dies wird durch die [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) -Element verwendet, um zu bestimmen, wann die Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0918b-165">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="0918b-166">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="0918b-166">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="0918b-167">Gibt an, ob eine Erinnerung für ein Element in der Exchange-Informationsspeicher festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="0918b-167">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0918b-168">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="0918b-168">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="0918b-169">Stellt die Anzahl der Minuten, bevor ein Ereignis, wenn eine Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0918b-169">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="0918b-170">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="0918b-170">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="0918b-171">Stellt die Zeichenfolge, die für den Inhalt der Cc-Zeile verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0918b-171">Represents the display string that is used for the contents of the Cc line.</span></span> <span data-ttu-id="0918b-172">Dies ist die verkettete Zeichenfolge alle Anzeigenamen der Cc-Empfänger.</span><span class="sxs-lookup"><span data-stu-id="0918b-172">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="0918b-173">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="0918b-173">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="0918b-174">Stellt die Zeichenfolge, die für den Inhalt des im Feld an verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0918b-174">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="0918b-175">Dies ist die verkettete Zeichenfolge aller in Empfänger Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="0918b-175">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="0918b-176">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="0918b-176">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="0918b-177">Stellt eine Eigenschaft, die auf **true** festgelegt ist, wenn ein Element eine Anlage enthält.</span><span class="sxs-lookup"><span data-stu-id="0918b-177">Represents a property that is set to **true** if an item has an attachment.</span></span> <span data-ttu-id="0918b-178">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0918b-178">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="0918b-179">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="0918b-179">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="0918b-180">Erweiterte Eigenschaften für Ordner und Elemente identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0918b-180">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="0918b-181">Kultur</span><span class="sxs-lookup"><span data-stu-id="0918b-181">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="0918b-182">Stellt die Kultur für ein bestimmtes Element in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="0918b-182">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="0918b-183">Absender</span><span class="sxs-lookup"><span data-stu-id="0918b-183">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="0918b-184">Bezeichnet den Absender eines Elements.</span><span class="sxs-lookup"><span data-stu-id="0918b-184">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="0918b-185">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="0918b-185">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="0918b-186">Enthält einen Satz an Empfänger einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="0918b-186">Contains a set of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="0918b-187">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="0918b-187">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="0918b-188">Stellt eine Auflistung der Empfänger dar, die eine Kopie der Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="0918b-188">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="0918b-189">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="0918b-189">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="0918b-190">Stellt eine Auflistung der Empfänger dar, die eine Blindkopie (Bcc) einer E-Mail erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="0918b-190">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="0918b-191">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="0918b-191">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="0918b-192">Gibt an, ob der Absender eines Elements eine lesebestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="0918b-192">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="0918b-193">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="0918b-193">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="0918b-194">Gibt an, ob der Absender eines Elements eine Empfangsbestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="0918b-194">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="0918b-195">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="0918b-195">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="0918b-196">Enthält eine binäre Kennung, die den Thread darstellt, zu dem diese Nachricht gehört.</span><span class="sxs-lookup"><span data-stu-id="0918b-196">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="0918b-197">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="0918b-197">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="0918b-198">Den Bezeichner für die Unterhaltung darstellt.</span><span class="sxs-lookup"><span data-stu-id="0918b-198">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="0918b-199">Von</span><span class="sxs-lookup"><span data-stu-id="0918b-199">From</span></span>](from.md) <br/> |<span data-ttu-id="0918b-200">Stellt die Adresse an, von der die Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="0918b-200">Represents the address from which the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="0918b-201">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="0918b-201">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="0918b-202">Die Internetnachricht-ID eines Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="0918b-202">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="0918b-203">IsRead</span><span class="sxs-lookup"><span data-stu-id="0918b-203">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="0918b-204">Gibt an, ob eine Nachricht gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="0918b-204">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="0918b-205">IsResponseRequested</span><span class="sxs-lookup"><span data-stu-id="0918b-205">IsResponseRequested</span></span>](isresponserequested.md) <br/> |<span data-ttu-id="0918b-206">Gibt an, ob eine Antwort auf eine E-mail-Nachricht angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="0918b-206">Indicates whether a response to an e-mail message is requested.</span></span>  <br/> |
|[<span data-ttu-id="0918b-207">Referenzen</span><span class="sxs-lookup"><span data-stu-id="0918b-207">References</span></span>](references.md) <br/> |<span data-ttu-id="0918b-208">Stellt die Usenet-Kopfzeile, die verwendet wird, die ihre ursprünglichen Nachrichten Antworten zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="0918b-208">Represents the Usenet header that is used to associate replies with their original messages.</span></span>  <br/> |
|[<span data-ttu-id="0918b-209">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="0918b-209">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="0918b-210">Identifiziert eine Reihe von Adressen, die an die Antworten gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0918b-210">Identifies a set of addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="0918b-211">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="0918b-211">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="0918b-212">Der Client Rechte basierend auf den berechtigungseinstellungen für das Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="0918b-212">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="0918b-213">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0918b-213">This element is read-only.</span></span> <span data-ttu-id="0918b-214">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0918b-214">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="0918b-215">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="0918b-215">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="0918b-216">Identifiziert den Delegaten in eine Access Stellvertreter-Szenario.</span><span class="sxs-lookup"><span data-stu-id="0918b-216">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="0918b-217">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0918b-217">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="0918b-218">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="0918b-218">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="0918b-219">Identifiziert den Prinzipal in einer Access Stellvertreter-Szenario.</span><span class="sxs-lookup"><span data-stu-id="0918b-219">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="0918b-220">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0918b-220">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="0918b-221">NewBodyContent</span><span class="sxs-lookup"><span data-stu-id="0918b-221">NewBodyContent</span></span>](newbodycontent.md) <br/> |<span data-ttu-id="0918b-222">Den neue Textkörperinhalt eines Post-Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="0918b-222">Represents the new body content of a post item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0918b-223">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0918b-223">Parent elements</span></span>

|<span data-ttu-id="0918b-224">**Element**</span><span class="sxs-lookup"><span data-stu-id="0918b-224">**Element**</span></span>|<span data-ttu-id="0918b-225">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0918b-225">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0918b-226">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="0918b-226">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="0918b-227">Werden alle Elemente, die an eine Besprechungszeit angrenzen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0918b-227">Describes all items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="0918b-228">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="0918b-228">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="0918b-229">Beschreibt alle Elemente, die mit einem bestimmten Zeitpunkt treffen in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="0918b-229">Describes all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="0918b-230">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="0918b-230">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="0918b-231">Enthält eine Auflistung aller Antwort-Objekte, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0918b-231">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0918b-232">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="0918b-232">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="0918b-233">Enthält ein Array von Elementen im Ordner zu erstellen, die durch das Element [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="0918b-233">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0918b-234">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0918b-234">Remarks</span></span>

<span data-ttu-id="0918b-235">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="0918b-235">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0918b-236">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0918b-236">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0918b-237">Namespace</span><span class="sxs-lookup"><span data-stu-id="0918b-237">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0918b-238">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0918b-238">Schema Name</span></span>  <br/> |<span data-ttu-id="0918b-239">Schematypen</span><span class="sxs-lookup"><span data-stu-id="0918b-239">Types schema</span></span>  <br/> |
|<span data-ttu-id="0918b-240">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0918b-240">Validation File</span></span>  <br/> |<span data-ttu-id="0918b-241">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0918b-241">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0918b-242">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0918b-242">Can be Empty</span></span>  <br/> |<span data-ttu-id="0918b-243">False</span><span class="sxs-lookup"><span data-stu-id="0918b-243">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0918b-244">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0918b-244">See also</span></span>



- [<span data-ttu-id="0918b-245">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0918b-245">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

