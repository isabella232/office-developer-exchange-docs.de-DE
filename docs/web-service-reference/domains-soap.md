---
title: Domänen (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 5f81d1b7-c6a4-456f-9935-13d04a3d92d7
description: Das Domänen-Element darstellt, die Domäne-Auflistung, die zurückgegeben wird, in einen GetDomainSettings-Vorgang (SOAP), die Domänen, die die Organisation in einem Vorgang GetFederationInformation (SOAP) federated hat oder die Domänen mit einer organisationsbeziehung als von GetOrganizationRelationshipSettings-Vorgang (SOAP) zurückgegeben.
ms.openlocfilehash: 7a21a3a09516de2d1c38021ca3ccd2161d9cdd1e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758098"
---
# <a name="domains-soap"></a><span data-ttu-id="7392a-103">Domänen (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7392a-103">Domains (SOAP)</span></span>

<span data-ttu-id="7392a-104">Das **Domänen** -Element darstellt, die Domäne-Auflistung, die zurückgegeben wird, in einen [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md), die Domänen, die die Organisation in einem [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)federated hat oder die Domänen mit einer organisationsbeziehung von [GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7392a-104">The **Domains** element represents the domain collection that is returned in a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), the domains that the organization has federated in a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md), or the domains with an organization relationship as returned by [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md).</span></span>
  
```XML
<Domains>
   <Domain/>
</Domains>
```

 <span data-ttu-id="7392a-105">**Domänen**</span><span class="sxs-lookup"><span data-stu-id="7392a-105">**Domains**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7392a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7392a-106">Attributes and elements</span></span>

<span data-ttu-id="7392a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7392a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7392a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7392a-108">Attributes</span></span>

<span data-ttu-id="7392a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7392a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7392a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7392a-110">Child elements</span></span>

|<span data-ttu-id="7392a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="7392a-111">**Element**</span></span>|<span data-ttu-id="7392a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7392a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7392a-113">Domäne (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7392a-113">Domain (SOAP)</span></span>](domain-soap.md) <br/> |<span data-ttu-id="7392a-114">Stellt eine einzelne Domäne.</span><span class="sxs-lookup"><span data-stu-id="7392a-114">Represents a single domain.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7392a-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7392a-115">Parent elements</span></span>

|<span data-ttu-id="7392a-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="7392a-116">**Element**</span></span>|<span data-ttu-id="7392a-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7392a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7392a-118">GetDomainSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7392a-118">GetDomainSettingsRequest (SOAP)</span></span>](getdomainsettingsrequest-soap.md) <br/> |<span data-ttu-id="7392a-119">Stellt eine Anforderung [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="7392a-119">Represents a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) request.</span></span>  <br/> |
|[<span data-ttu-id="7392a-120">Antwort (GetFederationInformation) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7392a-120">Response (GetFederationInformation) (SOAP)</span></span>](response-getfederationinformationsoap.md) <br/> |<span data-ttu-id="7392a-121">Enthält die Antwort-Informationen [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="7392a-121">Contains the [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) response information.</span></span>  <br/> |
|[<span data-ttu-id="7392a-122">GetOrganizationRelationshipSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7392a-122">GetOrganizationRelationshipSettingsRequest (SOAP)</span></span>](getorganizationrelationshipsettingsrequest-soap.md) <br/> |<span data-ttu-id="7392a-123">Stellt eine Anforderung [GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="7392a-123">Represents a [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7392a-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="7392a-124">Text value</span></span>

<span data-ttu-id="7392a-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="7392a-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7392a-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7392a-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7392a-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="7392a-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="7392a-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7392a-128">Schema Name</span></span>  <br/> |<span data-ttu-id="7392a-129">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="7392a-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="7392a-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7392a-130">Validation File</span></span>  <br/> |<span data-ttu-id="7392a-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7392a-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7392a-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7392a-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="7392a-133">True</span><span class="sxs-lookup"><span data-stu-id="7392a-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7392a-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7392a-134">See also</span></span>

- [<span data-ttu-id="7392a-135">GetDomainSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7392a-135">GetDomainSettingsRequest (SOAP)</span></span>](getdomainsettingsrequest-soap.md)  
- [<span data-ttu-id="7392a-136">GetFederationInformationResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7392a-136">GetFederationInformationResponse (SOAP)</span></span>](getfederationinformationresponse-soap.md)

