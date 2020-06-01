---
title: Kontakt
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Contact
api_type:
- schema
ms.assetid: 66bfff50-7a91-4d81-b6a0-610b9962f677
description: Das Contact-Element stellt ein Kontaktelement im Exchange-Informationsspeicher dar.
ms.openlocfilehash: b5b4af211815dbbd09449ca2f3c6b6b2dfba6f93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44445650"
---
# <a name="contact"></a><span data-ttu-id="7146c-103">Kontakt</span><span class="sxs-lookup"><span data-stu-id="7146c-103">Contact</span></span>

<span data-ttu-id="7146c-104">Das **Contact** -Element stellt ein Kontaktelement im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="7146c-104">The **Contact** element represents a contact item in the Exchange store.</span></span> 
  
```XML
<Contact>
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
   <FileAs/>
   <FileAsMapping/>
   <DisplayName/>
   <GivenName/>
   <Initials/>
   <MiddleName/>
   <Nickname/>
   <CompleteName/>
   <CompanyName/>
   <EmailAddresses/>
   <PhysicalAddresses/>
   <PhoneNumbers/>
   <AssistantName/>
   <Birthday/>
   <BusinessHomePage/>
   <Children/>
   <Companies/>
   <ContactSource/>
   <Department/>
   <Generation/>
   <ImAddresses/>
   <JobTitle/>
   <Manager/>
   <Mileage/>
   <OfficeLocation/>
   <PostalAddressIndex/>
   <Profession/>
   <SpouseName/>
   <Surname/>
   <WeddingAnniversary/>
   <HasPicture/>
   <PhoneticFullName/>
   <PhoneticFirstName/>
   <PhoneticLastName/>
   <Alias/>
   <Notes/>
   <Photo/>
   <UserSMIMECertificate/>
   <MSExchangeCertificate/>
   <DirectoryId/>
   <ManagerMailbox/>
   <DirectReports/>
</Contact>
```

 <span data-ttu-id="7146c-105">**ContactItemType**</span><span class="sxs-lookup"><span data-stu-id="7146c-105">**ContactItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7146c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7146c-106">Attributes and elements</span></span>

<span data-ttu-id="7146c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7146c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7146c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7146c-108">Attributes</span></span>

<span data-ttu-id="7146c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7146c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7146c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7146c-110">Child elements</span></span>

|<span data-ttu-id="7146c-111">**Elementname**</span><span class="sxs-lookup"><span data-stu-id="7146c-111">**Element name**</span></span>|<span data-ttu-id="7146c-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7146c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7146c-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="7146c-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="7146c-114">Enthält den systemeigenen Multipurpose Internet Mail Extensions (MIME) Stream eines Objekts, das im base64Binary-Format dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7146c-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="7146c-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="7146c-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="7146c-116">Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="7146c-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7146c-117">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="7146c-117">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="7146c-118">Stellt den Bezeichner des übergeordneten Ordners dar, der das Element oder den Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="7146c-118">Represents the identifier of the parent folder that contains the item or folder.</span></span>  <br/> |
|[<span data-ttu-id="7146c-119">ItemClass</span><span class="sxs-lookup"><span data-stu-id="7146c-119">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="7146c-120">Stellt die Nachrichtenklasse eines Elements dar.</span><span class="sxs-lookup"><span data-stu-id="7146c-120">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="7146c-121">Betreff</span><span class="sxs-lookup"><span data-stu-id="7146c-121">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="7146c-122">Stellt den Betreff für Exchange-Informationsspeicher Elemente und Response-Objekte dar.</span><span class="sxs-lookup"><span data-stu-id="7146c-122">Represents the subject for Exchange store items and response objects.</span></span>  <br/> |
|[<span data-ttu-id="7146c-123">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="7146c-123">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="7146c-124">Gibt die Empfindlichkeitsstufe eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="7146c-124">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="7146c-125">Body</span><span class="sxs-lookup"><span data-stu-id="7146c-125">Body</span></span>](body.md) <br/> |<span data-ttu-id="7146c-126">Stellt den tatsächlichen Textinhalt einer Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="7146c-126">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="7146c-127">Anlagen</span><span class="sxs-lookup"><span data-stu-id="7146c-127">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="7146c-128">Enthält die Elemente oder Dateien, die an ein Element im Exchange-Informationsspeicher angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="7146c-128">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7146c-129">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="7146c-129">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="7146c-130">Stellt das Datum und die Uhrzeit dar, zu denen ein Element in einem Postfach empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="7146c-130">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="7146c-131">Größe</span><span class="sxs-lookup"><span data-stu-id="7146c-131">Size</span></span>](size.md) <br/> |<span data-ttu-id="7146c-132">Stellt die Größe eines Elements in Bytes dar.</span><span class="sxs-lookup"><span data-stu-id="7146c-132">Represents the size in bytes of an item.</span></span> <span data-ttu-id="7146c-133">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7146c-133">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="7146c-134">Kategorien</span><span class="sxs-lookup"><span data-stu-id="7146c-134">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="7146c-135">Stellt eine Auflistung von Zeichenfolgen dar, die ermitteln, zu welchen Kategorien ein Element im Postfach gehört.</span><span class="sxs-lookup"><span data-stu-id="7146c-135">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="7146c-136">Importance</span><span class="sxs-lookup"><span data-stu-id="7146c-136">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="7146c-137">Beschreibt die Wichtigkeit eines Elements.</span><span class="sxs-lookup"><span data-stu-id="7146c-137">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="7146c-138">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="7146c-138">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="7146c-139">Stellt den Bezeichner des Elements dar, zu dem dieses Element eine Antwort ist.</span><span class="sxs-lookup"><span data-stu-id="7146c-139">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="7146c-140">Issubmitted</span><span class="sxs-lookup"><span data-stu-id="7146c-140">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="7146c-141">Gibt an, ob ein Element an den Standardordner Postausgang übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="7146c-141">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="7146c-142">IsDraft</span><span class="sxs-lookup"><span data-stu-id="7146c-142">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="7146c-143">Stellt dar, ob ein Element noch nicht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7146c-143">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="7146c-144">Isfromme</span><span class="sxs-lookup"><span data-stu-id="7146c-144">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="7146c-145">Gibt an, ob ein Benutzer ein Element an sich selbst gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="7146c-145">Indicates whether a user sent an item to himself or herself.</span></span>  <br/> |
|[<span data-ttu-id="7146c-146">IsResend</span><span class="sxs-lookup"><span data-stu-id="7146c-146">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="7146c-147">Gibt an, ob das Element zuvor gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7146c-147">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="7146c-148">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="7146c-148">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="7146c-149">Gibt an, ob das Element geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="7146c-149">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="7146c-150">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="7146c-150">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="7146c-151">Stellt die Auflistung aller Internet Nachrichtenkopfzeilen dar, die in einem Element in einem Postfach enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7146c-151">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="7146c-152">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="7146c-152">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="7146c-153">Stellt das Datum und die Uhrzeit dar, zu denen ein Element in einem Postfach gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7146c-153">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="7146c-154">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="7146c-154">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="7146c-155">Stellt das Datum und die Uhrzeit dar, zu der ein bestimmtes Element im Postfach erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7146c-155">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="7146c-156">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="7146c-156">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="7146c-157">Enthält eine Auflistung aller Response-Objekte, die einem Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7146c-157">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7146c-158">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="7146c-158">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="7146c-159">Stellt das Datum und die Uhrzeit des Eintretens des Ereignisses dar.</span><span class="sxs-lookup"><span data-stu-id="7146c-159">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="7146c-160">Dies wird vom [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) -Element verwendet, um zu bestimmen, wann die Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7146c-160">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="7146c-161">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="7146c-161">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="7146c-162">Gibt an, ob für ein Element im Exchange-Informationsspeicher eine Erinnerung festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="7146c-162">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7146c-163">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="7146c-163">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="7146c-164">Stellt die Anzahl von Minuten vor einem Ereignis dar, wenn eine Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7146c-164">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="7146c-165">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="7146c-165">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="7146c-166">Stellt die Anzeigezeichenfolge dar, die für den Inhalt der CC-Zeile verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7146c-166">Represents the display string that is used for the contents of the Cc line.</span></span> <span data-ttu-id="7146c-167">Dies ist die verkettete Zeichenfolge aller Anzeigenamen des CC-Empfängers.</span><span class="sxs-lookup"><span data-stu-id="7146c-167">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="7146c-168">Displayto ursprünglicher</span><span class="sxs-lookup"><span data-stu-id="7146c-168">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="7146c-169">Stellt die Anzeigezeichenfolge dar, die für den Inhalt der an-Verbindung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7146c-169">Represents the display string that is used for the contents of the To line.</span></span> <span data-ttu-id="7146c-170">Dies ist die verkettete Zeichenfolge aller in Empfänger Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="7146c-170">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="7146c-171">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="7146c-171">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="7146c-172">Stellt eine Eigenschaft dar, die auf **true** festgelegt ist, wenn ein Element mindestens eine sichtbare Anlage aufweist.</span><span class="sxs-lookup"><span data-stu-id="7146c-172">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="7146c-173">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7146c-173">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="7146c-174">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="7146c-174">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="7146c-175">Erweiterte Eigenschaften für Ordner und Elemente identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7146c-175">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="7146c-176">Kultur</span><span class="sxs-lookup"><span data-stu-id="7146c-176">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="7146c-177">Stellt die Kultur für ein bestimmtes Element in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="7146c-177">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="7146c-178">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="7146c-178">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="7146c-179">Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner.</span><span class="sxs-lookup"><span data-stu-id="7146c-179">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="7146c-180">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7146c-180">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="7146c-181">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="7146c-181">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="7146c-182">Enthält den Anzeigenamen des letzten Benutzers, der ein Element ändern soll.</span><span class="sxs-lookup"><span data-stu-id="7146c-182">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="7146c-183">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="7146c-183">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="7146c-184">Gibt an, wann ein Element zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="7146c-184">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="7146c-185">Isassociated</span><span class="sxs-lookup"><span data-stu-id="7146c-185">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="7146c-186">Gibt an, ob das Element einem Ordner zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7146c-186">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="7146c-187">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="7146c-187">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="7146c-188">Stellt eine URL dar, die mit dem Microsoft Office Outlook Web App-Endpunkt verkettet werden soll, um ein Element in Outlook Web App zu lesen.</span><span class="sxs-lookup"><span data-stu-id="7146c-188">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="7146c-189">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="7146c-189">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="7146c-190">Stellt eine URL dar, die mit dem Outlook Web App-Endpunkt verkettet werden soll, um ein Element in Outlook Web App zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="7146c-190">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="7146c-191">ConversationId</span><span class="sxs-lookup"><span data-stu-id="7146c-191">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="7146c-192">Enthält den Bezeichner eines Elements oder einer Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="7146c-192">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="7146c-193">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="7146c-193">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="7146c-194">Stellt ein HTML-Fragment oder nur-Text dar, der den eindeutigen Textkörper dieser Unterhaltung darstellt.</span><span class="sxs-lookup"><span data-stu-id="7146c-194">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="7146c-195">FileAs</span><span class="sxs-lookup"><span data-stu-id="7146c-195">FileAs</span></span>](fileas.md) <br/> |<span data-ttu-id="7146c-196">Stellt dar, wie ein Kontakt im Ordner Kontakte gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="7146c-196">Represents how a contact is filed in the Contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="7146c-197">FileAsMapping</span><span class="sxs-lookup"><span data-stu-id="7146c-197">FileAsMapping</span></span>](fileasmapping.md) <br/> |<span data-ttu-id="7146c-198">Definiert, wie die für einen Kontakt angezeigte Anzeige erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7146c-198">Defines how to construct what is displayed for a contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-199">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="7146c-199">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="7146c-200">Definiert den Anzeigenamen eines Kontakts.</span><span class="sxs-lookup"><span data-stu-id="7146c-200">Defines the display name of a contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-201">GivenName</span><span class="sxs-lookup"><span data-stu-id="7146c-201">GivenName</span></span>](givenname.md) <br/> |<span data-ttu-id="7146c-202">Enthält den angegebenen Namen des Kontakts.</span><span class="sxs-lookup"><span data-stu-id="7146c-202">Contains a contact's given name.</span></span>  <br/> |
|[<span data-ttu-id="7146c-203">Initialen</span><span class="sxs-lookup"><span data-stu-id="7146c-203">Initials</span></span>](initials.md) <br/> |<span data-ttu-id="7146c-204">Stellt die Initialen eines Kontakts dar.</span><span class="sxs-lookup"><span data-stu-id="7146c-204">Represents the initials of a contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-205">MiddleName</span><span class="sxs-lookup"><span data-stu-id="7146c-205">MiddleName</span></span>](middlename.md) <br/> |<span data-ttu-id="7146c-206">Stellt den zweiten Vornamen eines Kontakts dar.</span><span class="sxs-lookup"><span data-stu-id="7146c-206">Represents the middle name of a contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-207">Spitzname</span><span class="sxs-lookup"><span data-stu-id="7146c-207">Nickname</span></span>](nickname.md) <br/> |<span data-ttu-id="7146c-208">Stellt den Spitznamen eines Kontakts dar.</span><span class="sxs-lookup"><span data-stu-id="7146c-208">Represents the nickname of a contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-209">Completename</span><span class="sxs-lookup"><span data-stu-id="7146c-209">CompleteName</span></span>](completename.md) <br/> |<span data-ttu-id="7146c-210">Stellt den vollständigen Namen eines Kontakts dar.</span><span class="sxs-lookup"><span data-stu-id="7146c-210">Represents the complete name of a contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-211">CompanyName</span><span class="sxs-lookup"><span data-stu-id="7146c-211">CompanyName</span></span>](companyname.md) <br/> |<span data-ttu-id="7146c-212">Stellt den Firmennamen dar, der einem Kontakt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7146c-212">Represents the company name that is associated with a contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-213">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="7146c-213">EmailAddresses</span></span>](emailaddresses.md) <br/> |<span data-ttu-id="7146c-214">Stellt eine Auflistung von e-Mail-Adressen für einen Kontakt dar.</span><span class="sxs-lookup"><span data-stu-id="7146c-214">Represents a collection of e-mail addresses for a contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-215">PhysicalAddresses</span><span class="sxs-lookup"><span data-stu-id="7146c-215">PhysicalAddresses</span></span>](physicaladdresses.md) <br/> |<span data-ttu-id="7146c-216">Enthält eine Auflistung von physikalischen Adressen, die einem Kontakt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7146c-216">Contains a collection of physical addresses that are associated with a contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-217">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="7146c-217">PhoneNumbers</span></span>](phonenumbers.md) <br/> |<span data-ttu-id="7146c-218">Stellt eine Auflistung von Telefonnummern für einen Kontakt dar.</span><span class="sxs-lookup"><span data-stu-id="7146c-218">Represents a collection of telephone numbers for a contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-219">AssistantName</span><span class="sxs-lookup"><span data-stu-id="7146c-219">AssistantName</span></span>](assistantname.md) <br/> |<span data-ttu-id="7146c-220">Stellt einen Assistenten für einen Kontakt dar.</span><span class="sxs-lookup"><span data-stu-id="7146c-220">Represents an assistant to a contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-221">Birthday</span><span class="sxs-lookup"><span data-stu-id="7146c-221">Birthday</span></span>](birthday.md) <br/> |<span data-ttu-id="7146c-222">Stellt das Geburtsdatum eines Kontakts dar.</span><span class="sxs-lookup"><span data-stu-id="7146c-222">Represents the birth date of a contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-223">BusinessHomePage</span><span class="sxs-lookup"><span data-stu-id="7146c-223">BusinessHomePage</span></span>](businesshomepage.md) <br/> |<span data-ttu-id="7146c-224">Stellt die Startseite (Webadresse) für den Kontakt dar.</span><span class="sxs-lookup"><span data-stu-id="7146c-224">Represents the Home page (Web address) for the contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-225">Children</span><span class="sxs-lookup"><span data-stu-id="7146c-225">Children</span></span>](children.md) <br/> |<span data-ttu-id="7146c-226">Enthält die Namen der untergeordneten Elemente eines Kontakts.</span><span class="sxs-lookup"><span data-stu-id="7146c-226">Contains the names of a contact's children.</span></span>  <br/> |
|[<span data-ttu-id="7146c-227">Companies</span><span class="sxs-lookup"><span data-stu-id="7146c-227">Companies</span></span>](companies.md) <br/> |<span data-ttu-id="7146c-228">Stellt die Auflistung von Unternehmen dar, die einem Kontakt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7146c-228">Represents the collection of companies that are associated with a contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-229">ContactSource</span><span class="sxs-lookup"><span data-stu-id="7146c-229">ContactSource</span></span>](contactsource.md) <br/> |<span data-ttu-id="7146c-230">Beschreibt, ob sich der Kontakt im Exchange-Informationsspeicher oder im Active Directory Verzeichnisdienst befindet.</span><span class="sxs-lookup"><span data-stu-id="7146c-230">Describes whether the contact is located in the Exchange store or the Active Directory directory service.</span></span>  <br/> |
|[<span data-ttu-id="7146c-231">Department</span><span class="sxs-lookup"><span data-stu-id="7146c-231">Department</span></span>](department.md) <br/> |<span data-ttu-id="7146c-232">Stellt die Abteilung des Kontakts bei der Arbeit dar.</span><span class="sxs-lookup"><span data-stu-id="7146c-232">Represents the contact's department at work.</span></span>  <br/> |
|[<span data-ttu-id="7146c-233">Erzeugung</span><span class="sxs-lookup"><span data-stu-id="7146c-233">Generation</span></span>](generation.md) <br/> |<span data-ttu-id="7146c-234">Stellt eine Generierungs Abkürzung dar, die dem vollständigen Namen eines Kontakts folgt.</span><span class="sxs-lookup"><span data-stu-id="7146c-234">Represents a generational abbreviation that follows the full name of a contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-235">Imaddresses</span><span class="sxs-lookup"><span data-stu-id="7146c-235">ImAddresses</span></span>](imaddresses.md) <br/> |<span data-ttu-id="7146c-236">Stellt eine Auflistung von Instant Messaging-Adressen für einen Kontakt dar.</span><span class="sxs-lookup"><span data-stu-id="7146c-236">Represents a collection of instant messaging addresses for a contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-237">JobTitle</span><span class="sxs-lookup"><span data-stu-id="7146c-237">JobTitle</span></span>](jobtitle.md) <br/> |<span data-ttu-id="7146c-238">Stellt die Position eines Kontakts dar.</span><span class="sxs-lookup"><span data-stu-id="7146c-238">Represents the job title of a contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-239">Manager</span><span class="sxs-lookup"><span data-stu-id="7146c-239">Manager</span></span>](manager.md) <br/> |<span data-ttu-id="7146c-240">Stellt den Vorgesetzten eines Kontakts dar.</span><span class="sxs-lookup"><span data-stu-id="7146c-240">Represents a contact's manager.</span></span>  <br/> |
|[<span data-ttu-id="7146c-241">Mileage</span><span class="sxs-lookup"><span data-stu-id="7146c-241">Mileage</span></span>](mileage.md) <br/> |<span data-ttu-id="7146c-242">Stellt die Kilometerleistung für ein Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="7146c-242">Represents mileage for a contact item.</span></span>  <br/> |
|[<span data-ttu-id="7146c-243">OfficeLocation</span><span class="sxs-lookup"><span data-stu-id="7146c-243">OfficeLocation</span></span>](officelocation.md) <br/> |<span data-ttu-id="7146c-244">Stellt die Office-Position eines Kontakts dar.</span><span class="sxs-lookup"><span data-stu-id="7146c-244">Represents the office location of a contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-245">PostalAddressIndex</span><span class="sxs-lookup"><span data-stu-id="7146c-245">PostalAddressIndex</span></span>](postaladdressindex.md) <br/> |<span data-ttu-id="7146c-246">Stellt die Anzeigetypen für physikalische Adressen dar.</span><span class="sxs-lookup"><span data-stu-id="7146c-246">Represents the display types for physical addresses.</span></span>  <br/> |
|[<span data-ttu-id="7146c-247">Profession</span><span class="sxs-lookup"><span data-stu-id="7146c-247">Profession</span></span>](profession.md) <br/> |<span data-ttu-id="7146c-248">Stellt den Beruf eines Kontakts dar.</span><span class="sxs-lookup"><span data-stu-id="7146c-248">Represents the profession of a contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-249">Ehepartnername</span><span class="sxs-lookup"><span data-stu-id="7146c-249">SpouseName</span></span>](spousename.md) <br/> |<span data-ttu-id="7146c-250">Stellt den Namen des Ehepartners/Partners eines Kontakts dar.</span><span class="sxs-lookup"><span data-stu-id="7146c-250">Represents the name of a contact's spouse/partner.</span></span>  <br/> |
|[<span data-ttu-id="7146c-251">Nachname</span><span class="sxs-lookup"><span data-stu-id="7146c-251">Surname</span></span>](surname.md) <br/> |<span data-ttu-id="7146c-252">Steht für den Namen eines Kontakts.</span><span class="sxs-lookup"><span data-stu-id="7146c-252">Represents the surname of a contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-253">WeddingAnniversary</span><span class="sxs-lookup"><span data-stu-id="7146c-253">WeddingAnniversary</span></span>](weddinganniversary.md) <br/> |<span data-ttu-id="7146c-254">Enthält das Hochzeitsjubiläum eines Kontakts.</span><span class="sxs-lookup"><span data-stu-id="7146c-254">Contains the wedding anniversary of a contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-255">HasPicture</span><span class="sxs-lookup"><span data-stu-id="7146c-255">HasPicture</span></span>](haspicture.md) <br/> |<span data-ttu-id="7146c-256">Gibt an, ob das Kontaktelement über eine Dateianlage verfügt, die das Bild des Kontakts darstellt.</span><span class="sxs-lookup"><span data-stu-id="7146c-256">Indicates whether the contact item has a file attachment that represents the contact's picture.</span></span>  <br/> |
|[<span data-ttu-id="7146c-257">PhoneticFullName</span><span class="sxs-lookup"><span data-stu-id="7146c-257">PhoneticFullName</span></span>](phoneticfullname.md) <br/> |<span data-ttu-id="7146c-258">Enthält den vollständigen Namen eines Kontakts, einschließlich des vor-und Nachnamens, phonetisch buchstabiert.</span><span class="sxs-lookup"><span data-stu-id="7146c-258">Contains the full name of a contact, including the first and last name, spelled phonetically.</span></span>  <br/> |
|[<span data-ttu-id="7146c-259">PhoneticFirstName</span><span class="sxs-lookup"><span data-stu-id="7146c-259">PhoneticFirstName</span></span>](phoneticfirstname.md) <br/> |<span data-ttu-id="7146c-260">Enthält den Vornamen eines Kontakts, der phonetisch buchstabiert ist.</span><span class="sxs-lookup"><span data-stu-id="7146c-260">Contains the first name of a contact, spelled phonetically.</span></span>  <br/> |
|[<span data-ttu-id="7146c-261">PhoneticLastName</span><span class="sxs-lookup"><span data-stu-id="7146c-261">PhoneticLastName</span></span>](phoneticlastname.md) <br/> |<span data-ttu-id="7146c-262">Enthält den Nachnamen eines Kontakts, der phonetisch buchstabiert ist.</span><span class="sxs-lookup"><span data-stu-id="7146c-262">Contains the last name of a contact, spelled phonetically.</span></span>  <br/> |
|[<span data-ttu-id="7146c-263">Alias</span><span class="sxs-lookup"><span data-stu-id="7146c-263">Alias</span></span>](alias.md) <br/> |<span data-ttu-id="7146c-264">Enthält den e-Mail-Alias eines Kontakts.</span><span class="sxs-lookup"><span data-stu-id="7146c-264">Contains the email alias of a contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-265">Hinweise (Kontakt)</span><span class="sxs-lookup"><span data-stu-id="7146c-265">Notes (Contact)</span></span>](notes-contact.md) <br/> |<span data-ttu-id="7146c-266">Enthält zusätzliche Kontaktinformationen.</span><span class="sxs-lookup"><span data-stu-id="7146c-266">Contains supplementary contact information.</span></span>  <br/> |
|[<span data-ttu-id="7146c-267">Foto</span><span class="sxs-lookup"><span data-stu-id="7146c-267">Photo</span></span>](photo.md) <br/> |<span data-ttu-id="7146c-268">Enthält einen Wert, der das Foto eines Kontakts codiert.</span><span class="sxs-lookup"><span data-stu-id="7146c-268">Contains a value that encodes the photo of a contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-269">UserSMIMECertificate</span><span class="sxs-lookup"><span data-stu-id="7146c-269">UserSMIMECertificate</span></span>](usersmimecertificate.md) <br/> |<span data-ttu-id="7146c-270">Enthält einen Wert, der das SMIME-Zertifikat eines Kontakts codiert.</span><span class="sxs-lookup"><span data-stu-id="7146c-270">Contains a value that encodes the SMIME certificate of a contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-271">MSExchangeCertificate</span><span class="sxs-lookup"><span data-stu-id="7146c-271">MSExchangeCertificate</span></span>](msexchangecertificate.md) <br/> |<span data-ttu-id="7146c-272">Enthält einen Wert, der das Microsoft Exchange Zertifikat eines Kontakts codiert.</span><span class="sxs-lookup"><span data-stu-id="7146c-272">Contains a value that encodes the Microsoft Exchange certificate of a contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-273">Verzeichnis-Nr</span><span class="sxs-lookup"><span data-stu-id="7146c-273">DirectoryId</span></span>](directoryid.md) <br/> |<span data-ttu-id="7146c-274">Enthält die Verzeichnis-ID eines Kontakts.</span><span class="sxs-lookup"><span data-stu-id="7146c-274">Contains the directory ID of a contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-275">Manager Mailbox</span><span class="sxs-lookup"><span data-stu-id="7146c-275">ManagerMailbox</span></span>](managermailbox.md) <br/> |<span data-ttu-id="7146c-276">Enthält SMTP-Informationen, die das Manager Postfach des Kontakts identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7146c-276">Contains SMTP information that identifies the manager mailbox of the contact.</span></span>  <br/> |
|[<span data-ttu-id="7146c-277">DirectReports</span><span class="sxs-lookup"><span data-stu-id="7146c-277">DirectReports</span></span>](directreports.md) <br/> |<span data-ttu-id="7146c-278">Enthält SMTP-Informationen, die die direkten Berichte eines Kontakts identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7146c-278">Contains SMTP information that identifies the direct reports of a contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7146c-279">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7146c-279">Parent elements</span></span>

|<span data-ttu-id="7146c-280">**Elementname**</span><span class="sxs-lookup"><span data-stu-id="7146c-280">**Element name**</span></span>|<span data-ttu-id="7146c-281">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7146c-281">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7146c-282">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="7146c-282">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="7146c-283">Beschreibt alle Kalenderelemente, die an eine Besprechungszeit angrenzen.</span><span class="sxs-lookup"><span data-stu-id="7146c-283">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="7146c-284">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="7146c-284">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="7146c-285">Identifiziert Daten, die während eines [UpdateItem-Vorgangs](updateitem-operation.md)an eine einzelne Eigenschaft eines Elements oder Ordners angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7146c-285">Identifies data to append to a single property of an item or folder during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="7146c-286">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="7146c-286">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="7146c-287">Identifiziert alle Elemente, die mit einer Besprechungszeit in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="7146c-287">Identifies all items that conflict with a meeting time</span></span>  <br/> |
|[<span data-ttu-id="7146c-288">Erstellen (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="7146c-288">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="7146c-289">Gibt einen einzelnen Ordner an, der im lokalen Clientspeicher erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7146c-289">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="7146c-290">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="7146c-290">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="7146c-291">Stellt ein Exchange-Element dar, das an ein anderes Exchange-Element angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="7146c-291">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="7146c-292">Items</span><span class="sxs-lookup"><span data-stu-id="7146c-292">Items</span></span>](items.md) <br/> |<span data-ttu-id="7146c-293">Enthält ein Array von Elementen.</span><span class="sxs-lookup"><span data-stu-id="7146c-293">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="7146c-294">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="7146c-294">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="7146c-295">Enthält ein Array von Elementen, die in dem Ordner erstellt werden sollen, der durch das [parentfolderid (TargetFolderIdType)-](parentfolderid-targetfolderidtype.md) Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="7146c-295">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="7146c-296">Lösung</span><span class="sxs-lookup"><span data-stu-id="7146c-296">Resolution</span></span>](resolution.md) <br/> |<span data-ttu-id="7146c-297">Enthält eine einzelne aufgelöste Entität.</span><span class="sxs-lookup"><span data-stu-id="7146c-297">Contains a single resolved entity.</span></span>  <br/> |
|[<span data-ttu-id="7146c-298">SetItemField</span><span class="sxs-lookup"><span data-stu-id="7146c-298">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="7146c-299">Stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einer [UpdateItem Operation](updateitem-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="7146c-299">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="7146c-300">Update (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="7146c-300">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="7146c-301">Identifiziert ein einzelnes Element, das im lokalen Clientspeicher aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7146c-301">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7146c-302">Textwert</span><span class="sxs-lookup"><span data-stu-id="7146c-302">Text value</span></span>

<span data-ttu-id="7146c-303">Keine.</span><span class="sxs-lookup"><span data-stu-id="7146c-303">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7146c-304">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7146c-304">Remarks</span></span>

<span data-ttu-id="7146c-305">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7146c-305">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7146c-306">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7146c-306">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7146c-307">Namespace</span><span class="sxs-lookup"><span data-stu-id="7146c-307">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7146c-308">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7146c-308">Schema name</span></span>  <br/> |<span data-ttu-id="7146c-309">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7146c-309">Types schema</span></span>  <br/> |
|<span data-ttu-id="7146c-310">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7146c-310">Validation file</span></span>  <br/> |<span data-ttu-id="7146c-311">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7146c-311">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7146c-312">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="7146c-312">Can be empty</span></span>  <br/> |<span data-ttu-id="7146c-313">False</span><span class="sxs-lookup"><span data-stu-id="7146c-313">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7146c-314">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7146c-314">See also</span></span>



- [<span data-ttu-id="7146c-315">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7146c-315">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="7146c-316">Creating Contacts (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="7146c-316">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[<span data-ttu-id="7146c-317">Aktualisieren von Kontakten</span><span class="sxs-lookup"><span data-stu-id="7146c-317">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[<span data-ttu-id="7146c-318">Deleting Contacts</span><span class="sxs-lookup"><span data-stu-id="7146c-318">Deleting Contacts</span></span>](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

