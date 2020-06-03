---
title: CalendarPermissions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarPermissions
api_type:
- schema
ms.assetid: 9b659d83-45fb-42a2-b052-5bc4dbe3854d
description: Das CalendarPermissions-Element enthält ein Array von Kalenderberechtigungen für einen Ordner. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: f072339212d0fdff3983fbfb6bc8f53c272350c8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529469"
---
# <a name="calendarpermissions"></a><span data-ttu-id="1ce77-104">CalendarPermissions</span><span class="sxs-lookup"><span data-stu-id="1ce77-104">CalendarPermissions</span></span>

<span data-ttu-id="1ce77-105">Das **CalendarPermissions** -Element enthält ein Array von Kalenderberechtigungen für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="1ce77-105">The **CalendarPermissions** element contains an array of calendar permissions for a folder.</span></span> <span data-ttu-id="1ce77-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1ce77-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<CalendarPermissions>
   <PermissionSet/>
</CalendarPermissions>
```

 <span data-ttu-id="1ce77-107">**ArrayOfCalendarPermissionsType**</span><span class="sxs-lookup"><span data-stu-id="1ce77-107">**ArrayOfCalendarPermissionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1ce77-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1ce77-108">Attributes and elements</span></span>

<span data-ttu-id="1ce77-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1ce77-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1ce77-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="1ce77-110">Attributes</span></span>

<span data-ttu-id="1ce77-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="1ce77-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1ce77-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1ce77-112">Child elements</span></span>

|<span data-ttu-id="1ce77-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ce77-113">**Element**</span></span>|<span data-ttu-id="1ce77-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ce77-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1ce77-115">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="1ce77-115">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="1ce77-116">Definiert den Zugriff, den ein Stellvertreter Benutzer in einen Kalenderordner hat.</span><span class="sxs-lookup"><span data-stu-id="1ce77-116">Defines the access that a delegate user has to a calendar folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1ce77-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1ce77-117">Parent elements</span></span>

|<span data-ttu-id="1ce77-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ce77-118">**Element**</span></span>|<span data-ttu-id="1ce77-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ce77-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1ce77-120">PermissionSet (CalendarPermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="1ce77-120">PermissionSet (CalendarPermissionSetType)</span></span>](permissionset-calendarpermissionsettype.md) <br/> |<span data-ttu-id="1ce77-121">Enthält alle konfigurierten Berechtigungen für einen Kalenderordner.</span><span class="sxs-lookup"><span data-stu-id="1ce77-121">Contains all the configured permissions for a calendar folder.</span></span> <span data-ttu-id="1ce77-122">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1ce77-122">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ce77-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ce77-123">Remarks</span></span>

<span data-ttu-id="1ce77-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="1ce77-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1ce77-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1ce77-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ce77-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="1ce77-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1ce77-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1ce77-127">Schema Name</span></span>  <br/> |<span data-ttu-id="1ce77-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1ce77-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="1ce77-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1ce77-129">Validation File</span></span>  <br/> |<span data-ttu-id="1ce77-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1ce77-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1ce77-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1ce77-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="1ce77-132">False</span><span class="sxs-lookup"><span data-stu-id="1ce77-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ce77-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ce77-133">See also</span></span>



- [<span data-ttu-id="1ce77-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1ce77-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="1ce77-135">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="1ce77-135">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

