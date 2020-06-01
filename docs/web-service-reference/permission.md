---
title: Berechtigung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Permission
api_type:
- schema
ms.assetid: b8d0429a-0e58-4480-9847-4901970c7033
description: Das Permission-Element definiert den Zugriff, den ein Benutzer in einen Ordner hat.
ms.openlocfilehash: 0f7515dbb06f8423f8d4d95e1391496e8ac73653
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459258"
---
# <a name="permission"></a><span data-ttu-id="6c897-103">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="6c897-103">Permission</span></span>

<span data-ttu-id="6c897-104">Das **Permission** -Element definiert den Zugriff, den ein Benutzer in einen Ordner hat.</span><span class="sxs-lookup"><span data-stu-id="6c897-104">The **Permission** element defines the access that a user has to a folder.</span></span> 
  
```XML
<Permission>
   <CanCreateItems/>
   <CanCreateSubfolders/>
   <IsFolderOwner/>
   <IsFolderVisible/>
   <IsFolderContact/>
   <EditItems/>
   <DeleteItems/>
   <PermissionLevel/>
   <ReadItems/>
   <UserId/>
</Permission>
```

 <span data-ttu-id="6c897-105">**PermissionType**</span><span class="sxs-lookup"><span data-stu-id="6c897-105">**PermissionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6c897-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6c897-106">Attributes and elements</span></span>

<span data-ttu-id="6c897-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6c897-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6c897-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6c897-108">Attributes</span></span>

<span data-ttu-id="6c897-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6c897-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6c897-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6c897-110">Child elements</span></span>

|<span data-ttu-id="6c897-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="6c897-111">**Element**</span></span>|<span data-ttu-id="6c897-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6c897-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6c897-113">CanCreateItems</span><span class="sxs-lookup"><span data-stu-id="6c897-113">CanCreateItems</span></span>](cancreateitems.md) <br/> |<span data-ttu-id="6c897-114">Gibt an, ob ein Benutzer über die Berechtigung zum Erstellen von Elementen in einem Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="6c897-114">Indicates whether a user has permission to create items in a folder.</span></span> <span data-ttu-id="6c897-115">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6c897-115">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="6c897-116">CanCreateSubFolders</span><span class="sxs-lookup"><span data-stu-id="6c897-116">CanCreateSubFolders</span></span>](cancreatesubfolders.md) <br/> |<span data-ttu-id="6c897-117">Gibt an, ob ein Benutzer über die Berechtigung zum Erstellen von Unterordnern in einem Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="6c897-117">Indicates whether a user has permission to create subfolders in a folder.</span></span> <span data-ttu-id="6c897-118">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6c897-118">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="6c897-119">DeleteItems</span><span class="sxs-lookup"><span data-stu-id="6c897-119">DeleteItems</span></span>](deleteitems.md) <br/> |<span data-ttu-id="6c897-120">Gibt an, ob ein Benutzer über die Berechtigung zum Löschen von Elementen in einem Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="6c897-120">Indicates whether a user has permission to delete items in a folder.</span></span> <span data-ttu-id="6c897-121">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6c897-121">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="6c897-122">EditItems</span><span class="sxs-lookup"><span data-stu-id="6c897-122">EditItems</span></span>](edititems.md) <br/> |<span data-ttu-id="6c897-123">Gibt an, ob ein Benutzer über die Berechtigung zum Bearbeiten von Elementen in einem Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="6c897-123">Indicates whether a user has permission to edit items in a folder.</span></span> <span data-ttu-id="6c897-124">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6c897-124">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="6c897-125">IsFolderContact</span><span class="sxs-lookup"><span data-stu-id="6c897-125">IsFolderContact</span></span>](isfoldercontact.md) <br/> |<span data-ttu-id="6c897-126">Gibt an, ob ein Benutzer ein Kontakt für einen Ordner ist.</span><span class="sxs-lookup"><span data-stu-id="6c897-126">Indicates whether a user is a contact for a folder.</span></span> <span data-ttu-id="6c897-127">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6c897-127">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="6c897-128">IsFolderOwner</span><span class="sxs-lookup"><span data-stu-id="6c897-128">IsFolderOwner</span></span>](isfolderowner.md) <br/> |<span data-ttu-id="6c897-129">Gibt an, ob ein Benutzer der Besitzer eines Ordners ist.</span><span class="sxs-lookup"><span data-stu-id="6c897-129">Indicates whether a user is the owner of a folder.</span></span> <span data-ttu-id="6c897-130">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6c897-130">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="6c897-131">IsFolderVisible</span><span class="sxs-lookup"><span data-stu-id="6c897-131">IsFolderVisible</span></span>](isfoldervisible.md) <br/> |<span data-ttu-id="6c897-132">Gibt an, ob ein Benutzer einen Ordner anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="6c897-132">Indicates whether a user can view a folder.</span></span> <span data-ttu-id="6c897-133">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6c897-133">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="6c897-134">PermissionLevel</span><span class="sxs-lookup"><span data-stu-id="6c897-134">PermissionLevel</span></span>](permissionlevel.md) <br/> |<span data-ttu-id="6c897-135">Stellt die Kombination von Berechtigungen dar, die ein Benutzer für einen Ordner hat.</span><span class="sxs-lookup"><span data-stu-id="6c897-135">Represents the combination of permissions that a user has on a folder.</span></span> <span data-ttu-id="6c897-136">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6c897-136">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="6c897-137">ReadItems (PermissionType)</span><span class="sxs-lookup"><span data-stu-id="6c897-137">ReadItems (PermissionType)</span></span>](readitems-permissiontype.md) <br/> |<span data-ttu-id="6c897-138">Gibt an, ob ein Benutzer über die Berechtigung zum Lesen von Elementen in einem Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="6c897-138">Indicates whether a user has permission to read items within a folder.</span></span> <span data-ttu-id="6c897-139">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6c897-139">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="6c897-140">UserId</span><span class="sxs-lookup"><span data-stu-id="6c897-140">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="6c897-141">Identifiziert einen Stellvertreter Benutzer oder einen Benutzer, der über Ordnerzugriffsberechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="6c897-141">Identifies a delegate user or a user who has folder access permissions.</span></span> <span data-ttu-id="6c897-142">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6c897-142">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6c897-143">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6c897-143">Parent elements</span></span>

|<span data-ttu-id="6c897-144">**Element**</span><span class="sxs-lookup"><span data-stu-id="6c897-144">**Element**</span></span>|<span data-ttu-id="6c897-145">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6c897-145">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6c897-146">Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="6c897-146">Permissions</span></span>](permissions.md) <br/> |<span data-ttu-id="6c897-147">Enthält alle konfigurierten Berechtigungen für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="6c897-147">Contains all the configured permissions for a folder.</span></span> <span data-ttu-id="6c897-148">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6c897-148">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c897-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c897-149">Remarks</span></span>

<span data-ttu-id="6c897-150">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="6c897-150">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="6c897-151">Dieses Element wurde in Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6c897-151">This element was introduced in Exchange Server 2007 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="6c897-152">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="6c897-152">Version differences</span></span>

<span data-ttu-id="6c897-153">Für Anwendungen, die auf Exchange Online Zielen, Exchange Online im Rahmen von Office 365 oder einer lokalen Exchange-Version, die mit Exchange 2013 beginnt, werden Ordnerberechtigungen nicht zurückgegeben, wenn das [BaseShape](baseshape.md) -Element den Wert **allproperties** in der [GetFolder](getfolder-operation.md) -Vorgangsanforderung aufweist.</span><span class="sxs-lookup"><span data-stu-id="6c897-153">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="6c897-154">Zum Abrufen von Ordnerberechtigungen fügen Sie dem [AdditionalProperties](additionalproperties.md) -Element in der **GetFolder** -Anforderung das [PermissionSet-Element (permissionsettype)](permissionset-permissionsettype.md) hinzu.</span><span class="sxs-lookup"><span data-stu-id="6c897-154">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="6c897-155">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6c897-155">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6c897-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="6c897-156">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6c897-157">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6c897-157">Schema Name</span></span>  <br/> |<span data-ttu-id="6c897-158">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6c897-158">Types schema</span></span>  <br/> |
|<span data-ttu-id="6c897-159">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6c897-159">Validation File</span></span>  <br/> |<span data-ttu-id="6c897-160">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6c897-160">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6c897-161">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6c897-161">Can be Empty</span></span>  <br/> |<span data-ttu-id="6c897-162">False</span><span class="sxs-lookup"><span data-stu-id="6c897-162">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6c897-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c897-163">See also</span></span>



- [<span data-ttu-id="6c897-164">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6c897-164">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="6c897-165">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="6c897-165">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

