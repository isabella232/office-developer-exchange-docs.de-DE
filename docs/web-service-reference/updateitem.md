---
title: UpdateItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: 34643d58-2743-45b0-a08d-bff6dc1da61d
description: Das UpdateItem-Element definiert eine Anforderung zum Aktualisieren eines Elements in einem Postfach.
ms.openlocfilehash: 7b9b5f1dcffb95eb127572cb91f92d961c05a77e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/21/2018
ms.locfileid: "19839381"
---
# <a name="updateitem"></a><span data-ttu-id="d30cb-103">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="d30cb-103">UpdateItem</span></span>

<span data-ttu-id="d30cb-104">Das **UpdateItem** -Element definiert eine Anforderung zum Aktualisieren eines Elements in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="d30cb-104">The **UpdateItem** element defines a request to update an item in a mailbox.</span></span> 
  
```XML
<UpdateItem ConflictResolution="" MessageDisposition="" SendMeetingInvitationsOrCancellations="" SuppressReadReceipts="">
   <SavedItemFolderId/>
   <ItemChanges/>
</UpdateItem>
```

 <span data-ttu-id="d30cb-105">**UpdateItemType**</span><span class="sxs-lookup"><span data-stu-id="d30cb-105">**UpdateItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d30cb-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d30cb-106">Attributes and elements</span></span>

<span data-ttu-id="d30cb-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d30cb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d30cb-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d30cb-108">Attributes</span></span>

|<span data-ttu-id="d30cb-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d30cb-109">**Attribute**</span></span>|<span data-ttu-id="d30cb-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d30cb-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d30cb-111">**ConflictResolution**</span><span class="sxs-lookup"><span data-stu-id="d30cb-111">**ConflictResolution**</span></span> <br/> |<span data-ttu-id="d30cb-112">Identifiziert den Typ des Konfliktbehebung während einer Aktualisierung versuchen.</span><span class="sxs-lookup"><span data-stu-id="d30cb-112">Identifies the type of conflict resolution to try during an update.</span></span> <span data-ttu-id="d30cb-113">Der Standardwert ist auflösen.</span><span class="sxs-lookup"><span data-stu-id="d30cb-113">The default value is AutoResolve.</span></span>  <br/> |
|<span data-ttu-id="d30cb-114">**"MessageDisposition"**</span><span class="sxs-lookup"><span data-stu-id="d30cb-114">**MessageDisposition**</span></span> <br/> |<span data-ttu-id="d30cb-115">Beschreibt, wie das Element nach der Aktualisierung behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d30cb-115">Describes how the item will be handled after it is updated.</span></span> <span data-ttu-id="d30cb-116">Das Attribut **"MessageDisposition"** ist für Nachrichtenelemente, einschließlich der Besprechungsnachrichten wie Besprechungsabsagen, Besprechungsanfragen und Antworten auf Besprechungsanfragen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d30cb-116">The **MessageDisposition** attribute is required for message items, including meeting messages such as meeting cancellations, meeting requests, and meeting responses.</span></span>  <br/> |
|<span data-ttu-id="d30cb-117">**"SendMeetingInvitationsOrCancellations"**</span><span class="sxs-lookup"><span data-stu-id="d30cb-117">**SendMeetingInvitationsOrCancellations**</span></span> <br/> |<span data-ttu-id="d30cb-118">Beschreibt, wie Besprechung aktualisiert übermittelt werden, nachdem ein Kalenderelement aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d30cb-118">Describes how meeting updates are communicated after a calendar item is updated.</span></span> <span data-ttu-id="d30cb-119">Dieses Attribut ist für Kalenderelemente und Kalendertermine Element erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d30cb-119">This attribute is required for calendar items and calendar item occurrences.</span></span>  <br/> |
|<span data-ttu-id="d30cb-120">**SuppressReadReceipts**</span><span class="sxs-lookup"><span data-stu-id="d30cb-120">**SuppressReadReceipts**</span></span> <br/> |<span data-ttu-id="d30cb-121">Gibt an, ob lesebestätigungen für das aktualisierte Element unterdrückt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d30cb-121">Indicates whether read receipts for the updated item should be suppressed.</span></span> <span data-ttu-id="d30cb-122">Der Textwert **true** gibt an, dass das Read, Empfangsbestätigungen unterdrückt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d30cb-122">A text value of **true** indicates that read receipts should be suppressed.</span></span> <span data-ttu-id="d30cb-123">Der Wert **false** gibt an, dass die lesebestätigungen an den Absender gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="d30cb-123">A value of **false** indicates that the read receipts will be sent to the sender.</span></span> <span data-ttu-id="d30cb-124">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="d30cb-124">This attribute is optional.</span></span>  <br/> <span data-ttu-id="d30cb-125">Dieses Attribut wurde in Exchange Server 2013 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d30cb-125">This attribute was introduced in Exchange Server 2013 SP1.</span></span>  <br/> |
   
#### <a name="conflictresolution-attribute"></a><span data-ttu-id="d30cb-126">ConflictResolution-Attribut</span><span class="sxs-lookup"><span data-stu-id="d30cb-126">ConflictResolution Attribute</span></span>

|<span data-ttu-id="d30cb-127">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d30cb-127">**Value**</span></span>|<span data-ttu-id="d30cb-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d30cb-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d30cb-129">NeverOverwrite</span><span class="sxs-lookup"><span data-stu-id="d30cb-129">NeverOverwrite</span></span>  <br/> |<span data-ttu-id="d30cb-130">Wenn ein Konflikt vorliegt, die Aktualisierung fehl und ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d30cb-130">If there is a conflict, the update operation fails and an error is returned.</span></span>  <br/> |
|<span data-ttu-id="d30cb-131">Auflösen</span><span class="sxs-lookup"><span data-stu-id="d30cb-131">AutoResolve</span></span>  <br/> |<span data-ttu-id="d30cb-132">Der Aktualisierungsvorgang aufgelöst wird automatisch ein Konflikt.</span><span class="sxs-lookup"><span data-stu-id="d30cb-132">The update operation automatically resolves any conflict.</span></span>  <br/> |
|<span data-ttu-id="d30cb-133">AlwaysOverwrite</span><span class="sxs-lookup"><span data-stu-id="d30cb-133">AlwaysOverwrite</span></span>  <br/> |<span data-ttu-id="d30cb-134">Wenn ein Konflikt vorliegt, wird der Aktualisierungsvorgang Informationen überschrieben.</span><span class="sxs-lookup"><span data-stu-id="d30cb-134">If there is a conflict, the update operation will overwrite information.</span></span>  <br/> |
   
#### <a name="messagedisposition-attribute"></a><span data-ttu-id="d30cb-135">Attribut "MessageDisposition"</span><span class="sxs-lookup"><span data-stu-id="d30cb-135">MessageDisposition Attribute</span></span>

|<span data-ttu-id="d30cb-136">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d30cb-136">**Value**</span></span>|<span data-ttu-id="d30cb-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d30cb-137">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d30cb-138">SaveOnly</span><span class="sxs-lookup"><span data-stu-id="d30cb-138">SaveOnly</span></span>  <br/> |<span data-ttu-id="d30cb-139">Das Element wird aktualisiert und wieder in seinem aktuellen Ordner gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d30cb-139">The item is updated and saved back to its current folder.</span></span>  <br/> |
|<span data-ttu-id="d30cb-140">SendOnly</span><span class="sxs-lookup"><span data-stu-id="d30cb-140">SendOnly</span></span>  <br/> |<span data-ttu-id="d30cb-141">Das Element wird aktualisiert und gesendet, aber keine Kopie gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="d30cb-141">The item is updated and sent but no copy is saved.</span></span>  <br/> |
|<span data-ttu-id="d30cb-142">SendAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="d30cb-142">SendAndSaveCopy</span></span>  <br/> |<span data-ttu-id="d30cb-143">Das Element wird aktualisiert, und eine Kopie im durch das Element [des SavedItemFolderId](saveditemfolderid.md) identifizierten Ordner gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="d30cb-143">The item is updated and a copy is saved in the folder identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
   
#### <a name="sendmeetinginvitationsorcancellations-attribute"></a><span data-ttu-id="d30cb-144">Attribut "SendMeetingInvitationsOrCancellations"</span><span class="sxs-lookup"><span data-stu-id="d30cb-144">SendMeetingInvitationsOrCancellations Attribute</span></span>

|<span data-ttu-id="d30cb-145">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d30cb-145">**Value**</span></span>|<span data-ttu-id="d30cb-146">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d30cb-146">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d30cb-147">SendToNone</span><span class="sxs-lookup"><span data-stu-id="d30cb-147">SendToNone</span></span>  <br/> |<span data-ttu-id="d30cb-148">Das Kalenderelement wurde aktualisiert, jedoch Updates werden nicht an die Teilnehmer gesendet.</span><span class="sxs-lookup"><span data-stu-id="d30cb-148">The calendar item is updated but updates are not sent to attendees.</span></span>  <br/> |
|<span data-ttu-id="d30cb-149">SendOnlyToAll</span><span class="sxs-lookup"><span data-stu-id="d30cb-149">SendOnlyToAll</span></span>  <br/> |<span data-ttu-id="d30cb-150">Das Kalenderelement wird aktualisiert und die Besprechungsanfrage wird an alle Teilnehmer gesendet, aber nicht im Ordner "Gesendete Elemente" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d30cb-150">The calendar item is updated and the meeting update is sent to all attendees but is not saved in the Sent Items folder.</span></span>  <br/> |
|<span data-ttu-id="d30cb-151">SendOnlyToChanged</span><span class="sxs-lookup"><span data-stu-id="d30cb-151">SendOnlyToChanged</span></span>  <br/> |<span data-ttu-id="d30cb-152">Das Kalenderelement wird aktualisiert, und die besprechungsaktualisierung wird nur für Teilnehmer, die von der Änderung in der Besprechung betroffen sind gesendet.</span><span class="sxs-lookup"><span data-stu-id="d30cb-152">The calendar item is updated and the meeting update is sent only to attendees that are affected by the change in the meeting.</span></span>  <br/> |
|<span data-ttu-id="d30cb-153">SendToAllAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="d30cb-153">SendToAllAndSaveCopy</span></span>  <br/> |<span data-ttu-id="d30cb-154">Das Kalenderelement wird aktualisiert, die besprechungsaktualisierung wird an alle Teilnehmer gesendet und eine Kopie im Ordner "Gesendete Elemente" gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="d30cb-154">The calendar item is updated, the meeting update is sent to all attendees, and a copy is saved in the Sent Items folder.</span></span>  <br/> |
|<span data-ttu-id="d30cb-155">SendToChangedAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="d30cb-155">SendToChangedAndSaveCopy</span></span>  <br/> |<span data-ttu-id="d30cb-156">Das Kalenderelement wird aktualisiert, die besprechungsaktualisierung wird an alle Teilnehmer, die von der Änderung in der Besprechung betroffen sind gesendet, und eine Kopie im Ordner "Gesendete Elemente" gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="d30cb-156">The calendar item is updated, the meeting update is sent to all attendees that are affected by the change in the meeting, and a copy is saved in the Sent Items folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d30cb-157">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d30cb-157">Child elements</span></span>

|<span data-ttu-id="d30cb-158">**Element**</span><span class="sxs-lookup"><span data-stu-id="d30cb-158">**Element**</span></span>|<span data-ttu-id="d30cb-159">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d30cb-159">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d30cb-160">Des SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="d30cb-160">SavedItemFolderId</span></span>](saveditemfolderid.md) <br/> |<span data-ttu-id="d30cb-161">Identifiziert den Zielordner für Vorgänge, die zu aktualisieren, senden und Elemente im Exchange-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d30cb-161">Identifies the target folder for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d30cb-162">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="d30cb-162">ItemChanges</span></span>](itemchanges.md) <br/> |<span data-ttu-id="d30cb-163">Enthält ein Array von [ItemChange](itemchange.md) -Elementen, die Elemente und die Updates auf Elemente anwenden zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d30cb-163">Contains an array of [ItemChange](itemchange.md) elements that identify items and the updates to apply to the items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d30cb-164">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d30cb-164">Parent elements</span></span>

<span data-ttu-id="d30cb-165">Keine.</span><span class="sxs-lookup"><span data-stu-id="d30cb-165">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d30cb-166">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d30cb-166">Remarks</span></span>

<span data-ttu-id="d30cb-167">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d30cb-167">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d30cb-168">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d30cb-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d30cb-169">Namespace</span><span class="sxs-lookup"><span data-stu-id="d30cb-169">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d30cb-170">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d30cb-170">Schema Name</span></span>  <br/> |<span data-ttu-id="d30cb-171">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d30cb-171">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d30cb-172">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d30cb-172">Validation File</span></span>  <br/> |<span data-ttu-id="d30cb-173">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d30cb-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d30cb-174">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d30cb-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="d30cb-175">False</span><span class="sxs-lookup"><span data-stu-id="d30cb-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d30cb-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d30cb-176">See also</span></span>



[<span data-ttu-id="d30cb-177">UpdateItem Operation</span><span class="sxs-lookup"><span data-stu-id="d30cb-177">UpdateItem operation</span></span>](updateitem-operation.md)

