---
title: CreateItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateItem
api_type:
- schema
ms.assetid: c3707feb-3fd4-4b8a-a68f-2abadd455163
description: Das CreateItem-Element definiert eine Anforderung zum Erstellen eines Elements im Exchange-Speicher.
ms.openlocfilehash: 9453323bff07749f5852dae75284c61c0895adb6
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353126"
---
# <a name="createitem"></a><span data-ttu-id="88002-103">CreateItem</span><span class="sxs-lookup"><span data-stu-id="88002-103">CreateItem</span></span>

<span data-ttu-id="88002-104">Das **CreateItem** -Element definiert eine Anforderung zum Erstellen eines Elements im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="88002-104">The **CreateItem** element defines a request to create an item in the Exchange store.</span></span> 
  
```xml
<CreateItem MessageDisposition="" SendMeetingInvitations="">
   <SavedItemFolderId/>
   <Items/>
</CreateItem>
```

<span data-ttu-id="88002-105">**CreateItemType**</span><span class="sxs-lookup"><span data-stu-id="88002-105">**CreateItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="88002-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="88002-106">Attributes and elements</span></span>

<span data-ttu-id="88002-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="88002-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="88002-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="88002-108">Attributes</span></span>

|<span data-ttu-id="88002-109">Attribut</span><span class="sxs-lookup"><span data-stu-id="88002-109">Attribute</span></span>|<span data-ttu-id="88002-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88002-110">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="88002-111">**"MessageDisposition"**</span><span class="sxs-lookup"><span data-stu-id="88002-111">**MessageDisposition**</span></span> <br/> |<span data-ttu-id="88002-112">Beschreibt, wie das Element behandelt werden sollen, nachdem er erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="88002-112">Describes how the item will be handled after it is created.</span></span> <span data-ttu-id="88002-113">Das Attribut ist erforderlich, damit e-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="88002-113">The attribute is required for e-mail messages.</span></span> <span data-ttu-id="88002-114">Dieses Attribut gilt nur für e-mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="88002-114">This attribute is only applicable to e-mail messages.</span></span>  <br/> |
|<span data-ttu-id="88002-115">**"SendMeetingInvitations"**</span><span class="sxs-lookup"><span data-stu-id="88002-115">**SendMeetingInvitations**</span></span> <br/> |<span data-ttu-id="88002-116">Beschreibt, wie Besprechungsanfragen behandelt werden, nachdem sie erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="88002-116">Describes how meeting requests are handled after they are created.</span></span> <span data-ttu-id="88002-117">Dieses Attribut ist für Kalenderelemente erforderlich.</span><span class="sxs-lookup"><span data-stu-id="88002-117">This attribute is required for calendar items.</span></span>  <br/> |
   
#### <a name="messagedisposition-attribute"></a><span data-ttu-id="88002-118">Attribut "MessageDisposition"</span><span class="sxs-lookup"><span data-stu-id="88002-118">MessageDisposition Attribute</span></span>

|<span data-ttu-id="88002-119">Wert</span><span class="sxs-lookup"><span data-stu-id="88002-119">Value</span></span>|<span data-ttu-id="88002-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88002-120">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="88002-121">SaveOnly</span><span class="sxs-lookup"><span data-stu-id="88002-121">SaveOnly</span></span>  <br/> |<span data-ttu-id="88002-122">Das Nachrichten-Element wird im Ordner gespeichert, die durch das Element [des SavedItemFolderId](saveditemfolderid.md) angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="88002-122">The message item is saved in the folder that is specified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span> <span data-ttu-id="88002-123">Nachrichten können später gesendet werden, mit der [den SendItem-Vorgang](senditem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="88002-123">Messages can be sent later by using the [SendItem operation](senditem-operation.md).</span></span> <span data-ttu-id="88002-124">Eine Element-ID wird in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="88002-124">An item identifier is returned in the response.</span></span> <span data-ttu-id="88002-125">Element-IDs werden für alle Elementtypen außer Nachrichtenelemente nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="88002-125">Item identifiers are not returned for any item types except for message items.</span></span> <span data-ttu-id="88002-126">Dazu gehören Antwortobjekte.</span><span class="sxs-lookup"><span data-stu-id="88002-126">This includes response objects.</span></span>  <br/> |
|<span data-ttu-id="88002-127">SendOnly</span><span class="sxs-lookup"><span data-stu-id="88002-127">SendOnly</span></span>  <br/> |<span data-ttu-id="88002-128">Das Element wird gesendet, jedoch keine Kopie im Ordner "Gesendete Elemente" gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="88002-128">The item is sent but no copy is saved in the Sent Items folder.</span></span> <span data-ttu-id="88002-129">Eine Element-ID wird nicht in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="88002-129">An item identifier is not returned in the response.</span></span><br/><br/><span data-ttu-id="88002-130">**Hinweis**: **CreateItem** unterstützt keine Zugriffsrechte für Stellvertretung, wenn die Option SendOnly verwendet wird, da mit dieser Option ein Zielordner angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="88002-130">**NOTE**: **CreateItem** does not support delegate access when the SendOnly option is used because a destination folder cannot be specified with this option.</span></span> <span data-ttu-id="88002-131">Die problemumgehung besteht darin, das Element erstellen, der Element-ID abgerufen, und klicken Sie dann den SendItem-Vorgang verwenden, um das Element gesendet.</span><span class="sxs-lookup"><span data-stu-id="88002-131">The workaround is to create the item, get the item identifier, and then use the SendItem operation to send the item.</span></span>           |
|<span data-ttu-id="88002-132">SendAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="88002-132">SendAndSaveCopy</span></span>  <br/> |<span data-ttu-id="88002-133">Das Element wird gesendet, und eine Kopie in den Ordner, der durch das Element [des SavedItemFolderId](saveditemfolderid.md) identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="88002-133">The item is sent and a copy is saved in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span> <span data-ttu-id="88002-134">Eine Element-ID wird nicht in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="88002-134">An item identifier is not returned in the response.</span></span><br/><br/><span data-ttu-id="88002-135">**Hinweis**: Besprechungsanfragen werden nicht gespeichert, zu dem Ordner, die von der [SavedItemFolderId](saveditemfolderid.md) -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="88002-135">**NOTE**: Meeting requests are not saved to the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) property.</span></span> <span data-ttu-id="88002-136">Für Kalenderfunktionen, nur das Speichern des Speicherorts für Kalenderelemente von der **SavedItemFolderId** -Eigenschaft angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="88002-136">For calendaring, only the save location for calendar items can be specified by the **SavedItemFolderId** property.</span></span> <span data-ttu-id="88002-137">Sie können nicht steuern, auf dem eine Besprechungsanfrage Element gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="88002-137">You cannot control where a meeting request item is saved.</span></span> <span data-ttu-id="88002-138">Nur die zugeordneten Kalenderelemente werden kopiert und in den Ordner, der die **SavedItemFolderId** -Eigenschaft identifizierte gespeichert.</span><span class="sxs-lookup"><span data-stu-id="88002-138">Only the associated calendar items are copied and saved into the folder that is identified by the **SavedItemFolderId** property.</span></span>           |
   
#### <a name="sendmeetinginvitations-attribute"></a><span data-ttu-id="88002-139">Attribut "SendMeetingInvitations"</span><span class="sxs-lookup"><span data-stu-id="88002-139">SendMeetingInvitations Attribute</span></span>

|<span data-ttu-id="88002-140">Wert</span><span class="sxs-lookup"><span data-stu-id="88002-140">Value</span></span>|<span data-ttu-id="88002-141">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88002-141">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="88002-142">SendToNone</span><span class="sxs-lookup"><span data-stu-id="88002-142">SendToNone</span></span>  <br/> |<span data-ttu-id="88002-143">Wenn das Element eine Besprechungsanfrage ist, wird es als ein Kalenderelement gespeichert, aber nicht gesendet.</span><span class="sxs-lookup"><span data-stu-id="88002-143">If the item is a meeting request, it is saved as a calendar item but not sent.</span></span>  <br/> |
|<span data-ttu-id="88002-144">SendOnlyToAll</span><span class="sxs-lookup"><span data-stu-id="88002-144">SendOnlyToAll</span></span>  <br/> |<span data-ttu-id="88002-145">Die Besprechungsanfrage wird an alle Teilnehmer gesendet, aber nicht im Ordner "Gesendete Elemente" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="88002-145">The meeting request is sent to all attendees but is not saved in the Sent Items folder.</span></span>  <br/> |
|<span data-ttu-id="88002-146">SendToAllAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="88002-146">SendToAllAndSaveCopy</span></span>  <br/> |<span data-ttu-id="88002-147">Senden von Besprechungsanfragen an alle Teilnehmer und eine Kopie in den Ordner, der durch das Element [des SavedItemFolderId](saveditemfolderid.md) identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="88002-147">The meeting request is sent to all attendees and a copy is saved in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="88002-148">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="88002-148">Child elements</span></span>

|<span data-ttu-id="88002-149">Element</span><span class="sxs-lookup"><span data-stu-id="88002-149">Element</span></span>|<span data-ttu-id="88002-150">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88002-150">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="88002-151">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="88002-151">SavedItemFolderId</span></span>](saveditemfolderid.md) <br/> |<span data-ttu-id="88002-152">Identifiziert den Zielordner, in dem ein neues Element erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="88002-152">Identifies the target folder where a new item can be created.</span></span> <span data-ttu-id="88002-153">Wenn das Attribut **"MessageDisposition"** auf SendOnly festgelegt ist, wird nur eine erstellte Nachricht gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="88002-153">If the **MessageDisposition** attribute is set to SendOnly, a created message will only be sent.</span></span> <span data-ttu-id="88002-154">Die Nachricht wird nicht im Ordner versetzt werden, die durch das Element [des SavedItemFolderId](saveditemfolderid.md) identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="88002-154">The message will not be put in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
|[<span data-ttu-id="88002-155">Items (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="88002-155">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="88002-156">Enthält ein Array von Elementen im Ordner zu erstellen, die durch das Element [des SavedItemFolderId](saveditemfolderid.md) identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="88002-156">Contains an array of items to create in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="88002-157">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="88002-157">Parent elements</span></span>

<span data-ttu-id="88002-158">Keine.</span><span class="sxs-lookup"><span data-stu-id="88002-158">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="88002-159">Hinweise</span><span class="sxs-lookup"><span data-stu-id="88002-159">Remarks</span></span>

<span data-ttu-id="88002-160">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="88002-160">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="88002-161">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="88002-161">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88002-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="88002-162">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="88002-163">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="88002-163">Schema Name</span></span>  <br/> |<span data-ttu-id="88002-164">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="88002-164">Messages schema</span></span>  <br/> |
|<span data-ttu-id="88002-165">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="88002-165">Validation File</span></span>  <br/> |<span data-ttu-id="88002-166">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="88002-166">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="88002-167">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="88002-167">Can be Empty</span></span>  <br/> |<span data-ttu-id="88002-168">False</span><span class="sxs-lookup"><span data-stu-id="88002-168">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="88002-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88002-169">See also</span></span>

- [<span data-ttu-id="88002-170">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="88002-170">CreateItemResponse</span></span>](createitemresponse.md)  
- [<span data-ttu-id="88002-171">CreateItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="88002-171">CreateItem operation</span></span>](createitem-operation.md)
- [<span data-ttu-id="88002-172">Erstellen von e-Mail-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="88002-172">Creating E-mail Messages</span></span>](http://msdn.microsoft.com/library/05bfb83c-2866-427d-a9fe-14ba3cb02793%28Office.15%29.aspx) 
- [<span data-ttu-id="88002-173">Creating Contacts (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="88002-173">Creating Contacts (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)  
- [<span data-ttu-id="88002-174">Erstellen von Aufgaben</span><span class="sxs-lookup"><span data-stu-id="88002-174">Creating Tasks</span></span>](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx) 
- [<span data-ttu-id="88002-175">Erstellen von Terminen</span><span class="sxs-lookup"><span data-stu-id="88002-175">Creating Appointments</span></span>](http://msdn.microsoft.com/library/2385391e-c9e7-4d45-b803-c4ff94d5c94e%28Office.15%29.aspx)

