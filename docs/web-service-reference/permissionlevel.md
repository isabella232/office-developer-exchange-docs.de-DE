---
title: PermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PermissionLevel
api_type:
- schema
ms.assetid: 87978600-3523-451e-a725-ef092c543e2a
description: Das PermissionLevel-Element stellt die Berechtigungsstufe dar, die ein Benutzer für einen Ordner hat. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: e1e441c53b5c40c16051eb852a6b35a8af7476e2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458040"
---
# <a name="permissionlevel"></a><span data-ttu-id="6e0b2-104">PermissionLevel</span><span class="sxs-lookup"><span data-stu-id="6e0b2-104">PermissionLevel</span></span>

<span data-ttu-id="6e0b2-105">Das **PermissionLevel** -Element stellt die Berechtigungsstufe dar, die ein Benutzer für einen Ordner hat.</span><span class="sxs-lookup"><span data-stu-id="6e0b2-105">The **PermissionLevel** element represents the permission level that a user has on a folder.</span></span> <span data-ttu-id="6e0b2-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6e0b2-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<PermissionLevel>None or Owner or PublishingEditor or Editor or PublishingAuthor or Author or NoneditingAuthor or Reviewer or Contributor or Custom</PermissionLevel>
```

 <span data-ttu-id="6e0b2-107">**PermissionLevelType**</span><span class="sxs-lookup"><span data-stu-id="6e0b2-107">**PermissionLevelType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6e0b2-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6e0b2-108">Attributes and elements</span></span>

<span data-ttu-id="6e0b2-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6e0b2-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6e0b2-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="6e0b2-110">Attributes</span></span>

<span data-ttu-id="6e0b2-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="6e0b2-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6e0b2-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6e0b2-112">Child elements</span></span>

<span data-ttu-id="6e0b2-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="6e0b2-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6e0b2-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6e0b2-114">Parent elements</span></span>

|<span data-ttu-id="6e0b2-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="6e0b2-115">**Element**</span></span>|<span data-ttu-id="6e0b2-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6e0b2-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6e0b2-117">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="6e0b2-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="6e0b2-p103">Definiert den Zugriff, den ein Benutzer verfügt in einen Ordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6e0b2-p103">Defines the access that a user has to a folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6e0b2-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="6e0b2-120">Text value</span></span>

<span data-ttu-id="6e0b2-121">In der folgenden Tabelle sind die möglichen Werte für das **PermissionLevel** -Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6e0b2-121">The following table lists the possible values for the **PermissionLevel** element.</span></span> 
  
<span data-ttu-id="6e0b2-122">**PermissionLevel-Element Text Werte**</span><span class="sxs-lookup"><span data-stu-id="6e0b2-122">**PermissionLevel element text values**</span></span>

|<span data-ttu-id="6e0b2-123">**Wert**</span><span class="sxs-lookup"><span data-stu-id="6e0b2-123">**Value**</span></span>|<span data-ttu-id="6e0b2-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6e0b2-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6e0b2-125">Keine</span><span class="sxs-lookup"><span data-stu-id="6e0b2-125">None</span></span>  <br/> |<span data-ttu-id="6e0b2-126">Gibt an, dass der Benutzer über keine Berechtigungen für den Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="6e0b2-126">Indicates that the user has no permissions on the folder.</span></span>  <br/> |
|<span data-ttu-id="6e0b2-127">Besitzer</span><span class="sxs-lookup"><span data-stu-id="6e0b2-127">Owner</span></span>  <br/> |<span data-ttu-id="6e0b2-128">Gibt an, dass der Benutzer alle Elemente im Ordner erstellen, lesen, bearbeiten und löschen und Unterordner erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="6e0b2-128">Indicates that the user can create, read, edit, and delete all items in the folder, and create subfolders.</span></span> <span data-ttu-id="6e0b2-129">Der Benutzer ist sowohl Ordnerbesitzer als auch Ordner Kontakt.</span><span class="sxs-lookup"><span data-stu-id="6e0b2-129">The user is both folder owner and folder contact.</span></span>  <br/> |
|<span data-ttu-id="6e0b2-130">Publishing Editor</span><span class="sxs-lookup"><span data-stu-id="6e0b2-130">PublishingEditor</span></span>  <br/> |<span data-ttu-id="6e0b2-131">Gibt an, dass der Benutzer alle Elemente im Ordner erstellen, lesen, bearbeiten und löschen und Unterordner erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="6e0b2-131">Indicates that the user can create, read, edit, and delete all items in the folder, and create subfolders.</span></span>  <br/> |
|<span data-ttu-id="6e0b2-132">Editor</span><span class="sxs-lookup"><span data-stu-id="6e0b2-132">Editor</span></span>  <br/> |<span data-ttu-id="6e0b2-133">Gibt an, dass der Benutzer alle Elemente im Ordner erstellen, lesen, bearbeiten und löschen kann.</span><span class="sxs-lookup"><span data-stu-id="6e0b2-133">Indicates that the user can create, read, edit, and delete all items in the folder.</span></span>  <br/> |
|<span data-ttu-id="6e0b2-134">PublishingAuthor</span><span class="sxs-lookup"><span data-stu-id="6e0b2-134">PublishingAuthor</span></span>  <br/> |<span data-ttu-id="6e0b2-135">Gibt an, dass der Benutzer alle Elemente im Ordner erstellen und lesen, nur vom Benutzer erstellte Elemente bearbeiten und löschen sowie Unterordner erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="6e0b2-135">Indicates that the user can create and read all items in the folder, edit and delete only items that the user creates, and create subfolders.</span></span>  <br/> |
|<span data-ttu-id="6e0b2-136">Ursprung</span><span class="sxs-lookup"><span data-stu-id="6e0b2-136">Author</span></span>  <br/> |<span data-ttu-id="6e0b2-137">Gibt an, dass der Benutzer alle Elemente im Ordner erstellen und lesen kann, und nur vom Benutzer erstellte Elemente bearbeiten und löschen können.</span><span class="sxs-lookup"><span data-stu-id="6e0b2-137">Indicates that the user can create and read all items in the folder, and edit and delete only items that the user creates.</span></span>  <br/> |
|<span data-ttu-id="6e0b2-138">Noneditingauthorcreateitems</span><span class="sxs-lookup"><span data-stu-id="6e0b2-138">NoneditingAuthor</span></span>  <br/> |<span data-ttu-id="6e0b2-139">Gibt an, dass der Benutzer alle Elemente im Ordner erstellen und lesen und nur vom Benutzer erstellte Elemente löschen kann.</span><span class="sxs-lookup"><span data-stu-id="6e0b2-139">Indicates that the user can create and read all items in the folder, and delete only items that the user creates.</span></span>  <br/> |
|<span data-ttu-id="6e0b2-140">Reviewer</span><span class="sxs-lookup"><span data-stu-id="6e0b2-140">Reviewer</span></span>  <br/> |<span data-ttu-id="6e0b2-141">Gibt an, dass der Benutzer alle Elemente im Ordner lesen kann.</span><span class="sxs-lookup"><span data-stu-id="6e0b2-141">Indicates that the user can read all items in the folder.</span></span>  <br/> |
|<span data-ttu-id="6e0b2-142">Contributor</span><span class="sxs-lookup"><span data-stu-id="6e0b2-142">Contributor</span></span>  <br/> |<span data-ttu-id="6e0b2-143">Gibt an, dass der Benutzer Elemente im Ordner erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="6e0b2-143">Indicates that the user can create items in the folder.</span></span> <span data-ttu-id="6e0b2-144">Der Inhalt des Ordners wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6e0b2-144">The contents of the folder do not appear.</span></span>  <br/> |
|<span data-ttu-id="6e0b2-145">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="6e0b2-145">Custom</span></span>  <br/> |<span data-ttu-id="6e0b2-146">Gibt an, dass der Benutzer benutzerdefinierte Zugriffsberechtigungen für den Ordner besitzt.</span><span class="sxs-lookup"><span data-stu-id="6e0b2-146">Indicates that the user has custom access permissions on the folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e0b2-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e0b2-147">Remarks</span></span>

<span data-ttu-id="6e0b2-148">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="6e0b2-148">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6e0b2-149">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6e0b2-149">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6e0b2-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="6e0b2-150">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6e0b2-151">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6e0b2-151">Schema Name</span></span>  <br/> |<span data-ttu-id="6e0b2-152">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6e0b2-152">Types schema</span></span>  <br/> |
|<span data-ttu-id="6e0b2-153">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6e0b2-153">Validation File</span></span>  <br/> |<span data-ttu-id="6e0b2-154">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6e0b2-154">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6e0b2-155">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6e0b2-155">Can be Empty</span></span>  <br/> |<span data-ttu-id="6e0b2-156">False</span><span class="sxs-lookup"><span data-stu-id="6e0b2-156">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6e0b2-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e0b2-157">See also</span></span>



- [<span data-ttu-id="6e0b2-158">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6e0b2-158">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="6e0b2-159">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="6e0b2-159">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

