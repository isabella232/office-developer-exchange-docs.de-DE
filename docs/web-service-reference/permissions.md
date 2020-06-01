---
title: Berechtigungen
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Permissions
api_type:
- schema
ms.assetid: 2ba50bd9-819f-4e5f-a3bb-85a0a87d8a86
description: Das Permissions-Element enthält die Auflistung von Berechtigungen für einen Ordner.
ms.openlocfilehash: b8616cefdb8c453106753fb0788a6c7d6a0ded79
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459216"
---
# <a name="permissions"></a><span data-ttu-id="f8005-103">Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="f8005-103">Permissions</span></span>

<span data-ttu-id="f8005-104">Das **Permissions** -Element enthält die Auflistung von Berechtigungen für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="f8005-104">The **Permissions** element contains the collection of permissions for a folder.</span></span> 
  
```XML
<Permissions>
   <Permission/>
</Permissions>
```

 <span data-ttu-id="f8005-105">**PermissionType**</span><span class="sxs-lookup"><span data-stu-id="f8005-105">**PermissionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f8005-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f8005-106">Attributes and elements</span></span>

<span data-ttu-id="f8005-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f8005-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f8005-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f8005-108">Attributes</span></span>

<span data-ttu-id="f8005-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f8005-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f8005-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f8005-110">Child elements</span></span>

|<span data-ttu-id="f8005-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f8005-111">**Element**</span></span>|<span data-ttu-id="f8005-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f8005-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f8005-113">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="f8005-113">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="f8005-114">Definiert den Zugriff, den ein Delegat in einen Ordner hat.</span><span class="sxs-lookup"><span data-stu-id="f8005-114">Defines the access that a delegate has to a folder.</span></span> <span data-ttu-id="f8005-115">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f8005-115">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f8005-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f8005-116">Parent elements</span></span>

|<span data-ttu-id="f8005-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="f8005-117">**Element**</span></span>|<span data-ttu-id="f8005-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f8005-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f8005-119">PermissionSet (permissionsettype)</span><span class="sxs-lookup"><span data-stu-id="f8005-119">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="f8005-120">Enthält alle Berechtigungen, die für einen Ordner konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="f8005-120">Contains all the permissions that are configured for a folder.</span></span> <span data-ttu-id="f8005-121">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f8005-121">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8005-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8005-122">Remarks</span></span>

<span data-ttu-id="f8005-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f8005-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="f8005-124">Dieses Element wurde in Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f8005-124">This element was introduced in Exchange Server 2007 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="f8005-125">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="f8005-125">Version differences</span></span>

<span data-ttu-id="f8005-126">Für Anwendungen, die auf Exchange Online Zielen, Exchange Online im Rahmen von Office 365 oder einer lokalen Exchange-Version, die mit Exchange 2013 beginnt, werden Ordnerberechtigungen nicht zurückgegeben, wenn das [BaseShape](baseshape.md) -Element den Wert **allproperties** in der [GetFolder](getfolder-operation.md) -Vorgangsanforderung aufweist.</span><span class="sxs-lookup"><span data-stu-id="f8005-126">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="f8005-127">Zum Abrufen von Ordnerberechtigungen fügen Sie dem [AdditionalProperties](additionalproperties.md) -Element in der **GetFolder** -Anforderung das [PermissionSet-Element (permissionsettype)](permissionset-permissionsettype.md) hinzu.</span><span class="sxs-lookup"><span data-stu-id="f8005-127">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="f8005-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f8005-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f8005-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="f8005-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f8005-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f8005-130">Schema Name</span></span>  <br/> |<span data-ttu-id="f8005-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f8005-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="f8005-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f8005-132">Validation File</span></span>  <br/> |<span data-ttu-id="f8005-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f8005-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f8005-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f8005-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="f8005-135">False</span><span class="sxs-lookup"><span data-stu-id="f8005-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f8005-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8005-136">See also</span></span>



- [<span data-ttu-id="f8005-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f8005-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="f8005-138">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="f8005-138">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

