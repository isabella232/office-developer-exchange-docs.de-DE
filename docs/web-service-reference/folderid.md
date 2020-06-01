---
title: FolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderId
api_type:
- schema
ms.assetid: 00d14e3e-4365-4f21-8f88-eaeea73b9bf7
description: Das Folder-ID-Element enthält den Bezeichner und den Änderungsschlüssel eines Ordners.
ms.openlocfilehash: 7aa5070fa7a2c51303c7159de04fe277f909a874
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461387"
---
# <a name="folderid"></a><span data-ttu-id="f7f10-103">FolderId</span><span class="sxs-lookup"><span data-stu-id="f7f10-103">FolderId</span></span>

<span data-ttu-id="f7f10-104">Das **Folder** -ID-Element enthält den Bezeichner und den Änderungsschlüssel eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="f7f10-104">The **FolderId** element contains the identifier and change key of a folder.</span></span> 
  
```XML
<FolderId Id="" ChangeKey="" />
```

 <span data-ttu-id="f7f10-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="f7f10-105">**FolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f7f10-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f7f10-106">Attributes and elements</span></span>

<span data-ttu-id="f7f10-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f7f10-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f7f10-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f7f10-108">Attributes</span></span>

|<span data-ttu-id="f7f10-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f7f10-109">**Attribute**</span></span>|<span data-ttu-id="f7f10-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f7f10-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f7f10-111">Id</span><span class="sxs-lookup"><span data-stu-id="f7f10-111">Id</span></span>  <br/> |<span data-ttu-id="f7f10-112">Enthält eine Zeichenfolge, die einen Ordner im Exchange-Informationsspeicher identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f7f10-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="f7f10-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f7f10-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="f7f10-114">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="f7f10-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="f7f10-115">Enthält eine Zeichenfolge, die eine Version eines Ordners identifiziert, die durch das ID-Attribut identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="f7f10-115">Contains a string that identifies a version of a folder that is identified by the Id attribute.</span></span> <span data-ttu-id="f7f10-116">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="f7f10-116">This attribute is optional.</span></span> <span data-ttu-id="f7f10-117">Verwenden Sie dieses Attribut, um sicherzustellen, dass die richtige Version eines Ordners verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f7f10-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f7f10-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f7f10-118">Child elements</span></span>

<span data-ttu-id="f7f10-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="f7f10-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f7f10-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f7f10-120">Parent elements</span></span>

|<span data-ttu-id="f7f10-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="f7f10-121">**Element**</span></span>|<span data-ttu-id="f7f10-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f7f10-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f7f10-123">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="f7f10-123">ContextFolderId</span></span>](contextfolderid.md) <br/> |<span data-ttu-id="f7f10-124">Gibt den Ordner an, der für Aktionen vorgesehen ist, die Ordner verwenden.</span><span class="sxs-lookup"><span data-stu-id="f7f10-124">Indicates the folder that is targeted for actions that use folders.</span></span>  <br/> |
|[<span data-ttu-id="f7f10-125">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="f7f10-125">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="f7f10-126">Stellt ein Ereignis dar, in dem ein Element oder ein Ordner kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="f7f10-126">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="f7f10-127">DestinationFolderId</span><span class="sxs-lookup"><span data-stu-id="f7f10-127">DestinationFolderId</span></span>](destinationfolderid.md) <br/> |<span data-ttu-id="f7f10-128">Gibt den Zielordner für die Aktionen kopieren und verlegen an.</span><span class="sxs-lookup"><span data-stu-id="f7f10-128">Indicates the destination folder for copy and move actions.</span></span>  <br/> |
|[<span data-ttu-id="f7f10-129">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="f7f10-129">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md) <br/> | <span data-ttu-id="f7f10-130">Gibt den Ordner an, in dem ein neuer Ordner oder Element erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f7f10-130">Identifies the folder where a new folder or item is created.</span></span>  <br/><br/>  <span data-ttu-id="f7f10-131">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="f7f10-131">The following are the XPath expressions to this element:</span></span><br/>  <br/> `/CreateItem/ParentFolderId` <br/><br/>  `/CreateFolder/ParentFolderId` <br/> |
|[<span data-ttu-id="f7f10-132">BaseFolderIds</span><span class="sxs-lookup"><span data-stu-id="f7f10-132">BaseFolderIds</span></span>](basefolderids.md) <br/> |<span data-ttu-id="f7f10-133">Stellt die Auflistung von Ordnern dar, die abgebaut werden, um den Inhalt eines Suchordners zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="f7f10-133">Represents the collection of folders that will be mined to determine the contents of a search folder.</span></span>  <br/> |
|[<span data-ttu-id="f7f10-134">Delete (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="f7f10-134">Delete (FolderSync)</span></span>](delete-foldersync.md) <br/> |<span data-ttu-id="f7f10-135">Identifiziert einen einzelnen Ordner, der im lokalen Clientspeicher gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="f7f10-135">Identifies a single folder to delete in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="f7f10-136">Folder</span><span class="sxs-lookup"><span data-stu-id="f7f10-136">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="f7f10-137">Stellt einen Ordner in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="f7f10-137">Represents a folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="f7f10-138">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="f7f10-138">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="f7f10-139">Stellt einen Kalenderordner in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="f7f10-139">Represents a calendar folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="f7f10-140">FolderChange</span><span class="sxs-lookup"><span data-stu-id="f7f10-140">FolderChange</span></span>](folderchange.md) <br/> |<span data-ttu-id="f7f10-141">Stellt eine Auflistung von Änderungen dar, die für einen einzelnen Ordner ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f7f10-141">Represents a collection of changes to be performed on a single folder.</span></span>  <br/> <span data-ttu-id="f7f10-142">Im folgenden finden Sie den XPath-Ausdruck für dieses Element:`/UpdateFolder/FolderChanges/FolderChange`</span><span class="sxs-lookup"><span data-stu-id="f7f10-142">The following is the XPath expression to this element:  `/UpdateFolder/FolderChanges/FolderChange`</span></span> <br/> |
|[<span data-ttu-id="f7f10-143">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="f7f10-143">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="f7f10-144">Stellt einen Kontaktordner in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="f7f10-144">Represents a contact folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="f7f10-145">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="f7f10-145">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="f7f10-146">Stellt einen Suchordner in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="f7f10-146">Represents a search folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="f7f10-147">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="f7f10-147">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="f7f10-148">Stellt einen Aufgabenordner in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="f7f10-148">Represents a task folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="f7f10-149">Tofolder-Datei</span><span class="sxs-lookup"><span data-stu-id="f7f10-149">ToFolderId</span></span>](tofolderid.md) <br/> | <span data-ttu-id="f7f10-150">Stellt den Zielordner für ein kopiertes oder verschobenes Element oder einen verschobenen Ordner dar.</span><span class="sxs-lookup"><span data-stu-id="f7f10-150">Represents the destination folder for a copied or moved item or folder.</span></span> <br/> <br/>  <span data-ttu-id="f7f10-151">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="f7f10-151">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/MoveFolder/ToFolderId` <br/> <br/> `/CopyFolder/ToFolderId` <br/> <br/> `/MoveItem/ToFolderId`<br/> <br/>  `/CopyItem/ToFolderId` <br/> |
|[<span data-ttu-id="f7f10-152">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="f7f10-152">SavedItemFolderId</span></span>](saveditemfolderid.md) <br/> | <span data-ttu-id="f7f10-153">Identifiziert den Zielordner für Vorgänge, die Elemente im Exchange-Informationsspeicher aktualisieren, senden und erstellen.</span><span class="sxs-lookup"><span data-stu-id="f7f10-153">Identifies the target folder for operations that update, send, and create items in the Exchange store.</span></span>  <br/><br/>  <span data-ttu-id="f7f10-154">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="f7f10-154">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/CreateItem/SavedItemFolderId` <br/><br/>  `/UpdateItem/SavedItemFolderId` <br/><br/>  `/SendItem/SavedItemFolderId` <br/> |
|[<span data-ttu-id="f7f10-155">SyncFolderId</span><span class="sxs-lookup"><span data-stu-id="f7f10-155">SyncFolderId</span></span>](syncfolderid.md) <br/> |<span data-ttu-id="f7f10-156">Stellt den Ordner dar, der die zu synchronisierenden Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="f7f10-156">Represents the folder that contains the items to synchronize.</span></span>  <br/> |
|[<span data-ttu-id="f7f10-157">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f7f10-157">UserConfigurationName</span></span>](userconfigurationname.md) <br/> |<span data-ttu-id="f7f10-158">Stellt den Namen eines Benutzer Konfigurationsobjekts dar.</span><span class="sxs-lookup"><span data-stu-id="f7f10-158">Represents the name of a user configuration object.</span></span> <span data-ttu-id="f7f10-159">Der Benutzer Konfigurationsobjekt Name ist der Bezeichner für ein Benutzer Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="f7f10-159">The user configuration object name is the identifier for a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="f7f10-160">CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="f7f10-160">CopyToFolder</span></span>](copytofolder.md) <br/> |<span data-ttu-id="f7f10-161">Gibt die ID des Ordners an, in den e-Mail-Elemente kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="f7f10-161">Identifies the ID of the folder that e-mail items will be copied to.</span></span>  <br/> |
|[<span data-ttu-id="f7f10-162">MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="f7f10-162">MoveToFolder</span></span>](movetofolder.md) <br/> |<span data-ttu-id="f7f10-163">Gibt die ID des Ordners an, in den e-Mail-Elemente verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="f7f10-163">Identifies the ID of the folder that e-mail items will be moved to.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f7f10-164">Textwert</span><span class="sxs-lookup"><span data-stu-id="f7f10-164">Text value</span></span>

<span data-ttu-id="f7f10-165">Keine.</span><span class="sxs-lookup"><span data-stu-id="f7f10-165">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f7f10-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7f10-166">Remarks</span></span>

<span data-ttu-id="f7f10-167">Alle **folderl** -Elemente haben den **FolderIdType** -Typ.</span><span class="sxs-lookup"><span data-stu-id="f7f10-167">All **FolderId** elements are of the **FolderIdType** type.</span></span> <span data-ttu-id="f7f10-168">Das **folderl** -Element ist in jedem Fall erforderlich, außer in Elementen, deren Typ das **BaseFolderType** -Element erweitert oder in dem das **Folder** -Element ein Teil einer Auswahl ist.</span><span class="sxs-lookup"><span data-stu-id="f7f10-168">The **FolderId** element is required in every case except in elements whose type extends the **BaseFolderType** or where the **FolderId** element is a part of a choice.</span></span> <span data-ttu-id="f7f10-169">Lesen Sie das Schema, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f7f10-169">Review the schema for more information.</span></span> 
  
<span data-ttu-id="f7f10-170">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f7f10-170">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f7f10-171">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f7f10-171">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f7f10-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="f7f10-172">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f7f10-173">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f7f10-173">Schema Name</span></span>  <br/> |<span data-ttu-id="f7f10-174">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f7f10-174">Types schema</span></span>  <br/> |
|<span data-ttu-id="f7f10-175">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f7f10-175">Validation File</span></span>  <br/> |<span data-ttu-id="f7f10-176">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f7f10-176">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f7f10-177">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f7f10-177">Can be Empty</span></span>  <br/> |<span data-ttu-id="f7f10-178">False</span><span class="sxs-lookup"><span data-stu-id="f7f10-178">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f7f10-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7f10-179">See also</span></span>

- [<span data-ttu-id="f7f10-180">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f7f10-180">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="f7f10-181">Erstellen von Ordnern (Exchange Webdienste)</span><span class="sxs-lookup"><span data-stu-id="f7f10-181">Creating Folders (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

