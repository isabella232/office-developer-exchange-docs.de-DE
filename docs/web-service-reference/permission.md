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
description: Das Permission-Element definiert den Zugriff, den ein Benutzer verfügt in einen Ordner.
ms.openlocfilehash: 600d60f481c4f1d407c3a39ab65d6ddcf46d04e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830735"
---
# <a name="permission"></a><span data-ttu-id="002fe-103">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="002fe-103">Permission</span></span>

<span data-ttu-id="002fe-104">Das **Permission** -Element definiert den Zugriff, den ein Benutzer verfügt in einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="002fe-104">The **Permission** element defines the access that a user has to a folder.</span></span> 
  
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

 <span data-ttu-id="002fe-105">**PermissionType**</span><span class="sxs-lookup"><span data-stu-id="002fe-105">**PermissionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="002fe-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="002fe-106">Attributes and elements</span></span>

<span data-ttu-id="002fe-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="002fe-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="002fe-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="002fe-108">Attributes</span></span>

<span data-ttu-id="002fe-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="002fe-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="002fe-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="002fe-110">Child elements</span></span>

|<span data-ttu-id="002fe-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="002fe-111">**Element**</span></span>|<span data-ttu-id="002fe-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="002fe-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="002fe-113">CanCreateItems</span><span class="sxs-lookup"><span data-stu-id="002fe-113">CanCreateItems</span></span>](cancreateitems.md) <br/> |<span data-ttu-id="002fe-114">Gibt an, ob ein Benutzer über die Berechtigung zum Erstellen von Elementen in einem Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="002fe-114">Indicates whether a user has permission to create items in a folder.</span></span> <span data-ttu-id="002fe-115">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="002fe-115">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="002fe-116">CanCreateSubFolders</span><span class="sxs-lookup"><span data-stu-id="002fe-116">CanCreateSubFolders</span></span>](cancreatesubfolders.md) <br/> |<span data-ttu-id="002fe-117">Gibt an, ob ein Benutzer die Berechtigung zum Erstellen von Unterordnern in einem Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="002fe-117">Indicates whether a user has permission to create subfolders in a folder.</span></span> <span data-ttu-id="002fe-118">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="002fe-118">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="002fe-119">DeleteItems</span><span class="sxs-lookup"><span data-stu-id="002fe-119">DeleteItems</span></span>](deleteitems.md) <br/> |<span data-ttu-id="002fe-120">Gibt an, ob ein Benutzer über die Berechtigung zum Löschen von Elementen in einem Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="002fe-120">Indicates whether a user has permission to delete items in a folder.</span></span> <span data-ttu-id="002fe-121">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="002fe-121">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="002fe-122">-Smarttagbereich</span><span class="sxs-lookup"><span data-stu-id="002fe-122">EditItems</span></span>](edititems.md) <br/> |<span data-ttu-id="002fe-123">Gibt an, ob ein Benutzer die Berechtigung zum Bearbeiten von Elementen in einem Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="002fe-123">Indicates whether a user has permission to edit items in a folder.</span></span> <span data-ttu-id="002fe-124">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="002fe-124">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="002fe-125">IsFolderContact</span><span class="sxs-lookup"><span data-stu-id="002fe-125">IsFolderContact</span></span>](isfoldercontact.md) <br/> |<span data-ttu-id="002fe-126">Gibt an, ob ein Benutzer einen Kontakt für einen Ordner ist.</span><span class="sxs-lookup"><span data-stu-id="002fe-126">Indicates whether a user is a contact for a folder.</span></span> <span data-ttu-id="002fe-127">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="002fe-127">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="002fe-128">IsFolderOwner</span><span class="sxs-lookup"><span data-stu-id="002fe-128">IsFolderOwner</span></span>](isfolderowner.md) <br/> |<span data-ttu-id="002fe-129">Gibt an, ob ein Benutzer den Besitzer eines Ordners ist.</span><span class="sxs-lookup"><span data-stu-id="002fe-129">Indicates whether a user is the owner of a folder.</span></span> <span data-ttu-id="002fe-130">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="002fe-130">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="002fe-131">IsFolderVisible</span><span class="sxs-lookup"><span data-stu-id="002fe-131">IsFolderVisible</span></span>](isfoldervisible.md) <br/> |<span data-ttu-id="002fe-132">Gibt an, ob ein Benutzer einen Ordner anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="002fe-132">Indicates whether a user can view a folder.</span></span> <span data-ttu-id="002fe-133">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="002fe-133">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="002fe-134">PermissionLevel</span><span class="sxs-lookup"><span data-stu-id="002fe-134">PermissionLevel</span></span>](permissionlevel.md) <br/> |<span data-ttu-id="002fe-135">Stellt die Kombination von Berechtigungen, mit denen ein Benutzer für einen Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="002fe-135">Represents the combination of permissions that a user has on a folder.</span></span> <span data-ttu-id="002fe-136">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="002fe-136">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="002fe-137">ReadItems (PermissionType)</span><span class="sxs-lookup"><span data-stu-id="002fe-137">ReadItems (PermissionType)</span></span>](readitems-permissiontype.md) <br/> |<span data-ttu-id="002fe-138">Gibt an, ob ein Benutzer über die Berechtigung zum Lesen von Elementen in einem Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="002fe-138">Indicates whether a user has permission to read items within a folder.</span></span> <span data-ttu-id="002fe-139">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="002fe-139">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="002fe-140">Benutzer-ID</span><span class="sxs-lookup"><span data-stu-id="002fe-140">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="002fe-141">Identifiziert ein Stellvertreter oder ein Benutzer mit Zugriffsberechtigungen für Ordner.</span><span class="sxs-lookup"><span data-stu-id="002fe-141">Identifies a delegate user or a user who has folder access permissions.</span></span> <span data-ttu-id="002fe-142">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="002fe-142">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="002fe-143">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="002fe-143">Parent elements</span></span>

|<span data-ttu-id="002fe-144">**Element**</span><span class="sxs-lookup"><span data-stu-id="002fe-144">**Element**</span></span>|<span data-ttu-id="002fe-145">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="002fe-145">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="002fe-146">Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="002fe-146">Permissions</span></span>](permissions.md) <br/> |<span data-ttu-id="002fe-147">Enthält die konfigurierten Berechtigungen für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="002fe-147">Contains all the configured permissions for a folder.</span></span> <span data-ttu-id="002fe-148">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="002fe-148">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="002fe-149">Hinweise</span><span class="sxs-lookup"><span data-stu-id="002fe-149">Remarks</span></span>

<span data-ttu-id="002fe-150">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="002fe-150">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="002fe-151">Dieses Element wurde in Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="002fe-151">This element was introduced in Exchange Server 2007 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="002fe-152">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="002fe-152">Version differences</span></span>

<span data-ttu-id="002fe-153">Für Applikationen werden, Exchange Online abzielen, Exchange Online als Teil von Office 365 oder eine lokale Version von Exchange beginnend mit Exchange 2013 Ordnerberechtigungen nicht zurückgegeben, wenn das Element [BaseShape](baseshape.md) **AllProperties** Wert hat in der Anforderung [GetFolder](getfolder-operation.md) -Vorgang.</span><span class="sxs-lookup"><span data-stu-id="002fe-153">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="002fe-154">Um Ordnerberechtigungen abzurufen, fügen Sie dem [AdditionalProperties](additionalproperties.md) -Element in der Anforderung **GetFolder** die [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) -Element hinzu.</span><span class="sxs-lookup"><span data-stu-id="002fe-154">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="002fe-155">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="002fe-155">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="002fe-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="002fe-156">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="002fe-157">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="002fe-157">Schema Name</span></span>  <br/> |<span data-ttu-id="002fe-158">Schematypen</span><span class="sxs-lookup"><span data-stu-id="002fe-158">Types schema</span></span>  <br/> |
|<span data-ttu-id="002fe-159">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="002fe-159">Validation File</span></span>  <br/> |<span data-ttu-id="002fe-160">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="002fe-160">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="002fe-161">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="002fe-161">Can be Empty</span></span>  <br/> |<span data-ttu-id="002fe-162">False</span><span class="sxs-lookup"><span data-stu-id="002fe-162">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="002fe-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="002fe-163">See also</span></span>



- [<span data-ttu-id="002fe-164">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="002fe-164">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="002fe-165">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="002fe-165">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

