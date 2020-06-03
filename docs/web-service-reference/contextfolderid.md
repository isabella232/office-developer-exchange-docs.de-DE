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
description: Das ContextFolderId-Element gibt den Ordner an, der für Aktionen vorgesehen ist, die Ordner verwenden. Dieses Element muss beim Kopieren, löschen, verschieben und Festlegen des Lese Zustands für Unterhaltungselemente in einem Zielordner vorhanden sein.
ms.openlocfilehash: 60f1eaf3b45eee83632c7da6f453a1d09f54d9fd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529259"
---
# <a name="contextfolderid"></a><span data-ttu-id="12eeb-104">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="12eeb-104">ContextFolderId</span></span>

<span data-ttu-id="12eeb-105">Das **ContextFolderId** -Element gibt den Ordner an, der für Aktionen vorgesehen ist, die Ordner verwenden.</span><span class="sxs-lookup"><span data-stu-id="12eeb-105">The **ContextFolderId** element indicates the folder that is targeted for actions that use folders.</span></span> <span data-ttu-id="12eeb-106">Dieses Element muss beim Kopieren, löschen, verschieben und Festlegen des Lese Zustands für Unterhaltungselemente in einem Zielordner vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="12eeb-106">This element must be present when copying, deleting, moving, and setting read state on conversation items in a target folder.</span></span> 
  
- [<span data-ttu-id="12eeb-107">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="12eeb-107">ApplyConversationAction</span></span>](applyconversationaction.md) 
- [<span data-ttu-id="12eeb-108">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="12eeb-108">ConversationActions</span></span>](conversationactions.md)
- [<span data-ttu-id="12eeb-109">Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="12eeb-109">ConversationAction</span></span>](conversationaction.md)
- [<span data-ttu-id="12eeb-110">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="12eeb-110">ContextFolderId</span></span>](contextfolderid.md)
  
```XML
<ContextFolderId>
   <FolderId/>
</ContextFolderId>
```

```XML
<ContextFolderId>
   <DistinguishedFolderId/>
</ContextFolderId>
```


<span data-ttu-id="12eeb-111">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="12eeb-111">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="12eeb-112">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="12eeb-112">Attributes and elements</span></span>

<span data-ttu-id="12eeb-113">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="12eeb-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="12eeb-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="12eeb-114">Attributes</span></span>

<span data-ttu-id="12eeb-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="12eeb-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="12eeb-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="12eeb-116">Child elements</span></span>

|<span data-ttu-id="12eeb-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="12eeb-117">**Element**</span></span>|<span data-ttu-id="12eeb-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="12eeb-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="12eeb-119">FolderId</span><span class="sxs-lookup"><span data-stu-id="12eeb-119">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="12eeb-120">Enthält den Bezeichner und den Änderungsschlüssel des Kontext Ordners.</span><span class="sxs-lookup"><span data-stu-id="12eeb-120">Contains the identifier and change key of the context folder.</span></span>  <br/> |
|[<span data-ttu-id="12eeb-121">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="12eeb-121">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="12eeb-122">Identifiziert Ordner, auf die über den Namen verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="12eeb-122">Identifies folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="12eeb-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="12eeb-123">Parent elements</span></span>

|<span data-ttu-id="12eeb-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="12eeb-124">**Element**</span></span>|<span data-ttu-id="12eeb-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="12eeb-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="12eeb-126">Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="12eeb-126">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="12eeb-127">Enthält eine einzelne Aktion, die auf eine einzelne Unterhaltung angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="12eeb-127">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="12eeb-128">Textwert</span><span class="sxs-lookup"><span data-stu-id="12eeb-128">Text value</span></span>

<span data-ttu-id="12eeb-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="12eeb-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="12eeb-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12eeb-130">Remarks</span></span>

<span data-ttu-id="12eeb-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="12eeb-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="12eeb-132">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="12eeb-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="12eeb-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="12eeb-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="12eeb-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="12eeb-134">Schema Name</span></span>  <br/> |<span data-ttu-id="12eeb-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="12eeb-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="12eeb-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="12eeb-136">Validation File</span></span>  <br/> |<span data-ttu-id="12eeb-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="12eeb-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="12eeb-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="12eeb-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="12eeb-139">False</span><span class="sxs-lookup"><span data-stu-id="12eeb-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="12eeb-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12eeb-140">See also</span></span>

- [<span data-ttu-id="12eeb-141">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="12eeb-141">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)

