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
ms.openlocfilehash: 34372f2480825c7a9977eeae8e730c201307f36b
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353588"
---
# <a name="folders"></a><span data-ttu-id="d73ae-103">Ordner</span><span class="sxs-lookup"><span data-stu-id="d73ae-103">Folders</span></span>

<span data-ttu-id="d73ae-104">Das **Ordner** -Element enthält ein Array von Ordnern, die im Ordner Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d73ae-104">The **Folders** element contains an array of folders that are used in folder operations.</span></span> 
  
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

<span data-ttu-id="d73ae-105">**ArrayOfFoldersType** oder **NonEmptyArrayOfFoldersType**</span><span class="sxs-lookup"><span data-stu-id="d73ae-105">**ArrayOfFoldersType** or **NonEmptyArrayOfFoldersType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d73ae-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d73ae-106">Attributes and elements</span></span>

<span data-ttu-id="d73ae-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d73ae-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d73ae-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d73ae-108">Attributes</span></span>

<span data-ttu-id="d73ae-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d73ae-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d73ae-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d73ae-110">Child elements</span></span>

|<span data-ttu-id="d73ae-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d73ae-111">**Element**</span></span>|<span data-ttu-id="d73ae-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d73ae-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d73ae-113">Folder</span><span class="sxs-lookup"><span data-stu-id="d73ae-113">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="d73ae-114">Gibt einen Ordner erstellen, abrufen, suchen, synchronisieren oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d73ae-114">Identifies a folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="d73ae-115">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="d73ae-115">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="d73ae-116">Stellt einen Ordner, der in erster Linie Kalenderelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="d73ae-116">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="d73ae-117">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="d73ae-117">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="d73ae-118">Stellt einen Kontakteordner in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="d73ae-118">Represents a Contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d73ae-119">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="d73ae-119">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="d73ae-120">Stellt einen Suchordner in einem Postfach enthalten.</span><span class="sxs-lookup"><span data-stu-id="d73ae-120">Represents a Search folder contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d73ae-121">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="d73ae-121">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="d73ae-122">Stellt einen Aufgabenordner in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="d73ae-122">Represents a Tasks folder in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d73ae-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d73ae-123">Parent elements</span></span>

|<span data-ttu-id="d73ae-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="d73ae-124">**Element**</span></span>|<span data-ttu-id="d73ae-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d73ae-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d73ae-126">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d73ae-126">CopyFolderResponseMessage</span></span>](copyfolderresponsemessage.md) <br/> |<span data-ttu-id="d73ae-127">Enthält den Status und das Ergebnis einer einzelnen Anforderung [CopyFolder-Vorgang](copyfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="d73ae-127">Contains the status and result of a single [CopyFolder operation](copyfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="d73ae-128">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="d73ae-128">CreateFolder</span></span>](createfolder.md) <br/> |<span data-ttu-id="d73ae-129">Definiert eine Anforderung an einen Ordner im Exchange-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d73ae-129">Defines a request to create a folder in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d73ae-130">CreateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d73ae-130">CreateFolderResponseMessage</span></span>](createfolderresponsemessage.md) <br/> |<span data-ttu-id="d73ae-131">Enthält den Status und das Ergebnis einer einzelnen Anforderung [CreateFolder-Vorgang](createfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="d73ae-131">Contains the status and result of a single [CreateFolder operation](createfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="d73ae-132">CreateManagedFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d73ae-132">CreateManagedFolderResponseMessage</span></span>](createmanagedfolderresponsemessage.md) <br/> |<span data-ttu-id="d73ae-133">Enthält den Status und das Ergebnis einer einzelnen Anforderung [CreateManagedFolder Vorgang](createmanagedfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="d73ae-133">Contains the status and result of a single [CreateManagedFolder operation](createmanagedfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="d73ae-134">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d73ae-134">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md) <br/> |<span data-ttu-id="d73ae-135">Enthält den Status und das Ergebnis einer Anforderung [GetFolder-Vorgang](getfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="d73ae-135">Contains the status and result of a [GetFolder operation](getfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="d73ae-136">MoveFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d73ae-136">MoveFolderResponseMessage</span></span>](movefolderresponsemessage.md) <br/> |<span data-ttu-id="d73ae-137">Enthält den Status und das Ergebnis einer Anforderung [MoveFolder-Vorgang](movefolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="d73ae-137">Contains the status and result of a [MoveFolder operation](movefolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="d73ae-138">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="d73ae-138">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md) <br/> |<span data-ttu-id="d73ae-139">Identifiziert den Ordner, in dem ein neuer Ordner erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d73ae-139">Identifies the folder where a new folder is created.</span></span>  <br/> |
|[<span data-ttu-id="d73ae-140">RootFolder (FindFolderResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="d73ae-140">RootFolder (FindFolderResponseMessage)</span></span>](rootfolder-findfolderresponsemessage.md) <br/> |<span data-ttu-id="d73ae-141">Enthält die Ergebnisse einen einzelner Stammordner während eines [Vorgangs FindFolder](findfolder-operation.md)zu suchen.</span><span class="sxs-lookup"><span data-stu-id="d73ae-141">Contains the results from searching a single root folder during a [FindFolder operation](findfolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="d73ae-142">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d73ae-142">UpdateFolderResponseMessage</span></span>](updatefolderresponsemessage.md) <br/> |<span data-ttu-id="d73ae-143">Enthält den Status und das Ergebnis einer einzelnen Anforderung [UpdateFolder Vorgang](updatefolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="d73ae-143">Contains the status and result of a single [UpdateFolder operation](updatefolder-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d73ae-144">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d73ae-144">Remarks</span></span>

<span data-ttu-id="d73ae-145">Dieses Element ist ein erforderliches untergeordnetes Element des Elements [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .</span><span class="sxs-lookup"><span data-stu-id="d73ae-145">This element is a required child element of the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span> 
  
<span data-ttu-id="d73ae-146">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d73ae-146">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d73ae-147">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d73ae-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d73ae-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="d73ae-148">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d73ae-149">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d73ae-149">Schema Name</span></span>  <br/> |<span data-ttu-id="d73ae-150">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d73ae-150">Types schema</span></span>  <br/> |
|<span data-ttu-id="d73ae-151">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d73ae-151">Validation File</span></span>  <br/> |<span data-ttu-id="d73ae-152">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d73ae-152">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d73ae-153">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d73ae-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="d73ae-154">False</span><span class="sxs-lookup"><span data-stu-id="d73ae-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d73ae-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d73ae-155">See also</span></span>

- [<span data-ttu-id="d73ae-156">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="d73ae-156">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md)

