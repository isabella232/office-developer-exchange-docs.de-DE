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
description: Das parentfolderid-Element gibt den Ordner an, in dem ein neuer Ordner erstellt wird, oder den Ordner, der für den FindConversation-Vorgang gesucht werden soll.
ms.openlocfilehash: 36e63266d10603c4d453a37e2b0d22e02599e516
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467802"
---
# <a name="parentfolderid-targetfolderidtype"></a><span data-ttu-id="26525-103">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="26525-103">ParentFolderId (TargetFolderIdType)</span></span>

<span data-ttu-id="26525-104">Das **parentfolderid** -Element gibt den Ordner an, in dem ein neuer Ordner erstellt wird, oder den Ordner, der für den [FindConversation-Vorgang](findconversation-operation.md)gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="26525-104">The **ParentFolderId** element identifies the folder in which a new folder is created or the folder to search for the [FindConversation operation](findconversation-operation.md).</span></span>
  
```xml
<ParentFolderId>
   <DistinguishedFolderId/>
</ParentFolderId>
```

```xml
<ParentFolderId>
   <FolderId/> 
</ParentFolderId>
```

<span data-ttu-id="26525-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="26525-105">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="26525-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="26525-106">Attributes and elements</span></span>

<span data-ttu-id="26525-107">Das **parentfolderid** -Element enthält zwei untergeordnete Elemente.</span><span class="sxs-lookup"><span data-stu-id="26525-107">The **ParentFolderId** element contains two child elements.</span></span> <span data-ttu-id="26525-108">Die untergeordneten Elemente sind im Schema gegenseitig ausschliessend.</span><span class="sxs-lookup"><span data-stu-id="26525-108">The child elements are mutually exclusive in the schema.</span></span> 
  
### <a name="attributes"></a><span data-ttu-id="26525-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="26525-109">Attributes</span></span>

<span data-ttu-id="26525-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="26525-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="26525-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="26525-111">Child elements</span></span>

|<span data-ttu-id="26525-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="26525-112">**Element**</span></span>|<span data-ttu-id="26525-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="26525-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26525-114">FolderId</span><span class="sxs-lookup"><span data-stu-id="26525-114">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="26525-115">Enthält den erforderlichen Bezeichner und den optionalen Änderungsschlüssel eines Ordners, in dem ein neuer Ordner erstellt wird, oder der Ordner, der für den [FindConversation-Vorgang](findconversation-operation.md)durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="26525-115">Contains the required identifier and the optional change key of a folder in which a new folder is created or the folder that is searched for the [FindConversation operation](findconversation-operation.md).</span></span> <span data-ttu-id="26525-116">Die Verwendung dieses Elements schließt die Verwendung des [DistinguishedFolderId](distinguishedfolderid.md) -Elements aus.</span><span class="sxs-lookup"><span data-stu-id="26525-116">Using this element excludes the use of the [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span>  <br/> |
|[<span data-ttu-id="26525-117">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="26525-117">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="26525-118">Bezeichnet die standarmäßigen Microsoft Exchange Server 2007-Ordner.</span><span class="sxs-lookup"><span data-stu-id="26525-118">Identifies default Microsoft Exchange Server 2007 folders.</span></span> <span data-ttu-id="26525-119">Die Verwendung dieses Elements schließt die Verwendung des [Folder](folderid.md) -Elements aus.</span><span class="sxs-lookup"><span data-stu-id="26525-119">Using this element excludes the use of the [FolderId](folderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="26525-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="26525-120">Parent elements</span></span>

|<span data-ttu-id="26525-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="26525-121">**Element**</span></span>|<span data-ttu-id="26525-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="26525-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26525-123">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="26525-123">CreateFolder</span></span>](createfolder.md) <br/> |<span data-ttu-id="26525-124">Definiert eine Anforderung zum Erstellen eines Ordners in der Exchange-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="26525-124">Defines a request to create a folder in the Exchange database.</span></span>  <br/> <span data-ttu-id="26525-125">Im folgenden finden Sie den XPath-Ausdruck für dieses Element:`/CreateFolder`</span><span class="sxs-lookup"><span data-stu-id="26525-125">The following is the XPath expression to this element:  `/CreateFolder`</span></span> <br/> |
|[<span data-ttu-id="26525-126">FindConversation</span><span class="sxs-lookup"><span data-stu-id="26525-126">FindConversation</span></span>](findconversation.md) <br/> |<span data-ttu-id="26525-127">Definiert eine Anforderung zum Suchen von Unterhaltungen in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="26525-127">Defines a request to find conversations in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="26525-128">Textwert</span><span class="sxs-lookup"><span data-stu-id="26525-128">Text value</span></span>

<span data-ttu-id="26525-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="26525-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="26525-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26525-130">Remarks</span></span>

<span data-ttu-id="26525-131">Die beiden untergeordneten Elemente werden verwendet, um den Ordner zu definieren, der den neuen Ordner enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="26525-131">The two child elements are used to define the folder that will contain the new folder.</span></span> <span data-ttu-id="26525-132">Sie müssen entweder die [Ordner](folderid.md) -oder das [DistinguishedFolderId](distinguishedfolderid.md) -Element auswählen, um den übergeordneten Ordner des neuen Ordners zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="26525-132">You must select either the [FolderId](folderid.md) or the [DistinguishedFolderId](distinguishedfolderid.md) element to identify the parent folder of the new folder.</span></span> <span data-ttu-id="26525-133">Beide Elemente können nicht gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="26525-133">You cannot use both elements at the same time.</span></span> <span data-ttu-id="26525-134">Dieses Element ist zum Erstellen von Ordnern erforderlich.</span><span class="sxs-lookup"><span data-stu-id="26525-134">This element is required to create folders.</span></span> 
  
<span data-ttu-id="26525-135">Das [parentfolderid](parentfolderid.md) -Element beschreibt den Speicherort vorhandener Elemente und Ordner.</span><span class="sxs-lookup"><span data-stu-id="26525-135">The [ParentFolderId](parentfolderid.md) element describes the location of existing items and folders.</span></span> 
  
<span data-ttu-id="26525-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="26525-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="26525-137">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="26525-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26525-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="26525-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="26525-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="26525-139">Schema Name</span></span>  <br/> |<span data-ttu-id="26525-140">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="26525-140">Message schema</span></span>  <br/> |
|<span data-ttu-id="26525-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="26525-141">Validation File</span></span>  <br/> |<span data-ttu-id="26525-142">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="26525-142">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="26525-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="26525-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="26525-144">False</span><span class="sxs-lookup"><span data-stu-id="26525-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="26525-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26525-145">See also</span></span>

- [<span data-ttu-id="26525-146">CreateFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="26525-146">CreateFolder operation</span></span>](createfolder-operation.md)
- [<span data-ttu-id="26525-147">FindConversation-Vorgang</span><span class="sxs-lookup"><span data-stu-id="26525-147">FindConversation operation</span></span>](findconversation-operation.md)
- [<span data-ttu-id="26525-148">Erstellen von Ordnern (Exchange Webdienste)</span><span class="sxs-lookup"><span data-stu-id="26525-148">Creating Folders (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

