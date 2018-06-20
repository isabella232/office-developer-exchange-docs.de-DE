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
description: Das Änderungen-Element enthält eine sequenzierten Array von Änderungstypen, die den Typ der Unterschiede zwischen den Ordnern auf dem Client und die Ordner auf dem Computer mit Microsoft Exchange Server 2007 darstellen.
ms.openlocfilehash: 15e4f9f37c5e4a4083260dcf379a49beb2260030
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757565"
---
# <a name="changes-hierarchy"></a><span data-ttu-id="ccad7-103">Änderungen (Hierarchie)</span><span class="sxs-lookup"><span data-stu-id="ccad7-103">Changes (Hierarchy)</span></span>

<span data-ttu-id="ccad7-104">Das **Änderungen** -Element enthält eine sequenzierten Array von Änderungstypen, die den Typ der Unterschiede zwischen den Ordnern auf dem Client und die Ordner auf dem Computer mit Microsoft Exchange Server 2007 darstellen.</span><span class="sxs-lookup"><span data-stu-id="ccad7-104">The **Changes** element contains a sequenced array of change types that represent the type of differences between the folders on the client and the folders on the computer that is running Microsoft Exchange Server 2007.</span></span> 
  
[<span data-ttu-id="ccad7-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="ccad7-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)
  
[<span data-ttu-id="ccad7-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ccad7-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="ccad7-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ccad7-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
  
[<span data-ttu-id="ccad7-108">Änderungen (Hierarchie)</span><span class="sxs-lookup"><span data-stu-id="ccad7-108">Changes (Hierarchy)</span></span>](changes-hierarchy.md)
  
```xml
<Changes>
   <Create/>
   <Update/>
   <Delete/>
</Changes>
```

 <span data-ttu-id="ccad7-109">**SyncFolderHierarchyChangesType**</span><span class="sxs-lookup"><span data-stu-id="ccad7-109">**SyncFolderHierarchyChangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ccad7-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ccad7-110">Attributes and elements</span></span>

<span data-ttu-id="ccad7-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ccad7-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ccad7-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="ccad7-112">Attributes</span></span>

<span data-ttu-id="ccad7-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="ccad7-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ccad7-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ccad7-114">Child elements</span></span>

|<span data-ttu-id="ccad7-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="ccad7-115">**Element**</span></span>|<span data-ttu-id="ccad7-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ccad7-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ccad7-117">Erstellen (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="ccad7-117">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="ccad7-118">Gibt einen einzelnen Ordner im lokalen Client-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ccad7-118">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="ccad7-119">Update (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="ccad7-119">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="ccad7-120">Gibt einen einzelnen Ordner, in den lokalen Client-Speicher zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ccad7-120">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="ccad7-121">Delete (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="ccad7-121">Delete (FolderSync)</span></span>](delete-foldersync.md) <br/> |<span data-ttu-id="ccad7-122">Gibt einen einzelnen Ordner im lokalen Client-Speicher zu löschen.</span><span class="sxs-lookup"><span data-stu-id="ccad7-122">Identifies a single folder to delete in the local client store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ccad7-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ccad7-123">Parent elements</span></span>

|<span data-ttu-id="ccad7-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="ccad7-124">**Element**</span></span>|<span data-ttu-id="ccad7-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ccad7-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ccad7-126">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ccad7-126">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md) <br/> |<span data-ttu-id="ccad7-127">Enthält den Status und das Ergebnis einer Anforderung SyncFolderHierarchy.</span><span class="sxs-lookup"><span data-stu-id="ccad7-127">Contains the status and result of a SyncFolderHierarchy request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ccad7-128">Textwert</span><span class="sxs-lookup"><span data-stu-id="ccad7-128">Text value</span></span>

<span data-ttu-id="ccad7-129">Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ccad7-129">A text value that represents a Boolean value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ccad7-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ccad7-130">Remarks</span></span>

<span data-ttu-id="ccad7-131">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Exchange 2007-Computers, der die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ccad7-131">The schema that describes this element is located in the EWS virtual directory of the Exchange 2007 computer that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ccad7-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ccad7-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ccad7-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="ccad7-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ccad7-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ccad7-134">Schema name</span></span>  <br/> |<span data-ttu-id="ccad7-135">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ccad7-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ccad7-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ccad7-136">Validation file</span></span>  <br/> |<span data-ttu-id="ccad7-137">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ccad7-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ccad7-138">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ccad7-138">Can be empty</span></span>  <br/> |<span data-ttu-id="ccad7-139">False</span><span class="sxs-lookup"><span data-stu-id="ccad7-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ccad7-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ccad7-140">See also</span></span>



[<span data-ttu-id="ccad7-141">SyncFolderHierarchy-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ccad7-141">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)


[<span data-ttu-id="ccad7-142">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="ccad7-142">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
  
- [<span data-ttu-id="ccad7-143">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ccad7-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

