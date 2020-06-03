---
title: Antwort (GetFederationInformation) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: ca48a4b3-5006-4bb7-973e-d9137ce67e16
description: Das Response-Element enthält die GetFederationInformation-Vorgangs (SOAP)-Antwortinformationen.
ms.openlocfilehash: 0b9a2c518b968faa6ef86b7c1f544eac40f8e5c8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530586"
---
# <a name="response-getfederationinformation-soap"></a><span data-ttu-id="b373b-103">Antwort (GetFederationInformation) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b373b-103">Response (GetFederationInformation) (SOAP)</span></span>

<span data-ttu-id="b373b-104">Das **Response** -Element enthält die [GetFederationInformation-Vorgangs (SOAP)-](getfederationinformation-operation-soap.md) Antwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="b373b-104">The **Response** element contains the [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) response information.</span></span> 
  
```XML
<Response>
   <ErrorCode/>
   <ErrorMessage/>
   <ApplicationUri/>
   <Domains/>
</Response>
```

 <span data-ttu-id="b373b-105">**GetFederationInformationResponse**</span><span class="sxs-lookup"><span data-stu-id="b373b-105">**GetFederationInformationResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b373b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b373b-106">Attributes and elements</span></span>

<span data-ttu-id="b373b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b373b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b373b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b373b-108">Attributes</span></span>

<span data-ttu-id="b373b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b373b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b373b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b373b-110">Child elements</span></span>

|<span data-ttu-id="b373b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b373b-111">**Element**</span></span>|<span data-ttu-id="b373b-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b373b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b373b-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b373b-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="b373b-114">Stellt einen Fehlercode dar, der vom AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b373b-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="b373b-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b373b-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="b373b-116">Stellt eine Meldung dar, die einem Fehlercode zugeordnet ist, der vom AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b373b-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="b373b-117">ApplicationUri (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b373b-117">ApplicationUri (SOAP)</span></span>](applicationuri-soap.md) <br/> |<span data-ttu-id="b373b-118">Definiert den Speicherort einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b373b-118">Defines the location of an application.</span></span>  <br/> |
|[<span data-ttu-id="b373b-119">Domänen (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b373b-119">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="b373b-120">Stellt die Domänen Sammlung dar, für die Konfigurationen in einem [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)oder die Domänen, die die Organisation in einem [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)Verbund hat, zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b373b-120">Represents the domain collection the configurations for which are returned in a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), or the domains that the organization has federated in a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b373b-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b373b-121">Parent elements</span></span>

|<span data-ttu-id="b373b-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="b373b-122">**Element**</span></span>|<span data-ttu-id="b373b-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b373b-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b373b-124">GetFederationInformationResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b373b-124">GetFederationInformationResponseMessage (SOAP)</span></span>](getfederationinformationresponsemessage-soap.md) <br/> |<span data-ttu-id="b373b-125">Definiert eine Antwort auf eine [GetFederationInformation-Operation (SOAP)-](getfederationinformation-operation-soap.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b373b-125">Defines a response to a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b373b-126">Textwert</span><span class="sxs-lookup"><span data-stu-id="b373b-126">Text value</span></span>

<span data-ttu-id="b373b-127">Keine.</span><span class="sxs-lookup"><span data-stu-id="b373b-127">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b373b-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b373b-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b373b-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="b373b-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="b373b-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b373b-130">Schema Name</span></span>  <br/> |<span data-ttu-id="b373b-131">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="b373b-131">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="b373b-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b373b-132">Validation File</span></span>  <br/> |<span data-ttu-id="b373b-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b373b-133">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b373b-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b373b-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="b373b-135">True</span><span class="sxs-lookup"><span data-stu-id="b373b-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b373b-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b373b-136">See also</span></span>



[<span data-ttu-id="b373b-137">GetFederationInformation-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b373b-137">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

