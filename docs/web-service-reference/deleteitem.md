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
description: Das DeleteItem-Element definiert eine Anforderung zum Löschen eines Elements aus einem Postfach im Exchange-Speicher.
ms.openlocfilehash: de64787750c88c8a47bb69daddc0a1d2ebe8bde9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757932"
---
# <a name="deleteitem"></a><span data-ttu-id="fd436-103">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="fd436-103">DeleteItem</span></span>

<span data-ttu-id="fd436-104">Das **DeleteItem** -Element definiert eine Anforderung zum Löschen eines Elements aus einem Postfach im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="fd436-104">The **DeleteItem** element defines a request to delete an item from a mailbox in the Exchange store.</span></span> 
  
```XML
<DeleteItem DeleteType="" SendMeetingCancellations="" AffectedTaskOccurrences="" SuppressReadReceipts="">
   <ItemIds/>
</DeleteItem>
```

 <span data-ttu-id="fd436-105">**DeleteItemType**</span><span class="sxs-lookup"><span data-stu-id="fd436-105">**DeleteItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fd436-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fd436-106">Attributes and elements</span></span>

<span data-ttu-id="fd436-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fd436-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fd436-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="fd436-108">Attributes</span></span>

|<span data-ttu-id="fd436-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="fd436-109">**Attribute**</span></span>|<span data-ttu-id="fd436-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fd436-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fd436-111">**DeleteType**</span><span class="sxs-lookup"><span data-stu-id="fd436-111">**DeleteType**</span></span> <br/> |<span data-ttu-id="fd436-112">Beschreibt, wie ein Element gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="fd436-112">Describes how an item is deleted.</span></span> <span data-ttu-id="fd436-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fd436-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="fd436-114">**"SendMeetingCancellations"**</span><span class="sxs-lookup"><span data-stu-id="fd436-114">**SendMeetingCancellations**</span></span> <br/> |<span data-ttu-id="fd436-115">Beschreibt, ob eine Kalender Element Löschung an die Teilnehmer weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="fd436-115">Describes whether a calendar item deletion is communicated to attendees.</span></span> <span data-ttu-id="fd436-116">Dieses Attribut ist erforderlich, wenn die Elemente im Kalender gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="fd436-116">This attribute is required when calendar items are deleted.</span></span> <span data-ttu-id="fd436-117">Dieses Attribut ist optional, wenn nichtkalenderelemente gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="fd436-117">This attribute is optional if non-calendar items are deleted.</span></span>  <br/> |
|<span data-ttu-id="fd436-118">**"AffectedTaskOccurrences"**</span><span class="sxs-lookup"><span data-stu-id="fd436-118">**AffectedTaskOccurrences**</span></span> <br/> |<span data-ttu-id="fd436-119">Beschreibt, ob eine Aufgabeninstanz oder ein Master-Shape Aufgabe durch eine [DeleteItem Vorgang](deleteitem-operation.md)gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="fd436-119">Describes whether a task instance or a task master is deleted by a [DeleteItem operation](deleteitem-operation.md).</span></span> <span data-ttu-id="fd436-120">Dieses Attribut ist erforderlich, wenn Vorgänge gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="fd436-120">This attribute is required when tasks are deleted.</span></span> <span data-ttu-id="fd436-121">Dieses Attribut ist optional, wenn nicht Aufgabenelementen gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="fd436-121">This attribute is optional when non-task items are deleted.</span></span>  <br/> |
|<span data-ttu-id="fd436-122">**SuppressReadReceipts**</span><span class="sxs-lookup"><span data-stu-id="fd436-122">**SuppressReadReceipts**</span></span> <br/> |<span data-ttu-id="fd436-123">Gibt an, ob lesebestätigungen für das gelöschte Element unterdrückt werden.</span><span class="sxs-lookup"><span data-stu-id="fd436-123">Indicates whether read receipts for the deleted item are suppressed.</span></span> <span data-ttu-id="fd436-124">Der Textwert **true**, gibt an, dass die lesebestätigungen unterdrückt werden.</span><span class="sxs-lookup"><span data-stu-id="fd436-124">A text value of **true**, indicates that the read receipts are suppressed.</span></span> <span data-ttu-id="fd436-125">Der Wert **false** gibt an, dass die lesebestätigungen an den Absender gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd436-125">A value of **false** indicates that the read receipts are sent to the sender.</span></span> <span data-ttu-id="fd436-126">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="fd436-126">This attribute is optional.</span></span>  <br/> |
   
#### <a name="deletetype-attribute"></a><span data-ttu-id="fd436-127">DeleteType-Attribut</span><span class="sxs-lookup"><span data-stu-id="fd436-127">DeleteType attribute</span></span>

|<span data-ttu-id="fd436-128">**Wert**</span><span class="sxs-lookup"><span data-stu-id="fd436-128">**Value**</span></span>|<span data-ttu-id="fd436-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fd436-129">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fd436-130">HardDelete</span><span class="sxs-lookup"><span data-stu-id="fd436-130">HardDelete</span></span>  <br/> |<span data-ttu-id="fd436-131">Ein Element wird dauerhaft aus dem Speicher entfernt.</span><span class="sxs-lookup"><span data-stu-id="fd436-131">An item is permanently removed from the store.</span></span>  <br/> |
|<span data-ttu-id="fd436-132">SoftDelete</span><span class="sxs-lookup"><span data-stu-id="fd436-132">SoftDelete</span></span>  <br/> |<span data-ttu-id="fd436-133">Ein Element wird verschoben, um die Dumpster Wenn die Dumpster ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="fd436-133">An item is moved to the dumpster if the dumpster is enabled.</span></span>  <br/> |
|<span data-ttu-id="fd436-134">MoveToDeletedItems</span><span class="sxs-lookup"><span data-stu-id="fd436-134">MoveToDeletedItems</span></span>  <br/> |<span data-ttu-id="fd436-135">Ein Element wird in den Ordner Gelöschte Objekte verschoben.</span><span class="sxs-lookup"><span data-stu-id="fd436-135">An item is moved to the Deleted Items folder.</span></span>  <br/> |
   
#### <a name="sendmeetingcancellations-attribute"></a><span data-ttu-id="fd436-136">Attribut "SendMeetingCancellations"</span><span class="sxs-lookup"><span data-stu-id="fd436-136">SendMeetingCancellations attribute</span></span>

|<span data-ttu-id="fd436-137">**Wert**</span><span class="sxs-lookup"><span data-stu-id="fd436-137">**Value**</span></span>|<span data-ttu-id="fd436-138">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fd436-138">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fd436-139">SendToNone</span><span class="sxs-lookup"><span data-stu-id="fd436-139">SendToNone</span></span>  <br/> |<span data-ttu-id="fd436-140">Ein Kalenderelement wird gelöscht, ohne eine Absage senden.</span><span class="sxs-lookup"><span data-stu-id="fd436-140">A calendar item is deleted without sending a cancellation message.</span></span>  <br/> |
|<span data-ttu-id="fd436-141">SendOnlyToAll</span><span class="sxs-lookup"><span data-stu-id="fd436-141">SendOnlyToAll</span></span>  <br/> |<span data-ttu-id="fd436-142">Ein Kalenderelement wird gelöscht und eine Absage an alle Teilnehmer gesendet.</span><span class="sxs-lookup"><span data-stu-id="fd436-142">A calendar item is deleted and a cancellation message is sent to all attendees.</span></span>  <br/> |
|<span data-ttu-id="fd436-143">SendToAllAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="fd436-143">SendToAllAndSaveCopy</span></span>  <br/> |<span data-ttu-id="fd436-144">Ein Kalenderelement wird gelöscht und eine Absage an alle Teilnehmer gesendet.</span><span class="sxs-lookup"><span data-stu-id="fd436-144">A calendar item is deleted and a cancellation message is sent to all attendees.</span></span> <span data-ttu-id="fd436-145">Eine Kopie der Nachricht Abbruch wird im Ordner "Gesendete Elemente" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fd436-145">A copy of the cancellation message is saved in the Sent Items folder.</span></span>  <br/> |
   
#### <a name="affectedtaskoccurrences-attribute"></a><span data-ttu-id="fd436-146">Attribut "AffectedTaskOccurrences"</span><span class="sxs-lookup"><span data-stu-id="fd436-146">AffectedTaskOccurrences attribute</span></span>

|<span data-ttu-id="fd436-147">**Wert**</span><span class="sxs-lookup"><span data-stu-id="fd436-147">**Value**</span></span>|<span data-ttu-id="fd436-148">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fd436-148">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fd436-149">AllOccurrences</span><span class="sxs-lookup"><span data-stu-id="fd436-149">AllOccurrences</span></span>  <br/> |<span data-ttu-id="fd436-150">Anforderung für das Element löschen Löscht die Aufgabe Master-Shape, und daher alle Aufgabenserien, sind der master Aufgabe zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="fd436-150">A delete item request deletes the master task, and therefore all recurring tasks that are associated with the master task.</span></span>  <br/> |
|<span data-ttu-id="fd436-151">SpecifiedOccurrenceOnly</span><span class="sxs-lookup"><span data-stu-id="fd436-151">SpecifiedOccurrenceOnly</span></span>  <br/> |<span data-ttu-id="fd436-152">Anforderung für das Element löschen Löscht nur bestimmte Vorkommen eines Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="fd436-152">A delete item request deletes only specific occurrences of a task.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fd436-153">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fd436-153">Child elements</span></span>

|<span data-ttu-id="fd436-154">**Element**</span><span class="sxs-lookup"><span data-stu-id="fd436-154">**Element**</span></span>|<span data-ttu-id="fd436-155">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fd436-155">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fd436-156">Artikelnummern ein.</span><span class="sxs-lookup"><span data-stu-id="fd436-156">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="fd436-157">Enthält ein Array von Elementen, Vorkommen Elemente und master Terminserien aus einem Postfach im Exchange-Speicher zu löschen.</span><span class="sxs-lookup"><span data-stu-id="fd436-157">Contains an array of items, occurrence items, and recurring master items to delete from a mailbox in the Exchange store.</span></span> <span data-ttu-id="fd436-158">Die [DeleteItem Vorgang](deleteitem-operation.md) kann auf einem beliebigen Element ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fd436-158">The [DeleteItem operation](deleteitem-operation.md) can be performed on any item type.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fd436-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fd436-159">Parent elements</span></span>

<span data-ttu-id="fd436-160">Keine.</span><span class="sxs-lookup"><span data-stu-id="fd436-160">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fd436-161">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fd436-161">Remarks</span></span>

<span data-ttu-id="fd436-162">Die Optionen **MoveToDeletedItems** und **HardDelete** sind transaktional, was bedeutet, dass jeweils ein Webdienstaufruf abgeschlossen ist, die Datenbank hat das Element in den Ordner Gelöschte Objekte verschoben oder dauerhaft entfernt das Element aus der Exchange-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="fd436-162">The **MoveToDeletedItems** and **HardDelete** options are transactional, which means that by the time a Web service call completes, the database has moved the item to the Deleted Items folder or permanently removed the item from the Exchange database.</span></span> <span data-ttu-id="fd436-163">Dieses Verhalten gilt für MicrosoftExchange Server 2007 und Exchange Server 2010.</span><span class="sxs-lookup"><span data-stu-id="fd436-163">This behavior is the same for MicrosoftExchange Server 2007 and Exchange Server 2010.</span></span> 
  
<span data-ttu-id="fd436-164">Die Option **SoftDelete** funktioniert anders für andere Versionen von Exchange.</span><span class="sxs-lookup"><span data-stu-id="fd436-164">The **SoftDelete** option works differently for different target versions of Exchange.</span></span> <span data-ttu-id="fd436-165">**SoftDelete** für Exchange 2007 legt etwas auf das Element, das in der Exchange-Datenbank angibt, die das Element verschoben werden die Dumpster Ordner zu einem unbestimmten Zeitpunkt in der Zukunft.</span><span class="sxs-lookup"><span data-stu-id="fd436-165">**SoftDelete** for Exchange 2007 sets a bit on the item that indicates to the Exchange database that the item will be moved to the dumpster folder at an indeterminate time in the future.</span></span> <span data-ttu-id="fd436-166">**SoftDelete** für Exchange 2010 sofort verschoben wird das Element, das die Dumpster.</span><span class="sxs-lookup"><span data-stu-id="fd436-166">**SoftDelete** for Exchange 2010 immediately moves the item to the dumpster.</span></span> <span data-ttu-id="fd436-167">**SoftDelete** ist keine Option zum Ordner löschen.</span><span class="sxs-lookup"><span data-stu-id="fd436-167">**SoftDelete** is not an option for folder deletion.</span></span> <span data-ttu-id="fd436-168">**SoftDelete** durchqueren Suchvorgänge für Elemente und Ordner werden keine Ergebnisse zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fd436-168">**SoftDelete** traversal searches for items and folders will not return any results.</span></span> 
  
<span data-ttu-id="fd436-169">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="fd436-169">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fd436-170">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="fd436-170">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fd436-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="fd436-171">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fd436-172">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fd436-172">Schema Name</span></span>  <br/> |<span data-ttu-id="fd436-173">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="fd436-173">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fd436-174">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fd436-174">Validation File</span></span>  <br/> |<span data-ttu-id="fd436-175">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="fd436-175">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fd436-176">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="fd436-176">Can be Empty</span></span>  <br/> |<span data-ttu-id="fd436-177">False</span><span class="sxs-lookup"><span data-stu-id="fd436-177">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fd436-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd436-178">See also</span></span>

- [<span data-ttu-id="fd436-179">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="fd436-179">DeleteItemResponse</span></span>](deleteitemresponse.md)  
- [<span data-ttu-id="fd436-180">DeleteItem-Operation</span><span class="sxs-lookup"><span data-stu-id="fd436-180">DeleteItem operation</span></span>](deleteitem-operation.md)

