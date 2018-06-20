---
title: GetOrganizationRelationshipSettingsRequest (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e8aa3b3-4bfc-40c3-b96b-9f7062b09309
description: Das GetOrganizationRelationshipSettingsRequest-Element stellt die Parameter für einen Aufruf der GetOrganizationRelationshipSettings-Vorgang (SOAP) Vorgang dar. Das GetOrganizationRelationshipSettingsRequest-Element ist nur zur internen Verwendung. Dieses Element wird von Clients nicht verwendet.
ms.openlocfilehash: 451506d53212ddca416f5b797624688f511988d0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758747"
---
# <a name="getorganizationrelationshipsettingsrequest-soap"></a><span data-ttu-id="fac6e-105">GetOrganizationRelationshipSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="fac6e-105">GetOrganizationRelationshipSettingsRequest (SOAP)</span></span>

<span data-ttu-id="fac6e-106">Das **GetOrganizationRelationshipSettingsRequest** -Element stellt die Parameter für einen Aufruf der [GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md) Vorgang dar.</span><span class="sxs-lookup"><span data-stu-id="fac6e-106">The **GetOrganizationRelationshipSettingsRequest** element represents the parameters of a call to the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) operation.</span></span> <span data-ttu-id="fac6e-107">Das **GetOrganizationRelationshipSettingsRequest** -Element ist nur zur internen Verwendung.</span><span class="sxs-lookup"><span data-stu-id="fac6e-107">The **GetOrganizationRelationshipSettingsRequest** element is for internal use only.</span></span> <span data-ttu-id="fac6e-108">Dieses Element wird von Clients nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fac6e-108">This element is not used by clients.</span></span> 
  
```XML
<GetOrganizationRelationshipSettingsRequest>
   <Domains/>
</GetOrganizationRelationshipSettingsRequest>
```

 <span data-ttu-id="fac6e-109">**GetOrganizationRelationshipSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="fac6e-109">**GetOrganizationRelationshipSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fac6e-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fac6e-110">Attributes and elements</span></span>

<span data-ttu-id="fac6e-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fac6e-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fac6e-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="fac6e-112">Attributes</span></span>

<span data-ttu-id="fac6e-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="fac6e-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fac6e-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fac6e-114">Child elements</span></span>

|<span data-ttu-id="fac6e-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="fac6e-115">**Element**</span></span>|<span data-ttu-id="fac6e-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fac6e-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fac6e-117">Domänen (SOAP)</span><span class="sxs-lookup"><span data-stu-id="fac6e-117">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="fac6e-118">Stellt eine Sammlung von Bezeichnern Domäne dar.</span><span class="sxs-lookup"><span data-stu-id="fac6e-118">Represents a collection of domain identifiers.</span></span>  <br/> |
|||
   
### <a name="parent-elements"></a><span data-ttu-id="fac6e-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fac6e-119">Parent elements</span></span>

<span data-ttu-id="fac6e-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="fac6e-120">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fac6e-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="fac6e-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fac6e-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="fac6e-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="fac6e-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fac6e-123">Schema Name</span></span>  <br/> |<span data-ttu-id="fac6e-124">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="fac6e-124">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="fac6e-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fac6e-125">Validation File</span></span>  <br/> |<span data-ttu-id="fac6e-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="fac6e-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fac6e-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="fac6e-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="fac6e-128">True</span><span class="sxs-lookup"><span data-stu-id="fac6e-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fac6e-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fac6e-129">See also</span></span>



[<span data-ttu-id="fac6e-130">GetOrganizationRelationshipSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="fac6e-130">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

