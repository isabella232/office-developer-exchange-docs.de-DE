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
description: Das PermissionLevel-Element darstellt, die Berechtigungsstufe, die ein Benutzer für einen Ordner verfügt. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 7cc734f5807fe039467065315c220341f47d3fb4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830730"
---
# <a name="permissionlevel"></a><span data-ttu-id="37cac-104">PermissionLevel</span><span class="sxs-lookup"><span data-stu-id="37cac-104">PermissionLevel</span></span>

<span data-ttu-id="37cac-105">Das **PermissionLevel** -Element darstellt, die Berechtigungsstufe, die ein Benutzer für einen Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="37cac-105">The **PermissionLevel** element represents the permission level that a user has on a folder.</span></span> <span data-ttu-id="37cac-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="37cac-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<PermissionLevel>None or Owner or PublishingEditor or Editor or PublishingAuthor or Author or NoneditingAuthor or Reviewer or Contributor or Custom</PermissionLevel>
```

 <span data-ttu-id="37cac-107">**PermissionLevelType**</span><span class="sxs-lookup"><span data-stu-id="37cac-107">**PermissionLevelType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="37cac-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="37cac-108">Attributes and elements</span></span>

<span data-ttu-id="37cac-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="37cac-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="37cac-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="37cac-110">Attributes</span></span>

<span data-ttu-id="37cac-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="37cac-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="37cac-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="37cac-112">Child elements</span></span>

<span data-ttu-id="37cac-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="37cac-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="37cac-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="37cac-114">Parent elements</span></span>

|<span data-ttu-id="37cac-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="37cac-115">**Element**</span></span>|<span data-ttu-id="37cac-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="37cac-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="37cac-117">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="37cac-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="37cac-p103">Definiert den Zugriff, den ein Benutzer verfügt in einen Ordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="37cac-p103">Defines the access that a user has to a folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="37cac-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="37cac-120">Text value</span></span>

<span data-ttu-id="37cac-121">Die folgende Tabelle enthält die möglichen Werte für das **PermissionLevel** -Element.</span><span class="sxs-lookup"><span data-stu-id="37cac-121">The following table lists the possible values for the **PermissionLevel** element.</span></span> 
  
<span data-ttu-id="37cac-122">**Text-Elementwerte PermissionLevel**</span><span class="sxs-lookup"><span data-stu-id="37cac-122">**PermissionLevel element text values**</span></span>

|<span data-ttu-id="37cac-123">**Wert**</span><span class="sxs-lookup"><span data-stu-id="37cac-123">**Value**</span></span>|<span data-ttu-id="37cac-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="37cac-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="37cac-125">Keine</span><span class="sxs-lookup"><span data-stu-id="37cac-125">None</span></span>  <br/> |<span data-ttu-id="37cac-126">Gibt an, dass der Benutzer keine Berechtigungen für den Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="37cac-126">Indicates that the user has no permissions on the folder.</span></span>  <br/> |
|<span data-ttu-id="37cac-127">Besitzer</span><span class="sxs-lookup"><span data-stu-id="37cac-127">Owner</span></span>  <br/> |<span data-ttu-id="37cac-128">Gibt an, dass der Benutzer kann erstellen, lesen, bearbeiten und löschen alle Elemente im Ordner und Unterordner erstellen.</span><span class="sxs-lookup"><span data-stu-id="37cac-128">Indicates that the user can create, read, edit, and delete all items in the folder, and create subfolders.</span></span> <span data-ttu-id="37cac-129">Der Benutzer ist Besitzer des Ordners und Ordner Kontakt.</span><span class="sxs-lookup"><span data-stu-id="37cac-129">The user is both folder owner and folder contact.</span></span>  <br/> |
|<span data-ttu-id="37cac-130">Vom Typ PublishingEditor</span><span class="sxs-lookup"><span data-stu-id="37cac-130">PublishingEditor</span></span>  <br/> |<span data-ttu-id="37cac-131">Gibt an, dass der Benutzer kann erstellen, lesen, bearbeiten und löschen alle Elemente im Ordner und Unterordner erstellen.</span><span class="sxs-lookup"><span data-stu-id="37cac-131">Indicates that the user can create, read, edit, and delete all items in the folder, and create subfolders.</span></span>  <br/> |
|<span data-ttu-id="37cac-132">Herausgeber</span><span class="sxs-lookup"><span data-stu-id="37cac-132">Editor</span></span>  <br/> |<span data-ttu-id="37cac-133">Gibt an, dass der Benutzer erstellen, lesen, bearbeiten und löschen alle Elemente im Ordner.</span><span class="sxs-lookup"><span data-stu-id="37cac-133">Indicates that the user can create, read, edit, and delete all items in the folder.</span></span>  <br/> |
|<span data-ttu-id="37cac-134">PublishingAuthor</span><span class="sxs-lookup"><span data-stu-id="37cac-134">PublishingAuthor</span></span>  <br/> |<span data-ttu-id="37cac-135">Gibt an, dass der Benutzer kann erstellen und Lesen aller Elemente im Ordner, bearbeiten und Löschen nur Elemente, die der Benutzer erstellt und Unterordner erstellen.</span><span class="sxs-lookup"><span data-stu-id="37cac-135">Indicates that the user can create and read all items in the folder, edit and delete only items that the user creates, and create subfolders.</span></span>  <br/> |
|<span data-ttu-id="37cac-136">Autor</span><span class="sxs-lookup"><span data-stu-id="37cac-136">Author</span></span>  <br/> |<span data-ttu-id="37cac-137">Gibt an, dass der Benutzer erstellen und aller Elemente in den Ordner lesen und bearbeiten und löschen kann nur Elemente, die der Benutzer erstellt.</span><span class="sxs-lookup"><span data-stu-id="37cac-137">Indicates that the user can create and read all items in the folder, and edit and delete only items that the user creates.</span></span>  <br/> |
|<span data-ttu-id="37cac-138">NoneditingAuthor</span><span class="sxs-lookup"><span data-stu-id="37cac-138">NoneditingAuthor</span></span>  <br/> |<span data-ttu-id="37cac-139">Gibt an, dass der Benutzer kann erstellen und alle Elemente im Ordner lesen und nur Elemente löschen, die der Benutzer erstellt.</span><span class="sxs-lookup"><span data-stu-id="37cac-139">Indicates that the user can create and read all items in the folder, and delete only items that the user creates.</span></span>  <br/> |
|<span data-ttu-id="37cac-140">Prüfer</span><span class="sxs-lookup"><span data-stu-id="37cac-140">Reviewer</span></span>  <br/> |<span data-ttu-id="37cac-141">Gibt an, dass der Benutzer alle Elemente im Ordner lesen kann.</span><span class="sxs-lookup"><span data-stu-id="37cac-141">Indicates that the user can read all items in the folder.</span></span>  <br/> |
|<span data-ttu-id="37cac-142">Mitwirkender</span><span class="sxs-lookup"><span data-stu-id="37cac-142">Contributor</span></span>  <br/> |<span data-ttu-id="37cac-143">Gibt an, dass der Benutzer Elemente im Ordner erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="37cac-143">Indicates that the user can create items in the folder.</span></span> <span data-ttu-id="37cac-144">Der Inhalt des Ordners wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="37cac-144">The contents of the folder do not appear.</span></span>  <br/> |
|<span data-ttu-id="37cac-145">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="37cac-145">Custom</span></span>  <br/> |<span data-ttu-id="37cac-146">Gibt an, dass der Benutzer benutzerdefinierte Zugriffsberechtigungen für den Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="37cac-146">Indicates that the user has custom access permissions on the folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37cac-147">Hinweise</span><span class="sxs-lookup"><span data-stu-id="37cac-147">Remarks</span></span>

<span data-ttu-id="37cac-148">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="37cac-148">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="37cac-149">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="37cac-149">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="37cac-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="37cac-150">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="37cac-151">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="37cac-151">Schema Name</span></span>  <br/> |<span data-ttu-id="37cac-152">Schematypen</span><span class="sxs-lookup"><span data-stu-id="37cac-152">Types schema</span></span>  <br/> |
|<span data-ttu-id="37cac-153">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="37cac-153">Validation File</span></span>  <br/> |<span data-ttu-id="37cac-154">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="37cac-154">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="37cac-155">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="37cac-155">Can be Empty</span></span>  <br/> |<span data-ttu-id="37cac-156">False</span><span class="sxs-lookup"><span data-stu-id="37cac-156">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="37cac-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37cac-157">See also</span></span>



- [<span data-ttu-id="37cac-158">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="37cac-158">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="37cac-159">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="37cac-159">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

