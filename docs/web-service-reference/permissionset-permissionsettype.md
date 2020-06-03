---
title: PermissionSet (permissionsettype)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PermissionSet
api_type:
- schema
ms.assetid: 6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d
description: Das PermissionSet-Element enthält alle Berechtigungen, die für einen Ordner konfiguriert sind.
ms.openlocfilehash: 5639ee8ba64742f39c0274f4e3aaa76d75bea42b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468131"
---
# <a name="permissionset-permissionsettype"></a><span data-ttu-id="96651-103">PermissionSet (permissionsettype)</span><span class="sxs-lookup"><span data-stu-id="96651-103">PermissionSet (PermissionSetType)</span></span>

<span data-ttu-id="96651-104">Das **PermissionSet** -Element enthält alle Berechtigungen, die für einen Ordner konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="96651-104">The **PermissionSet** element contains all the permissions that are configured for a folder.</span></span> 
  
```XML
<PermissionSet>
   <Permissions/>
   <UnknownEntries/>
</PermissionSet>
```

 <span data-ttu-id="96651-105">**Permissionsettype**</span><span class="sxs-lookup"><span data-stu-id="96651-105">**PermissionSetType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="96651-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="96651-106">Attributes and elements</span></span>

<span data-ttu-id="96651-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="96651-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="96651-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="96651-108">Attributes</span></span>

<span data-ttu-id="96651-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="96651-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="96651-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="96651-110">Child elements</span></span>

|<span data-ttu-id="96651-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="96651-111">**Element**</span></span>|<span data-ttu-id="96651-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="96651-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="96651-113">Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="96651-113">Permissions</span></span>](permissions.md) <br/> |<span data-ttu-id="96651-114">Enthält die Sammlung von Berechtigungen für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="96651-114">Contains the collection of permissions for a folder.</span></span> <span data-ttu-id="96651-115">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="96651-115">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="96651-116">UnknownEntries</span><span class="sxs-lookup"><span data-stu-id="96651-116">UnknownEntries</span></span>](unknownentries.md) <br/> |<span data-ttu-id="96651-117">Enthält ein Array von unbekannten Einträgen, die nicht für den Active Directory Verzeichnisdienst aufgelöst werden können.</span><span class="sxs-lookup"><span data-stu-id="96651-117">Contains an array of unknown entries that cannot be resolved against the Active Directory directory service.</span></span> <span data-ttu-id="96651-118">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="96651-118">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="96651-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="96651-119">Parent elements</span></span>

|<span data-ttu-id="96651-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="96651-120">**Element**</span></span>|<span data-ttu-id="96651-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="96651-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="96651-122">Folder</span><span class="sxs-lookup"><span data-stu-id="96651-122">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="96651-123">Definiert einen Ordner zum Erstellen, abrufen, suchen, synchronisieren oder aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="96651-123">Defines a folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="96651-124">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="96651-124">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="96651-125">Stellt einen Suchordner dar, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="96651-125">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="96651-126">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="96651-126">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="96651-127">Stellt einen Kontakteordner dar, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="96651-127">Represents a contacts folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="96651-128">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="96651-128">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="96651-129">Stellt einen Aufgabenordner dar, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="96651-129">Represents a tasks folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96651-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96651-130">Remarks</span></span>

<span data-ttu-id="96651-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="96651-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="96651-132">Dieses Element wurde in Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="96651-132">This element was introduced in Exchange Server 2007 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="96651-133">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="96651-133">Version differences</span></span>

<span data-ttu-id="96651-134">Für Anwendungen, die auf Exchange Online Zielen, Exchange Online im Rahmen von Office 365 oder einer lokalen Exchange-Version, die mit Exchange 2013 beginnt, werden Ordnerberechtigungen nicht zurückgegeben, wenn das [BaseShape](baseshape.md) -Element den Wert **allproperties** in der [GetFolder](getfolder-operation.md) -Vorgangsanforderung aufweist.</span><span class="sxs-lookup"><span data-stu-id="96651-134">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="96651-135">Zum Abrufen von Ordnerberechtigungen fügen Sie dem [AdditionalProperties](additionalproperties.md) -Element in der **GetFolder** -Anforderung das [PermissionSet-Element (permissionsettype)](permissionset-permissionsettype.md) hinzu.</span><span class="sxs-lookup"><span data-stu-id="96651-135">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="96651-136">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="96651-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="96651-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="96651-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="96651-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="96651-138">Schema Name</span></span>  <br/> |<span data-ttu-id="96651-139">Schematypen</span><span class="sxs-lookup"><span data-stu-id="96651-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="96651-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="96651-140">Validation File</span></span>  <br/> |<span data-ttu-id="96651-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="96651-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="96651-142">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="96651-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="96651-143">False</span><span class="sxs-lookup"><span data-stu-id="96651-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="96651-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96651-144">See also</span></span>



- [<span data-ttu-id="96651-145">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="96651-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="96651-146">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="96651-146">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

