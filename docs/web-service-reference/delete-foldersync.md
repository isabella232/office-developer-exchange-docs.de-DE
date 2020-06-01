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
description: Das delete-Element identifiziert einen einzelnen Ordner, der im lokalen Clientspeicher gelöscht werden soll.
ms.openlocfilehash: 68f8687b8cf0723d7fd63a3d55da8ef7c2f98f8e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44454981"
---
# <a name="delete-foldersync"></a><span data-ttu-id="f533c-103">Delete (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="f533c-103">Delete (FolderSync)</span></span>

<span data-ttu-id="f533c-104">Das **Delete** -Element identifiziert einen einzelnen Ordner, der im lokalen Clientspeicher gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="f533c-104">The **Delete** element identifies a single folder to delete in the local client store.</span></span> 
  
- [<span data-ttu-id="f533c-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="f533c-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)  
- [<span data-ttu-id="f533c-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f533c-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="f533c-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f533c-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)  
- [<span data-ttu-id="f533c-108">Änderungen (Hierarchie)</span><span class="sxs-lookup"><span data-stu-id="f533c-108">Changes (Hierarchy)</span></span>](changes-hierarchy.md)  
- [<span data-ttu-id="f533c-109">Delete (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="f533c-109">Delete (FolderSync)</span></span>](delete-foldersync.md)
  
```xml
<Delete>
   <FolderId/>
</Delete>
```

<span data-ttu-id="f533c-110">**SyncFolderHierarchyDeleteType**</span><span class="sxs-lookup"><span data-stu-id="f533c-110">**SyncFolderHierarchyDeleteType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f533c-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f533c-111">Attributes and elements</span></span>

<span data-ttu-id="f533c-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f533c-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f533c-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="f533c-113">Attributes</span></span>

<span data-ttu-id="f533c-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="f533c-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f533c-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f533c-115">Child elements</span></span>

|<span data-ttu-id="f533c-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="f533c-116">**Element**</span></span>|<span data-ttu-id="f533c-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f533c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f533c-118">FolderId</span><span class="sxs-lookup"><span data-stu-id="f533c-118">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="f533c-119">Enthält den Bezeichner und den Änderungsschlüssel eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="f533c-119">Contains the identifier and change key of a folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f533c-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f533c-120">Parent elements</span></span>

|<span data-ttu-id="f533c-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="f533c-121">**Element**</span></span>|<span data-ttu-id="f533c-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f533c-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f533c-123">Änderungen (Hierarchie)</span><span class="sxs-lookup"><span data-stu-id="f533c-123">Changes (Hierarchy)</span></span>](changes-hierarchy.md) <br/> |<span data-ttu-id="f533c-124">Enthält ein sequenziertes Array von Änderungstypen, die die Art der Unterschiede zwischen den Ordnern auf dem Client und den Ordnern auf dem Computer mit Microsoft Exchange Server 2007 darstellen.</span><span class="sxs-lookup"><span data-stu-id="f533c-124">Contains a sequenced array of change types that represent the type of differences between the folders on the client and the folders on the computer that is running Microsoft Exchange Server 2007.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f533c-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f533c-125">Remarks</span></span>

<span data-ttu-id="f533c-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Exchange 2007 Computers, auf dem die Client Zugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f533c-126">The schema that describes this element is located in the EWS virtual directory of the Exchange 2007 computer that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f533c-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f533c-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f533c-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="f533c-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f533c-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f533c-129">Schema name</span></span>  <br/> |<span data-ttu-id="f533c-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f533c-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="f533c-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f533c-131">Validation file</span></span>  <br/> |<span data-ttu-id="f533c-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f533c-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f533c-133">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f533c-133">Can be empty</span></span>  <br/> |<span data-ttu-id="f533c-134">False</span><span class="sxs-lookup"><span data-stu-id="f533c-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f533c-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f533c-135">See also</span></span>

- [<span data-ttu-id="f533c-136">SyncFolderHierarchy-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f533c-136">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)
- [<span data-ttu-id="f533c-137">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="f533c-137">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="f533c-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f533c-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

