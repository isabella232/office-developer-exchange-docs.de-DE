---
title: ConversationAction
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
description: Das ConversationAction-Element enthält eine einzelne Aktion auf einem einzelnen Gespräch angewendet werden soll.
ms.openlocfilehash: 45cd6df3aba94062bd5aa0ddf9367e8cf118dc6b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757695"
---
# <a name="conversationaction"></a><span data-ttu-id="0fdb8-103">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="0fdb8-103">ConversationAction</span></span>

<span data-ttu-id="0fdb8-104">Das **ConversationAction** -Element enthält eine einzelne Aktion auf einem einzelnen Gespräch angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-104">The **ConversationAction** element contains a single action to be applied to a single conversation.</span></span> 
  
[<span data-ttu-id="0fdb8-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="0fdb8-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="0fdb8-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="0fdb8-106">ConversationActions</span></span>](conversationactions.md)
  
[<span data-ttu-id="0fdb8-107">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="0fdb8-107">ConversationAction</span></span>](conversationaction.md)
  
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

 <span data-ttu-id="0fdb8-108">**ConversationActionType**</span><span class="sxs-lookup"><span data-stu-id="0fdb8-108">**ConversationActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0fdb8-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0fdb8-109">Attributes and elements</span></span>

<span data-ttu-id="0fdb8-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0fdb8-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="0fdb8-111">Attributes</span></span>

<span data-ttu-id="0fdb8-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0fdb8-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0fdb8-113">Child elements</span></span>

|<span data-ttu-id="0fdb8-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="0fdb8-114">**Element**</span></span>|<span data-ttu-id="0fdb8-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0fdb8-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0fdb8-116">Aktion (ConversationActionTypeType)</span><span class="sxs-lookup"><span data-stu-id="0fdb8-116">Action (ConversationActionTypeType)</span></span>](action-conversationactiontypetype.md) <br/> |<span data-ttu-id="0fdb8-117">Enthält die Aktion auf die Unterhaltung vom [ConversationId](conversationid.md) -Element angegeben.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-117">Contains the action to perform on the conversation specified by the [ConversationId](conversationid.md) element.</span></span> <span data-ttu-id="0fdb8-118">Dieses Element muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-118">This element must be present.</span></span>  <br/> |
|[<span data-ttu-id="0fdb8-119">ConversationId</span><span class="sxs-lookup"><span data-stu-id="0fdb8-119">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="0fdb8-120">Enthält den Bezeichner der Unterhaltung, die die Aktion durch auf Elemente in der Unterhaltung angewendet [Action (ConversationActionTypeType)](action-conversationactiontypetype.md) -Elements angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-120">Contains the identifier of the conversation that will have the action specified by the [Action (ConversationActionTypeType)](action-conversationactiontypetype.md) element applied to items in the conversation.</span></span> <span data-ttu-id="0fdb8-121">Dieses Element muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-121">This element must be present.</span></span>  <br/> |
|[<span data-ttu-id="0fdb8-122">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="0fdb8-122">ContextFolderId</span></span>](contextfolderid.md) <br/> |<span data-ttu-id="0fdb8-123">Gibt den Ordner, der für Aktionen gerichtet ist, die Ordner zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-123">Indicates the folder that is targeted for actions that use folders.</span></span> <span data-ttu-id="0fdb8-124">Dieses Element muss beim Kopieren, löschen, verschieben und Festlegen von Zustand "gelesen" für Unterhaltungselemente in einem Zielordner vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-124">This element must be present when copying, deleting, moving, and setting read state on conversation items in a target folder.</span></span>  <br/> |
|[<span data-ttu-id="0fdb8-125">ConversationLastSyncTime</span><span class="sxs-lookup"><span data-stu-id="0fdb8-125">ConversationLastSyncTime</span></span>](conversationlastsynctime.md) <br/> |<span data-ttu-id="0fdb8-126">Enthält das Datum und die Uhrzeit, zu der der letzten eine Unterhaltung Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-126">Contains the date and time that a conversation was last synchronized.</span></span> <span data-ttu-id="0fdb8-127">Dieses Element muss vorhanden sein, wenn Sie versuchen, um alle Elemente in einer Unterhaltung zu löschen, die bis zu der angegebenen Zeit empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-127">This element must be present when trying to delete all items in a conversation that were received up to the specified time.</span></span>  <br/> |
|[<span data-ttu-id="0fdb8-128">ProcessRightAway</span><span class="sxs-lookup"><span data-stu-id="0fdb8-128">ProcessRightAway</span></span>](processrightaway.md) <br/> |<span data-ttu-id="0fdb8-129">Gibt an, ob die Antwort gesendet wird, sobald die Aktion startet die Verarbeitung auf dem Server oder gibt an, ob die Antwort gesendet wird, nachdem der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-129">Indicates whether the response is sent as soon as the action starts processing on the server or whether the response is sent after the action has completed.</span></span> <span data-ttu-id="0fdb8-130">Dieses Element muss vorhanden sein, damit die Antwort für die angeforderte Aktion asynchronen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-130">This element must be present for the response to be sent asynchronous to the requested action.</span></span>  <br/> |
|[<span data-ttu-id="0fdb8-131">DestinationFolderId</span><span class="sxs-lookup"><span data-stu-id="0fdb8-131">DestinationFolderId</span></span>](destinationfolderid.md) <br/> |<span data-ttu-id="0fdb8-132">Gibt den Zielordner für die Kopie an, und verschieben Sie Aktionen.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-132">Indicates the destination folder for copy and move actions.</span></span>  <br/> |
|[<span data-ttu-id="0fdb8-133">Kategorien</span><span class="sxs-lookup"><span data-stu-id="0fdb8-133">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="0fdb8-134">Enthält eine Auflistung von Zeichenfolgen, die die Kategorien zu identifizieren, zu denen Elemente in einer Unterhaltung gehören.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-134">Contains a collection of strings that identify the categories to which items in a conversation belong.</span></span>  <br/> |
|[<span data-ttu-id="0fdb8-135">EnableAlwaysDelete</span><span class="sxs-lookup"><span data-stu-id="0fdb8-135">EnableAlwaysDelete</span></span>](enablealwaysdelete.md) <br/> |<span data-ttu-id="0fdb8-136">Gibt ein Flag, das für alle neuen Elemente in einer Unterhaltung löschen kann.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-136">Specifies a flag that enables deletion for all new items in a conversation.</span></span>  <br/> |
|[<span data-ttu-id="0fdb8-137">IsRead</span><span class="sxs-lookup"><span data-stu-id="0fdb8-137">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="0fdb8-138">Gibt an, ob eine Nachricht gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-138">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="0fdb8-139">DeleteType</span><span class="sxs-lookup"><span data-stu-id="0fdb8-139">DeleteType</span></span>](deletetype.md) <br/> |<span data-ttu-id="0fdb8-140">Gibt an, wie Elemente in einer Unterhaltung gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-140">Indicates how items in a conversation are deleted.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0fdb8-141">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0fdb8-141">Parent elements</span></span>

|<span data-ttu-id="0fdb8-142">**Element**</span><span class="sxs-lookup"><span data-stu-id="0fdb8-142">**Element**</span></span>|<span data-ttu-id="0fdb8-143">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0fdb8-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0fdb8-144">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="0fdb8-144">ConversationActions</span></span>](conversationactions.md) <br/> |<span data-ttu-id="0fdb8-145">Enthält eine Auflistung von Unterhaltungen und die Aktionen darauf anwenden.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-145">Contains a collection of conversations and the actions to apply to them.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0fdb8-146">Textwert</span><span class="sxs-lookup"><span data-stu-id="0fdb8-146">Text value</span></span>

<span data-ttu-id="0fdb8-147">**Text-Elementwerte ConversationAction**</span><span class="sxs-lookup"><span data-stu-id="0fdb8-147">**ConversationAction element text values**</span></span>

|<span data-ttu-id="0fdb8-148">**Wert**</span><span class="sxs-lookup"><span data-stu-id="0fdb8-148">**Value**</span></span>|<span data-ttu-id="0fdb8-149">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0fdb8-149">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0fdb8-150">AlwaysCategorize</span><span class="sxs-lookup"><span data-stu-id="0fdb8-150">AlwaysCategorize</span></span>  <br/> |<span data-ttu-id="0fdb8-151">Kategorisieren Sie der Unterhaltung immer.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-151">Always categorize the conversation.</span></span>  <br/> |
|<span data-ttu-id="0fdb8-152">AlwaysDelete</span><span class="sxs-lookup"><span data-stu-id="0fdb8-152">AlwaysDelete</span></span>  <br/> |<span data-ttu-id="0fdb8-153">Löschen Sie die Unterhaltung immer.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-153">Always delete the conversation.</span></span>  <br/> |
|<span data-ttu-id="0fdb8-154">AlwaysMove</span><span class="sxs-lookup"><span data-stu-id="0fdb8-154">AlwaysMove</span></span>  <br/> |<span data-ttu-id="0fdb8-155">Die Unterhaltung verschoben immer.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-155">Always move the conversation.</span></span>  <br/> |
|<span data-ttu-id="0fdb8-156">Löschen</span><span class="sxs-lookup"><span data-stu-id="0fdb8-156">Delete</span></span>  <br/> |<span data-ttu-id="0fdb8-157">Löschen Sie die Unterhaltung an.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-157">Delete the conversation.</span></span>  <br/> |
|<span data-ttu-id="0fdb8-158">Verschieben</span><span class="sxs-lookup"><span data-stu-id="0fdb8-158">Move</span></span>  <br/> |<span data-ttu-id="0fdb8-159">Verschieben der Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-159">Move the conversation.</span></span>  <br/> |
|<span data-ttu-id="0fdb8-160">Kopie</span><span class="sxs-lookup"><span data-stu-id="0fdb8-160">Copy</span></span>  <br/> |<span data-ttu-id="0fdb8-161">Kopieren Sie die Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-161">Copy the conversation.</span></span>  <br/> |
|<span data-ttu-id="0fdb8-162">SetReadState</span><span class="sxs-lookup"><span data-stu-id="0fdb8-162">SetReadState</span></span>  <br/> |<span data-ttu-id="0fdb8-163">Legen Sie den Zustand "gelesen" der Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-163">Set the read state of the conversation.</span></span>  <br/> |
|<span data-ttu-id="0fdb8-164">SetRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0fdb8-164">SetRetentionPolicy</span></span>  <br/> |<span data-ttu-id="0fdb8-165">Legen Sie die Aufbewahrungsrichtlinie für die Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-165">Set the retention policy for the conversation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0fdb8-166">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0fdb8-166">Remarks</span></span>

<span data-ttu-id="0fdb8-167">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0fdb8-167">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0fdb8-168">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0fdb8-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0fdb8-169">Namespace</span><span class="sxs-lookup"><span data-stu-id="0fdb8-169">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0fdb8-170">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0fdb8-170">Schema Name</span></span>  <br/> |<span data-ttu-id="0fdb8-171">Schematypen</span><span class="sxs-lookup"><span data-stu-id="0fdb8-171">Types schema</span></span>  <br/> |
|<span data-ttu-id="0fdb8-172">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0fdb8-172">Validation File</span></span>  <br/> |<span data-ttu-id="0fdb8-173">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0fdb8-173">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0fdb8-174">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0fdb8-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="0fdb8-175">False</span><span class="sxs-lookup"><span data-stu-id="0fdb8-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0fdb8-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fdb8-176">See also</span></span>



[<span data-ttu-id="0fdb8-177">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0fdb8-177">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


- [<span data-ttu-id="0fdb8-178">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0fdb8-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

