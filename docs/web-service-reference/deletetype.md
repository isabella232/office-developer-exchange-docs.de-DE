---
title: DeleteType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteType
api_type:
- schema
ms.assetid: 6e3136cd-9cb4-493a-aa85-9678f719002d
description: Das DeleteType-Element gibt an, wie Elemente in einer Unterhaltung gelöscht werden.
ms.openlocfilehash: abaa0c3d8b7001b2f42a38d1c82475edba32d2c5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757930"
---
# <a name="deletetype"></a><span data-ttu-id="4f506-103">DeleteType</span><span class="sxs-lookup"><span data-stu-id="4f506-103">DeleteType</span></span>

<span data-ttu-id="4f506-104">Das **DeleteType** -Element gibt an, wie Elemente in einer Unterhaltung gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="4f506-104">The **DeleteType** element indicates how items in a conversation are deleted.</span></span> 
  
- [<span data-ttu-id="4f506-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="4f506-105">ApplyConversationAction</span></span>](applyconversationaction.md)  
- [<span data-ttu-id="4f506-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="4f506-106">ConversationActions</span></span>](conversationactions.md)  
- [<span data-ttu-id="4f506-107">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="4f506-107">ConversationAction</span></span>](conversationaction.md)  
- [<span data-ttu-id="4f506-108">DeleteType</span><span class="sxs-lookup"><span data-stu-id="4f506-108">DeleteType</span></span>](deletetype.md)
  
```XML
<DeleteType> HardDelete | MoveToDeletedItems | SoftDelete </DeleteType>
```

 <span data-ttu-id="4f506-109">**DisposalType**</span><span class="sxs-lookup"><span data-stu-id="4f506-109">**DisposalType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4f506-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4f506-110">Attributes and elements</span></span>

<span data-ttu-id="4f506-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4f506-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4f506-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="4f506-112">Attributes</span></span>

<span data-ttu-id="4f506-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="4f506-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4f506-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4f506-114">Child elements</span></span>

<span data-ttu-id="4f506-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="4f506-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4f506-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4f506-116">Parent elements</span></span>

|<span data-ttu-id="4f506-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f506-117">**Element**</span></span>|<span data-ttu-id="4f506-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f506-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4f506-119">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="4f506-119">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="4f506-120">Enthält eine einzelne Aktion auf einem einzelnen Gespräch angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f506-120">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4f506-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="4f506-121">Text value</span></span>

<span data-ttu-id="4f506-122">Der Textwert der **DeleteType** -Element gibt an, wie Elemente in einer Unterhaltung gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="4f506-122">The text value of the **DeleteType** element indicates how items in a conversation are deleted.</span></span> <span data-ttu-id="4f506-123">Im folgenden sind die möglichen Textwerte:</span><span class="sxs-lookup"><span data-stu-id="4f506-123">The following are the possible text values:</span></span> 
  
- <span data-ttu-id="4f506-124">HardDelete - gibt an, dass Elemente in einer Unterhaltung dauerhaft aus der Postfachdatenbank entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="4f506-124">HardDelete - Indicates that items in a conversation are permanently removed from the mailbox database.</span></span>
    
- <span data-ttu-id="4f506-125">MoveToDeleteItems - gibt an, dass Elemente in einer Unterhaltung in den Ordner Gelöschte Objekte verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="4f506-125">MoveToDeleteItems - Indicates that items in a conversation are moved to the Deleted Items folder.</span></span>
    
- <span data-ttu-id="4f506-126">SoftDelete - gibt an, dass Elemente in einer Unterhaltung in verschoben werden die Dumpster Wenn die Dumpster ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4f506-126">SoftDelete - Indicates that items in a conversation are moved to the dumpster if the dumpster is enabled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4f506-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4f506-127">Remarks</span></span>

<span data-ttu-id="4f506-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4f506-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4f506-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4f506-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f506-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="4f506-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4f506-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4f506-131">Schema Name</span></span>  <br/> |<span data-ttu-id="4f506-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="4f506-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="4f506-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4f506-133">Validation File</span></span>  <br/> |<span data-ttu-id="4f506-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4f506-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4f506-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4f506-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="4f506-136">False</span><span class="sxs-lookup"><span data-stu-id="4f506-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4f506-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f506-137">See also</span></span>

- [<span data-ttu-id="4f506-138">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4f506-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
- [<span data-ttu-id="4f506-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4f506-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

