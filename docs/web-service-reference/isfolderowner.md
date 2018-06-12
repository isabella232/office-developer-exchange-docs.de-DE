---
title: IsFolderOwner
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsFolderOwner
api_type:
- schema
ms.assetid: 6541ee78-d6e6-42a7-8e7a-d8736172b245
description: Das IsFolderOwner-Element gibt an, ob ein Benutzer den Besitzer eines Ordners ist. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: a8838b2a7ed1b16c1e332d34a38038ba8254fc3f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830016"
---
# <a name="isfolderowner"></a><span data-ttu-id="4afac-104">IsFolderOwner</span><span class="sxs-lookup"><span data-stu-id="4afac-104">IsFolderOwner</span></span>

<span data-ttu-id="4afac-105">Das **IsFolderOwner** -Element gibt an, ob ein Benutzer den Besitzer eines Ordners ist.</span><span class="sxs-lookup"><span data-stu-id="4afac-105">The **IsFolderOwner** element indicates whether a user is the owner of a folder.</span></span> <span data-ttu-id="4afac-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4afac-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<IsFolderOwner/>
```

 <span data-ttu-id="4afac-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="4afac-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4afac-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4afac-108">Attributes and elements</span></span>

<span data-ttu-id="4afac-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4afac-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4afac-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="4afac-110">Attributes</span></span>

<span data-ttu-id="4afac-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="4afac-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4afac-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4afac-112">Child elements</span></span>

<span data-ttu-id="4afac-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="4afac-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4afac-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4afac-114">Parent elements</span></span>

|<span data-ttu-id="4afac-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="4afac-115">**Element**</span></span>|<span data-ttu-id="4afac-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4afac-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4afac-117">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="4afac-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="4afac-p103">Definiert den Zugriff, den ein Benutzer verfügt in einen Ordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4afac-p103">Defines the access that a user has to a folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="4afac-120">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="4afac-120">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="4afac-p104">Definiert den, den ein Benutzer hat Zugriff auf einen Kalenderordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4afac-p104">Defines the access that a user has to a Calendar folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4afac-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="4afac-123">Text value</span></span>

<span data-ttu-id="4afac-124">Der Textwert **true** gibt an, dass der Benutzer den Besitzer des Ordners ist.</span><span class="sxs-lookup"><span data-stu-id="4afac-124">A text value of **true** indicates that the user is the owner of the folder.</span></span> <span data-ttu-id="4afac-125">Der Wert **false** gibt an, dass der Benutzer nicht der Besitzer des Ordners ist.</span><span class="sxs-lookup"><span data-stu-id="4afac-125">A value of **false** indicates that the user is not the owner of the folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4afac-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4afac-126">Remarks</span></span>

<span data-ttu-id="4afac-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="4afac-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4afac-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4afac-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4afac-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="4afac-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4afac-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4afac-130">Schema Name</span></span>  <br/> |<span data-ttu-id="4afac-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="4afac-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="4afac-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4afac-132">Validation File</span></span>  <br/> |<span data-ttu-id="4afac-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4afac-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4afac-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4afac-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="4afac-135">False</span><span class="sxs-lookup"><span data-stu-id="4afac-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4afac-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4afac-136">See also</span></span>



- [<span data-ttu-id="4afac-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4afac-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="4afac-138">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="4afac-138">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

