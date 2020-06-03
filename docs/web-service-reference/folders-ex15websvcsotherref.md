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
description: Das Folders-Element enthält ein Array von Ordnern, die in Ordnervorgängen verwendet werden.
ms.openlocfilehash: b087be0501f04390b80458458e7e7ccc24bf27bd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530979"
---
# <a name="folders"></a><span data-ttu-id="d2ab6-103">Ordner</span><span class="sxs-lookup"><span data-stu-id="d2ab6-103">Folders</span></span>

<span data-ttu-id="d2ab6-104">Das **Folders** -Element enthält ein Array von Ordnern, die in Ordnervorgängen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d2ab6-104">The **Folders** element contains an array of folders that are used in folder operations.</span></span> 
  
```xml
<Folders>
   <Folder/>
</Folders>
```

```xml
<Folders>
   <ContactsFolder/> 
</Folders>
```

```xml
<Folders>
   <TasksFolder/>
</Folders>
```

```xml
<Folders>
   <CalendarFolder/>
</Folders>
```

```xml
<Folders>
   <SearchFolder/> 
</Folders>
```

<span data-ttu-id="d2ab6-105">**ArrayOfFoldersType** oder **NonEmptyArrayOfFoldersType**</span><span class="sxs-lookup"><span data-stu-id="d2ab6-105">**ArrayOfFoldersType** or **NonEmptyArrayOfFoldersType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d2ab6-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d2ab6-106">Attributes and elements</span></span>

<span data-ttu-id="d2ab6-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d2ab6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d2ab6-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d2ab6-108">Attributes</span></span>

<span data-ttu-id="d2ab6-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d2ab6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d2ab6-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d2ab6-110">Child elements</span></span>

|<span data-ttu-id="d2ab6-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d2ab6-111">**Element**</span></span>|<span data-ttu-id="d2ab6-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d2ab6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d2ab6-113">Folder</span><span class="sxs-lookup"><span data-stu-id="d2ab6-113">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="d2ab6-114">Gibt einen Ordner zum Erstellen, abrufen, suchen, synchronisieren oder aktualisieren an.</span><span class="sxs-lookup"><span data-stu-id="d2ab6-114">Identifies a folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="d2ab6-115">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="d2ab6-115">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="d2ab6-116">Stellt einen Ordner dar, der in erster Linie Kalenderelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="d2ab6-116">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="d2ab6-117">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="d2ab6-117">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="d2ab6-118">Stellt einen Ordner Kontakte in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="d2ab6-118">Represents a Contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d2ab6-119">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="d2ab6-119">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="d2ab6-120">Stellt einen in einem Postfach enthaltenen Suchordner dar.</span><span class="sxs-lookup"><span data-stu-id="d2ab6-120">Represents a Search folder contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d2ab6-121">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="d2ab6-121">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="d2ab6-122">Stellt einen Aufgabenordner in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="d2ab6-122">Represents a Tasks folder in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d2ab6-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d2ab6-123">Parent elements</span></span>

|<span data-ttu-id="d2ab6-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="d2ab6-124">**Element**</span></span>|<span data-ttu-id="d2ab6-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d2ab6-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d2ab6-126">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d2ab6-126">CopyFolderResponseMessage</span></span>](copyfolderresponsemessage.md) <br/> |<span data-ttu-id="d2ab6-127">Enthält den Status und das Ergebnis einer einzelnen [CopyFolder-Vorgangs](copyfolder-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d2ab6-127">Contains the status and result of a single [CopyFolder operation](copyfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="d2ab6-128">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="d2ab6-128">CreateFolder</span></span>](createfolder.md) <br/> |<span data-ttu-id="d2ab6-129">Definiert eine Anforderung zum Erstellen eines Ordners im Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="d2ab6-129">Defines a request to create a folder in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d2ab6-130">CreateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d2ab6-130">CreateFolderResponseMessage</span></span>](createfolderresponsemessage.md) <br/> |<span data-ttu-id="d2ab6-131">Enthält den Status und das Ergebnis einer einzelnen [CreateFolder-Vorgangs](createfolder-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d2ab6-131">Contains the status and result of a single [CreateFolder operation](createfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="d2ab6-132">CreateManagedFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d2ab6-132">CreateManagedFolderResponseMessage</span></span>](createmanagedfolderresponsemessage.md) <br/> |<span data-ttu-id="d2ab6-133">Enthält den Status und das Ergebnis einer einzelnen [CreateManagedFolder-Vorgangs](createmanagedfolder-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d2ab6-133">Contains the status and result of a single [CreateManagedFolder operation](createmanagedfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="d2ab6-134">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d2ab6-134">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md) <br/> |<span data-ttu-id="d2ab6-135">Enthält den Status und das Ergebnis einer [GetFolder-Vorgangs](getfolder-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d2ab6-135">Contains the status and result of a [GetFolder operation](getfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="d2ab6-136">MoveFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d2ab6-136">MoveFolderResponseMessage</span></span>](movefolderresponsemessage.md) <br/> |<span data-ttu-id="d2ab6-137">Enthält den Status und das Ergebnis einer [MoveFolder-Vorgangs](movefolder-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d2ab6-137">Contains the status and result of a [MoveFolder operation](movefolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="d2ab6-138">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="d2ab6-138">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md) <br/> |<span data-ttu-id="d2ab6-139">Gibt den Ordner an, in dem ein neuer Ordner erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d2ab6-139">Identifies the folder where a new folder is created.</span></span>  <br/> |
|[<span data-ttu-id="d2ab6-140">RootFolder (FindFolderResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="d2ab6-140">RootFolder (FindFolderResponseMessage)</span></span>](rootfolder-findfolderresponsemessage.md) <br/> |<span data-ttu-id="d2ab6-141">Enthält die Ergebnisse der Suche eines einzelnen Stammordners während eines [FindFolder-Vorgangs](findfolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="d2ab6-141">Contains the results from searching a single root folder during a [FindFolder operation](findfolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="d2ab6-142">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d2ab6-142">UpdateFolderResponseMessage</span></span>](updatefolderresponsemessage.md) <br/> |<span data-ttu-id="d2ab6-143">Enthält den Status und das Ergebnis einer einzelnen [UpdateFolder-Vorgangs](updatefolder-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d2ab6-143">Contains the status and result of a single [UpdateFolder operation](updatefolder-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2ab6-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2ab6-144">Remarks</span></span>

<span data-ttu-id="d2ab6-145">Dieses Element ist ein erforderliches untergeordnetes Element des [parentfolderid-Elements (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .</span><span class="sxs-lookup"><span data-stu-id="d2ab6-145">This element is a required child element of the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span> 
  
<span data-ttu-id="d2ab6-146">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d2ab6-146">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d2ab6-147">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d2ab6-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d2ab6-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="d2ab6-148">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d2ab6-149">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d2ab6-149">Schema Name</span></span>  <br/> |<span data-ttu-id="d2ab6-150">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d2ab6-150">Types schema</span></span>  <br/> |
|<span data-ttu-id="d2ab6-151">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d2ab6-151">Validation File</span></span>  <br/> |<span data-ttu-id="d2ab6-152">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d2ab6-152">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d2ab6-153">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d2ab6-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="d2ab6-154">False</span><span class="sxs-lookup"><span data-stu-id="d2ab6-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d2ab6-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2ab6-155">See also</span></span>

- [<span data-ttu-id="d2ab6-156">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="d2ab6-156">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md)

