---
title: IsFolderVisible
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsFolderVisible
api_type:
- schema
ms.assetid: dd611fb5-9424-4ff9-bb27-c882c73c0c74
description: Das IsFolderVisible-Element gibt an, ob ein Benutzer einen Ordner anzeigen kann. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 27a6bca9ae71bc93de6c22cb87c8d582025144e9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830019"
---
# <a name="isfoldervisible"></a><span data-ttu-id="ca7b4-104">IsFolderVisible</span><span class="sxs-lookup"><span data-stu-id="ca7b4-104">IsFolderVisible</span></span>

<span data-ttu-id="ca7b4-105">Das **IsFolderVisible** -Element gibt an, ob ein Benutzer einen Ordner anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="ca7b4-105">The **IsFolderVisible** element indicates whether a user can view a folder.</span></span> <span data-ttu-id="ca7b4-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ca7b4-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<IsFolderVisible/>
```

 <span data-ttu-id="ca7b4-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ca7b4-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ca7b4-108">Attributes and elements</span></span>

<span data-ttu-id="ca7b4-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ca7b4-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ca7b4-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="ca7b4-110">Attributes</span></span>

<span data-ttu-id="ca7b4-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ca7b4-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ca7b4-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ca7b4-112">Child elements</span></span>

<span data-ttu-id="ca7b4-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="ca7b4-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ca7b4-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ca7b4-114">Parent elements</span></span>

|<span data-ttu-id="ca7b4-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-115">**Element**</span></span>|<span data-ttu-id="ca7b4-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ca7b4-117">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="ca7b4-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="ca7b4-p103">Definiert den Zugriff, den ein Benutzer verfügt in einen Ordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ca7b4-p103">Defines the access that a user has to a folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="ca7b4-120">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="ca7b4-120">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="ca7b4-p104">Definiert den, den ein Benutzer hat Zugriff auf einen Kalenderordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ca7b4-p104">Defines the access that a user has to a Calendar folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ca7b4-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="ca7b4-123">Text value</span></span>

<span data-ttu-id="ca7b4-124">Der Textwert **true** gibt an, dass der Benutzer den Ordner anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="ca7b4-124">A text value of **true** indicates that the user can view the folder.</span></span> <span data-ttu-id="ca7b4-125">Der Wert **false** gibt an, dass der Benutzer den Ordner nicht anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="ca7b4-125">A value of **false** indicates that the user cannot view the folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ca7b4-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ca7b4-126">Remarks</span></span>

<span data-ttu-id="ca7b4-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ca7b4-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ca7b4-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ca7b4-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ca7b4-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="ca7b4-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ca7b4-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ca7b4-130">Schema Name</span></span>  <br/> |<span data-ttu-id="ca7b4-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ca7b4-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="ca7b4-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ca7b4-132">Validation File</span></span>  <br/> |<span data-ttu-id="ca7b4-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ca7b4-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ca7b4-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ca7b4-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="ca7b4-135">False</span><span class="sxs-lookup"><span data-stu-id="ca7b4-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ca7b4-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca7b4-136">See also</span></span>



- [<span data-ttu-id="ca7b4-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ca7b4-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="ca7b4-138">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="ca7b4-138">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

