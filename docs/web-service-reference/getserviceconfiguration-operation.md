---
title: GetServiceConfiguration-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetServiceConfiguration
api_type:
- schema
ms.assetid: 070cbfe5-325a-4955-8e4a-8230ea0459a7
description: Der Vorgang GetServiceConfiguration Konfigurationsinformationen für den angegebenen Typ des Diensts abgerufen. Dieser Vorgang kann die Konfigurationseinstellungen für die Unified Messaging, die Regeln für den Schutz und die E-Mail-Infos Dienste zurückgeben.
ms.openlocfilehash: 7fdc4d8defac3d6d352c121483bf8a4c735d9629
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829667"
---
# <a name="getserviceconfiguration-operation"></a><span data-ttu-id="cbc06-104">GetServiceConfiguration-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cbc06-104">GetServiceConfiguration operation</span></span>

<span data-ttu-id="cbc06-105">Der Vorgang **GetServiceConfiguration** Konfigurationsinformationen für den angegebenen Typ des Diensts abgerufen.</span><span class="sxs-lookup"><span data-stu-id="cbc06-105">The **GetServiceConfiguration** operation gets configuration information for the specified type of service.</span></span> <span data-ttu-id="cbc06-106">Dieser Vorgang kann die Konfigurationseinstellungen für die Unified Messaging, die Regeln für den Schutz und die E-Mail-Infos Dienste zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="cbc06-106">This operation can return configuration settings for the Unified Messaging, Protection Rules, and Mail Tips services.</span></span> 
  
## <a name="getserviceconfiguration-request-example"></a><span data-ttu-id="cbc06-107">Anforderungsbeispiel GetServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="cbc06-107">GetServiceConfiguration request example</span></span>

### <a name="description"></a><span data-ttu-id="cbc06-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cbc06-108">Description</span></span>

<span data-ttu-id="cbc06-109">Im folgenden Beispiel wird eine Anforderung **GetServiceConfiguration** veranschaulicht eine Anforderung zum Abrufen von Konfigurationsinformationen für die Unified Messaging-Dienst zu bilden.</span><span class="sxs-lookup"><span data-stu-id="cbc06-109">The following example of a **GetServiceConfiguration** request shows how to form a request to get configuration information for the Unified Messaging service.</span></span> 
  
### <a name="code"></a><span data-ttu-id="cbc06-110">Code</span><span class="sxs-lookup"><span data-stu-id="cbc06-110">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:GetServiceConfiguration>
      <m:RequestedConfiguration>
        <m:ConfigurationName>UnifiedMessagingConfiguration</m:ConfigurationName>
      </m:RequestedConfiguration>
    </m:GetServiceConfiguration>
  </soap:Body>
</soap:Envelope>
```

## <a name="getserviceconfiguration-response-example"></a><span data-ttu-id="cbc06-111">GetServiceConfiguration antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="cbc06-111">GetServiceConfiguration response example</span></span>

### <a name="description"></a><span data-ttu-id="cbc06-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cbc06-112">Description</span></span>

<span data-ttu-id="cbc06-113">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung **GetServiceConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="cbc06-113">The following example shows a successful response to the **GetServiceConfiguration** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="cbc06-114">Code</span><span class="sxs-lookup"><span data-stu-id="cbc06-114">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="20" 
                         Version="Exchange2010" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetServiceConfigurationResponse ResponseClass="Success" 
                                     xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <ResponseMessages>
        <ServiceConfigurationResponseMessageType ResponseClass="Success">
          <ResponseCode>NoError</ResponseCode>
          <m:UnifiedMessagingConfiguration xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
            <t:UmEnabled xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">true</t:UmEnabled>
            <t:PlayOnPhoneDialString xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">user@contoso.com</t:PlayOnPhoneDialString>
            <t:PlayOnPhoneEnabled xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">true</t:PlayOnPhoneEnabled>
          </m:UnifiedMessagingConfiguration>
        </ServiceConfigurationResponseMessageType>
      </ResponseMessages>
    </GetServiceConfigurationResponse>
  </s:Body>
</s:Envelope>
```

## <a name="getserviceconfiguration-error-response-example"></a><span data-ttu-id="cbc06-115">Antwortbeispiel GetServiceConfiguration-Fehler</span><span class="sxs-lookup"><span data-stu-id="cbc06-115">GetServiceConfiguration Error response example</span></span>

### <a name="description"></a><span data-ttu-id="cbc06-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cbc06-116">Description</span></span>

<span data-ttu-id="cbc06-117">Das folgende Beispiel zeigt eine Fehlerantwort an die **GetServiceConfiguration** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="cbc06-117">The following example shows an error response to the **GetServiceConfiguration** request.</span></span> <span data-ttu-id="cbc06-118">Dieser Fehler wurde durch eine fehlerhafte Konfigurationsnamen verursacht.</span><span class="sxs-lookup"><span data-stu-id="cbc06-118">This error was caused by an incorrect configuration name.</span></span> 
  
### <a name="code"></a><span data-ttu-id="cbc06-119">Code</span><span class="sxs-lookup"><span data-stu-id="cbc06-119">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Body>
    <s:Fault>
      <faultcode xmlns:a="http://schemas.microsoft.com/exchange/services/2006/types">a:ErrorSchemaValidation</faultcode>
      <faultstring xml:lang="en-US">The request failed schema validation: 
      The 'http://schemas.microsoft.com/exchange/services/2006/messages:ConfigurationName' element 
      is invalid - The value 'UUnifiedMessagingConfiguration' is invalid according to its 
      datatype 'http://schemas.microsoft.com/exchange/services/2006/types:ServiceConfigurationType' 
      - The Enumeration constraint failed.</faultstring>
      <detail>
        <e:ResponseCode xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">ErrorSchemaValidation</e:ResponseCode>
        <e:Message xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">The request failed schema validation.</e:Message>
        <t:MessageXml xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
          <t:LineNumber>13</t:LineNumber>
          <t:LinePosition>62</t:LinePosition>
          <t:Violation>The 'http://schemas.microsoft.com/exchange/services/2006/messages:ConfigurationName' element 
          is invalid - The value 'UUnifiedMessagingConfiguration' is invalid according to its 
          datatype 'http://schemas.microsoft.com/exchange/services/2006/types:ServiceConfigurationType'
          - The Enumeration constraint failed.</t:Violation>
        </t:MessageXml>
      </detail>
    </s:Fault>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="cbc06-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cbc06-120">See also</span></span>



[<span data-ttu-id="cbc06-121">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="cbc06-121">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="cbc06-122">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="cbc06-122">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

