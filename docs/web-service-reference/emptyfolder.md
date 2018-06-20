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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758211"
---
# <a name="emptyfolder"></a><span data-ttu-id="f0b0b-104">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="f0b0b-104">EmptyFolder</span></span>

<span data-ttu-id="f0b0b-105">Das **EmptyFolder** -Element definiert eine Anforderung an einen Ordner in einem Postfach im Exchange-Speicher zu leeren.</span><span class="sxs-lookup"><span data-stu-id="f0b0b-105">The **EmptyFolder** element defines a request to empty a folder in a mailbox in the Exchange store.</span></span> <span data-ttu-id="f0b0b-106">Optional können Unterordner auch gelöscht werden, wenn der Ordner geleert wird.</span><span class="sxs-lookup"><span data-stu-id="f0b0b-106">Optionally, subfolders can also be deleted when the folder is emptied.</span></span> 
  
```XML
<EmptyFolder>
   <FolderIds/>
</EmptyFolder>
```

 <span data-ttu-id="f0b0b-107">**EmptyFolderType**</span><span class="sxs-lookup"><span data-stu-id="f0b0b-107">**EmptyFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f0b0b-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f0b0b-108">Attributes and elements</span></span>

<span data-ttu-id="f0b0b-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f0b0b-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f0b0b-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="f0b0b-110">Attributes</span></span>

|<span data-ttu-id="f0b0b-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f0b0b-111">**Attribute**</span></span>|<span data-ttu-id="f0b0b-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f0b0b-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f0b0b-113">**DeleteType**</span><span class="sxs-lookup"><span data-stu-id="f0b0b-113">**DeleteType**</span></span> <br/> |<span data-ttu-id="f0b0b-114">Gibt an, wie ein Ordner geleert wird.</span><span class="sxs-lookup"><span data-stu-id="f0b0b-114">Specifies how a folder is emptied.</span></span> <span data-ttu-id="f0b0b-115">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f0b0b-115">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="f0b0b-116">**DeleteSubFolders**</span><span class="sxs-lookup"><span data-stu-id="f0b0b-116">**DeleteSubFolders**</span></span> <br/> |<span data-ttu-id="f0b0b-117">Gibt an, ob Unterordner gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="f0b0b-117">Specifies whether subfolders are to be deleted.</span></span> <span data-ttu-id="f0b0b-118">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f0b0b-118">This attribute is required.</span></span>  <br/> |
   
#### <a name="deletetype-attribute"></a><span data-ttu-id="f0b0b-119">DeleteType-Attribut</span><span class="sxs-lookup"><span data-stu-id="f0b0b-119">DeleteType Attribute</span></span>

|<span data-ttu-id="f0b0b-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="f0b0b-120">**Value**</span></span>|<span data-ttu-id="f0b0b-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f0b0b-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f0b0b-122">HardDelete</span><span class="sxs-lookup"><span data-stu-id="f0b0b-122">HardDelete</span></span>  <br/> |<span data-ttu-id="f0b0b-123">Eine Nachrichten und Ordnern dauerhaft aus dem Speicher entfernt.</span><span class="sxs-lookup"><span data-stu-id="f0b0b-123">A messages and folders are permanently removed from the store.</span></span>  <br/> |
|<span data-ttu-id="f0b0b-124">SoftDelete</span><span class="sxs-lookup"><span data-stu-id="f0b0b-124">SoftDelete</span></span>  <br/> |<span data-ttu-id="f0b0b-125">Eine Nachrichten und Ordnern werden verschoben und die Dumpster Wenn die Dumpster ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f0b0b-125">A messages and folders are moved to the dumpster if the dumpster is enabled.</span></span>  <br/> |
|<span data-ttu-id="f0b0b-126">MoveToDeletedItems</span><span class="sxs-lookup"><span data-stu-id="f0b0b-126">MoveToDeletedItems</span></span>  <br/> |<span data-ttu-id="f0b0b-127">Eine Nachrichten und Ordnern in den Ordner Gelöschte Objekte verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="f0b0b-127">A messages and folders are moved to the Deleted Items folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f0b0b-128">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f0b0b-128">Child elements</span></span>

|<span data-ttu-id="f0b0b-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="f0b0b-129">**Element**</span></span>|<span data-ttu-id="f0b0b-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f0b0b-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f0b0b-131">FolderIds</span><span class="sxs-lookup"><span data-stu-id="f0b0b-131">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="f0b0b-132">Enthält ein Array von Bezeichnern für Ordner, die zum Identifizieren der zu löschenden Ordner verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f0b0b-132">Contains an array of folder identifiers that are used to identify folders to delete.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f0b0b-133">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f0b0b-133">Parent elements</span></span>

<span data-ttu-id="f0b0b-134">Keine.</span><span class="sxs-lookup"><span data-stu-id="f0b0b-134">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="f0b0b-135">Textwert</span><span class="sxs-lookup"><span data-stu-id="f0b0b-135">Text value</span></span>

<span data-ttu-id="f0b0b-136">Keine.</span><span class="sxs-lookup"><span data-stu-id="f0b0b-136">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f0b0b-137">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f0b0b-137">Remarks</span></span>

<span data-ttu-id="f0b0b-138">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f0b0b-138">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f0b0b-139">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f0b0b-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f0b0b-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="f0b0b-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f0b0b-141">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f0b0b-141">Schema Name</span></span>  <br/> |<span data-ttu-id="f0b0b-142">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="f0b0b-142">Message schema</span></span>  <br/> |
|<span data-ttu-id="f0b0b-143">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f0b0b-143">Validation File</span></span>  <br/> |<span data-ttu-id="f0b0b-144">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f0b0b-144">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f0b0b-145">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f0b0b-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="f0b0b-146">False</span><span class="sxs-lookup"><span data-stu-id="f0b0b-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f0b0b-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0b0b-147">See also</span></span>



[<span data-ttu-id="f0b0b-148">EmptyFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f0b0b-148">EmptyFolder operation</span></span>](emptyfolder-operation.md)

