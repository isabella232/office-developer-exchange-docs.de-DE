---
title: DeleteFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteFolder
api_type:
- schema
ms.assetid: e37963f4-af9e-4481-b389-16175711e66d
description: Das DeleteFolder-Element definiert eine Anforderung zum Löschen von Ordnern aus einem Postfach im Exchange-Informationsspeicher.
ms.openlocfilehash: eb705a47b78b19c79b2e87561ba3696ed40e09cd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458768"
---
# <a name="deletefolder"></a><span data-ttu-id="12fb0-103">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="12fb0-103">DeleteFolder</span></span>

<span data-ttu-id="12fb0-104">Das **DeleteFolder** -Element definiert eine Anforderung zum Löschen von Ordnern aus einem Postfach im Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="12fb0-104">The **DeleteFolder** element defines a request to delete folders from a mailbox in the Exchange store.</span></span> 
  
```XML
<DeleteFolder DeleteType="">
   <FolderIds/>
</DeleteFolder>
```

 <span data-ttu-id="12fb0-105">**DeleteFolderType**</span><span class="sxs-lookup"><span data-stu-id="12fb0-105">**DeleteFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="12fb0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="12fb0-106">Attributes and elements</span></span>

<span data-ttu-id="12fb0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="12fb0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="12fb0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="12fb0-108">Attributes</span></span>

|<span data-ttu-id="12fb0-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="12fb0-109">**Attribute**</span></span>|<span data-ttu-id="12fb0-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="12fb0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="12fb0-111">**Deletetypeharddelete**</span><span class="sxs-lookup"><span data-stu-id="12fb0-111">**DeleteType**</span></span> <br/> |<span data-ttu-id="12fb0-112">Beschreibt, wie ein Ordner gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="12fb0-112">Describes how a folder is deleted.</span></span> <span data-ttu-id="12fb0-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="12fb0-113">This attribute is required.</span></span>  <br/> |
   
#### <a name="deletetype-attribute"></a><span data-ttu-id="12fb0-114">DeleteType-Attribut</span><span class="sxs-lookup"><span data-stu-id="12fb0-114">DeleteType attribute</span></span>

|<span data-ttu-id="12fb0-115">**Wert**</span><span class="sxs-lookup"><span data-stu-id="12fb0-115">**Value**</span></span>|<span data-ttu-id="12fb0-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="12fb0-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="12fb0-117">HardDelete</span><span class="sxs-lookup"><span data-stu-id="12fb0-117">HardDelete</span></span>  <br/> |<span data-ttu-id="12fb0-118">Ein Ordner wird dauerhaft aus dem Speicher entfernt.</span><span class="sxs-lookup"><span data-stu-id="12fb0-118">A folder is permanently removed from the store.</span></span>  <br/> |
|<span data-ttu-id="12fb0-119">SoftDelete</span><span class="sxs-lookup"><span data-stu-id="12fb0-119">SoftDelete</span></span>  <br/> |<span data-ttu-id="12fb0-120">Wenn der Papierkorb aktiviert ist, wird ein Ordner in den Papierkorb verschoben.</span><span class="sxs-lookup"><span data-stu-id="12fb0-120">A folder is moved to the dumpster if the dumpster is enabled.</span></span>  <br/> |
|<span data-ttu-id="12fb0-121">MoveToDeletedItems</span><span class="sxs-lookup"><span data-stu-id="12fb0-121">MoveToDeletedItems</span></span>  <br/> |<span data-ttu-id="12fb0-122">Ein Ordner wird in den Ordner "Gelöschte Elemente" verschoben.</span><span class="sxs-lookup"><span data-stu-id="12fb0-122">A folder is moved to the Deleted Items folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="12fb0-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="12fb0-123">Child elements</span></span>

|<span data-ttu-id="12fb0-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="12fb0-124">**Element**</span></span>|<span data-ttu-id="12fb0-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="12fb0-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="12fb0-126">FolderIds</span><span class="sxs-lookup"><span data-stu-id="12fb0-126">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="12fb0-127">Enthält ein Array von Ordner Bezeichnern, die zum Identifizieren von zu löschenden Ordnern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12fb0-127">Contains an array of folder identifiers that are used to identify folders to delete.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="12fb0-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="12fb0-128">Parent elements</span></span>

<span data-ttu-id="12fb0-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="12fb0-129">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="12fb0-130">Textwert</span><span class="sxs-lookup"><span data-stu-id="12fb0-130">Text value</span></span>

<span data-ttu-id="12fb0-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="12fb0-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="12fb0-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12fb0-132">Remarks</span></span>

<span data-ttu-id="12fb0-133">Die **MoveToDeletedItems** -und **HardDelete** -Optionen sind transaktional, was bedeutet, dass die Datenbank zum Zeitpunkt des Abschlusses eines Webdienstaufrufs das Element in den Ordner "Gelöschte Elemente" verschoben oder das Element endgültig aus der Exchange-Datenbank entfernt hat.</span><span class="sxs-lookup"><span data-stu-id="12fb0-133">The **MoveToDeletedItems** and **HardDelete** options are transactional, which means that by the time a Web service call completes, the database has moved the item to the Deleted Items folder or permanently removed the item from the Exchange database.</span></span> <span data-ttu-id="12fb0-134">Dieses Verhalten ist für Microsoft Exchange Server 2007 und Exchange Server 2010 identisch.</span><span class="sxs-lookup"><span data-stu-id="12fb0-134">This behavior is the same for MicrosoftExchange Server 2007 and Exchange Server 2010.</span></span> 
  
<span data-ttu-id="12fb0-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="12fb0-135">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="12fb0-136">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="12fb0-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="12fb0-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="12fb0-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="12fb0-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="12fb0-138">Schema Name</span></span>  <br/> |<span data-ttu-id="12fb0-139">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="12fb0-139">Message schema</span></span>  <br/> |
|<span data-ttu-id="12fb0-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="12fb0-140">Validation File</span></span>  <br/> |<span data-ttu-id="12fb0-141">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="12fb0-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="12fb0-142">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="12fb0-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="12fb0-143">False</span><span class="sxs-lookup"><span data-stu-id="12fb0-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="12fb0-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12fb0-144">See also</span></span>

- [<span data-ttu-id="12fb0-145">DeleteFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="12fb0-145">DeleteFolder operation</span></span>](deletefolder-operation.md)

