---
title: Aktion (ConversationActionTypeType)
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
description: Das Action-Element enthält die Aktion auf die Unterhaltung vom ConversationId-Element angegeben.
ms.openlocfilehash: b468eeaf0c2509bfa53cbd83f497f0bae20a7f68
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757207"
---
# <a name="action-conversationactiontypetype"></a><span data-ttu-id="8ba9e-103">Aktion (ConversationActionTypeType)</span><span class="sxs-lookup"><span data-stu-id="8ba9e-103">Action (ConversationActionTypeType)</span></span>

<span data-ttu-id="8ba9e-104">Das **Action** -Element enthält die Aktion auf die Unterhaltung vom [ConversationId](conversationid.md) -Element angegeben.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-104">The **Action** element contains the action to perform on the conversation specified by the [ConversationId](conversationid.md) element.</span></span> 
  
- [<span data-ttu-id="8ba9e-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="8ba9e-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
- [<span data-ttu-id="8ba9e-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="8ba9e-106">ConversationActions</span></span>](conversationactions.md)
  
- [<span data-ttu-id="8ba9e-107">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="8ba9e-107">ConversationAction</span></span>](conversationaction.md)
  
- [<span data-ttu-id="8ba9e-108">Aktion (ConversationActionTypeType)</span><span class="sxs-lookup"><span data-stu-id="8ba9e-108">Action (ConversationActionTypeType)</span></span>](action-conversationactiontypetype.md)
  
```XML
<Action> AlwaysCategorize | AlwaysDelete | AlwaysMove | Delete | Move | Copy | SetReadState </Action>
```

 <span data-ttu-id="8ba9e-109">**ConversationActionTypeType**</span><span class="sxs-lookup"><span data-stu-id="8ba9e-109">**ConversationActionTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8ba9e-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8ba9e-110">Attributes and elements</span></span>

<span data-ttu-id="8ba9e-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8ba9e-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="8ba9e-112">Attributes</span></span>

<span data-ttu-id="8ba9e-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8ba9e-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8ba9e-114">Child elements</span></span>

<span data-ttu-id="8ba9e-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8ba9e-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8ba9e-116">Parent elements</span></span>

|<span data-ttu-id="8ba9e-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="8ba9e-117">**Element**</span></span>|<span data-ttu-id="8ba9e-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8ba9e-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8ba9e-119">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="8ba9e-119">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="8ba9e-120">Enthält eine einzelne Aktion auf einem einzelnen Gespräch angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-120">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8ba9e-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="8ba9e-121">Text value</span></span>

<span data-ttu-id="8ba9e-122">Der Textwert des **Action** -Elements gibt an, welche Aktion für eine Unterhaltung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-122">The text value of the **Action** element indicates which action will be performed on a conversation.</span></span> <span data-ttu-id="8ba9e-123">Im folgenden sind die möglichen Textwerte und die entsprechenden Aktionen:</span><span class="sxs-lookup"><span data-stu-id="8ba9e-123">The following are the possible text values and the corresponding actions:</span></span> 
  
- <span data-ttu-id="8ba9e-124">**AlwaysCategorize** - die aktuelle und neue Elemente in der Unterhaltung wird automatisch mit den Kategorien in der [Categories](categories-ex15websvcsotherref.md) -Element identifiziert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-124">**AlwaysCategorize** - The current items and new items in the conversation will automatically be set with the categories identified in the [Categories](categories-ex15websvcsotherref.md) element.</span></span> 
    
- <span data-ttu-id="8ba9e-125">**AlwaysDelete** - die aktuelle und neue Elemente in der Unterhaltung werden automatisch gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-125">**AlwaysDelete** - The current items and new items in the conversation will automatically be deleted.</span></span> <span data-ttu-id="8ba9e-126">Der Modus Löschung wird vom [DeleteType](deletetype.md) -Element festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-126">The deletion mode is set by the [DeleteType](deletetype.md) element.</span></span> 
    
- <span data-ttu-id="8ba9e-127">**AlwaysMove** - die aktuelle und neue Elemente in der Unterhaltung wird automatisch in den Ordner vom [DestinationFolderId](destinationfolderid.md) -Element identifiziert verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-127">**AlwaysMove** - The current items and new items in the conversation will automatically be moved to the folder identified by the [DestinationFolderId](destinationfolderid.md) element.</span></span> 
    
- <span data-ttu-id="8ba9e-128">**Löschen** – der aktuelle Elemente in der Unterhaltung wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-128">**Delete** - The current items in the conversation will be deleted.</span></span> <span data-ttu-id="8ba9e-129">Nachfolgende Elemente in der Unterhaltung werden nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-129">Subsequent items in the conversation will not be deleted.</span></span> <span data-ttu-id="8ba9e-130">Der Modus Löschung wird vom [DeleteType](deletetype.md) -Element festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-130">The deletion mode is set by the [DeleteType](deletetype.md) element.</span></span> 
    
- <span data-ttu-id="8ba9e-131">**Verschieben** - aktuelle Elemente in der Unterhaltung werden in den Ordner, der durch das [DestinationFolderId](destinationfolderid.md) -Element identifiziert verschoben.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-131">**Move** - The current items in the conversation will be moved to the folder identified by the [DestinationFolderId](destinationfolderid.md) element.</span></span> <span data-ttu-id="8ba9e-132">Nachfolgende Elemente in der Unterhaltung werden nicht verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-132">Subsequent items in the conversation will not be moved.</span></span> 
    
- <span data-ttu-id="8ba9e-133">**Kopieren** - die aktuelle Elemente in der Unterhaltung werden in den Ordner, der durch das [DestinationFolderId](destinationfolderid.md) -Element identifiziert kopiert.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-133">**Copy** - The current items in the conversation will be copied to the folder identified by the [DestinationFolderId](destinationfolderid.md) element.</span></span> <span data-ttu-id="8ba9e-134">Nachfolgende Elemente in der Unterhaltung werden nicht kopiert.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-134">Subsequent items in the conversation will not be copied.</span></span> 
    
- <span data-ttu-id="8ba9e-135">**SetReadState** - die aktuelle Elemente in der Unterhaltung müssen ihre Zustand "gelesen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-135">**SetReadState** - The current items in the conversation will have their read state set.</span></span> <span data-ttu-id="8ba9e-136">Der Zustand "gelesen" wird durch das [IsRead](isread.md) -Element festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-136">The read state is set by the [IsRead](isread.md) element.</span></span> 
    
- <span data-ttu-id="8ba9e-137">**Flag** - aktuelle Elemente in der Unterhaltung wird ein Flag gesetzt, das durch das Element [Flag](flag.md) festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-137">**Flag** - The current items in the conversation will have a flag set as defined by the [Flag](flag.md) element.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8ba9e-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8ba9e-138">Remarks</span></span>

<span data-ttu-id="8ba9e-139">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8ba9e-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8ba9e-140">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8ba9e-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8ba9e-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="8ba9e-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8ba9e-142">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8ba9e-142">Schema Name</span></span>  <br/> |<span data-ttu-id="8ba9e-143">Schematypen</span><span class="sxs-lookup"><span data-stu-id="8ba9e-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="8ba9e-144">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8ba9e-144">Validation File</span></span>  <br/> |<span data-ttu-id="8ba9e-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8ba9e-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8ba9e-146">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8ba9e-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="8ba9e-147">False</span><span class="sxs-lookup"><span data-stu-id="8ba9e-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8ba9e-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ba9e-148">See also</span></span>

- [<span data-ttu-id="8ba9e-149">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8ba9e-149">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
- [<span data-ttu-id="8ba9e-150">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8ba9e-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

