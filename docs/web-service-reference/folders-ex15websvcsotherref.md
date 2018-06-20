---
title: Ordner
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Folders
api_type:
- schema
ms.assetid: 8e71cb44-1df6-444a-add7-0c1363863f65
description: Das Ordner-Element enthält ein Array von Ordnern, die im Ordner Vorgänge verwendet werden.
ms.openlocfilehash: e1b9e337f633dbf6fda159c28725d3fb8dcd55a6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758512"
---
# <a name="folders"></a><span data-ttu-id="93c59-103">Ordner</span><span class="sxs-lookup"><span data-stu-id="93c59-103">Folders</span></span>

<span data-ttu-id="93c59-104">Das **Ordner** -Element enthält ein Array von Ordnern, die im Ordner Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93c59-104">The **Folders** element contains an array of folders that are used in folder operations.</span></span> 
  
```xml
<Folders>
   <Folder/>
</Folders>
```

 <span data-ttu-id="93c59-105">**ArrayOfFoldersType** oder **NonEmptyArrayOfFoldersType**</span><span class="sxs-lookup"><span data-stu-id="93c59-105">**ArrayOfFoldersType** or **NonEmptyArrayOfFoldersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="93c59-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="93c59-106">Attributes and elements</span></span>

<span data-ttu-id="93c59-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="93c59-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="93c59-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="93c59-108">Attributes</span></span>

<span data-ttu-id="93c59-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="93c59-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="93c59-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="93c59-110">Child elements</span></span>

|<span data-ttu-id="93c59-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="93c59-111">**Element**</span></span>|<span data-ttu-id="93c59-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="93c59-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="93c59-113">Folder</span><span class="sxs-lookup"><span data-stu-id="93c59-113">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="93c59-114">Gibt einen Ordner erstellen, abrufen, suchen, synchronisieren oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="93c59-114">Identifies a folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="93c59-115">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="93c59-115">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="93c59-116">Stellt einen Ordner, der in erster Linie Kalenderelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="93c59-116">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="93c59-117">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="93c59-117">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="93c59-118">Stellt einen Kontakteordner in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="93c59-118">Represents a Contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="93c59-119">"SearchFolder"</span><span class="sxs-lookup"><span data-stu-id="93c59-119">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="93c59-120">Stellt einen Suchordner in einem Postfach enthalten.</span><span class="sxs-lookup"><span data-stu-id="93c59-120">Represents a Search folder contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="93c59-121">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="93c59-121">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="93c59-122">Stellt einen Aufgabenordner in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="93c59-122">Represents a Tasks folder in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="93c59-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="93c59-123">Parent elements</span></span>

|<span data-ttu-id="93c59-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="93c59-124">**Element**</span></span>|<span data-ttu-id="93c59-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="93c59-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="93c59-126">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="93c59-126">CopyFolderResponseMessage</span></span>](copyfolderresponsemessage.md) <br/> |<span data-ttu-id="93c59-127">Enthält den Status und das Ergebnis einer einzelnen Anforderung [CopyFolder-Vorgang](copyfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="93c59-127">Contains the status and result of a single [CopyFolder operation](copyfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="93c59-128">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="93c59-128">CreateFolder</span></span>](createfolder.md) <br/> |<span data-ttu-id="93c59-129">Definiert eine Anforderung an einen Ordner im Exchange-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="93c59-129">Defines a request to create a folder in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="93c59-130">CreateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="93c59-130">CreateFolderResponseMessage</span></span>](createfolderresponsemessage.md) <br/> |<span data-ttu-id="93c59-131">Enthält den Status und das Ergebnis einer einzelnen Anforderung [CreateFolder-Vorgang](createfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="93c59-131">Contains the status and result of a single [CreateFolder operation](createfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="93c59-132">CreateManagedFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="93c59-132">CreateManagedFolderResponseMessage</span></span>](createmanagedfolderresponsemessage.md) <br/> |<span data-ttu-id="93c59-133">Enthält den Status und das Ergebnis einer einzelnen Anforderung [CreateManagedFolder Vorgang](createmanagedfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="93c59-133">Contains the status and result of a single [CreateManagedFolder operation](createmanagedfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="93c59-134">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="93c59-134">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md) <br/> |<span data-ttu-id="93c59-135">Enthält den Status und das Ergebnis einer Anforderung [GetFolder-Vorgang](getfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="93c59-135">Contains the status and result of a [GetFolder operation](getfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="93c59-136">MoveFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="93c59-136">MoveFolderResponseMessage</span></span>](movefolderresponsemessage.md) <br/> |<span data-ttu-id="93c59-137">Enthält den Status und das Ergebnis einer Anforderung [MoveFolder-Vorgang](movefolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="93c59-137">Contains the status and result of a [MoveFolder operation](movefolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="93c59-138">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="93c59-138">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md) <br/> |<span data-ttu-id="93c59-139">Identifiziert den Ordner, in dem ein neuer Ordner erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="93c59-139">Identifies the folder where a new folder is created.</span></span>  <br/> |
|[<span data-ttu-id="93c59-140">RootFolder (FindFolderResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="93c59-140">RootFolder (FindFolderResponseMessage)</span></span>](rootfolder-findfolderresponsemessage.md) <br/> |<span data-ttu-id="93c59-141">Enthält die Ergebnisse einen einzelner Stammordner während eines [Vorgangs FindFolder](findfolder-operation.md)zu suchen.</span><span class="sxs-lookup"><span data-stu-id="93c59-141">Contains the results from searching a single root folder during a [FindFolder operation](findfolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="93c59-142">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="93c59-142">UpdateFolderResponseMessage</span></span>](updatefolderresponsemessage.md) <br/> |<span data-ttu-id="93c59-143">Enthält den Status und das Ergebnis einer einzelnen Anforderung [UpdateFolder Vorgang](updatefolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="93c59-143">Contains the status and result of a single [UpdateFolder operation](updatefolder-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93c59-144">Hinweise</span><span class="sxs-lookup"><span data-stu-id="93c59-144">Remarks</span></span>

<span data-ttu-id="93c59-145">Dieses Element ist ein erforderliches untergeordnetes Element des Elements [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .</span><span class="sxs-lookup"><span data-stu-id="93c59-145">This element is a required child element of the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span> 
  
<span data-ttu-id="93c59-146">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="93c59-146">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="93c59-147">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="93c59-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="93c59-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="93c59-148">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="93c59-149">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="93c59-149">Schema Name</span></span>  <br/> |<span data-ttu-id="93c59-150">Schematypen</span><span class="sxs-lookup"><span data-stu-id="93c59-150">Types schema</span></span>  <br/> |
|<span data-ttu-id="93c59-151">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="93c59-151">Validation File</span></span>  <br/> |<span data-ttu-id="93c59-152">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="93c59-152">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="93c59-153">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="93c59-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="93c59-154">False</span><span class="sxs-lookup"><span data-stu-id="93c59-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="93c59-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93c59-155">See also</span></span>



[<span data-ttu-id="93c59-156">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="93c59-156">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md)

