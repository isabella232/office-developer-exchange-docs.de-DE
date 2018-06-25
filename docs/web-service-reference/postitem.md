---
title: PostItem-Objekt
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PostItem
api_type:
- schema
ms.assetid: 7727ed84-9591-4a1c-bb04-12129926499b
description: Das PostItem-Element stellt ein Post-Element im Exchange-Speicher.
ms.openlocfilehash: 3fb6d6cfe334999c93ca0238547dd5aee8150a5f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830866"
---
# <a name="postitem"></a><span data-ttu-id="fa3fe-103">PostItem-Objekt</span><span class="sxs-lookup"><span data-stu-id="fa3fe-103">PostItem</span></span>

<span data-ttu-id="fa3fe-104">Das **PostItem** -Element stellt ein Post-Element im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-104">The **PostItem** element represents a post item in the Exchange store.</span></span> 
  
```xml
<PostItem>
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
   <ConversationIndex/>
   <ConversationTopic/>
   <From/>
   <InternetMessageId/>
   <IsRead/>
   <PostedTime/>
   <References/>
   <Sender/>
</PostItem>
```

 <span data-ttu-id="fa3fe-105">**PostItemType**</span><span class="sxs-lookup"><span data-stu-id="fa3fe-105">**PostItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fa3fe-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fa3fe-106">Attributes and elements</span></span>

<span data-ttu-id="fa3fe-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa3fe-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="fa3fe-108">Attributes</span></span>

<span data-ttu-id="fa3fe-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fa3fe-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fa3fe-110">Child elements</span></span>

|<span data-ttu-id="fa3fe-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="fa3fe-111">**Element**</span></span>|<span data-ttu-id="fa3fe-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fa3fe-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa3fe-113">' MimeContent '</span><span class="sxs-lookup"><span data-stu-id="fa3fe-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="fa3fe-114">Enthält den systemeigene Multipurpose Internet Mail Extensions (MIME) Stream eines Objekts, das im Format base64Binary dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="fa3fe-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="fa3fe-116">Enthält den eindeutigen Bezeichner und Ändern eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="fa3fe-117">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-118">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="fa3fe-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="fa3fe-119">Stellt den Bezeichner des übergeordneten Ordners, der das Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="fa3fe-120">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="fa3fe-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="fa3fe-122">Die Nachrichtenklasse eines Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-123">Betreff</span><span class="sxs-lookup"><span data-stu-id="fa3fe-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="fa3fe-124">Der Betreff den Exchange-Speicherelemente und Antwortobjekte darstellt.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="fa3fe-125">Der Betreff ist auf 255 Zeichen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-126">Vertraulichkeit</span><span class="sxs-lookup"><span data-stu-id="fa3fe-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="fa3fe-127">Gibt die Vertraulichkeitsstufe eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-128">Body</span><span class="sxs-lookup"><span data-stu-id="fa3fe-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="fa3fe-129">Stellt den tatsächlichen Textkörperinhalt einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-130">Anlagen</span><span class="sxs-lookup"><span data-stu-id="fa3fe-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="fa3fe-131">Enthält die Elemente oder Dateien, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="fa3fe-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="fa3fe-133">Stellt das Datum und die Uhrzeit, die ein Element in einem Postfach empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-133">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-134">Size</span><span class="sxs-lookup"><span data-stu-id="fa3fe-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="fa3fe-135">Die Größe in Bytes eines Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="fa3fe-136">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-137">Kategorien</span><span class="sxs-lookup"><span data-stu-id="fa3fe-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="fa3fe-138">Stellt eine Auflistung von Zeichenfolgen, die die Kategorien zu identifizieren, zu denen ein Element im Postfach gehört.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-138">Represents a collection of strings that identify the categories to which an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-139">Importance</span><span class="sxs-lookup"><span data-stu-id="fa3fe-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="fa3fe-140">Beschreibt die Bedeutung eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-141">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="fa3fe-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="fa3fe-142">Stellt den Bezeichner des Elements, der dieses Element eine Antwort ist.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="fa3fe-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="fa3fe-144">Gibt an, ob ein Element in den Standardordner Postausgang gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="fa3fe-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="fa3fe-146">Stellt dar, ob ein Element noch nicht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-147">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="fa3fe-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="fa3fe-148">Gibt an, ob ein Benutzer ein Element an sich gesendet.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-148">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="fa3fe-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="fa3fe-150">Gibt an, ob das Element zuvor gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="fa3fe-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="fa3fe-152">Gibt an, ob das Element geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-153">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="fa3fe-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="fa3fe-154">Stellt die Auflistung aller Internet Message Header, die in einem Element in einem Postfach enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-154">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="fa3fe-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="fa3fe-156">Stellt das Datum und die Uhrzeit, die ein Element in einem Postfach gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-157">"Datetimecreated"</span><span class="sxs-lookup"><span data-stu-id="fa3fe-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="fa3fe-158">Stellt das Datum und die Uhrzeit, die ein bestimmtes Element im Postfach erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="fa3fe-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="fa3fe-160">Enthält eine Auflistung aller Antwort-Objekte, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="fa3fe-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="fa3fe-162">Stellt das Datum und die Uhrzeit bei des Ereignisses eintreten.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="fa3fe-163">Dies wird durch die [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) -Element verwendet, um zu bestimmen, wann die Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="fa3fe-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="fa3fe-165">Gibt an, ob eine Erinnerung für ein Element in der Exchange-Informationsspeicher festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="fa3fe-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="fa3fe-167">Stellt die Anzahl der Minuten, bevor ein Ereignis, wenn eine Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-167">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="fa3fe-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="fa3fe-169">Stellt die Zeichenfolge, die für den Inhalt des im Feld "Cc" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-169">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="fa3fe-170">Dies ist die verkettete Zeichenfolge alle Anzeigenamen der Cc-Empfänger.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-170">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-171">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="fa3fe-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="fa3fe-172">Stellt die Zeichenfolge, die für den Inhalt des im Feld an verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="fa3fe-173">Dies ist die verkettete Zeichenfolge aller in Empfänger Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="fa3fe-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="fa3fe-175">Stellt eine Eigenschaft, die auf **true** festgelegt ist, wenn ein Element mindestens eine Anlage hat.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-175">Represents a property that is set to **true** if an item has at least one attachment.</span></span> <span data-ttu-id="fa3fe-176">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-176">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-177">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="fa3fe-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="fa3fe-178">Erweiterte Eigenschaften für Ordner und Elemente identifiziert.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-179">Kultur</span><span class="sxs-lookup"><span data-stu-id="fa3fe-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="fa3fe-180">Stellt die Kultur für ein bestimmtes Element in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-181">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="fa3fe-181">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="fa3fe-182">Der Client Rechte basierend auf den berechtigungseinstellungen für das Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-182">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="fa3fe-183">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-183">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-184">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="fa3fe-184">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="fa3fe-185">Enthält den Anzeigenamen des Benutzers auf ein Element zu ändern.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-185">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-186">ZuletztGeändertUm</span><span class="sxs-lookup"><span data-stu-id="fa3fe-186">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="fa3fe-187">Gibt an, wann ein Element zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-187">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-188">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="fa3fe-188">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="fa3fe-189">Gibt an, ob das Element einem Ordner zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-189">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-190">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="fa3fe-190">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="fa3fe-191">Stellt eine URL zu verketten an den Microsoft Office Outlook Web App-Endpunkt ein Elements in Outlook Web App zu lesen.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-191">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-192">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="fa3fe-192">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="fa3fe-193">Stellt eine URL an den Endpunkt Outlook Web App so bearbeiten Sie ein Element in Outlook Web App verketten.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-193">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-194">ConversationId</span><span class="sxs-lookup"><span data-stu-id="fa3fe-194">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="fa3fe-195">Enthält die ID eines Elements oder einer Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-195">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-196">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="fa3fe-196">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="fa3fe-197">Stellt ein HTML-Fragment oder nur-Text, der den eindeutigen Text an dieser Unterhaltung darstellt.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-197">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-198">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="fa3fe-198">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="fa3fe-199">Enthält eine binäre Kennung, die den Thread darstellt, zu dem diese Nachricht gehört.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-199">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-200">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="fa3fe-200">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="fa3fe-201">Den Bezeichner für die Unterhaltung darstellt.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-201">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-202">Von</span><span class="sxs-lookup"><span data-stu-id="fa3fe-202">From</span></span>](from.md) <br/> |<span data-ttu-id="fa3fe-203">Stellt die Adresse an, von der das Post-Element gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-203">Represents the address from which the post item was sent.</span></span> <span data-ttu-id="fa3fe-204">Das Element **von** kann nur zum Zeitpunkt der Erstellung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-204">The **From** element can only be set at creation time.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-205">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="fa3fe-205">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="fa3fe-206">Die Internetnachricht-ID eines Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-206">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-207">IsRead</span><span class="sxs-lookup"><span data-stu-id="fa3fe-207">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="fa3fe-208">Gibt an, ob eine Nachricht gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-208">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-209">PostedTime</span><span class="sxs-lookup"><span data-stu-id="fa3fe-209">PostedTime</span></span>](postedtime.md) <br/> |<span data-ttu-id="fa3fe-210">Gibt die Zeit, die ein [PostItem-Objekt](postitem.md) veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-210">Represents the time that a [PostItem](postitem.md) was posted.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-211">Referenzen</span><span class="sxs-lookup"><span data-stu-id="fa3fe-211">References</span></span>](references.md) <br/> |<span data-ttu-id="fa3fe-212">Stellt den Usenet-Header, der mit den ursprünglichen Nachrichten Antworten zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-212">Represents the Usenet header that is used to associate replies with the original messages.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-213">Absender</span><span class="sxs-lookup"><span data-stu-id="fa3fe-213">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="fa3fe-214">Bezeichnet den Absender eines Elements.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-214">Identifies the sender of an item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fa3fe-215">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fa3fe-215">Parent elements</span></span>

|<span data-ttu-id="fa3fe-216">**Element**</span><span class="sxs-lookup"><span data-stu-id="fa3fe-216">**Element**</span></span>|<span data-ttu-id="fa3fe-217">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fa3fe-217">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa3fe-218">SetItemField</span><span class="sxs-lookup"><span data-stu-id="fa3fe-218">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="fa3fe-219">Stellt eine Aktualisierung einer einzelnen Eigenschaft eines Elements in einer UpdateItem-Operation dar.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-219">Represents an update to a single property of an item in an UpdateItem operation.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-220">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="fa3fe-220">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="fa3fe-221">Identifiziert Daten an eine einzelne Eigenschaft eines Elements oder Ordners während eines [Vorgangs UpdateItem](updateitem-operation.md)angefügt.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-221">Identifies data to append to a single property of an item or folder during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-222">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="fa3fe-222">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="fa3fe-223">Stellt ein Exchange-Element, das mit einem anderen Exchange-Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-223">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-224">Erstellen (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="fa3fe-224">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="fa3fe-225">Gibt ein einzelnes Element in der lokalen Client-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-225">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-226">Update (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="fa3fe-226">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="fa3fe-227">Gibt ein einzelnes Element in den Speicher des lokalen Client aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-227">Identifies a single item to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-228">ReadFlagChange</span><span class="sxs-lookup"><span data-stu-id="fa3fe-228">ReadFlagChange</span></span>](readflagchange.md) <br/> |<span data-ttu-id="fa3fe-229">In [SyncFolderItems](syncfolderitems.md) Antworten zurückgegeben, wenn ein Element gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-229">Returned in [SyncFolderItems](syncfolderitems.md) responses when an item has been read.</span></span> <span data-ttu-id="fa3fe-230">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-230">This property is read-only.</span></span> <span data-ttu-id="fa3fe-231">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-231">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-232">Elemente</span><span class="sxs-lookup"><span data-stu-id="fa3fe-232">Items</span></span>](items.md) <br/> |<span data-ttu-id="fa3fe-233">Enthält ein Array von Elementen an.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-233">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-234">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="fa3fe-234">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="fa3fe-235">Identifiziert alle Elemente, die mit einem bestimmten Zeitpunkt treffen Konflikt.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-235">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="fa3fe-236">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="fa3fe-236">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="fa3fe-237">Werden alle Kalenderelemente, die an eine Besprechungszeit angrenzen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-237">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fa3fe-238">Textwert</span><span class="sxs-lookup"><span data-stu-id="fa3fe-238">Text value</span></span>

<span data-ttu-id="fa3fe-239">Keine.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-239">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fa3fe-240">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fa3fe-240">Remarks</span></span>

<span data-ttu-id="fa3fe-241">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-241">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fa3fe-242">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="fa3fe-242">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa3fe-243">Namespace</span><span class="sxs-lookup"><span data-stu-id="fa3fe-243">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fa3fe-244">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fa3fe-244">Schema Name</span></span>  <br/> |<span data-ttu-id="fa3fe-245">Schematypen</span><span class="sxs-lookup"><span data-stu-id="fa3fe-245">Types schema</span></span>  <br/> |
|<span data-ttu-id="fa3fe-246">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fa3fe-246">Validation File</span></span>  <br/> |<span data-ttu-id="fa3fe-247">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fa3fe-247">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fa3fe-248">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="fa3fe-248">Can be Empty</span></span>  <br/> |<span data-ttu-id="fa3fe-249">False</span><span class="sxs-lookup"><span data-stu-id="fa3fe-249">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fa3fe-250">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa3fe-250">See also</span></span>



- [<span data-ttu-id="fa3fe-251">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="fa3fe-251">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

