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
description: Das GetFederationInformationResponse-Element enthält die Antwort des GetFederationInformation-Vorgang (SOAP).
ms.openlocfilehash: 28b002b45968278ad4c7160b4eed29721422646d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758672"
---
# <a name="getfederationinformationresponse-soap"></a><span data-ttu-id="bdc37-103">GetFederationInformationResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bdc37-103">GetFederationInformationResponse (SOAP)</span></span>

<span data-ttu-id="bdc37-104">Das **GetFederationInformationResponse** -Element enthält die Antwort [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="bdc37-104">The **GetFederationInformationResponse** element contains the [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) response.</span></span> 
  
```XML
<GetFederationInformationResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <TokenIssuers/>
   <ApplicationUri/>
   <Domains/>
</GetFederationInformationResponse>
```

 <span data-ttu-id="bdc37-105">**GetFederationInformationResponse**</span><span class="sxs-lookup"><span data-stu-id="bdc37-105">**GetFederationInformationResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bdc37-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bdc37-106">Attributes and elements</span></span>

<span data-ttu-id="bdc37-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bdc37-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bdc37-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="bdc37-108">Attributes</span></span>

<span data-ttu-id="bdc37-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="bdc37-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bdc37-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bdc37-110">Child elements</span></span>

|<span data-ttu-id="bdc37-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="bdc37-111">**Element**</span></span>|<span data-ttu-id="bdc37-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bdc37-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bdc37-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bdc37-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="bdc37-114">Stellt einen Fehlercode, der von den AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bdc37-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="bdc37-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bdc37-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="bdc37-116">Stellt eine Nachricht, die ein Fehlercode zugeordnet ist, die von den AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bdc37-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="bdc37-117">ApplicationUri (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bdc37-117">ApplicationUri (SOAP)</span></span>](applicationuri-soap.md) <br/> |<span data-ttu-id="bdc37-118">Definiert den Ort einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="bdc37-118">Defines the location of an application.</span></span>  <br/> |
|[<span data-ttu-id="bdc37-119">TokenIssuers (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bdc37-119">TokenIssuers (SOAP)</span></span>](tokenissuers-soap.md) <br/> |<span data-ttu-id="bdc37-120">Stellt eine Auflistung von Sicherheitstoken, die Sicherheits-Tokens-Dienst-IDs und Endpunkte enthalten.</span><span class="sxs-lookup"><span data-stu-id="bdc37-120">Represents a collection of security tokens, which contain security token service identifiers and endpoints.</span></span>  <br/> |
|[<span data-ttu-id="bdc37-121">Domänen (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bdc37-121">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="bdc37-122">Stellt die Domänen, die die Konfigurationen für die in einem Vorgang [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md) **GetDomainSettings** zurückgegeben werden oder die Domänen, die die Organisation in einem [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md) federated hat **GetFederationInformation** Vorgang.</span><span class="sxs-lookup"><span data-stu-id="bdc37-122">Represents the domains the configurations for which are returned in a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) **GetDomainSettings** operation or the domains the organization has federated in a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) **GetFederationInformation** operation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bdc37-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bdc37-123">Parent elements</span></span>

<span data-ttu-id="bdc37-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="bdc37-124">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="bdc37-125">Textwert</span><span class="sxs-lookup"><span data-stu-id="bdc37-125">Text value</span></span>

<span data-ttu-id="bdc37-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="bdc37-126">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bdc37-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="bdc37-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bdc37-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="bdc37-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="bdc37-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bdc37-129">Schema Name</span></span>  <br/> |<span data-ttu-id="bdc37-130">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="bdc37-130">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="bdc37-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bdc37-131">Validation File</span></span>  <br/> |<span data-ttu-id="bdc37-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="bdc37-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bdc37-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="bdc37-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="bdc37-134">True</span><span class="sxs-lookup"><span data-stu-id="bdc37-134">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bdc37-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdc37-135">See also</span></span>



[<span data-ttu-id="bdc37-136">GetFederationInformation-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bdc37-136">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

