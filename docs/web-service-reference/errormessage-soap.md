---
title: ErrorMessage (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: b84dd664-4c49-42c9-a49f-2ec4a9f7588b
description: ErrorMessage-Element stellt eine Nachricht, die ein Fehlercode zugeordnet ist, die von den AutoErmittlungsdienst zurückgegeben wird.
ms.openlocfilehash: 888eedc9c7cbbd1aad5cba21e76d999699c7ed02
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758272"
---
# <a name="errormessage-soap"></a><span data-ttu-id="10e60-103">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="10e60-103">ErrorMessage (SOAP)</span></span>

<span data-ttu-id="10e60-104">**ErrorMessage** -Element stellt eine Nachricht, die ein Fehlercode zugeordnet ist, die von den AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="10e60-104">The **ErrorMessage** element represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span> 
  
```XML
<ErrorMessage/>
```

 <span data-ttu-id="10e60-105">**string**</span><span class="sxs-lookup"><span data-stu-id="10e60-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="10e60-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="10e60-106">Attributes and elements</span></span>

<span data-ttu-id="10e60-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="10e60-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="10e60-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="10e60-108">Attributes</span></span>

<span data-ttu-id="10e60-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="10e60-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="10e60-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="10e60-110">Child elements</span></span>

<span data-ttu-id="10e60-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="10e60-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="10e60-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="10e60-112">Parent elements</span></span>

|<span data-ttu-id="10e60-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="10e60-113">**Element**</span></span>|<span data-ttu-id="10e60-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="10e60-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="10e60-115">AutodiscoverResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="10e60-115">AutodiscoverResponse (SOAP)</span></span>](autodiscoverresponse-soap.md) <br/> |<span data-ttu-id="10e60-116">Stellt den Basistyp für alle Antworten, die von den AutoErmittlungsdienst zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="10e60-116">Represents the base type for all responses that are returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="10e60-117">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="10e60-117">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="10e60-118">Enthält die angeforderten Einstellungen für die angegebene Domäne.</span><span class="sxs-lookup"><span data-stu-id="10e60-118">Contains the requested settings for the specified domain.</span></span>  <br/> |
|[<span data-ttu-id="10e60-119">GetDomainSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="10e60-119">GetDomainSettingsResponse (SOAP)</span></span>](getdomainsettingsresponse-soap.md) <br/> |<span data-ttu-id="10e60-120">Enthält die Antwort zu einem Anruf [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md) für eine einzelne Domäne.</span><span class="sxs-lookup"><span data-stu-id="10e60-120">Contains the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) call for an individual domain.</span></span>  <br/> |
|[<span data-ttu-id="10e60-121">GetFederationInformationResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="10e60-121">GetFederationInformationResponse (SOAP)</span></span>](getfederationinformationresponse-soap.md) <br/> |<span data-ttu-id="10e60-122">Enthält die Antwort auf eine Anforderung [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="10e60-122">Contains the response to a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) request.</span></span>  <br/> |
|[<span data-ttu-id="10e60-123">Antwort (SOAP)</span><span class="sxs-lookup"><span data-stu-id="10e60-123">Response (SOAP)</span></span>](response-soap.md) <br/> |<span data-ttu-id="10e60-124">Enthält die Antwort auf eine Anforderung [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="10e60-124">Contains the response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request.</span></span>  <br/> |
|[<span data-ttu-id="10e60-125">UserSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="10e60-125">UserSettingError (SOAP)</span></span>](usersettingerror-soap.md) <br/> |<span data-ttu-id="10e60-126">Stellt einen Fehler, der beim Abrufen einer benutzereinstellung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="10e60-126">Represents an error that is returned while retrieving a user setting.</span></span>  <br/> |
|[<span data-ttu-id="10e60-127">UserResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="10e60-127">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="10e60-128">Stellt eine Antwort auf eine Anforderung [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md) für einen einzelnen Benutzer dar.</span><span class="sxs-lookup"><span data-stu-id="10e60-128">Represents a response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request for an individual user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="10e60-129">Textwert</span><span class="sxs-lookup"><span data-stu-id="10e60-129">Text value</span></span>

<span data-ttu-id="10e60-130">Der Textwert stellt die Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="10e60-130">The text value represents the error message.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="10e60-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="10e60-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="10e60-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="10e60-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="10e60-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="10e60-133">Schema Name</span></span>  <br/> |<span data-ttu-id="10e60-134">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="10e60-134">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="10e60-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="10e60-135">Validation File</span></span>  <br/> |<span data-ttu-id="10e60-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="10e60-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="10e60-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="10e60-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="10e60-138">True</span><span class="sxs-lookup"><span data-stu-id="10e60-138">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="10e60-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10e60-139">See also</span></span>



[<span data-ttu-id="10e60-140">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="10e60-140">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="10e60-141">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="10e60-141">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
  
[<span data-ttu-id="10e60-142">GetFederationInformation-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="10e60-142">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

