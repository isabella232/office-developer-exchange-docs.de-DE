---
title: TargetApplicationUri (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e13c0edd-2ab1-49bb-a993-54a8db2dfbb9
description: Das TargetApplicationUri-Element definiert die URI-Zielanwendung. Das TargetApplicationUri-Element ist nur zur internen Verwendung. Dieses Element wird von Clients nicht verwendet.
ms.openlocfilehash: fa401d4c1e8c1460804f116d840fe21129957852
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839157"
---
# <a name="targetapplicationuri-soap"></a><span data-ttu-id="9d89b-105">TargetApplicationUri (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9d89b-105">TargetApplicationUri (SOAP)</span></span>

<span data-ttu-id="9d89b-106">Das **TargetApplicationUri** -Element definiert die URI-Zielanwendung.</span><span class="sxs-lookup"><span data-stu-id="9d89b-106">The **TargetApplicationUri** element defines the target application URI.</span></span> <span data-ttu-id="9d89b-107">Das **TargetApplicationUri** -Element ist nur zur internen Verwendung.</span><span class="sxs-lookup"><span data-stu-id="9d89b-107">The **TargetApplicationUri** element is for internal use only.</span></span> <span data-ttu-id="9d89b-108">Dieses Element wird von Clients nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9d89b-108">This element is not used by clients.</span></span> 
  
```XML
<TargetApplicationUri/>
```

 <span data-ttu-id="9d89b-109">**anyURI**</span><span class="sxs-lookup"><span data-stu-id="9d89b-109">**anyURI**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9d89b-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9d89b-110">Attributes and elements</span></span>

<span data-ttu-id="9d89b-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9d89b-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9d89b-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="9d89b-112">Attributes</span></span>

<span data-ttu-id="9d89b-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="9d89b-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9d89b-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9d89b-114">Child elements</span></span>

<span data-ttu-id="9d89b-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="9d89b-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9d89b-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9d89b-116">Parent elements</span></span>

|<span data-ttu-id="9d89b-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="9d89b-117">**Element**</span></span>|<span data-ttu-id="9d89b-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d89b-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9d89b-119">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9d89b-119">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="9d89b-120">Stellt eine Liste von organisationsbeziehungen für eine einzelne Organisation</span><span class="sxs-lookup"><span data-stu-id="9d89b-120">Represents a list of organization relationships for a single organization</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d89b-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9d89b-121">Remarks</span></span>

<span data-ttu-id="9d89b-122">Dieses Element definiert den Ziel-URI der externen Organisation.</span><span class="sxs-lookup"><span data-stu-id="9d89b-122">This element defines the target URI of the external organization.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9d89b-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9d89b-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d89b-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d89b-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="9d89b-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9d89b-125">Schema Name</span></span>  <br/> |<span data-ttu-id="9d89b-126">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="9d89b-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="9d89b-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9d89b-127">Validation File</span></span>  <br/> |<span data-ttu-id="9d89b-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9d89b-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9d89b-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9d89b-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="9d89b-130">True</span><span class="sxs-lookup"><span data-stu-id="9d89b-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9d89b-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d89b-131">See also</span></span>



[<span data-ttu-id="9d89b-132">GetOrganizationRelationshipSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9d89b-132">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

