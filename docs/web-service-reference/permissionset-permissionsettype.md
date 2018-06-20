---
title: PermissionSet (PermissionSetType)
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
description: PermissionSet-Element enthält alle Berechtigungen, die für einen Ordner konfiguriert sind.
ms.openlocfilehash: 0fa0ac78a0db2bf382ad413cbb8bd072aa88c6fb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830732"
---
# <a name="permissionset-permissionsettype"></a><span data-ttu-id="6773e-103">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="6773e-103">PermissionSet (PermissionSetType)</span></span>

<span data-ttu-id="6773e-104">**PermissionSet** -Element enthält alle Berechtigungen, die für einen Ordner konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="6773e-104">The **PermissionSet** element contains all the permissions that are configured for a folder.</span></span> 
  
```XML
<PermissionSet>
   <Permissions/>
   <UnknownEntries/>
</PermissionSet>
```

 <span data-ttu-id="6773e-105">**PermissionSetType**</span><span class="sxs-lookup"><span data-stu-id="6773e-105">**PermissionSetType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6773e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6773e-106">Attributes and elements</span></span>

<span data-ttu-id="6773e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6773e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6773e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6773e-108">Attributes</span></span>

<span data-ttu-id="6773e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6773e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6773e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6773e-110">Child elements</span></span>

|<span data-ttu-id="6773e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="6773e-111">**Element**</span></span>|<span data-ttu-id="6773e-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6773e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6773e-113">Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="6773e-113">Permissions</span></span>](permissions.md) <br/> |<span data-ttu-id="6773e-114">Enthält die Auflistung von Berechtigungen für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="6773e-114">Contains the collection of permissions for a folder.</span></span> <span data-ttu-id="6773e-115">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6773e-115">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="6773e-116">UnknownEntries</span><span class="sxs-lookup"><span data-stu-id="6773e-116">UnknownEntries</span></span>](unknownentries.md) <br/> |<span data-ttu-id="6773e-117">Enthält ein Array von unbekannten Einträgen, die gegen den Verzeichnisdienst Active Directory nicht aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="6773e-117">Contains an array of unknown entries that cannot be resolved against the Active Directory directory service.</span></span> <span data-ttu-id="6773e-118">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6773e-118">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6773e-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6773e-119">Parent elements</span></span>

|<span data-ttu-id="6773e-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="6773e-120">**Element**</span></span>|<span data-ttu-id="6773e-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6773e-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6773e-122">Folder</span><span class="sxs-lookup"><span data-stu-id="6773e-122">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="6773e-123">Definiert einen Ordner erstellen, abrufen, suchen, synchronisieren oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6773e-123">Defines a folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="6773e-124">"SearchFolder"</span><span class="sxs-lookup"><span data-stu-id="6773e-124">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="6773e-125">Stellt einen Suchordner, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="6773e-125">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="6773e-126">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="6773e-126">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="6773e-127">Stellt einen Kontakteordner, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="6773e-127">Represents a contacts folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="6773e-128">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="6773e-128">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="6773e-129">Stellt einen Aufgabenordner, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="6773e-129">Represents a tasks folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6773e-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6773e-130">Remarks</span></span>

<span data-ttu-id="6773e-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="6773e-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="6773e-132">Dieses Element wurde in Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6773e-132">This element was introduced in Exchange Server 2007 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="6773e-133">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="6773e-133">Version differences</span></span>

<span data-ttu-id="6773e-134">Für Applikationen werden, Exchange Online abzielen, Exchange Online als Teil von Office 365 oder eine lokale Version von Exchange beginnend mit Exchange 2013 Ordnerberechtigungen nicht zurückgegeben, wenn das Element [BaseShape](baseshape.md) **AllProperties** Wert hat in der Anforderung [GetFolder](getfolder-operation.md) -Vorgang.</span><span class="sxs-lookup"><span data-stu-id="6773e-134">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="6773e-135">Um Ordnerberechtigungen abzurufen, fügen Sie dem [AdditionalProperties](additionalproperties.md) -Element in der Anforderung **GetFolder** die [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) -Element hinzu.</span><span class="sxs-lookup"><span data-stu-id="6773e-135">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="6773e-136">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6773e-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6773e-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="6773e-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6773e-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6773e-138">Schema Name</span></span>  <br/> |<span data-ttu-id="6773e-139">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6773e-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="6773e-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6773e-140">Validation File</span></span>  <br/> |<span data-ttu-id="6773e-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6773e-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6773e-142">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6773e-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="6773e-143">False</span><span class="sxs-lookup"><span data-stu-id="6773e-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6773e-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6773e-144">See also</span></span>



- [<span data-ttu-id="6773e-145">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6773e-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="6773e-146">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="6773e-146">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

