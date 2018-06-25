---
title: Anforderung (GetDomainSettings) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 3ea026fc-74f1-4118-86ae-908ed4f82a4b
description: Das angeforderte Element enthält eine Anforderung an die domäneneinstellungen zurückzugeben.
ms.openlocfilehash: 71a6072d476fd665dad8b0c0fe388a40db56e059
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831135"
---
# <a name="request-getdomainsettings-soap"></a><span data-ttu-id="9950d-103">Anforderung (GetDomainSettings) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9950d-103">Request (GetDomainSettings) (SOAP)</span></span>

<span data-ttu-id="9950d-104">Das **angeforderte** Element enthält eine Anforderung an die domäneneinstellungen zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="9950d-104">The **Request** element contains a request to return domain settings.</span></span> 
  
```xml
<Request>
   <Domains/>
   <RequestedSettings/>
</Request>
```

 <span data-ttu-id="9950d-105">**GetDomainSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="9950d-105">**GetDomainSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9950d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9950d-106">Attributes and elements</span></span>

<span data-ttu-id="9950d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9950d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9950d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9950d-108">Attributes</span></span>

<span data-ttu-id="9950d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9950d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9950d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9950d-110">Child elements</span></span>

|<span data-ttu-id="9950d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="9950d-111">**Element**</span></span>|<span data-ttu-id="9950d-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9950d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9950d-113">Domänen (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9950d-113">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="9950d-114">Stellt die Domänen, die die Konfigurationen für die in einem [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md) zurückgegeben werden oder die Domänen, die die Organisation in einem [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)federated hat dar.</span><span class="sxs-lookup"><span data-stu-id="9950d-114">Represents the domains the configurations for which are returned in a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) or the domains the organization has federated in a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md).</span></span>  <br/> |
|[<span data-ttu-id="9950d-115">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9950d-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="9950d-116">Enthält die Namen der angeforderten Konfigurationseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="9950d-116">Contains the names of the requested configuration settings.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9950d-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9950d-117">Parent elements</span></span>

|<span data-ttu-id="9950d-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="9950d-118">**Element**</span></span>|<span data-ttu-id="9950d-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9950d-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9950d-120">GetDomainSettingsRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9950d-120">GetDomainSettingsRequestMessage (SOAP)</span></span>](getdomainsettingsrequestmessage-soap.md) <br/> |<span data-ttu-id="9950d-121">Stellt eine Anforderung [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md).</span><span class="sxs-lookup"><span data-stu-id="9950d-121">Represents a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9950d-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="9950d-122">Text value</span></span>

<span data-ttu-id="9950d-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="9950d-123">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9950d-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9950d-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9950d-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="9950d-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="9950d-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9950d-126">Schema Name</span></span>  <br/> |<span data-ttu-id="9950d-127">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="9950d-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="9950d-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9950d-128">Validation File</span></span>  <br/> |<span data-ttu-id="9950d-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9950d-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9950d-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9950d-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="9950d-131">True</span><span class="sxs-lookup"><span data-stu-id="9950d-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9950d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9950d-132">See also</span></span>



[<span data-ttu-id="9950d-133">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9950d-133">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

