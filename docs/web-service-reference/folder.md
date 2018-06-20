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
description: Das Folder-Element definiert einen Ordner erstellen, abrufen, suchen, synchronisieren oder zu aktualisieren.
ms.openlocfilehash: ecfea52d2105599372a22b78778ac0d0d066bc60
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758506"
---
# <a name="folder"></a><span data-ttu-id="c735c-103">Ordner</span><span class="sxs-lookup"><span data-stu-id="c735c-103">Folder</span></span>

<span data-ttu-id="c735c-104">Das **Folder** -Element definiert einen Ordner erstellen, abrufen, suchen, synchronisieren oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c735c-104">The **Folder** element defines a folder to create, get, find, synchronize, or update.</span></span> 
  
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

 <span data-ttu-id="c735c-105">**FolderType**</span><span class="sxs-lookup"><span data-stu-id="c735c-105">**FolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c735c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c735c-106">Attributes and elements</span></span>

<span data-ttu-id="c735c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c735c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c735c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c735c-108">Attributes</span></span>

<span data-ttu-id="c735c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c735c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c735c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c735c-110">Child elements</span></span>

|<span data-ttu-id="c735c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c735c-111">**Element**</span></span>|<span data-ttu-id="c735c-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c735c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c735c-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="c735c-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="c735c-114">Enthält den Schlüssel-ID und Ändern eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="c735c-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="c735c-115">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="c735c-115">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="c735c-116">Stellt den Bezeichner des übergeordneten Ordners, der den Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="c735c-116">Represents the identifier of the parent folder that contains the folder.</span></span>  <br/> |
|[<span data-ttu-id="c735c-117">FolderClass</span><span class="sxs-lookup"><span data-stu-id="c735c-117">FolderClass</span></span>](folderclass.md) <br/> |<span data-ttu-id="c735c-118">Stellt die Ordner-Klasse für einen bestimmten Ordner.</span><span class="sxs-lookup"><span data-stu-id="c735c-118">Represents the folder class for a given folder.</span></span>  <br/> |
|[<span data-ttu-id="c735c-119">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="c735c-119">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="c735c-120">Enthält den Anzeigenamen eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="c735c-120">Contains the display name of a folder.</span></span>  <br/> |
|[<span data-ttu-id="c735c-121">TotalCount</span><span class="sxs-lookup"><span data-stu-id="c735c-121">TotalCount</span></span>](totalcount.md) <br/> |<span data-ttu-id="c735c-122">Stellt die gesamte Anzahl von Elementen in einem bestimmten Ordner an.</span><span class="sxs-lookup"><span data-stu-id="c735c-122">Represents the total count of items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="c735c-123">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="c735c-123">ChildFolderCount</span></span>](childfoldercount.md) <br/> |<span data-ttu-id="c735c-124">Stellt die Anzahl der untergeordneten Ordner, die in einem Ordner enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c735c-124">Represents the number of child folders that are contained within a folder.</span></span> <span data-ttu-id="c735c-125">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c735c-125">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="c735c-126">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="c735c-126">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="c735c-127">Erweiterte Eigenschaften für Ordner identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c735c-127">Identifies extended properties on folders.</span></span>  <br/> |
|[<span data-ttu-id="c735c-128">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="c735c-128">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="c735c-129">Enthält Informationen zu einem verwalteten Ordner.</span><span class="sxs-lookup"><span data-stu-id="c735c-129">Contains information about a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="c735c-130">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="c735c-130">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="c735c-131">Die Anzahl der ungelesenen Elemente innerhalb eines bestimmten Ordners darstellt.</span><span class="sxs-lookup"><span data-stu-id="c735c-131">Represents the count of unread items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="c735c-132">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="c735c-132">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="c735c-133">Enthält die konfigurierten Berechtigungen für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="c735c-133">Contains all the configured permissions for a folder.</span></span> <span data-ttu-id="c735c-134">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c735c-134">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="c735c-135">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="c735c-135">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="c735c-136">Der Client Rechte basierend auf den berechtigungseinstellungen für das Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="c735c-136">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="c735c-137">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c735c-137">This element is read-only.</span></span> <span data-ttu-id="c735c-138">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c735c-138">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c735c-139">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c735c-139">Parent elements</span></span>

|<span data-ttu-id="c735c-140">**Element**</span><span class="sxs-lookup"><span data-stu-id="c735c-140">**Element**</span></span>|<span data-ttu-id="c735c-141">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c735c-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c735c-142">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="c735c-142">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="c735c-143">Gibt Daten an, die während einer [UpdateFolder-Vorgang](updatefolder-operation.md) an eine Ordnereigenschaft angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c735c-143">Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="c735c-144">Erstellen (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="c735c-144">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="c735c-145">Gibt einen einzelnen Ordner im lokalen Client-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c735c-145">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="c735c-146">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="c735c-146">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="c735c-147">Stellt eine Aktualisierung auf eine einzelne Eigenschaft in einem Ordner in einer [UpdateFolder-Vorgang](updatefolder-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="c735c-147">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="c735c-148">Update (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="c735c-148">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="c735c-149">Gibt einen einzelnen Ordner, in den lokalen Client-Speicher zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c735c-149">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="c735c-150">Ordner</span><span class="sxs-lookup"><span data-stu-id="c735c-150">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="c735c-151">Enthält ein Array von Ordnern, die im Ordner Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c735c-151">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c735c-152">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c735c-152">Remarks</span></span>

<span data-ttu-id="c735c-153">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Exchange 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="c735c-153">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c735c-154">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c735c-154">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c735c-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="c735c-155">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c735c-156">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c735c-156">Schema Name</span></span>  <br/> |<span data-ttu-id="c735c-157">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c735c-157">Types schema</span></span>  <br/> |
|<span data-ttu-id="c735c-158">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c735c-158">Validation File</span></span>  <br/> |<span data-ttu-id="c735c-159">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c735c-159">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c735c-160">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c735c-160">Can be Empty</span></span>  <br/> |<span data-ttu-id="c735c-161">False</span><span class="sxs-lookup"><span data-stu-id="c735c-161">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c735c-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c735c-162">See also</span></span>



[<span data-ttu-id="c735c-163">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c735c-163">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="c735c-164">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c735c-164">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

