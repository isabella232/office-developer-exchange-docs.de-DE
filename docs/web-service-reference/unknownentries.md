---
title: UnknownEntries
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnknownEntries
api_type:
- schema
ms.assetid: 107ec73e-083a-4956-9d37-33d4734cc157
description: Das UnknownEntries-Element enthält ein Array von unbekannten Berechtigungseinträge, die gegen den Verzeichnisdienst Active Directory nicht aufgelöst werden kann. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 306e5f226a56694bb1ff32362f77e7dff80865ad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839320"
---
# <a name="unknownentries"></a><span data-ttu-id="01cbc-104">UnknownEntries</span><span class="sxs-lookup"><span data-stu-id="01cbc-104">UnknownEntries</span></span>

<span data-ttu-id="01cbc-105">Das **UnknownEntries** -Element enthält ein Array von unbekannten Berechtigungseinträge, die gegen den Verzeichnisdienst Active Directory nicht aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="01cbc-105">The **UnknownEntries** element contains an array of unknown permission entries that cannot be resolved against the Active Directory directory service.</span></span> <span data-ttu-id="01cbc-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="01cbc-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<UnknownEntries>
   <UnknownEntry/>
</UnknownEntries>
```

 <span data-ttu-id="01cbc-107">**ArrayOfUnknownEntriesType**</span><span class="sxs-lookup"><span data-stu-id="01cbc-107">**ArrayOfUnknownEntriesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="01cbc-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="01cbc-108">Attributes and elements</span></span>

<span data-ttu-id="01cbc-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="01cbc-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="01cbc-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="01cbc-110">Attributes</span></span>

<span data-ttu-id="01cbc-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="01cbc-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="01cbc-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="01cbc-112">Child elements</span></span>

|<span data-ttu-id="01cbc-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="01cbc-113">**Element**</span></span>|<span data-ttu-id="01cbc-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="01cbc-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01cbc-115">UnknownEntry</span><span class="sxs-lookup"><span data-stu-id="01cbc-115">UnknownEntry</span></span>](unknownentry.md) <br/> |<span data-ttu-id="01cbc-116">Stellt einen einzelnen unbekannte Berechtigungseintrag, der anhand von Active Directory nicht aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="01cbc-116">Represents a single unknown permission entry that cannot be resolved against Active Directory.</span></span> <span data-ttu-id="01cbc-117">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="01cbc-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="01cbc-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="01cbc-118">Parent elements</span></span>

|<span data-ttu-id="01cbc-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="01cbc-119">**Element**</span></span>|<span data-ttu-id="01cbc-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="01cbc-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01cbc-121">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="01cbc-121">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="01cbc-122">Enthält alle Berechtigungen, die für einen Ordner konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="01cbc-122">Contains all the permissions that are configured for a folder.</span></span> <span data-ttu-id="01cbc-123">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="01cbc-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="01cbc-124">PermissionSet (CalendarPermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="01cbc-124">PermissionSet (CalendarPermissionSetType)</span></span>](permissionset-calendarpermissionsettype.md) <br/> |<span data-ttu-id="01cbc-125">Enthält alle Berechtigungen, die für einen Kalenderordner konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="01cbc-125">Contains all the permissions that are configured for a calendar folder.</span></span> <span data-ttu-id="01cbc-126">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="01cbc-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01cbc-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="01cbc-127">Remarks</span></span>

<span data-ttu-id="01cbc-128">Sie können unbekannte Einträge aus einem Ordner mit der UpdateFolder-Operation mit dem [SetFolderField](setfolderfield.md) Element löschen.</span><span class="sxs-lookup"><span data-stu-id="01cbc-128">You can delete unknown entries from a folder by using the UpdateFolder operation with the [SetFolderField](setfolderfield.md) element.</span></span> <span data-ttu-id="01cbc-129">Die unbekannte Einträge werden gelöscht, wenn Sie mithilfe der Option SetFolderField des Vorgangs UpdateFolder PermissionSet zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="01cbc-129">The unknown entries are deleted when you reset the PermissionSet by using the SetFolderField option of the UpdateFolder operation.</span></span> <span data-ttu-id="01cbc-130">Exchange-Webdienste unterstützt nicht das Löschen der einzelnen Einträge.</span><span class="sxs-lookup"><span data-stu-id="01cbc-130">Exchange Web Services does not support the deletion of individual entries.</span></span> 
  
<span data-ttu-id="01cbc-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="01cbc-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="01cbc-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="01cbc-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="01cbc-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="01cbc-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="01cbc-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="01cbc-134">Schema Name</span></span>  <br/> |<span data-ttu-id="01cbc-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="01cbc-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="01cbc-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="01cbc-136">Validation File</span></span>  <br/> |<span data-ttu-id="01cbc-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="01cbc-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="01cbc-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="01cbc-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="01cbc-139">False</span><span class="sxs-lookup"><span data-stu-id="01cbc-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="01cbc-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01cbc-140">See also</span></span>



[<span data-ttu-id="01cbc-141">UpdateFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="01cbc-141">UpdateFolder operation</span></span>](updatefolder-operation.md)


- [<span data-ttu-id="01cbc-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="01cbc-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="01cbc-143">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="01cbc-143">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

