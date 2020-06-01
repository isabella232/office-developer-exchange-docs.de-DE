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
ms.openlocfilehash: 43821db58457ffce22be918a7ba6427f57230010
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466570"
---
# <a name="updateitem"></a><span data-ttu-id="9602f-103">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="9602f-103">UpdateItem</span></span>

<span data-ttu-id="9602f-104">Das **UpdateItem** -Element definiert eine Anforderung zum Aktualisieren eines Elements in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="9602f-104">The **UpdateItem** element defines a request to update an item in a mailbox.</span></span> 
  
```XML
<UpdateItem ConflictResolution="" MessageDisposition="" SendMeetingInvitationsOrCancellations="" SuppressReadReceipts="">
   <SavedItemFolderId/>
   <ItemChanges/>
</UpdateItem>
```

 <span data-ttu-id="9602f-105">**UpdateItemType**</span><span class="sxs-lookup"><span data-stu-id="9602f-105">**UpdateItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9602f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9602f-106">Attributes and elements</span></span>

<span data-ttu-id="9602f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9602f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9602f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9602f-108">Attributes</span></span>

|<span data-ttu-id="9602f-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9602f-109">**Attribute**</span></span>|<span data-ttu-id="9602f-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9602f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9602f-111">**ConflictResolution**</span><span class="sxs-lookup"><span data-stu-id="9602f-111">**ConflictResolution**</span></span> <br/> |<span data-ttu-id="9602f-112">Gibt den Typ der Konfliktlösung an, die während einer Aktualisierung versucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="9602f-112">Identifies the type of conflict resolution to try during an update.</span></span> <span data-ttu-id="9602f-113">Der Standardwert ist autoresolve.</span><span class="sxs-lookup"><span data-stu-id="9602f-113">The default value is AutoResolve.</span></span>  <br/> |
|<span data-ttu-id="9602f-114">**MessageDisposition**</span><span class="sxs-lookup"><span data-stu-id="9602f-114">**MessageDisposition**</span></span> <br/> |<span data-ttu-id="9602f-115">Beschreibt, wie das Element nach seiner Aktualisierung behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="9602f-115">Describes how the item will be handled after it is updated.</span></span> <span data-ttu-id="9602f-116">Das **MessageDisposition** -Attribut ist für Nachrichtenelemente erforderlich, einschließlich Besprechungsnachrichten wie Besprechungsabsagen, Besprechungsanfragen und Besprechungsantworten.</span><span class="sxs-lookup"><span data-stu-id="9602f-116">The **MessageDisposition** attribute is required for message items, including meeting messages such as meeting cancellations, meeting requests, and meeting responses.</span></span>  <br/> |
|<span data-ttu-id="9602f-117">**SendMeetingInvitationsOrCancellations**</span><span class="sxs-lookup"><span data-stu-id="9602f-117">**SendMeetingInvitationsOrCancellations**</span></span> <br/> |<span data-ttu-id="9602f-118">Beschreibt, wie Besprechungsaktualisierungen mitgeteilt werden, nachdem ein Kalenderelement aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9602f-118">Describes how meeting updates are communicated after a calendar item is updated.</span></span> <span data-ttu-id="9602f-119">Dieses Attribut ist für Kalenderelemente und Kalenderelement vorkommen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9602f-119">This attribute is required for calendar items and calendar item occurrences.</span></span>  <br/> |
|<span data-ttu-id="9602f-120">**SuppressReadReceipts**</span><span class="sxs-lookup"><span data-stu-id="9602f-120">**SuppressReadReceipts**</span></span> <br/> |<span data-ttu-id="9602f-121">Gibt an, ob Lesebestätigungen für das aktualisierte Element unterdrückt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9602f-121">Indicates whether read receipts for the updated item should be suppressed.</span></span> <span data-ttu-id="9602f-122">Der Textwert **true** gibt an, dass Lesebestätigungen unterdrückt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9602f-122">A text value of **true** indicates that read receipts should be suppressed.</span></span> <span data-ttu-id="9602f-123">Der Wert **false** gibt an, dass die Lesebestätigungen an den Absender gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="9602f-123">A value of **false** indicates that the read receipts will be sent to the sender.</span></span> <span data-ttu-id="9602f-124">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="9602f-124">This attribute is optional.</span></span>  <br/> <span data-ttu-id="9602f-125">Dieses Attribut wurde in Exchange Server 2013 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9602f-125">This attribute was introduced in Exchange Server 2013 SP1.</span></span>  <br/> |
   
#### <a name="conflictresolution-attribute"></a><span data-ttu-id="9602f-126">ConflictResolution-Attribut</span><span class="sxs-lookup"><span data-stu-id="9602f-126">ConflictResolution Attribute</span></span>

|<span data-ttu-id="9602f-127">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9602f-127">**Value**</span></span>|<span data-ttu-id="9602f-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9602f-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9602f-129">NeverOverwrite</span><span class="sxs-lookup"><span data-stu-id="9602f-129">NeverOverwrite</span></span>  <br/> |<span data-ttu-id="9602f-130">Wenn ein Konflikt vorliegt, schlägt der Aktualisierungsvorgang fehl, und es wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9602f-130">If there is a conflict, the update operation fails and an error is returned.</span></span>  <br/> |
|<span data-ttu-id="9602f-131">Alle automatisch auflösen</span><span class="sxs-lookup"><span data-stu-id="9602f-131">AutoResolve</span></span>  <br/> |<span data-ttu-id="9602f-132">Der Aktualisierungsvorgang löst alle Konflikte automatisch auf.</span><span class="sxs-lookup"><span data-stu-id="9602f-132">The update operation automatically resolves any conflict.</span></span>  <br/> |
|<span data-ttu-id="9602f-133">AlwaysOverwrite</span><span class="sxs-lookup"><span data-stu-id="9602f-133">AlwaysOverwrite</span></span>  <br/> |<span data-ttu-id="9602f-134">Wenn ein Konflikt vorliegt, werden Informationen vom Aktualisierungsvorgang überschrieben.</span><span class="sxs-lookup"><span data-stu-id="9602f-134">If there is a conflict, the update operation will overwrite information.</span></span>  <br/> |
   
#### <a name="messagedisposition-attribute"></a><span data-ttu-id="9602f-135">MessageDisposition-Attribut</span><span class="sxs-lookup"><span data-stu-id="9602f-135">MessageDisposition Attribute</span></span>

|<span data-ttu-id="9602f-136">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9602f-136">**Value**</span></span>|<span data-ttu-id="9602f-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9602f-137">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9602f-138">SaveOnly</span><span class="sxs-lookup"><span data-stu-id="9602f-138">SaveOnly</span></span>  <br/> |<span data-ttu-id="9602f-139">Das Element wird aktualisiert und in seinem aktuellen Ordner zurückgespeichert.</span><span class="sxs-lookup"><span data-stu-id="9602f-139">The item is updated and saved back to its current folder.</span></span>  <br/> |
|<span data-ttu-id="9602f-140">SendOnly</span><span class="sxs-lookup"><span data-stu-id="9602f-140">SendOnly</span></span>  <br/> |<span data-ttu-id="9602f-141">Das Element wird aktualisiert und gesendet, aber es wird keine Kopie gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9602f-141">The item is updated and sent but no copy is saved.</span></span>  <br/> |
|<span data-ttu-id="9602f-142">SendAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="9602f-142">SendAndSaveCopy</span></span>  <br/> |<span data-ttu-id="9602f-143">Das Element wird aktualisiert, und eine Kopie wird in dem durch das [SavedItemFolderId](saveditemfolderid.md) -Element identifizierten Ordner gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9602f-143">The item is updated and a copy is saved in the folder identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
   
#### <a name="sendmeetinginvitationsorcancellations-attribute"></a><span data-ttu-id="9602f-144">SendMeetingInvitationsOrCancellations-Attribut</span><span class="sxs-lookup"><span data-stu-id="9602f-144">SendMeetingInvitationsOrCancellations Attribute</span></span>

|<span data-ttu-id="9602f-145">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9602f-145">**Value**</span></span>|<span data-ttu-id="9602f-146">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9602f-146">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9602f-147">SendToNone</span><span class="sxs-lookup"><span data-stu-id="9602f-147">SendToNone</span></span>  <br/> |<span data-ttu-id="9602f-148">Das Kalenderelement wird aktualisiert, aber Updates werden nicht an die Teilnehmer gesendet.</span><span class="sxs-lookup"><span data-stu-id="9602f-148">The calendar item is updated but updates are not sent to attendees.</span></span>  <br/> |
|<span data-ttu-id="9602f-149">SendOnlyToAll</span><span class="sxs-lookup"><span data-stu-id="9602f-149">SendOnlyToAll</span></span>  <br/> |<span data-ttu-id="9602f-150">Das Kalenderelement wird aktualisiert, und das Besprechungs Update wird an alle Teilnehmer gesendet, aber nicht im Ordner "Gesendete Elemente" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9602f-150">The calendar item is updated and the meeting update is sent to all attendees but is not saved in the Sent Items folder.</span></span>  <br/> |
|<span data-ttu-id="9602f-151">SendOnlyToChanged</span><span class="sxs-lookup"><span data-stu-id="9602f-151">SendOnlyToChanged</span></span>  <br/> |<span data-ttu-id="9602f-152">Das Kalenderelement wird aktualisiert, und das Besprechungs Update wird nur an Teilnehmer gesendet, die von der Änderung in der Besprechung betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="9602f-152">The calendar item is updated and the meeting update is sent only to attendees that are affected by the change in the meeting.</span></span>  <br/> |
|<span data-ttu-id="9602f-153">SendToAllAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="9602f-153">SendToAllAndSaveCopy</span></span>  <br/> |<span data-ttu-id="9602f-154">Das Kalenderelement wird aktualisiert, das Besprechungs Update wird an alle Teilnehmer gesendet, und eine Kopie wird im Ordner "Gesendete Elemente" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9602f-154">The calendar item is updated, the meeting update is sent to all attendees, and a copy is saved in the Sent Items folder.</span></span>  <br/> |
|<span data-ttu-id="9602f-155">SendToChangedAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="9602f-155">SendToChangedAndSaveCopy</span></span>  <br/> |<span data-ttu-id="9602f-156">Das Kalenderelement wird aktualisiert, das Besprechungs Update wird an alle Teilnehmer gesendet, die von der Änderung in der Besprechung betroffen sind, und eine Kopie wird im Ordner "Gesendete Elemente" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9602f-156">The calendar item is updated, the meeting update is sent to all attendees that are affected by the change in the meeting, and a copy is saved in the Sent Items folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9602f-157">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9602f-157">Child elements</span></span>

|<span data-ttu-id="9602f-158">**Element**</span><span class="sxs-lookup"><span data-stu-id="9602f-158">**Element**</span></span>|<span data-ttu-id="9602f-159">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9602f-159">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9602f-160">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="9602f-160">SavedItemFolderId</span></span>](saveditemfolderid.md) <br/> |<span data-ttu-id="9602f-161">Identifiziert den Zielordner für Vorgänge, die Elemente im Exchange-Informationsspeicher aktualisieren, senden und erstellen.</span><span class="sxs-lookup"><span data-stu-id="9602f-161">Identifies the target folder for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9602f-162">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="9602f-162">ItemChanges</span></span>](itemchanges.md) <br/> |<span data-ttu-id="9602f-163">Enthält ein Array von [ItemChange](itemchange.md) -Elementen, mit denen Elemente identifiziert werden, und die Updates, die auf die Elemente angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9602f-163">Contains an array of [ItemChange](itemchange.md) elements that identify items and the updates to apply to the items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9602f-164">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9602f-164">Parent elements</span></span>

<span data-ttu-id="9602f-165">Keine.</span><span class="sxs-lookup"><span data-stu-id="9602f-165">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9602f-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9602f-166">Remarks</span></span>

<span data-ttu-id="9602f-167">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9602f-167">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9602f-168">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="9602f-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9602f-169">Namespace</span><span class="sxs-lookup"><span data-stu-id="9602f-169">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9602f-170">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9602f-170">Schema Name</span></span>  <br/> |<span data-ttu-id="9602f-171">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="9602f-171">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9602f-172">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9602f-172">Validation File</span></span>  <br/> |<span data-ttu-id="9602f-173">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="9602f-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9602f-174">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9602f-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="9602f-175">False</span><span class="sxs-lookup"><span data-stu-id="9602f-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9602f-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9602f-176">See also</span></span>



[<span data-ttu-id="9602f-177">UpdateItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9602f-177">UpdateItem operation</span></span>](updateitem-operation.md)

