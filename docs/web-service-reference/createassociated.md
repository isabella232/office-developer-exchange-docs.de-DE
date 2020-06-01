---
title: Createassociated
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateAssociated
api_type:
- schema
ms.assetid: 742a6136-6015-4924-bae4-f3868127e966
description: Das createassociated-Element gibt an, ob ein Client eine zugeordnete Inhaltstabelle erstellen kann. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: e88d7670fd9ef848221dab8cc145395bcb11e5bf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460792"
---
# <a name="createassociated"></a><span data-ttu-id="698be-104">Createassociated</span><span class="sxs-lookup"><span data-stu-id="698be-104">CreateAssociated</span></span>

<span data-ttu-id="698be-105">Das **createassociated** -Element gibt an, ob ein Client eine zugeordnete Inhaltstabelle erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="698be-105">The **CreateAssociated** element indicates whether a client can create an associated contents table.</span></span> <span data-ttu-id="698be-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="698be-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<CreateAssociated>true or false</CreateAssociated>
```

 <span data-ttu-id="698be-107">**boolean**</span><span class="sxs-lookup"><span data-stu-id="698be-107">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="698be-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="698be-108">Attributes and elements</span></span>

<span data-ttu-id="698be-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="698be-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="698be-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="698be-110">Attributes</span></span>

<span data-ttu-id="698be-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="698be-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="698be-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="698be-112">Child elements</span></span>

<span data-ttu-id="698be-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="698be-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="698be-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="698be-114">Parent elements</span></span>

|<span data-ttu-id="698be-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="698be-115">**Element**</span></span>|<span data-ttu-id="698be-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="698be-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="698be-117">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="698be-117">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="698be-118">Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner.</span><span class="sxs-lookup"><span data-stu-id="698be-118">Contains the rights of the client based on the permission settings for the item or folder.</span></span> <span data-ttu-id="698be-119">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="698be-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="698be-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="698be-120">Text value</span></span>

<span data-ttu-id="698be-121">Der Textwert **true** gibt an, dass ein Client eine zugeordnete Inhaltstabelle erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="698be-121">A text value of **true** indicates that a client can create an associated contents table.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="698be-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="698be-122">Remarks</span></span>

<span data-ttu-id="698be-123">Diese Eigenschaft wird nur für Folder-Objekte verwendet.</span><span class="sxs-lookup"><span data-stu-id="698be-123">This property is only used on folder objects.</span></span>
  
<span data-ttu-id="698be-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="698be-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="698be-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="698be-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="698be-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="698be-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="698be-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="698be-127">Schema Name</span></span>  <br/> |<span data-ttu-id="698be-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="698be-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="698be-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="698be-129">Validation File</span></span>  <br/> |<span data-ttu-id="698be-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="698be-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="698be-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="698be-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="698be-132">False</span><span class="sxs-lookup"><span data-stu-id="698be-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="698be-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="698be-133">See also</span></span>



- [<span data-ttu-id="698be-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="698be-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="698be-135">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="698be-135">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

