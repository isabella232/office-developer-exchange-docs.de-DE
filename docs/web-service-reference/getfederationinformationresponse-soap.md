---
title: GetFederationInformationResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 2033c14f-dcc8-43c2-9fd9-a51946ec7055
description: Das GetFederationInformationResponse-Element enthält die GetFederationInformation-Vorgang (SOAP)-Antwort.
ms.openlocfilehash: c9e65a2b1759946b8493b3c730f08df6fe353fd8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460043"
---
# <a name="getfederationinformationresponse-soap"></a><span data-ttu-id="e68ad-103">GetFederationInformationResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e68ad-103">GetFederationInformationResponse (SOAP)</span></span>

<span data-ttu-id="e68ad-104">Das **GetFederationInformationResponse** -Element enthält die [GetFederationInformation-Vorgang (SOAP)-](getfederationinformation-operation-soap.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="e68ad-104">The **GetFederationInformationResponse** element contains the [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) response.</span></span> 
  
```XML
<GetFederationInformationResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <TokenIssuers/>
   <ApplicationUri/>
   <Domains/>
</GetFederationInformationResponse>
```

 <span data-ttu-id="e68ad-105">**GetFederationInformationResponse**</span><span class="sxs-lookup"><span data-stu-id="e68ad-105">**GetFederationInformationResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e68ad-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e68ad-106">Attributes and elements</span></span>

<span data-ttu-id="e68ad-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e68ad-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e68ad-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e68ad-108">Attributes</span></span>

<span data-ttu-id="e68ad-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e68ad-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e68ad-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e68ad-110">Child elements</span></span>

|<span data-ttu-id="e68ad-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e68ad-111">**Element**</span></span>|<span data-ttu-id="e68ad-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e68ad-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e68ad-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e68ad-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="e68ad-114">Stellt einen Fehlercode dar, der vom AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e68ad-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="e68ad-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e68ad-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="e68ad-116">Stellt eine Meldung dar, die einem Fehlercode zugeordnet ist, der vom AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e68ad-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="e68ad-117">ApplicationUri (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e68ad-117">ApplicationUri (SOAP)</span></span>](applicationuri-soap.md) <br/> |<span data-ttu-id="e68ad-118">Definiert den Speicherort einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e68ad-118">Defines the location of an application.</span></span>  <br/> |
|[<span data-ttu-id="e68ad-119">TokenIssuers (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e68ad-119">TokenIssuers (SOAP)</span></span>](tokenissuers-soap.md) <br/> |<span data-ttu-id="e68ad-120">Stellt eine Auflistung von Sicherheitstoken dar, die Dienst Bezeichner und Endpunkte des Sicherheitstokens enthalten.</span><span class="sxs-lookup"><span data-stu-id="e68ad-120">Represents a collection of security tokens, which contain security token service identifiers and endpoints.</span></span>  <br/> |
|[<span data-ttu-id="e68ad-121">Domänen (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e68ad-121">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="e68ad-122">Stellt die Domänen dar, deren Konfigurationen in einem **GetDomainSettings** -Vorgang des [GetDomainSettings-Vorgangs (SOAP)](getdomainsettings-operation-soap.md) oder in den Domänen, die die Organisation in einem [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md) **GetFederationInformation** -Vorgang Verbund hat, zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e68ad-122">Represents the domains the configurations for which are returned in a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) **GetDomainSettings** operation or the domains the organization has federated in a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) **GetFederationInformation** operation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e68ad-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e68ad-123">Parent elements</span></span>

<span data-ttu-id="e68ad-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="e68ad-124">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="e68ad-125">Textwert</span><span class="sxs-lookup"><span data-stu-id="e68ad-125">Text value</span></span>

<span data-ttu-id="e68ad-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="e68ad-126">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e68ad-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e68ad-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e68ad-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="e68ad-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="e68ad-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e68ad-129">Schema Name</span></span>  <br/> |<span data-ttu-id="e68ad-130">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="e68ad-130">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="e68ad-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e68ad-131">Validation File</span></span>  <br/> |<span data-ttu-id="e68ad-132">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="e68ad-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e68ad-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e68ad-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="e68ad-134">True</span><span class="sxs-lookup"><span data-stu-id="e68ad-134">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e68ad-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e68ad-135">See also</span></span>



[<span data-ttu-id="e68ad-136">GetFederationInformation-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e68ad-136">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

