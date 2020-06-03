---
title: Unterhaltung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConversationAction
api_type:
- schema
ms.assetid: 9ecea41a-3860-4569-8e9b-284b451fc4e0
description: Das Conversation Action-Element enthält eine einzelne Aktion, die auf eine einzelne Unterhaltung angewendet werden soll.
ms.openlocfilehash: cb7d874f787b105d5185749dfaf1e940d2411d89
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529252"
---
# <a name="conversationaction"></a><span data-ttu-id="753cb-103">Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="753cb-103">ConversationAction</span></span>

<span data-ttu-id="753cb-104">Das **Conversation** Action-Element enthält eine einzelne Aktion, die auf eine einzelne Unterhaltung angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="753cb-104">The **ConversationAction** element contains a single action to be applied to a single conversation.</span></span> 
  
[<span data-ttu-id="753cb-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="753cb-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="753cb-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="753cb-106">ConversationActions</span></span>](conversationactions.md)
  
[<span data-ttu-id="753cb-107">Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="753cb-107">ConversationAction</span></span>](conversationaction.md)
  
```XML
<ConversationAction>
   <Action/>
   <ConversationId/>
   <ContextFolderId/>
   <ConversationLastSyncTime/>
   <ProcessRightAway/>
   <DestinationFolderId/>
   <Categories/>
   <EnableAlwaysDelete/>
   <IsRead/>
   <DeleteType/>
</ConversationAction>
```

 <span data-ttu-id="753cb-108">**ConversationActionType**</span><span class="sxs-lookup"><span data-stu-id="753cb-108">**ConversationActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="753cb-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="753cb-109">Attributes and elements</span></span>

<span data-ttu-id="753cb-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="753cb-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="753cb-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="753cb-111">Attributes</span></span>

<span data-ttu-id="753cb-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="753cb-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="753cb-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="753cb-113">Child elements</span></span>

|<span data-ttu-id="753cb-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="753cb-114">**Element**</span></span>|<span data-ttu-id="753cb-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="753cb-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="753cb-116">Action (ConversationActionTypeType)</span><span class="sxs-lookup"><span data-stu-id="753cb-116">Action (ConversationActionTypeType)</span></span>](action-conversationactiontypetype.md) <br/> |<span data-ttu-id="753cb-117">Enthält die Aktion, die für die durch das [Conversation](conversationid.md) -Element angegebene Konversation ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="753cb-117">Contains the action to perform on the conversation specified by the [ConversationId](conversationid.md) element.</span></span> <span data-ttu-id="753cb-118">Dieses Element muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="753cb-118">This element must be present.</span></span>  <br/> |
|[<span data-ttu-id="753cb-119">ConversationId</span><span class="sxs-lookup"><span data-stu-id="753cb-119">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="753cb-120">Enthält den Bezeichner der Unterhaltung, für die die durch das [Action-Element (ConversationActionTypeType)](action-conversationactiontypetype.md) angegebene Aktion auf Elemente in der Unterhaltung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="753cb-120">Contains the identifier of the conversation that will have the action specified by the [Action (ConversationActionTypeType)](action-conversationactiontypetype.md) element applied to items in the conversation.</span></span> <span data-ttu-id="753cb-121">Dieses Element muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="753cb-121">This element must be present.</span></span>  <br/> |
|[<span data-ttu-id="753cb-122">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="753cb-122">ContextFolderId</span></span>](contextfolderid.md) <br/> |<span data-ttu-id="753cb-123">Gibt den Ordner an, der für Aktionen vorgesehen ist, die Ordner verwenden.</span><span class="sxs-lookup"><span data-stu-id="753cb-123">Indicates the folder that is targeted for actions that use folders.</span></span> <span data-ttu-id="753cb-124">Dieses Element muss beim Kopieren, löschen, verschieben und Festlegen des Lese Zustands für Unterhaltungselemente in einem Zielordner vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="753cb-124">This element must be present when copying, deleting, moving, and setting read state on conversation items in a target folder.</span></span>  <br/> |
|[<span data-ttu-id="753cb-125">ConversationLastSyncTime</span><span class="sxs-lookup"><span data-stu-id="753cb-125">ConversationLastSyncTime</span></span>](conversationlastsynctime.md) <br/> |<span data-ttu-id="753cb-126">Enthält das Datum und die Uhrzeit, zu der eine Unterhaltung zuletzt synchronisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="753cb-126">Contains the date and time that a conversation was last synchronized.</span></span> <span data-ttu-id="753cb-127">Dieses Element muss vorhanden sein, wenn Sie versuchen, alle Elemente in einer Unterhaltung zu löschen, die bis zur angegebenen Zeit empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="753cb-127">This element must be present when trying to delete all items in a conversation that were received up to the specified time.</span></span>  <br/> |
|[<span data-ttu-id="753cb-128">ProcessRightAway</span><span class="sxs-lookup"><span data-stu-id="753cb-128">ProcessRightAway</span></span>](processrightaway.md) <br/> |<span data-ttu-id="753cb-129">Gibt an, ob die Antwort gesendet wird, sobald die Aktion auf dem Server verarbeitet wird oder ob die Antwort gesendet wird, nachdem die Aktion abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="753cb-129">Indicates whether the response is sent as soon as the action starts processing on the server or whether the response is sent after the action has completed.</span></span> <span data-ttu-id="753cb-130">Dieses Element muss vorhanden sein, damit die Antwort asynchron an die angeforderte Aktion gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="753cb-130">This element must be present for the response to be sent asynchronous to the requested action.</span></span>  <br/> |
|[<span data-ttu-id="753cb-131">DestinationFolderId</span><span class="sxs-lookup"><span data-stu-id="753cb-131">DestinationFolderId</span></span>](destinationfolderid.md) <br/> |<span data-ttu-id="753cb-132">Gibt den Zielordner für die Aktionen kopieren und verlegen an.</span><span class="sxs-lookup"><span data-stu-id="753cb-132">Indicates the destination folder for copy and move actions.</span></span>  <br/> |
|[<span data-ttu-id="753cb-133">Kategorien</span><span class="sxs-lookup"><span data-stu-id="753cb-133">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="753cb-134">Enthält eine Auflistung von Zeichenfolgen, die die Kategorien identifizieren, zu denen Elemente in einer Unterhaltung gehören.</span><span class="sxs-lookup"><span data-stu-id="753cb-134">Contains a collection of strings that identify the categories to which items in a conversation belong.</span></span>  <br/> |
|[<span data-ttu-id="753cb-135">EnableAlwaysDelete</span><span class="sxs-lookup"><span data-stu-id="753cb-135">EnableAlwaysDelete</span></span>](enablealwaysdelete.md) <br/> |<span data-ttu-id="753cb-136">Gibt ein Flag an, das das Löschen für alle neuen Elemente in einer Unterhaltung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="753cb-136">Specifies a flag that enables deletion for all new items in a conversation.</span></span>  <br/> |
|[<span data-ttu-id="753cb-137">IsRead</span><span class="sxs-lookup"><span data-stu-id="753cb-137">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="753cb-138">Gibt an, ob eine Nachricht gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="753cb-138">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="753cb-139">Deletetypeharddelete</span><span class="sxs-lookup"><span data-stu-id="753cb-139">DeleteType</span></span>](deletetype.md) <br/> |<span data-ttu-id="753cb-140">Gibt an, wie Elemente in einer Unterhaltung gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="753cb-140">Indicates how items in a conversation are deleted.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="753cb-141">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="753cb-141">Parent elements</span></span>

|<span data-ttu-id="753cb-142">**Element**</span><span class="sxs-lookup"><span data-stu-id="753cb-142">**Element**</span></span>|<span data-ttu-id="753cb-143">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="753cb-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="753cb-144">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="753cb-144">ConversationActions</span></span>](conversationactions.md) <br/> |<span data-ttu-id="753cb-145">Enthält eine Auflistung von Unterhaltungen und die Aktionen, die auf diese angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="753cb-145">Contains a collection of conversations and the actions to apply to them.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="753cb-146">Textwert</span><span class="sxs-lookup"><span data-stu-id="753cb-146">Text value</span></span>

<span data-ttu-id="753cb-147">**Textwerte des Conversation-Elementtexts**</span><span class="sxs-lookup"><span data-stu-id="753cb-147">**ConversationAction element text values**</span></span>

|<span data-ttu-id="753cb-148">**Wert**</span><span class="sxs-lookup"><span data-stu-id="753cb-148">**Value**</span></span>|<span data-ttu-id="753cb-149">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="753cb-149">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="753cb-150">AlwaysCategorize</span><span class="sxs-lookup"><span data-stu-id="753cb-150">AlwaysCategorize</span></span>  <br/> |<span data-ttu-id="753cb-151">Unterhaltung immer kategorisieren.</span><span class="sxs-lookup"><span data-stu-id="753cb-151">Always categorize the conversation.</span></span>  <br/> |
|<span data-ttu-id="753cb-152">Alwaysdeleteolalwaysdelete</span><span class="sxs-lookup"><span data-stu-id="753cb-152">AlwaysDelete</span></span>  <br/> |<span data-ttu-id="753cb-153">Die Unterhaltung wird immer gelöscht.</span><span class="sxs-lookup"><span data-stu-id="753cb-153">Always delete the conversation.</span></span>  <br/> |
|<span data-ttu-id="753cb-154">AlwaysMove</span><span class="sxs-lookup"><span data-stu-id="753cb-154">AlwaysMove</span></span>  <br/> |<span data-ttu-id="753cb-155">Die Unterhaltung immer verlagern.</span><span class="sxs-lookup"><span data-stu-id="753cb-155">Always move the conversation.</span></span>  <br/> |
|<span data-ttu-id="753cb-156">Löschen</span><span class="sxs-lookup"><span data-stu-id="753cb-156">Delete</span></span>  <br/> |<span data-ttu-id="753cb-157">Löschen Sie die Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="753cb-157">Delete the conversation.</span></span>  <br/> |
|<span data-ttu-id="753cb-158">Move</span><span class="sxs-lookup"><span data-stu-id="753cb-158">Move</span></span>  <br/> |<span data-ttu-id="753cb-159">Die Unterhaltung zu verlegen.</span><span class="sxs-lookup"><span data-stu-id="753cb-159">Move the conversation.</span></span>  <br/> |
|<span data-ttu-id="753cb-160">Copy</span><span class="sxs-lookup"><span data-stu-id="753cb-160">Copy</span></span>  <br/> |<span data-ttu-id="753cb-161">Kopieren Sie die Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="753cb-161">Copy the conversation.</span></span>  <br/> |
|<span data-ttu-id="753cb-162">SetReadState</span><span class="sxs-lookup"><span data-stu-id="753cb-162">SetReadState</span></span>  <br/> |<span data-ttu-id="753cb-163">Legen Sie den Lesestatus der Unterhaltung fest.</span><span class="sxs-lookup"><span data-stu-id="753cb-163">Set the read state of the conversation.</span></span>  <br/> |
|<span data-ttu-id="753cb-164">SetRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="753cb-164">SetRetentionPolicy</span></span>  <br/> |<span data-ttu-id="753cb-165">Legen Sie die Aufbewahrungsrichtlinie für die Unterhaltung fest.</span><span class="sxs-lookup"><span data-stu-id="753cb-165">Set the retention policy for the conversation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="753cb-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="753cb-166">Remarks</span></span>

<span data-ttu-id="753cb-167">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="753cb-167">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="753cb-168">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="753cb-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="753cb-169">Namespace</span><span class="sxs-lookup"><span data-stu-id="753cb-169">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="753cb-170">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="753cb-170">Schema Name</span></span>  <br/> |<span data-ttu-id="753cb-171">Schematypen</span><span class="sxs-lookup"><span data-stu-id="753cb-171">Types schema</span></span>  <br/> |
|<span data-ttu-id="753cb-172">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="753cb-172">Validation File</span></span>  <br/> |<span data-ttu-id="753cb-173">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="753cb-173">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="753cb-174">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="753cb-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="753cb-175">False</span><span class="sxs-lookup"><span data-stu-id="753cb-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="753cb-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="753cb-176">See also</span></span>



[<span data-ttu-id="753cb-177">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="753cb-177">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


- [<span data-ttu-id="753cb-178">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="753cb-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

