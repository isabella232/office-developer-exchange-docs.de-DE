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
description: Das ErrorCode-Element stellt einen Fehlercode dar, der vom AutoErmittlungsdienst zurückgegeben wird.
ms.openlocfilehash: d66167e51733ffcaa3d62a985d3e03e2ac80b715
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460092"
---
# <a name="errorcode-soap"></a><span data-ttu-id="e3dff-103">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e3dff-103">ErrorCode (SOAP)</span></span>

<span data-ttu-id="e3dff-104">Das **errorCode** -Element stellt einen Fehlercode dar, der vom AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e3dff-104">The **ErrorCode** element represents an error code that is returned by the Autodiscover service.</span></span> 
  
```XML
<ErrorCode/>
```

 <span data-ttu-id="e3dff-105">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e3dff-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e3dff-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e3dff-106">Attributes and elements</span></span>

<span data-ttu-id="e3dff-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e3dff-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e3dff-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e3dff-108">Attributes</span></span>

<span data-ttu-id="e3dff-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e3dff-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e3dff-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e3dff-110">Child elements</span></span>

<span data-ttu-id="e3dff-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="e3dff-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e3dff-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e3dff-112">Parent elements</span></span>

|<span data-ttu-id="e3dff-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e3dff-113">**Element**</span></span>|<span data-ttu-id="e3dff-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e3dff-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e3dff-115">AutodiscoverResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e3dff-115">AutodiscoverResponse (SOAP)</span></span>](autodiscoverresponse-soap.md) <br/> |<span data-ttu-id="e3dff-116">Stellt den Basistyp für alle Antworten dar, die vom AutoErmittlungsdienst zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e3dff-116">Represents the base type for all responses that are returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="e3dff-117">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e3dff-117">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="e3dff-118">Enthält die angeforderten Einstellungen für die angegebene Domäne.</span><span class="sxs-lookup"><span data-stu-id="e3dff-118">Contains the requested settings for the specified domain.</span></span>  <br/> |
|[<span data-ttu-id="e3dff-119">GetDomainSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e3dff-119">GetDomainSettingsResponse (SOAP)</span></span>](getdomainsettingsresponse-soap.md) <br/> |<span data-ttu-id="e3dff-120">Enthält die Antwort auf einen [GetDomainSettings-Vorgang (SOAP)-](getdomainsettings-operation-soap.md) Aufruf für eine einzelne Domäne.</span><span class="sxs-lookup"><span data-stu-id="e3dff-120">Contains the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) call for an individual domain.</span></span>  <br/> |
|[<span data-ttu-id="e3dff-121">GetFederationInformationResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e3dff-121">GetFederationInformationResponse (SOAP)</span></span>](getfederationinformationresponse-soap.md) <br/> |<span data-ttu-id="e3dff-122">Enthält die Antwort auf eine [GetFederationInformation-Vorgang (SOAP)-](getfederationinformation-operation-soap.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e3dff-122">Contains the response to a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) request.</span></span>  <br/> |
|[<span data-ttu-id="e3dff-123">Antwort (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e3dff-123">Response (SOAP)</span></span>](response-soap.md) <br/> |<span data-ttu-id="e3dff-124">Enthält die Antwort auf eine [GetUserSettings-Vorgang (SOAP)-](getusersettings-operation-soap.md)Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e3dff-124">Contains the response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)request.</span></span>  <br/> |
|[<span data-ttu-id="e3dff-125">UserSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e3dff-125">UserSettingError (SOAP)</span></span>](usersettingerror-soap.md) <br/> |<span data-ttu-id="e3dff-126">Stellt einen Fehler dar, der beim Abrufen einer Benutzereinstellung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e3dff-126">Represents an error that is returned while retrieving a user setting.</span></span>  <br/> |
|[<span data-ttu-id="e3dff-127">User Response (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e3dff-127">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="e3dff-128">Stellt eine Antwort auf eine [GetUserSettings-Vorgang (SOAP)-](getusersettings-operation-soap.md) Anforderung für einen einzelnen Benutzer dar.</span><span class="sxs-lookup"><span data-stu-id="e3dff-128">Represents a response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request for an individual user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e3dff-129">Textwert</span><span class="sxs-lookup"><span data-stu-id="e3dff-129">Text value</span></span>

<span data-ttu-id="e3dff-130">Der Text-Wert stellt den Fehlercode für eine Auto Ermittlungsfehler Antwort dar.</span><span class="sxs-lookup"><span data-stu-id="e3dff-130">The text value represents the error code for an Autodiscover error response.</span></span> <span data-ttu-id="e3dff-131">In der folgenden Tabelle sind die möglichen Text Werte für das **errorCode** -Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e3dff-131">The following table lists the possible text values for the **ErrorCode** element.</span></span> 
  
|<span data-ttu-id="e3dff-132">**Fehlercodetext Wert**</span><span class="sxs-lookup"><span data-stu-id="e3dff-132">**Error code text value**</span></span>|<span data-ttu-id="e3dff-133">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e3dff-133">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e3dff-134">NoError</span><span class="sxs-lookup"><span data-stu-id="e3dff-134">NoError</span></span>  <br/> |<span data-ttu-id="e3dff-135">Es ist kein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="e3dff-135">There was no error.</span></span>  <br/> |
|<span data-ttu-id="e3dff-136">RedirectAddress</span><span class="sxs-lookup"><span data-stu-id="e3dff-136">RedirectAddress</span></span>  <br/> |<span data-ttu-id="e3dff-137">Der Anrufer muss die von der AutoErmittlung zurückgegebene e-Mail-Adress Umleitung befolgten.</span><span class="sxs-lookup"><span data-stu-id="e3dff-137">The caller must follow the e-mail address redirection that was returned by Autodiscover.</span></span>  <br/> |
|<span data-ttu-id="e3dff-138">RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="e3dff-138">RedirectUrl</span></span>  <br/> |<span data-ttu-id="e3dff-139">Der Aufrufer muss die von der AutoErmittlung zurückgegebene URL-Umleitung befolgten.</span><span class="sxs-lookup"><span data-stu-id="e3dff-139">The caller must follow the URL redirection that was returned by Autodiscover.</span></span>  <br/> |
|<span data-ttu-id="e3dff-140">InvalidUser</span><span class="sxs-lookup"><span data-stu-id="e3dff-140">InvalidUser</span></span>  <br/> |<span data-ttu-id="e3dff-141">Der Benutzer, der in der Anforderung übergeben wurde, ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e3dff-141">The user that was passed in the request is invalid.</span></span>  <br/> |
|<span data-ttu-id="e3dff-142">InvalidRequest</span><span class="sxs-lookup"><span data-stu-id="e3dff-142">InvalidRequest</span></span>  <br/> |<span data-ttu-id="e3dff-143">Die Anforderung ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e3dff-143">The request is invalid.</span></span>  <br/> |
|<span data-ttu-id="e3dff-144">InvalidSetting</span><span class="sxs-lookup"><span data-stu-id="e3dff-144">InvalidSetting</span></span>  <br/> |<span data-ttu-id="e3dff-145">Eine angegebene Einstellung ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e3dff-145">A specified setting is invalid.</span></span>  <br/> |
|<span data-ttu-id="e3dff-146">SettingIsNotAvailable</span><span class="sxs-lookup"><span data-stu-id="e3dff-146">SettingIsNotAvailable</span></span>  <br/> |<span data-ttu-id="e3dff-147">Eine angegebene Einstellung ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e3dff-147">A specified setting is not available.</span></span>  <br/> |
|<span data-ttu-id="e3dff-148">ServerBusy</span><span class="sxs-lookup"><span data-stu-id="e3dff-148">ServerBusy</span></span>  <br/> |<span data-ttu-id="e3dff-149">Der Server ist zu beschäftigt, um die Anforderung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="e3dff-149">The server is too busy to process the request.</span></span>  <br/> |
|<span data-ttu-id="e3dff-150">InvalidDomain</span><span class="sxs-lookup"><span data-stu-id="e3dff-150">InvalidDomain</span></span>  <br/> |<span data-ttu-id="e3dff-151">Die angeforderte Domäne ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e3dff-151">The requested domain is not valid.</span></span>  <br/> |
|<span data-ttu-id="e3dff-152">NotFederated</span><span class="sxs-lookup"><span data-stu-id="e3dff-152">NotFederated</span></span>  <br/> |<span data-ttu-id="e3dff-153">Die Organisation ist nicht Verbund.</span><span class="sxs-lookup"><span data-stu-id="e3dff-153">The organization is not federated.</span></span>  <br/> |
|<span data-ttu-id="e3dff-154">InternalServerError</span><span class="sxs-lookup"><span data-stu-id="e3dff-154">InternalServerError</span></span>  <br/> |<span data-ttu-id="e3dff-155">Es ist ein interner Serverfehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="e3dff-155">There is an internal server error.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="e3dff-156">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e3dff-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e3dff-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="e3dff-157">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="e3dff-158">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e3dff-158">Schema Name</span></span>  <br/> |<span data-ttu-id="e3dff-159">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="e3dff-159">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="e3dff-160">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e3dff-160">Validation File</span></span>  <br/> |<span data-ttu-id="e3dff-161">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="e3dff-161">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e3dff-162">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e3dff-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="e3dff-163">True</span><span class="sxs-lookup"><span data-stu-id="e3dff-163">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e3dff-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3dff-164">See also</span></span>



[<span data-ttu-id="e3dff-165">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e3dff-165">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="e3dff-166">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e3dff-166">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
  
[<span data-ttu-id="e3dff-167">GetFederationInformation-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e3dff-167">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

