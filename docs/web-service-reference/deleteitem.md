---
title: DeleteItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteItem
api_type:
- schema
ms.assetid: 055cdee8-3c7d-47db-9f27-740f4a674729
description: Das DeleteItem-Element definiert eine Anforderung zum Löschen eines Elements aus einem Postfach im Exchange-Informationsspeicher.
ms.openlocfilehash: ed13ee32b487f49740aed80e8705257d3e2e6938
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529203"
---
# <a name="deleteitem"></a><span data-ttu-id="fe6b8-103">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="fe6b8-103">DeleteItem</span></span>

<span data-ttu-id="fe6b8-104">Das **DeleteItem** -Element definiert eine Anforderung zum Löschen eines Elements aus einem Postfach im Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-104">The **DeleteItem** element defines a request to delete an item from a mailbox in the Exchange store.</span></span> 
  
```XML
<DeleteItem DeleteType="" SendMeetingCancellations="" AffectedTaskOccurrences="" SuppressReadReceipts="">
   <ItemIds/>
</DeleteItem>
```

 <span data-ttu-id="fe6b8-105">**DeleteItemType**</span><span class="sxs-lookup"><span data-stu-id="fe6b8-105">**DeleteItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fe6b8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fe6b8-106">Attributes and elements</span></span>

<span data-ttu-id="fe6b8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fe6b8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="fe6b8-108">Attributes</span></span>

|<span data-ttu-id="fe6b8-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="fe6b8-109">**Attribute**</span></span>|<span data-ttu-id="fe6b8-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fe6b8-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fe6b8-111">**Deletetypeharddelete**</span><span class="sxs-lookup"><span data-stu-id="fe6b8-111">**DeleteType**</span></span> <br/> |<span data-ttu-id="fe6b8-112">Beschreibt, wie ein Element gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-112">Describes how an item is deleted.</span></span> <span data-ttu-id="fe6b8-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="fe6b8-114">**SendMeetingCancellations**</span><span class="sxs-lookup"><span data-stu-id="fe6b8-114">**SendMeetingCancellations**</span></span> <br/> |<span data-ttu-id="fe6b8-115">Beschreibt, ob ein Löschen eines Kalenderelements an die Teilnehmer kommuniziert wird.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-115">Describes whether a calendar item deletion is communicated to attendees.</span></span> <span data-ttu-id="fe6b8-116">Dieses Attribut ist erforderlich, wenn Kalenderelemente gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-116">This attribute is required when calendar items are deleted.</span></span> <span data-ttu-id="fe6b8-117">Dieses Attribut ist optional, wenn nicht Kalenderelemente gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-117">This attribute is optional if non-calendar items are deleted.</span></span>  <br/> |
|<span data-ttu-id="fe6b8-118">**AffectedTaskOccurrences**</span><span class="sxs-lookup"><span data-stu-id="fe6b8-118">**AffectedTaskOccurrences**</span></span> <br/> |<span data-ttu-id="fe6b8-119">Beschreibt, ob eine Aufgabeninstanz oder ein Aufgaben Master durch einen [DeleteItem-Vorgang](deleteitem-operation.md)gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-119">Describes whether a task instance or a task master is deleted by a [DeleteItem operation](deleteitem-operation.md).</span></span> <span data-ttu-id="fe6b8-120">Dieses Attribut ist erforderlich, wenn Aufgaben gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-120">This attribute is required when tasks are deleted.</span></span> <span data-ttu-id="fe6b8-121">Dieses Attribut ist optional, wenn nicht Aufgabenelemente gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-121">This attribute is optional when non-task items are deleted.</span></span>  <br/> |
|<span data-ttu-id="fe6b8-122">**SuppressReadReceipts**</span><span class="sxs-lookup"><span data-stu-id="fe6b8-122">**SuppressReadReceipts**</span></span> <br/> |<span data-ttu-id="fe6b8-123">Gibt an, ob Lesebestätigungen für das gelöschte Element unterdrückt werden.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-123">Indicates whether read receipts for the deleted item are suppressed.</span></span> <span data-ttu-id="fe6b8-124">Der Textwert **true**, gibt an, dass die Lesebestätigungen unterdrückt werden.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-124">A text value of **true**, indicates that the read receipts are suppressed.</span></span> <span data-ttu-id="fe6b8-125">Der Wert **false** gibt an, dass die Lesebestätigungen an den Absender gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-125">A value of **false** indicates that the read receipts are sent to the sender.</span></span> <span data-ttu-id="fe6b8-126">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-126">This attribute is optional.</span></span>  <br/> |
   
#### <a name="deletetype-attribute"></a><span data-ttu-id="fe6b8-127">DeleteType-Attribut</span><span class="sxs-lookup"><span data-stu-id="fe6b8-127">DeleteType attribute</span></span>

|<span data-ttu-id="fe6b8-128">**Wert**</span><span class="sxs-lookup"><span data-stu-id="fe6b8-128">**Value**</span></span>|<span data-ttu-id="fe6b8-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fe6b8-129">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fe6b8-130">HardDelete</span><span class="sxs-lookup"><span data-stu-id="fe6b8-130">HardDelete</span></span>  <br/> |<span data-ttu-id="fe6b8-131">Ein Element wird dauerhaft aus dem Speicher entfernt.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-131">An item is permanently removed from the store.</span></span>  <br/> |
|<span data-ttu-id="fe6b8-132">SoftDelete</span><span class="sxs-lookup"><span data-stu-id="fe6b8-132">SoftDelete</span></span>  <br/> |<span data-ttu-id="fe6b8-133">Ein Element wird in den Papierkorb verschoben, wenn der Papierkorb aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-133">An item is moved to the dumpster if the dumpster is enabled.</span></span>  <br/> |
|<span data-ttu-id="fe6b8-134">MoveToDeletedItems</span><span class="sxs-lookup"><span data-stu-id="fe6b8-134">MoveToDeletedItems</span></span>  <br/> |<span data-ttu-id="fe6b8-135">Ein Element wird in den Ordner "Gelöschte Elemente" verschoben.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-135">An item is moved to the Deleted Items folder.</span></span>  <br/> |
   
#### <a name="sendmeetingcancellations-attribute"></a><span data-ttu-id="fe6b8-136">SendMeetingCancellations-Attribut</span><span class="sxs-lookup"><span data-stu-id="fe6b8-136">SendMeetingCancellations attribute</span></span>

|<span data-ttu-id="fe6b8-137">**Wert**</span><span class="sxs-lookup"><span data-stu-id="fe6b8-137">**Value**</span></span>|<span data-ttu-id="fe6b8-138">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fe6b8-138">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fe6b8-139">SendToNone</span><span class="sxs-lookup"><span data-stu-id="fe6b8-139">SendToNone</span></span>  <br/> |<span data-ttu-id="fe6b8-140">Ein Kalenderelement wird gelöscht, ohne eine Abbruch Nachricht zu senden.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-140">A calendar item is deleted without sending a cancellation message.</span></span>  <br/> |
|<span data-ttu-id="fe6b8-141">SendOnlyToAll</span><span class="sxs-lookup"><span data-stu-id="fe6b8-141">SendOnlyToAll</span></span>  <br/> |<span data-ttu-id="fe6b8-142">Ein Kalenderelement wird gelöscht, und eine Abbruchmeldung wird an alle Teilnehmer gesendet.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-142">A calendar item is deleted and a cancellation message is sent to all attendees.</span></span>  <br/> |
|<span data-ttu-id="fe6b8-143">SendToAllAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="fe6b8-143">SendToAllAndSaveCopy</span></span>  <br/> |<span data-ttu-id="fe6b8-144">Ein Kalenderelement wird gelöscht, und eine Abbruchmeldung wird an alle Teilnehmer gesendet.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-144">A calendar item is deleted and a cancellation message is sent to all attendees.</span></span> <span data-ttu-id="fe6b8-145">Eine Kopie der Abbruch Nachricht wird im Ordner "Gesendete Elemente" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-145">A copy of the cancellation message is saved in the Sent Items folder.</span></span>  <br/> |
   
#### <a name="affectedtaskoccurrences-attribute"></a><span data-ttu-id="fe6b8-146">AffectedTaskOccurrences-Attribut</span><span class="sxs-lookup"><span data-stu-id="fe6b8-146">AffectedTaskOccurrences attribute</span></span>

|<span data-ttu-id="fe6b8-147">**Wert**</span><span class="sxs-lookup"><span data-stu-id="fe6b8-147">**Value**</span></span>|<span data-ttu-id="fe6b8-148">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fe6b8-148">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fe6b8-149">Allvorkommen</span><span class="sxs-lookup"><span data-stu-id="fe6b8-149">AllOccurrences</span></span>  <br/> |<span data-ttu-id="fe6b8-150">Eine Delete Item-Anforderung löscht den hauptvorgang und somit alle wiederkehrenden Vorgänge, die dem hauptvorgang zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-150">A delete item request deletes the master task, and therefore all recurring tasks that are associated with the master task.</span></span>  <br/> |
|<span data-ttu-id="fe6b8-151">SpecifiedOccurrenceOnly</span><span class="sxs-lookup"><span data-stu-id="fe6b8-151">SpecifiedOccurrenceOnly</span></span>  <br/> |<span data-ttu-id="fe6b8-152">Eine Delete Item-Anforderung löscht nur bestimmte Vorkommen eines Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-152">A delete item request deletes only specific occurrences of a task.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fe6b8-153">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fe6b8-153">Child elements</span></span>

|<span data-ttu-id="fe6b8-154">**Element**</span><span class="sxs-lookup"><span data-stu-id="fe6b8-154">**Element**</span></span>|<span data-ttu-id="fe6b8-155">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fe6b8-155">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fe6b8-156">ItemIds</span><span class="sxs-lookup"><span data-stu-id="fe6b8-156">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="fe6b8-157">Enthält ein Array von Elementen, vorkommen-Elementen und wiederkehrenden Master Elementen, die aus einem Postfach im Exchange-Informationsspeicher gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-157">Contains an array of items, occurrence items, and recurring master items to delete from a mailbox in the Exchange store.</span></span> <span data-ttu-id="fe6b8-158">Der [DeleteItem-Vorgang](deleteitem-operation.md) kann für beliebige Elementtypen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-158">The [DeleteItem operation](deleteitem-operation.md) can be performed on any item type.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fe6b8-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fe6b8-159">Parent elements</span></span>

<span data-ttu-id="fe6b8-160">Keine.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-160">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fe6b8-161">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe6b8-161">Remarks</span></span>

<span data-ttu-id="fe6b8-162">Die **MoveToDeletedItems** -und **HardDelete** -Optionen sind transaktional, was bedeutet, dass die Datenbank zum Zeitpunkt des Abschlusses eines Webdienstaufrufs das Element in den Ordner "Gelöschte Elemente" verschoben oder das Element endgültig aus der Exchange-Datenbank entfernt hat.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-162">The **MoveToDeletedItems** and **HardDelete** options are transactional, which means that by the time a Web service call completes, the database has moved the item to the Deleted Items folder or permanently removed the item from the Exchange database.</span></span> <span data-ttu-id="fe6b8-163">Dieses Verhalten ist für Microsoft Exchange Server 2007 und Exchange Server 2010 identisch.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-163">This behavior is the same for MicrosoftExchange Server 2007 and Exchange Server 2010.</span></span> 
  
<span data-ttu-id="fe6b8-164">Die Option **SoftDelete** kann für unterschiedliche Zielversionen von Exchange anders verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-164">The **SoftDelete** option works differently for different target versions of Exchange.</span></span> <span data-ttu-id="fe6b8-165">**SoftDelete** für Exchange 2007 legt ein Bit für das Element fest, das der Exchange-Datenbank angibt, dass das Element zu einem bestimmten Zeitpunkt in der Zukunft in den Ordner "Papierkorb" verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-165">**SoftDelete** for Exchange 2007 sets a bit on the item that indicates to the Exchange database that the item will be moved to the dumpster folder at an indeterminate time in the future.</span></span> <span data-ttu-id="fe6b8-166">**SoftDelete** für Exchange 2010 verschiebt das Element sofort in den Papierkorb.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-166">**SoftDelete** for Exchange 2010 immediately moves the item to the dumpster.</span></span> <span data-ttu-id="fe6b8-167">**SoftDelete** ist keine Option für das Löschen von Ordnern.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-167">**SoftDelete** is not an option for folder deletion.</span></span> <span data-ttu-id="fe6b8-168">**SoftDelete** Traversal sucht nach Elementen und Ordnern werden keine Ergebnisse zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-168">**SoftDelete** traversal searches for items and folders will not return any results.</span></span> 
  
<span data-ttu-id="fe6b8-169">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="fe6b8-169">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fe6b8-170">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="fe6b8-170">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fe6b8-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="fe6b8-171">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fe6b8-172">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fe6b8-172">Schema Name</span></span>  <br/> |<span data-ttu-id="fe6b8-173">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="fe6b8-173">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fe6b8-174">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fe6b8-174">Validation File</span></span>  <br/> |<span data-ttu-id="fe6b8-175">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="fe6b8-175">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fe6b8-176">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="fe6b8-176">Can be Empty</span></span>  <br/> |<span data-ttu-id="fe6b8-177">False</span><span class="sxs-lookup"><span data-stu-id="fe6b8-177">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fe6b8-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe6b8-178">See also</span></span>

- [<span data-ttu-id="fe6b8-179">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="fe6b8-179">DeleteItemResponse</span></span>](deleteitemresponse.md)  
- [<span data-ttu-id="fe6b8-180">DeleteItem-Operation</span><span class="sxs-lookup"><span data-stu-id="fe6b8-180">DeleteItem operation</span></span>](deleteitem-operation.md)

