---
title: PostItem
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
description: Das PostItem-Element stellt ein Post-Element im Exchange-Informationsspeicher dar.
ms.openlocfilehash: 5fba1a9a6a3abc95ea2ce65cafa2b62bc7423f28
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528867"
---
# <a name="postitem"></a><span data-ttu-id="3e6bc-103">PostItem</span><span class="sxs-lookup"><span data-stu-id="3e6bc-103">PostItem</span></span>

<span data-ttu-id="3e6bc-104">Das **PostItem** -Element stellt ein Post-Element im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-104">The **PostItem** element represents a post item in the Exchange store.</span></span> 
  
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

 <span data-ttu-id="3e6bc-105">**PostItemType**</span><span class="sxs-lookup"><span data-stu-id="3e6bc-105">**PostItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3e6bc-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3e6bc-106">Attributes and elements</span></span>

<span data-ttu-id="3e6bc-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3e6bc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3e6bc-108">Attributes</span></span>

<span data-ttu-id="3e6bc-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3e6bc-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3e6bc-110">Child elements</span></span>

|<span data-ttu-id="3e6bc-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3e6bc-111">**Element**</span></span>|<span data-ttu-id="3e6bc-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3e6bc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3e6bc-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="3e6bc-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="3e6bc-114">Enthält den systemeigenen Multipurpose Internet Mail Extensions (MIME) Stream eines Objekts, das im base64Binary-Format dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="3e6bc-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="3e6bc-116">Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="3e6bc-117">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-118">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="3e6bc-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="3e6bc-119">Stellt den Bezeichner des übergeordneten Ordners dar, der das Element oder den Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="3e6bc-120">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="3e6bc-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="3e6bc-122">Stellt die Nachrichtenklasse eines Elements dar.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-123">Betreff</span><span class="sxs-lookup"><span data-stu-id="3e6bc-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="3e6bc-124">Stellt den Betreff für Exchange-Informationsspeicher Elemente und Response-Objekte dar.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="3e6bc-125">Der Betreff ist auf 255 Zeichen limitiert.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-126">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="3e6bc-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="3e6bc-127">Gibt die Empfindlichkeitsstufe eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-128">Body</span><span class="sxs-lookup"><span data-stu-id="3e6bc-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="3e6bc-129">Stellt den tatsächlichen Textinhalt einer Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-130">Anlagen</span><span class="sxs-lookup"><span data-stu-id="3e6bc-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="3e6bc-131">Enthält die Elemente oder Dateien, die an ein Element im Exchange-Informationsspeicher angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="3e6bc-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="3e6bc-133">Stellt das Datum und die Uhrzeit dar, zu denen ein Element in einem Postfach empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-133">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-134">Größe</span><span class="sxs-lookup"><span data-stu-id="3e6bc-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="3e6bc-135">Stellt die Größe eines Elements in Bytes dar.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="3e6bc-136">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-137">Kategorien</span><span class="sxs-lookup"><span data-stu-id="3e6bc-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="3e6bc-138">Stellt eine Auflistung von Zeichenfolgen dar, die die Kategorien identifizieren, zu denen ein Element im Postfach gehört.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-138">Represents a collection of strings that identify the categories to which an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-139">Importance</span><span class="sxs-lookup"><span data-stu-id="3e6bc-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="3e6bc-140">Beschreibt die Wichtigkeit eines Elements.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-141">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="3e6bc-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="3e6bc-142">Stellt den Bezeichner des Elements dar, zu dem dieses Element eine Antwort ist.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-143">Issubmitted</span><span class="sxs-lookup"><span data-stu-id="3e6bc-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="3e6bc-144">Gibt an, ob ein Element an den Standardordner Postausgang übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="3e6bc-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="3e6bc-146">Stellt dar, ob ein Element noch nicht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-147">Isfromme</span><span class="sxs-lookup"><span data-stu-id="3e6bc-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="3e6bc-148">Gibt an, ob ein Benutzer ein Element an sich selbst gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-148">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="3e6bc-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="3e6bc-150">Gibt an, ob das Element zuvor gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="3e6bc-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="3e6bc-152">Gibt an, ob das Element geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-153">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="3e6bc-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="3e6bc-154">Stellt die Auflistung aller Internet Nachrichtenkopfzeilen dar, die in einem Element in einem Postfach enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-154">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="3e6bc-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="3e6bc-156">Stellt das Datum und die Uhrzeit dar, zu denen ein Element in einem Postfach gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-157">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="3e6bc-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="3e6bc-158">Stellt das Datum und die Uhrzeit dar, zu der ein bestimmtes Element im Postfach erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="3e6bc-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="3e6bc-160">Enthält eine Auflistung aller Response-Objekte, die einem Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="3e6bc-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="3e6bc-162">Stellt das Datum und die Uhrzeit des Eintretens des Ereignisses dar.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="3e6bc-163">Dies wird vom [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) -Element verwendet, um zu bestimmen, wann die Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="3e6bc-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="3e6bc-165">Gibt an, ob für ein Element im Exchange-Informationsspeicher eine Erinnerung festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="3e6bc-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="3e6bc-167">Stellt die Anzahl von Minuten vor einem Ereignis dar, wenn eine Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-167">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="3e6bc-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="3e6bc-169">Stellt die Anzeigezeichenfolge dar, die für den Inhalt des Felds CC verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-169">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="3e6bc-170">Dies ist die verkettete Zeichenfolge aller Anzeigenamen des CC-Empfängers.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-170">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-171">Displayto ursprünglicher</span><span class="sxs-lookup"><span data-stu-id="3e6bc-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="3e6bc-172">Stellt die Anzeigezeichenfolge dar, die für den Inhalt des Felds an verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="3e6bc-173">Dies ist die verkettete Zeichenfolge aller in Empfänger Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="3e6bc-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="3e6bc-175">Stellt eine Eigenschaft dar, die auf **true** festgelegt ist, wenn ein Element mindestens eine Anlage aufweist.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-175">Represents a property that is set to **true** if an item has at least one attachment.</span></span> <span data-ttu-id="3e6bc-176">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-176">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-177">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="3e6bc-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="3e6bc-178">Erweiterte Eigenschaften für Ordner und Elemente identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-179">Kultur</span><span class="sxs-lookup"><span data-stu-id="3e6bc-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="3e6bc-180">Stellt die Kultur für ein bestimmtes Element in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-181">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="3e6bc-181">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="3e6bc-182">Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-182">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="3e6bc-183">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-183">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-184">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="3e6bc-184">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="3e6bc-185">Enthält den Anzeigenamen des letzten Benutzers, der ein Element ändern soll.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-185">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-186">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="3e6bc-186">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="3e6bc-187">Gibt an, wann ein Element zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-187">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-188">Isassociated</span><span class="sxs-lookup"><span data-stu-id="3e6bc-188">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="3e6bc-189">Gibt an, ob das Element einem Ordner zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-189">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-190">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="3e6bc-190">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="3e6bc-191">Stellt eine URL dar, die mit dem Microsoft Office Outlook Web App-Endpunkt verkettet werden soll, um ein Element in Outlook Web App zu lesen.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-191">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-192">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="3e6bc-192">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="3e6bc-193">Stellt eine URL dar, die mit dem Outlook Web App-Endpunkt verkettet werden soll, um ein Element in Outlook Web App zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-193">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-194">ConversationId</span><span class="sxs-lookup"><span data-stu-id="3e6bc-194">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="3e6bc-195">Enthält den Bezeichner eines Elements oder einer Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-195">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-196">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="3e6bc-196">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="3e6bc-197">Stellt ein HTML-Fragment oder nur-Text dar, der den eindeutigen Textkörper dieser Unterhaltung darstellt.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-197">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-198">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="3e6bc-198">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="3e6bc-199">Enthält eine binäre ID, die den Thread darstellt, zu dem diese Nachricht gehört.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-199">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-200">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="3e6bc-200">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="3e6bc-201">Stellt den Konversationsbezeichner dar.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-201">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-202">From</span><span class="sxs-lookup"><span data-stu-id="3e6bc-202">From</span></span>](from.md) <br/> |<span data-ttu-id="3e6bc-203">Stellt die Adresse dar, von der das Post-Element gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-203">Represents the address from which the post item was sent.</span></span> <span data-ttu-id="3e6bc-204">Das **from** -Element kann nur zum Zeitpunkt der Erstellung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-204">The **From** element can only be set at creation time.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-205">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="3e6bc-205">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="3e6bc-206">Stellt die Internet Nachrichten-ID eines Elements dar.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-206">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-207">IsRead</span><span class="sxs-lookup"><span data-stu-id="3e6bc-207">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="3e6bc-208">Gibt an, ob eine Nachricht gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-208">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-209">Gebucht</span><span class="sxs-lookup"><span data-stu-id="3e6bc-209">PostedTime</span></span>](postedtime.md) <br/> |<span data-ttu-id="3e6bc-210">Stellt die Uhrzeit dar, zu der ein [PostItem](postitem.md) bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-210">Represents the time that a [PostItem](postitem.md) was posted.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-211">References</span><span class="sxs-lookup"><span data-stu-id="3e6bc-211">References</span></span>](references.md) <br/> |<span data-ttu-id="3e6bc-212">Stellt den Usenet-Header dar, der zum Zuordnen von Antworten zu den ursprünglichen Nachrichten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-212">Represents the Usenet header that is used to associate replies with the original messages.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-213">Absender</span><span class="sxs-lookup"><span data-stu-id="3e6bc-213">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="3e6bc-214">Bezeichnet den Absender eines Elements.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-214">Identifies the sender of an item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3e6bc-215">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3e6bc-215">Parent elements</span></span>

|<span data-ttu-id="3e6bc-216">**Element**</span><span class="sxs-lookup"><span data-stu-id="3e6bc-216">**Element**</span></span>|<span data-ttu-id="3e6bc-217">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3e6bc-217">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3e6bc-218">SetItemField</span><span class="sxs-lookup"><span data-stu-id="3e6bc-218">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="3e6bc-219">Stellt eine Aktualisierung einer einzelnen Eigenschaft eines Elements in einer UpdateItem-Operation dar.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-219">Represents an update to a single property of an item in an UpdateItem operation.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-220">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="3e6bc-220">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="3e6bc-221">Identifiziert Daten, die während eines [UpdateItem-Vorgangs](updateitem-operation.md)an eine einzelne Eigenschaft eines Elements oder Ordners angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-221">Identifies data to append to a single property of an item or folder during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-222">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="3e6bc-222">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="3e6bc-223">Stellt ein Exchange-Element dar, das an ein anderes Exchange-Element angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-223">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-224">Erstellen (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="3e6bc-224">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="3e6bc-225">Identifiziert ein einzelnes Element, das im lokalen Clientspeicher erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-225">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-226">Update (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="3e6bc-226">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="3e6bc-227">Identifiziert ein einzelnes Element, das im lokalen Clientspeicher aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-227">Identifies a single item to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-228">ReadFlagChange</span><span class="sxs-lookup"><span data-stu-id="3e6bc-228">ReadFlagChange</span></span>](readflagchange.md) <br/> |<span data-ttu-id="3e6bc-229">Wird in [SyncFolderItems](syncfolderitems.md) -Antworten zurückgegeben, wenn ein Element gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-229">Returned in [SyncFolderItems](syncfolderitems.md) responses when an item has been read.</span></span> <span data-ttu-id="3e6bc-230">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-230">This property is read-only.</span></span> <span data-ttu-id="3e6bc-231">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-231">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-232">Elemente</span><span class="sxs-lookup"><span data-stu-id="3e6bc-232">Items</span></span>](items.md) <br/> |<span data-ttu-id="3e6bc-233">Enthält ein Array von Elementen.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-233">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-234">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="3e6bc-234">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="3e6bc-235">Identifiziert alle Elemente, die mit einer Besprechungszeit in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-235">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="3e6bc-236">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="3e6bc-236">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="3e6bc-237">Beschreibt alle Kalenderelemente, die an eine Besprechungszeit angrenzen.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-237">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3e6bc-238">Textwert</span><span class="sxs-lookup"><span data-stu-id="3e6bc-238">Text value</span></span>

<span data-ttu-id="3e6bc-239">Keine.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-239">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3e6bc-240">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e6bc-240">Remarks</span></span>

<span data-ttu-id="3e6bc-241">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3e6bc-241">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3e6bc-242">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3e6bc-242">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3e6bc-243">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e6bc-243">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3e6bc-244">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3e6bc-244">Schema Name</span></span>  <br/> |<span data-ttu-id="3e6bc-245">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3e6bc-245">Types schema</span></span>  <br/> |
|<span data-ttu-id="3e6bc-246">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3e6bc-246">Validation File</span></span>  <br/> |<span data-ttu-id="3e6bc-247">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3e6bc-247">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3e6bc-248">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3e6bc-248">Can be Empty</span></span>  <br/> |<span data-ttu-id="3e6bc-249">False</span><span class="sxs-lookup"><span data-stu-id="3e6bc-249">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3e6bc-250">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e6bc-250">See also</span></span>



- [<span data-ttu-id="3e6bc-251">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3e6bc-251">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

