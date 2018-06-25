---
title: ContextFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContextFolderId
api_type:
- schema
ms.assetid: 48de92aa-e124-42b5-89bc-cdce5e93d78b
description: Das ContextFolderId-Element gibt an, den Ordner, der für Aktionen gerichtet ist, die Ordner zu verwenden. Dieses Element muss beim Kopieren, löschen, verschieben und Festlegen von Zustand "gelesen" für Unterhaltungselemente in einem Zielordner vorhanden sein.
ms.openlocfilehash: bd863d0395b9b9d7b437833acfb656fec4580985
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757684"
---
# <a name="contextfolderid"></a><span data-ttu-id="4390b-104">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="4390b-104">ContextFolderId</span></span>

<span data-ttu-id="4390b-105">Das **ContextFolderId** -Element gibt an, den Ordner, der für Aktionen gerichtet ist, die Ordner zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4390b-105">The **ContextFolderId** element indicates the folder that is targeted for actions that use folders.</span></span> <span data-ttu-id="4390b-106">Dieses Element muss beim Kopieren, löschen, verschieben und Festlegen von Zustand "gelesen" für Unterhaltungselemente in einem Zielordner vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="4390b-106">This element must be present when copying, deleting, moving, and setting read state on conversation items in a target folder.</span></span> 
  
[<span data-ttu-id="4390b-107">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="4390b-107">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="4390b-108">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="4390b-108">ConversationActions</span></span>](conversationactions.md)
  
[<span data-ttu-id="4390b-109">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="4390b-109">ConversationAction</span></span>](conversationaction.md)
  
[<span data-ttu-id="4390b-110">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="4390b-110">ContextFolderId</span></span>](contextfolderid.md)
  
```XML
<ContextFolderId>
   <FolderId/>
</ContextFolderId>
```

 <span data-ttu-id="4390b-111">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="4390b-111">**TargetFolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4390b-112">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4390b-112">Attributes and elements</span></span>

<span data-ttu-id="4390b-113">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4390b-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4390b-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="4390b-114">Attributes</span></span>

<span data-ttu-id="4390b-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="4390b-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4390b-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4390b-116">Child elements</span></span>

|<span data-ttu-id="4390b-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="4390b-117">**Element**</span></span>|<span data-ttu-id="4390b-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4390b-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4390b-119">FolderId</span><span class="sxs-lookup"><span data-stu-id="4390b-119">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="4390b-120">Enthält den Schlüssel-ID und die Änderung des kontextordners.</span><span class="sxs-lookup"><span data-stu-id="4390b-120">Contains the identifier and change key of the context folder.</span></span>  <br/> |
|[<span data-ttu-id="4390b-121">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="4390b-121">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="4390b-122">Bezeichnet die Ordner, die nach Namen verwiesen werden können.</span><span class="sxs-lookup"><span data-stu-id="4390b-122">Identifies folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4390b-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4390b-123">Parent elements</span></span>

|<span data-ttu-id="4390b-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="4390b-124">**Element**</span></span>|<span data-ttu-id="4390b-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4390b-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4390b-126">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="4390b-126">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="4390b-127">Enthält eine einzelne Aktion auf einem einzelnen Gespräch angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4390b-127">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4390b-128">Textwert</span><span class="sxs-lookup"><span data-stu-id="4390b-128">Text value</span></span>

<span data-ttu-id="4390b-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="4390b-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4390b-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4390b-130">Remarks</span></span>

<span data-ttu-id="4390b-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4390b-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4390b-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4390b-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4390b-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="4390b-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4390b-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4390b-134">Schema Name</span></span>  <br/> |<span data-ttu-id="4390b-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="4390b-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="4390b-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4390b-136">Validation File</span></span>  <br/> |<span data-ttu-id="4390b-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4390b-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4390b-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4390b-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="4390b-139">False</span><span class="sxs-lookup"><span data-stu-id="4390b-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4390b-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4390b-140">See also</span></span>



[<span data-ttu-id="4390b-141">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4390b-141">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)

