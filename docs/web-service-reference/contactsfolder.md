---
title: ContactsFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContactsFolder
api_type:
- schema
ms.assetid: 6c299de8-2087-4aeb-8e66-2bc7586509a6
description: Das ContactsFolder-Element stellt einen Kontakteordner, der in einem Postfach enthalten ist.
ms.openlocfilehash: 01302f00d84cfff9713e3b188b7799c537fc0629
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757623"
---
# <a name="contactsfolder"></a><span data-ttu-id="1287c-103">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="1287c-103">ContactsFolder</span></span>

<span data-ttu-id="1287c-104">Das **ContactsFolder** -Element stellt einen Kontakteordner, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="1287c-104">The **ContactsFolder** element represents a contacts folder that is contained in a mailbox.</span></span> 
  
```xml
<ContactsFolder>
   <FolderId/>
   <ParentFolderId/>
   <FolderClass/>
   <DisplayName/>
   <TotalCount/>
   <ChildFolderCount/>
   <ExtendedProperty/>
   <ManagedFolderInformation/>
   <EffectiveRights/>
   <SharingEffectiveRights/>
   <PermissionSet/>
</ContactsFolder>
```

 <span data-ttu-id="1287c-105">**ContactsFolderType**</span><span class="sxs-lookup"><span data-stu-id="1287c-105">**ContactsFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1287c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1287c-106">Attributes and elements</span></span>

<span data-ttu-id="1287c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1287c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1287c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1287c-108">Attributes</span></span>

<span data-ttu-id="1287c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1287c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1287c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1287c-110">Child elements</span></span>

|<span data-ttu-id="1287c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1287c-111">**Element**</span></span>|<span data-ttu-id="1287c-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1287c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1287c-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="1287c-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="1287c-114">Enthält den Schlüssel-ID und Ändern eines Ordners Kontakte.</span><span class="sxs-lookup"><span data-stu-id="1287c-114">Contains the identifier and change key of a contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="1287c-115">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="1287c-115">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="1287c-116">Stellt den Bezeichner des übergeordneten Ordners, das den Kontakteordner enthält.</span><span class="sxs-lookup"><span data-stu-id="1287c-116">Represents the identifier of the parent folder that contains the contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="1287c-117">FolderClass</span><span class="sxs-lookup"><span data-stu-id="1287c-117">FolderClass</span></span>](folderclass.md) <br/> |<span data-ttu-id="1287c-118">Stellt die Ordner-Klasse für einen Kontakteordner dar.</span><span class="sxs-lookup"><span data-stu-id="1287c-118">Represents the folder class for a contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="1287c-119">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="1287c-119">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="1287c-120">Enthält den Anzeigenamen eines Ordners Kontakte.</span><span class="sxs-lookup"><span data-stu-id="1287c-120">Contains the display name of a contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="1287c-121">TotalCount</span><span class="sxs-lookup"><span data-stu-id="1287c-121">TotalCount</span></span>](totalcount.md) <br/> |<span data-ttu-id="1287c-122">Stellt die gesamte Anzahl von Elementen in einem Kontakteordner dar.</span><span class="sxs-lookup"><span data-stu-id="1287c-122">Represents the total count of items within a contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="1287c-123">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="1287c-123">ChildFolderCount</span></span>](childfoldercount.md) <br/> |<span data-ttu-id="1287c-124">Stellt die Anzahl der untergeordneten Ordner, die in einem Kontakteordner enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="1287c-124">Represents the number of child folders that are contained within a contacts folder.</span></span> <span data-ttu-id="1287c-125">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1287c-125">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="1287c-126">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="1287c-126">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="1287c-127">Erweiterte Eigenschaften für den Kontakteordner identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1287c-127">Identifies extended properties on contacts folders.</span></span>  <br/> |
|[<span data-ttu-id="1287c-128">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="1287c-128">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="1287c-129">Enthält Informationen zu einem verwalteten Ordner.</span><span class="sxs-lookup"><span data-stu-id="1287c-129">Contains information about a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="1287c-130">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="1287c-130">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="1287c-131">Der Client Rechte basierend auf den berechtigungseinstellungen für das Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="1287c-131">Contains the client's rights based on the permission settings for the item or folder.</span></span>  <br/> |
|[<span data-ttu-id="1287c-132">SharingEffectiveRights (PermissionReadAccessType)</span><span class="sxs-lookup"><span data-stu-id="1287c-132">SharingEffectiveRights (PermissionReadAccessType)</span></span>](sharingeffectiverights-permissionreadaccesstype.md) <br/> |<span data-ttu-id="1287c-133">Gibt an, die Berechtigungen, die der Benutzer für die Kontaktdaten aufweist, die gemeinsam genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="1287c-133">Indicates the permissions that the user has for the contact data that is being shared.</span></span>  <br/> |
|[<span data-ttu-id="1287c-134">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="1287c-134">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="1287c-135">Enthält die konfigurierten Berechtigungen für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="1287c-135">Contains all the configured permissions for a folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1287c-136">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1287c-136">Parent elements</span></span>

|<span data-ttu-id="1287c-137">**Element**</span><span class="sxs-lookup"><span data-stu-id="1287c-137">**Element**</span></span>|<span data-ttu-id="1287c-138">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1287c-138">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1287c-139">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="1287c-139">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="1287c-140">Gibt Daten an, die während einer [UpdateFolder-Vorgang](updatefolder-operation.md) an eine Ordnereigenschaft angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1287c-140">Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="1287c-141">Erstellen (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="1287c-141">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="1287c-142">Gibt einen einzelnen Ordner im lokalen Client-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1287c-142">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="1287c-143">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="1287c-143">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="1287c-144">Stellt eine Aktualisierung auf eine einzelne Eigenschaft in einem Ordner in einer [UpdateFolder-Vorgang](updatefolder-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="1287c-144">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="1287c-145">Update (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="1287c-145">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="1287c-146">Gibt einen einzelnen Ordner, in den lokalen Client-Speicher zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1287c-146">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="1287c-147">Ordner</span><span class="sxs-lookup"><span data-stu-id="1287c-147">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="1287c-148">Enthält ein Array von Ordnern, die im Ordner Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1287c-148">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1287c-149">Textwert</span><span class="sxs-lookup"><span data-stu-id="1287c-149">Text value</span></span>

<span data-ttu-id="1287c-150">Keine.</span><span class="sxs-lookup"><span data-stu-id="1287c-150">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1287c-151">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1287c-151">Remarks</span></span>

<span data-ttu-id="1287c-152">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1287c-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1287c-153">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1287c-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1287c-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="1287c-154">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1287c-155">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1287c-155">Schema Name</span></span>  <br/> |<span data-ttu-id="1287c-156">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1287c-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="1287c-157">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1287c-157">Validation File</span></span>  <br/> |<span data-ttu-id="1287c-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1287c-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1287c-159">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1287c-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="1287c-160">False</span><span class="sxs-lookup"><span data-stu-id="1287c-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1287c-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1287c-161">See also</span></span>



- [<span data-ttu-id="1287c-162">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1287c-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

