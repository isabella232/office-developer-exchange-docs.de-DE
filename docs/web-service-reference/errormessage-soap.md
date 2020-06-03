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
description: Das ErrorMessage-Element stellt eine Meldung dar, die einem Fehlercode zugeordnet ist, der vom AutoErmittlungsdienst zurückgegeben wird.
ms.openlocfilehash: 4ebaf91fe26083cf241826e1fc16ac184fddf57c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530642"
---
# <a name="errormessage-soap"></a><span data-ttu-id="3e1ee-103">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3e1ee-103">ErrorMessage (SOAP)</span></span>

<span data-ttu-id="3e1ee-104">Das **ErrorMessage** -Element stellt eine Meldung dar, die einem Fehlercode zugeordnet ist, der vom AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3e1ee-104">The **ErrorMessage** element represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span> 
  
```XML
<ErrorMessage/>
```

 <span data-ttu-id="3e1ee-105">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3e1ee-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3e1ee-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3e1ee-106">Attributes and elements</span></span>

<span data-ttu-id="3e1ee-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3e1ee-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3e1ee-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3e1ee-108">Attributes</span></span>

<span data-ttu-id="3e1ee-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3e1ee-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3e1ee-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3e1ee-110">Child elements</span></span>

<span data-ttu-id="3e1ee-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="3e1ee-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3e1ee-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3e1ee-112">Parent elements</span></span>

|<span data-ttu-id="3e1ee-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3e1ee-113">**Element**</span></span>|<span data-ttu-id="3e1ee-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3e1ee-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3e1ee-115">AutodiscoverResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3e1ee-115">AutodiscoverResponse (SOAP)</span></span>](autodiscoverresponse-soap.md) <br/> |<span data-ttu-id="3e1ee-116">Stellt den Basistyp für alle Antworten dar, die vom AutoErmittlungsdienst zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3e1ee-116">Represents the base type for all responses that are returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="3e1ee-117">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3e1ee-117">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="3e1ee-118">Enthält die angeforderten Einstellungen für die angegebene Domäne.</span><span class="sxs-lookup"><span data-stu-id="3e1ee-118">Contains the requested settings for the specified domain.</span></span>  <br/> |
|[<span data-ttu-id="3e1ee-119">GetDomainSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3e1ee-119">GetDomainSettingsResponse (SOAP)</span></span>](getdomainsettingsresponse-soap.md) <br/> |<span data-ttu-id="3e1ee-120">Enthält die Antwort auf einen [GetDomainSettings-Vorgang (SOAP)-](getdomainsettings-operation-soap.md) Aufruf für eine einzelne Domäne.</span><span class="sxs-lookup"><span data-stu-id="3e1ee-120">Contains the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) call for an individual domain.</span></span>  <br/> |
|[<span data-ttu-id="3e1ee-121">GetFederationInformationResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3e1ee-121">GetFederationInformationResponse (SOAP)</span></span>](getfederationinformationresponse-soap.md) <br/> |<span data-ttu-id="3e1ee-122">Enthält die Antwort auf eine [GetFederationInformation-Vorgang (SOAP)-](getfederationinformation-operation-soap.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="3e1ee-122">Contains the response to a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) request.</span></span>  <br/> |
|[<span data-ttu-id="3e1ee-123">Antwort (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3e1ee-123">Response (SOAP)</span></span>](response-soap.md) <br/> |<span data-ttu-id="3e1ee-124">Enthält die Antwort auf eine [GetUserSettings-Vorgang (SOAP)-](getusersettings-operation-soap.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="3e1ee-124">Contains the response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request.</span></span>  <br/> |
|[<span data-ttu-id="3e1ee-125">UserSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3e1ee-125">UserSettingError (SOAP)</span></span>](usersettingerror-soap.md) <br/> |<span data-ttu-id="3e1ee-126">Stellt einen Fehler dar, der beim Abrufen einer Benutzereinstellung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3e1ee-126">Represents an error that is returned while retrieving a user setting.</span></span>  <br/> |
|[<span data-ttu-id="3e1ee-127">User Response (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3e1ee-127">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="3e1ee-128">Stellt eine Antwort auf eine [GetUserSettings-Vorgang (SOAP)-](getusersettings-operation-soap.md) Anforderung für einen einzelnen Benutzer dar.</span><span class="sxs-lookup"><span data-stu-id="3e1ee-128">Represents a response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request for an individual user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3e1ee-129">Textwert</span><span class="sxs-lookup"><span data-stu-id="3e1ee-129">Text value</span></span>

<span data-ttu-id="3e1ee-130">Der Text-Wert stellt die Fehlermeldung dar.</span><span class="sxs-lookup"><span data-stu-id="3e1ee-130">The text value represents the error message.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3e1ee-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3e1ee-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3e1ee-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e1ee-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="3e1ee-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3e1ee-133">Schema Name</span></span>  <br/> |<span data-ttu-id="3e1ee-134">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="3e1ee-134">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="3e1ee-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3e1ee-135">Validation File</span></span>  <br/> |<span data-ttu-id="3e1ee-136">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="3e1ee-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3e1ee-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3e1ee-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="3e1ee-138">True</span><span class="sxs-lookup"><span data-stu-id="3e1ee-138">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3e1ee-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e1ee-139">See also</span></span>



[<span data-ttu-id="3e1ee-140">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3e1ee-140">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="3e1ee-141">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3e1ee-141">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
  
[<span data-ttu-id="3e1ee-142">GetFederationInformation-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3e1ee-142">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

