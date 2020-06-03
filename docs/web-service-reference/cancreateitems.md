---
title: CanCreateItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CanCreateItems
api_type:
- schema
ms.assetid: c4574e9a-3c42-40a1-a5f9-79b6560e9b30
description: Das CanCreateItems-Element gibt an, ob ein Benutzer über die Berechtigung zum Erstellen von Elementen in einem Ordner verfügt. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 73d3d967774d9fcff53722d0936462025e02b659
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458782"
---
# <a name="cancreateitems"></a><span data-ttu-id="5fb78-104">CanCreateItems</span><span class="sxs-lookup"><span data-stu-id="5fb78-104">CanCreateItems</span></span>

<span data-ttu-id="5fb78-105">Das **CanCreateItems** -Element gibt an, ob ein Benutzer über die Berechtigung zum Erstellen von Elementen in einem Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="5fb78-105">The **CanCreateItems** element indicates whether a user has permission to create items in a folder.</span></span> <span data-ttu-id="5fb78-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5fb78-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<CanCreateItems/>
```

 <span data-ttu-id="5fb78-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="5fb78-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5fb78-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5fb78-108">Attributes and elements</span></span>

<span data-ttu-id="5fb78-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5fb78-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5fb78-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="5fb78-110">Attributes</span></span>

<span data-ttu-id="5fb78-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="5fb78-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5fb78-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5fb78-112">Child elements</span></span>

<span data-ttu-id="5fb78-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="5fb78-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5fb78-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5fb78-114">Parent elements</span></span>

|<span data-ttu-id="5fb78-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="5fb78-115">**Element**</span></span>|<span data-ttu-id="5fb78-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5fb78-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5fb78-117">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="5fb78-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="5fb78-p103">Definiert den Zugriff, den ein Benutzer verfügt in einen Ordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5fb78-p103">Defines the access that a user has to a folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="5fb78-120">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="5fb78-120">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="5fb78-p104">Definiert den, den ein Benutzer hat Zugriff auf einen Kalenderordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5fb78-p104">Defines the access that a user has to a Calendar folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5fb78-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="5fb78-123">Text value</span></span>

<span data-ttu-id="5fb78-124">Der Textwert **true** gibt an, dass der Benutzer Elemente im Ordner erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="5fb78-124">A text value of **true** indicates that the user can create items in the folder.</span></span> <span data-ttu-id="5fb78-125">Der Wert **false** gibt an, dass der Benutzer keine Elemente im Ordner erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="5fb78-125">A value of **false** indicates that the user cannot create items in the folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5fb78-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5fb78-126">Remarks</span></span>

<span data-ttu-id="5fb78-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="5fb78-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5fb78-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="5fb78-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5fb78-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="5fb78-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5fb78-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5fb78-130">Schema Name</span></span>  <br/> |<span data-ttu-id="5fb78-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5fb78-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="5fb78-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5fb78-132">Validation File</span></span>  <br/> |<span data-ttu-id="5fb78-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5fb78-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5fb78-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5fb78-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="5fb78-135">False</span><span class="sxs-lookup"><span data-stu-id="5fb78-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5fb78-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5fb78-136">See also</span></span>



- [<span data-ttu-id="5fb78-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5fb78-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="5fb78-138">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="5fb78-138">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

