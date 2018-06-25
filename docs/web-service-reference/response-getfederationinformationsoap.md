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
description: Das Antwort-Element enthält die GetFederationInformation-Vorgang (SOAP) Antwortinformationen.
ms.openlocfilehash: 946cba56d7503a0e20ec59640f4f1258c00a844e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831171"
---
# <a name="response-getfederationinformation-soap"></a><span data-ttu-id="5341a-103">Antwort (GetFederationInformation) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5341a-103">Response (GetFederationInformation) (SOAP)</span></span>

<span data-ttu-id="5341a-104">Das **Antwort** -Element enthält die [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md) Antwort-Informationen.</span><span class="sxs-lookup"><span data-stu-id="5341a-104">The **Response** element contains the [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) response information.</span></span> 
  
```XML
<Response>
   <ErrorCode/>
   <ErrorMessage/>
   <ApplicationUri/>
   <Domains/>
</Response>
```

 <span data-ttu-id="5341a-105">**GetFederationInformationResponse**</span><span class="sxs-lookup"><span data-stu-id="5341a-105">**GetFederationInformationResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5341a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5341a-106">Attributes and elements</span></span>

<span data-ttu-id="5341a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5341a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5341a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5341a-108">Attributes</span></span>

<span data-ttu-id="5341a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5341a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5341a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5341a-110">Child elements</span></span>

|<span data-ttu-id="5341a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="5341a-111">**Element**</span></span>|<span data-ttu-id="5341a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5341a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5341a-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5341a-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="5341a-114">Stellt einen Fehlercode, der von den AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5341a-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="5341a-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5341a-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="5341a-116">Stellt eine Nachricht, die ein Fehlercode zugeordnet ist, die von den AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5341a-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="5341a-117">ApplicationUri (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5341a-117">ApplicationUri (SOAP)</span></span>](applicationuri-soap.md) <br/> |<span data-ttu-id="5341a-118">Definiert den Ort einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="5341a-118">Defines the location of an application.</span></span>  <br/> |
|[<span data-ttu-id="5341a-119">Domänen (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5341a-119">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="5341a-120">Stellt die Domäne-Auflistung in einer [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)oder die Domänen an, denen die Organisation in einem [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)im Verbund wurde die Konfigurationen für die zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5341a-120">Represents the domain collection the configurations for which are returned in a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), or the domains that the organization has federated in a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5341a-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5341a-121">Parent elements</span></span>

|<span data-ttu-id="5341a-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="5341a-122">**Element**</span></span>|<span data-ttu-id="5341a-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5341a-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5341a-124">GetFederationInformationResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5341a-124">GetFederationInformationResponseMessage (SOAP)</span></span>](getfederationinformationresponsemessage-soap.md) <br/> |<span data-ttu-id="5341a-125">Definiert eine Antwort auf eine [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md) an.</span><span class="sxs-lookup"><span data-stu-id="5341a-125">Defines a response to a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5341a-126">Textwert</span><span class="sxs-lookup"><span data-stu-id="5341a-126">Text value</span></span>

<span data-ttu-id="5341a-127">Keine.</span><span class="sxs-lookup"><span data-stu-id="5341a-127">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5341a-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5341a-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5341a-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="5341a-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="5341a-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5341a-130">Schema Name</span></span>  <br/> |<span data-ttu-id="5341a-131">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="5341a-131">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="5341a-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5341a-132">Validation File</span></span>  <br/> |<span data-ttu-id="5341a-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5341a-133">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5341a-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5341a-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="5341a-135">True</span><span class="sxs-lookup"><span data-stu-id="5341a-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5341a-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5341a-136">See also</span></span>



[<span data-ttu-id="5341a-137">GetFederationInformation-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5341a-137">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

