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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831302"
---
# <a name="searchfolder"></a><span data-ttu-id="bac56-103">"SearchFolder"</span><span class="sxs-lookup"><span data-stu-id="bac56-103">SearchFolder</span></span>

<span data-ttu-id="bac56-104">Das Element **"SearchFolder"** stellt einen Suchordner, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="bac56-104">The **SearchFolder** element represents a search folder that is contained in a mailbox.</span></span> 
  
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

 <span data-ttu-id="bac56-105">**SearchFolderType**</span><span class="sxs-lookup"><span data-stu-id="bac56-105">**SearchFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bac56-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bac56-106">Attributes and elements</span></span>

<span data-ttu-id="bac56-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bac56-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bac56-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="bac56-108">Attributes</span></span>

<span data-ttu-id="bac56-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="bac56-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bac56-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bac56-110">Child elements</span></span>

|<span data-ttu-id="bac56-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="bac56-111">**Element**</span></span>|<span data-ttu-id="bac56-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bac56-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bac56-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="bac56-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="bac56-114">Enthält den Schlüssel-ID und Ändern eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="bac56-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="bac56-115">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="bac56-115">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="bac56-116">Stellt den Bezeichner des übergeordneten Ordners, der den Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="bac56-116">Represents the identifier of the parent folder that contains the folder.</span></span>  <br/> |
|[<span data-ttu-id="bac56-117">FolderClass</span><span class="sxs-lookup"><span data-stu-id="bac56-117">FolderClass</span></span>](folderclass.md) <br/> |<span data-ttu-id="bac56-118">Stellt die Ordner-Klasse für einen bestimmten Ordner.</span><span class="sxs-lookup"><span data-stu-id="bac56-118">Represents the folder class for a given folder.</span></span>  <br/> |
|[<span data-ttu-id="bac56-119">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="bac56-119">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="bac56-120">Enthält den Anzeigenamen eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="bac56-120">Contains the display name of a folder.</span></span>  <br/> |
|[<span data-ttu-id="bac56-121">TotalCount</span><span class="sxs-lookup"><span data-stu-id="bac56-121">TotalCount</span></span>](totalcount.md) <br/> |<span data-ttu-id="bac56-122">Stellt die gesamte Anzahl von Elementen in einem bestimmten Ordner an.</span><span class="sxs-lookup"><span data-stu-id="bac56-122">Represents the total count of items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="bac56-123">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="bac56-123">ChildFolderCount</span></span>](childfoldercount.md) <br/> |<span data-ttu-id="bac56-124">Die Anzahl der in einem Ordner enthaltenen untergeordneten Ordner darstellt.</span><span class="sxs-lookup"><span data-stu-id="bac56-124">Represents the number of child folders contained within a folder.</span></span> <span data-ttu-id="bac56-125">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="bac56-125">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="bac56-126">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="bac56-126">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="bac56-127">Erweiterte Eigenschaften für Ordner identifiziert.</span><span class="sxs-lookup"><span data-stu-id="bac56-127">Identifies extended properties on folders.</span></span>  <br/> |
|[<span data-ttu-id="bac56-128">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="bac56-128">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="bac56-129">Enthält Informationen zu einem verwalteten Ordner.</span><span class="sxs-lookup"><span data-stu-id="bac56-129">Contains information about a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="bac56-130">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="bac56-130">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="bac56-131">Die Anzahl der ungelesenen Elemente innerhalb eines bestimmten Ordners darstellt.</span><span class="sxs-lookup"><span data-stu-id="bac56-131">Represents the count of unread items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="bac56-132">SearchParameters</span><span class="sxs-lookup"><span data-stu-id="bac56-132">SearchParameters</span></span>](searchparameters.md) <br/> |<span data-ttu-id="bac56-133">Enthält die Parameter, die einen Suchordner definieren.</span><span class="sxs-lookup"><span data-stu-id="bac56-133">Contains the parameters that define a search folder.</span></span>  <br/> |
|[<span data-ttu-id="bac56-134">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="bac56-134">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="bac56-135">Enthält die konfigurierten Berechtigungen für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="bac56-135">Contains all the configured permissions for a folder.</span></span> <span data-ttu-id="bac56-136">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="bac56-136">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="bac56-137">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="bac56-137">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="bac56-138">Der Client Rechte basierend auf den berechtigungseinstellungen für das Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="bac56-138">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="bac56-139">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="bac56-139">This element is read-only.</span></span> <span data-ttu-id="bac56-140">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="bac56-140">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bac56-141">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bac56-141">Parent elements</span></span>

|<span data-ttu-id="bac56-142">**Element**</span><span class="sxs-lookup"><span data-stu-id="bac56-142">**Element**</span></span>|<span data-ttu-id="bac56-143">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bac56-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bac56-144">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="bac56-144">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="bac56-145">Gibt Daten an, die während einer [UpdateFolder-Vorgang](updatefolder-operation.md) an eine Ordnereigenschaft angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bac56-145">Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="bac56-146">Erstellen (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="bac56-146">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="bac56-147">Gibt einen einzelnen Ordner im lokalen Client-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bac56-147">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="bac56-148">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="bac56-148">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="bac56-149">Stellt eine Aktualisierung auf eine einzelne Eigenschaft in einem Ordner in einer [UpdateFolder-Vorgang](updatefolder-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="bac56-149">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="bac56-150">Update (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="bac56-150">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="bac56-151">Gibt einen einzelnen Ordner, in den lokalen Client-Speicher zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="bac56-151">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="bac56-152">Ordner</span><span class="sxs-lookup"><span data-stu-id="bac56-152">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="bac56-153">Enthält ein Array von Ordnern im Ordner Vorgänge verwendet.</span><span class="sxs-lookup"><span data-stu-id="bac56-153">Contains an array of folders used in folder operations.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bac56-154">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bac56-154">Remarks</span></span>

 <span data-ttu-id="bac56-155">**"SearchFolder"** wird für die regulären Suchordner und MicrosoftOfficeOutlook und Outlook Web Access sichtbar Suchordner.</span><span class="sxs-lookup"><span data-stu-id="bac56-155">**SearchFolder** is used for both regular search folders and MicrosoftOfficeOutlook and Outlook Web Access visible search folders.</span></span> <span data-ttu-id="bac56-156">Für ein Suchordner für Outlook und Outlook Web Access sichtbar sein soll muss der Ordner unter dem definierten SearchFolders-Ordner erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="bac56-156">For a search folder to be visible to Outlook and Outlook Web Access, the folder must be created under the SearchFolders distinguished folder.</span></span> 
  
<span data-ttu-id="bac56-157">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="bac56-157">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bac56-158">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="bac56-158">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bac56-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="bac56-159">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bac56-160">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bac56-160">Schema Name</span></span>  <br/> |<span data-ttu-id="bac56-161">Schematypen</span><span class="sxs-lookup"><span data-stu-id="bac56-161">Types schema</span></span>  <br/> |
|<span data-ttu-id="bac56-162">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bac56-162">Validation File</span></span>  <br/> |<span data-ttu-id="bac56-163">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bac56-163">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bac56-164">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="bac56-164">Can be Empty</span></span>  <br/> |<span data-ttu-id="bac56-165">False</span><span class="sxs-lookup"><span data-stu-id="bac56-165">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bac56-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bac56-166">See also</span></span>



- [<span data-ttu-id="bac56-167">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="bac56-167">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

