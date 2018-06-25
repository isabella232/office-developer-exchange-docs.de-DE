---
title: GetFederationInformation-Vorgang (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: c6666a42-a18f-4e4b-beb6-b25ff62cfcc5
description: Der Vorgang GetFederationInformation enthält Informationen zu den Verbund Status von der Organisation, beispielsweise die Ziel-URI verwendet werden, wenn Token an, die in der Übergangsphase sind diese Organisation und den anderen Domänen, die auch die Organisation hat Verbund.
ms.openlocfilehash: bf38b2f2b3db3e38b9b0157d1677efe4fc274e1b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758676"
---
# <a name="getfederationinformation-operation-soap"></a><span data-ttu-id="4421b-103">GetFederationInformation-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4421b-103">GetFederationInformation operation (SOAP)</span></span>

<span data-ttu-id="4421b-104">Der Vorgang **GetFederationInformation** enthält Informationen zu den Verbund Status der Organisation, beispielsweise das Ziel URI beim Anfordern Token zu verwendende sind in der Übergangsphase diese Organisation und die anderen Domänen, die der Organisation auch federated hat.</span><span class="sxs-lookup"><span data-stu-id="4421b-104">The **GetFederationInformation** operation provides information about the federation status of the organization, such as the target URI to be used when requesting tokens that are targeted at this organization, and the other domains that the organization has also federated.</span></span> 
  
<span data-ttu-id="4421b-105">Nur verbundorganisationen können freigeben, Kalender, Kontakte und Nachrichten an externe Benutzer.</span><span class="sxs-lookup"><span data-stu-id="4421b-105">Only federated organizations can share calendar, contacts, and messages to external users.</span></span>
  
## <a name="getfederationinformation-request-example"></a><span data-ttu-id="4421b-106">Anforderungsbeispiel GetFederationInformation</span><span class="sxs-lookup"><span data-stu-id="4421b-106">GetFederationInformation request example</span></span>

### <a name="description"></a><span data-ttu-id="4421b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4421b-107">Description</span></span>

<span data-ttu-id="4421b-108">Im folgenden Beispiel wird eine Anforderung **GetFederationInformation** zeigt eine Anforderung für den Verbund-Informationen eines Benutzers.</span><span class="sxs-lookup"><span data-stu-id="4421b-108">The following example of a **GetFederationInformation** request shows a request for a user's federation information.</span></span> <span data-ttu-id="4421b-109">Der Client sendet diese Anforderung an den Server.</span><span class="sxs-lookup"><span data-stu-id="4421b-109">The client sends this request to the server.</span></span> 
  
### <a name="code"></a><span data-ttu-id="4421b-110">Code</span><span class="sxs-lookup"><span data-stu-id="4421b-110">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?> 
<soap:Envelope xmlns:exm="http://schemas.microsoft.com/exchange/services/2006/messages"
           xmlns:ext="http://schemas.microsoft.com/exchange/services/2006/types"
           xmlns:a="http://www.w3.org/2005/08/addressing"
           xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema"> 
    <soap:Header> 
        <a:MessageID>urn:uuid:6389558d-9e05-465e-ade9-aae14c4bcd10</a:MessageID> 
        <a:Action soap:mustUnderstand="1">http://schemas.microsoft.com/
            exchange/2010/Autodiscover/Autodiscover/GetFederationInformation
        </a:Action> 
        <a:To soap:mustUnderstand="1">https://autodiscover.byfcxu-
            dom.extest.microsoft.com/autodiscover/autodiscover.svc</a:To> 
        <a:ReplyTo>
            <a:Address>http://www.w3.org/2005/08/addressing/anonymous</a:Address> 
        </a:ReplyTo> 
    </soap:Header> 
    <soap:Body> 
        <GetFederationInformationRequestMessage 
            xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover"> 
            <Request> 
                <Domain>contoso.com</Domain> 
            </Request> 
        </GetFederationInformationRequestMessage>
    </soap:Body> 
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="4421b-111">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="4421b-111">Request elements</span></span>

<span data-ttu-id="4421b-112">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="4421b-112">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="4421b-113">GetFederationInformationRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4421b-113">GetFederationInformationRequestMessage (SOAP)</span></span>](getfederationinformationrequestmessage-soap.md)
    
- [<span data-ttu-id="4421b-114">Anforderung (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4421b-114">Request (SOAP)</span></span>](request-soap.md)
    
- [<span data-ttu-id="4421b-115">Domäne (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4421b-115">Domain (SOAP)</span></span>](domain-soap.md)
    
## <a name="getfederationinformation-response-example"></a><span data-ttu-id="4421b-116">GetFederationInformation antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="4421b-116">GetFederationInformation response example</span></span>

### <a name="description"></a><span data-ttu-id="4421b-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4421b-117">Description</span></span>

<span data-ttu-id="4421b-118">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die **GetFederationInformation** -Anforderung, die der Server an den Client sendet.</span><span class="sxs-lookup"><span data-stu-id="4421b-118">The following example shows a successful response to the **GetFederationInformation** request that the server sends to the client.</span></span> 
  
### <a name="code"></a><span data-ttu-id="4421b-119">Code</span><span class="sxs-lookup"><span data-stu-id="4421b-119">Code</span></span>

```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" 
xmlns:a="http://www.w3.org/2005/08/addressing"> 
    <s:Header> 
        <a:Action s:mustUnderstand="1">
            http://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetFederationInformationResponse
        </a:Action> 
        <a:RelatesTo>urn:uuid:6389558d-9e05-465e-ade9-aae14c4bcd10</a:RelatesTo> 
    </s:Header> 
    <s:Body> 
        <GetFederationInformationResponseMessage xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover"> 
            <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance"> 
                <ErrorCode>NoError</ErrorCode> 
                <ErrorMessage/> 
                <ApplicationUri>BYFCXU-DOM.EXTEST.MICROSOFT.COM</ApplicationUri> 
                <Domains> 
                    <Domain>contoso.com</Domain> 
                    <Domain>europe.contoso.com</Domain> 
                    <Domain>americas.contoso.com</Domain> 
                    <Domain>contosolive.com</Domain> 
                </Domains> 
            </Response> 
        </GetFederationInformationResponseMessage> 
    </s:Body> 
</s:Envelope>
```

### <a name="response-elements"></a><span data-ttu-id="4421b-120">Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="4421b-120">Response elements</span></span>

<span data-ttu-id="4421b-121">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="4421b-121">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="4421b-122">GetFederationInformationResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4421b-122">GetFederationInformationResponseMessage (SOAP)</span></span>](getfederationinformationresponsemessage-soap.md)
    
- [<span data-ttu-id="4421b-123">Antwort (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4421b-123">Response (SOAP)</span></span>](response-soap.md)
    
- [<span data-ttu-id="4421b-124">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4421b-124">ErrorCode (SOAP)</span></span>](errorcode-soap.md)
    
- [<span data-ttu-id="4421b-125">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4421b-125">ErrorMessage (SOAP)</span></span>](errormessage-soap.md)
    
- [<span data-ttu-id="4421b-126">ApplicationUri (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4421b-126">ApplicationUri (SOAP)</span></span>](applicationuri-soap.md)
    
- [<span data-ttu-id="4421b-127">Domänen (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4421b-127">Domains (SOAP)</span></span>](domains-soap.md)
    
- [<span data-ttu-id="4421b-128">Domäne (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4421b-128">Domain (SOAP)</span></span>](domain-soap.md)
    
## <a name="see-also"></a><span data-ttu-id="4421b-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4421b-129">See also</span></span>

- [<span data-ttu-id="4421b-130">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4421b-130">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
- [<span data-ttu-id="4421b-131">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4421b-131">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

