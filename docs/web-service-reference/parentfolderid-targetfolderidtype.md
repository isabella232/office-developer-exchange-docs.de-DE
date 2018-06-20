---
title: ParentFolderId (TargetFolderIdType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ParentFolderId
api_type:
- schema
ms.assetid: 0e3e6e5f-06d0-499b-8ca4-d36036521658
description: Das ParentFolderId-Element identifiziert den Ordner in der erstellt wird, eines neuen Ordners oder den Ordner für den Vorgang FindConversation suchen.
ms.openlocfilehash: 61072e1dd3321beb5f3b76d9accf20530b443796
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830686"
---
# <a name="parentfolderid-targetfolderidtype"></a><span data-ttu-id="dd847-103">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="dd847-103">ParentFolderId (TargetFolderIdType)</span></span>

<span data-ttu-id="dd847-104">Das **ParentFolderId** -Element identifiziert den Ordner in der erstellt wird, eines neuen Ordners oder den Ordner für den [Vorgang FindConversation](findconversation-operation.md)suchen.</span><span class="sxs-lookup"><span data-stu-id="dd847-104">The **ParentFolderId** element identifies the folder in which a new folder is created or the folder to search for the [FindConversation operation](findconversation-operation.md).</span></span>
  
```xml
<ParentFolderId>
   <DistinguishedFolderId/>
</ParentFolderId>
```

<span data-ttu-id="dd847-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="dd847-105">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="dd847-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="dd847-106">Attributes and elements</span></span>

<span data-ttu-id="dd847-107">Das **ParentFolderId** -Element enthält zwei untergeordnete Elemente.</span><span class="sxs-lookup"><span data-stu-id="dd847-107">The **ParentFolderId** element contains two child elements.</span></span> <span data-ttu-id="dd847-108">Die untergeordneten Elemente schließen sich gegenseitig aus im Schema.</span><span class="sxs-lookup"><span data-stu-id="dd847-108">The child elements are mutually exclusive in the schema.</span></span> 
  
### <a name="attributes"></a><span data-ttu-id="dd847-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="dd847-109">Attributes</span></span>

<span data-ttu-id="dd847-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="dd847-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dd847-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dd847-111">Child elements</span></span>

|<span data-ttu-id="dd847-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="dd847-112">**Element**</span></span>|<span data-ttu-id="dd847-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dd847-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dd847-114">FolderId</span><span class="sxs-lookup"><span data-stu-id="dd847-114">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="dd847-115">Enthält die erforderlichen Bezeichner und der Key optional Ändern eines Ordners in der erstellt wird, eines neuen Ordners oder den Ordner, der für den [Vorgang FindConversation](findconversation-operation.md)durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="dd847-115">Contains the required identifier and the optional change key of a folder in which a new folder is created or the folder that is searched for the [FindConversation operation](findconversation-operation.md).</span></span> <span data-ttu-id="dd847-116">Die Verwendung dieses Elements schließt die Verwendung des [DistinguishedFolderId](distinguishedfolderid.md) -Elements.</span><span class="sxs-lookup"><span data-stu-id="dd847-116">Using this element excludes the use of the [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span>  <br/> |
|[<span data-ttu-id="dd847-117">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="dd847-117">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="dd847-118">Bezeichnet die standarmäßigen Microsoft Exchange Server 2007-Ordner.</span><span class="sxs-lookup"><span data-stu-id="dd847-118">Identifies default Microsoft Exchange Server 2007 folders.</span></span> <span data-ttu-id="dd847-119">Die Verwendung dieses Elements schließt die Verwendung des [FolderId](folderid.md) -Elements.</span><span class="sxs-lookup"><span data-stu-id="dd847-119">Using this element excludes the use of the [FolderId](folderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dd847-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dd847-120">Parent elements</span></span>

|<span data-ttu-id="dd847-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="dd847-121">**Element**</span></span>|<span data-ttu-id="dd847-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dd847-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dd847-123">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="dd847-123">CreateFolder</span></span>](createfolder.md) <br/> |<span data-ttu-id="dd847-124">Definiert eine Anforderung an einen Ordner in der Exchange-Datenbank zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dd847-124">Defines a request to create a folder in the Exchange database.</span></span>  <br/> <span data-ttu-id="dd847-125">Es folgt der XPath-Ausdruck, der dieses Element:`/CreateFolder`</span><span class="sxs-lookup"><span data-stu-id="dd847-125">The following is the XPath expression to this element:  `/CreateFolder`</span></span> <br/> |
|[<span data-ttu-id="dd847-126">FindConversation</span><span class="sxs-lookup"><span data-stu-id="dd847-126">FindConversation</span></span>](findconversation.md) <br/> |<span data-ttu-id="dd847-127">Definiert eine Anforderung an Unterhaltungen in einem Postfach suchen.</span><span class="sxs-lookup"><span data-stu-id="dd847-127">Defines a request to find conversations in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dd847-128">Textwert</span><span class="sxs-lookup"><span data-stu-id="dd847-128">Text value</span></span>

<span data-ttu-id="dd847-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="dd847-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dd847-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dd847-130">Remarks</span></span>

<span data-ttu-id="dd847-131">Die beiden untergeordneten Elemente werden verwendet, den Ordner zu definieren, der den neuen Ordner enthalten wird.</span><span class="sxs-lookup"><span data-stu-id="dd847-131">The two child elements are used to define the folder that will contain the new folder.</span></span> <span data-ttu-id="dd847-132">Sie müssen entweder die [FolderId](folderid.md) oder das [DistinguishedFolderId](distinguishedfolderid.md) -Element zum Identifizieren des übergeordneten Ordners des neuen Ordners auswählen.</span><span class="sxs-lookup"><span data-stu-id="dd847-132">You must select either the [FolderId](folderid.md) or the [DistinguishedFolderId](distinguishedfolderid.md) element to identify the parent folder of the new folder.</span></span> <span data-ttu-id="dd847-133">Sie können nicht beide Elemente gleichzeitig verwenden.</span><span class="sxs-lookup"><span data-stu-id="dd847-133">You cannot use both elements at the same time.</span></span> <span data-ttu-id="dd847-134">Dieses Element ist erforderlich, um Ordner zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dd847-134">This element is required to create folders.</span></span> 
  
<span data-ttu-id="dd847-135">Das Element [ParentFolderId](parentfolderid.md) beschreibt den Speicherort der vorhandenen Elemente und Ordner.</span><span class="sxs-lookup"><span data-stu-id="dd847-135">The [ParentFolderId](parentfolderid.md) element describes the location of existing items and folders.</span></span> 
  
<span data-ttu-id="dd847-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="dd847-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dd847-137">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="dd847-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dd847-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="dd847-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dd847-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="dd847-139">Schema Name</span></span>  <br/> |<span data-ttu-id="dd847-140">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="dd847-140">Message schema</span></span>  <br/> |
|<span data-ttu-id="dd847-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="dd847-141">Validation File</span></span>  <br/> |<span data-ttu-id="dd847-142">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="dd847-142">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dd847-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="dd847-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="dd847-144">False</span><span class="sxs-lookup"><span data-stu-id="dd847-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dd847-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd847-145">See also</span></span>

- [<span data-ttu-id="dd847-146">CreateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="dd847-146">CreateFolder operation</span></span>](createfolder-operation.md)
- [<span data-ttu-id="dd847-147">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="dd847-147">FindConversation operation</span></span>](findconversation-operation.md)
- [<span data-ttu-id="dd847-148">Erstellen von Ordnern (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="dd847-148">Creating Folders (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

