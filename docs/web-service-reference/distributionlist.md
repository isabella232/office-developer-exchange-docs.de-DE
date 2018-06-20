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
description: Das Element DistributionList stellt eine Verteilerliste dar.
ms.openlocfilehash: 5edcc83eef6a5b16470e6c290aacd057ceecceb1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758077"
---
# <a name="distributionlist"></a><span data-ttu-id="c4aa1-103">DistributionList</span><span class="sxs-lookup"><span data-stu-id="c4aa1-103">DistributionList</span></span>

<span data-ttu-id="c4aa1-104">Das Element **DistributionList** stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-104">The **DistributionList** element represents a distribution list.</span></span> 
  
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

 <span data-ttu-id="c4aa1-105">**DistributionListType**</span><span class="sxs-lookup"><span data-stu-id="c4aa1-105">**DistributionListType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c4aa1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c4aa1-106">Attributes and elements</span></span>

<span data-ttu-id="c4aa1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c4aa1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c4aa1-108">Attributes</span></span>

<span data-ttu-id="c4aa1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c4aa1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c4aa1-110">Child elements</span></span>

|<span data-ttu-id="c4aa1-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c4aa1-111">**Element**</span></span>|<span data-ttu-id="c4aa1-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c4aa1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4aa1-113">' MimeContent '</span><span class="sxs-lookup"><span data-stu-id="c4aa1-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="c4aa1-114">Enthält den systemeigenen MIME-Stream eines Objekts in base64Binary Format dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-114">Contains the native MIME stream of an object represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="c4aa1-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="c4aa1-116">Enthält den eindeutigen Bezeichner und Ändern eines Listenelements Verteilung im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-116">Contains the unique identifier and change key of a distribution list item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-117">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="c4aa1-117">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="c4aa1-118">Stellt den Bezeichner des übergeordneten Ordners, der die verteilerlistenelement enthält.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-118">Represents the identifier of the parent folder that contains the distribution list item.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-119">ItemClass</span><span class="sxs-lookup"><span data-stu-id="c4aa1-119">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="c4aa1-120">Stellt die Nachrichtenklasse eines Listenelements Verteilung.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-120">Represents the message class of a distribution list item.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-121">Betreff</span><span class="sxs-lookup"><span data-stu-id="c4aa1-121">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="c4aa1-122">Der Betreff den Exchange-Speicherelemente und Antwortobjekte darstellt.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-122">Represents the subject for Exchange store items and response objects.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-123">Vertraulichkeit</span><span class="sxs-lookup"><span data-stu-id="c4aa1-123">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="c4aa1-124">Enthält den Status für ein Listenelement Verteilung Vertraulichkeit.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-124">Contains the status for a distribution list item's sensitivity.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-125">Body</span><span class="sxs-lookup"><span data-stu-id="c4aa1-125">Body</span></span>](body.md) <br/> |<span data-ttu-id="c4aa1-126">Stellt den tatsächlichen Textkörperinhalt eines Listenelements Verteilung.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-126">Represents the actual body content of a distribution list item.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-127">Anlagen</span><span class="sxs-lookup"><span data-stu-id="c4aa1-127">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="c4aa1-128">Enthält die Elemente oder Dateien, die ein verteilerlistenelement im Exchange-Speicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-128">Contains the items or files that are attached to a distribution list item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-129">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="c4aa1-129">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="c4aa1-130">Stellt das Datum und die Uhrzeit, zu der eine verteilerlistenelement in einem Postfach empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-130">Represents the date and time that a distribution list item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-131">Size</span><span class="sxs-lookup"><span data-stu-id="c4aa1-131">Size</span></span>](size.md) <br/> |<span data-ttu-id="c4aa1-132">Stellt die Größe in Bytes eines Listenelements Verteilung.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-132">Represents the size, in bytes, of a distribution list item.</span></span> <span data-ttu-id="c4aa1-133">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-133">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-134">Kategorien</span><span class="sxs-lookup"><span data-stu-id="c4aa1-134">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="c4aa1-135">Stellt eine Auflistung von Zeichenfolgen, die identifizieren, welche, die Kategorien ein Listenelement Verteilung im Postfach gehört.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-135">Represents a collection of strings that identify to which categories a distribution list item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-136">Importance</span><span class="sxs-lookup"><span data-stu-id="c4aa1-136">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="c4aa1-137">Beschreibt die Bedeutung eines Listenelements Verteilung.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-137">Describes the importance of a distribution list item.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-138">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="c4aa1-138">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="c4aa1-139">Stellt den Bezeichner des Elements, das dieses Element eine Antwort ist.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-139">Represents the identifier of the item which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-140">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="c4aa1-140">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="c4aa1-141">Gibt an, ob ein Element in den Standardordner Postausgang gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-141">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-142">IsDraft</span><span class="sxs-lookup"><span data-stu-id="c4aa1-142">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="c4aa1-143">Stellt dar, ob ein Element noch nicht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-143">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-144">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="c4aa1-144">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="c4aa1-145">Gibt an, ob ein Benutzer ein Element auf sich selbst gesendet.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-145">Indicates whether a user sent an item to itself.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-146">IsResend</span><span class="sxs-lookup"><span data-stu-id="c4aa1-146">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="c4aa1-147">Gibt an, ob das Element zuvor gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-147">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-148">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="c4aa1-148">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="c4aa1-149">Gibt an, ob das Element geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-149">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-150">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="c4aa1-150">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="c4aa1-151">Stellt die Auflistung aller Internet Message Header, die innerhalb eines Elements in einem Postfach enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-151">Represents the collection of all Internet message headers contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-152">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="c4aa1-152">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="c4aa1-153">Stellt das Datum und die Uhrzeit, die ein Element in einem Postfach gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-153">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-154">"Datetimecreated"</span><span class="sxs-lookup"><span data-stu-id="c4aa1-154">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="c4aa1-155">Stellt das Datum und die Uhrzeit, die ein bestimmtes Element im Postfach erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-155">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-156">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="c4aa1-156">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="c4aa1-157">Enthält eine Auflistung aller Antwort-Objekte, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-157">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-158">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="c4aa1-158">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="c4aa1-159">Stellt das Datum und die Uhrzeit bei des Ereignisses eintreten.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-159">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="c4aa1-160">Dies wird durch die [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) -Element verwendet, um zu bestimmen, wann die Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-160">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-161">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="c4aa1-161">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="c4aa1-162">Gibt an, ob eine Erinnerung für ein Element in der Exchange-Informationsspeicher festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-162">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-163">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="c4aa1-163">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="c4aa1-164">Stellt die Anzahl der Minuten, bevor ein Ereignis, wenn eine Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-164">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-165">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="c4aa1-165">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="c4aa1-166">Stellt die Zeichenfolge, die für den Inhalt der Cc-Zeile verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-166">Represents the display string that is used for the contents of the Cc line.</span></span> <span data-ttu-id="c4aa1-167">Dies ist die verkettete Zeichenfolge alle Anzeigenamen der Cc-Empfänger.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-167">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-168">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="c4aa1-168">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="c4aa1-169">Stellt die Zeichenfolge, die für den Inhalt der Zeile verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-169">Represents the display string that is used for the contents of the To line.</span></span> <span data-ttu-id="c4aa1-170">Dies ist die verkettete Zeichenfolge aller in Empfänger Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-170">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-171">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="c4aa1-171">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="c4aa1-172">Stellt eine Eigenschaft, die auf **true** festgelegt ist, wenn ein Element mindestens eine Anlage sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-172">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="c4aa1-173">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-173">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-174">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="c4aa1-174">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="c4aa1-175">Erweiterte Eigenschaften für ein Listenelement Verteilung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-175">Identifies extended properties on a distribution list item.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-176">Kultur</span><span class="sxs-lookup"><span data-stu-id="c4aa1-176">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="c4aa1-177">Stellt die Kultur für ein Listenelement Verteilung in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-177">Represents the culture for a distribution list item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-178">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="c4aa1-178">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="c4aa1-179">Der Client Rechte basierend auf den berechtigungseinstellungen für das Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-179">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="c4aa1-180">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-180">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-181">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="c4aa1-181">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="c4aa1-182">Enthält den Anzeigenamen des Benutzers auf ein Element zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-182">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-183">ZuletztGeändertUm</span><span class="sxs-lookup"><span data-stu-id="c4aa1-183">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="c4aa1-184">Gibt an, wann ein Element zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-184">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-185">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="c4aa1-185">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="c4aa1-186">Gibt an, ob das Element einem Ordner zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-186">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-187">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="c4aa1-187">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="c4aa1-188">Stellt eine URL zu verketten an den Microsoft Office Outlook Web App-Endpunkt ein Elements in Outlook Web App zu lesen.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-188">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-189">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="c4aa1-189">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="c4aa1-190">Stellt eine URL an den Endpunkt Outlook Web App so bearbeiten Sie ein Element in Outlook Web App verketten.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-190">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-191">ConversationId</span><span class="sxs-lookup"><span data-stu-id="c4aa1-191">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="c4aa1-192">Enthält die ID eines Elements oder einer Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-192">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-193">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="c4aa1-193">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="c4aa1-194">Stellt ein HTML-Fragment oder nur-Text, der den eindeutigen Text an dieser Unterhaltung darstellt.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-194">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-195">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="c4aa1-195">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="c4aa1-196">Definiert den Anzeigenamen einer Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-196">Defines the display name of a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-197">FileAs</span><span class="sxs-lookup"><span data-stu-id="c4aa1-197">FileAs</span></span>](fileas.md) <br/> |<span data-ttu-id="c4aa1-198">Stellt dar, wie eine Verteilerliste im Ordner "Kontakte" abgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-198">Represents how a distribution list is filed in the Contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-199">ContactSource</span><span class="sxs-lookup"><span data-stu-id="c4aa1-199">ContactSource</span></span>](contactsource.md) <br/> |<span data-ttu-id="c4aa1-200">Beschreibt, ob der Kontakt in der Exchange-Speicher oder in Active Directory-Domänendienste (AD DS) gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-200">Describes whether the contact is located in the Exchange store or in Active Directory Domain Services (AD DS).</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-201">Elemente des Objekts (MemberListType)</span><span class="sxs-lookup"><span data-stu-id="c4aa1-201">Members (MemberListType)</span></span>](members-memberlisttype.md) <br/> |<span data-ttu-id="c4aa1-202">Enthält eine Liste der Mitglieder der Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-202">Contains a list of members of the distribution list.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c4aa1-203">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c4aa1-203">Parent elements</span></span>

|<span data-ttu-id="c4aa1-204">**Element**</span><span class="sxs-lookup"><span data-stu-id="c4aa1-204">**Element**</span></span>|<span data-ttu-id="c4aa1-205">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c4aa1-205">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4aa1-206">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="c4aa1-206">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="c4aa1-207">Werden alle Kalenderelemente, die an eine Besprechungszeit angrenzen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-207">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-208">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="c4aa1-208">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="c4aa1-209">Identifiziert Daten an eine einzelne Eigenschaft einer Verteilerliste während eines [Vorgangs UpdateItem](updateitem-operation.md)angefügt.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-209">Identifies data to append to a single property of a distribution list during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-210">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="c4aa1-210">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="c4aa1-211">Identifiziert alle Elemente, die mit einem bestimmten Zeitpunkt treffen Konflikt.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-211">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-212">Erstellen (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="c4aa1-212">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="c4aa1-213">Identifiziert eine Verteilerliste im lokalen Client-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-213">Identifies a single distribution list to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-214">Update (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="c4aa1-214">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="c4aa1-215">Identifiziert eine Verteilerliste, die in den Speicher des lokalen Client aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-215">Identifies a single distribution list to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-216">Elemente</span><span class="sxs-lookup"><span data-stu-id="c4aa1-216">Items</span></span>](items.md) <br/> |<span data-ttu-id="c4aa1-217">Enthält ein Array von Elementen an.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-217">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-218">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="c4aa1-218">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="c4aa1-219">Enthält ein Array von Elementen, die in den Ordner vom [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) -Element zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-219">Contains an array of items to create in the folder identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="c4aa1-220">SetItemField</span><span class="sxs-lookup"><span data-stu-id="c4aa1-220">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="c4aa1-221">Stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Listenelements Verteilung in einer [UpdateItem Vorgang](updateitem-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-221">Represents an update to a single property of a distribution list item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c4aa1-222">Textwert</span><span class="sxs-lookup"><span data-stu-id="c4aa1-222">Text value</span></span>

<span data-ttu-id="c4aa1-223">Keine.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-223">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c4aa1-224">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c4aa1-224">Remarks</span></span>

<span data-ttu-id="c4aa1-225">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c4aa1-225">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c4aa1-226">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c4aa1-226">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4aa1-227">Namespace</span><span class="sxs-lookup"><span data-stu-id="c4aa1-227">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c4aa1-228">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c4aa1-228">Schema Name</span></span>  <br/> |<span data-ttu-id="c4aa1-229">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c4aa1-229">Types schema</span></span>  <br/> |
|<span data-ttu-id="c4aa1-230">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c4aa1-230">Validation File</span></span>  <br/> |<span data-ttu-id="c4aa1-231">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c4aa1-231">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c4aa1-232">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c4aa1-232">Can be Empty</span></span>  <br/> |<span data-ttu-id="c4aa1-233">False</span><span class="sxs-lookup"><span data-stu-id="c4aa1-233">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c4aa1-234">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4aa1-234">See also</span></span>

- [<span data-ttu-id="c4aa1-235">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c4aa1-235">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

