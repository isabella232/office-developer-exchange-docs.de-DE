---
title: CanCreateSubFolders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CanCreateSubFolders
api_type:
- schema
ms.assetid: 4404a1cc-6d3f-4996-9647-58a740e8f883
description: Das CanCreateSubFolders -Element gibt an, ob ein Benutzer die Berechtigung zum Erstellen von Unterordnern in einem Ordner verfügt. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 234cbf604a3f0f5aa6e7fa896b7b6735516bd9ec
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757551"
---
# <a name="cancreatesubfolders"></a><span data-ttu-id="e95b0-104">CanCreateSubFolders</span><span class="sxs-lookup"><span data-stu-id="e95b0-104">CanCreateSubFolders</span></span>

<span data-ttu-id="e95b0-p102">Das **CanCreateSubFolders** -Element gibt an, ob ein Benutzer die Berechtigung zum Erstellen von Unterordnern in einem Ordner verfügt. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e95b0-p102">The **CanCreateSubFolders** element indicates whether a user has permission to create subfolders in a folder. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<CanCreateSubFolders/>
```

 <span data-ttu-id="e95b0-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e95b0-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e95b0-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e95b0-108">Attributes and elements</span></span>

<span data-ttu-id="e95b0-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e95b0-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e95b0-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="e95b0-110">Attributes</span></span>

<span data-ttu-id="e95b0-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="e95b0-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e95b0-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e95b0-112">Child elements</span></span>

<span data-ttu-id="e95b0-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="e95b0-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e95b0-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e95b0-114">Parent elements</span></span>

|<span data-ttu-id="e95b0-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="e95b0-115">**Element**</span></span>|<span data-ttu-id="e95b0-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e95b0-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e95b0-117">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="e95b0-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="e95b0-p103">Definiert den Zugriff, den ein Benutzer verfügt in einen Ordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e95b0-p103">Defines the access that a user has to a folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="e95b0-120">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="e95b0-120">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="e95b0-p104">Definiert den, den ein Benutzer hat Zugriff auf einen Kalenderordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e95b0-p104">Defines the access that a user has to a Calendar folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e95b0-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="e95b0-123">Text value</span></span>

<span data-ttu-id="e95b0-p105">Der Textwert **true** gibt an, dass der Benutzer Unterordner im Ordner erstellen kann. Der Wert **false** gibt an, dass der Benutzer nicht Unterordner im Ordner erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="e95b0-p105">A text value of **true** indicates that the user can create subfolders in the folder. A value of **false** indicates that the user cannot create subfolders in the folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e95b0-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e95b0-126">Remarks</span></span>

<span data-ttu-id="e95b0-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="e95b0-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e95b0-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e95b0-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e95b0-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="e95b0-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e95b0-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e95b0-130">Schema Name</span></span>  <br/> |<span data-ttu-id="e95b0-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e95b0-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="e95b0-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e95b0-132">Validation File</span></span>  <br/> |<span data-ttu-id="e95b0-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e95b0-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e95b0-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e95b0-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="e95b0-135">False</span><span class="sxs-lookup"><span data-stu-id="e95b0-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e95b0-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e95b0-136">See also</span></span>



- [<span data-ttu-id="e95b0-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e95b0-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="e95b0-138">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="e95b0-138">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

