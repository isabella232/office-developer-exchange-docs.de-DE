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
description: Das DeleteItems-Element gibt an, welche Elemente in einem Ordner ein Benutzer berechtigt ist, zu löschen. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: a0bbefc8b021d047bb2e001669c3e92a6e2536ce
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44454407"
---
# <a name="deleteitems"></a><span data-ttu-id="ef077-104">DeleteItems</span><span class="sxs-lookup"><span data-stu-id="ef077-104">DeleteItems</span></span>

<span data-ttu-id="ef077-105">Das **DeleteItems** -Element gibt an, welche Elemente in einem Ordner ein Benutzer berechtigt ist, zu löschen.</span><span class="sxs-lookup"><span data-stu-id="ef077-105">The **DeleteItems** element indicates which items in a folder a user has permission to delete.</span></span> <span data-ttu-id="ef077-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ef077-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<DeleteItems>None or Owned or All</DeleteItems>
```

 <span data-ttu-id="ef077-107">**PermissionActionType**</span><span class="sxs-lookup"><span data-stu-id="ef077-107">**PermissionActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ef077-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ef077-108">Attributes and elements</span></span>

<span data-ttu-id="ef077-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ef077-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef077-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="ef077-110">Attributes</span></span>

<span data-ttu-id="ef077-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ef077-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ef077-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ef077-112">Child elements</span></span>

<span data-ttu-id="ef077-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="ef077-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ef077-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ef077-114">Parent elements</span></span>

|<span data-ttu-id="ef077-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="ef077-115">**Element**</span></span>|<span data-ttu-id="ef077-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ef077-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ef077-117">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="ef077-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="ef077-p103">Definiert den Zugriff, den ein Benutzer verfügt in einen Ordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ef077-p103">Defines the access that a user has to a folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="ef077-120">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="ef077-120">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="ef077-p104">Definiert den, den ein Benutzer hat Zugriff auf einen Kalenderordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ef077-p104">Defines the access that a user has to a Calendar folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ef077-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="ef077-123">Text value</span></span>

<span data-ttu-id="ef077-124">In der folgenden Tabelle sind die möglichen Werte für das **DeleteItems** -Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="ef077-124">The following table lists the possible values for the **DeleteItems** element.</span></span> 
  
<span data-ttu-id="ef077-125">**DeleteItems-Element Text Werte**</span><span class="sxs-lookup"><span data-stu-id="ef077-125">**DeleteItems element text values**</span></span>

|<span data-ttu-id="ef077-126">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ef077-126">**Value**</span></span>|<span data-ttu-id="ef077-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ef077-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ef077-128">Keine</span><span class="sxs-lookup"><span data-stu-id="ef077-128">None</span></span>  <br/> |<span data-ttu-id="ef077-129">Gibt an, dass der Benutzer nicht über die Berechtigung zum Löschen von Elementen im Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="ef077-129">Indicates that the user does not have permission to delete items in the folder.</span></span>  <br/> |
|<span data-ttu-id="ef077-130">Im Besitz</span><span class="sxs-lookup"><span data-stu-id="ef077-130">Owned</span></span>  <br/> |<span data-ttu-id="ef077-131">Gibt an, dass der Benutzer über die Berechtigung zum Löschen der Elemente verfügt, die der Benutzer im Ordner besitzt.</span><span class="sxs-lookup"><span data-stu-id="ef077-131">Indicates that the user has permission to delete the items that the user owns in the folder.</span></span>  <br/> |
|<span data-ttu-id="ef077-132">Alle</span><span class="sxs-lookup"><span data-stu-id="ef077-132">All</span></span>  <br/> |<span data-ttu-id="ef077-133">Gibt an, dass der Benutzer berechtigt ist, alle Elemente im Ordner zu löschen.</span><span class="sxs-lookup"><span data-stu-id="ef077-133">Indicates that the user has permission to delete all items in the folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef077-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef077-134">Remarks</span></span>

<span data-ttu-id="ef077-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ef077-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef077-136">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ef077-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef077-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="ef077-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ef077-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ef077-138">Schema Name</span></span>  <br/> |<span data-ttu-id="ef077-139">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ef077-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="ef077-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ef077-140">Validation File</span></span>  <br/> |<span data-ttu-id="ef077-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ef077-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ef077-142">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ef077-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="ef077-143">False</span><span class="sxs-lookup"><span data-stu-id="ef077-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ef077-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef077-144">See also</span></span>

- [<span data-ttu-id="ef077-145">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ef077-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="ef077-146">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="ef077-146">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

