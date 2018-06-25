---
title: TargetAutodiscoverEpr (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fdb9cc7a-cf0a-431b-9f6f-5f1db1792db7
description: Das Element TargetAutodiscoverEpr stellt die TargetAutodiscoverEpr-Eigenschaft. Das TargetAutodiscoverEpr-Element ist nur zur internen Verwendung. Dieses Element wird von Clients nicht verwendet.
ms.openlocfilehash: 0b28444727e21a98925b6d1062bcbbac62c68981
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839158"
---
# <a name="targetautodiscoverepr-soap"></a><span data-ttu-id="9d273-105">TargetAutodiscoverEpr (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9d273-105">TargetAutodiscoverEpr (SOAP)</span></span>

<span data-ttu-id="9d273-106">Das Element **TargetAutodiscoverEpr** stellt die **TargetAutodiscoverEpr** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="9d273-106">The **TargetAutodiscoverEpr** element represents the **TargetAutodiscoverEpr** property.</span></span> <span data-ttu-id="9d273-107">Das **TargetAutodiscoverEpr** -Element ist nur zur internen Verwendung.</span><span class="sxs-lookup"><span data-stu-id="9d273-107">The **TargetAutodiscoverEpr** element is for internal use only.</span></span> <span data-ttu-id="9d273-108">Dieses Element wird von Clients nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9d273-108">This element is not used by clients.</span></span> 
  
```XML
<TargetAutodiscoverEpr/>
```

 <span data-ttu-id="9d273-109">**anyURI**</span><span class="sxs-lookup"><span data-stu-id="9d273-109">**anyURI**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9d273-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9d273-110">Attributes and elements</span></span>

<span data-ttu-id="9d273-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9d273-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9d273-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="9d273-112">Attributes</span></span>

<span data-ttu-id="9d273-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="9d273-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9d273-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9d273-114">Child elements</span></span>

<span data-ttu-id="9d273-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="9d273-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9d273-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9d273-116">Parent elements</span></span>

|<span data-ttu-id="9d273-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="9d273-117">**Element**</span></span>|<span data-ttu-id="9d273-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d273-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9d273-119">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9d273-119">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="9d273-120">Stellt eine Liste von organisationsbeziehungen für eine einzelne Organisation.</span><span class="sxs-lookup"><span data-stu-id="9d273-120">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9d273-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="9d273-121">Text value</span></span>

<span data-ttu-id="9d273-122">Der Textwert für dieses Element ist ein URI (uniform Resource Identifier) für die organisationsbeziehung.</span><span class="sxs-lookup"><span data-stu-id="9d273-122">The text value for this element is a uniform resource identifier (URI) for the organization relationship.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9d273-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9d273-123">Remarks</span></span>

<span data-ttu-id="9d273-124">Dieses Element gibt den AutoErmittlungsdienst-URL des Servers für die externe Organisation an.</span><span class="sxs-lookup"><span data-stu-id="9d273-124">This element specifies the Autodiscover URL of the server for the external organization.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="9d273-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9d273-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d273-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d273-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="9d273-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9d273-127">Schema Name</span></span>  <br/> |<span data-ttu-id="9d273-128">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="9d273-128">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="9d273-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9d273-129">Validation File</span></span>  <br/> |<span data-ttu-id="9d273-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9d273-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9d273-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9d273-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="9d273-132">True</span><span class="sxs-lookup"><span data-stu-id="9d273-132">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9d273-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d273-133">See also</span></span>



[<span data-ttu-id="9d273-134">GetOrganizationRelationshipSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9d273-134">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

