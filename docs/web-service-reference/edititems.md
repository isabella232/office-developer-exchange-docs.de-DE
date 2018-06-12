---
title: -Smarttagbereich
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EditItems
api_type:
- schema
ms.assetid: 1cb14493-c999-4d66-b82c-ecb410dc1c00
description: Das-Smarttagbereich-Element gibt an, welche Elemente in einem Ordner ein Benutzer über die Berechtigung zum Bearbeiten verfügt. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: bbcc103f171cca7c72967796284c6016d8e284e3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758142"
---
# <a name="edititems"></a><span data-ttu-id="63d5a-104">-Smarttagbereich</span><span class="sxs-lookup"><span data-stu-id="63d5a-104">EditItems</span></span>

<span data-ttu-id="63d5a-105">Das **-Smarttagbereich** -Element gibt an, welche Elemente in einem Ordner ein Benutzer über die Berechtigung zum Bearbeiten verfügt.</span><span class="sxs-lookup"><span data-stu-id="63d5a-105">The **EditItems** element indicates which items in a folder a user has permission to edit.</span></span> <span data-ttu-id="63d5a-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="63d5a-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<EditItems>None or Owned or All</EditItems>
```

 <span data-ttu-id="63d5a-107">**PermissionActionType**</span><span class="sxs-lookup"><span data-stu-id="63d5a-107">**PermissionActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="63d5a-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="63d5a-108">Attributes and elements</span></span>

<span data-ttu-id="63d5a-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="63d5a-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="63d5a-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="63d5a-110">Attributes</span></span>

<span data-ttu-id="63d5a-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="63d5a-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="63d5a-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="63d5a-112">Child elements</span></span>

<span data-ttu-id="63d5a-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="63d5a-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="63d5a-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="63d5a-114">Parent elements</span></span>

|<span data-ttu-id="63d5a-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="63d5a-115">**Element**</span></span>|<span data-ttu-id="63d5a-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="63d5a-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="63d5a-117">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="63d5a-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="63d5a-p103">Definiert den Zugriff, den ein Benutzer verfügt in einen Ordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="63d5a-p103">Defines the access that a user has to a folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="63d5a-120">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="63d5a-120">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="63d5a-p104">Definiert den, den ein Benutzer hat Zugriff auf einen Kalenderordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="63d5a-p104">Defines the access that a user has to a Calendar folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="63d5a-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="63d5a-123">Text value</span></span>

<span data-ttu-id="63d5a-124">Die folgende Tabelle enthält die möglichen Werte für das Element **-Smarttagbereich** .</span><span class="sxs-lookup"><span data-stu-id="63d5a-124">The following table lists the possible values for the **EditItems** element.</span></span> 
  
<span data-ttu-id="63d5a-125">**Text-Elementwerte-Smarttagbereich**</span><span class="sxs-lookup"><span data-stu-id="63d5a-125">**EditItems element text values**</span></span>

|<span data-ttu-id="63d5a-126">**Wert**</span><span class="sxs-lookup"><span data-stu-id="63d5a-126">**Value**</span></span>|<span data-ttu-id="63d5a-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="63d5a-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="63d5a-128">Keine</span><span class="sxs-lookup"><span data-stu-id="63d5a-128">None</span></span>  <br/> |<span data-ttu-id="63d5a-129">Gibt an, dass der Benutzer nicht über die Berechtigung zum Bearbeiten von Elementen in den Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="63d5a-129">Indicates that the user does not have permission to edit items in the folder.</span></span>  <br/> |
|<span data-ttu-id="63d5a-130">Gehören</span><span class="sxs-lookup"><span data-stu-id="63d5a-130">Owned</span></span>  <br/> |<span data-ttu-id="63d5a-131">Gibt an, dass der Benutzer verfügt über die Berechtigung zum Bearbeiten die Elemente, die der Benutzer im Ordner besitzt.</span><span class="sxs-lookup"><span data-stu-id="63d5a-131">Indicates that the user has permission to edit the items that the user owns in the folder.</span></span>  <br/> |
|<span data-ttu-id="63d5a-132">Alle</span><span class="sxs-lookup"><span data-stu-id="63d5a-132">All</span></span>  <br/> |<span data-ttu-id="63d5a-133">Gibt an, dass der Benutzer über Berechtigungen zum Bearbeiten aller Elemente im Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="63d5a-133">Indicates that the user has permission to edit all items in the folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63d5a-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="63d5a-134">Remarks</span></span>

<span data-ttu-id="63d5a-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="63d5a-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="63d5a-136">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="63d5a-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="63d5a-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="63d5a-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="63d5a-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="63d5a-138">Schema Name</span></span>  <br/> |<span data-ttu-id="63d5a-139">Schematypen</span><span class="sxs-lookup"><span data-stu-id="63d5a-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="63d5a-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="63d5a-140">Validation File</span></span>  <br/> |<span data-ttu-id="63d5a-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="63d5a-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="63d5a-142">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="63d5a-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="63d5a-143">False</span><span class="sxs-lookup"><span data-stu-id="63d5a-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="63d5a-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63d5a-144">See also</span></span>

- [<span data-ttu-id="63d5a-145">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="63d5a-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="63d5a-146">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="63d5a-146">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

