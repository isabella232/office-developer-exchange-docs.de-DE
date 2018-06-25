---
title: DomainNames (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 79ffc3f9-25c4-40b5-84ce-09a3c5f892fa
description: Das Element DomainNames stellt die Domain Names-Auflistung dar. Das DomainNames-Element ist nur zur internen Verwendung. Dieses Element wird von Clients nicht verwendet.
ms.openlocfilehash: 45d256f3d5a57028a04572ad67d4be0786ca39e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758089"
---
# <a name="domainnames-soap"></a><span data-ttu-id="05a5e-105">DomainNames (SOAP)</span><span class="sxs-lookup"><span data-stu-id="05a5e-105">DomainNames (SOAP)</span></span>

<span data-ttu-id="05a5e-106">Das Element **DomainNames** stellt die Domain Names-Auflistung dar.</span><span class="sxs-lookup"><span data-stu-id="05a5e-106">The **DomainNames** element represents the domain names collection.</span></span> <span data-ttu-id="05a5e-107">Das **DomainNames** -Element ist nur zur internen Verwendung.</span><span class="sxs-lookup"><span data-stu-id="05a5e-107">The **DomainNames** element is for internal use only.</span></span> <span data-ttu-id="05a5e-108">Dieses Element wird von Clients nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="05a5e-108">This element is not used by clients.</span></span> 
  
```XML
<DomainNames>
    <Domains/>
</DomainNames>
```

 <span data-ttu-id="05a5e-109">**DomainNames**</span><span class="sxs-lookup"><span data-stu-id="05a5e-109">**DomainNames**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="05a5e-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="05a5e-110">Attributes and elements</span></span>

<span data-ttu-id="05a5e-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="05a5e-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="05a5e-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="05a5e-112">Attributes</span></span>

<span data-ttu-id="05a5e-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="05a5e-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="05a5e-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="05a5e-114">Child elements</span></span>

|<span data-ttu-id="05a5e-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="05a5e-115">**Element**</span></span>|<span data-ttu-id="05a5e-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="05a5e-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="05a5e-117">Domänen (SOAP)</span><span class="sxs-lookup"><span data-stu-id="05a5e-117">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="05a5e-118">Stellt eine Sammlung von Domänen, die von den [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md), [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)oder den [GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md)zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="05a5e-118">Represents a collection of domains that are returned from the [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md), or the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="05a5e-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="05a5e-119">Parent elements</span></span>

|<span data-ttu-id="05a5e-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="05a5e-120">**Element**</span></span>|<span data-ttu-id="05a5e-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="05a5e-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="05a5e-122">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="05a5e-122">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="05a5e-123">Stellt eine Liste von organisationsbeziehungen für eine einzelne Organisation.</span><span class="sxs-lookup"><span data-stu-id="05a5e-123">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="05a5e-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="05a5e-124">Text value</span></span>

<span data-ttu-id="05a5e-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="05a5e-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="05a5e-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="05a5e-126">Remarks</span></span>

<span data-ttu-id="05a5e-127">Dieses Element stellt die SMTP-Domänen der externen Organisationen.</span><span class="sxs-lookup"><span data-stu-id="05a5e-127">This element represents the SMTP domains of the external organizations.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="05a5e-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="05a5e-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="05a5e-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="05a5e-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="05a5e-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="05a5e-130">Schema Name</span></span>  <br/> |<span data-ttu-id="05a5e-131">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="05a5e-131">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="05a5e-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="05a5e-132">Validation File</span></span>  <br/> |<span data-ttu-id="05a5e-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="05a5e-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="05a5e-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="05a5e-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="05a5e-135">True</span><span class="sxs-lookup"><span data-stu-id="05a5e-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="05a5e-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05a5e-136">See also</span></span>

- [<span data-ttu-id="05a5e-137">GetOrganizationRelationshipSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="05a5e-137">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

