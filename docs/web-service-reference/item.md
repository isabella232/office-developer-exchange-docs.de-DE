---
title: Element
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Item
api_type:
- schema
ms.assetid: 4dfe8f48-e7b4-444d-bdf9-a34e180f598b
description: Das Item-Element stellt ein generisches Element in der Exchange-Informationsspeicher dar.
ms.openlocfilehash: 72d8b1344bea3bcd105a0e293365b17f37193ac3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460316"
---
# <a name="item"></a><span data-ttu-id="7cef1-103">Element</span><span class="sxs-lookup"><span data-stu-id="7cef1-103">Item</span></span>

<span data-ttu-id="7cef1-104">Das **Item** -Element stellt ein generisches Element in der Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="7cef1-104">The **Item** element represents a generic item in the Exchange store.</span></span> 
  
```xml
<Item>
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
</Item>
```

 <span data-ttu-id="7cef1-105">**ItemType**</span><span class="sxs-lookup"><span data-stu-id="7cef1-105">**ItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7cef1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7cef1-106">Attributes and elements</span></span>

<span data-ttu-id="7cef1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7cef1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7cef1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7cef1-108">Attributes</span></span>

<span data-ttu-id="7cef1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7cef1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7cef1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7cef1-110">Child elements</span></span>

|<span data-ttu-id="7cef1-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="7cef1-111">**Element**</span></span>|<span data-ttu-id="7cef1-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7cef1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7cef1-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="7cef1-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="7cef1-114">Enthält den systemeigenen Multipurpose Internet Mail Extensions (MIME) Stream eines Objekts, das im base64Binary-Format dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7cef1-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="7cef1-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="7cef1-116">Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="7cef1-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="7cef1-117">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7cef1-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-118">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="7cef1-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="7cef1-119">Stellt den Bezeichner des übergeordneten Ordners dar, der das Element oder den Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="7cef1-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="7cef1-120">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7cef1-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="7cef1-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="7cef1-122">Stellt die Nachrichtenklasse eines Elements dar.</span><span class="sxs-lookup"><span data-stu-id="7cef1-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-123">Betreff</span><span class="sxs-lookup"><span data-stu-id="7cef1-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="7cef1-124">Stellt den Betreff für Exchange-Informationsspeicher Elemente und Response-Objekte dar.</span><span class="sxs-lookup"><span data-stu-id="7cef1-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="7cef1-125">Der Betreff ist auf 255 Zeichen limitiert.</span><span class="sxs-lookup"><span data-stu-id="7cef1-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-126">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="7cef1-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="7cef1-127">Gibt die Empfindlichkeitsstufe eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="7cef1-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-128">Body</span><span class="sxs-lookup"><span data-stu-id="7cef1-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="7cef1-129">Stellt den tatsächlichen Textinhalt einer Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="7cef1-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-130">Anlagen</span><span class="sxs-lookup"><span data-stu-id="7cef1-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="7cef1-131">Enthält die Elemente oder Dateien, die an ein Element im Exchange-Informationsspeicher angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="7cef1-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="7cef1-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="7cef1-133">Stellt das Datum und die Uhrzeit dar, zu denen ein Element in einem Postfach empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="7cef1-133">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-134">Größe</span><span class="sxs-lookup"><span data-stu-id="7cef1-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="7cef1-135">Stellt die Größe eines Elements in Bytes dar.</span><span class="sxs-lookup"><span data-stu-id="7cef1-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="7cef1-136">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7cef1-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-137">Kategorien</span><span class="sxs-lookup"><span data-stu-id="7cef1-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="7cef1-138">Stellt eine Auflistung von Zeichenfolgen dar, die ermitteln, zu welchen Kategorien ein Element im Postfach gehört.</span><span class="sxs-lookup"><span data-stu-id="7cef1-138">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-139">Importance</span><span class="sxs-lookup"><span data-stu-id="7cef1-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="7cef1-140">Beschreibt die Wichtigkeit eines Elements.</span><span class="sxs-lookup"><span data-stu-id="7cef1-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-141">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="7cef1-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="7cef1-142">Stellt den Bezeichner des Elements dar, zu dem dieses Element eine Antwort ist.</span><span class="sxs-lookup"><span data-stu-id="7cef1-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-143">Issubmitted</span><span class="sxs-lookup"><span data-stu-id="7cef1-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="7cef1-144">Gibt an, ob ein Element an den Standardordner Postausgang übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="7cef1-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="7cef1-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="7cef1-146">Stellt dar, ob ein Element noch nicht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7cef1-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-147">Isfromme</span><span class="sxs-lookup"><span data-stu-id="7cef1-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="7cef1-148">Gibt an, ob ein Benutzer ein Element an sich selbst gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="7cef1-148">Indicates whether a user sent an item to itself.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="7cef1-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="7cef1-150">Gibt an, ob das Element zuvor gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7cef1-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="7cef1-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="7cef1-152">Gibt an, ob das Element geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="7cef1-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-153">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="7cef1-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="7cef1-154">Stellt die Auflistung aller Internet Nachrichtenkopfzeilen dar, die in einem Element in einem Postfach enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7cef1-154">Represents the collection of all Internet message headers that are contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="7cef1-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="7cef1-156">Stellt das Datum und die Uhrzeit dar, zu denen ein Element in einem Postfach gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7cef1-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-157">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="7cef1-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="7cef1-158">Stellt das Datum und die Uhrzeit dar, zu der ein bestimmtes Element im Postfach erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7cef1-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="7cef1-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="7cef1-160">Enthält eine Auflistung aller Response-Objekte, die einem Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7cef1-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="7cef1-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="7cef1-162">Stellt das Datum und die Uhrzeit des Eintretens des Ereignisses dar.</span><span class="sxs-lookup"><span data-stu-id="7cef1-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="7cef1-163">Dies wird vom [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) -Element verwendet, um zu bestimmen, wann die Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7cef1-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="7cef1-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="7cef1-165">Gibt an, ob für ein Element im Exchange-Informationsspeicher eine Erinnerung festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="7cef1-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="7cef1-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="7cef1-167">Stellt die Anzahl von Minuten vor einem Ereignis dar, wenn eine Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7cef1-167">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="7cef1-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="7cef1-169">Stellt die Anzeigezeichenfolge dar, die für den Inhalt des Felds CC verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7cef1-169">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="7cef1-170">Dies ist die verkettete Zeichenfolge aller Anzeigenamen des CC-Empfängers.</span><span class="sxs-lookup"><span data-stu-id="7cef1-170">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-171">Displayto ursprünglicher</span><span class="sxs-lookup"><span data-stu-id="7cef1-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="7cef1-172">Stellt die Anzeigezeichenfolge dar, die für den Inhalt des Felds an verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7cef1-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="7cef1-173">Dies ist die verkettete Zeichenfolge aller in Empfänger Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="7cef1-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="7cef1-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="7cef1-175">Stellt eine Eigenschaft dar, die auf **true** festgelegt ist, wenn ein Element Anlagen mindestens eine sichtbare Anlage aufweist.</span><span class="sxs-lookup"><span data-stu-id="7cef1-175">Represents a property that is set to **true** if an item has attachments at least one visible attachment.</span></span> <span data-ttu-id="7cef1-176">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7cef1-176">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-177">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="7cef1-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="7cef1-178">Erweiterte Eigenschaften für Ordner und Elemente identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7cef1-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-179">Kultur</span><span class="sxs-lookup"><span data-stu-id="7cef1-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="7cef1-180">Stellt die Kultur für ein bestimmtes Element in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="7cef1-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-181">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="7cef1-181">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="7cef1-182">Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner.</span><span class="sxs-lookup"><span data-stu-id="7cef1-182">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="7cef1-183">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7cef1-183">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-184">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="7cef1-184">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="7cef1-185">Enthält den Anzeigenamen des letzten Benutzers, der ein Element ändern soll.</span><span class="sxs-lookup"><span data-stu-id="7cef1-185">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-186">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="7cef1-186">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="7cef1-187">Gibt an, wann ein Element zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="7cef1-187">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-188">Isassociated</span><span class="sxs-lookup"><span data-stu-id="7cef1-188">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="7cef1-189">Gibt an, ob das Element einem Ordner zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7cef1-189">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-190">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="7cef1-190">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="7cef1-191">Stellt eine URL dar, die mit dem Microsoft Office Outlook Web App-Endpunkt verkettet werden soll, um ein Element in Outlook Web App zu lesen.</span><span class="sxs-lookup"><span data-stu-id="7cef1-191">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-192">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="7cef1-192">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="7cef1-193">Stellt eine URL dar, die mit dem Outlook Web App-Endpunkt verkettet werden soll, um ein Element in Outlook Web App zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="7cef1-193">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-194">ConversationId</span><span class="sxs-lookup"><span data-stu-id="7cef1-194">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="7cef1-195">Enthält den Bezeichner eines Elements oder einer Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="7cef1-195">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-196">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="7cef1-196">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="7cef1-197">Stellt ein HTML-Fragment oder nur-Text dar, der den eindeutigen Textkörper dieser Unterhaltung darstellt.</span><span class="sxs-lookup"><span data-stu-id="7cef1-197">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7cef1-198">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7cef1-198">Parent elements</span></span>

|<span data-ttu-id="7cef1-199">**Element**</span><span class="sxs-lookup"><span data-stu-id="7cef1-199">**Element**</span></span>|<span data-ttu-id="7cef1-200">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7cef1-200">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7cef1-201">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="7cef1-201">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="7cef1-202">Beschreibt alle Kalenderelemente, die an eine Besprechungszeit angrenzen.</span><span class="sxs-lookup"><span data-stu-id="7cef1-202">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-203">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="7cef1-203">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="7cef1-204">Identifiziert Daten, die während eines [UpdateItem-Vorgangs](updateitem-operation.md)an eine einzelne Eigenschaft eines Elements/Ordners angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7cef1-204">Identifies data to append to a single property of an item/folder during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="7cef1-205">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="7cef1-205">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="7cef1-206">Identifiziert alle Elemente, die mit einer Besprechungszeit in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="7cef1-206">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-207">Erstellen (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="7cef1-207">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="7cef1-208">Identifiziert ein einzelnes Element, das im lokalen Clientspeicher erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7cef1-208">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-209">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="7cef1-209">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="7cef1-210">Stellt ein Exchange-Element dar, das an ein anderes Exchange-Element angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="7cef1-210">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-211">Items</span><span class="sxs-lookup"><span data-stu-id="7cef1-211">Items</span></span>](items.md) <br/> |<span data-ttu-id="7cef1-212">Enthält ein Array von Elementen.</span><span class="sxs-lookup"><span data-stu-id="7cef1-212">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-213">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="7cef1-213">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="7cef1-214">Enthält ein Array von Elementen, die in dem Ordner erstellt werden sollen, der durch das [parentfolderid (TargetFolderIdType)-](parentfolderid-targetfolderidtype.md) Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="7cef1-214">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="7cef1-215">SetItemField</span><span class="sxs-lookup"><span data-stu-id="7cef1-215">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="7cef1-216">Stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einer [UpdateItem Operation](updateitem-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="7cef1-216">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="7cef1-217">Update (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="7cef1-217">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="7cef1-218">Identifiziert ein einzelnes Element, das im lokalen Clientspeicher aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7cef1-218">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7cef1-219">Textwert</span><span class="sxs-lookup"><span data-stu-id="7cef1-219">Text value</span></span>

<span data-ttu-id="7cef1-220">Keine.</span><span class="sxs-lookup"><span data-stu-id="7cef1-220">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7cef1-221">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7cef1-221">Remarks</span></span>

<span data-ttu-id="7cef1-222">Beachten Sie, dass **ItemType** der Basistyp für [Task](task.md), [CalendarItem](calendaritem.md), [Contact](contact.md), [DistributionList](distributionlist.md)und [Message](message-ex15websvcsotherref.md)ist.</span><span class="sxs-lookup"><span data-stu-id="7cef1-222">It is important to note that **ItemType** is the base type for [Task](task.md), [CalendarItem](calendaritem.md), [Contact](contact.md), [DistributionList](distributionlist.md), and [Message](message-ex15websvcsotherref.md).</span></span>
  
<span data-ttu-id="7cef1-223">[Nachrichten](message-ex15websvcsotherref.md) Elemente stellen e-Mail-Nachrichten und alle anderen Elemente dar, die nicht stark vom Exchange-Webdienste Schema typisiert sind.</span><span class="sxs-lookup"><span data-stu-id="7cef1-223">[Message](message-ex15websvcsotherref.md) elements represent e-mail messages and all other items that are not strongly typed by the Exchange Web Services (EWS) schema.</span></span> <span data-ttu-id="7cef1-224">Elemente wie IPM.Sharing- und IPM.InfoPath-Elemente werden als **Message**-Elemente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7cef1-224">Items such as IPM.Sharing and IPM.InfoPath are returned as **Message** elements.</span></span> <span data-ttu-id="7cef1-225">Microsoft Exchange Server 2010 gibt nicht das Basis **Element** Element in Antworten zurück.</span><span class="sxs-lookup"><span data-stu-id="7cef1-225">Microsoft Exchange Server 2010 does not return the base **Item** element in responses.</span></span> 
  
<span data-ttu-id="7cef1-226">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7cef1-226">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7cef1-227">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7cef1-227">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7cef1-228">Namespace</span><span class="sxs-lookup"><span data-stu-id="7cef1-228">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7cef1-229">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7cef1-229">Schema Name</span></span>  <br/> |<span data-ttu-id="7cef1-230">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7cef1-230">Types schema</span></span>  <br/> |
|<span data-ttu-id="7cef1-231">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7cef1-231">Validation File</span></span>  <br/> |<span data-ttu-id="7cef1-232">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7cef1-232">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7cef1-233">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7cef1-233">Can be Empty</span></span>  <br/> |<span data-ttu-id="7cef1-234">False</span><span class="sxs-lookup"><span data-stu-id="7cef1-234">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7cef1-235">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7cef1-235">See also</span></span>



- [<span data-ttu-id="7cef1-236">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7cef1-236">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
  
[<span data-ttu-id="7cef1-237">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="7cef1-237">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

