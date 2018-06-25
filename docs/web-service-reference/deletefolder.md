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
description: Das DeleteFolder-Element definiert eine Anforderung zum Löschen von Ordnern aus einem Postfach im Exchange-Speicher.
ms.openlocfilehash: d31f98f26f537104e40b303de4199f45c65f49c7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757920"
---
# <a name="deletefolder"></a><span data-ttu-id="a6c4c-103">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="a6c4c-103">DeleteFolder</span></span>

<span data-ttu-id="a6c4c-104">Das **DeleteFolder** -Element definiert eine Anforderung zum Löschen von Ordnern aus einem Postfach im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="a6c4c-104">The **DeleteFolder** element defines a request to delete folders from a mailbox in the Exchange store.</span></span> 
  
```XML
<DeleteFolder DeleteType="">
   <FolderIds/>
</DeleteFolder>
```

 <span data-ttu-id="a6c4c-105">**DeleteFolderType**</span><span class="sxs-lookup"><span data-stu-id="a6c4c-105">**DeleteFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a6c4c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a6c4c-106">Attributes and elements</span></span>

<span data-ttu-id="a6c4c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a6c4c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a6c4c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a6c4c-108">Attributes</span></span>

|<span data-ttu-id="a6c4c-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a6c4c-109">**Attribute**</span></span>|<span data-ttu-id="a6c4c-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a6c4c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a6c4c-111">**DeleteType**</span><span class="sxs-lookup"><span data-stu-id="a6c4c-111">**DeleteType**</span></span> <br/> |<span data-ttu-id="a6c4c-112">Beschreibt, wie ein Ordner gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="a6c4c-112">Describes how a folder is deleted.</span></span> <span data-ttu-id="a6c4c-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a6c4c-113">This attribute is required.</span></span>  <br/> |
   
#### <a name="deletetype-attribute"></a><span data-ttu-id="a6c4c-114">DeleteType-Attribut</span><span class="sxs-lookup"><span data-stu-id="a6c4c-114">DeleteType attribute</span></span>

|<span data-ttu-id="a6c4c-115">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a6c4c-115">**Value**</span></span>|<span data-ttu-id="a6c4c-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a6c4c-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a6c4c-117">HardDelete</span><span class="sxs-lookup"><span data-stu-id="a6c4c-117">HardDelete</span></span>  <br/> |<span data-ttu-id="a6c4c-118">Ein Ordner wird dauerhaft aus dem Speicher entfernt.</span><span class="sxs-lookup"><span data-stu-id="a6c4c-118">A folder is permanently removed from the store.</span></span>  <br/> |
|<span data-ttu-id="a6c4c-119">SoftDelete</span><span class="sxs-lookup"><span data-stu-id="a6c4c-119">SoftDelete</span></span>  <br/> |<span data-ttu-id="a6c4c-120">In ein Ordner verschoben die Dumpster Wenn die Dumpster ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a6c4c-120">A folder is moved to the dumpster if the dumpster is enabled.</span></span>  <br/> |
|<span data-ttu-id="a6c4c-121">MoveToDeletedItems</span><span class="sxs-lookup"><span data-stu-id="a6c4c-121">MoveToDeletedItems</span></span>  <br/> |<span data-ttu-id="a6c4c-122">Ein Ordner wird in den Ordner Gelöschte Objekte verschoben.</span><span class="sxs-lookup"><span data-stu-id="a6c4c-122">A folder is moved to the Deleted Items folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a6c4c-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a6c4c-123">Child elements</span></span>

|<span data-ttu-id="a6c4c-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="a6c4c-124">**Element**</span></span>|<span data-ttu-id="a6c4c-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a6c4c-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a6c4c-126">FolderIds</span><span class="sxs-lookup"><span data-stu-id="a6c4c-126">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="a6c4c-127">Enthält ein Array von Bezeichnern für Ordner, die zum Identifizieren der zu löschenden Ordner verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a6c4c-127">Contains an array of folder identifiers that are used to identify folders to delete.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a6c4c-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a6c4c-128">Parent elements</span></span>

<span data-ttu-id="a6c4c-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="a6c4c-129">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="a6c4c-130">Textwert</span><span class="sxs-lookup"><span data-stu-id="a6c4c-130">Text value</span></span>

<span data-ttu-id="a6c4c-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="a6c4c-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a6c4c-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a6c4c-132">Remarks</span></span>

<span data-ttu-id="a6c4c-133">Die Optionen **MoveToDeletedItems** und **HardDelete** sind transaktional, was bedeutet, dass jeweils ein Webdienstaufruf abgeschlossen ist, die Datenbank hat das Element in den Ordner Gelöschte Objekte verschoben oder dauerhaft entfernt das Element aus der Exchange-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="a6c4c-133">The **MoveToDeletedItems** and **HardDelete** options are transactional, which means that by the time a Web service call completes, the database has moved the item to the Deleted Items folder or permanently removed the item from the Exchange database.</span></span> <span data-ttu-id="a6c4c-134">Dieses Verhalten gilt für MicrosoftExchange Server 2007 und Exchange Server 2010.</span><span class="sxs-lookup"><span data-stu-id="a6c4c-134">This behavior is the same for MicrosoftExchange Server 2007 and Exchange Server 2010.</span></span> 
  
<span data-ttu-id="a6c4c-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a6c4c-135">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a6c4c-136">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a6c4c-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a6c4c-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="a6c4c-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a6c4c-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a6c4c-138">Schema Name</span></span>  <br/> |<span data-ttu-id="a6c4c-139">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="a6c4c-139">Message schema</span></span>  <br/> |
|<span data-ttu-id="a6c4c-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a6c4c-140">Validation File</span></span>  <br/> |<span data-ttu-id="a6c4c-141">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a6c4c-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a6c4c-142">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a6c4c-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="a6c4c-143">False</span><span class="sxs-lookup"><span data-stu-id="a6c4c-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a6c4c-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6c4c-144">See also</span></span>

- [<span data-ttu-id="a6c4c-145">DeleteFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a6c4c-145">DeleteFolder operation</span></span>](deletefolder-operation.md)

