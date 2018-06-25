---
title: Antwort (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 4c2bcdeb-95ce-4ffa-bd83-118af53b534f
description: Das Antwort-Element enthält die Antwort auf einen GetUserSettings-Vorgang (SOAP), GetDomainSettings-Vorgang (SOAP) oder eine GetFederationInformation-Anforderung (SOAP)-Vorgang.
ms.openlocfilehash: 240c8e1f904ad685b51c1f657b2bc18e14fd985e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831179"
---
# <a name="response-soap"></a><span data-ttu-id="82e9d-103">Antwort (SOAP)</span><span class="sxs-lookup"><span data-stu-id="82e9d-103">Response (SOAP)</span></span>

<span data-ttu-id="82e9d-104">Das **Antwort** -Element enthält die Antwort auf eine [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md), [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)oder eine Anforderung [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="82e9d-104">The **Response** element contains the response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md), [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), or a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) request.</span></span> 
  
```XML
<Response>
   <ErrorCode/>
   <ErrorMessage/>
   <UserResponses/>
</Response>
```

 <span data-ttu-id="82e9d-105">**GetUserSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="82e9d-105">**GetUserSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="82e9d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="82e9d-106">Attributes and elements</span></span>

<span data-ttu-id="82e9d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="82e9d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="82e9d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="82e9d-108">Attributes</span></span>

<span data-ttu-id="82e9d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="82e9d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="82e9d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="82e9d-110">Child elements</span></span>

|<span data-ttu-id="82e9d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="82e9d-111">**Element**</span></span>|<span data-ttu-id="82e9d-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="82e9d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="82e9d-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="82e9d-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="82e9d-114">Stellt einen Fehlercode, der von den AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="82e9d-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="82e9d-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="82e9d-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="82e9d-116">Stellt eine Nachricht, die ein Fehlercode zugeordnet ist, die von den AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="82e9d-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="82e9d-117">UserResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="82e9d-117">UserResponses (SOAP)</span></span>](userresponses-soap.md) <br/> |<span data-ttu-id="82e9d-118">Enthält die Konfigurationseinstellungen für jeden angeforderten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="82e9d-118">Contains the configuration settings for each requested user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="82e9d-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="82e9d-119">Parent elements</span></span>

|<span data-ttu-id="82e9d-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="82e9d-120">**Element**</span></span>|<span data-ttu-id="82e9d-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="82e9d-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="82e9d-122">GetUserSettingsResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="82e9d-122">GetUserSettingsResponseMessage (SOAP)</span></span>](getusersettingsresponsemessage-soap.md) <br/> |<span data-ttu-id="82e9d-123">Definiert eine Antwort auf eine [GetUserSettingsRequest (SOAP)](getusersettingsrequest-soap.md)</span><span class="sxs-lookup"><span data-stu-id="82e9d-123">Defines a response to a [GetUserSettingsRequest (SOAP)](getusersettingsrequest-soap.md)</span></span> <br/> |
|[<span data-ttu-id="82e9d-124">GetDomainSettingsResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="82e9d-124">GetDomainSettingsResponseMessage (SOAP)</span></span>](getdomainsettingsresponsemessage-soap.md) <br/> |<span data-ttu-id="82e9d-125">Definiert eine Antwort auf eine [GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md).</span><span class="sxs-lookup"><span data-stu-id="82e9d-125">Defines a response to a [GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md).</span></span>  <br/> |
|[<span data-ttu-id="82e9d-126">GetFederationInformationResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="82e9d-126">GetFederationInformationResponseMessage (SOAP)</span></span>](getfederationinformationresponsemessage-soap.md) <br/> |<span data-ttu-id="82e9d-127">Definiert eine Antwort auf eine [GetFederationInformationRequest (SOAP)](getfederationinformationrequest-soap.md).</span><span class="sxs-lookup"><span data-stu-id="82e9d-127">Defines a response to a [GetFederationInformationRequest (SOAP)](getfederationinformationrequest-soap.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="82e9d-128">Textwert</span><span class="sxs-lookup"><span data-stu-id="82e9d-128">Text value</span></span>

<span data-ttu-id="82e9d-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="82e9d-129">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="82e9d-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="82e9d-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="82e9d-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="82e9d-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="82e9d-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="82e9d-132">Schema Name</span></span>  <br/> |<span data-ttu-id="82e9d-133">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="82e9d-133">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="82e9d-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="82e9d-134">Validation File</span></span>  <br/> |<span data-ttu-id="82e9d-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="82e9d-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="82e9d-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="82e9d-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="82e9d-137">True</span><span class="sxs-lookup"><span data-stu-id="82e9d-137">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="82e9d-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82e9d-138">See also</span></span>



[<span data-ttu-id="82e9d-139">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="82e9d-139">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)


[<span data-ttu-id="82e9d-140">AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="82e9d-140">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="82e9d-141">SOAP-Autodiscover XML-Elemente für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="82e9d-141">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

