---
title: GetPhoneCallInformation-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetPhoneCallInformation
api_type:
- schema
ms.assetid: 418bd6ca-39d9-49a9-841e-7a71ede1fa51
description: Der Vorgang GetPhoneCallInformation zurückgegeben Informationen zu den angegebenen Telefonanruf.
ms.openlocfilehash: 8f98ca5dd304eadffc307fa47620b7db6401c782
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758778"
---
# <a name="getphonecallinformation-operation"></a><span data-ttu-id="086db-103">GetPhoneCallInformation-Vorgang</span><span class="sxs-lookup"><span data-stu-id="086db-103">GetPhoneCallInformation operation</span></span>

<span data-ttu-id="086db-104">Der Vorgang **GetPhoneCallInformation** zurückgegeben Informationen zu den angegebenen Telefonanruf.</span><span class="sxs-lookup"><span data-stu-id="086db-104">The **GetPhoneCallInformation** operation returns information about the specified telephone call.</span></span> 
  
## <a name="getphonecallinformation-request-example"></a><span data-ttu-id="086db-105">Anforderungsbeispiel GetPhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="086db-105">GetPhoneCallInformation request example</span></span>

### <a name="description"></a><span data-ttu-id="086db-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="086db-106">Description</span></span>

<span data-ttu-id="086db-107">Im folgenden Beispiel wird eine Anforderung **GetPhoneCallInformation** veranschaulicht eine Anforderung zum Abrufen von Informationen zu einem bestimmten Anruf bilden.</span><span class="sxs-lookup"><span data-stu-id="086db-107">The following example of a **GetPhoneCallInformation** request shows how to form a request to get information about a specific telephone call.</span></span> 
  
### <a name="code"></a><span data-ttu-id="086db-108">Code</span><span class="sxs-lookup"><span data-stu-id="086db-108">Code</span></span>

```xml
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
    <m:GetPhoneCallInformation>
      <m:PhoneCallId Id="NDDY5uY29y9t"/>
    </m:GetPhoneCallInformation>
  </soap:Body>
</soap:Envelope>
```

## <a name="getphonecallinformation-response-example"></a><span data-ttu-id="086db-109">GetPhoneCallInformation antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="086db-109">GetPhoneCallInformation response example</span></span>

### <a name="description"></a><span data-ttu-id="086db-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="086db-110">Description</span></span>

<span data-ttu-id="086db-111">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung **GetPhoneCallInformation** .</span><span class="sxs-lookup"><span data-stu-id="086db-111">The following example shows a successful response to the **GetPhoneCallInformation** request.</span></span> <span data-ttu-id="086db-112">Die Antwort stellt einen Telefonanruf, der aktuell verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="086db-112">The response represents a telephone call that is currently connected.</span></span> 
  
### <a name="code"></a><span data-ttu-id="086db-113">Code</span><span class="sxs-lookup"><span data-stu-id="086db-113">Code</span></span>

```xml
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
    <GetPhoneCallInformationResponse ResponseClass="Success" 
                                     xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <m:PhoneCallInformation xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
        <t:PhoneCallState xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">Connected</t:PhoneCallState>
        <t:ConnectionFailureCause xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">None</t:ConnectionFailureCause>
      </m:PhoneCallInformation>
    </GetPhoneCallInformationResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="086db-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="086db-114">See also</span></span>

- [<span data-ttu-id="086db-115">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="086db-115">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
- [<span data-ttu-id="086db-116">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="086db-116">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

