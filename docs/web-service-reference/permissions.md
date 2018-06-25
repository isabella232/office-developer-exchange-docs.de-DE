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
description: Das Permissions-Element enthält die Auflistung der Berechtigungen für einen Ordner.
ms.openlocfilehash: 08d015c3b1afb58fce0fb4b99466965cc5c29fc6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830727"
---
# <a name="permissions"></a><span data-ttu-id="2393b-103">Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="2393b-103">Permissions</span></span>

<span data-ttu-id="2393b-104">Das **Permissions** -Element enthält die Auflistung der Berechtigungen für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="2393b-104">The **Permissions** element contains the collection of permissions for a folder.</span></span> 
  
```XML
<Permissions>
   <Permission/>
</Permissions>
```

 <span data-ttu-id="2393b-105">**PermissionType**</span><span class="sxs-lookup"><span data-stu-id="2393b-105">**PermissionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2393b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2393b-106">Attributes and elements</span></span>

<span data-ttu-id="2393b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2393b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2393b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2393b-108">Attributes</span></span>

<span data-ttu-id="2393b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2393b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2393b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2393b-110">Child elements</span></span>

|<span data-ttu-id="2393b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="2393b-111">**Element**</span></span>|<span data-ttu-id="2393b-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2393b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2393b-113">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="2393b-113">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="2393b-114">Definiert den Zugriff, den eine Stellvertretung hat in einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="2393b-114">Defines the access that a delegate has to a folder.</span></span> <span data-ttu-id="2393b-115">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2393b-115">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2393b-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2393b-116">Parent elements</span></span>

|<span data-ttu-id="2393b-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="2393b-117">**Element**</span></span>|<span data-ttu-id="2393b-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2393b-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2393b-119">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="2393b-119">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="2393b-120">Enthält alle Berechtigungen, die für einen Ordner konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="2393b-120">Contains all the permissions that are configured for a folder.</span></span> <span data-ttu-id="2393b-121">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2393b-121">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2393b-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2393b-122">Remarks</span></span>

<span data-ttu-id="2393b-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2393b-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="2393b-124">Dieses Element wurde in Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2393b-124">This element was introduced in Exchange Server 2007 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="2393b-125">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="2393b-125">Version differences</span></span>

<span data-ttu-id="2393b-126">Für Applikationen werden, Exchange Online abzielen, Exchange Online als Teil von Office 365 oder eine lokale Version von Exchange beginnend mit Exchange 2013 Ordnerberechtigungen nicht zurückgegeben, wenn das Element [BaseShape](baseshape.md) **AllProperties** Wert hat in der Anforderung [GetFolder](getfolder-operation.md) -Vorgang.</span><span class="sxs-lookup"><span data-stu-id="2393b-126">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="2393b-127">Um Ordnerberechtigungen abzurufen, fügen Sie dem [AdditionalProperties](additionalproperties.md) -Element in der Anforderung **GetFolder** die [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) -Element hinzu.</span><span class="sxs-lookup"><span data-stu-id="2393b-127">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="2393b-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2393b-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2393b-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="2393b-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2393b-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2393b-130">Schema Name</span></span>  <br/> |<span data-ttu-id="2393b-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="2393b-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="2393b-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2393b-132">Validation File</span></span>  <br/> |<span data-ttu-id="2393b-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2393b-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2393b-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2393b-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="2393b-135">False</span><span class="sxs-lookup"><span data-stu-id="2393b-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2393b-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2393b-136">See also</span></span>



- [<span data-ttu-id="2393b-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2393b-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="2393b-138">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="2393b-138">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

