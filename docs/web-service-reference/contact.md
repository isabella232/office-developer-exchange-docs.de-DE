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
description: Das Kontakt-Element stellt ein Kontaktelement im Exchange-Speicher.
ms.openlocfilehash: 7b2e7c0197914c2a0a0ba3815dd05fca52a5f872
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757615"
---
# <a name="contact"></a><span data-ttu-id="d73d2-103">Kontakt</span><span class="sxs-lookup"><span data-stu-id="d73d2-103">Contact</span></span>

<span data-ttu-id="d73d2-104">**Wenden Sie sich an** -Element stellt ein Kontaktelement im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="d73d2-104">The **Contact** element represents a contact item in the Exchange store.</span></span> 
  
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

 <span data-ttu-id="d73d2-105">**ContactItemType**</span><span class="sxs-lookup"><span data-stu-id="d73d2-105">**ContactItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d73d2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d73d2-106">Attributes and elements</span></span>

<span data-ttu-id="d73d2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d73d2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d73d2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d73d2-108">Attributes</span></span>

<span data-ttu-id="d73d2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d73d2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d73d2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d73d2-110">Child elements</span></span>

|<span data-ttu-id="d73d2-111">**Elementname**</span><span class="sxs-lookup"><span data-stu-id="d73d2-111">**Element name**</span></span>|<span data-ttu-id="d73d2-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d73d2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d73d2-113">' MimeContent '</span><span class="sxs-lookup"><span data-stu-id="d73d2-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="d73d2-114">Enthält den systemeigene Multipurpose Internet Mail Extensions (MIME) Stream eines Objekts, das im Format base64Binary dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d73d2-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="d73d2-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="d73d2-116">Enthält den eindeutigen Bezeichner und Ändern eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="d73d2-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-117">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="d73d2-117">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="d73d2-118">Stellt den Bezeichner des übergeordneten Ordners, der das Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="d73d2-118">Represents the identifier of the parent folder that contains the item or folder.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-119">ItemClass</span><span class="sxs-lookup"><span data-stu-id="d73d2-119">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="d73d2-120">Die Nachrichtenklasse eines Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="d73d2-120">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-121">Betreff</span><span class="sxs-lookup"><span data-stu-id="d73d2-121">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="d73d2-122">Der Betreff den Exchange-Speicherelemente und Antwortobjekte darstellt.</span><span class="sxs-lookup"><span data-stu-id="d73d2-122">Represents the subject for Exchange store items and response objects.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-123">Vertraulichkeit</span><span class="sxs-lookup"><span data-stu-id="d73d2-123">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="d73d2-124">Gibt die Vertraulichkeitsstufe eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="d73d2-124">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-125">Body</span><span class="sxs-lookup"><span data-stu-id="d73d2-125">Body</span></span>](body.md) <br/> |<span data-ttu-id="d73d2-126">Stellt den tatsächlichen Textkörperinhalt einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d73d2-126">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-127">Anlagen</span><span class="sxs-lookup"><span data-stu-id="d73d2-127">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d73d2-128">Enthält die Elemente oder Dateien, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d73d2-128">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-129">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="d73d2-129">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="d73d2-130">Stellt das Datum und die Uhrzeit, die ein Element in einem Postfach empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="d73d2-130">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-131">Size</span><span class="sxs-lookup"><span data-stu-id="d73d2-131">Size</span></span>](size.md) <br/> |<span data-ttu-id="d73d2-132">Die Größe in Bytes eines Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="d73d2-132">Represents the size in bytes of an item.</span></span> <span data-ttu-id="d73d2-133">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d73d2-133">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-134">Kategorien</span><span class="sxs-lookup"><span data-stu-id="d73d2-134">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d73d2-135">Stellt eine Auflistung von Zeichenfolgen, die identifizieren, welche, die Kategorien ein Elements im Postfach gehört.</span><span class="sxs-lookup"><span data-stu-id="d73d2-135">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-136">Importance</span><span class="sxs-lookup"><span data-stu-id="d73d2-136">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="d73d2-137">Beschreibt die Bedeutung eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="d73d2-137">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-138">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="d73d2-138">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="d73d2-139">Stellt den Bezeichner des Elements, der dieses Element eine Antwort ist.</span><span class="sxs-lookup"><span data-stu-id="d73d2-139">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-140">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="d73d2-140">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="d73d2-141">Gibt an, ob ein Element in den Standardordner Postausgang gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d73d2-141">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-142">IsDraft</span><span class="sxs-lookup"><span data-stu-id="d73d2-142">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="d73d2-143">Stellt dar, ob ein Element noch nicht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d73d2-143">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-144">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="d73d2-144">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="d73d2-145">Gibt an, ob ein Benutzer ein Element auf sich selbst gesendet.</span><span class="sxs-lookup"><span data-stu-id="d73d2-145">Indicates whether a user sent an item to himself or herself.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-146">IsResend</span><span class="sxs-lookup"><span data-stu-id="d73d2-146">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="d73d2-147">Gibt an, ob das Element zuvor gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="d73d2-147">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-148">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="d73d2-148">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="d73d2-149">Gibt an, ob das Element geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="d73d2-149">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-150">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="d73d2-150">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="d73d2-151">Stellt die Auflistung aller Internet Message Header, die in einem Element in einem Postfach enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d73d2-151">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-152">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="d73d2-152">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="d73d2-153">Stellt das Datum und die Uhrzeit, die ein Element in einem Postfach gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d73d2-153">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-154">"Datetimecreated"</span><span class="sxs-lookup"><span data-stu-id="d73d2-154">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="d73d2-155">Stellt das Datum und die Uhrzeit, die ein bestimmtes Element im Postfach erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d73d2-155">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-156">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="d73d2-156">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="d73d2-157">Enthält eine Auflistung aller Antwort-Objekte, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d73d2-157">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-158">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="d73d2-158">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="d73d2-159">Stellt das Datum und die Uhrzeit bei des Ereignisses eintreten.</span><span class="sxs-lookup"><span data-stu-id="d73d2-159">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="d73d2-160">Dies wird durch die [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) -Element verwendet, um zu bestimmen, wann die Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d73d2-160">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-161">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="d73d2-161">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="d73d2-162">Gibt an, ob eine Erinnerung für ein Element in der Exchange-Informationsspeicher festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="d73d2-162">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-163">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="d73d2-163">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="d73d2-164">Stellt die Anzahl der Minuten, bevor ein Ereignis, wenn eine Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d73d2-164">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-165">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="d73d2-165">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="d73d2-166">Stellt die Zeichenfolge, die für den Inhalt der Cc-Zeile verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d73d2-166">Represents the display string that is used for the contents of the Cc line.</span></span> <span data-ttu-id="d73d2-167">Dies ist die verkettete Zeichenfolge alle Anzeigenamen der Cc-Empfänger.</span><span class="sxs-lookup"><span data-stu-id="d73d2-167">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-168">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="d73d2-168">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="d73d2-169">Stellt die Zeichenfolge, die für den Inhalt der Zeile verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d73d2-169">Represents the display string that is used for the contents of the To line.</span></span> <span data-ttu-id="d73d2-170">Dies ist die verkettete Zeichenfolge aller in Empfänger Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="d73d2-170">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-171">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="d73d2-171">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="d73d2-172">Stellt eine Eigenschaft, die auf **true** festgelegt ist, wenn ein Element mindestens eine Anlage sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="d73d2-172">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="d73d2-173">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d73d2-173">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-174">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="d73d2-174">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="d73d2-175">Erweiterte Eigenschaften für Ordner und Elemente identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d73d2-175">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-176">Kultur</span><span class="sxs-lookup"><span data-stu-id="d73d2-176">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="d73d2-177">Stellt die Kultur für ein bestimmtes Element in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="d73d2-177">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-178">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="d73d2-178">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="d73d2-179">Der Client Rechte basierend auf den berechtigungseinstellungen für das Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="d73d2-179">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="d73d2-180">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d73d2-180">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-181">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="d73d2-181">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="d73d2-182">Enthält den Anzeigenamen des Benutzers auf ein Element zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d73d2-182">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-183">ZuletztGeändertUm</span><span class="sxs-lookup"><span data-stu-id="d73d2-183">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="d73d2-184">Gibt an, wann ein Element zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="d73d2-184">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-185">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="d73d2-185">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="d73d2-186">Gibt an, ob das Element einem Ordner zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d73d2-186">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-187">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="d73d2-187">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="d73d2-188">Stellt eine URL zu verketten an den Microsoft Office Outlook Web App-Endpunkt ein Elements in Outlook Web App zu lesen.</span><span class="sxs-lookup"><span data-stu-id="d73d2-188">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-189">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="d73d2-189">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="d73d2-190">Stellt eine URL an den Endpunkt Outlook Web App so bearbeiten Sie ein Element in Outlook Web App verketten.</span><span class="sxs-lookup"><span data-stu-id="d73d2-190">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-191">ConversationId</span><span class="sxs-lookup"><span data-stu-id="d73d2-191">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="d73d2-192">Enthält die ID eines Elements oder einer Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="d73d2-192">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-193">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="d73d2-193">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="d73d2-194">Stellt ein HTML-Fragment oder nur-Text, der den eindeutigen Text an dieser Unterhaltung darstellt.</span><span class="sxs-lookup"><span data-stu-id="d73d2-194">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-195">FileAs</span><span class="sxs-lookup"><span data-stu-id="d73d2-195">FileAs</span></span>](fileas.md) <br/> |<span data-ttu-id="d73d2-196">Stellt dar, wie ein Kontakt im Ordner Kontakte vorgebracht wurde.</span><span class="sxs-lookup"><span data-stu-id="d73d2-196">Represents how a contact is filed in the Contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-197">FileAsMapping</span><span class="sxs-lookup"><span data-stu-id="d73d2-197">FileAsMapping</span></span>](fileasmapping.md) <br/> |<span data-ttu-id="d73d2-198">Definiert, wie erstellen, was für einen Kontakt angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d73d2-198">Defines how to construct what is displayed for a contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-199">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="d73d2-199">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="d73d2-200">Definiert den Anzeigenamen eines Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="d73d2-200">Defines the display name of a contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-201">Vorname</span><span class="sxs-lookup"><span data-stu-id="d73d2-201">GivenName</span></span>](givenname.md) <br/> |<span data-ttu-id="d73d2-202">Enthält den Namen eines Kontakts angegebenen.</span><span class="sxs-lookup"><span data-stu-id="d73d2-202">Contains a contact's given name.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-203">Initialen</span><span class="sxs-lookup"><span data-stu-id="d73d2-203">Initials</span></span>](initials.md) <br/> |<span data-ttu-id="d73d2-204">Stellt die Initialen eines Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="d73d2-204">Represents the initials of a contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-205">MiddleName</span><span class="sxs-lookup"><span data-stu-id="d73d2-205">MiddleName</span></span>](middlename.md) <br/> |<span data-ttu-id="d73d2-206">Stellt den Vornamen eines Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="d73d2-206">Represents the middle name of a contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-207">Spitzname</span><span class="sxs-lookup"><span data-stu-id="d73d2-207">Nickname</span></span>](nickname.md) <br/> |<span data-ttu-id="d73d2-208">Stellt den Spitznamen eines Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="d73d2-208">Represents the nickname of a contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-209">CompleteName</span><span class="sxs-lookup"><span data-stu-id="d73d2-209">CompleteName</span></span>](completename.md) <br/> |<span data-ttu-id="d73d2-210">Stellt den vollständigen Namen eines Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="d73d2-210">Represents the complete name of a contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-211">Firma</span><span class="sxs-lookup"><span data-stu-id="d73d2-211">CompanyName</span></span>](companyname.md) <br/> |<span data-ttu-id="d73d2-212">Stellt den Firmennamen, der einem Kontakt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d73d2-212">Represents the company name that is associated with a contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-213">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="d73d2-213">EmailAddresses</span></span>](emailaddresses.md) <br/> |<span data-ttu-id="d73d2-214">Stellt eine Auflistung von E-mail-Adressen für einen Kontakt.</span><span class="sxs-lookup"><span data-stu-id="d73d2-214">Represents a collection of e-mail addresses for a contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-215">PhysicalAddresses</span><span class="sxs-lookup"><span data-stu-id="d73d2-215">PhysicalAddresses</span></span>](physicaladdresses.md) <br/> |<span data-ttu-id="d73d2-216">Enthält eine Auflistung von physischen Adressen, die mit einem Kontakt verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="d73d2-216">Contains a collection of physical addresses that are associated with a contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-217">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="d73d2-217">PhoneNumbers</span></span>](phonenumbers.md) <br/> |<span data-ttu-id="d73d2-218">Stellt eine Auflistung von Telefonnummern für einen Kontakt.</span><span class="sxs-lookup"><span data-stu-id="d73d2-218">Represents a collection of telephone numbers for a contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-219">AssistantName</span><span class="sxs-lookup"><span data-stu-id="d73d2-219">AssistantName</span></span>](assistantname.md) <br/> |<span data-ttu-id="d73d2-220">Stellt dar, wenn ein Assistent einen Kontakt.</span><span class="sxs-lookup"><span data-stu-id="d73d2-220">Represents an assistant to a contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-221">Birthday</span><span class="sxs-lookup"><span data-stu-id="d73d2-221">Birthday</span></span>](birthday.md) <br/> |<span data-ttu-id="d73d2-222">Stellt das Geburtsdatum eines Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="d73d2-222">Represents the birth date of a contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-223">BusinessHomePage</span><span class="sxs-lookup"><span data-stu-id="d73d2-223">BusinessHomePage</span></span>](businesshomepage.md) <br/> |<span data-ttu-id="d73d2-224">Die Homepage (Webadresse) für den Kontakt darstellt.</span><span class="sxs-lookup"><span data-stu-id="d73d2-224">Represents the Home page (Web address) for the contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-225">Children</span><span class="sxs-lookup"><span data-stu-id="d73d2-225">Children</span></span>](children.md) <br/> |<span data-ttu-id="d73d2-226">Enthält die Namen der untergeordneten Elemente eines Kontakts.</span><span class="sxs-lookup"><span data-stu-id="d73d2-226">Contains the names of a contact's children.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-227">Companies</span><span class="sxs-lookup"><span data-stu-id="d73d2-227">Companies</span></span>](companies.md) <br/> |<span data-ttu-id="d73d2-228">Stellt die Auflistung der Unternehmen, die mit einem Kontakt verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="d73d2-228">Represents the collection of companies that are associated with a contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-229">ContactSource</span><span class="sxs-lookup"><span data-stu-id="d73d2-229">ContactSource</span></span>](contactsource.md) <br/> |<span data-ttu-id="d73d2-230">Beschreibt, ob der Kontakt in der Exchange-Speicher oder den Active Directory-Verzeichnisdienst befindet.</span><span class="sxs-lookup"><span data-stu-id="d73d2-230">Describes whether the contact is located in the Exchange store or the Active Directory directory service.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-231">Department</span><span class="sxs-lookup"><span data-stu-id="d73d2-231">Department</span></span>](department.md) <br/> |<span data-ttu-id="d73d2-232">Stellt die Abteilung des Kontakts im Büro.</span><span class="sxs-lookup"><span data-stu-id="d73d2-232">Represents the contact's department at work.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-233">Generierung</span><span class="sxs-lookup"><span data-stu-id="d73d2-233">Generation</span></span>](generation.md) <br/> |<span data-ttu-id="d73d2-234">Stellt eine generationsbasierten Abkürzung, die den vollständigen Namen eines Kontakts bildet.</span><span class="sxs-lookup"><span data-stu-id="d73d2-234">Represents a generational abbreviation that follows the full name of a contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-235">ImAddresses</span><span class="sxs-lookup"><span data-stu-id="d73d2-235">ImAddresses</span></span>](imaddresses.md) <br/> |<span data-ttu-id="d73d2-236">Stellt eine Auflistung von instant messaging-Adressen für einen Kontakt.</span><span class="sxs-lookup"><span data-stu-id="d73d2-236">Represents a collection of instant messaging addresses for a contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-237">JobTitle</span><span class="sxs-lookup"><span data-stu-id="d73d2-237">JobTitle</span></span>](jobtitle.md) <br/> |<span data-ttu-id="d73d2-238">Stellt die Position eines Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="d73d2-238">Represents the job title of a contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-239">Manager</span><span class="sxs-lookup"><span data-stu-id="d73d2-239">Manager</span></span>](manager.md) <br/> |<span data-ttu-id="d73d2-240">Stellt einen Kontakt-Manager.</span><span class="sxs-lookup"><span data-stu-id="d73d2-240">Represents a contact's manager.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-241">Mileage</span><span class="sxs-lookup"><span data-stu-id="d73d2-241">Mileage</span></span>](mileage.md) <br/> |<span data-ttu-id="d73d2-242">Mileage ein Kontaktelement darstellt.</span><span class="sxs-lookup"><span data-stu-id="d73d2-242">Represents mileage for a contact item.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-243">OfficeLocation</span><span class="sxs-lookup"><span data-stu-id="d73d2-243">OfficeLocation</span></span>](officelocation.md) <br/> |<span data-ttu-id="d73d2-244">Stellt den Bürostandort eines Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="d73d2-244">Represents the office location of a contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-245">PostalAddressIndex</span><span class="sxs-lookup"><span data-stu-id="d73d2-245">PostalAddressIndex</span></span>](postaladdressindex.md) <br/> |<span data-ttu-id="d73d2-246">Stellt die Anzeigetypen für physikalische Adressen an.</span><span class="sxs-lookup"><span data-stu-id="d73d2-246">Represents the display types for physical addresses.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-247">Profession</span><span class="sxs-lookup"><span data-stu-id="d73d2-247">Profession</span></span>](profession.md) <br/> |<span data-ttu-id="d73d2-248">Stellt den Beruf eines Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="d73d2-248">Represents the profession of a contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-249">SpouseName</span><span class="sxs-lookup"><span data-stu-id="d73d2-249">SpouseName</span></span>](spousename.md) <br/> |<span data-ttu-id="d73d2-250">Stellt den Namen des eines Kontakts Partner/in.</span><span class="sxs-lookup"><span data-stu-id="d73d2-250">Represents the name of a contact's spouse/partner.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-251">Nachname</span><span class="sxs-lookup"><span data-stu-id="d73d2-251">Surname</span></span>](surname.md) <br/> |<span data-ttu-id="d73d2-252">Stellt den Nachnamen eines Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="d73d2-252">Represents the surname of a contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-253">WeddingAnniversary</span><span class="sxs-lookup"><span data-stu-id="d73d2-253">WeddingAnniversary</span></span>](weddinganniversary.md) <br/> |<span data-ttu-id="d73d2-254">Enthält die Hochzeitstag eines Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="d73d2-254">Contains the wedding anniversary of a contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-255">HasPicture</span><span class="sxs-lookup"><span data-stu-id="d73d2-255">HasPicture</span></span>](haspicture.md) <br/> |<span data-ttu-id="d73d2-256">Gibt an, ob das Kontaktelement eine Dateianlage verfügt, die Bild für den Kontakt darstellt.</span><span class="sxs-lookup"><span data-stu-id="d73d2-256">Indicates whether the contact item has a file attachment that represents the contact's picture.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-257">PhoneticFullName</span><span class="sxs-lookup"><span data-stu-id="d73d2-257">PhoneticFullName</span></span>](phoneticfullname.md) <br/> |<span data-ttu-id="d73d2-258">Enthält den vollständigen Namen eines Kontakts, einschließlich des Namens vor- und Nachname, phonetisch geschrieben.</span><span class="sxs-lookup"><span data-stu-id="d73d2-258">Contains the full name of a contact, including the first and last name, spelled phonetically.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-259">PhoneticFirstName</span><span class="sxs-lookup"><span data-stu-id="d73d2-259">PhoneticFirstName</span></span>](phoneticfirstname.md) <br/> |<span data-ttu-id="d73d2-260">Enthält den Vornamen eines Kontakts phonetisch geschrieben.</span><span class="sxs-lookup"><span data-stu-id="d73d2-260">Contains the first name of a contact, spelled phonetically.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-261">PhoneticLastName</span><span class="sxs-lookup"><span data-stu-id="d73d2-261">PhoneticLastName</span></span>](phoneticlastname.md) <br/> |<span data-ttu-id="d73d2-262">Enthält den Nachnamen eines Kontakts phonetisch geschrieben.</span><span class="sxs-lookup"><span data-stu-id="d73d2-262">Contains the last name of a contact, spelled phonetically.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-263">Alias</span><span class="sxs-lookup"><span data-stu-id="d73d2-263">Alias</span></span>](alias.md) <br/> |<span data-ttu-id="d73d2-264">Enthält den e-Mail-Alias eines Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="d73d2-264">Contains the email alias of a contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-265">Notizen (Kontakt)</span><span class="sxs-lookup"><span data-stu-id="d73d2-265">Notes (Contact)</span></span>](notes-contact.md) <br/> |<span data-ttu-id="d73d2-266">Zusätzliche Kontaktinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="d73d2-266">Contains supplementary contact information.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-267">Photo</span><span class="sxs-lookup"><span data-stu-id="d73d2-267">Photo</span></span>](photo.md) <br/> |<span data-ttu-id="d73d2-268">Enthält einen Wert, der das Foto des Kontakts codiert.</span><span class="sxs-lookup"><span data-stu-id="d73d2-268">Contains a value that encodes the photo of a contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-269">UserSMIMECertificate</span><span class="sxs-lookup"><span data-stu-id="d73d2-269">UserSMIMECertificate</span></span>](usersmimecertificate.md) <br/> |<span data-ttu-id="d73d2-270">Enthält einen Wert, der das SMIME-Zertifikat eines Kontakts codiert.</span><span class="sxs-lookup"><span data-stu-id="d73d2-270">Contains a value that encodes the SMIME certificate of a contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-271">MSExchangeCertificate</span><span class="sxs-lookup"><span data-stu-id="d73d2-271">MSExchangeCertificate</span></span>](msexchangecertificate.md) <br/> |<span data-ttu-id="d73d2-272">Enthält einen Wert, der das Microsoft Exchange-Zertifikat eines Kontakts codiert.</span><span class="sxs-lookup"><span data-stu-id="d73d2-272">Contains a value that encodes the Microsoft Exchange certificate of a contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-273">DirectoryId</span><span class="sxs-lookup"><span data-stu-id="d73d2-273">DirectoryId</span></span>](directoryid.md) <br/> |<span data-ttu-id="d73d2-274">Enthält die Verzeichnis-ID eines Kontakts.</span><span class="sxs-lookup"><span data-stu-id="d73d2-274">Contains the directory ID of a contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-275">ManagerMailbox</span><span class="sxs-lookup"><span data-stu-id="d73d2-275">ManagerMailbox</span></span>](managermailbox.md) <br/> |<span data-ttu-id="d73d2-276">Enthält die SMTP-Informationen, die das Postfach Manager des Kontakts zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d73d2-276">Contains SMTP information that identifies the manager mailbox of the contact.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-277">DirectReports</span><span class="sxs-lookup"><span data-stu-id="d73d2-277">DirectReports</span></span>](directreports.md) <br/> |<span data-ttu-id="d73d2-278">Enthält die SMTP-Informationen, die die direkten Vorgesetzten eines Kontakts zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d73d2-278">Contains SMTP information that identifies the direct reports of a contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d73d2-279">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d73d2-279">Parent elements</span></span>

|<span data-ttu-id="d73d2-280">**Elementname**</span><span class="sxs-lookup"><span data-stu-id="d73d2-280">**Element name**</span></span>|<span data-ttu-id="d73d2-281">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d73d2-281">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d73d2-282">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="d73d2-282">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="d73d2-283">Werden alle Kalenderelemente, die an eine Besprechungszeit angrenzen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d73d2-283">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-284">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="d73d2-284">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="d73d2-285">Identifiziert Daten an eine einzelne Eigenschaft eines Elements oder Ordners während eines [Vorgangs UpdateItem](updateitem-operation.md)angefügt.</span><span class="sxs-lookup"><span data-stu-id="d73d2-285">Identifies data to append to a single property of an item or folder during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="d73d2-286">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="d73d2-286">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="d73d2-287">Identifiziert alle Elemente, die mit einem bestimmten Zeitpunkt treffen Konflikt</span><span class="sxs-lookup"><span data-stu-id="d73d2-287">Identifies all items that conflict with a meeting time</span></span>  <br/> |
|[<span data-ttu-id="d73d2-288">Erstellen (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="d73d2-288">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="d73d2-289">Gibt einen einzelnen Ordner im lokalen Client-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d73d2-289">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-290">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="d73d2-290">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="d73d2-291">Stellt ein Exchange-Element, das mit einem anderen Exchange-Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d73d2-291">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-292">Elemente</span><span class="sxs-lookup"><span data-stu-id="d73d2-292">Items</span></span>](items.md) <br/> |<span data-ttu-id="d73d2-293">Enthält ein Array von Elementen an.</span><span class="sxs-lookup"><span data-stu-id="d73d2-293">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-294">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="d73d2-294">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="d73d2-295">Enthält ein Array von Elementen im Ordner zu erstellen, die durch das Element [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="d73d2-295">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-296">Lösung</span><span class="sxs-lookup"><span data-stu-id="d73d2-296">Resolution</span></span>](resolution.md) <br/> |<span data-ttu-id="d73d2-297">Enthält eine einzelne aufgelöste Entität.</span><span class="sxs-lookup"><span data-stu-id="d73d2-297">Contains a single resolved entity.</span></span>  <br/> |
|[<span data-ttu-id="d73d2-298">SetItemField</span><span class="sxs-lookup"><span data-stu-id="d73d2-298">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="d73d2-299">Stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einer [UpdateItem Operation](updateitem-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="d73d2-299">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="d73d2-300">Update (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="d73d2-300">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="d73d2-301">Gibt ein einzelnes Element in den Speicher des lokalen Client aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d73d2-301">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d73d2-302">Textwert</span><span class="sxs-lookup"><span data-stu-id="d73d2-302">Text value</span></span>

<span data-ttu-id="d73d2-303">Keine.</span><span class="sxs-lookup"><span data-stu-id="d73d2-303">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d73d2-304">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d73d2-304">Remarks</span></span>

<span data-ttu-id="d73d2-305">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d73d2-305">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d73d2-306">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d73d2-306">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d73d2-307">Namespace</span><span class="sxs-lookup"><span data-stu-id="d73d2-307">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d73d2-308">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d73d2-308">Schema name</span></span>  <br/> |<span data-ttu-id="d73d2-309">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d73d2-309">Types schema</span></span>  <br/> |
|<span data-ttu-id="d73d2-310">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d73d2-310">Validation file</span></span>  <br/> |<span data-ttu-id="d73d2-311">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d73d2-311">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d73d2-312">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d73d2-312">Can be empty</span></span>  <br/> |<span data-ttu-id="d73d2-313">False</span><span class="sxs-lookup"><span data-stu-id="d73d2-313">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d73d2-314">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d73d2-314">See also</span></span>



- [<span data-ttu-id="d73d2-315">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d73d2-315">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="d73d2-316">Creating Contacts (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="d73d2-316">Creating Contacts (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[<span data-ttu-id="d73d2-317">Aktualisierung von Kontakten</span><span class="sxs-lookup"><span data-stu-id="d73d2-317">Updating Contacts</span></span>](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[<span data-ttu-id="d73d2-318">Deleting Contacts</span><span class="sxs-lookup"><span data-stu-id="d73d2-318">Deleting Contacts</span></span>](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

