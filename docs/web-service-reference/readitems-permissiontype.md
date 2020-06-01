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
ms.openlocfilehash: af6ef5107b5e4f2b3071c0bc9b4b528efea6dcca
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468271"
---
# <a name="readitems-permissiontype"></a><span data-ttu-id="3c52a-104">ReadItems (PermissionType)</span><span class="sxs-lookup"><span data-stu-id="3c52a-104">ReadItems (PermissionType)</span></span>

<span data-ttu-id="3c52a-105">Das **ReadItems** -Element gibt an, ob ein Benutzer über die Berechtigung zum Lesen von Elementen in einem Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="3c52a-105">The **ReadItems** element indicates whether a user has permission to read items within a folder.</span></span> <span data-ttu-id="3c52a-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3c52a-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ReadItems>None or FullDetails</ReadItems>
```

 <span data-ttu-id="3c52a-107">**PermissionReadAccessType**</span><span class="sxs-lookup"><span data-stu-id="3c52a-107">**PermissionReadAccessType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3c52a-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3c52a-108">Attributes and elements</span></span>

<span data-ttu-id="3c52a-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3c52a-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3c52a-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="3c52a-110">Attributes</span></span>

<span data-ttu-id="3c52a-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="3c52a-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3c52a-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3c52a-112">Child elements</span></span>

<span data-ttu-id="3c52a-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="3c52a-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3c52a-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3c52a-114">Parent elements</span></span>

|<span data-ttu-id="3c52a-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="3c52a-115">**Element**</span></span>|<span data-ttu-id="3c52a-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3c52a-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3c52a-117">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="3c52a-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="3c52a-p103">Definiert den Zugriff, den ein Benutzer verfügt in einen Ordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3c52a-p103">Defines the access that a user has to a folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3c52a-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="3c52a-120">Text value</span></span>

<span data-ttu-id="3c52a-121">In der folgenden Tabelle sind die möglichen Werte für das **ReadItems** -Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="3c52a-121">The following table lists the possible values for the **ReadItems** element.</span></span> 
  
<span data-ttu-id="3c52a-122">**ReadItems-Element Text Werte**</span><span class="sxs-lookup"><span data-stu-id="3c52a-122">**ReadItems element text values**</span></span>

|<span data-ttu-id="3c52a-123">**Wert**</span><span class="sxs-lookup"><span data-stu-id="3c52a-123">**Value**</span></span>|<span data-ttu-id="3c52a-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3c52a-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3c52a-125">Keine</span><span class="sxs-lookup"><span data-stu-id="3c52a-125">None</span></span>  <br/> |<span data-ttu-id="3c52a-126">Gibt an, dass der Benutzer nicht über die Berechtigung zum Lesen von Elementen im Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="3c52a-126">Indicates that the user does not have permission to read items in the folder.</span></span>  <br/> |
|<span data-ttu-id="3c52a-127">FullDetails</span><span class="sxs-lookup"><span data-stu-id="3c52a-127">FullDetails</span></span>  <br/> |<span data-ttu-id="3c52a-128">Gibt an, dass der Benutzer über die Berechtigung zum Lesen aller Elemente im Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="3c52a-128">Indicates that the user has permission to read all items in the folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c52a-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c52a-129">Remarks</span></span>

<span data-ttu-id="3c52a-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="3c52a-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3c52a-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3c52a-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c52a-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="3c52a-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3c52a-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3c52a-133">Schema Name</span></span>  <br/> |<span data-ttu-id="3c52a-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3c52a-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="3c52a-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3c52a-135">Validation File</span></span>  <br/> |<span data-ttu-id="3c52a-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3c52a-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3c52a-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3c52a-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="3c52a-138">False</span><span class="sxs-lookup"><span data-stu-id="3c52a-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3c52a-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c52a-139">See also</span></span>



- [<span data-ttu-id="3c52a-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3c52a-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="3c52a-141">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="3c52a-141">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

