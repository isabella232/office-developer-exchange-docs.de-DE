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
description: Das CreateItem-Element definiert eine Anforderung zum Erstellen eines Elements in der Exchange-Informationsspeicher.
ms.openlocfilehash: 235664b7baeceeccb14135fd346123f0f7d99346
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527061"
---
# <a name="createitem"></a><span data-ttu-id="6177d-103">CreateItem</span><span class="sxs-lookup"><span data-stu-id="6177d-103">CreateItem</span></span>

<span data-ttu-id="6177d-104">Das **CreateItem** -Element definiert eine Anforderung zum Erstellen eines Elements in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="6177d-104">The **CreateItem** element defines a request to create an item in the Exchange store.</span></span> 
  
```xml
<CreateItem MessageDisposition="" SendMeetingInvitations="">
   <SavedItemFolderId/>
   <Items/>
</CreateItem>
```

<span data-ttu-id="6177d-105">**CreateItemType**</span><span class="sxs-lookup"><span data-stu-id="6177d-105">**CreateItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="6177d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6177d-106">Attributes and elements</span></span>

<span data-ttu-id="6177d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6177d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6177d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6177d-108">Attributes</span></span>

|<span data-ttu-id="6177d-109">Attribut</span><span class="sxs-lookup"><span data-stu-id="6177d-109">Attribute</span></span>|<span data-ttu-id="6177d-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6177d-110">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="6177d-111">**MessageDisposition**</span><span class="sxs-lookup"><span data-stu-id="6177d-111">**MessageDisposition**</span></span> <br/> |<span data-ttu-id="6177d-112">Beschreibt, wie das Element nach seiner Erstellung behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="6177d-112">Describes how the item will be handled after it is created.</span></span> <span data-ttu-id="6177d-113">Das Attribut ist für e-Mail-Nachrichten erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6177d-113">The attribute is required for e-mail messages.</span></span> <span data-ttu-id="6177d-114">Dieses Attribut gilt nur für e-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="6177d-114">This attribute is only applicable to e-mail messages.</span></span>  <br/> |
|<span data-ttu-id="6177d-115">**SendMeetingInvitations**</span><span class="sxs-lookup"><span data-stu-id="6177d-115">**SendMeetingInvitations**</span></span> <br/> |<span data-ttu-id="6177d-116">Beschreibt, wie Besprechungsanfragen verarbeitet werden, nachdem Sie erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="6177d-116">Describes how meeting requests are handled after they are created.</span></span> <span data-ttu-id="6177d-117">Dieses Attribut ist für Kalenderelemente erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6177d-117">This attribute is required for calendar items.</span></span>  <br/> |
   
#### <a name="messagedisposition-attribute"></a><span data-ttu-id="6177d-118">MessageDisposition-Attribut</span><span class="sxs-lookup"><span data-stu-id="6177d-118">MessageDisposition Attribute</span></span>

|<span data-ttu-id="6177d-119">Wert</span><span class="sxs-lookup"><span data-stu-id="6177d-119">Value</span></span>|<span data-ttu-id="6177d-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6177d-120">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="6177d-121">SaveOnly</span><span class="sxs-lookup"><span data-stu-id="6177d-121">SaveOnly</span></span>  <br/> |<span data-ttu-id="6177d-122">Das Nachrichtenelement wird in dem Ordner gespeichert, der durch das [SavedItemFolderId](saveditemfolderid.md) -Element angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6177d-122">The message item is saved in the folder that is specified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span> <span data-ttu-id="6177d-123">Nachrichten können später mit dem SendItem- [Vorgang](senditem-operation.md)gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="6177d-123">Messages can be sent later by using the [SendItem operation](senditem-operation.md).</span></span> <span data-ttu-id="6177d-124">In der Antwort wird ein Elementbezeichner zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6177d-124">An item identifier is returned in the response.</span></span> <span data-ttu-id="6177d-125">Element-IDs werden nicht für Elementtypen mit Ausnahme von Nachrichtenelementen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6177d-125">Item identifiers are not returned for any item types except for message items.</span></span> <span data-ttu-id="6177d-126">Dies umfasst Antwortobjekte.</span><span class="sxs-lookup"><span data-stu-id="6177d-126">This includes response objects.</span></span>  <br/> |
|<span data-ttu-id="6177d-127">SendOnly</span><span class="sxs-lookup"><span data-stu-id="6177d-127">SendOnly</span></span>  <br/> |<span data-ttu-id="6177d-128">Das Element wird gesendet, aber keine Kopie wird im Ordner "Gesendete Elemente" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6177d-128">The item is sent but no copy is saved in the Sent Items folder.</span></span> <span data-ttu-id="6177d-129">In der Antwort wird kein Elementbezeichner zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6177d-129">An item identifier is not returned in the response.</span></span><br/><br/><span data-ttu-id="6177d-130">**Hinweis**: **CreateItem** unterstützt keinen Stellvertretungszugriff, wenn die Option SendOnly verwendet wird, da ein Zielordner mit dieser Option nicht angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="6177d-130">**NOTE**: **CreateItem** does not support delegate access when the SendOnly option is used because a destination folder cannot be specified with this option.</span></span> <span data-ttu-id="6177d-131">Die Problemumgehung besteht darin, das Element zu erstellen, den Elementbezeichner abzurufen und dann mit dem SendItem-Vorgang das Element zu senden.</span><span class="sxs-lookup"><span data-stu-id="6177d-131">The workaround is to create the item, get the item identifier, and then use the SendItem operation to send the item.</span></span>           |
|<span data-ttu-id="6177d-132">SendAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="6177d-132">SendAndSaveCopy</span></span>  <br/> |<span data-ttu-id="6177d-133">Das Element wird gesendet, und eine Kopie wird in dem Ordner gespeichert, der durch das [SavedItemFolderId](saveditemfolderid.md) -Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="6177d-133">The item is sent and a copy is saved in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span> <span data-ttu-id="6177d-134">In der Antwort wird kein Elementbezeichner zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6177d-134">An item identifier is not returned in the response.</span></span><br/><br/><span data-ttu-id="6177d-135">**Hinweis**: Besprechungsanfragen werden nicht in dem Ordner gespeichert, der von der [SavedItemFolderId](saveditemfolderid.md) -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6177d-135">**NOTE**: Meeting requests are not saved to the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) property.</span></span> <span data-ttu-id="6177d-136">Bei Kalendern kann nur der Speicherort für Kalenderelemente von der **SavedItemFolderId** -Eigenschaft angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6177d-136">For calendaring, only the save location for calendar items can be specified by the **SavedItemFolderId** property.</span></span> <span data-ttu-id="6177d-137">Sie können nicht steuern, wo ein Besprechungsanfrage Element gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="6177d-137">You cannot control where a meeting request item is saved.</span></span> <span data-ttu-id="6177d-138">Nur die zugeordneten Kalenderelemente werden kopiert und in dem Ordner gespeichert, der von der **SavedItemFolderId** -Eigenschaft identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="6177d-138">Only the associated calendar items are copied and saved into the folder that is identified by the **SavedItemFolderId** property.</span></span>           |
   
#### <a name="sendmeetinginvitations-attribute"></a><span data-ttu-id="6177d-139">SendMeetingInvitations-Attribut</span><span class="sxs-lookup"><span data-stu-id="6177d-139">SendMeetingInvitations Attribute</span></span>

|<span data-ttu-id="6177d-140">Wert</span><span class="sxs-lookup"><span data-stu-id="6177d-140">Value</span></span>|<span data-ttu-id="6177d-141">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6177d-141">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="6177d-142">SendToNone</span><span class="sxs-lookup"><span data-stu-id="6177d-142">SendToNone</span></span>  <br/> |<span data-ttu-id="6177d-143">Wenn es sich bei dem Element um eine Besprechungsanfrage handelt, wird es als Kalenderelement gespeichert, aber nicht gesendet.</span><span class="sxs-lookup"><span data-stu-id="6177d-143">If the item is a meeting request, it is saved as a calendar item but not sent.</span></span>  <br/> |
|<span data-ttu-id="6177d-144">SendOnlyToAll</span><span class="sxs-lookup"><span data-stu-id="6177d-144">SendOnlyToAll</span></span>  <br/> |<span data-ttu-id="6177d-145">Die Besprechungsanfrage wird an alle Teilnehmer gesendet, aber nicht im Ordner "Gesendete Elemente" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6177d-145">The meeting request is sent to all attendees but is not saved in the Sent Items folder.</span></span>  <br/> |
|<span data-ttu-id="6177d-146">SendToAllAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="6177d-146">SendToAllAndSaveCopy</span></span>  <br/> |<span data-ttu-id="6177d-147">Die Besprechungsanfrage wird an alle Teilnehmer gesendet, und eine Kopie wird in dem Ordner gespeichert, der durch das [SavedItemFolderId](saveditemfolderid.md) -Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="6177d-147">The meeting request is sent to all attendees and a copy is saved in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6177d-148">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6177d-148">Child elements</span></span>

|<span data-ttu-id="6177d-149">Element</span><span class="sxs-lookup"><span data-stu-id="6177d-149">Element</span></span>|<span data-ttu-id="6177d-150">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6177d-150">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6177d-151">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="6177d-151">SavedItemFolderId</span></span>](saveditemfolderid.md) <br/> |<span data-ttu-id="6177d-152">Gibt den Zielordner an, in dem ein neues Element erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="6177d-152">Identifies the target folder where a new item can be created.</span></span> <span data-ttu-id="6177d-153">Wenn das **MessageDisposition** -Attribut auf SendOnly festgelegt ist, wird nur eine erstellte Nachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="6177d-153">If the **MessageDisposition** attribute is set to SendOnly, a created message will only be sent.</span></span> <span data-ttu-id="6177d-154">Die Nachricht wird nicht in den Ordner eingefügt, der durch das [SavedItemFolderId](saveditemfolderid.md) -Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="6177d-154">The message will not be put in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
|[<span data-ttu-id="6177d-155">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="6177d-155">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="6177d-156">Enthält ein Array von Elementen, die in dem Ordner erstellt werden sollen, der durch das [SavedItemFolderId](saveditemfolderid.md) -Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="6177d-156">Contains an array of items to create in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6177d-157">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6177d-157">Parent elements</span></span>

<span data-ttu-id="6177d-158">Keine.</span><span class="sxs-lookup"><span data-stu-id="6177d-158">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6177d-159">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6177d-159">Remarks</span></span>

<span data-ttu-id="6177d-160">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="6177d-160">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6177d-161">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6177d-161">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6177d-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="6177d-162">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6177d-163">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6177d-163">Schema Name</span></span>  <br/> |<span data-ttu-id="6177d-164">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="6177d-164">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6177d-165">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6177d-165">Validation File</span></span>  <br/> |<span data-ttu-id="6177d-166">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6177d-166">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6177d-167">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6177d-167">Can be Empty</span></span>  <br/> |<span data-ttu-id="6177d-168">False</span><span class="sxs-lookup"><span data-stu-id="6177d-168">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6177d-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6177d-169">See also</span></span>

- [<span data-ttu-id="6177d-170">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="6177d-170">CreateItemResponse</span></span>](createitemresponse.md)  
- [<span data-ttu-id="6177d-171">CreateItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6177d-171">CreateItem operation</span></span>](createitem-operation.md)
- [<span data-ttu-id="6177d-172">Erstellen von e-Mail-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="6177d-172">Creating E-mail Messages</span></span>](https://msdn.microsoft.com/library/05bfb83c-2866-427d-a9fe-14ba3cb02793%28Office.15%29.aspx) 
- [<span data-ttu-id="6177d-173">Creating Contacts (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="6177d-173">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)  
- [<span data-ttu-id="6177d-174">Erstellen von Aufgaben</span><span class="sxs-lookup"><span data-stu-id="6177d-174">Creating Tasks</span></span>](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx) 
- [<span data-ttu-id="6177d-175">Erstellen von Terminen</span><span class="sxs-lookup"><span data-stu-id="6177d-175">Creating Appointments</span></span>](https://msdn.microsoft.com/library/2385391e-c9e7-4d45-b803-c4ff94d5c94e%28Office.15%29.aspx)

