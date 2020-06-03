---
title: SearchFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SearchFolder
api_type:
- schema
ms.assetid: 1a7d408b-2e98-4391-8834-085ed6d5757c
description: Das SearchFolder-Element stellt einen Suchordner dar, der in einem Postfach enthalten ist.
ms.openlocfilehash: e1d5893e00f3b199451622061785e2566c6f32e5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464007"
---
# <a name="searchfolder"></a><span data-ttu-id="702cc-103">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="702cc-103">SearchFolder</span></span>

<span data-ttu-id="702cc-104">Das **SearchFolder** -Element stellt einen Suchordner dar, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="702cc-104">The **SearchFolder** element represents a search folder that is contained in a mailbox.</span></span> 
  
```xml
<SearchFolder>
   <FolderId/>
   <ParentFolderId/>
   <FolderClass/>
   <DisplayName/>
   <TotalCount/>
   <ChildFolderCount/>
   <ExtendedProperty/>
   <ManagedFolderInformation/>
   <UnreadCount/>
   <SearchParameters/>
   <PermissionSet/>
      <EffectiveRights/>
</SearchFolder>
```

 <span data-ttu-id="702cc-105">**SearchFolderType**</span><span class="sxs-lookup"><span data-stu-id="702cc-105">**SearchFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="702cc-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="702cc-106">Attributes and elements</span></span>

<span data-ttu-id="702cc-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="702cc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="702cc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="702cc-108">Attributes</span></span>

<span data-ttu-id="702cc-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="702cc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="702cc-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="702cc-110">Child elements</span></span>

|<span data-ttu-id="702cc-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="702cc-111">**Element**</span></span>|<span data-ttu-id="702cc-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="702cc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="702cc-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="702cc-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="702cc-114">Enthält den Bezeichner und den Änderungsschlüssel eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="702cc-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="702cc-115">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="702cc-115">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="702cc-116">Stellt den Bezeichner des übergeordneten Ordners dar, der den Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="702cc-116">Represents the identifier of the parent folder that contains the folder.</span></span>  <br/> |
|[<span data-ttu-id="702cc-117">FolderClass</span><span class="sxs-lookup"><span data-stu-id="702cc-117">FolderClass</span></span>](folderclass.md) <br/> |<span data-ttu-id="702cc-118">Stellt die Folder-Klasse für einen bestimmten Ordner dar.</span><span class="sxs-lookup"><span data-stu-id="702cc-118">Represents the folder class for a given folder.</span></span>  <br/> |
|[<span data-ttu-id="702cc-119">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="702cc-119">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="702cc-120">Enthält den Anzeigenamen eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="702cc-120">Contains the display name of a folder.</span></span>  <br/> |
|[<span data-ttu-id="702cc-121">Total count</span><span class="sxs-lookup"><span data-stu-id="702cc-121">TotalCount</span></span>](totalcount.md) <br/> |<span data-ttu-id="702cc-122">Stellt die Gesamtanzahl der Elemente in einem bestimmten Ordner dar.</span><span class="sxs-lookup"><span data-stu-id="702cc-122">Represents the total count of items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="702cc-123">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="702cc-123">ChildFolderCount</span></span>](childfoldercount.md) <br/> |<span data-ttu-id="702cc-124">Stellt die Anzahl der untergeordneten Ordner dar, die in einem Ordner enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="702cc-124">Represents the number of child folders contained within a folder.</span></span> <span data-ttu-id="702cc-125">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="702cc-125">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="702cc-126">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="702cc-126">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="702cc-127">Identifiziert erweiterte Eigenschaften für Ordner.</span><span class="sxs-lookup"><span data-stu-id="702cc-127">Identifies extended properties on folders.</span></span>  <br/> |
|[<span data-ttu-id="702cc-128">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="702cc-128">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="702cc-129">Enthält Informationen zu einem verwalteten Ordner.</span><span class="sxs-lookup"><span data-stu-id="702cc-129">Contains information about a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="702cc-130">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="702cc-130">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="702cc-131">Stellt die Anzahl der ungelesenen Elemente in einem bestimmten Ordner dar.</span><span class="sxs-lookup"><span data-stu-id="702cc-131">Represents the count of unread items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="702cc-132">SearchParameters</span><span class="sxs-lookup"><span data-stu-id="702cc-132">SearchParameters</span></span>](searchparameters.md) <br/> |<span data-ttu-id="702cc-133">Enthält die Parameter, die einen Suchordner definieren.</span><span class="sxs-lookup"><span data-stu-id="702cc-133">Contains the parameters that define a search folder.</span></span>  <br/> |
|[<span data-ttu-id="702cc-134">PermissionSet (permissionsettype)</span><span class="sxs-lookup"><span data-stu-id="702cc-134">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="702cc-135">Enthält alle konfigurierten Berechtigungen für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="702cc-135">Contains all the configured permissions for a folder.</span></span> <span data-ttu-id="702cc-136">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="702cc-136">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="702cc-137">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="702cc-137">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="702cc-138">Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner.</span><span class="sxs-lookup"><span data-stu-id="702cc-138">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="702cc-139">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="702cc-139">This element is read-only.</span></span> <span data-ttu-id="702cc-140">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="702cc-140">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="702cc-141">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="702cc-141">Parent elements</span></span>

|<span data-ttu-id="702cc-142">**Element**</span><span class="sxs-lookup"><span data-stu-id="702cc-142">**Element**</span></span>|<span data-ttu-id="702cc-143">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="702cc-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="702cc-144">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="702cc-144">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="702cc-145">Gibt Daten an, die während einer [UpdateFolder-Vorgang](updatefolder-operation.md) an eine Ordnereigenschaft angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="702cc-145">Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="702cc-146">Erstellen (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="702cc-146">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="702cc-147">Gibt einen einzelnen Ordner an, der im lokalen Clientspeicher erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="702cc-147">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="702cc-148">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="702cc-148">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="702cc-149">Stellt eine Aktualisierung auf eine einzelne Eigenschaft in einem Ordner in einer [UpdateFolder-Vorgang](updatefolder-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="702cc-149">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="702cc-150">Update (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="702cc-150">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="702cc-151">Gibt einen einzelnen Ordner an, der im lokalen Clientspeicher aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="702cc-151">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="702cc-152">Ordner</span><span class="sxs-lookup"><span data-stu-id="702cc-152">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="702cc-153">Enthält ein Array von Ordnern, die in Ordnervorgängen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="702cc-153">Contains an array of folders used in folder operations.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="702cc-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="702cc-154">Remarks</span></span>

 <span data-ttu-id="702cc-155">**SearchFolder** wird sowohl für reguläre Suchordner als auch für MicrosoftOfficeOutlook und Outlook Web Access sichtbare Suchordner verwendet.</span><span class="sxs-lookup"><span data-stu-id="702cc-155">**SearchFolder** is used for both regular search folders and MicrosoftOfficeOutlook and Outlook Web Access visible search folders.</span></span> <span data-ttu-id="702cc-156">Damit ein Suchordner für Outlook und Outlook Web Access sichtbar ist, muss der Ordner unter dem Distinguished Folder SearchFolders erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="702cc-156">For a search folder to be visible to Outlook and Outlook Web Access, the folder must be created under the SearchFolders distinguished folder.</span></span> 
  
<span data-ttu-id="702cc-157">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="702cc-157">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="702cc-158">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="702cc-158">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="702cc-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="702cc-159">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="702cc-160">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="702cc-160">Schema Name</span></span>  <br/> |<span data-ttu-id="702cc-161">Schematypen</span><span class="sxs-lookup"><span data-stu-id="702cc-161">Types schema</span></span>  <br/> |
|<span data-ttu-id="702cc-162">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="702cc-162">Validation File</span></span>  <br/> |<span data-ttu-id="702cc-163">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="702cc-163">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="702cc-164">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="702cc-164">Can be Empty</span></span>  <br/> |<span data-ttu-id="702cc-165">False</span><span class="sxs-lookup"><span data-stu-id="702cc-165">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="702cc-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="702cc-166">See also</span></span>



- [<span data-ttu-id="702cc-167">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="702cc-167">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

