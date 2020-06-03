---
title: CalendarFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarFolder
api_type:
- schema
ms.assetid: 48687a78-e757-4c04-9641-bf4302c6b565
description: Das CalendarFolder-Element stellt einen Ordner dar, der in erster Linie Kalenderelemente enthält.
ms.openlocfilehash: dcd0ab9d7dea1152766997de0618b3dcceed5567
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461492"
---
# <a name="calendarfolder"></a><span data-ttu-id="3ca5b-103">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="3ca5b-103">CalendarFolder</span></span>

<span data-ttu-id="3ca5b-104">Das **CalendarFolder** -Element stellt einen Ordner dar, der in erster Linie Kalenderelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-104">The **CalendarFolder** element represents a folder that primarily contains calendar items.</span></span> 
  
```xml
<CalendarFolder>
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
</CalendarFolder>
```

 <span data-ttu-id="3ca5b-105">**CalendarFolderType**</span><span class="sxs-lookup"><span data-stu-id="3ca5b-105">**CalendarFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3ca5b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3ca5b-106">Attributes and elements</span></span>

<span data-ttu-id="3ca5b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3ca5b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3ca5b-108">Attributes</span></span>

<span data-ttu-id="3ca5b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3ca5b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3ca5b-110">Child elements</span></span>

|<span data-ttu-id="3ca5b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3ca5b-111">**Element**</span></span>|<span data-ttu-id="3ca5b-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3ca5b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3ca5b-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="3ca5b-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="3ca5b-114">Enthält den Bezeichner und den Änderungsschlüssel eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="3ca5b-115">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="3ca5b-115">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="3ca5b-116">Stellt den Bezeichner des übergeordneten Ordners dar, der den Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-116">Represents the identifier of the parent folder that contains the folder.</span></span>  <br/> |
|[<span data-ttu-id="3ca5b-117">FolderClass</span><span class="sxs-lookup"><span data-stu-id="3ca5b-117">FolderClass</span></span>](folderclass.md) <br/> |<span data-ttu-id="3ca5b-118">Stellt die Folder-Klasse für einen bestimmten Ordner dar.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-118">Represents the folder class for a given folder.</span></span>  <br/> |
|[<span data-ttu-id="3ca5b-119">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="3ca5b-119">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="3ca5b-120">Enthält den Anzeigenamen eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-120">Contains the display name of a folder.</span></span>  <br/> |
|[<span data-ttu-id="3ca5b-121">Total count</span><span class="sxs-lookup"><span data-stu-id="3ca5b-121">TotalCount</span></span>](totalcount.md) <br/> |<span data-ttu-id="3ca5b-122">Stellt die Gesamtanzahl der Elemente in einem bestimmten Ordner dar.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-122">Represents the total count of items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="3ca5b-123">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="3ca5b-123">ChildFolderCount</span></span>](childfoldercount.md) <br/> |<span data-ttu-id="3ca5b-124">Stellt die Anzahl der untergeordneten Ordner dar, die in einem Ordner enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-124">Represents the number of child folders that are contained within a folder.</span></span> <span data-ttu-id="3ca5b-125">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-125">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="3ca5b-126">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="3ca5b-126">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="3ca5b-127">Identifiziert erweiterte Eigenschaften für Ordner.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-127">Identifies extended properties on folders.</span></span>  <br/> |
|[<span data-ttu-id="3ca5b-128">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="3ca5b-128">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="3ca5b-129">Enthält Informationen zu einem verwalteten Ordner.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-129">Contains information about a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="3ca5b-130">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="3ca5b-130">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="3ca5b-131">Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-131">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="3ca5b-132">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-132">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="3ca5b-133">SharingEffectiveRights (CalendarPermissionReadAccessType)</span><span class="sxs-lookup"><span data-stu-id="3ca5b-133">SharingEffectiveRights (CalendarPermissionReadAccessType)</span></span>](sharingeffectiverights-calendarpermissionreadaccesstype.md) <br/> |<span data-ttu-id="3ca5b-134">Gibt die Berechtigungen an, die der Benutzer für die Kalenderdaten verwendet, die freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-134">Indicates the permissions that the user has for the calendar data that is being shared.</span></span>  <br/> |
|[<span data-ttu-id="3ca5b-135">PermissionSet (CalendarPermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="3ca5b-135">PermissionSet (CalendarPermissionSetType)</span></span>](permissionset-calendarpermissionsettype.md) <br/> |<span data-ttu-id="3ca5b-136">Enthält alle konfigurierten Berechtigungen für einen Kalenderordner.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-136">Contains all the configured permissions for a calendar folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3ca5b-137">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3ca5b-137">Parent elements</span></span>

|<span data-ttu-id="3ca5b-138">**Element**</span><span class="sxs-lookup"><span data-stu-id="3ca5b-138">**Element**</span></span>|<span data-ttu-id="3ca5b-139">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3ca5b-139">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3ca5b-140">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="3ca5b-140">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="3ca5b-141">Gibt Daten an, die während einer [UpdateFolder-Vorgang](updatefolder-operation.md) an eine Ordnereigenschaft angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-141">Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="3ca5b-142">Erstellen (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="3ca5b-142">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="3ca5b-143">Gibt einen einzelnen Ordner an, der im lokalen Clientspeicher erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-143">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="3ca5b-144">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="3ca5b-144">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="3ca5b-145">Stellt eine Aktualisierung auf eine einzelne Eigenschaft in einem Ordner in einer [UpdateFolder-Vorgang](updatefolder-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-145">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="3ca5b-146">Update (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="3ca5b-146">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="3ca5b-147">Gibt einen einzelnen Ordner an, der im lokalen Clientspeicher aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-147">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="3ca5b-148">Ordner</span><span class="sxs-lookup"><span data-stu-id="3ca5b-148">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="3ca5b-149">Enthält ein Array von Ordnern, die in Ordnervorgängen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-149">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3ca5b-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ca5b-150">Remarks</span></span>

<span data-ttu-id="3ca5b-151">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-151">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3ca5b-152">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3ca5b-152">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3ca5b-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="3ca5b-153">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3ca5b-154">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3ca5b-154">Schema Name</span></span>  <br/> |<span data-ttu-id="3ca5b-155">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3ca5b-155">Types schema</span></span>  <br/> |
|<span data-ttu-id="3ca5b-156">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3ca5b-156">Validation File</span></span>  <br/> |<span data-ttu-id="3ca5b-157">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3ca5b-157">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3ca5b-158">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3ca5b-158">Can be Empty</span></span>  <br/> |<span data-ttu-id="3ca5b-159">False</span><span class="sxs-lookup"><span data-stu-id="3ca5b-159">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3ca5b-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ca5b-160">See also</span></span>



- [<span data-ttu-id="3ca5b-161">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3ca5b-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

