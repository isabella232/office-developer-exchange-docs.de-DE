---
title: Änderungen (Hierarchie)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Changes
api_type:
- schema
ms.assetid: 918a0d1f-90a5-4eef-9592-07e15bef94e6
description: Das Changes-Element enthält ein sequenziertes Array von Änderungstypen, die die Art der Unterschiede zwischen den Ordnern auf dem Client und den Ordnern auf dem Computer mit Microsoft Exchange Server 2007 darstellen.
ms.openlocfilehash: a296d87f23e85d42b4c8c858e92eddfb586a8324
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463272"
---
# <a name="changes-hierarchy"></a><span data-ttu-id="cb6e1-103">Änderungen (Hierarchie)</span><span class="sxs-lookup"><span data-stu-id="cb6e1-103">Changes (Hierarchy)</span></span>

<span data-ttu-id="cb6e1-104">Das **Changes** -Element enthält ein sequenziertes Array von Änderungstypen, die die Art der Unterschiede zwischen den Ordnern auf dem Client und den Ordnern auf dem Computer mit Microsoft Exchange Server 2007 darstellen.</span><span class="sxs-lookup"><span data-stu-id="cb6e1-104">The **Changes** element contains a sequenced array of change types that represent the type of differences between the folders on the client and the folders on the computer that is running Microsoft Exchange Server 2007.</span></span> 
  
[<span data-ttu-id="cb6e1-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="cb6e1-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)
  
[<span data-ttu-id="cb6e1-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="cb6e1-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="cb6e1-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="cb6e1-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
  
[<span data-ttu-id="cb6e1-108">Änderungen (Hierarchie)</span><span class="sxs-lookup"><span data-stu-id="cb6e1-108">Changes (Hierarchy)</span></span>](changes-hierarchy.md)
  
```xml
<Changes>
   <Create/>
   <Update/>
   <Delete/>
</Changes>
```

 <span data-ttu-id="cb6e1-109">**SyncFolderHierarchyChangesType**</span><span class="sxs-lookup"><span data-stu-id="cb6e1-109">**SyncFolderHierarchyChangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cb6e1-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cb6e1-110">Attributes and elements</span></span>

<span data-ttu-id="cb6e1-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cb6e1-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cb6e1-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="cb6e1-112">Attributes</span></span>

<span data-ttu-id="cb6e1-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="cb6e1-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cb6e1-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cb6e1-114">Child elements</span></span>

|<span data-ttu-id="cb6e1-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="cb6e1-115">**Element**</span></span>|<span data-ttu-id="cb6e1-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cb6e1-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cb6e1-117">Erstellen (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="cb6e1-117">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="cb6e1-118">Gibt einen einzelnen Ordner an, der im lokalen Clientspeicher erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cb6e1-118">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="cb6e1-119">Update (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="cb6e1-119">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="cb6e1-120">Gibt einen einzelnen Ordner an, der im lokalen Clientspeicher aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cb6e1-120">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="cb6e1-121">Delete (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="cb6e1-121">Delete (FolderSync)</span></span>](delete-foldersync.md) <br/> |<span data-ttu-id="cb6e1-122">Identifiziert einen einzelnen Ordner, der im lokalen Clientspeicher gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="cb6e1-122">Identifies a single folder to delete in the local client store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cb6e1-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cb6e1-123">Parent elements</span></span>

|<span data-ttu-id="cb6e1-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="cb6e1-124">**Element**</span></span>|<span data-ttu-id="cb6e1-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cb6e1-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cb6e1-126">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="cb6e1-126">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md) <br/> |<span data-ttu-id="cb6e1-127">Enthält den Status und das Ergebnis einer SyncFolderHierarchy-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="cb6e1-127">Contains the status and result of a SyncFolderHierarchy request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cb6e1-128">Textwert</span><span class="sxs-lookup"><span data-stu-id="cb6e1-128">Text value</span></span>

<span data-ttu-id="cb6e1-129">Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cb6e1-129">A text value that represents a Boolean value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cb6e1-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb6e1-130">Remarks</span></span>

<span data-ttu-id="cb6e1-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Exchange 2007 Computers, auf dem die Client Zugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="cb6e1-131">The schema that describes this element is located in the EWS virtual directory of the Exchange 2007 computer that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cb6e1-132">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="cb6e1-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb6e1-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="cb6e1-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cb6e1-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cb6e1-134">Schema name</span></span>  <br/> |<span data-ttu-id="cb6e1-135">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="cb6e1-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cb6e1-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cb6e1-136">Validation file</span></span>  <br/> |<span data-ttu-id="cb6e1-137">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="cb6e1-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cb6e1-138">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="cb6e1-138">Can be empty</span></span>  <br/> |<span data-ttu-id="cb6e1-139">False</span><span class="sxs-lookup"><span data-stu-id="cb6e1-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb6e1-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb6e1-140">See also</span></span>



[<span data-ttu-id="cb6e1-141">SyncFolderHierarchy-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cb6e1-141">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)


[<span data-ttu-id="cb6e1-142">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="cb6e1-142">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
  
- [<span data-ttu-id="cb6e1-143">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="cb6e1-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

