---
title: DistributionList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DistributionList
api_type:
- schema
ms.assetid: f65aea01-e870-44a2-8571-fa6c001341cc
description: Das DistributionList-Element stellt eine Verteilerliste dar.
ms.openlocfilehash: 5eb97bef349ca02848f65fa58370b9c81c6653d0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457004"
---
# <a name="distributionlist"></a><span data-ttu-id="f2787-103">DistributionList</span><span class="sxs-lookup"><span data-stu-id="f2787-103">DistributionList</span></span>

<span data-ttu-id="f2787-104">Das **DistributionList** -Element stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="f2787-104">The **DistributionList** element represents a distribution list.</span></span> 
  
```xml
<DistributionList>
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
   <DisplayName/>
   <FileAs/>
   <ContactSource/>
   <Members/>
</DistributionList>
```

 <span data-ttu-id="f2787-105">**DistributionListType**</span><span class="sxs-lookup"><span data-stu-id="f2787-105">**DistributionListType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f2787-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f2787-106">Attributes and elements</span></span>

<span data-ttu-id="f2787-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f2787-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f2787-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f2787-108">Attributes</span></span>

<span data-ttu-id="f2787-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f2787-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f2787-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f2787-110">Child elements</span></span>

|<span data-ttu-id="f2787-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f2787-111">**Element**</span></span>|<span data-ttu-id="f2787-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f2787-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2787-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="f2787-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="f2787-114">Enthält den systemeigenen MIME-Stream eines im base64Binary-Format dargestellten Objekts.</span><span class="sxs-lookup"><span data-stu-id="f2787-114">Contains the native MIME stream of an object represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="f2787-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="f2787-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="f2787-116">Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Verteilerlisten Elements in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="f2787-116">Contains the unique identifier and change key of a distribution list item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f2787-117">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="f2787-117">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="f2787-118">Stellt den Bezeichner des übergeordneten Ordners dar, der das Verteilerlistenelement enthält.</span><span class="sxs-lookup"><span data-stu-id="f2787-118">Represents the identifier of the parent folder that contains the distribution list item.</span></span>  <br/> |
|[<span data-ttu-id="f2787-119">ItemClass</span><span class="sxs-lookup"><span data-stu-id="f2787-119">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="f2787-120">Stellt die Nachrichtenklasse eines Verteilerlisten Elements dar.</span><span class="sxs-lookup"><span data-stu-id="f2787-120">Represents the message class of a distribution list item.</span></span>  <br/> |
|[<span data-ttu-id="f2787-121">Betreff</span><span class="sxs-lookup"><span data-stu-id="f2787-121">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="f2787-122">Stellt den Betreff für Exchange-Informationsspeicher Elemente und Response-Objekte dar.</span><span class="sxs-lookup"><span data-stu-id="f2787-122">Represents the subject for Exchange store items and response objects.</span></span>  <br/> |
|[<span data-ttu-id="f2787-123">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="f2787-123">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="f2787-124">Enthält den Status für die Empfindlichkeit eines Verteilerlisten Elements.</span><span class="sxs-lookup"><span data-stu-id="f2787-124">Contains the status for a distribution list item's sensitivity.</span></span>  <br/> |
|[<span data-ttu-id="f2787-125">Body</span><span class="sxs-lookup"><span data-stu-id="f2787-125">Body</span></span>](body.md) <br/> |<span data-ttu-id="f2787-126">Stellt den tatsächlichen Textinhalt eines Verteilerlisten Elements dar.</span><span class="sxs-lookup"><span data-stu-id="f2787-126">Represents the actual body content of a distribution list item.</span></span>  <br/> |
|[<span data-ttu-id="f2787-127">Anlagen</span><span class="sxs-lookup"><span data-stu-id="f2787-127">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f2787-128">Enthält die Elemente oder Dateien, die an ein Verteilerlistenelement im Exchange-Informationsspeicher angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="f2787-128">Contains the items or files that are attached to a distribution list item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f2787-129">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="f2787-129">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="f2787-130">Stellt das Datum und die Uhrzeit des Empfangs eines Verteilerlisten Elements in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="f2787-130">Represents the date and time that a distribution list item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="f2787-131">Größe</span><span class="sxs-lookup"><span data-stu-id="f2787-131">Size</span></span>](size.md) <br/> |<span data-ttu-id="f2787-132">Stellt die Größe eines Verteilerlisten Elements in Bytes dar.</span><span class="sxs-lookup"><span data-stu-id="f2787-132">Represents the size, in bytes, of a distribution list item.</span></span> <span data-ttu-id="f2787-133">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f2787-133">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="f2787-134">Kategorien</span><span class="sxs-lookup"><span data-stu-id="f2787-134">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f2787-135">Stellt eine Auflistung von Zeichenfolgen dar, die ermitteln, zu welchen Kategorien ein Verteilerlistenelement im Postfach gehört.</span><span class="sxs-lookup"><span data-stu-id="f2787-135">Represents a collection of strings that identify to which categories a distribution list item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="f2787-136">Importance</span><span class="sxs-lookup"><span data-stu-id="f2787-136">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="f2787-137">Beschreibt die Wichtigkeit eines Verteilerlisten Elements.</span><span class="sxs-lookup"><span data-stu-id="f2787-137">Describes the importance of a distribution list item.</span></span>  <br/> |
|[<span data-ttu-id="f2787-138">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="f2787-138">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="f2787-139">Stellt den Bezeichner des Elements dar, für das dieses Element eine Antwort ist.</span><span class="sxs-lookup"><span data-stu-id="f2787-139">Represents the identifier of the item which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="f2787-140">Issubmitted</span><span class="sxs-lookup"><span data-stu-id="f2787-140">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="f2787-141">Gibt an, ob ein Element an den Standardordner Postausgang übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="f2787-141">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="f2787-142">IsDraft</span><span class="sxs-lookup"><span data-stu-id="f2787-142">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="f2787-143">Stellt dar, ob ein Element noch nicht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f2787-143">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="f2787-144">Isfromme</span><span class="sxs-lookup"><span data-stu-id="f2787-144">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="f2787-145">Gibt an, ob ein Benutzer ein Element an sich selbst gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="f2787-145">Indicates whether a user sent an item to itself.</span></span>  <br/> |
|[<span data-ttu-id="f2787-146">IsResend</span><span class="sxs-lookup"><span data-stu-id="f2787-146">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="f2787-147">Gibt an, ob das Element zuvor gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f2787-147">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="f2787-148">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="f2787-148">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="f2787-149">Gibt an, ob das Element geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="f2787-149">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="f2787-150">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="f2787-150">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="f2787-151">Stellt die Auflistung aller Internet Nachrichtenkopfzeilen dar, die in einem Element in einem Postfach enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="f2787-151">Represents the collection of all Internet message headers contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="f2787-152">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="f2787-152">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="f2787-153">Stellt das Datum und die Uhrzeit dar, zu denen ein Element in einem Postfach gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f2787-153">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="f2787-154">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="f2787-154">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="f2787-155">Stellt das Datum und die Uhrzeit dar, zu der ein bestimmtes Element im Postfach erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f2787-155">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="f2787-156">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="f2787-156">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="f2787-157">Enthält eine Auflistung aller Response-Objekte, die einem Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f2787-157">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f2787-158">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="f2787-158">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="f2787-159">Stellt das Datum und die Uhrzeit des Eintretens des Ereignisses dar.</span><span class="sxs-lookup"><span data-stu-id="f2787-159">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="f2787-160">Dies wird vom [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) -Element verwendet, um zu bestimmen, wann die Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f2787-160">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="f2787-161">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="f2787-161">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="f2787-162">Gibt an, ob für ein Element im Exchange-Informationsspeicher eine Erinnerung festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="f2787-162">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f2787-163">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="f2787-163">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="f2787-164">Stellt die Anzahl von Minuten vor einem Ereignis dar, wenn eine Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f2787-164">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="f2787-165">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="f2787-165">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="f2787-166">Stellt die Anzeigezeichenfolge dar, die für den Inhalt der CC-Zeile verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f2787-166">Represents the display string that is used for the contents of the Cc line.</span></span> <span data-ttu-id="f2787-167">Dies ist die verkettete Zeichenfolge aller Anzeigenamen des CC-Empfängers.</span><span class="sxs-lookup"><span data-stu-id="f2787-167">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="f2787-168">Displayto ursprünglicher</span><span class="sxs-lookup"><span data-stu-id="f2787-168">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="f2787-169">Stellt die Anzeigezeichenfolge dar, die für den Inhalt der an-Verbindung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f2787-169">Represents the display string that is used for the contents of the To line.</span></span> <span data-ttu-id="f2787-170">Dies ist die verkettete Zeichenfolge aller in Empfänger Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="f2787-170">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="f2787-171">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="f2787-171">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="f2787-172">Stellt eine Eigenschaft dar, die auf **true** festgelegt ist, wenn ein Element mindestens eine sichtbare Anlage aufweist.</span><span class="sxs-lookup"><span data-stu-id="f2787-172">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="f2787-173">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f2787-173">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="f2787-174">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="f2787-174">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="f2787-175">Identifiziert erweiterte Eigenschaften für ein Verteilerlistenelement.</span><span class="sxs-lookup"><span data-stu-id="f2787-175">Identifies extended properties on a distribution list item.</span></span>  <br/> |
|[<span data-ttu-id="f2787-176">Kultur</span><span class="sxs-lookup"><span data-stu-id="f2787-176">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="f2787-177">Stellt die Kultur für ein Verteilerlistenelement in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="f2787-177">Represents the culture for a distribution list item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="f2787-178">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="f2787-178">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="f2787-179">Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner.</span><span class="sxs-lookup"><span data-stu-id="f2787-179">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="f2787-180">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f2787-180">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="f2787-181">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="f2787-181">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="f2787-182">Enthält den Anzeigenamen des letzten Benutzers, der ein Element ändern soll.</span><span class="sxs-lookup"><span data-stu-id="f2787-182">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="f2787-183">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="f2787-183">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="f2787-184">Gibt an, wann ein Element zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="f2787-184">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="f2787-185">Isassociated</span><span class="sxs-lookup"><span data-stu-id="f2787-185">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="f2787-186">Gibt an, ob das Element einem Ordner zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f2787-186">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="f2787-187">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="f2787-187">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="f2787-188">Stellt eine URL dar, die mit dem Microsoft Office Outlook Web App-Endpunkt verkettet werden soll, um ein Element in Outlook Web App zu lesen.</span><span class="sxs-lookup"><span data-stu-id="f2787-188">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="f2787-189">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="f2787-189">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="f2787-190">Stellt eine URL dar, die mit dem Outlook Web App-Endpunkt verkettet werden soll, um ein Element in Outlook Web App zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="f2787-190">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="f2787-191">ConversationId</span><span class="sxs-lookup"><span data-stu-id="f2787-191">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="f2787-192">Enthält den Bezeichner eines Elements oder einer Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="f2787-192">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="f2787-193">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="f2787-193">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="f2787-194">Stellt ein HTML-Fragment oder nur-Text dar, der den eindeutigen Textkörper dieser Unterhaltung darstellt.</span><span class="sxs-lookup"><span data-stu-id="f2787-194">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="f2787-195">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="f2787-195">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="f2787-196">Definiert den Anzeigenamen einer Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="f2787-196">Defines the display name of a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="f2787-197">FileAs</span><span class="sxs-lookup"><span data-stu-id="f2787-197">FileAs</span></span>](fileas.md) <br/> |<span data-ttu-id="f2787-198">Stellt dar, wie eine Verteilerliste im Ordner Kontakte gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="f2787-198">Represents how a distribution list is filed in the Contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="f2787-199">ContactSource</span><span class="sxs-lookup"><span data-stu-id="f2787-199">ContactSource</span></span>](contactsource.md) <br/> |<span data-ttu-id="f2787-200">Beschreibt, ob sich der Kontakt im Exchange-Informationsspeicher oder in Active Directory-Domänendienste (AD DS) befindet.</span><span class="sxs-lookup"><span data-stu-id="f2787-200">Describes whether the contact is located in the Exchange store or in Active Directory Domain Services (AD DS).</span></span>  <br/> |
|[<span data-ttu-id="f2787-201">Members (MemberListType)</span><span class="sxs-lookup"><span data-stu-id="f2787-201">Members (MemberListType)</span></span>](members-memberlisttype.md) <br/> |<span data-ttu-id="f2787-202">Enthält eine Liste der Mitglieder der Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="f2787-202">Contains a list of members of the distribution list.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f2787-203">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f2787-203">Parent elements</span></span>

|<span data-ttu-id="f2787-204">**Element**</span><span class="sxs-lookup"><span data-stu-id="f2787-204">**Element**</span></span>|<span data-ttu-id="f2787-205">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f2787-205">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2787-206">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="f2787-206">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="f2787-207">Beschreibt alle Kalenderelemente, die an eine Besprechungszeit angrenzen.</span><span class="sxs-lookup"><span data-stu-id="f2787-207">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="f2787-208">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="f2787-208">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="f2787-209">Identifiziert Daten, die während eines [UpdateItem-Vorgangs](updateitem-operation.md)an eine einzelne Eigenschaft einer Verteilerliste angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f2787-209">Identifies data to append to a single property of a distribution list during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="f2787-210">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="f2787-210">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="f2787-211">Identifiziert alle Elemente, die mit einer Besprechungszeit in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="f2787-211">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="f2787-212">Erstellen (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="f2787-212">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="f2787-213">Identifiziert eine einzelne Verteilerliste, die im lokalen Clientspeicher erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f2787-213">Identifies a single distribution list to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="f2787-214">Update (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="f2787-214">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="f2787-215">Identifiziert eine einzelne Verteilerliste, die im lokalen Clientspeicher aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f2787-215">Identifies a single distribution list to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="f2787-216">Items</span><span class="sxs-lookup"><span data-stu-id="f2787-216">Items</span></span>](items.md) <br/> |<span data-ttu-id="f2787-217">Enthält ein Array von Elementen.</span><span class="sxs-lookup"><span data-stu-id="f2787-217">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="f2787-218">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="f2787-218">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="f2787-219">Enthält ein Array von Elementen, die in dem durch das [parentfolderid (TargetFolderIdType)-](parentfolderid-targetfolderidtype.md) Element identifizierten Ordner erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f2787-219">Contains an array of items to create in the folder identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="f2787-220">SetItemField</span><span class="sxs-lookup"><span data-stu-id="f2787-220">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="f2787-221">Stellt eine Aktualisierung einer einzelnen Eigenschaft eines Verteilerlisten Elements in einem UpdateItem- [Vorgang](updateitem-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="f2787-221">Represents an update to a single property of a distribution list item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f2787-222">Textwert</span><span class="sxs-lookup"><span data-stu-id="f2787-222">Text value</span></span>

<span data-ttu-id="f2787-223">Keine.</span><span class="sxs-lookup"><span data-stu-id="f2787-223">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f2787-224">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2787-224">Remarks</span></span>

<span data-ttu-id="f2787-225">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f2787-225">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f2787-226">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f2787-226">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f2787-227">Namespace</span><span class="sxs-lookup"><span data-stu-id="f2787-227">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f2787-228">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f2787-228">Schema Name</span></span>  <br/> |<span data-ttu-id="f2787-229">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f2787-229">Types schema</span></span>  <br/> |
|<span data-ttu-id="f2787-230">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f2787-230">Validation File</span></span>  <br/> |<span data-ttu-id="f2787-231">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f2787-231">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f2787-232">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f2787-232">Can be Empty</span></span>  <br/> |<span data-ttu-id="f2787-233">False</span><span class="sxs-lookup"><span data-stu-id="f2787-233">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f2787-234">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2787-234">See also</span></span>

- [<span data-ttu-id="f2787-235">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f2787-235">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

