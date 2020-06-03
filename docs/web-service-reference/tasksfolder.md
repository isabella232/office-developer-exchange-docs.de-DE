---
title: TasksFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TasksFolder
api_type:
- schema
ms.assetid: 5a9a4612-8064-4986-b467-c44f268c64df
description: Das TasksFolder-Element stellt einen Aufgabenordner dar, der in einem Postfach enthalten ist.
ms.openlocfilehash: 522fe485482bd8159927f9925b7a5582ba2e1c22
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465338"
---
# <a name="tasksfolder"></a><span data-ttu-id="19adc-103">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="19adc-103">TasksFolder</span></span>

<span data-ttu-id="19adc-104">Das **TasksFolder** -Element stellt einen Aufgabenordner dar, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="19adc-104">The **TasksFolder** element represents a Tasks folder that is contained in a mailbox.</span></span> 
  
```xml
<TasksFolder>
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
</TasksFolder>
```

<span data-ttu-id="19adc-105">**TasksFolderType**</span><span class="sxs-lookup"><span data-stu-id="19adc-105">**TasksFolderType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="19adc-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="19adc-106">Attributes and elements</span></span>

<span data-ttu-id="19adc-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="19adc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="19adc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="19adc-108">Attributes</span></span>

<span data-ttu-id="19adc-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="19adc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="19adc-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="19adc-110">Child elements</span></span>

|<span data-ttu-id="19adc-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="19adc-111">**Element**</span></span>|<span data-ttu-id="19adc-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="19adc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="19adc-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="19adc-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="19adc-114">Enthält den Bezeichner und den Änderungsschlüssel eines Aufgabenordners.</span><span class="sxs-lookup"><span data-stu-id="19adc-114">Contains the identifier and change key of a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="19adc-115">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="19adc-115">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="19adc-116">Stellt den Bezeichner des übergeordneten Ordners dar, der den Ordner Aufgaben enthält.</span><span class="sxs-lookup"><span data-stu-id="19adc-116">Represents the identifier of the parent folder that contains the Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="19adc-117">FolderClass</span><span class="sxs-lookup"><span data-stu-id="19adc-117">FolderClass</span></span>](folderclass.md) <br/> |<span data-ttu-id="19adc-118">Stellt die Folder-Klasse für einen Aufgabenordner dar.</span><span class="sxs-lookup"><span data-stu-id="19adc-118">Represents the folder class for a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="19adc-119">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="19adc-119">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="19adc-120">Enthält den Anzeigenamen eines Aufgabenordners.</span><span class="sxs-lookup"><span data-stu-id="19adc-120">Contains the display name of a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="19adc-121">Total count</span><span class="sxs-lookup"><span data-stu-id="19adc-121">TotalCount</span></span>](totalcount.md) <br/> |<span data-ttu-id="19adc-122">Stellt die Gesamtanzahl der Elemente in einem Aufgabenordner dar.</span><span class="sxs-lookup"><span data-stu-id="19adc-122">Represents the total count of items within a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="19adc-123">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="19adc-123">ChildFolderCount</span></span>](childfoldercount.md) <br/> |<span data-ttu-id="19adc-124">Stellt die Anzahl der untergeordneten Ordner dar, die in einem Aufgabenordner enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="19adc-124">Represents the number of child folders that are contained within a Tasks folder.</span></span> <span data-ttu-id="19adc-125">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="19adc-125">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="19adc-126">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="19adc-126">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="19adc-127">Identifiziert erweiterte Eigenschaften für einen Aufgabenordner.</span><span class="sxs-lookup"><span data-stu-id="19adc-127">Identifies extended properties on a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="19adc-128">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="19adc-128">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="19adc-129">Enthält Informationen zu einem verwalteten Ordner.</span><span class="sxs-lookup"><span data-stu-id="19adc-129">Contains information about a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="19adc-130">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="19adc-130">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="19adc-131">Stellt die Anzahl der ungelesenen Elemente in einem Aufgabenordner dar.</span><span class="sxs-lookup"><span data-stu-id="19adc-131">Represents the count of unread items within a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="19adc-132">PermissionSet (permissionsettype)</span><span class="sxs-lookup"><span data-stu-id="19adc-132">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="19adc-133">Enthält alle konfigurierten Berechtigungen für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="19adc-133">Contains all the configured permissions for a folder.</span></span> <span data-ttu-id="19adc-134">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="19adc-134">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="19adc-135">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="19adc-135">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="19adc-136">Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner.</span><span class="sxs-lookup"><span data-stu-id="19adc-136">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="19adc-137">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="19adc-137">This element is read-only.</span></span> <span data-ttu-id="19adc-138">Dieses Element wurde in Microsoft Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="19adc-138">This element was introduced in Microsoft Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="19adc-139">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="19adc-139">Parent elements</span></span>

|<span data-ttu-id="19adc-140">**Element**</span><span class="sxs-lookup"><span data-stu-id="19adc-140">**Element**</span></span>|<span data-ttu-id="19adc-141">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="19adc-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="19adc-142">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="19adc-142">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="19adc-143">Gibt Daten an, die während einer [UpdateFolder-Vorgang](updatefolder-operation.md) an eine Ordnereigenschaft angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="19adc-143">Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="19adc-144">Erstellen (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="19adc-144">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="19adc-145">Gibt einen einzelnen Ordner an, der im lokalen Clientspeicher erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="19adc-145">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="19adc-146">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="19adc-146">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="19adc-147">Stellt eine Aktualisierung auf eine einzelne Eigenschaft in einem Ordner in einer [UpdateFolder-Vorgang](updatefolder-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="19adc-147">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="19adc-148">Update (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="19adc-148">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="19adc-149">Gibt einen einzelnen Ordner an, der im lokalen Clientspeicher aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="19adc-149">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="19adc-150">Ordner</span><span class="sxs-lookup"><span data-stu-id="19adc-150">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="19adc-151">Enthält ein Array von Ordnern, die in Ordnervorgängen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="19adc-151">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="19adc-152">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19adc-152">Remarks</span></span>

<span data-ttu-id="19adc-153">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="19adc-153">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="19adc-154">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="19adc-154">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19adc-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="19adc-155">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="19adc-156">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="19adc-156">Schema Name</span></span>  <br/> |<span data-ttu-id="19adc-157">Schematypen</span><span class="sxs-lookup"><span data-stu-id="19adc-157">Types schema</span></span>  <br/> |
|<span data-ttu-id="19adc-158">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="19adc-158">Validation File</span></span>  <br/> |<span data-ttu-id="19adc-159">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="19adc-159">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="19adc-160">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="19adc-160">Can be Empty</span></span>  <br/> |<span data-ttu-id="19adc-161">False</span><span class="sxs-lookup"><span data-stu-id="19adc-161">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="19adc-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19adc-162">See also</span></span>

- [<span data-ttu-id="19adc-163">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="19adc-163">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

