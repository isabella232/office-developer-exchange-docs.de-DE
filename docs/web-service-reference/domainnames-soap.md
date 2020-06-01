---
title: Domainnamen (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 79ffc3f9-25c4-40b5-84ce-09a3c5f892fa
description: Das Domainnamen-Element stellt die Domain Names-Auflistung dar. Das Domainnamen-Element ist nur für die interne Verwendung. Dieses Element wird nicht von Clients verwendet.
ms.openlocfilehash: 0b425b3cd4c0e7cb2427920d61feb04010a3b123
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458418"
---
# <a name="domainnames-soap"></a><span data-ttu-id="e244a-105">Domainnamen (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e244a-105">DomainNames (SOAP)</span></span>

<span data-ttu-id="e244a-106">Das **Domainnamen** -Element stellt die Domain Names-Auflistung dar.</span><span class="sxs-lookup"><span data-stu-id="e244a-106">The **DomainNames** element represents the domain names collection.</span></span> <span data-ttu-id="e244a-107">Das **Domainnamen** -Element ist nur für die interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="e244a-107">The **DomainNames** element is for internal use only.</span></span> <span data-ttu-id="e244a-108">Dieses Element wird nicht von Clients verwendet.</span><span class="sxs-lookup"><span data-stu-id="e244a-108">This element is not used by clients.</span></span> 
  
```XML
<DomainNames>
    <Domains/>
</DomainNames>
```

 <span data-ttu-id="e244a-109">**Domainnamen**</span><span class="sxs-lookup"><span data-stu-id="e244a-109">**DomainNames**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e244a-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e244a-110">Attributes and elements</span></span>

<span data-ttu-id="e244a-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e244a-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e244a-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="e244a-112">Attributes</span></span>

<span data-ttu-id="e244a-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="e244a-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e244a-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e244a-114">Child elements</span></span>

|<span data-ttu-id="e244a-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="e244a-115">**Element**</span></span>|<span data-ttu-id="e244a-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e244a-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e244a-117">Domänen (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e244a-117">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="e244a-118">Stellt eine Auflistung von Domänen dar, die vom [GetDomainSettings-Vorgang (](getdomainsettings-operation-soap.md)SOAP), [GetFederationInformation-Vorgang (](getfederationinformation-operation-soap.md)SOAP) oder dem [GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md)zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e244a-118">Represents a collection of domains that are returned from the [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md), or the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e244a-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e244a-119">Parent elements</span></span>

|<span data-ttu-id="e244a-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="e244a-120">**Element**</span></span>|<span data-ttu-id="e244a-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e244a-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e244a-122">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e244a-122">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="e244a-123">Stellt eine Liste von Organisationsbeziehungen für eine einzelne Organisation dar.</span><span class="sxs-lookup"><span data-stu-id="e244a-123">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e244a-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="e244a-124">Text value</span></span>

<span data-ttu-id="e244a-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="e244a-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e244a-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e244a-126">Remarks</span></span>

<span data-ttu-id="e244a-127">Dieses Element stellt die SMTP-Domänen der externen Organisationen dar.</span><span class="sxs-lookup"><span data-stu-id="e244a-127">This element represents the SMTP domains of the external organizations.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e244a-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e244a-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e244a-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="e244a-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="e244a-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e244a-130">Schema Name</span></span>  <br/> |<span data-ttu-id="e244a-131">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="e244a-131">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="e244a-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e244a-132">Validation File</span></span>  <br/> |<span data-ttu-id="e244a-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="e244a-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e244a-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e244a-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="e244a-135">True</span><span class="sxs-lookup"><span data-stu-id="e244a-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e244a-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e244a-136">See also</span></span>

- [<span data-ttu-id="e244a-137">GetOrganizationRelationshipSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e244a-137">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

