---
title: Ordner
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Folder
api_type:
- schema
ms.assetid: 812948d8-c7db-45ce-bb3a-77233a53a974
description: Das Folder-Element definiert einen Ordner zum Erstellen, abrufen, suchen, synchronisieren oder aktualisieren.
ms.openlocfilehash: 156813b3f7ecc6a2e1437f473ae1daa76b138e6e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457249"
---
# <a name="folder"></a><span data-ttu-id="1aec4-103">Ordner</span><span class="sxs-lookup"><span data-stu-id="1aec4-103">Folder</span></span>

<span data-ttu-id="1aec4-104">Das **Folder** -Element definiert einen Ordner zum Erstellen, abrufen, suchen, synchronisieren oder aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1aec4-104">The **Folder** element defines a folder to create, get, find, synchronize, or update.</span></span> 
  
```xml
<Folder>
   <FolderId/>
   <ParentFolderId/>
   <FolderClass/>
   <DisplayName/>
   <TotalCount/>
   <ChildFolderCount/>
   <ExtendedProperty/>
   <ManagedFolderInformation/>
   <UnreadCount/>
   <PermissionSet/>
   <EffectiveRights/>
</Folder>
```

 <span data-ttu-id="1aec4-105">**FolderType**</span><span class="sxs-lookup"><span data-stu-id="1aec4-105">**FolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1aec4-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1aec4-106">Attributes and elements</span></span>

<span data-ttu-id="1aec4-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1aec4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1aec4-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1aec4-108">Attributes</span></span>

<span data-ttu-id="1aec4-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1aec4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1aec4-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1aec4-110">Child elements</span></span>

|<span data-ttu-id="1aec4-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1aec4-111">**Element**</span></span>|<span data-ttu-id="1aec4-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1aec4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1aec4-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="1aec4-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="1aec4-114">Enthält den Bezeichner und den Änderungsschlüssel eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="1aec4-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="1aec4-115">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="1aec4-115">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="1aec4-116">Stellt den Bezeichner des übergeordneten Ordners dar, der den Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="1aec4-116">Represents the identifier of the parent folder that contains the folder.</span></span>  <br/> |
|[<span data-ttu-id="1aec4-117">FolderClass</span><span class="sxs-lookup"><span data-stu-id="1aec4-117">FolderClass</span></span>](folderclass.md) <br/> |<span data-ttu-id="1aec4-118">Stellt die Folder-Klasse für einen bestimmten Ordner dar.</span><span class="sxs-lookup"><span data-stu-id="1aec4-118">Represents the folder class for a given folder.</span></span>  <br/> |
|[<span data-ttu-id="1aec4-119">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="1aec4-119">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="1aec4-120">Enthält den Anzeigenamen eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="1aec4-120">Contains the display name of a folder.</span></span>  <br/> |
|[<span data-ttu-id="1aec4-121">Total count</span><span class="sxs-lookup"><span data-stu-id="1aec4-121">TotalCount</span></span>](totalcount.md) <br/> |<span data-ttu-id="1aec4-122">Stellt die Gesamtanzahl der Elemente in einem bestimmten Ordner dar.</span><span class="sxs-lookup"><span data-stu-id="1aec4-122">Represents the total count of items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="1aec4-123">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="1aec4-123">ChildFolderCount</span></span>](childfoldercount.md) <br/> |<span data-ttu-id="1aec4-124">Stellt die Anzahl der untergeordneten Ordner dar, die in einem Ordner enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="1aec4-124">Represents the number of child folders that are contained within a folder.</span></span> <span data-ttu-id="1aec4-125">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1aec4-125">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="1aec4-126">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="1aec4-126">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="1aec4-127">Identifiziert erweiterte Eigenschaften für Ordner.</span><span class="sxs-lookup"><span data-stu-id="1aec4-127">Identifies extended properties on folders.</span></span>  <br/> |
|[<span data-ttu-id="1aec4-128">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="1aec4-128">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="1aec4-129">Enthält Informationen zu einem verwalteten Ordner.</span><span class="sxs-lookup"><span data-stu-id="1aec4-129">Contains information about a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="1aec4-130">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="1aec4-130">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="1aec4-131">Stellt die Anzahl der ungelesenen Elemente in einem bestimmten Ordner dar.</span><span class="sxs-lookup"><span data-stu-id="1aec4-131">Represents the count of unread items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="1aec4-132">PermissionSet (permissionsettype)</span><span class="sxs-lookup"><span data-stu-id="1aec4-132">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="1aec4-133">Enthält alle konfigurierten Berechtigungen für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="1aec4-133">Contains all the configured permissions for a folder.</span></span> <span data-ttu-id="1aec4-134">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1aec4-134">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="1aec4-135">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="1aec4-135">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="1aec4-136">Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner.</span><span class="sxs-lookup"><span data-stu-id="1aec4-136">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="1aec4-137">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1aec4-137">This element is read-only.</span></span> <span data-ttu-id="1aec4-138">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1aec4-138">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1aec4-139">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1aec4-139">Parent elements</span></span>

|<span data-ttu-id="1aec4-140">**Element**</span><span class="sxs-lookup"><span data-stu-id="1aec4-140">**Element**</span></span>|<span data-ttu-id="1aec4-141">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1aec4-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1aec4-142">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="1aec4-142">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="1aec4-143">Gibt Daten an, die während einer [UpdateFolder-Vorgang](updatefolder-operation.md) an eine Ordnereigenschaft angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1aec4-143">Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="1aec4-144">Erstellen (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="1aec4-144">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="1aec4-145">Gibt einen einzelnen Ordner an, der im lokalen Clientspeicher erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1aec4-145">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="1aec4-146">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="1aec4-146">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="1aec4-147">Stellt eine Aktualisierung auf eine einzelne Eigenschaft in einem Ordner in einer [UpdateFolder-Vorgang](updatefolder-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="1aec4-147">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="1aec4-148">Update (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="1aec4-148">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="1aec4-149">Gibt einen einzelnen Ordner an, der im lokalen Clientspeicher aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1aec4-149">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="1aec4-150">Ordner</span><span class="sxs-lookup"><span data-stu-id="1aec4-150">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="1aec4-151">Enthält ein Array von Ordnern, die in Ordnervorgängen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1aec4-151">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1aec4-152">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1aec4-152">Remarks</span></span>

<span data-ttu-id="1aec4-153">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange 2007 ausgeführt wird, auf dem die Client Zugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1aec4-153">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1aec4-154">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1aec4-154">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1aec4-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="1aec4-155">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1aec4-156">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1aec4-156">Schema Name</span></span>  <br/> |<span data-ttu-id="1aec4-157">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1aec4-157">Types schema</span></span>  <br/> |
|<span data-ttu-id="1aec4-158">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1aec4-158">Validation File</span></span>  <br/> |<span data-ttu-id="1aec4-159">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1aec4-159">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1aec4-160">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1aec4-160">Can be Empty</span></span>  <br/> |<span data-ttu-id="1aec4-161">False</span><span class="sxs-lookup"><span data-stu-id="1aec4-161">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1aec4-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1aec4-162">See also</span></span>



[<span data-ttu-id="1aec4-163">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1aec4-163">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="1aec4-164">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1aec4-164">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

