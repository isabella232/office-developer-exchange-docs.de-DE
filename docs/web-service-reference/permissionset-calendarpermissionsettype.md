---
title: PermissionSet (CalendarPermissionSetType)
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
ms.assetid: 75f20033-85eb-4627-b4f8-be85e4889e96
description: PermissionSet-Element enthält alle Berechtigungen, die für einen Kalenderordner konfiguriert sind.
ms.openlocfilehash: b2e642fd2ee8ded4d0d4c67509a5587f7b1efa8a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830728"
---
# <a name="permissionset-calendarpermissionsettype"></a><span data-ttu-id="84e45-103">PermissionSet (CalendarPermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="84e45-103">PermissionSet (CalendarPermissionSetType)</span></span>

<span data-ttu-id="84e45-104">**PermissionSet** -Element enthält alle Berechtigungen, die für einen Kalenderordner konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="84e45-104">The **PermissionSet** element contains all the permissions that are configured for a calendar folder.</span></span> 
  
```XML
<PermissionSet>
   <CalendarPermissions/>
   <UnknownEntries/>
</PermissionSet>
```

 <span data-ttu-id="84e45-105">**CalendarPermissonSetType**</span><span class="sxs-lookup"><span data-stu-id="84e45-105">**CalendarPermissonSetType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="84e45-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="84e45-106">Attributes and elements</span></span>

<span data-ttu-id="84e45-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="84e45-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="84e45-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="84e45-108">Attributes</span></span>

<span data-ttu-id="84e45-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="84e45-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="84e45-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="84e45-110">Child elements</span></span>

|<span data-ttu-id="84e45-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="84e45-111">**Element**</span></span>|<span data-ttu-id="84e45-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="84e45-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84e45-113">CalendarPermissions</span><span class="sxs-lookup"><span data-stu-id="84e45-113">CalendarPermissions</span></span>](calendarpermissions.md) <br/> |<span data-ttu-id="84e45-114">Enthält ein Array von Kalenderberechtigungen für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="84e45-114">Contains an array of calendar permissions for a folder.</span></span> <span data-ttu-id="84e45-115">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="84e45-115">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="84e45-116">UnknownEntries</span><span class="sxs-lookup"><span data-stu-id="84e45-116">UnknownEntries</span></span>](unknownentries.md) <br/> |<span data-ttu-id="84e45-117">Enthält ein Array von unbekannten Einträgen, die gegen den Verzeichnisdienst Active Directory nicht aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="84e45-117">Contains an array of unknown entries that cannot be resolved against the Active Directory directory service.</span></span> <span data-ttu-id="84e45-118">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="84e45-118">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="84e45-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="84e45-119">Parent elements</span></span>

|<span data-ttu-id="84e45-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="84e45-120">**Element**</span></span>|<span data-ttu-id="84e45-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="84e45-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84e45-122">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="84e45-122">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="84e45-123">Stellt einen Ordner, der in erster Linie Kalenderelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="84e45-123">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84e45-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="84e45-124">Remarks</span></span>

<span data-ttu-id="84e45-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="84e45-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="84e45-126">Dieses Element wurde in Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="84e45-126">This element was introduced in Exchange Server 2007 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="84e45-127">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="84e45-127">Version differences</span></span>

<span data-ttu-id="84e45-128">Für Applikationen werden, Exchange Online abzielen, Exchange Online als Teil von Office 365 oder eine lokale Version von Exchange beginnend mit Exchange 2013 Ordnerberechtigungen nicht zurückgegeben, wenn das Element [BaseShape](baseshape.md) **AllProperties** Wert hat in der Anforderung [GetFolder](getfolder-operation.md) -Vorgang.</span><span class="sxs-lookup"><span data-stu-id="84e45-128">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="84e45-129">Um Ordnerberechtigungen abzurufen, fügen Sie dem [AdditionalProperties](additionalproperties.md) -Element in der Anforderung **GetFolder** die [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) -Element hinzu.</span><span class="sxs-lookup"><span data-stu-id="84e45-129">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="84e45-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="84e45-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="84e45-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="84e45-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="84e45-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="84e45-132">Schema Name</span></span>  <br/> |<span data-ttu-id="84e45-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="84e45-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="84e45-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="84e45-134">Validation File</span></span>  <br/> |<span data-ttu-id="84e45-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="84e45-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="84e45-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="84e45-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="84e45-137">False</span><span class="sxs-lookup"><span data-stu-id="84e45-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="84e45-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84e45-138">See also</span></span>



- [<span data-ttu-id="84e45-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="84e45-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="84e45-140">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="84e45-140">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

