---
title: EmptyFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 502b2841-103d-4340-97d5-51a1db813fb2
description: Das EmptyFolder-Element definiert eine Anforderung an einen Ordner in einem Postfach im Exchange-Speicher zu leeren. Optional können Unterordner auch gelöscht werden, wenn der Ordner geleert wird.
ms.openlocfilehash: c72e11cea29e2e55c9c29754eec60e73bd1e4d9c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758211"
---
# <a name="emptyfolder"></a><span data-ttu-id="88f37-104">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="88f37-104">EmptyFolder</span></span>

<span data-ttu-id="88f37-105">Das **EmptyFolder** -Element definiert eine Anforderung an einen Ordner in einem Postfach im Exchange-Speicher zu leeren.</span><span class="sxs-lookup"><span data-stu-id="88f37-105">The **EmptyFolder** element defines a request to empty a folder in a mailbox in the Exchange store.</span></span> <span data-ttu-id="88f37-106">Optional können Unterordner auch gelöscht werden, wenn der Ordner geleert wird.</span><span class="sxs-lookup"><span data-stu-id="88f37-106">Optionally, subfolders can also be deleted when the folder is emptied.</span></span> 
  
```XML
<EmptyFolder>
   <FolderIds/>
</EmptyFolder>
```

 <span data-ttu-id="88f37-107">**EmptyFolderType**</span><span class="sxs-lookup"><span data-stu-id="88f37-107">**EmptyFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="88f37-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="88f37-108">Attributes and elements</span></span>

<span data-ttu-id="88f37-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="88f37-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="88f37-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="88f37-110">Attributes</span></span>

|<span data-ttu-id="88f37-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="88f37-111">**Attribute**</span></span>|<span data-ttu-id="88f37-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="88f37-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="88f37-113">**DeleteType**</span><span class="sxs-lookup"><span data-stu-id="88f37-113">**DeleteType**</span></span> <br/> |<span data-ttu-id="88f37-114">Gibt an, wie ein Ordner geleert wird.</span><span class="sxs-lookup"><span data-stu-id="88f37-114">Specifies how a folder is emptied.</span></span> <span data-ttu-id="88f37-115">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="88f37-115">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="88f37-116">**DeleteSubFolders**</span><span class="sxs-lookup"><span data-stu-id="88f37-116">**DeleteSubFolders**</span></span> <br/> |<span data-ttu-id="88f37-117">Gibt an, ob Unterordner gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="88f37-117">Specifies whether subfolders are to be deleted.</span></span> <span data-ttu-id="88f37-118">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="88f37-118">This attribute is required.</span></span>  <br/> |
   
#### <a name="deletetype-attribute"></a><span data-ttu-id="88f37-119">DeleteType-Attribut</span><span class="sxs-lookup"><span data-stu-id="88f37-119">DeleteType Attribute</span></span>

|<span data-ttu-id="88f37-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="88f37-120">**Value**</span></span>|<span data-ttu-id="88f37-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="88f37-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="88f37-122">HardDelete</span><span class="sxs-lookup"><span data-stu-id="88f37-122">HardDelete</span></span>  <br/> |<span data-ttu-id="88f37-123">Eine Nachrichten und Ordnern dauerhaft aus dem Speicher entfernt.</span><span class="sxs-lookup"><span data-stu-id="88f37-123">A messages and folders are permanently removed from the store.</span></span>  <br/> |
|<span data-ttu-id="88f37-124">SoftDelete</span><span class="sxs-lookup"><span data-stu-id="88f37-124">SoftDelete</span></span>  <br/> |<span data-ttu-id="88f37-125">Eine Nachrichten und Ordnern werden verschoben und die Dumpster Wenn die Dumpster ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="88f37-125">A messages and folders are moved to the dumpster if the dumpster is enabled.</span></span>  <br/> |
|<span data-ttu-id="88f37-126">MoveToDeletedItems</span><span class="sxs-lookup"><span data-stu-id="88f37-126">MoveToDeletedItems</span></span>  <br/> |<span data-ttu-id="88f37-127">Eine Nachrichten und Ordnern in den Ordner Gelöschte Objekte verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="88f37-127">A messages and folders are moved to the Deleted Items folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="88f37-128">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="88f37-128">Child elements</span></span>

|<span data-ttu-id="88f37-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="88f37-129">**Element**</span></span>|<span data-ttu-id="88f37-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="88f37-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="88f37-131">FolderIds</span><span class="sxs-lookup"><span data-stu-id="88f37-131">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="88f37-132">Enthält ein Array von Bezeichnern für Ordner, die zum Identifizieren der zu löschenden Ordner verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="88f37-132">Contains an array of folder identifiers that are used to identify folders to delete.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="88f37-133">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="88f37-133">Parent elements</span></span>

<span data-ttu-id="88f37-134">Keine.</span><span class="sxs-lookup"><span data-stu-id="88f37-134">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="88f37-135">Textwert</span><span class="sxs-lookup"><span data-stu-id="88f37-135">Text value</span></span>

<span data-ttu-id="88f37-136">Keine.</span><span class="sxs-lookup"><span data-stu-id="88f37-136">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="88f37-137">Hinweise</span><span class="sxs-lookup"><span data-stu-id="88f37-137">Remarks</span></span>

<span data-ttu-id="88f37-138">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="88f37-138">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="88f37-139">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="88f37-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88f37-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="88f37-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="88f37-141">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="88f37-141">Schema Name</span></span>  <br/> |<span data-ttu-id="88f37-142">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="88f37-142">Message schema</span></span>  <br/> |
|<span data-ttu-id="88f37-143">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="88f37-143">Validation File</span></span>  <br/> |<span data-ttu-id="88f37-144">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="88f37-144">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="88f37-145">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="88f37-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="88f37-146">False</span><span class="sxs-lookup"><span data-stu-id="88f37-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="88f37-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88f37-147">See also</span></span>



[<span data-ttu-id="88f37-148">EmptyFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="88f37-148">EmptyFolder operation</span></span>](emptyfolder-operation.md)

