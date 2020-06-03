---
title: Action (ConversationActionTypeType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Action
api_type:
- schema
ms.assetid: 8bbc12f2-76c5-4fda-828f-56b2086a0454
description: Das Action-Element enthält die Aktion, die für die durch das Conversation-Element angegebene Konversation ausgeführt werden soll.
ms.openlocfilehash: f97b04b98cdc29bee9aff5fa1fc6f37400b8314c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527544"
---
# <a name="action-conversationactiontypetype"></a><span data-ttu-id="d74df-103">Action (ConversationActionTypeType)</span><span class="sxs-lookup"><span data-stu-id="d74df-103">Action (ConversationActionTypeType)</span></span>

<span data-ttu-id="d74df-104">Das **Action** -Element enthält die Aktion, die für die durch das [Conversation](conversationid.md) -Element angegebene Konversation ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d74df-104">The **Action** element contains the action to perform on the conversation specified by the [ConversationId](conversationid.md) element.</span></span> 
  
- [<span data-ttu-id="d74df-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="d74df-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
- [<span data-ttu-id="d74df-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="d74df-106">ConversationActions</span></span>](conversationactions.md)
  
- [<span data-ttu-id="d74df-107">Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="d74df-107">ConversationAction</span></span>](conversationaction.md)
  
- [<span data-ttu-id="d74df-108">Action (ConversationActionTypeType)</span><span class="sxs-lookup"><span data-stu-id="d74df-108">Action (ConversationActionTypeType)</span></span>](action-conversationactiontypetype.md)
  
```XML
<Action> AlwaysCategorize | AlwaysDelete | AlwaysMove | Delete | Move | Copy | SetReadState </Action>
```

 <span data-ttu-id="d74df-109">**ConversationActionTypeType**</span><span class="sxs-lookup"><span data-stu-id="d74df-109">**ConversationActionTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d74df-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d74df-110">Attributes and elements</span></span>

<span data-ttu-id="d74df-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d74df-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d74df-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="d74df-112">Attributes</span></span>

<span data-ttu-id="d74df-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="d74df-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d74df-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d74df-114">Child elements</span></span>

<span data-ttu-id="d74df-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="d74df-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d74df-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d74df-116">Parent elements</span></span>

|<span data-ttu-id="d74df-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="d74df-117">**Element**</span></span>|<span data-ttu-id="d74df-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d74df-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d74df-119">Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="d74df-119">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="d74df-120">Enthält eine einzelne Aktion, die auf eine einzelne Unterhaltung angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d74df-120">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d74df-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="d74df-121">Text value</span></span>

<span data-ttu-id="d74df-122">Der Textwert des **Action** -Elements gibt an, welche Aktion für eine Unterhaltung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d74df-122">The text value of the **Action** element indicates which action will be performed on a conversation.</span></span> <span data-ttu-id="d74df-123">Im folgenden sind die möglichen Text Werte und die entsprechenden Aktionen:</span><span class="sxs-lookup"><span data-stu-id="d74df-123">The following are the possible text values and the corresponding actions:</span></span> 
  
- <span data-ttu-id="d74df-124">**AlwaysCategorize** – die aktuellen Elemente und neuen Elemente in der Unterhaltung werden automatisch mit den Kategorien festgelegt, die im [Categories](categories-ex15websvcsotherref.md) -Element angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="d74df-124">**AlwaysCategorize** - The current items and new items in the conversation will automatically be set with the categories identified in the [Categories](categories-ex15websvcsotherref.md) element.</span></span> 
    
- <span data-ttu-id="d74df-125">**Alwaysdeleteolalwaysdelete** – die aktuellen Elemente und neuen Elemente in der Unterhaltung werden automatisch gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d74df-125">**AlwaysDelete** - The current items and new items in the conversation will automatically be deleted.</span></span> <span data-ttu-id="d74df-126">Der Löschmodus wird durch das [deleteType](deletetype.md) -Element festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d74df-126">The deletion mode is set by the [DeleteType](deletetype.md) element.</span></span> 
    
- <span data-ttu-id="d74df-127">**AlwaysMove** – die aktuellen Elemente und neuen Elemente in der Unterhaltung werden automatisch in den Ordner verschoben, der durch das [DestinationFolderId](destinationfolderid.md) -Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="d74df-127">**AlwaysMove** - The current items and new items in the conversation will automatically be moved to the folder identified by the [DestinationFolderId](destinationfolderid.md) element.</span></span> 
    
- <span data-ttu-id="d74df-128">**Delete** – die aktuellen Elemente in der Unterhaltung werden gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d74df-128">**Delete** - The current items in the conversation will be deleted.</span></span> <span data-ttu-id="d74df-129">Nachfolgende Elemente in der Unterhaltung werden nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d74df-129">Subsequent items in the conversation will not be deleted.</span></span> <span data-ttu-id="d74df-130">Der Löschmodus wird durch das [deleteType](deletetype.md) -Element festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d74df-130">The deletion mode is set by the [DeleteType](deletetype.md) element.</span></span> 
    
- <span data-ttu-id="d74df-131">**Move** – die aktuellen Elemente in der Unterhaltung werden in den durch das [DestinationFolderId](destinationfolderid.md) -Element identifizierten Ordner verschoben.</span><span class="sxs-lookup"><span data-stu-id="d74df-131">**Move** - The current items in the conversation will be moved to the folder identified by the [DestinationFolderId](destinationfolderid.md) element.</span></span> <span data-ttu-id="d74df-132">Nachfolgende Elemente in der Unterhaltung werden nicht verschoben.</span><span class="sxs-lookup"><span data-stu-id="d74df-132">Subsequent items in the conversation will not be moved.</span></span> 
    
- <span data-ttu-id="d74df-133">**Copy** – die aktuellen Elemente in der Unterhaltung werden in den durch das [DestinationFolderId](destinationfolderid.md) -Element identifizierten Ordner kopiert.</span><span class="sxs-lookup"><span data-stu-id="d74df-133">**Copy** - The current items in the conversation will be copied to the folder identified by the [DestinationFolderId](destinationfolderid.md) element.</span></span> <span data-ttu-id="d74df-134">Nachfolgende Elemente in der Unterhaltung werden nicht kopiert.</span><span class="sxs-lookup"><span data-stu-id="d74df-134">Subsequent items in the conversation will not be copied.</span></span> 
    
- <span data-ttu-id="d74df-135">**SetReadState** – für die aktuellen Elemente in der Unterhaltung ist der Lesestatus festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d74df-135">**SetReadState** - The current items in the conversation will have their read state set.</span></span> <span data-ttu-id="d74df-136">Der Read-Zustand wird durch das [isread](isread.md) -Element festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d74df-136">The read state is set by the [IsRead](isread.md) element.</span></span> 
    
- <span data-ttu-id="d74df-137">**Flag** – für die aktuellen Elemente in der Unterhaltung wird ein Flag festgelegt, das durch das [Flag](flag.md) -Element definiert ist.</span><span class="sxs-lookup"><span data-stu-id="d74df-137">**Flag** - The current items in the conversation will have a flag set as defined by the [Flag](flag.md) element.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d74df-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d74df-138">Remarks</span></span>

<span data-ttu-id="d74df-139">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d74df-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d74df-140">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d74df-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d74df-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="d74df-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d74df-142">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d74df-142">Schema Name</span></span>  <br/> |<span data-ttu-id="d74df-143">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d74df-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="d74df-144">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d74df-144">Validation File</span></span>  <br/> |<span data-ttu-id="d74df-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d74df-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d74df-146">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d74df-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="d74df-147">False</span><span class="sxs-lookup"><span data-stu-id="d74df-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d74df-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d74df-148">See also</span></span>

- [<span data-ttu-id="d74df-149">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d74df-149">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
- [<span data-ttu-id="d74df-150">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d74df-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

