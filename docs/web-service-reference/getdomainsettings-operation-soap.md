---
title: GetDomainSettings-Vorgang (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a6f4a53d-d7f6-4ad1-8afb-78745c500eaa
description: Der GetDomainSettings-Vorgang ruft die angegebenen Einstellungen der Domäne für den Benutzer ab. Die AutoErmittlung gibt die zu entdeckenden Domänen und die angeforderten Einstellungen dieser Domänen zurück.
ms.openlocfilehash: fd655e088b73372bc1dd68a740ebc2b516d1804a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460967"
---
# <a name="getdomainsettings-operation-soap"></a><span data-ttu-id="ad379-104">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad379-104">GetDomainSettings operation (SOAP)</span></span>

<span data-ttu-id="ad379-105">Der **GetDomainSettings** -Vorgang ruft die angegebenen Einstellungen der Domäne für den Benutzer ab.</span><span class="sxs-lookup"><span data-stu-id="ad379-105">The **GetDomainSettings** operation retrieves the specified settings of the domain for the user.</span></span> <span data-ttu-id="ad379-106">Die AutoErmittlung gibt die zu entdeckenden Domänen und die angeforderten Einstellungen dieser Domänen zurück.</span><span class="sxs-lookup"><span data-stu-id="ad379-106">Autodiscover returns the domains that are to be discovered and the requested settings of those domains.</span></span> 
  
## <a name="getdomainsettings-request-example"></a><span data-ttu-id="ad379-107">GetDomainSettings-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="ad379-107">GetDomainSettings request example</span></span>

### <a name="description"></a><span data-ttu-id="ad379-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad379-108">Description</span></span>

<span data-ttu-id="ad379-109">Im folgenden Beispiel einer **GetDomainSettings** -Anforderung wird eine Anforderung für die **ExternalEWSUrl** -Domäneneinstellungen eines Benutzers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ad379-109">The following example of a **GetDomainSettings** request shows a request for a user's **ExternalEWSUrl** domain settings.</span></span> <span data-ttu-id="ad379-110">Der Client sendet diese Anforderung an den Server.</span><span class="sxs-lookup"><span data-stu-id="ad379-110">The client sends this request to the server.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ad379-111">Code</span><span class="sxs-lookup"><span data-stu-id="ad379-111">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?> 
<soap:Envelope xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover"
               xmlns:wsa="http://www.w3.org/2005/08/addressing"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
    <soap:Header> 
        <a:RequestedServerVersion>Exchange2010</a:RequestedServerVersion>
        <wsa:Action>https://schemas.microsoft.com/exchange/2010/
            Autodiscover/Autodiscover/GetDomainSettings</wsa:Action>
        <wsa:To>
            https://autodiscover.exchange.microsoft.com/autodiscover/autodiscover.svc
        </wsa:To>
    </soap:Header> 
    <soap:Body> 
        <a:GetDomainSettingsRequestMessage xmlns:a="https://schemas.microsoft.com
            /exchange/2010/Autodiscover"> 
            <a:Request> 
                <a:Domains> 
                    <a:Domain>contoso.com<</a:Domain> 
                </a:Domains> 
                <a:RequestedSettings> 
                    <a:Setting>ExternalEwsUrl</a:Setting> 
                </a:RequestedSettings> 
            </a:Request> 
        </a:GetDomainSettingsRequestMessage> 
    </soap:Body> 
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="ad379-112">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="ad379-112">Request elements</span></span>

<span data-ttu-id="ad379-113">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="ad379-113">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="ad379-114">GetDomainSettingsRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad379-114">GetDomainSettingsRequestMessage (SOAP)</span></span>](getdomainsettingsrequestmessage-soap.md)
    
- [<span data-ttu-id="ad379-115">Request (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad379-115">Request (SOAP)</span></span>](request-soap.md)
    
- [<span data-ttu-id="ad379-116">Domänen (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad379-116">Domains (SOAP)</span></span>](domains-soap.md)
    
- [<span data-ttu-id="ad379-117">Domäne (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad379-117">Domain (SOAP)</span></span>](domain-soap.md)
    
- [<span data-ttu-id="ad379-118">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad379-118">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md)
    
- [<span data-ttu-id="ad379-119">Einstellung (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad379-119">Setting (SOAP)</span></span>](setting-soap.md)
    
## <a name="getdomainsettings-response-example"></a><span data-ttu-id="ad379-120">GetDomainSettings-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="ad379-120">GetDomainSettings response example</span></span>

### <a name="description"></a><span data-ttu-id="ad379-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad379-121">Description</span></span>

<span data-ttu-id="ad379-122">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die **GetDomainSettings** -Anforderung, die der Server an den Client sendet.</span><span class="sxs-lookup"><span data-stu-id="ad379-122">The following example shows a successful response to the **GetDomainSettings** request that the server sends to the client.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ad379-123">Code</span><span class="sxs-lookup"><span data-stu-id="ad379-123">Code</span></span>

```XML
//www.w3.org/2005/08/addressing"> 
    <s:Header> 
        <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/ 
            Autodiscover/Autodiscover/GetDomainSettingsResponse
        </a:Action> 
        <h:ServerVersionInfo xmlns:h="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
            xmlns:i="http://www.w3.org/2001/XMLSchema-instance"> 
        <h:MajorVersion>14</h:MajorVersion> 
        <h:MinorVersion>0</h:MinorVersion> 
        <h:MajorBuildNumber>639</h:MajorBuildNumber> 
        <h:MinorBuildNumber>20</h:MinorBuildNumber> 
        <h:Version>Exchange2010</h:Version> 
        </h:ServerVersionInfo>
    </s:Header> 
    <s:Body> 
        <GetDomainSettingsResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover"> 
            <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance"> 
                <ErrorCode>NoError</ErrorCode> 
                <ErrorMessage /> 
                <DomainResponses> 
                    <DomainResponse> 
                        <ErrorCode>NoError</ErrorCode> 
                        <ErrorMessage>No error.</ErrorMessage> 
                        <DomainSettingErrors /> 
                        <DomainSettings> 
                            <DomainSetting i:type="DomainStringSetting"> 
                                <Name>ExternalEwsUrl</Name> 
                                <Value>https://emea.mail.microsoft.com/EWS/Exchange.asmx</Value> 
                            </DomainSetting> 
                        </DomainSettings> 
                        <RedirectTarget i:nil="true" /> 
                    </DomainResponse> 
                </DomainResponses> 
            </Response> 
        </GetDomainSettingsResponseMessage> 
    </s:Body> 
</s:Envelope>
```

### <a name="response-elements"></a><span data-ttu-id="ad379-124">Response-Elemente</span><span class="sxs-lookup"><span data-stu-id="ad379-124">Response elements</span></span>

<span data-ttu-id="ad379-125">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="ad379-125">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="ad379-126">GetDomainSettingsResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad379-126">GetDomainSettingsResponseMessage (SOAP)</span></span>](getdomainsettingsresponsemessage-soap.md)
    
- [<span data-ttu-id="ad379-127">Antwort (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad379-127">Response (SOAP)</span></span>](response-soap.md)
    
- [<span data-ttu-id="ad379-128">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad379-128">ErrorCode (SOAP)</span></span>](errorcode-soap.md)
    
- [<span data-ttu-id="ad379-129">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad379-129">ErrorMessage (SOAP)</span></span>](errormessage-soap.md)
    
- [<span data-ttu-id="ad379-130">DomainResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad379-130">DomainResponses (SOAP)</span></span>](domainresponses-soap.md)
    
- [<span data-ttu-id="ad379-131">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad379-131">DomainResponse (SOAP)</span></span>](domainresponse-soap.md)
    
- [<span data-ttu-id="ad379-132">DomainSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad379-132">DomainSettingErrors (SOAP)</span></span>](domainsettingerrors-soap.md)
    
- [<span data-ttu-id="ad379-133">DomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad379-133">DomainSettings (SOAP)</span></span>](domainsettings-soap.md)
    
- [<span data-ttu-id="ad379-134">DomainSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad379-134">DomainSetting (SOAP)</span></span>](domainsetting-soap.md)
    
- [<span data-ttu-id="ad379-135">Name (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad379-135">Name (SOAP)</span></span>](name-soap.md)
    
- [<span data-ttu-id="ad379-136">Wert (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad379-136">Value (SOAP)</span></span>](value-soap.md)
    
- [<span data-ttu-id="ad379-137">RedirectTarget (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad379-137">RedirectTarget (SOAP)</span></span>](redirecttarget-soap.md)
    
## <a name="see-also"></a><span data-ttu-id="ad379-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad379-138">See also</span></span>



[<span data-ttu-id="ad379-139">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad379-139">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="ad379-140">GetFederationInformation-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad379-140">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

