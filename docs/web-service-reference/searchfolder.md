---
title: "\"SearchFolder\""
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
description: Das Element "SearchFolder" stellt einen Suchordner, der in einem Postfach enthalten ist.
ms.openlocfilehash: d842c54dab7950c68e26804b676834c2d95debad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831302"
---
# <a name="searchfolder"></a><span data-ttu-id="427f0-103">"SearchFolder"</span><span class="sxs-lookup"><span data-stu-id="427f0-103">SearchFolder</span></span>

<span data-ttu-id="427f0-104">Das Element **"SearchFolder"** stellt einen Suchordner, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="427f0-104">The **SearchFolder** element represents a search folder that is contained in a mailbox.</span></span> 
  
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

 <span data-ttu-id="427f0-105">**SearchFolderType**</span><span class="sxs-lookup"><span data-stu-id="427f0-105">**SearchFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="427f0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="427f0-106">Attributes and elements</span></span>

<span data-ttu-id="427f0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="427f0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="427f0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="427f0-108">Attributes</span></span>

<span data-ttu-id="427f0-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="427f0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="427f0-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="427f0-110">Child elements</span></span>

|<span data-ttu-id="427f0-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="427f0-111">**Element**</span></span>|<span data-ttu-id="427f0-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="427f0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="427f0-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="427f0-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="427f0-114">Enthält den Schlüssel-ID und Ändern eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="427f0-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="427f0-115">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="427f0-115">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="427f0-116">Stellt den Bezeichner des übergeordneten Ordners, der den Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="427f0-116">Represents the identifier of the parent folder that contains the folder.</span></span>  <br/> |
|[<span data-ttu-id="427f0-117">FolderClass</span><span class="sxs-lookup"><span data-stu-id="427f0-117">FolderClass</span></span>](folderclass.md) <br/> |<span data-ttu-id="427f0-118">Stellt die Ordner-Klasse für einen bestimmten Ordner.</span><span class="sxs-lookup"><span data-stu-id="427f0-118">Represents the folder class for a given folder.</span></span>  <br/> |
|[<span data-ttu-id="427f0-119">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="427f0-119">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="427f0-120">Enthält den Anzeigenamen eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="427f0-120">Contains the display name of a folder.</span></span>  <br/> |
|[<span data-ttu-id="427f0-121">TotalCount</span><span class="sxs-lookup"><span data-stu-id="427f0-121">TotalCount</span></span>](totalcount.md) <br/> |<span data-ttu-id="427f0-122">Stellt die gesamte Anzahl von Elementen in einem bestimmten Ordner an.</span><span class="sxs-lookup"><span data-stu-id="427f0-122">Represents the total count of items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="427f0-123">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="427f0-123">ChildFolderCount</span></span>](childfoldercount.md) <br/> |<span data-ttu-id="427f0-124">Die Anzahl der in einem Ordner enthaltenen untergeordneten Ordner darstellt.</span><span class="sxs-lookup"><span data-stu-id="427f0-124">Represents the number of child folders contained within a folder.</span></span> <span data-ttu-id="427f0-125">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="427f0-125">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="427f0-126">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="427f0-126">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="427f0-127">Erweiterte Eigenschaften für Ordner identifiziert.</span><span class="sxs-lookup"><span data-stu-id="427f0-127">Identifies extended properties on folders.</span></span>  <br/> |
|[<span data-ttu-id="427f0-128">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="427f0-128">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="427f0-129">Enthält Informationen zu einem verwalteten Ordner.</span><span class="sxs-lookup"><span data-stu-id="427f0-129">Contains information about a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="427f0-130">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="427f0-130">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="427f0-131">Die Anzahl der ungelesenen Elemente innerhalb eines bestimmten Ordners darstellt.</span><span class="sxs-lookup"><span data-stu-id="427f0-131">Represents the count of unread items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="427f0-132">SearchParameters</span><span class="sxs-lookup"><span data-stu-id="427f0-132">SearchParameters</span></span>](searchparameters.md) <br/> |<span data-ttu-id="427f0-133">Enthält die Parameter, die einen Suchordner definieren.</span><span class="sxs-lookup"><span data-stu-id="427f0-133">Contains the parameters that define a search folder.</span></span>  <br/> |
|[<span data-ttu-id="427f0-134">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="427f0-134">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="427f0-135">Enthält die konfigurierten Berechtigungen für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="427f0-135">Contains all the configured permissions for a folder.</span></span> <span data-ttu-id="427f0-136">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="427f0-136">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="427f0-137">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="427f0-137">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="427f0-138">Der Client Rechte basierend auf den berechtigungseinstellungen für das Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="427f0-138">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="427f0-139">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="427f0-139">This element is read-only.</span></span> <span data-ttu-id="427f0-140">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="427f0-140">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="427f0-141">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="427f0-141">Parent elements</span></span>

|<span data-ttu-id="427f0-142">**Element**</span><span class="sxs-lookup"><span data-stu-id="427f0-142">**Element**</span></span>|<span data-ttu-id="427f0-143">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="427f0-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="427f0-144">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="427f0-144">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="427f0-145">Gibt Daten an, die während einer [UpdateFolder-Vorgang](updatefolder-operation.md) an eine Ordnereigenschaft angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="427f0-145">Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="427f0-146">Erstellen (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="427f0-146">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="427f0-147">Gibt einen einzelnen Ordner im lokalen Client-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="427f0-147">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="427f0-148">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="427f0-148">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="427f0-149">Stellt eine Aktualisierung auf eine einzelne Eigenschaft in einem Ordner in einer [UpdateFolder-Vorgang](updatefolder-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="427f0-149">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="427f0-150">Update (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="427f0-150">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="427f0-151">Gibt einen einzelnen Ordner, in den lokalen Client-Speicher zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="427f0-151">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="427f0-152">Ordner</span><span class="sxs-lookup"><span data-stu-id="427f0-152">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="427f0-153">Enthält ein Array von Ordnern im Ordner Vorgänge verwendet.</span><span class="sxs-lookup"><span data-stu-id="427f0-153">Contains an array of folders used in folder operations.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="427f0-154">Hinweise</span><span class="sxs-lookup"><span data-stu-id="427f0-154">Remarks</span></span>

 <span data-ttu-id="427f0-155">**"SearchFolder"** wird für die regulären Suchordner und MicrosoftOfficeOutlook und Outlook Web Access sichtbar Suchordner.</span><span class="sxs-lookup"><span data-stu-id="427f0-155">**SearchFolder** is used for both regular search folders and MicrosoftOfficeOutlook and Outlook Web Access visible search folders.</span></span> <span data-ttu-id="427f0-156">Für ein Suchordner für Outlook und Outlook Web Access sichtbar sein soll muss der Ordner unter dem definierten SearchFolders-Ordner erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="427f0-156">For a search folder to be visible to Outlook and Outlook Web Access, the folder must be created under the SearchFolders distinguished folder.</span></span> 
  
<span data-ttu-id="427f0-157">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="427f0-157">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="427f0-158">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="427f0-158">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="427f0-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="427f0-159">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="427f0-160">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="427f0-160">Schema Name</span></span>  <br/> |<span data-ttu-id="427f0-161">Schematypen</span><span class="sxs-lookup"><span data-stu-id="427f0-161">Types schema</span></span>  <br/> |
|<span data-ttu-id="427f0-162">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="427f0-162">Validation File</span></span>  <br/> |<span data-ttu-id="427f0-163">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="427f0-163">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="427f0-164">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="427f0-164">Can be Empty</span></span>  <br/> |<span data-ttu-id="427f0-165">False</span><span class="sxs-lookup"><span data-stu-id="427f0-165">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="427f0-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="427f0-166">See also</span></span>



- [<span data-ttu-id="427f0-167">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="427f0-167">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

