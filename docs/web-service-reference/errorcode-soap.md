---
title: ErrorCode (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 5e5ec861-0191-4ecb-a906-47ce8ed96381
description: ErrorCode-Element stellt einen Fehlercode, der von den AutoErmittlungsdienst zurückgegeben wird.
ms.openlocfilehash: 2dd91cec4645325c02bc8588af0ee0547909b945
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758262"
---
# <a name="errorcode-soap"></a><span data-ttu-id="5c073-103">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5c073-103">ErrorCode (SOAP)</span></span>

<span data-ttu-id="5c073-104">**ErrorCode** -Element stellt einen Fehlercode, der von den AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5c073-104">The **ErrorCode** element represents an error code that is returned by the Autodiscover service.</span></span> 
  
```XML
<ErrorCode/>
```

 <span data-ttu-id="5c073-105">**string**</span><span class="sxs-lookup"><span data-stu-id="5c073-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5c073-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5c073-106">Attributes and elements</span></span>

<span data-ttu-id="5c073-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5c073-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5c073-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5c073-108">Attributes</span></span>

<span data-ttu-id="5c073-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5c073-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5c073-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5c073-110">Child elements</span></span>

<span data-ttu-id="5c073-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="5c073-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5c073-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5c073-112">Parent elements</span></span>

|<span data-ttu-id="5c073-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5c073-113">**Element**</span></span>|<span data-ttu-id="5c073-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5c073-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5c073-115">AutodiscoverResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5c073-115">AutodiscoverResponse (SOAP)</span></span>](autodiscoverresponse-soap.md) <br/> |<span data-ttu-id="5c073-116">Stellt den Basistyp für alle Antworten, die von den AutoErmittlungsdienst zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5c073-116">Represents the base type for all responses that are returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="5c073-117">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5c073-117">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="5c073-118">Enthält die angeforderten Einstellungen für die angegebene Domäne.</span><span class="sxs-lookup"><span data-stu-id="5c073-118">Contains the requested settings for the specified domain.</span></span>  <br/> |
|[<span data-ttu-id="5c073-119">GetDomainSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5c073-119">GetDomainSettingsResponse (SOAP)</span></span>](getdomainsettingsresponse-soap.md) <br/> |<span data-ttu-id="5c073-120">Enthält die Antwort zu einem Anruf [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md) für eine einzelne Domäne.</span><span class="sxs-lookup"><span data-stu-id="5c073-120">Contains the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) call for an individual domain.</span></span>  <br/> |
|[<span data-ttu-id="5c073-121">GetFederationInformationResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5c073-121">GetFederationInformationResponse (SOAP)</span></span>](getfederationinformationresponse-soap.md) <br/> |<span data-ttu-id="5c073-122">Enthält die Antwort auf eine Anforderung [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="5c073-122">Contains the response to a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) request.</span></span>  <br/> |
|[<span data-ttu-id="5c073-123">Antwort (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5c073-123">Response (SOAP)</span></span>](response-soap.md) <br/> |<span data-ttu-id="5c073-124">Enthält die Antwort auf eine Anforderung [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md).</span><span class="sxs-lookup"><span data-stu-id="5c073-124">Contains the response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)request.</span></span>  <br/> |
|[<span data-ttu-id="5c073-125">UserSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5c073-125">UserSettingError (SOAP)</span></span>](usersettingerror-soap.md) <br/> |<span data-ttu-id="5c073-126">Stellt einen Fehler, der beim Abrufen einer benutzereinstellung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5c073-126">Represents an error that is returned while retrieving a user setting.</span></span>  <br/> |
|[<span data-ttu-id="5c073-127">UserResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5c073-127">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="5c073-128">Stellt eine Antwort auf eine Anforderung [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md) für einen einzelnen Benutzer dar.</span><span class="sxs-lookup"><span data-stu-id="5c073-128">Represents a response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request for an individual user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5c073-129">Textwert</span><span class="sxs-lookup"><span data-stu-id="5c073-129">Text value</span></span>

<span data-ttu-id="5c073-130">Der Textwert stellt den Fehlercode für eine Fehlerantwort AutoErmittlung.</span><span class="sxs-lookup"><span data-stu-id="5c073-130">The text value represents the error code for an Autodiscover error response.</span></span> <span data-ttu-id="5c073-131">Die folgende Tabelle enthält die möglichen Textwerte für die **ErrorCode** -Element.</span><span class="sxs-lookup"><span data-stu-id="5c073-131">The following table lists the possible text values for the **ErrorCode** element.</span></span> 
  
|<span data-ttu-id="5c073-132">**Fehlercodewert text**</span><span class="sxs-lookup"><span data-stu-id="5c073-132">**Error code text value**</span></span>|<span data-ttu-id="5c073-133">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5c073-133">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5c073-134">NoError</span><span class="sxs-lookup"><span data-stu-id="5c073-134">NoError</span></span>  <br/> |<span data-ttu-id="5c073-135">Kein Fehler.</span><span class="sxs-lookup"><span data-stu-id="5c073-135">There was no error.</span></span>  <br/> |
|<span data-ttu-id="5c073-136">RedirectAddress</span><span class="sxs-lookup"><span data-stu-id="5c073-136">RedirectAddress</span></span>  <br/> |<span data-ttu-id="5c073-137">Der Aufrufer muss die e-Mail-Adressumleitung folgen, die von der AutoErmittlung zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="5c073-137">The caller must follow the e-mail address redirection that was returned by Autodiscover.</span></span>  <br/> |
|<span data-ttu-id="5c073-138">RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="5c073-138">RedirectUrl</span></span>  <br/> |<span data-ttu-id="5c073-139">Der Aufrufer muss die URL-Umleitung folgen, die von der AutoErmittlung zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="5c073-139">The caller must follow the URL redirection that was returned by Autodiscover.</span></span>  <br/> |
|<span data-ttu-id="5c073-140">InvalidUser</span><span class="sxs-lookup"><span data-stu-id="5c073-140">InvalidUser</span></span>  <br/> |<span data-ttu-id="5c073-141">Der Benutzer, der in der Anforderung übergeben wurde, ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="5c073-141">The user that was passed in the request is invalid.</span></span>  <br/> |
|<span data-ttu-id="5c073-142">InvalidRequest</span><span class="sxs-lookup"><span data-stu-id="5c073-142">InvalidRequest</span></span>  <br/> |<span data-ttu-id="5c073-143">Die Anforderung ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="5c073-143">The request is invalid.</span></span>  <br/> |
|<span data-ttu-id="5c073-144">InvalidSetting</span><span class="sxs-lookup"><span data-stu-id="5c073-144">InvalidSetting</span></span>  <br/> |<span data-ttu-id="5c073-145">Eine festgelegte Einstellung ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="5c073-145">A specified setting is invalid.</span></span>  <br/> |
|<span data-ttu-id="5c073-146">SettingIsNotAvailable</span><span class="sxs-lookup"><span data-stu-id="5c073-146">SettingIsNotAvailable</span></span>  <br/> |<span data-ttu-id="5c073-147">Eine festgelegte Einstellung ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5c073-147">A specified setting is not available.</span></span>  <br/> |
|<span data-ttu-id="5c073-148">ServerBusy</span><span class="sxs-lookup"><span data-stu-id="5c073-148">ServerBusy</span></span>  <br/> |<span data-ttu-id="5c073-149">Der Server ist ausgelastet und die Anforderung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="5c073-149">The server is too busy to process the request.</span></span>  <br/> |
|<span data-ttu-id="5c073-150">InvalidDomain</span><span class="sxs-lookup"><span data-stu-id="5c073-150">InvalidDomain</span></span>  <br/> |<span data-ttu-id="5c073-151">Die angeforderte Domäne ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="5c073-151">The requested domain is not valid.</span></span>  <br/> |
|<span data-ttu-id="5c073-152">NotFederated</span><span class="sxs-lookup"><span data-stu-id="5c073-152">NotFederated</span></span>  <br/> |<span data-ttu-id="5c073-153">Die Organisation nicht im Verbund arbeitet.</span><span class="sxs-lookup"><span data-stu-id="5c073-153">The organization is not federated.</span></span>  <br/> |
|<span data-ttu-id="5c073-154">InternalServerError</span><span class="sxs-lookup"><span data-stu-id="5c073-154">InternalServerError</span></span>  <br/> |<span data-ttu-id="5c073-155">Es ist ein interner Serverfehler.</span><span class="sxs-lookup"><span data-stu-id="5c073-155">There is an internal server error.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="5c073-156">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5c073-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5c073-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="5c073-157">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="5c073-158">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5c073-158">Schema Name</span></span>  <br/> |<span data-ttu-id="5c073-159">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="5c073-159">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="5c073-160">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5c073-160">Validation File</span></span>  <br/> |<span data-ttu-id="5c073-161">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5c073-161">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5c073-162">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5c073-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="5c073-163">True</span><span class="sxs-lookup"><span data-stu-id="5c073-163">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5c073-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c073-164">See also</span></span>



[<span data-ttu-id="5c073-165">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5c073-165">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="5c073-166">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5c073-166">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
  
[<span data-ttu-id="5c073-167">GetFederationInformation-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5c073-167">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

