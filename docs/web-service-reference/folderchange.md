---
title: FolderChange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderChange
api_type:
- schema
ms.assetid: 23279750-131b-4e1a-b7d1-be235c4e0891
description: Das FolderChange-Element stellt eine Auflistung von Änderungen dar, die für einen einzelnen Ordner ausgeführt werden sollen.
ms.openlocfilehash: e4a025bef100fdd478be545b6448b15886e47c60
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530239"
---
# <a name="folderchange"></a><span data-ttu-id="0cc60-103">FolderChange</span><span class="sxs-lookup"><span data-stu-id="0cc60-103">FolderChange</span></span>

<span data-ttu-id="0cc60-104">Das **FolderChange** -Element stellt eine Auflistung von Änderungen dar, die für einen einzelnen Ordner ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0cc60-104">The **FolderChange** element represents a collection of changes to be performed on a single folder.</span></span> 
  
- [<span data-ttu-id="0cc60-105">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="0cc60-105">UpdateFolder</span></span>](updatefolder.md) 
- [<span data-ttu-id="0cc60-106">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="0cc60-106">FolderChanges</span></span>](folderchanges.md) 
- [<span data-ttu-id="0cc60-107">FolderChange</span><span class="sxs-lookup"><span data-stu-id="0cc60-107">FolderChange</span></span>](folderchange.md)
  
```xml
<FolderChange>
   <FolderId/>
   <Updates/>
</FolderChange>
```

```xml
<FolderChange>
   <DistinguishedFolderId/>
   <Updates/>
</FolderChange>
```

<span data-ttu-id="0cc60-108">**FolderChangeType**</span><span class="sxs-lookup"><span data-stu-id="0cc60-108">**FolderChangeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="0cc60-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0cc60-109">Attributes and elements</span></span>

<span data-ttu-id="0cc60-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0cc60-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0cc60-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="0cc60-111">Attributes</span></span>

<span data-ttu-id="0cc60-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="0cc60-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0cc60-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0cc60-113">Child elements</span></span>

|<span data-ttu-id="0cc60-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="0cc60-114">**Element**</span></span>|<span data-ttu-id="0cc60-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0cc60-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0cc60-116">FolderId</span><span class="sxs-lookup"><span data-stu-id="0cc60-116">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="0cc60-117">Enthält den Bezeichner und den Änderungsschlüssel eines Ordners, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0cc60-117">Contains the identifier and change key of a folder to update.</span></span>  <br/> |
|[<span data-ttu-id="0cc60-118">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="0cc60-118">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="0cc60-119">Identifiziert Microsoft Exchange Server 2007-Ordner, auf die über den Namen verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="0cc60-119">Identifies MicrosoftExchange Server 2007 folders that can be referenced by name.</span></span>  <br/> |
|[<span data-ttu-id="0cc60-120">Updates (Ordner)</span><span class="sxs-lookup"><span data-stu-id="0cc60-120">Updates (Folder)</span></span>](updates-folder.md) <br/> |<span data-ttu-id="0cc60-121">Definiert den Aktualisierungstyp, der für einen Ordner ausgeführt wird, der entweder durch das [Folder](folderid.md) -oder [DistinguishedFolderId](distinguishedfolderid.md) -Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="0cc60-121">Defines the type of update that is performed on a folder that is identified by either the [FolderId](folderid.md) or [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0cc60-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0cc60-122">Parent elements</span></span>

|<span data-ttu-id="0cc60-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="0cc60-123">**Element**</span></span>|<span data-ttu-id="0cc60-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0cc60-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0cc60-125">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="0cc60-125">FolderChanges</span></span>](folderchanges.md) <br/> |<span data-ttu-id="0cc60-126">Stellt eine Auflistung von Änderungen für einen Ordner dar.</span><span class="sxs-lookup"><span data-stu-id="0cc60-126">Represents a collection of changes for a folder.</span></span>  <br/> <span data-ttu-id="0cc60-127">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="0cc60-127">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateFolder/FolderChanges` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0cc60-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0cc60-128">Remarks</span></span>

<span data-ttu-id="0cc60-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server 2007 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0cc60-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0cc60-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="0cc60-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0cc60-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="0cc60-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0cc60-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0cc60-132">Schema name</span></span>  <br/> |<span data-ttu-id="0cc60-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="0cc60-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="0cc60-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0cc60-134">Validation file</span></span>  <br/> |<span data-ttu-id="0cc60-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0cc60-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0cc60-136">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="0cc60-136">Can be empty</span></span>  <br/> |<span data-ttu-id="0cc60-137">False</span><span class="sxs-lookup"><span data-stu-id="0cc60-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0cc60-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0cc60-138">See also</span></span>

- [<span data-ttu-id="0cc60-139">UpdateFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0cc60-139">UpdateFolder operation</span></span>](updatefolder-operation.md)

