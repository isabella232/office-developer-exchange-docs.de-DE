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
description: Das PermissionSet-Element enthält alle Berechtigungen, die für einen Kalenderordner konfiguriert sind.
ms.openlocfilehash: 9564608397ac8a5ab0ddd4508eacd8cad665d76e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458033"
---
# <a name="permissionset-calendarpermissionsettype"></a><span data-ttu-id="48056-103">PermissionSet (CalendarPermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="48056-103">PermissionSet (CalendarPermissionSetType)</span></span>

<span data-ttu-id="48056-104">Das **PermissionSet** -Element enthält alle Berechtigungen, die für einen Kalenderordner konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="48056-104">The **PermissionSet** element contains all the permissions that are configured for a calendar folder.</span></span> 
  
```XML
<PermissionSet>
   <CalendarPermissions/>
   <UnknownEntries/>
</PermissionSet>
```

 <span data-ttu-id="48056-105">**CalendarPermissonSetType**</span><span class="sxs-lookup"><span data-stu-id="48056-105">**CalendarPermissonSetType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="48056-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="48056-106">Attributes and elements</span></span>

<span data-ttu-id="48056-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="48056-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="48056-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="48056-108">Attributes</span></span>

<span data-ttu-id="48056-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="48056-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="48056-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="48056-110">Child elements</span></span>

|<span data-ttu-id="48056-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="48056-111">**Element**</span></span>|<span data-ttu-id="48056-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="48056-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="48056-113">CalendarPermissions</span><span class="sxs-lookup"><span data-stu-id="48056-113">CalendarPermissions</span></span>](calendarpermissions.md) <br/> |<span data-ttu-id="48056-114">Enthält ein Array von Kalenderberechtigungen für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="48056-114">Contains an array of calendar permissions for a folder.</span></span> <span data-ttu-id="48056-115">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="48056-115">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="48056-116">UnknownEntries</span><span class="sxs-lookup"><span data-stu-id="48056-116">UnknownEntries</span></span>](unknownentries.md) <br/> |<span data-ttu-id="48056-117">Enthält ein Array von unbekannten Einträgen, die nicht für den Active Directory Verzeichnisdienst aufgelöst werden können.</span><span class="sxs-lookup"><span data-stu-id="48056-117">Contains an array of unknown entries that cannot be resolved against the Active Directory directory service.</span></span> <span data-ttu-id="48056-118">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="48056-118">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="48056-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="48056-119">Parent elements</span></span>

|<span data-ttu-id="48056-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="48056-120">**Element**</span></span>|<span data-ttu-id="48056-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="48056-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="48056-122">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="48056-122">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="48056-123">Stellt einen Ordner dar, der in erster Linie Kalenderelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="48056-123">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48056-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48056-124">Remarks</span></span>

<span data-ttu-id="48056-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="48056-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="48056-126">Dieses Element wurde in Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="48056-126">This element was introduced in Exchange Server 2007 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="48056-127">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="48056-127">Version differences</span></span>

<span data-ttu-id="48056-128">Für Anwendungen, die auf Exchange Online Zielen, Exchange Online im Rahmen von Office 365 oder einer lokalen Exchange-Version, die mit Exchange 2013 beginnt, werden Ordnerberechtigungen nicht zurückgegeben, wenn das [BaseShape](baseshape.md) -Element den Wert **allproperties** in der [GetFolder](getfolder-operation.md) -Vorgangsanforderung aufweist.</span><span class="sxs-lookup"><span data-stu-id="48056-128">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="48056-129">Zum Abrufen von Ordnerberechtigungen fügen Sie dem [AdditionalProperties](additionalproperties.md) -Element in der **GetFolder** -Anforderung das [PermissionSet-Element (permissionsettype)](permissionset-permissionsettype.md) hinzu.</span><span class="sxs-lookup"><span data-stu-id="48056-129">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="48056-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="48056-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="48056-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="48056-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="48056-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="48056-132">Schema Name</span></span>  <br/> |<span data-ttu-id="48056-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="48056-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="48056-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="48056-134">Validation File</span></span>  <br/> |<span data-ttu-id="48056-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="48056-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="48056-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="48056-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="48056-137">False</span><span class="sxs-lookup"><span data-stu-id="48056-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="48056-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48056-138">See also</span></span>



- [<span data-ttu-id="48056-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="48056-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="48056-140">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="48056-140">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

