---
title: Createhierarchy
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
description: Das createhierarchy-Element gibt an, ob ein Client eine Hierarchietabelle erstellen kann. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 3fb0c34a8a148cc8336c70d643a21ecb6fef30b5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457522"
---
# <a name="createhierarchy"></a><span data-ttu-id="377c8-104">Createhierarchy</span><span class="sxs-lookup"><span data-stu-id="377c8-104">CreateHierarchy</span></span>

<span data-ttu-id="377c8-105">Das **createhierarchy** -Element gibt an, ob ein Client eine Hierarchietabelle erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="377c8-105">The **CreateHierarchy** element indicates whether a client can create a hierarchy table.</span></span> <span data-ttu-id="377c8-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="377c8-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<CreateHierarchy>true or false</CreateHierarchy>
```

 <span data-ttu-id="377c8-107">**boolean**</span><span class="sxs-lookup"><span data-stu-id="377c8-107">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="377c8-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="377c8-108">Attributes and elements</span></span>

<span data-ttu-id="377c8-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="377c8-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="377c8-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="377c8-110">Attributes</span></span>

<span data-ttu-id="377c8-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="377c8-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="377c8-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="377c8-112">Child elements</span></span>

<span data-ttu-id="377c8-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="377c8-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="377c8-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="377c8-114">Parent elements</span></span>

|<span data-ttu-id="377c8-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="377c8-115">**Element**</span></span>|<span data-ttu-id="377c8-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="377c8-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="377c8-117">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="377c8-117">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="377c8-118">Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner.</span><span class="sxs-lookup"><span data-stu-id="377c8-118">Contains the rights of the client based on the permission settings for the item or folder.</span></span> <span data-ttu-id="377c8-119">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="377c8-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="377c8-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="377c8-120">Text value</span></span>

<span data-ttu-id="377c8-121">Der Textwert **true** gibt an, dass ein Client eine Hierarchietabelle erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="377c8-121">A text value of **true** indicates that a client can create a hierarchy table.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="377c8-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="377c8-122">Remarks</span></span>

<span data-ttu-id="377c8-123">Diese Eigenschaft wird nur für Folder-Objekte verwendet.</span><span class="sxs-lookup"><span data-stu-id="377c8-123">This property is only used on folder objects.</span></span>
  
<span data-ttu-id="377c8-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="377c8-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="377c8-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="377c8-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="377c8-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="377c8-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="377c8-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="377c8-127">Schema Name</span></span>  <br/> |<span data-ttu-id="377c8-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="377c8-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="377c8-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="377c8-129">Validation File</span></span>  <br/> |<span data-ttu-id="377c8-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="377c8-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="377c8-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="377c8-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="377c8-132">False</span><span class="sxs-lookup"><span data-stu-id="377c8-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="377c8-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="377c8-133">See also</span></span>



- [<span data-ttu-id="377c8-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="377c8-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="377c8-135">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="377c8-135">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

