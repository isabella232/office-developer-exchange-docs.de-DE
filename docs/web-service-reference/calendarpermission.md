---
title: CalendarPermission
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarPermission
api_type:
- schema
ms.assetid: 3aafb221-a04b-41f6-804e-eda810f1ba28
description: Das CalendarPermission-Element definiert den Zugriff, den ein Benutzer in einen Kalenderordner hat. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: c43f75e6cf5abc2dce9af6c04122ec9a589dcd58
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529476"
---
# <a name="calendarpermission"></a><span data-ttu-id="e83d2-104">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="e83d2-104">CalendarPermission</span></span>

<span data-ttu-id="e83d2-105">Das **CalendarPermission** -Element definiert den Zugriff, den ein Benutzer in einen Kalenderordner hat.</span><span class="sxs-lookup"><span data-stu-id="e83d2-105">The **CalendarPermission** element defines the access that a user has to a Calendar folder.</span></span> <span data-ttu-id="e83d2-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e83d2-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<Permission>
   <CalendarPermissionLevel/>
   <CanCreateItems/>
   <CanCreateSubfolders/>
   <IsFolderOwner/>
   <IsFolderVisible/>
   <IsFolderContact/>
   <EditItems/>
   <DeleteItems/>
   <ReadItems/>
   <UserId/>
</Permission>
```

 <span data-ttu-id="e83d2-107">**CalendarPermissionType**</span><span class="sxs-lookup"><span data-stu-id="e83d2-107">**CalendarPermissionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e83d2-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e83d2-108">Attributes and elements</span></span>

<span data-ttu-id="e83d2-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e83d2-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e83d2-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="e83d2-110">Attributes</span></span>

<span data-ttu-id="e83d2-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="e83d2-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e83d2-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e83d2-112">Child elements</span></span>

|<span data-ttu-id="e83d2-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e83d2-113">**Element**</span></span>|<span data-ttu-id="e83d2-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e83d2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e83d2-115">CalendarPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="e83d2-115">CalendarPermissionLevel</span></span>](calendarpermissionlevel.md) <br/> |<span data-ttu-id="e83d2-116">Stellt die Berechtigungsstufe dar, die ein Benutzer für einen Kalenderordner hat.</span><span class="sxs-lookup"><span data-stu-id="e83d2-116">Represents the permission level that a user has on a Calendar folder.</span></span> <span data-ttu-id="e83d2-117">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e83d2-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="e83d2-118">CanCreateItems</span><span class="sxs-lookup"><span data-stu-id="e83d2-118">CanCreateItems</span></span>](cancreateitems.md) <br/> |<span data-ttu-id="e83d2-119">Gibt an, ob ein Benutzer über die Berechtigung zum Erstellen von Elementen in einem Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="e83d2-119">Indicates whether a user has permission to create items in a folder.</span></span> <span data-ttu-id="e83d2-120">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e83d2-120">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="e83d2-121">CanCreateSubFolders</span><span class="sxs-lookup"><span data-stu-id="e83d2-121">CanCreateSubFolders</span></span>](cancreatesubfolders.md) <br/> |<span data-ttu-id="e83d2-122">Gibt an, ob ein Benutzer über die Berechtigung zum Erstellen von Unterordnern in einem Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="e83d2-122">Indicates whether a user has permission to create subfolders in a folder.</span></span> <span data-ttu-id="e83d2-123">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e83d2-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="e83d2-124">DeleteItems</span><span class="sxs-lookup"><span data-stu-id="e83d2-124">DeleteItems</span></span>](deleteitems.md) <br/> |<span data-ttu-id="e83d2-125">Gibt an, ob ein Benutzer über die Berechtigung zum Löschen von Elementen in einem Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="e83d2-125">Indicates whether a user has permission to delete items in a folder.</span></span> <span data-ttu-id="e83d2-126">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e83d2-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="e83d2-127">EditItems</span><span class="sxs-lookup"><span data-stu-id="e83d2-127">EditItems</span></span>](edititems.md) <br/> |<span data-ttu-id="e83d2-128">Gibt an, ob ein Benutzer über die Berechtigung zum Bearbeiten von Elementen in einem Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="e83d2-128">Indicates whether a user has permission to edit items in a folder.</span></span> <span data-ttu-id="e83d2-129">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e83d2-129">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="e83d2-130">IsFolderContact</span><span class="sxs-lookup"><span data-stu-id="e83d2-130">IsFolderContact</span></span>](isfoldercontact.md) <br/> |<span data-ttu-id="e83d2-131">Gibt an, ob ein Benutzer ein Kontakt für einen Ordner ist.</span><span class="sxs-lookup"><span data-stu-id="e83d2-131">Indicates whether a user is a contact for a folder.</span></span> <span data-ttu-id="e83d2-132">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e83d2-132">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="e83d2-133">IsFolderOwner</span><span class="sxs-lookup"><span data-stu-id="e83d2-133">IsFolderOwner</span></span>](isfolderowner.md) <br/> |<span data-ttu-id="e83d2-134">Gibt an, ob ein Benutzer der Besitzer eines Ordners ist.</span><span class="sxs-lookup"><span data-stu-id="e83d2-134">Indicates whether a user is the owner of a folder.</span></span> <span data-ttu-id="e83d2-135">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e83d2-135">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="e83d2-136">IsFolderVisible</span><span class="sxs-lookup"><span data-stu-id="e83d2-136">IsFolderVisible</span></span>](isfoldervisible.md) <br/> |<span data-ttu-id="e83d2-137">Gibt an, ob ein Benutzer einen Ordner anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="e83d2-137">Indicates whether a user can view a folder.</span></span> <span data-ttu-id="e83d2-138">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e83d2-138">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="e83d2-139">ReadItems (CalendarPermissionType)</span><span class="sxs-lookup"><span data-stu-id="e83d2-139">ReadItems (CalendarPermissionType)</span></span>](readitems-calendarpermissiontype.md) <br/> |<span data-ttu-id="e83d2-140">Gibt an, ob ein Benutzer über die Berechtigung zum Lesen von Elementen in einem Kalenderordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="e83d2-140">Indicates whether a user has permission to read items within a calendar folder.</span></span> <span data-ttu-id="e83d2-141">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e83d2-141">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="e83d2-142">UserId</span><span class="sxs-lookup"><span data-stu-id="e83d2-142">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="e83d2-143">Identifiziert einen Stellvertreter Benutzer oder einen Benutzer, der über Ordnerzugriffsberechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="e83d2-143">Identifies a delegate user or a user who has folder access permissions.</span></span> <span data-ttu-id="e83d2-144">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e83d2-144">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e83d2-145">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e83d2-145">Parent elements</span></span>

|<span data-ttu-id="e83d2-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="e83d2-146">**Element**</span></span>|<span data-ttu-id="e83d2-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e83d2-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e83d2-148">CalendarPermissions</span><span class="sxs-lookup"><span data-stu-id="e83d2-148">CalendarPermissions</span></span>](calendarpermissions.md) <br/> |<span data-ttu-id="e83d2-149">Enthält ein Array von Kalenderberechtigungen für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="e83d2-149">Contains an array of calendar permissions for a folder.</span></span> <span data-ttu-id="e83d2-150">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e83d2-150">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e83d2-151">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e83d2-151">Remarks</span></span>

<span data-ttu-id="e83d2-152">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="e83d2-152">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e83d2-153">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e83d2-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e83d2-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="e83d2-154">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e83d2-155">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e83d2-155">Schema Name</span></span>  <br/> |<span data-ttu-id="e83d2-156">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e83d2-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="e83d2-157">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e83d2-157">Validation File</span></span>  <br/> |<span data-ttu-id="e83d2-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e83d2-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e83d2-159">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e83d2-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="e83d2-160">False</span><span class="sxs-lookup"><span data-stu-id="e83d2-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e83d2-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e83d2-161">See also</span></span>



- [<span data-ttu-id="e83d2-162">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e83d2-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="e83d2-163">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="e83d2-163">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

