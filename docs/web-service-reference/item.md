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
description: Das Element stellt ein allgemeines Element im Exchange-Speicher.
ms.openlocfilehash: 7af8e063c3bfd77bd87b80463c11c58d996626b5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830143"
---
# <a name="item"></a><span data-ttu-id="d3448-103">Element</span><span class="sxs-lookup"><span data-stu-id="d3448-103">Item</span></span>

<span data-ttu-id="d3448-104">**Das Element** stellt ein allgemeines Element im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="d3448-104">The **Item** element represents a generic item in the Exchange store.</span></span> 
  
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

 <span data-ttu-id="d3448-105">**ItemType**</span><span class="sxs-lookup"><span data-stu-id="d3448-105">**ItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d3448-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d3448-106">Attributes and elements</span></span>

<span data-ttu-id="d3448-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d3448-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d3448-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d3448-108">Attributes</span></span>

<span data-ttu-id="d3448-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d3448-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d3448-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d3448-110">Child elements</span></span>

|<span data-ttu-id="d3448-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d3448-111">**Element**</span></span>|<span data-ttu-id="d3448-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d3448-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d3448-113">' MimeContent '</span><span class="sxs-lookup"><span data-stu-id="d3448-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="d3448-114">Enthält den systemeigene Multipurpose Internet Mail Extensions (MIME) Stream eines Objekts, das im Format base64Binary dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d3448-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="d3448-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="d3448-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="d3448-116">Enthält den eindeutigen Bezeichner und Ändern eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="d3448-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="d3448-117">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d3448-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d3448-118">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="d3448-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="d3448-119">Stellt den Bezeichner des übergeordneten Ordners, der das Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="d3448-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="d3448-120">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d3448-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d3448-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="d3448-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="d3448-122">Die Nachrichtenklasse eines Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="d3448-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="d3448-123">Betreff</span><span class="sxs-lookup"><span data-stu-id="d3448-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="d3448-124">Der Betreff den Exchange-Speicherelemente und Antwortobjekte darstellt.</span><span class="sxs-lookup"><span data-stu-id="d3448-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="d3448-125">Der Betreff ist auf 255 Zeichen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="d3448-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="d3448-126">Vertraulichkeit</span><span class="sxs-lookup"><span data-stu-id="d3448-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="d3448-127">Gibt die Vertraulichkeitsstufe eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="d3448-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="d3448-128">Body</span><span class="sxs-lookup"><span data-stu-id="d3448-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="d3448-129">Stellt den tatsächlichen Textkörperinhalt einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d3448-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="d3448-130">Anlagen</span><span class="sxs-lookup"><span data-stu-id="d3448-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d3448-131">Enthält die Elemente oder Dateien, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d3448-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d3448-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="d3448-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="d3448-133">Stellt das Datum und die Uhrzeit, die ein Element in einem Postfach empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="d3448-133">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="d3448-134">Size</span><span class="sxs-lookup"><span data-stu-id="d3448-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="d3448-135">Die Größe in Bytes eines Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="d3448-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="d3448-136">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d3448-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d3448-137">Kategorien</span><span class="sxs-lookup"><span data-stu-id="d3448-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d3448-138">Stellt eine Auflistung von Zeichenfolgen, die identifizieren, welche, die Kategorien ein Elements im Postfach gehört.</span><span class="sxs-lookup"><span data-stu-id="d3448-138">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="d3448-139">Importance</span><span class="sxs-lookup"><span data-stu-id="d3448-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="d3448-140">Beschreibt die Bedeutung eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="d3448-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="d3448-141">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="d3448-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="d3448-142">Stellt den Bezeichner des Elements, der dieses Element eine Antwort ist.</span><span class="sxs-lookup"><span data-stu-id="d3448-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="d3448-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="d3448-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="d3448-144">Gibt an, ob ein Element in den Standardordner Postausgang gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d3448-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="d3448-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="d3448-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="d3448-146">Stellt dar, ob ein Element noch nicht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d3448-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="d3448-147">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="d3448-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="d3448-148">Gibt an, ob ein Benutzer ein Element auf sich selbst gesendet.</span><span class="sxs-lookup"><span data-stu-id="d3448-148">Indicates whether a user sent an item to itself.</span></span>  <br/> |
|[<span data-ttu-id="d3448-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="d3448-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="d3448-150">Gibt an, ob das Element zuvor gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="d3448-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="d3448-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="d3448-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="d3448-152">Gibt an, ob das Element geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="d3448-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="d3448-153">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="d3448-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="d3448-154">Stellt die Auflistung aller Internet Message Header, die innerhalb eines Elements in einem Postfach enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d3448-154">Represents the collection of all Internet message headers that are contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d3448-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="d3448-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="d3448-156">Stellt das Datum und die Uhrzeit, die ein Element in einem Postfach gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d3448-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="d3448-157">"Datetimecreated"</span><span class="sxs-lookup"><span data-stu-id="d3448-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="d3448-158">Stellt das Datum und die Uhrzeit, die ein bestimmtes Element im Postfach erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d3448-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="d3448-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="d3448-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="d3448-160">Enthält eine Auflistung aller Antwort-Objekte, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d3448-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d3448-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="d3448-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="d3448-162">Stellt das Datum und die Uhrzeit bei des Ereignisses eintreten.</span><span class="sxs-lookup"><span data-stu-id="d3448-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="d3448-163">Dies wird durch die [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) -Element verwendet, um zu bestimmen, wann die Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d3448-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="d3448-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="d3448-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="d3448-165">Gibt an, ob eine Erinnerung für ein Element in der Exchange-Informationsspeicher festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="d3448-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d3448-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="d3448-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="d3448-167">Stellt die Anzahl der Minuten, bevor ein Ereignis, wenn eine Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d3448-167">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="d3448-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="d3448-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="d3448-169">Stellt die Zeichenfolge, die für den Inhalt des im Feld "Cc" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d3448-169">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="d3448-170">Dies ist die verkettete Zeichenfolge alle Anzeigenamen der Cc-Empfänger.</span><span class="sxs-lookup"><span data-stu-id="d3448-170">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="d3448-171">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="d3448-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="d3448-172">Stellt die Zeichenfolge, die für den Inhalt des im Feld an verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d3448-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="d3448-173">Dies ist die verkettete Zeichenfolge aller in Empfänger Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="d3448-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="d3448-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="d3448-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="d3448-175">Stellt eine Eigenschaft, die auf **true** festgelegt ist, wenn ein Element Anlagen enthält mindestens eine Anlage sichtbar.</span><span class="sxs-lookup"><span data-stu-id="d3448-175">Represents a property that is set to **true** if an item has attachments at least one visible attachment.</span></span> <span data-ttu-id="d3448-176">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d3448-176">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d3448-177">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="d3448-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="d3448-178">Erweiterte Eigenschaften für Ordner und Elemente identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d3448-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="d3448-179">Kultur</span><span class="sxs-lookup"><span data-stu-id="d3448-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="d3448-180">Stellt die Kultur für ein bestimmtes Element in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="d3448-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d3448-181">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="d3448-181">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="d3448-182">Der Client Rechte basierend auf den berechtigungseinstellungen für das Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="d3448-182">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="d3448-183">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d3448-183">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="d3448-184">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="d3448-184">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="d3448-185">Enthält den Anzeigenamen des Benutzers auf ein Element zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d3448-185">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="d3448-186">ZuletztGeändertUm</span><span class="sxs-lookup"><span data-stu-id="d3448-186">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="d3448-187">Gibt an, wann ein Element zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="d3448-187">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="d3448-188">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="d3448-188">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="d3448-189">Gibt an, ob das Element einem Ordner zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d3448-189">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="d3448-190">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="d3448-190">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="d3448-191">Stellt eine URL zu verketten an den Microsoft Office Outlook Web App-Endpunkt ein Elements in Outlook Web App zu lesen.</span><span class="sxs-lookup"><span data-stu-id="d3448-191">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="d3448-192">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="d3448-192">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="d3448-193">Stellt eine URL an den Endpunkt Outlook Web App so bearbeiten Sie ein Element in Outlook Web App verketten.</span><span class="sxs-lookup"><span data-stu-id="d3448-193">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="d3448-194">ConversationId</span><span class="sxs-lookup"><span data-stu-id="d3448-194">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="d3448-195">Enthält die ID eines Elements oder einer Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="d3448-195">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="d3448-196">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="d3448-196">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="d3448-197">Stellt ein HTML-Fragment oder nur-Text, der den eindeutigen Text an dieser Unterhaltung darstellt.</span><span class="sxs-lookup"><span data-stu-id="d3448-197">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d3448-198">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d3448-198">Parent elements</span></span>

|<span data-ttu-id="d3448-199">**Element**</span><span class="sxs-lookup"><span data-stu-id="d3448-199">**Element**</span></span>|<span data-ttu-id="d3448-200">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d3448-200">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d3448-201">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="d3448-201">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="d3448-202">Werden alle Kalenderelemente, die an eine Besprechungszeit angrenzen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d3448-202">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="d3448-203">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="d3448-203">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="d3448-204">Identifiziert Daten an eine einzelne Eigenschaft eines Elements-Ordners während eines [Vorgangs UpdateItem](updateitem-operation.md)angefügt.</span><span class="sxs-lookup"><span data-stu-id="d3448-204">Identifies data to append to a single property of an item/folder during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="d3448-205">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="d3448-205">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="d3448-206">Identifiziert alle Elemente, die mit einem bestimmten Zeitpunkt treffen Konflikt.</span><span class="sxs-lookup"><span data-stu-id="d3448-206">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="d3448-207">Erstellen (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="d3448-207">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="d3448-208">Gibt ein einzelnes Element in der lokalen Client-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d3448-208">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="d3448-209">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="d3448-209">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="d3448-210">Stellt ein Exchange-Element, das mit einem anderen Exchange-Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d3448-210">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="d3448-211">Elemente</span><span class="sxs-lookup"><span data-stu-id="d3448-211">Items</span></span>](items.md) <br/> |<span data-ttu-id="d3448-212">Enthält ein Array von Elementen an.</span><span class="sxs-lookup"><span data-stu-id="d3448-212">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="d3448-213">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="d3448-213">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="d3448-214">Enthält ein Array von Elementen im Ordner zu erstellen, die durch das Element [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="d3448-214">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="d3448-215">SetItemField</span><span class="sxs-lookup"><span data-stu-id="d3448-215">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="d3448-216">Stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einer [UpdateItem Operation](updateitem-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="d3448-216">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="d3448-217">Update (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="d3448-217">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="d3448-218">Gibt ein einzelnes Element in den Speicher des lokalen Client aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d3448-218">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d3448-219">Textwert</span><span class="sxs-lookup"><span data-stu-id="d3448-219">Text value</span></span>

<span data-ttu-id="d3448-220">Keine.</span><span class="sxs-lookup"><span data-stu-id="d3448-220">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d3448-221">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d3448-221">Remarks</span></span>

<span data-ttu-id="d3448-222">Es ist wichtig, dass **ItemType** den Basistyp für die [Aufgabe](task.md), [CalendarItem](calendaritem.md), [Kontakt-](contact.md), [DistributionList](distributionlist.md)und [Nachricht](message-ex15websvcsotherref.md)ist.</span><span class="sxs-lookup"><span data-stu-id="d3448-222">It is important to note that **ItemType** is the base type for [Task](task.md), [CalendarItem](calendaritem.md), [Contact](contact.md), [DistributionList](distributionlist.md), and [Message](message-ex15websvcsotherref.md).</span></span>
  
<span data-ttu-id="d3448-223">[Nachrichtenelemente](message-ex15websvcsotherref.md) darstellen, E-mail-Nachrichten und andere Elemente, die vom Exchange-Webdienste (EWS) Schema nicht stark typisiert sind.</span><span class="sxs-lookup"><span data-stu-id="d3448-223">[Message](message-ex15websvcsotherref.md) elements represent e-mail messages and all other items that are not strongly typed by the Exchange Web Services (EWS) schema.</span></span> <span data-ttu-id="d3448-224">Elemente wie IPM.Sharing- und IPM.InfoPath-Elemente werden als **Message**-Elemente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d3448-224">Items such as IPM.Sharing and IPM.InfoPath are returned as **Message** elements.</span></span> <span data-ttu-id="d3448-225">Microsoft Exchange Server 2010 werden keine das Basiselement **Element** in Antworten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d3448-225">Microsoft Exchange Server 2010 does not return the base **Item** element in responses.</span></span> 
  
<span data-ttu-id="d3448-226">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d3448-226">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d3448-227">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d3448-227">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d3448-228">Namespace</span><span class="sxs-lookup"><span data-stu-id="d3448-228">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d3448-229">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d3448-229">Schema Name</span></span>  <br/> |<span data-ttu-id="d3448-230">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d3448-230">Types schema</span></span>  <br/> |
|<span data-ttu-id="d3448-231">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d3448-231">Validation File</span></span>  <br/> |<span data-ttu-id="d3448-232">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d3448-232">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d3448-233">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d3448-233">Can be Empty</span></span>  <br/> |<span data-ttu-id="d3448-234">False</span><span class="sxs-lookup"><span data-stu-id="d3448-234">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d3448-235">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3448-235">See also</span></span>



- [<span data-ttu-id="d3448-236">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d3448-236">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
  
[<span data-ttu-id="d3448-237">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="d3448-237">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

