---
title: ReadItems (PermissionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReadItems
api_type:
- schema
ms.assetid: 0a11a802-28e2-436b-b5a9-30fd064675a6
description: Das ReadItems-Element gibt an, ob ein Benutzer über die Berechtigung zum Lesen von Elementen in einem Ordner verfügt. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: bf266c77106f25b90ffd174e25fb0c3972ab91cb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830961"
---
# <a name="readitems-permissiontype"></a><span data-ttu-id="b8d11-104">ReadItems (PermissionType)</span><span class="sxs-lookup"><span data-stu-id="b8d11-104">ReadItems (PermissionType)</span></span>

<span data-ttu-id="b8d11-105">Das **ReadItems** -Element gibt an, ob ein Benutzer über die Berechtigung zum Lesen von Elementen in einem Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="b8d11-105">The **ReadItems** element indicates whether a user has permission to read items within a folder.</span></span> <span data-ttu-id="b8d11-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b8d11-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ReadItems>None or FullDetails</ReadItems>
```

 <span data-ttu-id="b8d11-107">**PermissionReadAccessType**</span><span class="sxs-lookup"><span data-stu-id="b8d11-107">**PermissionReadAccessType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b8d11-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b8d11-108">Attributes and elements</span></span>

<span data-ttu-id="b8d11-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b8d11-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b8d11-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="b8d11-110">Attributes</span></span>

<span data-ttu-id="b8d11-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b8d11-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b8d11-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b8d11-112">Child elements</span></span>

<span data-ttu-id="b8d11-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="b8d11-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b8d11-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b8d11-114">Parent elements</span></span>

|<span data-ttu-id="b8d11-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="b8d11-115">**Element**</span></span>|<span data-ttu-id="b8d11-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b8d11-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8d11-117">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="b8d11-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="b8d11-p103">Definiert den Zugriff, den ein Benutzer verfügt in einen Ordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b8d11-p103">Defines the access that a user has to a folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b8d11-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="b8d11-120">Text value</span></span>

<span data-ttu-id="b8d11-121">Die folgende Tabelle enthält die möglichen Werte für das **ReadItems** -Element.</span><span class="sxs-lookup"><span data-stu-id="b8d11-121">The following table lists the possible values for the **ReadItems** element.</span></span> 
  
<span data-ttu-id="b8d11-122">**ReadItems Elementwerte text**</span><span class="sxs-lookup"><span data-stu-id="b8d11-122">**ReadItems element text values**</span></span>

|<span data-ttu-id="b8d11-123">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b8d11-123">**Value**</span></span>|<span data-ttu-id="b8d11-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b8d11-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b8d11-125">Keine</span><span class="sxs-lookup"><span data-stu-id="b8d11-125">None</span></span>  <br/> |<span data-ttu-id="b8d11-126">Gibt an, dass der Benutzer nicht über die Berechtigung zum Lesen von Elementen in den Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="b8d11-126">Indicates that the user does not have permission to read items in the folder.</span></span>  <br/> |
|<span data-ttu-id="b8d11-127">FullDetails</span><span class="sxs-lookup"><span data-stu-id="b8d11-127">FullDetails</span></span>  <br/> |<span data-ttu-id="b8d11-128">Gibt an, dass der Benutzer die Berechtigung zum Lesen aller Elemente im Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="b8d11-128">Indicates that the user has permission to read all items in the folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8d11-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b8d11-129">Remarks</span></span>

<span data-ttu-id="b8d11-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="b8d11-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b8d11-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b8d11-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b8d11-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="b8d11-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b8d11-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b8d11-133">Schema Name</span></span>  <br/> |<span data-ttu-id="b8d11-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b8d11-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="b8d11-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b8d11-135">Validation File</span></span>  <br/> |<span data-ttu-id="b8d11-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b8d11-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b8d11-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b8d11-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="b8d11-138">False</span><span class="sxs-lookup"><span data-stu-id="b8d11-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b8d11-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8d11-139">See also</span></span>



- [<span data-ttu-id="b8d11-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b8d11-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="b8d11-141">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="b8d11-141">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

