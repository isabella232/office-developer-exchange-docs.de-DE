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
description: Das TasksFolder-Element darstellt, einen Aufgabenordner, der in einem Postfach enthalten ist.
ms.openlocfilehash: b2151c68519a6ff15fbc74b48fc93a7e06af9e76
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839162"
---
# <a name="tasksfolder"></a><span data-ttu-id="9465b-103">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="9465b-103">TasksFolder</span></span>

<span data-ttu-id="9465b-104">Das **TasksFolder** -Element darstellt, einen Aufgabenordner, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="9465b-104">The **TasksFolder** element represents a Tasks folder that is contained in a mailbox.</span></span> 
  
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

<span data-ttu-id="9465b-105">**TasksFolderType**</span><span class="sxs-lookup"><span data-stu-id="9465b-105">**TasksFolderType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="9465b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9465b-106">Attributes and elements</span></span>

<span data-ttu-id="9465b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9465b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9465b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9465b-108">Attributes</span></span>

<span data-ttu-id="9465b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9465b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9465b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9465b-110">Child elements</span></span>

|<span data-ttu-id="9465b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="9465b-111">**Element**</span></span>|<span data-ttu-id="9465b-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9465b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9465b-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="9465b-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="9465b-114">Den Schlüssel-ID und Ändern des einem Aufgabenordner enthält.</span><span class="sxs-lookup"><span data-stu-id="9465b-114">Contains the identifier and change key of a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="9465b-115">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="9465b-115">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="9465b-116">Stellt den Bezeichner des übergeordneten Ordners, der den Ordner Aufgaben enthält.</span><span class="sxs-lookup"><span data-stu-id="9465b-116">Represents the identifier of the parent folder that contains the Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="9465b-117">FolderClass</span><span class="sxs-lookup"><span data-stu-id="9465b-117">FolderClass</span></span>](folderclass.md) <br/> |<span data-ttu-id="9465b-118">Stellt die Ordner-Klasse für einen Aufgabenordner dar.</span><span class="sxs-lookup"><span data-stu-id="9465b-118">Represents the folder class for a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="9465b-119">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="9465b-119">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="9465b-120">Enthält den Anzeigenamen der Aufgabenordner.</span><span class="sxs-lookup"><span data-stu-id="9465b-120">Contains the display name of a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="9465b-121">TotalCount</span><span class="sxs-lookup"><span data-stu-id="9465b-121">TotalCount</span></span>](totalcount.md) <br/> |<span data-ttu-id="9465b-122">Stellt die gesamte Anzahl von Elementen in einem Aufgabenordner dar.</span><span class="sxs-lookup"><span data-stu-id="9465b-122">Represents the total count of items within a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="9465b-123">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="9465b-123">ChildFolderCount</span></span>](childfoldercount.md) <br/> |<span data-ttu-id="9465b-124">Stellt die Anzahl der untergeordneten Ordner, die in einem Aufgabenordner enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="9465b-124">Represents the number of child folders that are contained within a Tasks folder.</span></span> <span data-ttu-id="9465b-125">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9465b-125">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="9465b-126">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="9465b-126">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="9465b-127">Erweiterte Eigenschaften auf einem Aufgabenordner identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9465b-127">Identifies extended properties on a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="9465b-128">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="9465b-128">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="9465b-129">Enthält Informationen zu einem verwalteten Ordner.</span><span class="sxs-lookup"><span data-stu-id="9465b-129">Contains information about a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="9465b-130">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="9465b-130">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="9465b-131">Stellt die Anzahl der ungelesenen Elemente in einem Aufgabenordner dar.</span><span class="sxs-lookup"><span data-stu-id="9465b-131">Represents the count of unread items within a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="9465b-132">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="9465b-132">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="9465b-133">Enthält die konfigurierten Berechtigungen für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="9465b-133">Contains all the configured permissions for a folder.</span></span> <span data-ttu-id="9465b-134">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9465b-134">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="9465b-135">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="9465b-135">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="9465b-136">Der Client Rechte basierend auf den berechtigungseinstellungen für das Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="9465b-136">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="9465b-137">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9465b-137">This element is read-only.</span></span> <span data-ttu-id="9465b-138">Dieses Element wurde in Microsoft Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9465b-138">This element was introduced in Microsoft Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9465b-139">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9465b-139">Parent elements</span></span>

|<span data-ttu-id="9465b-140">**Element**</span><span class="sxs-lookup"><span data-stu-id="9465b-140">**Element**</span></span>|<span data-ttu-id="9465b-141">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9465b-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9465b-142">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="9465b-142">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="9465b-143">Gibt Daten an, die während einer [UpdateFolder-Vorgang](updatefolder-operation.md) an eine Ordnereigenschaft angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9465b-143">Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="9465b-144">Erstellen (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="9465b-144">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="9465b-145">Gibt einen einzelnen Ordner im lokalen Client-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9465b-145">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="9465b-146">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="9465b-146">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="9465b-147">Stellt eine Aktualisierung auf eine einzelne Eigenschaft in einem Ordner in einer [UpdateFolder-Vorgang](updatefolder-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="9465b-147">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="9465b-148">Update (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="9465b-148">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="9465b-149">Gibt einen einzelnen Ordner, in den lokalen Client-Speicher zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9465b-149">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="9465b-150">Ordner</span><span class="sxs-lookup"><span data-stu-id="9465b-150">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="9465b-151">Enthält ein Array von Ordnern, die im Ordner Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9465b-151">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9465b-152">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9465b-152">Remarks</span></span>

<span data-ttu-id="9465b-153">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="9465b-153">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9465b-154">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9465b-154">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9465b-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="9465b-155">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9465b-156">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9465b-156">Schema Name</span></span>  <br/> |<span data-ttu-id="9465b-157">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9465b-157">Types schema</span></span>  <br/> |
|<span data-ttu-id="9465b-158">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9465b-158">Validation File</span></span>  <br/> |<span data-ttu-id="9465b-159">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9465b-159">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9465b-160">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9465b-160">Can be Empty</span></span>  <br/> |<span data-ttu-id="9465b-161">False</span><span class="sxs-lookup"><span data-stu-id="9465b-161">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9465b-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9465b-162">See also</span></span>

- [<span data-ttu-id="9465b-163">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9465b-163">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

