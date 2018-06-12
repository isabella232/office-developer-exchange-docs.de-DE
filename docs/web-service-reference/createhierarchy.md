---
title: CreateHierarchy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateHierarchy
api_type:
- schema
ms.assetid: 630b5610-1c19-4d4a-a5df-8cebb9afd2f4
description: Das CreateHierarchy-Element gibt an, ob ein Client eine Hierarchietabelle erstellen kann. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: a5b428fe453dbc31761309b017367a7d25a01b76
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757765"
---
# <a name="createhierarchy"></a><span data-ttu-id="99999-104">CreateHierarchy</span><span class="sxs-lookup"><span data-stu-id="99999-104">CreateHierarchy</span></span>

<span data-ttu-id="99999-105">Das **CreateHierarchy** -Element gibt an, ob ein Client eine Hierarchietabelle erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="99999-105">The **CreateHierarchy** element indicates whether a client can create a hierarchy table.</span></span> <span data-ttu-id="99999-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="99999-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<CreateHierarchy>true or false</CreateHierarchy>
```

 <span data-ttu-id="99999-107">**boolean**</span><span class="sxs-lookup"><span data-stu-id="99999-107">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="99999-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="99999-108">Attributes and elements</span></span>

<span data-ttu-id="99999-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="99999-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="99999-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="99999-110">Attributes</span></span>

<span data-ttu-id="99999-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="99999-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="99999-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="99999-112">Child elements</span></span>

<span data-ttu-id="99999-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="99999-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="99999-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="99999-114">Parent elements</span></span>

|<span data-ttu-id="99999-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="99999-115">**Element**</span></span>|<span data-ttu-id="99999-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="99999-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="99999-117">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="99999-117">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="99999-118">Die Rechte des Clients basierend auf die berechtigungseinstellungen für das Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="99999-118">Contains the rights of the client based on the permission settings for the item or folder.</span></span> <span data-ttu-id="99999-119">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="99999-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="99999-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="99999-120">Text value</span></span>

<span data-ttu-id="99999-121">Der Textwert **true** gibt an, dass ein Client eine Hierarchietabelle erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="99999-121">A text value of **true** indicates that a client can create a hierarchy table.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="99999-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99999-122">Remarks</span></span>

<span data-ttu-id="99999-123">Diese Eigenschaft wird nur auf Folder-Objekten verwendet.</span><span class="sxs-lookup"><span data-stu-id="99999-123">This property is only used on folder objects.</span></span>
  
<span data-ttu-id="99999-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="99999-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="99999-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="99999-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="99999-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="99999-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="99999-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="99999-127">Schema Name</span></span>  <br/> |<span data-ttu-id="99999-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="99999-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="99999-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="99999-129">Validation File</span></span>  <br/> |<span data-ttu-id="99999-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="99999-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="99999-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="99999-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="99999-132">False</span><span class="sxs-lookup"><span data-stu-id="99999-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="99999-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99999-133">See also</span></span>



- [<span data-ttu-id="99999-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="99999-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="99999-135">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="99999-135">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

