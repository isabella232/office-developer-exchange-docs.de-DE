---
title: Aufgabe
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
description: Task-Element repräsentiert eine Aufgabe in der Exchange-Speicher.
ms.openlocfilehash: 2c61fca6ac85290e34f1365b0cb9e841e1fe279f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839167"
---
# <a name="task"></a><span data-ttu-id="4b182-103">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="4b182-103">Task</span></span>

<span data-ttu-id="4b182-104">**Task** -Element repräsentiert eine Aufgabe in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="4b182-104">The **Task** element represents a task in the Exchange store.</span></span> 
  
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

<span data-ttu-id="4b182-105">**TaskType**</span><span class="sxs-lookup"><span data-stu-id="4b182-105">**TaskType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="4b182-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4b182-106">Attributes and elements</span></span>

<span data-ttu-id="4b182-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4b182-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4b182-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4b182-108">Attributes</span></span>

<span data-ttu-id="4b182-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4b182-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4b182-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4b182-110">Child elements</span></span>

|<span data-ttu-id="4b182-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4b182-111">**Element**</span></span>|<span data-ttu-id="4b182-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4b182-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4b182-113">' MimeContent '</span><span class="sxs-lookup"><span data-stu-id="4b182-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="4b182-114">Enthält den systemeigene Multipurpose Internet Mail Extensions (MIME) Stream eines Objekts, das im Format base64Binary dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4b182-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="4b182-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="4b182-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="4b182-116">Enthält den eindeutigen Bezeichner und Ändern eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="4b182-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4b182-117">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="4b182-117">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="4b182-118">Stellt den Bezeichner des übergeordneten Ordners, der das Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="4b182-118">Represents the identifier of the parent folder that contains the item or folder.</span></span>  <br/> |
|[<span data-ttu-id="4b182-119">ItemClass</span><span class="sxs-lookup"><span data-stu-id="4b182-119">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="4b182-120">Die Nachrichtenklasse eines Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="4b182-120">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="4b182-121">Betreff</span><span class="sxs-lookup"><span data-stu-id="4b182-121">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="4b182-122">Der Betreff den Exchange-Speicherelemente und Antwortobjekte darstellt.</span><span class="sxs-lookup"><span data-stu-id="4b182-122">Represents the subject for Exchange store items and response objects.</span></span>  <br/> |
|[<span data-ttu-id="4b182-123">Vertraulichkeit</span><span class="sxs-lookup"><span data-stu-id="4b182-123">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="4b182-124">Enthält den Status für ein Element Vertraulichkeit.</span><span class="sxs-lookup"><span data-stu-id="4b182-124">Contains the status for an item's sensitivity.</span></span>  <br/> |
|[<span data-ttu-id="4b182-125">Body</span><span class="sxs-lookup"><span data-stu-id="4b182-125">Body</span></span>](body.md) <br/> |<span data-ttu-id="4b182-126">Stellt den tatsächlichen Textkörperinhalt einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="4b182-126">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="4b182-127">Anlagen</span><span class="sxs-lookup"><span data-stu-id="4b182-127">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="4b182-128">Enthält die Elemente oder Dateien, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4b182-128">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4b182-129">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="4b182-129">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="4b182-130">Stellt das Datum und die Uhrzeit, die ein Element in einem Postfach empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="4b182-130">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="4b182-131">Size</span><span class="sxs-lookup"><span data-stu-id="4b182-131">Size</span></span>](size.md) <br/> |<span data-ttu-id="4b182-132">Die Größe in Bytes eines Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="4b182-132">Represents the size, in bytes, of an item.</span></span> <span data-ttu-id="4b182-133">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="4b182-133">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="4b182-134">Kategorien</span><span class="sxs-lookup"><span data-stu-id="4b182-134">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="4b182-135">Stellt eine Auflistung von Zeichenfolgen, die identifizieren, welche, die Kategorien ein Elements im Postfach gehört.</span><span class="sxs-lookup"><span data-stu-id="4b182-135">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="4b182-136">Importance</span><span class="sxs-lookup"><span data-stu-id="4b182-136">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="4b182-137">Beschreibt die Bedeutung eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="4b182-137">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="4b182-138">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="4b182-138">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="4b182-139">Stellt den Bezeichner des Elements, der dieses Element eine Antwort ist.</span><span class="sxs-lookup"><span data-stu-id="4b182-139">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="4b182-140">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="4b182-140">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="4b182-141">Gibt an, ob ein Element in den Standardordner Postausgang gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="4b182-141">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="4b182-142">IsDraft</span><span class="sxs-lookup"><span data-stu-id="4b182-142">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="4b182-143">Stellt dar, ob ein Element noch nicht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="4b182-143">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="4b182-144">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="4b182-144">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="4b182-145">Gibt an, ob ein Benutzer ein Element an sich gesendet.</span><span class="sxs-lookup"><span data-stu-id="4b182-145">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="4b182-146">IsResend</span><span class="sxs-lookup"><span data-stu-id="4b182-146">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="4b182-147">Gibt an, ob das Element zuvor gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="4b182-147">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="4b182-148">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="4b182-148">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="4b182-149">Gibt an, ob das Element geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="4b182-149">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="4b182-150">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="4b182-150">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="4b182-151">Stellt die Auflistung aller Internet Message Header, die in einem Element in einem Postfach enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="4b182-151">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="4b182-152">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="4b182-152">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="4b182-153">Stellt das Datum und die Uhrzeit, die ein Element in einem Postfach gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="4b182-153">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="4b182-154">"Datetimecreated"</span><span class="sxs-lookup"><span data-stu-id="4b182-154">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="4b182-155">Stellt das Datum und die Uhrzeit, die ein bestimmtes Element im Postfach erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4b182-155">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="4b182-156">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="4b182-156">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="4b182-157">Enthält eine Auflistung aller Antwort-Objekte, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4b182-157">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4b182-158">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="4b182-158">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="4b182-159">Stellt das Datum und die Uhrzeit bei des Ereignisses eintreten.</span><span class="sxs-lookup"><span data-stu-id="4b182-159">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="4b182-160">Dies wird durch die [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) -Element verwendet, um zu bestimmen, wann die Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4b182-160">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="4b182-161">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="4b182-161">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="4b182-162">Gibt an, ob eine Erinnerung für ein Element in der Exchange-Informationsspeicher festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="4b182-162">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4b182-163">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="4b182-163">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="4b182-164">Stellt die Anzahl der Minuten, bevor ein Ereignis, wenn eine Erinnerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4b182-164">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="4b182-165">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="4b182-165">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="4b182-166">Stellt die Zeichenfolge, die für den Inhalt des im Feld "Cc" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4b182-166">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="4b182-167">Dies ist die verkettete Zeichenfolge alle Anzeigenamen der Cc-Empfänger.</span><span class="sxs-lookup"><span data-stu-id="4b182-167">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="4b182-168">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="4b182-168">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="4b182-169">Stellt die Zeichenfolge, die für den Inhalt des im Feld an verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4b182-169">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="4b182-170">Dies ist die verkettete Zeichenfolge aller in Empfänger Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="4b182-170">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="4b182-171">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="4b182-171">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="4b182-172">Stellt eine Eigenschaft, die auf **true** festgelegt ist, wenn ein Element mindestens eine Anlage sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="4b182-172">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="4b182-173">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="4b182-173">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="4b182-174">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="4b182-174">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="4b182-175">Erweiterte Eigenschaften für Ordner und Elemente identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4b182-175">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="4b182-176">Kultur</span><span class="sxs-lookup"><span data-stu-id="4b182-176">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="4b182-177">Stellt die Kultur für ein bestimmtes Element in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="4b182-177">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="4b182-178">ActualWork</span><span class="sxs-lookup"><span data-stu-id="4b182-178">ActualWork</span></span>](actualwork.md) <br/> |<span data-ttu-id="4b182-179">Stellt die tatsächliche Vergrößerung Zeitspanne für die für einen Vorgang dar.</span><span class="sxs-lookup"><span data-stu-id="4b182-179">Represents the actual amount of time that is spent on a task.</span></span>  <br/> |
|[<span data-ttu-id="4b182-180">AssignedTime</span><span class="sxs-lookup"><span data-stu-id="4b182-180">AssignedTime</span></span>](assignedtime.md) <br/> |<span data-ttu-id="4b182-181">Gibt die Zeit an, wenn eine Aufgabe mit einem Kontakt zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="4b182-181">Represents the time when a task is assigned to a contact.</span></span>  <br/> |
|[<span data-ttu-id="4b182-182">BillingInformation</span><span class="sxs-lookup"><span data-stu-id="4b182-182">BillingInformation</span></span>](billinginformation.md) <br/> |<span data-ttu-id="4b182-183">Abrechnungsinformationen für einen Vorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="4b182-183">Holds billing information for a task.</span></span>  <br/> |
|[<span data-ttu-id="4b182-184">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="4b182-184">ChangeCount</span></span>](changecount.md) <br/> |<span data-ttu-id="4b182-185">Gibt die Version des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="4b182-185">Specifies the version of the task.</span></span>  <br/> |
|[<span data-ttu-id="4b182-186">Companies</span><span class="sxs-lookup"><span data-stu-id="4b182-186">Companies</span></span>](companies.md) <br/> |<span data-ttu-id="4b182-187">Stellt die Auflistung der Unternehmen, die einen Kontakt oder eine Aufgabe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4b182-187">Represents the collection of companies that are associated with a contact or task.</span></span>  <br/> |
|[<span data-ttu-id="4b182-188">"CompleteDate" darf</span><span class="sxs-lookup"><span data-stu-id="4b182-188">CompleteDate</span></span>](completedate.md) <br/> |<span data-ttu-id="4b182-189">Stellt das Datum, an dem eine Aufgabe abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="4b182-189">Represents the date on which a task is completed.</span></span>  <br/> |
|[<span data-ttu-id="4b182-190">Kontakte</span><span class="sxs-lookup"><span data-stu-id="4b182-190">Contacts</span></span>](contacts-ex15websvcsotherref.md) <br/> |<span data-ttu-id="4b182-191">Enthält eine Liste von Kontakten, die mit einem Vorgang verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="4b182-191">Contains a list of contacts that are associated with a task.</span></span>  <br/> |
|[<span data-ttu-id="4b182-192">DelegationState</span><span class="sxs-lookup"><span data-stu-id="4b182-192">DelegationState</span></span>](delegationstate.md) <br/> |<span data-ttu-id="4b182-193">Stellt den Status eines delegierten Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="4b182-193">Represents the status of a delegated task.</span></span>  <br/> |
|[<span data-ttu-id="4b182-194">Delegator</span><span class="sxs-lookup"><span data-stu-id="4b182-194">Delegator</span></span>](delegator.md) <br/> |<span data-ttu-id="4b182-195">Enthält den Namen des Stellvertreters, die die Aufgabe zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="4b182-195">Contains the name of the delegator who assigned the task.</span></span>  <br/> |
|[<span data-ttu-id="4b182-196">DueDate</span><span class="sxs-lookup"><span data-stu-id="4b182-196">DueDate</span></span>](duedate.md) <br/> |<span data-ttu-id="4b182-197">Stellt das Datum ein Aufgabenelement fällig ist.</span><span class="sxs-lookup"><span data-stu-id="4b182-197">Represents the date when a task item is due.</span></span>  <br/> |
|[<span data-ttu-id="4b182-198">IsAssignmentEditable</span><span class="sxs-lookup"><span data-stu-id="4b182-198">IsAssignmentEditable</span></span>](isassignmenteditable.md) <br/> |<span data-ttu-id="4b182-199">Gibt an, ob die Aufgabe bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4b182-199">Indicates whether the task is editable or not.</span></span>  <br/> |
|[<span data-ttu-id="4b182-200">IsComplete</span><span class="sxs-lookup"><span data-stu-id="4b182-200">IsComplete</span></span>](iscomplete.md) <br/> |<span data-ttu-id="4b182-201">Gibt an, ob der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="4b182-201">Indicates whether the task has been completed or not.</span></span>  <br/> |
|[<span data-ttu-id="4b182-202">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="4b182-202">IsRecurring</span></span>](isrecurring.md) <br/> |<span data-ttu-id="4b182-203">Gibt an, ob eine Aufgabe Teil einer Terminserie ist.</span><span class="sxs-lookup"><span data-stu-id="4b182-203">Indicates whether a task is part of a recurring item.</span></span> <span data-ttu-id="4b182-204">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="4b182-204">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="4b182-205">IsTeamTask</span><span class="sxs-lookup"><span data-stu-id="4b182-205">IsTeamTask</span></span>](isteamtask.md) <br/> |<span data-ttu-id="4b182-206">Gibt an, ob die Aufgabe von einem Team gehören ist.</span><span class="sxs-lookup"><span data-stu-id="4b182-206">Indicates whether the task is owned by a team or not.</span></span>  <br/> |
|[<span data-ttu-id="4b182-207">Mileage</span><span class="sxs-lookup"><span data-stu-id="4b182-207">Mileage</span></span>](mileage.md) <br/> |<span data-ttu-id="4b182-208">Mileage ein Aufgabenelement darstellt.</span><span class="sxs-lookup"><span data-stu-id="4b182-208">Represents mileage for a task item.</span></span>  <br/> |
|[<span data-ttu-id="4b182-209">Owner</span><span class="sxs-lookup"><span data-stu-id="4b182-209">Owner</span></span>](owner.md) <br/> |<span data-ttu-id="4b182-210">Stellt den Besitzer eines Vorgangs dar.</span><span class="sxs-lookup"><span data-stu-id="4b182-210">Represents the owner of a task.</span></span>  <br/> |
|[<span data-ttu-id="4b182-211">PercentComplete</span><span class="sxs-lookup"><span data-stu-id="4b182-211">PercentComplete</span></span>](percentcomplete.md) <br/> |<span data-ttu-id="4b182-212">Beschreibt den Status eines Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="4b182-212">Describes the completion status of a task.</span></span>  <br/> |
|[<span data-ttu-id="4b182-213">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="4b182-213">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="4b182-214">Serieninformationen für wiederkehrende Aufgaben enthält.</span><span class="sxs-lookup"><span data-stu-id="4b182-214">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="4b182-215">StartDate</span><span class="sxs-lookup"><span data-stu-id="4b182-215">StartDate</span></span>](startdate.md) <br/> |<span data-ttu-id="4b182-216">Den Anfangstermin eines Aufgabenelements darstellt.</span><span class="sxs-lookup"><span data-stu-id="4b182-216">Represents the start date of a task item.</span></span>  <br/> |
|[<span data-ttu-id="4b182-217">Status</span><span class="sxs-lookup"><span data-stu-id="4b182-217">Status</span></span>](status.md) <br/> |<span data-ttu-id="4b182-218">Stellt den Status eines Aufgabenelements dar.</span><span class="sxs-lookup"><span data-stu-id="4b182-218">Represents the status of a task item.</span></span>  <br/> |
|[<span data-ttu-id="4b182-219">StatusDescription</span><span class="sxs-lookup"><span data-stu-id="4b182-219">StatusDescription</span></span>](statusdescription.md) <br/> |<span data-ttu-id="4b182-220">Enthält eine Erläuterung der den Aufgabenstatus an.</span><span class="sxs-lookup"><span data-stu-id="4b182-220">Contains an explanation of the task status.</span></span>  <br/> |
|[<span data-ttu-id="4b182-221">TotalWork</span><span class="sxs-lookup"><span data-stu-id="4b182-221">TotalWork</span></span>](totalwork.md) <br/> |<span data-ttu-id="4b182-222">Enthält eine Beschreibung der Umfang der Arbeit mit einem Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4b182-222">Contains a description of how much work is associated with an item.</span></span>  <br/> |
|[<span data-ttu-id="4b182-223">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="4b182-223">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="4b182-224">Die Rechte des Clients basierend auf die berechtigungseinstellungen für das Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="4b182-224">Contains the rights of the client based on the permission settings for the item or folder.</span></span> <span data-ttu-id="4b182-225">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="4b182-225">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="4b182-226">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="4b182-226">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="4b182-227">Enthält den Anzeigenamen des Benutzers auf ein Element zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4b182-227">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="4b182-228">ZuletztGeändertUm</span><span class="sxs-lookup"><span data-stu-id="4b182-228">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="4b182-229">Gibt an, wann ein Element zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="4b182-229">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="4b182-230">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="4b182-230">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="4b182-231">Gibt an, ob das Element einem Ordner zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4b182-231">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="4b182-232">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="4b182-232">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="4b182-233">Stellt eine URL zu verketten an den Microsoft Office Outlook Web App-Endpunkt ein Elements in Outlook Web App zu lesen.</span><span class="sxs-lookup"><span data-stu-id="4b182-233">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="4b182-234">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="4b182-234">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="4b182-235">Stellt eine URL an den Endpunkt Outlook Web App so bearbeiten Sie ein Element in Outlook Web App verketten.</span><span class="sxs-lookup"><span data-stu-id="4b182-235">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="4b182-236">ConversationId</span><span class="sxs-lookup"><span data-stu-id="4b182-236">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="4b182-237">Enthält die ID eines Elements oder einer Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="4b182-237">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="4b182-238">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="4b182-238">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="4b182-239">Stellt ein HTML-Fragment oder nur-Text, der den eindeutigen Text an dieser Unterhaltung darstellt.</span><span class="sxs-lookup"><span data-stu-id="4b182-239">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4b182-240">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4b182-240">Parent elements</span></span>

|<span data-ttu-id="4b182-241">**Element**</span><span class="sxs-lookup"><span data-stu-id="4b182-241">**Element**</span></span>|<span data-ttu-id="4b182-242">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4b182-242">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4b182-243">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="4b182-243">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="4b182-244">Werden alle Kalenderelemente, die an eine Besprechungszeit angrenzen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4b182-244">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="4b182-245">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="4b182-245">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="4b182-246">Identifiziert Daten an eine einzelne Eigenschaft eines Elements-Ordners während eines [Vorgangs UpdateItem](updateitem-operation.md)angefügt.</span><span class="sxs-lookup"><span data-stu-id="4b182-246">Identifies data to append to a single property of an item/folder during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="4b182-247">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="4b182-247">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="4b182-248">Identifiziert alle Elemente, die mit einem bestimmten Zeitpunkt treffen Konflikt.</span><span class="sxs-lookup"><span data-stu-id="4b182-248">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="4b182-249">Erstellen (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="4b182-249">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="4b182-250">Gibt ein einzelnes Element in der lokalen Client-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4b182-250">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="4b182-251">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="4b182-251">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="4b182-252">Stellt ein Exchange-Element, das mit einem anderen Exchange-Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4b182-252">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="4b182-253">Elemente</span><span class="sxs-lookup"><span data-stu-id="4b182-253">Items</span></span>](items.md) <br/> |<span data-ttu-id="4b182-254">Enthält ein Array von Elementen an.</span><span class="sxs-lookup"><span data-stu-id="4b182-254">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="4b182-255">SetItemField</span><span class="sxs-lookup"><span data-stu-id="4b182-255">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="4b182-256">Stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einer [UpdateItem Operation](updateitem-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="4b182-256">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="4b182-257">Update (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="4b182-257">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="4b182-258">Gibt ein einzelnes Element in den Speicher des lokalen Client aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="4b182-258">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4b182-259">Textwert</span><span class="sxs-lookup"><span data-stu-id="4b182-259">Text value</span></span>

<span data-ttu-id="4b182-260">Keine.</span><span class="sxs-lookup"><span data-stu-id="4b182-260">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4b182-261">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4b182-261">Remarks</span></span>

<span data-ttu-id="4b182-262">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4b182-262">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4b182-263">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4b182-263">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4b182-264">Namespace</span><span class="sxs-lookup"><span data-stu-id="4b182-264">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4b182-265">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4b182-265">Schema name</span></span>  <br/> |<span data-ttu-id="4b182-266">Schematypen</span><span class="sxs-lookup"><span data-stu-id="4b182-266">Types schema</span></span>  <br/> |
|<span data-ttu-id="4b182-267">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4b182-267">Validation file</span></span>  <br/> |<span data-ttu-id="4b182-268">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4b182-268">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4b182-269">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="4b182-269">Can be empty</span></span>  <br/> |<span data-ttu-id="4b182-270">False</span><span class="sxs-lookup"><span data-stu-id="4b182-270">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4b182-271">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b182-271">See also</span></span>

- [<span data-ttu-id="4b182-272">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4b182-272">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="4b182-273">Erstellen von Aufgaben</span><span class="sxs-lookup"><span data-stu-id="4b182-273">Creating Tasks</span></span>](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
- [<span data-ttu-id="4b182-274">Deleting Tasks</span><span class="sxs-lookup"><span data-stu-id="4b182-274">Deleting Tasks</span></span>](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

