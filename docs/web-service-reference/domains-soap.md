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
description: Das Domains-Element stellt die Domänen Sammlung dar, die in einem GetDomainSettings-Vorgang (SOAP), die Domänen, die die Organisation in einen GetFederationInformation-Vorgang (SOAP) integriert hat, oder die Domänen mit einer Organisationsbeziehung zurückgegeben werden, die von GetOrganizationRelationshipSettings-Vorgang (SOAP) zurückgegeben werden.
ms.openlocfilehash: c56fb72841776c0060c1300b52b2f6a06b1ec0ed
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526305"
---
# <a name="domains-soap"></a><span data-ttu-id="d93ff-103">Domänen (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d93ff-103">Domains (SOAP)</span></span>

<span data-ttu-id="d93ff-104">Das **Domains** -Element stellt die Domänen Sammlung dar, die in einem [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md), die Domänen, die die Organisation in einen [GetFederationInformation-Vorgang (](getfederationinformation-operation-soap.md)SOAP) integriert hat, oder die Domänen mit einer Organisationsbeziehung zurückgegeben werden, die von [GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md)zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d93ff-104">The **Domains** element represents the domain collection that is returned in a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), the domains that the organization has federated in a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md), or the domains with an organization relationship as returned by [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md).</span></span>
  
```XML
<Domains>
   <Domain/>
</Domains>
```

 <span data-ttu-id="d93ff-105">**Domänen**</span><span class="sxs-lookup"><span data-stu-id="d93ff-105">**Domains**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d93ff-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d93ff-106">Attributes and elements</span></span>

<span data-ttu-id="d93ff-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d93ff-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d93ff-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d93ff-108">Attributes</span></span>

<span data-ttu-id="d93ff-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d93ff-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d93ff-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d93ff-110">Child elements</span></span>

|<span data-ttu-id="d93ff-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d93ff-111">**Element**</span></span>|<span data-ttu-id="d93ff-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d93ff-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d93ff-113">Domäne (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d93ff-113">Domain (SOAP)</span></span>](domain-soap.md) <br/> |<span data-ttu-id="d93ff-114">Stellt eine einzelne Domäne dar.</span><span class="sxs-lookup"><span data-stu-id="d93ff-114">Represents a single domain.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d93ff-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d93ff-115">Parent elements</span></span>

|<span data-ttu-id="d93ff-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="d93ff-116">**Element**</span></span>|<span data-ttu-id="d93ff-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d93ff-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d93ff-118">GetDomainSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d93ff-118">GetDomainSettingsRequest (SOAP)</span></span>](getdomainsettingsrequest-soap.md) <br/> |<span data-ttu-id="d93ff-119">Stellt eine [SOAP-Anforderung (GetDomainSettings Operation)](getdomainsettings-operation-soap.md) dar.</span><span class="sxs-lookup"><span data-stu-id="d93ff-119">Represents a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) request.</span></span>  <br/> |
|[<span data-ttu-id="d93ff-120">Antwort (GetFederationInformation) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d93ff-120">Response (GetFederationInformation) (SOAP)</span></span>](response-getfederationinformationsoap.md) <br/> |<span data-ttu-id="d93ff-121">Enthält die Antwortinformationen für den [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="d93ff-121">Contains the [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) response information.</span></span>  <br/> |
|[<span data-ttu-id="d93ff-122">GetOrganizationRelationshipSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d93ff-122">GetOrganizationRelationshipSettingsRequest (SOAP)</span></span>](getorganizationrelationshipsettingsrequest-soap.md) <br/> |<span data-ttu-id="d93ff-123">Stellt eine [SOAP-Anforderung (GetOrganizationRelationshipSettings Operation)](getorganizationrelationshipsettings-operation-soap.md) dar.</span><span class="sxs-lookup"><span data-stu-id="d93ff-123">Represents a [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d93ff-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="d93ff-124">Text value</span></span>

<span data-ttu-id="d93ff-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="d93ff-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d93ff-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d93ff-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d93ff-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="d93ff-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="d93ff-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d93ff-128">Schema Name</span></span>  <br/> |<span data-ttu-id="d93ff-129">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="d93ff-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="d93ff-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d93ff-130">Validation File</span></span>  <br/> |<span data-ttu-id="d93ff-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d93ff-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d93ff-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d93ff-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="d93ff-133">True</span><span class="sxs-lookup"><span data-stu-id="d93ff-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d93ff-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d93ff-134">See also</span></span>

- [<span data-ttu-id="d93ff-135">GetDomainSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d93ff-135">GetDomainSettingsRequest (SOAP)</span></span>](getdomainsettingsrequest-soap.md)  
- [<span data-ttu-id="d93ff-136">GetFederationInformationResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d93ff-136">GetFederationInformationResponse (SOAP)</span></span>](getfederationinformationresponse-soap.md)

