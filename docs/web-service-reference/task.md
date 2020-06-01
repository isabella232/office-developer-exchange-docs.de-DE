---
title: Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Task
api_type:
- schema
ms.assetid: 7c84927e-db28-4c5d-b0b5-cbcc2b88d869
description: Das Task-Element stellt eine Aufgabe im Exchange-Informationsspeicher dar.
ms.openlocfilehash: 669f90dfa74cd085091e9836a1d31ca53bbf165e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458943"
---
# <a name="task"></a><span data-ttu-id="e7adf-103">Vorgang</span><span class="sxs-lookup"><span data-stu-id="e7adf-103">Task</span></span>

<span data-ttu-id="e7adf-104">Das **Task** -Element stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="e7adf-104">The **Task** element represents a task in the Exchange store.</span></span> 
  
```xml
<Task>
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
   <ActualWork/>
   <AssignedTime/>
   <BillingInformation/>
   <ChangeCount/>
   <Companies/>
   <CompleteDate/>
   <Contacts/>
   <DelegationState/>
   <Delegator/>
   <DueDate/>
   <IsAssignmentEditable/>
   <IsComplete/>
   <IsRecurring/>
   <IsTeamTask/>
   <Mileage/>
   <Owner/>
   <PercentComplete/>
   <Recurrence/>
   <StartDate/>
   <Status/>
   <StatusDescription/>
   <TotalWork/>
   <EffectiveRights/>
   <LastModifiedName/>
   <LastModifiedTime/>
   <IsAssociated/>
   <WebClientReadFormQueryString/>
   <WebClientEditFormQueryString/>
   <ConversationId/>
   <UniqueBody/>
</Task>
```

<span data-ttu-id="e7adf-105">**TaskType**</span><span class="sxs-lookup"><span data-stu-id="e7adf-105">**TaskType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="e7adf-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e7adf-106">Attributes and elements</span></span>

<span data-ttu-id="e7adf-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e7adf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e7adf-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e7adf-108">Attributes</span></span>

<span data-ttu-id="e7adf-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e7adf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e7adf-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e7adf-110">Child elements</span></span>

|<span data-ttu-id="e7adf-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e7adf-111">**Element**</span></span>|<span data-ttu-id="e7adf-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e7adf-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e7adf-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="e7adf-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="e7adf-114">Enthält den systemeigenen Multipurpose Internet Mail Extensions (MIME) Stream eines Objekts, das im base64Binary-Format dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e7adf-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="e7adf-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="e7adf-116">Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="e7adf-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-117">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="e7adf-117">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="e7adf-118">Stellt den Bezeichner des übergeordneten Ordners dar, der das Element oder den Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="e7adf-118">Represents the identifier of the parent folder that contains the item or folder.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-119">ItemClass</span><span class="sxs-lookup"><span data-stu-id="e7adf-119">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="e7adf-120">Stellt die Nachrichtenklasse eines Elements dar.</span><span class="sxs-lookup"><span data-stu-id="e7adf-120">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-121">Betreff</span><span class="sxs-lookup"><span data-stu-id="e7adf-121">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="e7adf-122">Stellt den Betreff für Exchange-Informationsspeicher Elemente und Response-Objekte dar.</span><span class="sxs-lookup"><span data-stu-id="e7adf-122">Represents the subject for Exchange store items and response objects.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-123">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="e7adf-123">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="e7adf-124">Enthält den Status für die Empfindlichkeit eines Elements.</span><span class="sxs-lookup"><span data-stu-id="e7adf-124">Contains the status for an item's sensitivity.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-125">Body</span><span class="sxs-lookup"><span data-stu-id="e7adf-125">Body</span></span>](body.md) <br/> |<span data-ttu-id="e7adf-126">Stellt den tatsächlichen Textinhalt einer Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="e7adf-126">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-127">Anlagen</span><span class="sxs-lookup"><span data-stu-id="e7adf-127">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="e7adf-128">Enthält die Elemente oder Dateien, die an ein Element im Exchange-Informationsspeicher angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="e7adf-128">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-129">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="e7adf-129">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="e7adf-130">Stellt das Datum und die Uhrzeit dar, zu denen ein Element in einem Postfach empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="e7adf-130">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-131">Größe</span><span class="sxs-lookup"><span data-stu-id="e7adf-131">Size</span></span>](size.md) <br/> |<span data-ttu-id="e7adf-132">Stellt die Größe eines Elements in Bytes dar.</span><span class="sxs-lookup"><span data-stu-id="e7adf-132">Represents the size, in bytes, of an item.</span></span> <span data-ttu-id="e7adf-133">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e7adf-133">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-134">Kategorien</span><span class="sxs-lookup"><span data-stu-id="e7adf-134">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="e7adf-135">Stellt eine Auflistung von Zeichenfolgen dar, die ermitteln, zu welchen Kategorien ein Element im Postfach gehört.</span><span class="sxs-lookup"><span data-stu-id="e7adf-135">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-136">Importance</span><span class="sxs-lookup"><span data-stu-id="e7adf-136">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="e7adf-137">Beschreibt die Wichtigkeit eines Elements.</span><span class="sxs-lookup"><span data-stu-id="e7adf-137">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-138">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="e7adf-138">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="e7adf-139">Stellt den Bezeichner des Elements dar, zu dem dieses Element eine Antwort ist.</span><span class="sxs-lookup"><span data-stu-id="e7adf-139">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-140">Issubmitted</span><span class="sxs-lookup"><span data-stu-id="e7adf-140">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="e7adf-141">Gibt an, ob ein Element an den Standardordner Postausgang übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="e7adf-141">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-142">IsDraft</span><span class="sxs-lookup"><span data-stu-id="e7adf-142">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="e7adf-143">Stellt dar, ob ein Element noch nicht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e7adf-143">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-144">Isfromme</span><span class="sxs-lookup"><span data-stu-id="e7adf-144">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="e7adf-145">Gibt an, ob ein Benutzer ein Element an sich selbst gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="e7adf-145">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-146">IsResend</span><span class="sxs-lookup"><span data-stu-id="e7adf-146">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="e7adf-147">Gibt an, ob das Element zuvor gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e7adf-147">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-148">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="e7adf-148">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="e7adf-149">Gibt an, ob das Element geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="e7adf-149">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-150">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="e7adf-150">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="e7adf-151">Stellt die Auflistung aller Internet Nachrichtenkopfzeilen dar, die in einem Element in einem Postfach enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="e7adf-151">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-152">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="e7adf-152">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="e7adf-153">Stellt das Datum und die Uhrzeit dar, zu denen ein Element in einem Postfach gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e7adf-153">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-154">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="e7adf-154">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="e7adf-155">Stellt das Datum und die Uhrzeit dar, zu der ein bestimmtes Element im Postfach erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e7adf-155">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-156">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="e7adf-156">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="e7adf-157">Enthält eine Auflistung aller Response-Objekte, die einem Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e7adf-157">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-158">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="e7adf-158">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="e7adf-159">Stellt das Datum und die Uhrzeit des Eintretens des Ereignisses dar.</span><span class="sxs-lookup"><span data-stu-id="e7adf-159">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="e7adf-160">Dies wird vom [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) -Element verwendet, um zu bestimmen, wann die Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e7adf-160">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-161">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="e7adf-161">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="e7adf-162">Gibt an, ob für ein Element im Exchange-Informationsspeicher eine Erinnerung festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="e7adf-162">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-163">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="e7adf-163">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="e7adf-164">Stellt die Anzahl von Minuten vor einem Ereignis dar, wenn eine Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e7adf-164">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-165">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="e7adf-165">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="e7adf-166">Stellt die Anzeigezeichenfolge dar, die für den Inhalt des Felds CC verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e7adf-166">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="e7adf-167">Dies ist die verkettete Zeichenfolge aller Anzeigenamen des CC-Empfängers.</span><span class="sxs-lookup"><span data-stu-id="e7adf-167">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-168">Displayto ursprünglicher</span><span class="sxs-lookup"><span data-stu-id="e7adf-168">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="e7adf-169">Stellt die Anzeigezeichenfolge dar, die für den Inhalt des Felds an verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e7adf-169">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="e7adf-170">Dies ist die verkettete Zeichenfolge aller in Empfänger Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="e7adf-170">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-171">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="e7adf-171">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="e7adf-172">Stellt eine Eigenschaft dar, die auf **true** festgelegt ist, wenn ein Element mindestens eine sichtbare Anlage aufweist.</span><span class="sxs-lookup"><span data-stu-id="e7adf-172">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="e7adf-173">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e7adf-173">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-174">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="e7adf-174">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="e7adf-175">Erweiterte Eigenschaften für Ordner und Elemente identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e7adf-175">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-176">Kultur</span><span class="sxs-lookup"><span data-stu-id="e7adf-176">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="e7adf-177">Stellt die Kultur für ein bestimmtes Element in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="e7adf-177">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-178">ActualWork</span><span class="sxs-lookup"><span data-stu-id="e7adf-178">ActualWork</span></span>](actualwork.md) <br/> |<span data-ttu-id="e7adf-179">Stellt die tatsächliche Zeitspanne dar, die für einen Vorgang aufgewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e7adf-179">Represents the actual amount of time that is spent on a task.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-180">Zugewiesenezeit</span><span class="sxs-lookup"><span data-stu-id="e7adf-180">AssignedTime</span></span>](assignedtime.md) <br/> |<span data-ttu-id="e7adf-181">Stellt die Uhrzeit dar, zu der ein Vorgang einem Kontakt zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="e7adf-181">Represents the time when a task is assigned to a contact.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-182">BillingInformation</span><span class="sxs-lookup"><span data-stu-id="e7adf-182">BillingInformation</span></span>](billinginformation.md) <br/> |<span data-ttu-id="e7adf-183">Speichert Abrechnungsinformationen für einen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="e7adf-183">Holds billing information for a task.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-184">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="e7adf-184">ChangeCount</span></span>](changecount.md) <br/> |<span data-ttu-id="e7adf-185">Gibt die Version des Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="e7adf-185">Specifies the version of the task.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-186">Companies</span><span class="sxs-lookup"><span data-stu-id="e7adf-186">Companies</span></span>](companies.md) <br/> |<span data-ttu-id="e7adf-187">Stellt die Auflistung von Unternehmen dar, die einem Kontakt oder einer Aufgabe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e7adf-187">Represents the collection of companies that are associated with a contact or task.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-188">CompleteDate</span><span class="sxs-lookup"><span data-stu-id="e7adf-188">CompleteDate</span></span>](completedate.md) <br/> |<span data-ttu-id="e7adf-189">Stellt das Datum dar, an dem ein Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="e7adf-189">Represents the date on which a task is completed.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-190">Kontakte</span><span class="sxs-lookup"><span data-stu-id="e7adf-190">Contacts</span></span>](contacts-ex15websvcsotherref.md) <br/> |<span data-ttu-id="e7adf-191">Enthält eine Liste der Kontakte, die einem Vorgang zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e7adf-191">Contains a list of contacts that are associated with a task.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-192">DelegationState</span><span class="sxs-lookup"><span data-stu-id="e7adf-192">DelegationState</span></span>](delegationstate.md) <br/> |<span data-ttu-id="e7adf-193">Stellt den Status einer Delegierten Aufgabe dar.</span><span class="sxs-lookup"><span data-stu-id="e7adf-193">Represents the status of a delegated task.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-194">Delegator</span><span class="sxs-lookup"><span data-stu-id="e7adf-194">Delegator</span></span>](delegator.md) <br/> |<span data-ttu-id="e7adf-195">Enthält den Namen des delegars, der die Aufgabe zugewiesen hat.</span><span class="sxs-lookup"><span data-stu-id="e7adf-195">Contains the name of the delegator who assigned the task.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-196">DueDate</span><span class="sxs-lookup"><span data-stu-id="e7adf-196">DueDate</span></span>](duedate.md) <br/> |<span data-ttu-id="e7adf-197">Stellt das Datum dar, an dem ein Aufgabenelement fällig ist.</span><span class="sxs-lookup"><span data-stu-id="e7adf-197">Represents the date when a task item is due.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-198">IsAssignmentEditable</span><span class="sxs-lookup"><span data-stu-id="e7adf-198">IsAssignmentEditable</span></span>](isassignmenteditable.md) <br/> |<span data-ttu-id="e7adf-199">Gibt an, ob der Vorgang bearbeitbar ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="e7adf-199">Indicates whether the task is editable or not.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-200">IsComplete</span><span class="sxs-lookup"><span data-stu-id="e7adf-200">IsComplete</span></span>](iscomplete.md) <br/> |<span data-ttu-id="e7adf-201">Gibt an, ob der Vorgang abgeschlossen wurde oder nicht.</span><span class="sxs-lookup"><span data-stu-id="e7adf-201">Indicates whether the task has been completed or not.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-202">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="e7adf-202">IsRecurring</span></span>](isrecurring.md) <br/> |<span data-ttu-id="e7adf-203">Gibt an, ob ein Vorgang Teil eines wiederkehrenden Elements ist.</span><span class="sxs-lookup"><span data-stu-id="e7adf-203">Indicates whether a task is part of a recurring item.</span></span> <span data-ttu-id="e7adf-204">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e7adf-204">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-205">IsTeamTask</span><span class="sxs-lookup"><span data-stu-id="e7adf-205">IsTeamTask</span></span>](isteamtask.md) <br/> |<span data-ttu-id="e7adf-206">Gibt an, ob die Aufgabe einem Team gehört oder nicht.</span><span class="sxs-lookup"><span data-stu-id="e7adf-206">Indicates whether the task is owned by a team or not.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-207">Mileage</span><span class="sxs-lookup"><span data-stu-id="e7adf-207">Mileage</span></span>](mileage.md) <br/> |<span data-ttu-id="e7adf-208">Stellt die Kilometerleistung für ein Aufgabenelement dar.</span><span class="sxs-lookup"><span data-stu-id="e7adf-208">Represents mileage for a task item.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-209">Owner</span><span class="sxs-lookup"><span data-stu-id="e7adf-209">Owner</span></span>](owner.md) <br/> |<span data-ttu-id="e7adf-210">Stellt den Besitzer einer Aufgabe dar.</span><span class="sxs-lookup"><span data-stu-id="e7adf-210">Represents the owner of a task.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-211">PercentComplete</span><span class="sxs-lookup"><span data-stu-id="e7adf-211">PercentComplete</span></span>](percentcomplete.md) <br/> |<span data-ttu-id="e7adf-212">Beschreibt den Abschlussstatus eines Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="e7adf-212">Describes the completion status of a task.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-213">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="e7adf-213">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="e7adf-214">Enthält Serieninformationen für wiederkehrende Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="e7adf-214">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-215">StartDate</span><span class="sxs-lookup"><span data-stu-id="e7adf-215">StartDate</span></span>](startdate.md) <br/> |<span data-ttu-id="e7adf-216">Stellt das Startdatum eines Aufgabenelements dar.</span><span class="sxs-lookup"><span data-stu-id="e7adf-216">Represents the start date of a task item.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-217">Status</span><span class="sxs-lookup"><span data-stu-id="e7adf-217">Status</span></span>](status.md) <br/> |<span data-ttu-id="e7adf-218">Stellt den Status eines Aufgabenelements dar.</span><span class="sxs-lookup"><span data-stu-id="e7adf-218">Represents the status of a task item.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-219">StatusDescription</span><span class="sxs-lookup"><span data-stu-id="e7adf-219">StatusDescription</span></span>](statusdescription.md) <br/> |<span data-ttu-id="e7adf-220">Enthält eine Erläuterung des Vorgangsstatus.</span><span class="sxs-lookup"><span data-stu-id="e7adf-220">Contains an explanation of the task status.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-221">TotalWork</span><span class="sxs-lookup"><span data-stu-id="e7adf-221">TotalWork</span></span>](totalwork.md) <br/> |<span data-ttu-id="e7adf-222">Enthält eine Beschreibung, wie viel Arbeit einem Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e7adf-222">Contains a description of how much work is associated with an item.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-223">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="e7adf-223">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="e7adf-224">Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner.</span><span class="sxs-lookup"><span data-stu-id="e7adf-224">Contains the rights of the client based on the permission settings for the item or folder.</span></span> <span data-ttu-id="e7adf-225">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e7adf-225">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-226">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="e7adf-226">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="e7adf-227">Enthält den Anzeigenamen des letzten Benutzers, der ein Element ändern soll.</span><span class="sxs-lookup"><span data-stu-id="e7adf-227">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-228">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="e7adf-228">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="e7adf-229">Gibt an, wann ein Element zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="e7adf-229">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-230">Isassociated</span><span class="sxs-lookup"><span data-stu-id="e7adf-230">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="e7adf-231">Gibt an, ob das Element einem Ordner zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e7adf-231">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-232">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="e7adf-232">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="e7adf-233">Stellt eine URL dar, die mit dem Microsoft Office Outlook Web App-Endpunkt verkettet werden soll, um ein Element in Outlook Web App zu lesen.</span><span class="sxs-lookup"><span data-stu-id="e7adf-233">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-234">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="e7adf-234">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="e7adf-235">Stellt eine URL dar, die mit dem Outlook Web App-Endpunkt verkettet werden soll, um ein Element in Outlook Web App zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="e7adf-235">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-236">ConversationId</span><span class="sxs-lookup"><span data-stu-id="e7adf-236">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="e7adf-237">Enthält den Bezeichner eines Elements oder einer Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="e7adf-237">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-238">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="e7adf-238">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="e7adf-239">Stellt ein HTML-Fragment oder nur-Text dar, der den eindeutigen Textkörper dieser Unterhaltung darstellt.</span><span class="sxs-lookup"><span data-stu-id="e7adf-239">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e7adf-240">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e7adf-240">Parent elements</span></span>

|<span data-ttu-id="e7adf-241">**Element**</span><span class="sxs-lookup"><span data-stu-id="e7adf-241">**Element**</span></span>|<span data-ttu-id="e7adf-242">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e7adf-242">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e7adf-243">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="e7adf-243">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="e7adf-244">Beschreibt alle Kalenderelemente, die an eine Besprechungszeit angrenzen.</span><span class="sxs-lookup"><span data-stu-id="e7adf-244">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-245">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="e7adf-245">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="e7adf-246">Identifiziert Daten, die während eines [UpdateItem-Vorgangs](updateitem-operation.md)an eine einzelne Eigenschaft eines Elements/Ordners angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e7adf-246">Identifies data to append to a single property of an item/folder during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="e7adf-247">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="e7adf-247">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="e7adf-248">Identifiziert alle Elemente, die mit einer Besprechungszeit in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="e7adf-248">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-249">Erstellen (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="e7adf-249">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="e7adf-250">Identifiziert ein einzelnes Element, das im lokalen Clientspeicher erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e7adf-250">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-251">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="e7adf-251">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="e7adf-252">Stellt ein Exchange-Element dar, das an ein anderes Exchange-Element angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="e7adf-252">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-253">Items</span><span class="sxs-lookup"><span data-stu-id="e7adf-253">Items</span></span>](items.md) <br/> |<span data-ttu-id="e7adf-254">Enthält ein Array von Elementen.</span><span class="sxs-lookup"><span data-stu-id="e7adf-254">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="e7adf-255">SetItemField</span><span class="sxs-lookup"><span data-stu-id="e7adf-255">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="e7adf-256">Stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einer [UpdateItem Operation](updateitem-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="e7adf-256">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="e7adf-257">Update (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="e7adf-257">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="e7adf-258">Identifiziert ein einzelnes Element, das im lokalen Clientspeicher aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e7adf-258">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e7adf-259">Textwert</span><span class="sxs-lookup"><span data-stu-id="e7adf-259">Text value</span></span>

<span data-ttu-id="e7adf-260">Keine.</span><span class="sxs-lookup"><span data-stu-id="e7adf-260">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e7adf-261">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7adf-261">Remarks</span></span>

<span data-ttu-id="e7adf-262">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="e7adf-262">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e7adf-263">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e7adf-263">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e7adf-264">Namespace</span><span class="sxs-lookup"><span data-stu-id="e7adf-264">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e7adf-265">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e7adf-265">Schema name</span></span>  <br/> |<span data-ttu-id="e7adf-266">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e7adf-266">Types schema</span></span>  <br/> |
|<span data-ttu-id="e7adf-267">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e7adf-267">Validation file</span></span>  <br/> |<span data-ttu-id="e7adf-268">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e7adf-268">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e7adf-269">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="e7adf-269">Can be empty</span></span>  <br/> |<span data-ttu-id="e7adf-270">False</span><span class="sxs-lookup"><span data-stu-id="e7adf-270">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e7adf-271">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7adf-271">See also</span></span>

- [<span data-ttu-id="e7adf-272">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e7adf-272">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="e7adf-273">Erstellen von Aufgaben</span><span class="sxs-lookup"><span data-stu-id="e7adf-273">Creating Tasks</span></span>](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
- [<span data-ttu-id="e7adf-274">Deleting Tasks</span><span class="sxs-lookup"><span data-stu-id="e7adf-274">Deleting Tasks</span></span>](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

