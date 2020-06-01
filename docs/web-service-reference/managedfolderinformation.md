---
title: ManagedFolderInformation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ManagedFolderInformation
api_type:
- schema
ms.assetid: dea980eb-8303-47fe-a380-20a8efc9ead6
description: Das ManagedFolderInformation-Element enthält Informationen zu einem verwalteten benutzerdefinierten Ordner.
ms.openlocfilehash: ce15dcb15cccdce253494beefd2f4a2a7a0c0ad8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44450949"
---
# <a name="managedfolderinformation"></a><span data-ttu-id="033d1-103">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="033d1-103">ManagedFolderInformation</span></span>

<span data-ttu-id="033d1-104">Das **ManagedFolderInformation** -Element enthält Informationen zu einem verwalteten benutzerdefinierten Ordner.</span><span class="sxs-lookup"><span data-stu-id="033d1-104">The **ManagedFolderInformation** element contains information about a managed custom folder.</span></span> 
  
```xml
<ManagedFolderInformation>
   <CanDelete/>
   <CanRenameOrMove/>
   <MustDisplayComment/>
   <HasQuota/>
   <IsManagedFoldersRoot/>
   <ManagedFolderId/>
   <Comment/>
   <StorageQuota/>
   <FolderSize/>
   <HomePage/>
</ManagedFolderInformation>
```

 <span data-ttu-id="033d1-105">**ManagedFolderInformationType**</span><span class="sxs-lookup"><span data-stu-id="033d1-105">**ManagedFolderInformationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="033d1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="033d1-106">Attributes and elements</span></span>

<span data-ttu-id="033d1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="033d1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="033d1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="033d1-108">Attributes</span></span>

<span data-ttu-id="033d1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="033d1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="033d1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="033d1-110">Child elements</span></span>

|<span data-ttu-id="033d1-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="033d1-111">**Element**</span></span>|<span data-ttu-id="033d1-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="033d1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="033d1-113">CanDelete</span><span class="sxs-lookup"><span data-stu-id="033d1-113">CanDelete</span></span>](candelete.md) <br/> |<span data-ttu-id="033d1-114">Gibt an, ob ein verwalteter Ordner von einem Kunden gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="033d1-114">Indicates whether a managed folder can be deleted by a customer.</span></span>  <br/> |
|[<span data-ttu-id="033d1-115">CanRenameOrMove</span><span class="sxs-lookup"><span data-stu-id="033d1-115">CanRenameOrMove</span></span>](canrenameormove.md) <br/> |<span data-ttu-id="033d1-116">Gibt an, ob ein bestimmter verwalteter Ordner vom Kunden umbenannt oder verschoben werden kann.</span><span class="sxs-lookup"><span data-stu-id="033d1-116">Indicates whether a given managed folder can be renamed or moved by the customer.</span></span>  <br/> |
|[<span data-ttu-id="033d1-117">MustDisplayComment</span><span class="sxs-lookup"><span data-stu-id="033d1-117">MustDisplayComment</span></span>](mustdisplaycomment.md) <br/> |<span data-ttu-id="033d1-118">Gibt an, ob der Kommentar des verwalteten Ordners angezeigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="033d1-118">Indicates whether the managed folder comment must be displayed.</span></span>  <br/> |
|[<span data-ttu-id="033d1-119">HasQuota</span><span class="sxs-lookup"><span data-stu-id="033d1-119">HasQuota</span></span>](hasquota.md) <br/> |<span data-ttu-id="033d1-120">Gibt an, ob der verwaltete Ordner ein Kontingent aufweist.</span><span class="sxs-lookup"><span data-stu-id="033d1-120">Indicates whether the managed folder has a quota.</span></span>  <br/> |
|[<span data-ttu-id="033d1-121">IsManagedFoldersRoot</span><span class="sxs-lookup"><span data-stu-id="033d1-121">IsManagedFoldersRoot</span></span>](ismanagedfoldersroot.md) <br/> |<span data-ttu-id="033d1-122">Gibt an, ob der verwaltete Ordner der Stamm für alle verwalteten Ordner ist.</span><span class="sxs-lookup"><span data-stu-id="033d1-122">Indicates whether the managed folder is the root for all managed folders.</span></span>  <br/> |
|[<span data-ttu-id="033d1-123">ManagedFolderId</span><span class="sxs-lookup"><span data-stu-id="033d1-123">ManagedFolderId</span></span>](managedfolderid.md) <br/> |<span data-ttu-id="033d1-124">Enthält die Ordner-ID des verwalteten Ordners.</span><span class="sxs-lookup"><span data-stu-id="033d1-124">Contains the folder ID of the managed folder.</span></span>  <br/> |
|[<span data-ttu-id="033d1-125">Kommentar</span><span class="sxs-lookup"><span data-stu-id="033d1-125">Comment</span></span>](comment.md) <br/> |<span data-ttu-id="033d1-126">Enthält den Kommentar, der einem verwalteten Ordner zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="033d1-126">Contains the comment that is associated with a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="033d1-127">StorageQuota</span><span class="sxs-lookup"><span data-stu-id="033d1-127">StorageQuota</span></span>](storagequota.md) <br/> |<span data-ttu-id="033d1-128">Beschreibt das Speicherkontingent für den verwalteten Ordner.</span><span class="sxs-lookup"><span data-stu-id="033d1-128">Describes the storage quota for the managed folder.</span></span>  <br/> |
|[<span data-ttu-id="033d1-129">FolderSize</span><span class="sxs-lookup"><span data-stu-id="033d1-129">FolderSize</span></span>](foldersize.md) <br/> |<span data-ttu-id="033d1-130">Beschreibt die Gesamtgröße aller Inhalte eines verwalteten Ordners.</span><span class="sxs-lookup"><span data-stu-id="033d1-130">Describes the total size of all the contents of a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="033d1-131">HomePage</span><span class="sxs-lookup"><span data-stu-id="033d1-131">HomePage</span></span>](homepage.md) <br/> |<span data-ttu-id="033d1-132">Gibt die URL an, die als Standardstartseite für den verwalteten Ordner verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="033d1-132">Specifies the URL that will be the default home page for the managed folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="033d1-133">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="033d1-133">Parent elements</span></span>

|<span data-ttu-id="033d1-134">**Element**</span><span class="sxs-lookup"><span data-stu-id="033d1-134">**Element**</span></span>|<span data-ttu-id="033d1-135">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="033d1-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="033d1-136">Folder</span><span class="sxs-lookup"><span data-stu-id="033d1-136">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="033d1-137">Stellt einen Ordner im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="033d1-137">Represents a folder in the Exchange store.</span></span> <span data-ttu-id="033d1-138">Verwaltete benutzerdefinierte Ordner können nur Unterordner des Ordners mit dem Namen " **verwaltete Ordner**" sein.</span><span class="sxs-lookup"><span data-stu-id="033d1-138">Managed custom folders can only be subfolders of the folder named **Managed Folders**.</span></span>  <br/> |
|[<span data-ttu-id="033d1-139">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="033d1-139">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="033d1-140">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="033d1-140">Not applicable.</span></span>  <br/> |
|[<span data-ttu-id="033d1-141">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="033d1-141">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="033d1-142">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="033d1-142">Not applicable.</span></span>  <br/> |
|[<span data-ttu-id="033d1-143">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="033d1-143">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="033d1-144">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="033d1-144">Not applicable.</span></span>  <br/> |
|[<span data-ttu-id="033d1-145">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="033d1-145">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="033d1-146">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="033d1-146">Not applicable.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="033d1-147">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="033d1-147">Remarks</span></span>

<span data-ttu-id="033d1-148">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="033d1-148">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="033d1-149">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="033d1-149">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="033d1-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="033d1-150">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="033d1-151">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="033d1-151">Schema name</span></span>  <br/> |<span data-ttu-id="033d1-152">Schematypen</span><span class="sxs-lookup"><span data-stu-id="033d1-152">Types schema</span></span>  <br/> |
|<span data-ttu-id="033d1-153">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="033d1-153">Validation file</span></span>  <br/> |<span data-ttu-id="033d1-154">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="033d1-154">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="033d1-155">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="033d1-155">Can be empty</span></span>  <br/> |<span data-ttu-id="033d1-156">False</span><span class="sxs-lookup"><span data-stu-id="033d1-156">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="033d1-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="033d1-157">See also</span></span>



[<span data-ttu-id="033d1-158">CreateManagedFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="033d1-158">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md)


- [<span data-ttu-id="033d1-159">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="033d1-159">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="033d1-160">Hinzufügen von verwalteten Ordnern</span><span class="sxs-lookup"><span data-stu-id="033d1-160">Adding Managed Folders</span></span>](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

