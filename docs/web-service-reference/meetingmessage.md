---
title: MeetingMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingMessage
api_type:
- schema
ms.assetid: c95956a8-7505-44b4-bea4-11d1f5182796
description: Das MeetingMessage-Element darstellt, eine Besprechung im Exchange-Speicher.
ms.openlocfilehash: a2e87bc9800ee1dc66c1a3110df76745ac7c05b6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830443"
---
# <a name="meetingmessage"></a><span data-ttu-id="1d691-103">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="1d691-103">MeetingMessage</span></span>

<span data-ttu-id="1d691-104">Das **MeetingMessage** -Element darstellt, eine Besprechung im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="1d691-104">The **MeetingMessage** element represents a meeting in the Exchange store.</span></span> 
  
```xml
<MeetingMessage>
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
   <LastModifiedName/>
   <LastModifiedTime/>
   <IsAssociated/>
   <WebClientReadFormQueryString/>
   <WebClientEditFormQueryString/>
   <ConversationId/>
   <UniqueBody/>
</MeetingMessage>
```

 <span data-ttu-id="1d691-105">**MeetingMessageType**</span><span class="sxs-lookup"><span data-stu-id="1d691-105">**MeetingMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1d691-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1d691-106">Attributes and elements</span></span>

<span data-ttu-id="1d691-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1d691-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1d691-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1d691-108">Attributes</span></span>

<span data-ttu-id="1d691-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1d691-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1d691-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1d691-110">Child elements</span></span>

|<span data-ttu-id="1d691-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1d691-111">**Element**</span></span>|<span data-ttu-id="1d691-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1d691-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1d691-113">' MimeContent '</span><span class="sxs-lookup"><span data-stu-id="1d691-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="1d691-114">Enthält den systemeigenen MIME-Stream eines Objekts, das im Format base64Binary dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="1d691-114">Contains the native MIME stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="1d691-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="1d691-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="1d691-116">Enthält den eindeutigen Bezeichner und Ändern eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="1d691-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="1d691-117">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1d691-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="1d691-118">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="1d691-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="1d691-119">Stellt den Bezeichner des übergeordneten Ordners, der das Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="1d691-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="1d691-120">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1d691-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="1d691-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="1d691-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="1d691-122">Die Nachrichtenklasse eines Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="1d691-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="1d691-123">Betreff</span><span class="sxs-lookup"><span data-stu-id="1d691-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="1d691-124">Der Betreff den Exchange-Speicherelemente und Antwortobjekte darstellt.</span><span class="sxs-lookup"><span data-stu-id="1d691-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="1d691-125">Der Betreff ist auf 255 Zeichen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="1d691-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="1d691-126">Vertraulichkeit</span><span class="sxs-lookup"><span data-stu-id="1d691-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="1d691-127">Enthält den Status für ein Element Vertraulichkeit.</span><span class="sxs-lookup"><span data-stu-id="1d691-127">Contains the status for an item's sensitivity.</span></span>  <br/> |
|[<span data-ttu-id="1d691-128">Body</span><span class="sxs-lookup"><span data-stu-id="1d691-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="1d691-129">Stellt den tatsächlichen Textkörperinhalt einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1d691-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="1d691-130">Anlagen</span><span class="sxs-lookup"><span data-stu-id="1d691-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="1d691-131">Enthält die Elemente oder Dateien, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1d691-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="1d691-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="1d691-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="1d691-133">Stellt das Datum und die Uhrzeit, die ein Element in einem Postfach empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="1d691-133">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="1d691-134">Size</span><span class="sxs-lookup"><span data-stu-id="1d691-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="1d691-135">Die Größe in Bytes eines Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="1d691-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="1d691-136">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1d691-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="1d691-137">Kategorien</span><span class="sxs-lookup"><span data-stu-id="1d691-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="1d691-138">Stellt eine Auflistung von Zeichenfolgen, die identifizieren, welche, die Kategorien ein Elements im Postfach gehört.</span><span class="sxs-lookup"><span data-stu-id="1d691-138">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="1d691-139">Importance</span><span class="sxs-lookup"><span data-stu-id="1d691-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="1d691-140">Beschreibt die Bedeutung eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="1d691-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="1d691-141">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="1d691-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="1d691-142">Stellt den Bezeichner des Elements, der dieses Element eine Antwort ist.</span><span class="sxs-lookup"><span data-stu-id="1d691-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="1d691-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="1d691-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="1d691-144">Gibt an, ob ein Element in den Standardordner Postausgang gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="1d691-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="1d691-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="1d691-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="1d691-146">Stellt dar, ob ein Element noch nicht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="1d691-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="1d691-147">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="1d691-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="1d691-148">Gibt an, ob ein Benutzer ein Element an sich gesendet.</span><span class="sxs-lookup"><span data-stu-id="1d691-148">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="1d691-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="1d691-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="1d691-150">Gibt an, ob das Element zuvor gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="1d691-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="1d691-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="1d691-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="1d691-152">Gibt an, ob das Element geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="1d691-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="1d691-153">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="1d691-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="1d691-154">Stellt die Auflistung aller Internet Message Header, die innerhalb eines Elements in einem Postfach enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="1d691-154">Represents the collection of all Internet message headers that are contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="1d691-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="1d691-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="1d691-156">Stellt das Datum und die Uhrzeit, die ein Element in einem Postfach gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="1d691-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="1d691-157">"Datetimecreated"</span><span class="sxs-lookup"><span data-stu-id="1d691-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="1d691-158">Stellt das Datum und die Uhrzeit, die ein bestimmtes Element im Postfach erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1d691-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="1d691-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="1d691-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="1d691-160">Enthält eine Auflistung aller Antwort-Objekte, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1d691-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="1d691-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="1d691-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="1d691-162">Stellt das Datum und die Uhrzeit bei des Ereignisses eintreten.</span><span class="sxs-lookup"><span data-stu-id="1d691-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="1d691-163">Dies wird durch die [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) -Element verwendet, um zu bestimmen, wann die Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1d691-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="1d691-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="1d691-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="1d691-165">Gibt an, ob eine Erinnerung für ein Element in der Exchange-Informationsspeicher festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="1d691-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="1d691-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="1d691-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="1d691-167">Stellt die Anzahl der Minuten, bevor ein Ereignis, wenn eine Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1d691-167">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="1d691-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="1d691-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="1d691-169">Stellt die Zeichenfolge, die für den Inhalt des im Feld "Cc" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1d691-169">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="1d691-170">Dies ist die verkettete Zeichenfolge alle Anzeigenamen der Cc-Empfänger.</span><span class="sxs-lookup"><span data-stu-id="1d691-170">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="1d691-171">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="1d691-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="1d691-172">Stellt die Zeichenfolge, die für den Inhalt des im Feld an verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1d691-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="1d691-173">Dies ist die verkettete Zeichenfolge aller in Empfänger Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="1d691-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="1d691-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="1d691-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="1d691-175">Stellt eine Eigenschaft, die auf **true** festgelegt ist, wenn ein Element mindestens eine Anlage sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="1d691-175">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="1d691-176">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1d691-176">This property is read only.</span></span>  <br/> |
|[<span data-ttu-id="1d691-177">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="1d691-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="1d691-178">Erweiterte Eigenschaften für Ordner und Elemente identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1d691-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="1d691-179">Kultur</span><span class="sxs-lookup"><span data-stu-id="1d691-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="1d691-180">Stellt die Kultur für ein bestimmtes Element in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="1d691-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="1d691-181">Absender</span><span class="sxs-lookup"><span data-stu-id="1d691-181">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="1d691-182">Bezeichnet den Absender eines Elements.</span><span class="sxs-lookup"><span data-stu-id="1d691-182">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="1d691-183">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="1d691-183">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="1d691-184">Enthält einen Satz an Empfänger einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1d691-184">Contains a set of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="1d691-185">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="1d691-185">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="1d691-186">Stellt eine Auflistung der Empfänger dar, die eine Kopie der Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="1d691-186">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="1d691-187">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="1d691-187">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="1d691-188">Stellt eine Auflistung der Empfänger dar, die eine Blindkopie (Bcc) einer E-Mail erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="1d691-188">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="1d691-189">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="1d691-189">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="1d691-190">Gibt an, ob der Absender eines Elements eine lesebestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="1d691-190">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="1d691-191">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="1d691-191">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="1d691-192">Gibt an, ob der Absender eines Elements eine Empfangsbestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="1d691-192">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="1d691-193">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="1d691-193">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="1d691-194">Enthält eine binäre Kennung, die den Thread darstellt, zu dem diese Nachricht gehört.</span><span class="sxs-lookup"><span data-stu-id="1d691-194">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="1d691-195">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="1d691-195">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="1d691-196">Den Bezeichner für die Unterhaltung darstellt.</span><span class="sxs-lookup"><span data-stu-id="1d691-196">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="1d691-197">Von</span><span class="sxs-lookup"><span data-stu-id="1d691-197">From</span></span>](from.md) <br/> |<span data-ttu-id="1d691-198">Stellt den Adressat dar, der die Nachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="1d691-198">Represents the addressee from whom the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="1d691-199">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="1d691-199">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="1d691-200">Die Internetnachricht-ID eines Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="1d691-200">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="1d691-201">IsRead</span><span class="sxs-lookup"><span data-stu-id="1d691-201">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="1d691-202">Gibt an, ob eine Nachricht gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="1d691-202">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="1d691-203">IsResponseRequested</span><span class="sxs-lookup"><span data-stu-id="1d691-203">IsResponseRequested</span></span>](isresponserequested.md) <br/> |<span data-ttu-id="1d691-204">Gibt an, ob eine Antwort auf eine E-mail-Nachricht angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="1d691-204">Indicates whether a response to an e-mail message is requested.</span></span>  <br/> |
|[<span data-ttu-id="1d691-205">Referenzen</span><span class="sxs-lookup"><span data-stu-id="1d691-205">References</span></span>](references.md) <br/> |<span data-ttu-id="1d691-206">Stellt den Usenet-Header, der zum Korrelieren Antworten mit ihrer ursprünglichen Nachrichten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1d691-206">Represents the Usenet header that is used to correlate replies with their original messages.</span></span>  <br/> |
|[<span data-ttu-id="1d691-207">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="1d691-207">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="1d691-208">Identifiziert eine Reihe von Adressen, die an die Antworten gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1d691-208">Identifies a set of addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="1d691-209">AssociatedCalendarItemId</span><span class="sxs-lookup"><span data-stu-id="1d691-209">AssociatedCalendarItemId</span></span>](associatedcalendaritemid.md) <br/> |<span data-ttu-id="1d691-210">Stellt das Kalenderelement, das eine [MeetingMessage](meetingmessage.md)zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1d691-210">Represents the calendar item that is associated with a [MeetingMessage](meetingmessage.md).</span></span>  <br/> |
|[<span data-ttu-id="1d691-211">IsDelegated</span><span class="sxs-lookup"><span data-stu-id="1d691-211">IsDelegated</span></span>](isdelegated.md) <br/> |<span data-ttu-id="1d691-212">Gibt an, ob eine Besprechung über ein Konto mit Stellvertretungszugriff behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="1d691-212">Indicates whether a meeting was handled by an account with delegate access.</span></span>  <br/> |
|[<span data-ttu-id="1d691-213">IsOutOfDate</span><span class="sxs-lookup"><span data-stu-id="1d691-213">IsOutOfDate</span></span>](isoutofdate.md) <br/> |<span data-ttu-id="1d691-214">Gibt an, ob eine Besprechungsnachricht veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="1d691-214">Indicates whether a meeting message is out-of-date.</span></span>  <br/> |
|[<span data-ttu-id="1d691-215">HasBeenProcessed</span><span class="sxs-lookup"><span data-stu-id="1d691-215">HasBeenProcessed</span></span>](hasbeenprocessed.md) <br/> |<span data-ttu-id="1d691-216">Gibt an, ob eine Besprechungsnachricht Element verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="1d691-216">Indicates whether a meeting message item has been processed.</span></span>  <br/> |
|[<span data-ttu-id="1d691-217">ResponseType</span><span class="sxs-lookup"><span data-stu-id="1d691-217">ResponseType</span></span>](responsetype.md) <br/> |<span data-ttu-id="1d691-218">Stellt den Typ der Empfänger für eine Besprechung zurückgegebenen Antwort.</span><span class="sxs-lookup"><span data-stu-id="1d691-218">Represents the type of recipient response received for a meeting.</span></span>  <br/> |
|[<span data-ttu-id="1d691-219">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="1d691-219">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="1d691-220">Der Client Rechte basierend auf den berechtigungseinstellungen für das Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="1d691-220">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="1d691-221">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1d691-221">This element is read-only.</span></span> <span data-ttu-id="1d691-222">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1d691-222">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="1d691-223">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="1d691-223">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="1d691-224">Enthält den Anzeigenamen des Benutzers auf ein Element zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1d691-224">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="1d691-225">ZuletztGeändertUm</span><span class="sxs-lookup"><span data-stu-id="1d691-225">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="1d691-226">Gibt an, wann ein Element zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="1d691-226">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="1d691-227">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="1d691-227">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="1d691-228">Gibt an, ob das Element einem Ordner zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1d691-228">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="1d691-229">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="1d691-229">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="1d691-230">Stellt eine URL zu verketten an den Microsoft Office Outlook Web App-Endpunkt ein Elements in Outlook Web App zu lesen.</span><span class="sxs-lookup"><span data-stu-id="1d691-230">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="1d691-231">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="1d691-231">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="1d691-232">Stellt eine URL an den Endpunkt Outlook Web App so bearbeiten Sie ein Element in Outlook Web App verketten.</span><span class="sxs-lookup"><span data-stu-id="1d691-232">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="1d691-233">ConversationId</span><span class="sxs-lookup"><span data-stu-id="1d691-233">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="1d691-234">Enthält die ID eines Elements oder einer Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="1d691-234">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="1d691-235">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="1d691-235">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="1d691-236">Stellt ein HTML-Fragment oder nur-Text, der den eindeutigen Text an dieser Unterhaltung darstellt.</span><span class="sxs-lookup"><span data-stu-id="1d691-236">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="1d691-237">UID</span><span class="sxs-lookup"><span data-stu-id="1d691-237">UID</span></span>](uid.md) <br/> |<span data-ttu-id="1d691-238">Ein Kalenderelement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1d691-238">Identifies a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="1d691-239">RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="1d691-239">RecurrenceId</span></span>](recurrenceid.md) <br/> |<span data-ttu-id="1d691-240">Verwendet, um eine bestimmte Instanz eines sich wiederholenden Kalenderelements zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="1d691-240">Used to identify a specific instance of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="1d691-241">DateTimeStamp</span><span class="sxs-lookup"><span data-stu-id="1d691-241">DateTimeStamp</span></span>](datetimestamp.md) <br/> |<span data-ttu-id="1d691-242">Gibt an, das Datum und die Uhrzeit der Erstellung eine Instanz eines iCalendar-Objekts.</span><span class="sxs-lookup"><span data-stu-id="1d691-242">Indicates the date and time that an instance of an iCalendar object was created.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1d691-243">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1d691-243">Parent elements</span></span>

|<span data-ttu-id="1d691-244">**Element**</span><span class="sxs-lookup"><span data-stu-id="1d691-244">**Element**</span></span>|<span data-ttu-id="1d691-245">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1d691-245">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1d691-246">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="1d691-246">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="1d691-247">Werden alle Kalenderelemente, die an eine Besprechungszeit angrenzen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1d691-247">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="1d691-248">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="1d691-248">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="1d691-249">Identifiziert Daten, die während einer [UpdateItem Operation](updateitem-operation.md) an eine einzelne Eigenschaft eines Elements angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1d691-249">Identifies data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="1d691-250">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="1d691-250">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="1d691-251">Identifiziert alle Elemente, die mit einem bestimmten Zeitpunkt treffen Konflikt.</span><span class="sxs-lookup"><span data-stu-id="1d691-251">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="1d691-252">Erstellen (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="1d691-252">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="1d691-253">Gibt ein einzelnes Element in der lokalen Client-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1d691-253">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="1d691-254">Update (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="1d691-254">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="1d691-255">Gibt ein einzelnes Element in den Speicher des lokalen Client aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1d691-255">Identifies a single item to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="1d691-256">Elemente</span><span class="sxs-lookup"><span data-stu-id="1d691-256">Items</span></span>](items.md) <br/> |<span data-ttu-id="1d691-257">Enthält ein Array von Elementen an.</span><span class="sxs-lookup"><span data-stu-id="1d691-257">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="1d691-258">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="1d691-258">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="1d691-259">Enthält ein Array von Elementen, die in den Ordner vom [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) -Element zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1d691-259">Contains an array of items to create in the folder identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="1d691-260">SetItemField</span><span class="sxs-lookup"><span data-stu-id="1d691-260">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="1d691-261">Stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einer [UpdateItem Operation](updateitem-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="1d691-261">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="1d691-262">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="1d691-262">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="1d691-263">Stellt ein Exchange-Element, das mit einem anderen Exchange-Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1d691-263">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1d691-264">Textwert</span><span class="sxs-lookup"><span data-stu-id="1d691-264">Text value</span></span>

<span data-ttu-id="1d691-265">Keine.</span><span class="sxs-lookup"><span data-stu-id="1d691-265">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1d691-266">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1d691-266">Remarks</span></span>

<span data-ttu-id="1d691-267">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1d691-267">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1d691-268">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1d691-268">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d691-269">Namespace</span><span class="sxs-lookup"><span data-stu-id="1d691-269">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1d691-270">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1d691-270">Schema Name</span></span>  <br/> |<span data-ttu-id="1d691-271">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1d691-271">Types schema</span></span>  <br/> |
|<span data-ttu-id="1d691-272">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1d691-272">Validation File</span></span>  <br/> |<span data-ttu-id="1d691-273">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1d691-273">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1d691-274">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1d691-274">Can be Empty</span></span>  <br/> |<span data-ttu-id="1d691-275">False</span><span class="sxs-lookup"><span data-stu-id="1d691-275">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1d691-276">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d691-276">See also</span></span>



- [<span data-ttu-id="1d691-277">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1d691-277">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

