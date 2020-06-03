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
description: Das UnknownEntries-Element enthält ein Array von unbekannten Berechtigungseinträgen, die nicht für den Active Directory Verzeichnisdienst aufgelöst werden können. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 68cb2518b895ca0a74e6b9ed649ee92b7502ab05
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459419"
---
# <a name="unknownentries"></a><span data-ttu-id="2f015-104">UnknownEntries</span><span class="sxs-lookup"><span data-stu-id="2f015-104">UnknownEntries</span></span>

<span data-ttu-id="2f015-105">Das **UnknownEntries** -Element enthält ein Array von unbekannten Berechtigungseinträgen, die nicht für den Active Directory Verzeichnisdienst aufgelöst werden können.</span><span class="sxs-lookup"><span data-stu-id="2f015-105">The **UnknownEntries** element contains an array of unknown permission entries that cannot be resolved against the Active Directory directory service.</span></span> <span data-ttu-id="2f015-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2f015-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<UnknownEntries>
   <UnknownEntry/>
</UnknownEntries>
```

 <span data-ttu-id="2f015-107">**ArrayOfUnknownEntriesType**</span><span class="sxs-lookup"><span data-stu-id="2f015-107">**ArrayOfUnknownEntriesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2f015-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2f015-108">Attributes and elements</span></span>

<span data-ttu-id="2f015-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2f015-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2f015-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="2f015-110">Attributes</span></span>

<span data-ttu-id="2f015-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="2f015-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2f015-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2f015-112">Child elements</span></span>

|<span data-ttu-id="2f015-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2f015-113">**Element**</span></span>|<span data-ttu-id="2f015-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2f015-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f015-115">UnknownEntry</span><span class="sxs-lookup"><span data-stu-id="2f015-115">UnknownEntry</span></span>](unknownentry.md) <br/> |<span data-ttu-id="2f015-116">Stellt einen einzelnen unbekannten Berechtigungseintrag dar, der nicht für Active Directory aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="2f015-116">Represents a single unknown permission entry that cannot be resolved against Active Directory.</span></span> <span data-ttu-id="2f015-117">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2f015-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2f015-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2f015-118">Parent elements</span></span>

|<span data-ttu-id="2f015-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="2f015-119">**Element**</span></span>|<span data-ttu-id="2f015-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2f015-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f015-121">PermissionSet (permissionsettype)</span><span class="sxs-lookup"><span data-stu-id="2f015-121">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="2f015-122">Enthält alle Berechtigungen, die für einen Ordner konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="2f015-122">Contains all the permissions that are configured for a folder.</span></span> <span data-ttu-id="2f015-123">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2f015-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="2f015-124">PermissionSet (CalendarPermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="2f015-124">PermissionSet (CalendarPermissionSetType)</span></span>](permissionset-calendarpermissionsettype.md) <br/> |<span data-ttu-id="2f015-125">Enthält alle Berechtigungen, die für einen Kalenderordner konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="2f015-125">Contains all the permissions that are configured for a calendar folder.</span></span> <span data-ttu-id="2f015-126">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2f015-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f015-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f015-127">Remarks</span></span>

<span data-ttu-id="2f015-128">Sie können unbekannte Einträge aus einem Ordner löschen, indem Sie den UpdateFolder-Vorgang mit dem [setfolderfield](setfolderfield.md) -Element verwenden.</span><span class="sxs-lookup"><span data-stu-id="2f015-128">You can delete unknown entries from a folder by using the UpdateFolder operation with the [SetFolderField](setfolderfield.md) element.</span></span> <span data-ttu-id="2f015-129">Die unbekannten Einträge werden gelöscht, wenn Sie das PermissionSet mithilfe der Option setfolderfield des UpdateFolder-Vorgangs zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="2f015-129">The unknown entries are deleted when you reset the PermissionSet by using the SetFolderField option of the UpdateFolder operation.</span></span> <span data-ttu-id="2f015-130">Das Löschen einzelner Einträge wird von Exchange Webdienste nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2f015-130">Exchange Web Services does not support the deletion of individual entries.</span></span> 
  
<span data-ttu-id="2f015-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="2f015-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2f015-132">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2f015-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f015-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="2f015-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2f015-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2f015-134">Schema Name</span></span>  <br/> |<span data-ttu-id="2f015-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="2f015-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="2f015-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2f015-136">Validation File</span></span>  <br/> |<span data-ttu-id="2f015-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2f015-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2f015-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2f015-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="2f015-139">False</span><span class="sxs-lookup"><span data-stu-id="2f015-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2f015-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f015-140">See also</span></span>



[<span data-ttu-id="2f015-141">UpdateFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2f015-141">UpdateFolder operation</span></span>](updatefolder-operation.md)


- [<span data-ttu-id="2f015-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2f015-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="2f015-143">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="2f015-143">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

