---
title: Request (GetDomainSettings) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 3ea026fc-74f1-4118-86ae-908ed4f82a4b
description: Das Request-Element enthält eine Anforderung zum Zurückgeben von Domäneneinstellungen.
ms.openlocfilehash: c5f666102be8aaeee001a23706732e9e6c44b560
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459588"
---
# <a name="request-getdomainsettings-soap"></a><span data-ttu-id="61886-103">Request (GetDomainSettings) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="61886-103">Request (GetDomainSettings) (SOAP)</span></span>

<span data-ttu-id="61886-104">Das **Request** -Element enthält eine Anforderung zum Zurückgeben von Domäneneinstellungen.</span><span class="sxs-lookup"><span data-stu-id="61886-104">The **Request** element contains a request to return domain settings.</span></span> 
  
```xml
<Request>
   <Domains/>
   <RequestedSettings/>
</Request>
```

 <span data-ttu-id="61886-105">**GetDomainSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="61886-105">**GetDomainSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="61886-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="61886-106">Attributes and elements</span></span>

<span data-ttu-id="61886-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="61886-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="61886-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="61886-108">Attributes</span></span>

<span data-ttu-id="61886-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="61886-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="61886-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="61886-110">Child elements</span></span>

|<span data-ttu-id="61886-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="61886-111">**Element**</span></span>|<span data-ttu-id="61886-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="61886-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="61886-113">Domänen (SOAP)</span><span class="sxs-lookup"><span data-stu-id="61886-113">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="61886-114">Stellt die Domänen dar, deren Konfigurationen in einem [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md) oder in den Domänen, die die Organisation in einem [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)Verbund hat, zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="61886-114">Represents the domains the configurations for which are returned in a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) or the domains the organization has federated in a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md).</span></span>  <br/> |
|[<span data-ttu-id="61886-115">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="61886-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="61886-116">Enthält die Namen der angeforderten Konfigurationseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="61886-116">Contains the names of the requested configuration settings.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="61886-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="61886-117">Parent elements</span></span>

|<span data-ttu-id="61886-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="61886-118">**Element**</span></span>|<span data-ttu-id="61886-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="61886-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="61886-120">GetDomainSettingsRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="61886-120">GetDomainSettingsRequestMessage (SOAP)</span></span>](getdomainsettingsrequestmessage-soap.md) <br/> |<span data-ttu-id="61886-121">Stellt eine [SOAP-Anforderung (GetDomainSettings Operation)](getdomainsettings-operation-soap.md)dar.</span><span class="sxs-lookup"><span data-stu-id="61886-121">Represents a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="61886-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="61886-122">Text value</span></span>

<span data-ttu-id="61886-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="61886-123">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="61886-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="61886-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61886-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="61886-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="61886-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="61886-126">Schema Name</span></span>  <br/> |<span data-ttu-id="61886-127">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="61886-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="61886-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="61886-128">Validation File</span></span>  <br/> |<span data-ttu-id="61886-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="61886-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="61886-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="61886-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="61886-131">True</span><span class="sxs-lookup"><span data-stu-id="61886-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="61886-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61886-132">See also</span></span>



[<span data-ttu-id="61886-133">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="61886-133">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

