---
title: DeleteItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteItems
api_type:
- schema
ms.assetid: a5898bfc-f5ae-451d-9713-3e55864c690c
description: Das Element DeleteItems gibt an, welche Elemente in einem Ordner ein Benutzer über die Berechtigung zum Löschen verfügt. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 0be2154d1ceb6a995df8b27033fdc59bca81f9ef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757936"
---
# <a name="deleteitems"></a><span data-ttu-id="0591b-104">DeleteItems</span><span class="sxs-lookup"><span data-stu-id="0591b-104">DeleteItems</span></span>

<span data-ttu-id="0591b-105">Das Element **DeleteItems** gibt an, welche Elemente in einem Ordner ein Benutzer über die Berechtigung zum Löschen verfügt.</span><span class="sxs-lookup"><span data-stu-id="0591b-105">The **DeleteItems** element indicates which items in a folder a user has permission to delete.</span></span> <span data-ttu-id="0591b-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0591b-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<DeleteItems>None or Owned or All</DeleteItems>
```

 <span data-ttu-id="0591b-107">**PermissionActionType**</span><span class="sxs-lookup"><span data-stu-id="0591b-107">**PermissionActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0591b-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0591b-108">Attributes and elements</span></span>

<span data-ttu-id="0591b-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0591b-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0591b-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="0591b-110">Attributes</span></span>

<span data-ttu-id="0591b-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="0591b-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0591b-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0591b-112">Child elements</span></span>

<span data-ttu-id="0591b-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="0591b-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0591b-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0591b-114">Parent elements</span></span>

|<span data-ttu-id="0591b-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="0591b-115">**Element**</span></span>|<span data-ttu-id="0591b-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0591b-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0591b-117">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="0591b-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="0591b-p103">Definiert den Zugriff, den ein Benutzer verfügt in einen Ordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0591b-p103">Defines the access that a user has to a folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="0591b-120">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="0591b-120">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="0591b-p104">Definiert den, den ein Benutzer hat Zugriff auf einen Kalenderordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0591b-p104">Defines the access that a user has to a Calendar folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0591b-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="0591b-123">Text value</span></span>

<span data-ttu-id="0591b-124">Die folgende Tabelle enthält die möglichen Werte für das **DeleteItems** -Element.</span><span class="sxs-lookup"><span data-stu-id="0591b-124">The following table lists the possible values for the **DeleteItems** element.</span></span> 
  
<span data-ttu-id="0591b-125">**DeleteItems Elementwerte text**</span><span class="sxs-lookup"><span data-stu-id="0591b-125">**DeleteItems element text values**</span></span>

|<span data-ttu-id="0591b-126">**Wert**</span><span class="sxs-lookup"><span data-stu-id="0591b-126">**Value**</span></span>|<span data-ttu-id="0591b-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0591b-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0591b-128">Keine</span><span class="sxs-lookup"><span data-stu-id="0591b-128">None</span></span>  <br/> |<span data-ttu-id="0591b-129">Gibt an, dass der Benutzer über die Berechtigung zum Löschen von Elementen im Ordner nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0591b-129">Indicates that the user does not have permission to delete items in the folder.</span></span>  <br/> |
|<span data-ttu-id="0591b-130">Gehören</span><span class="sxs-lookup"><span data-stu-id="0591b-130">Owned</span></span>  <br/> |<span data-ttu-id="0591b-131">Gibt an, dass der Benutzer verfügt über die Berechtigung, die Elemente löschen, die der Benutzer im Ordner besitzt.</span><span class="sxs-lookup"><span data-stu-id="0591b-131">Indicates that the user has permission to delete the items that the user owns in the folder.</span></span>  <br/> |
|<span data-ttu-id="0591b-132">Alle</span><span class="sxs-lookup"><span data-stu-id="0591b-132">All</span></span>  <br/> |<span data-ttu-id="0591b-133">Gibt an, dass der Benutzer die Berechtigung zum Löschen aller Elemente im Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="0591b-133">Indicates that the user has permission to delete all items in the folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0591b-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0591b-134">Remarks</span></span>

<span data-ttu-id="0591b-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="0591b-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0591b-136">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0591b-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0591b-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="0591b-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0591b-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0591b-138">Schema Name</span></span>  <br/> |<span data-ttu-id="0591b-139">Schematypen</span><span class="sxs-lookup"><span data-stu-id="0591b-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="0591b-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0591b-140">Validation File</span></span>  <br/> |<span data-ttu-id="0591b-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0591b-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0591b-142">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0591b-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="0591b-143">False</span><span class="sxs-lookup"><span data-stu-id="0591b-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0591b-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0591b-144">See also</span></span>

- [<span data-ttu-id="0591b-145">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0591b-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="0591b-146">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="0591b-146">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

