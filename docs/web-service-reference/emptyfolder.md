---
title: EmptyFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 502b2841-103d-4340-97d5-51a1db813fb2
description: Das EmptyFolder-Element definiert eine Anforderung zum leeren eines Ordners in einem Postfach im Exchange-Informationsspeicher. Optional können Unterordner auch gelöscht werden, wenn der Ordner geleert wird.
ms.openlocfilehash: a42e4e3f25741a96ee65fe6f87fc3236b68f4dc9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457277"
---
# <a name="emptyfolder"></a><span data-ttu-id="e8ced-104">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="e8ced-104">EmptyFolder</span></span>

<span data-ttu-id="e8ced-105">Das **EmptyFolder** -Element definiert eine Anforderung zum leeren eines Ordners in einem Postfach im Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="e8ced-105">The **EmptyFolder** element defines a request to empty a folder in a mailbox in the Exchange store.</span></span> <span data-ttu-id="e8ced-106">Optional können Unterordner auch gelöscht werden, wenn der Ordner geleert wird.</span><span class="sxs-lookup"><span data-stu-id="e8ced-106">Optionally, subfolders can also be deleted when the folder is emptied.</span></span> 
  
```XML
<EmptyFolder>
   <FolderIds/>
</EmptyFolder>
```

 <span data-ttu-id="e8ced-107">**EmptyFolderType**</span><span class="sxs-lookup"><span data-stu-id="e8ced-107">**EmptyFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e8ced-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e8ced-108">Attributes and elements</span></span>

<span data-ttu-id="e8ced-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e8ced-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e8ced-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="e8ced-110">Attributes</span></span>

|<span data-ttu-id="e8ced-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e8ced-111">**Attribute**</span></span>|<span data-ttu-id="e8ced-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e8ced-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e8ced-113">**Deletetypeharddelete**</span><span class="sxs-lookup"><span data-stu-id="e8ced-113">**DeleteType**</span></span> <br/> |<span data-ttu-id="e8ced-114">Gibt an, wie ein Ordner geleert wird.</span><span class="sxs-lookup"><span data-stu-id="e8ced-114">Specifies how a folder is emptied.</span></span> <span data-ttu-id="e8ced-115">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e8ced-115">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="e8ced-116">**DeleteSubFolders**</span><span class="sxs-lookup"><span data-stu-id="e8ced-116">**DeleteSubFolders**</span></span> <br/> |<span data-ttu-id="e8ced-117">Gibt an, ob Unterordner gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e8ced-117">Specifies whether subfolders are to be deleted.</span></span> <span data-ttu-id="e8ced-118">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e8ced-118">This attribute is required.</span></span>  <br/> |
   
#### <a name="deletetype-attribute"></a><span data-ttu-id="e8ced-119">DeleteType-Attribut</span><span class="sxs-lookup"><span data-stu-id="e8ced-119">DeleteType Attribute</span></span>

|<span data-ttu-id="e8ced-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e8ced-120">**Value**</span></span>|<span data-ttu-id="e8ced-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e8ced-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e8ced-122">HardDelete</span><span class="sxs-lookup"><span data-stu-id="e8ced-122">HardDelete</span></span>  <br/> |<span data-ttu-id="e8ced-123">Nachrichten und Ordner werden endgültig aus dem Speicher entfernt.</span><span class="sxs-lookup"><span data-stu-id="e8ced-123">A messages and folders are permanently removed from the store.</span></span>  <br/> |
|<span data-ttu-id="e8ced-124">SoftDelete</span><span class="sxs-lookup"><span data-stu-id="e8ced-124">SoftDelete</span></span>  <br/> |<span data-ttu-id="e8ced-125">Wenn der Papierkorb aktiviert ist, werden Nachrichten und Ordner in den Papierkorb verschoben.</span><span class="sxs-lookup"><span data-stu-id="e8ced-125">A messages and folders are moved to the dumpster if the dumpster is enabled.</span></span>  <br/> |
|<span data-ttu-id="e8ced-126">MoveToDeletedItems</span><span class="sxs-lookup"><span data-stu-id="e8ced-126">MoveToDeletedItems</span></span>  <br/> |<span data-ttu-id="e8ced-127">Nachrichten und Ordner werden in den Ordner "Gelöschte Elemente" verschoben.</span><span class="sxs-lookup"><span data-stu-id="e8ced-127">A messages and folders are moved to the Deleted Items folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e8ced-128">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e8ced-128">Child elements</span></span>

|<span data-ttu-id="e8ced-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="e8ced-129">**Element**</span></span>|<span data-ttu-id="e8ced-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e8ced-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8ced-131">FolderIds</span><span class="sxs-lookup"><span data-stu-id="e8ced-131">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="e8ced-132">Enthält ein Array von Ordner Bezeichnern, die zum Identifizieren von zu löschenden Ordnern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e8ced-132">Contains an array of folder identifiers that are used to identify folders to delete.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e8ced-133">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e8ced-133">Parent elements</span></span>

<span data-ttu-id="e8ced-134">Keine.</span><span class="sxs-lookup"><span data-stu-id="e8ced-134">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="e8ced-135">Textwert</span><span class="sxs-lookup"><span data-stu-id="e8ced-135">Text value</span></span>

<span data-ttu-id="e8ced-136">Keine.</span><span class="sxs-lookup"><span data-stu-id="e8ced-136">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e8ced-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8ced-137">Remarks</span></span>

<span data-ttu-id="e8ced-138">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="e8ced-138">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e8ced-139">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e8ced-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e8ced-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="e8ced-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e8ced-141">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e8ced-141">Schema Name</span></span>  <br/> |<span data-ttu-id="e8ced-142">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="e8ced-142">Message schema</span></span>  <br/> |
|<span data-ttu-id="e8ced-143">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e8ced-143">Validation File</span></span>  <br/> |<span data-ttu-id="e8ced-144">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="e8ced-144">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e8ced-145">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e8ced-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="e8ced-146">False</span><span class="sxs-lookup"><span data-stu-id="e8ced-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e8ced-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8ced-147">See also</span></span>



[<span data-ttu-id="e8ced-148">EmptyFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e8ced-148">EmptyFolder operation</span></span>](emptyfolder-operation.md)

