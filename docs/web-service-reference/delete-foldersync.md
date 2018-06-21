---
title: Delete (FolderSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Delete
api_type:
- schema
ms.assetid: c4397d91-43ef-40a9-a80e-d31501a33caa
description: Das Löschen eines Elements bezeichnet einen einzelnen Ordner im lokalen Client-Speicher zu löschen.
ms.openlocfilehash: 5cad36c6fcff782195fdb285e2d3c4f3c5ec0f1e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/21/2018
ms.locfileid: "19757899"
---
# <a name="delete-foldersync"></a><span data-ttu-id="c5e3b-103">Delete (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="c5e3b-103">Delete (FolderSync)</span></span>

<span data-ttu-id="c5e3b-104">Das Element **Löschen** bezeichnet einen einzelnen Ordner im lokalen Client-Speicher zu löschen.</span><span class="sxs-lookup"><span data-stu-id="c5e3b-104">The **Delete** element identifies a single folder to delete in the local client store.</span></span> 
  
- [<span data-ttu-id="c5e3b-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="c5e3b-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)  
- [<span data-ttu-id="c5e3b-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c5e3b-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="c5e3b-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c5e3b-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)  
- [<span data-ttu-id="c5e3b-108">Änderungen (Hierarchie)</span><span class="sxs-lookup"><span data-stu-id="c5e3b-108">Changes (Hierarchy)</span></span>](changes-hierarchy.md)  
- [<span data-ttu-id="c5e3b-109">Delete (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="c5e3b-109">Delete (FolderSync)</span></span>](delete-foldersync.md)
  
```xml
<Delete>
   <FolderId/>
</Delete>
```

<span data-ttu-id="c5e3b-110">**SyncFolderHierarchyDeleteType**</span><span class="sxs-lookup"><span data-stu-id="c5e3b-110">**SyncFolderHierarchyDeleteType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c5e3b-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c5e3b-111">Attributes and elements</span></span>

<span data-ttu-id="c5e3b-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c5e3b-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c5e3b-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="c5e3b-113">Attributes</span></span>

<span data-ttu-id="c5e3b-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="c5e3b-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c5e3b-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c5e3b-115">Child elements</span></span>

|<span data-ttu-id="c5e3b-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="c5e3b-116">**Element**</span></span>|<span data-ttu-id="c5e3b-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c5e3b-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c5e3b-118">FolderId</span><span class="sxs-lookup"><span data-stu-id="c5e3b-118">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="c5e3b-119">Enthält den Schlüssel-ID und Ändern eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="c5e3b-119">Contains the identifier and change key of a folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c5e3b-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c5e3b-120">Parent elements</span></span>

|<span data-ttu-id="c5e3b-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="c5e3b-121">**Element**</span></span>|<span data-ttu-id="c5e3b-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c5e3b-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c5e3b-123">Änderungen (Hierarchie)</span><span class="sxs-lookup"><span data-stu-id="c5e3b-123">Changes (Hierarchy)</span></span>](changes-hierarchy.md) <br/> |<span data-ttu-id="c5e3b-124">Enthält eine sequenzierten Array von Änderungstypen, die den Typ der Unterschiede zwischen den Ordnern auf dem Client und die Ordner auf dem Computer mit Microsoft Exchange Server 2007 darstellen.</span><span class="sxs-lookup"><span data-stu-id="c5e3b-124">Contains a sequenced array of change types that represent the type of differences between the folders on the client and the folders on the computer that is running Microsoft Exchange Server 2007.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5e3b-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c5e3b-125">Remarks</span></span>

<span data-ttu-id="c5e3b-126">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Exchange 2007-Computers, der die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="c5e3b-126">The schema that describes this element is located in the EWS virtual directory of the Exchange 2007 computer that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c5e3b-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c5e3b-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5e3b-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="c5e3b-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c5e3b-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c5e3b-129">Schema name</span></span>  <br/> |<span data-ttu-id="c5e3b-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c5e3b-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="c5e3b-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c5e3b-131">Validation file</span></span>  <br/> |<span data-ttu-id="c5e3b-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c5e3b-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c5e3b-133">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="c5e3b-133">Can be empty</span></span>  <br/> |<span data-ttu-id="c5e3b-134">False</span><span class="sxs-lookup"><span data-stu-id="c5e3b-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c5e3b-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5e3b-135">See also</span></span>

- [<span data-ttu-id="c5e3b-136">SyncFolderHierarchy-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c5e3b-136">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)
- [<span data-ttu-id="c5e3b-137">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="c5e3b-137">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="c5e3b-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c5e3b-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

