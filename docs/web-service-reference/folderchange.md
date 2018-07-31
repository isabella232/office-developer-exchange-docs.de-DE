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
description: FolderChange-Element stellt eine Auflistung von Änderungen in einem gemeinsamen Ordner ausgeführt werden.
ms.openlocfilehash: f25defa9974f7b5dd0c683c7657983741890d45d
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354330"
---
# <a name="folderchange"></a><span data-ttu-id="6a9a5-103">FolderChange</span><span class="sxs-lookup"><span data-stu-id="6a9a5-103">FolderChange</span></span>

<span data-ttu-id="6a9a5-104">**FolderChange** -Element stellt eine Auflistung von Änderungen in einem gemeinsamen Ordner ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6a9a5-104">The **FolderChange** element represents a collection of changes to be performed on a single folder.</span></span> 
  
- [<span data-ttu-id="6a9a5-105">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="6a9a5-105">UpdateFolder</span></span>](updatefolder.md) 
- [<span data-ttu-id="6a9a5-106">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="6a9a5-106">FolderChanges</span></span>](folderchanges.md) 
- [<span data-ttu-id="6a9a5-107">FolderChange</span><span class="sxs-lookup"><span data-stu-id="6a9a5-107">FolderChange</span></span>](folderchange.md)
  
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

<span data-ttu-id="6a9a5-108">**FolderChangeType**</span><span class="sxs-lookup"><span data-stu-id="6a9a5-108">**FolderChangeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="6a9a5-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6a9a5-109">Attributes and elements</span></span>

<span data-ttu-id="6a9a5-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6a9a5-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6a9a5-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="6a9a5-111">Attributes</span></span>

<span data-ttu-id="6a9a5-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="6a9a5-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6a9a5-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6a9a5-113">Child elements</span></span>

|<span data-ttu-id="6a9a5-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="6a9a5-114">**Element**</span></span>|<span data-ttu-id="6a9a5-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6a9a5-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6a9a5-116">FolderId</span><span class="sxs-lookup"><span data-stu-id="6a9a5-116">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="6a9a5-117">Enthält den Schlüssel-ID und Ändern eines Ordners zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6a9a5-117">Contains the identifier and change key of a folder to update.</span></span>  <br/> |
|[<span data-ttu-id="6a9a5-118">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="6a9a5-118">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="6a9a5-119">Identifiziert MicrosoftExchange Server 2007-Ordner, die nach Namen verwiesen werden können.</span><span class="sxs-lookup"><span data-stu-id="6a9a5-119">Identifies MicrosoftExchange Server 2007 folders that can be referenced by name.</span></span>  <br/> |
|[<span data-ttu-id="6a9a5-120">Updates (Ordner)</span><span class="sxs-lookup"><span data-stu-id="6a9a5-120">Updates (Folder)</span></span>](updates-folder.md) <br/> |<span data-ttu-id="6a9a5-121">Definiert den Typ des Updates, die für einen Ordner ausgeführt wird, die durch die [FolderId](folderid.md) oder [DistinguishedFolderId](distinguishedfolderid.md) -Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="6a9a5-121">Defines the type of update that is performed on a folder that is identified by either the [FolderId](folderid.md) or [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6a9a5-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6a9a5-122">Parent elements</span></span>

|<span data-ttu-id="6a9a5-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="6a9a5-123">**Element**</span></span>|<span data-ttu-id="6a9a5-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6a9a5-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6a9a5-125">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="6a9a5-125">FolderChanges</span></span>](folderchanges.md) <br/> |<span data-ttu-id="6a9a5-126">Stellt eine Auflistung von Änderungen für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="6a9a5-126">Represents a collection of changes for a folder.</span></span>  <br/> <span data-ttu-id="6a9a5-127">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="6a9a5-127">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateFolder/FolderChanges` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a9a5-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6a9a5-128">Remarks</span></span>

<span data-ttu-id="6a9a5-129">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Exchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6a9a5-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6a9a5-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6a9a5-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6a9a5-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="6a9a5-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6a9a5-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6a9a5-132">Schema name</span></span>  <br/> |<span data-ttu-id="6a9a5-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6a9a5-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="6a9a5-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6a9a5-134">Validation file</span></span>  <br/> |<span data-ttu-id="6a9a5-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6a9a5-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6a9a5-136">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="6a9a5-136">Can be empty</span></span>  <br/> |<span data-ttu-id="6a9a5-137">False</span><span class="sxs-lookup"><span data-stu-id="6a9a5-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6a9a5-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a9a5-138">See also</span></span>

- [<span data-ttu-id="6a9a5-139">UpdateFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6a9a5-139">UpdateFolder operation</span></span>](updatefolder-operation.md)

