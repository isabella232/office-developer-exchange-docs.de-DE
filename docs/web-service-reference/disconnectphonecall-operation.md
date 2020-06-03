---
title: DisconnectPhoneCall-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DisconnectPhoneCall
api_type:
- schema
ms.assetid: b42fb512-2ae4-4072-906a-ccebb85edb84
description: Der DisconnectPhoneCall-Vorgang beendet den Telefonanruf.
ms.openlocfilehash: e337185bc2d5c4d2d4e010605816eacea8dfa0ee
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529063"
---
# <a name="disconnectphonecall-operation"></a><span data-ttu-id="e99b6-103">DisconnectPhoneCall-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e99b6-103">DisconnectPhoneCall operation</span></span>

<span data-ttu-id="e99b6-104">Der **DisconnectPhoneCall** -Vorgang beendet den Telefonanruf.</span><span class="sxs-lookup"><span data-stu-id="e99b6-104">The **DisconnectPhoneCall** operation terminates the telephone call.</span></span> 
  
## <a name="disconnectphonecall-request-example"></a><span data-ttu-id="e99b6-105">DisconnectPhoneCall-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="e99b6-105">DisconnectPhoneCall request example</span></span>

### <a name="description"></a><span data-ttu-id="e99b6-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e99b6-106">Description</span></span>

<span data-ttu-id="e99b6-107">Das folgende Beispiel einer **DisconnectPhoneCall** -Anforderung zeigt, wie Sie eine Anforderung zum Trennen eines Telefonanrufs bilden.</span><span class="sxs-lookup"><span data-stu-id="e99b6-107">The following example of a **DisconnectPhoneCall** request shows how to form a request to disconnect a telephone call.</span></span> 
  
### <a name="code"></a><span data-ttu-id="e99b6-108">Code</span><span class="sxs-lookup"><span data-stu-id="e99b6-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:DisconnectPhoneCall>
      <m:PhoneCallId Id="OWVl4NWb3N29t"/>
    </m:DisconnectPhoneCall>
  </soap:Body>
</soap:Envelope>
```

## <a name="disconnectphonecall-response-example"></a><span data-ttu-id="e99b6-109">DisconnectPhoneCall-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="e99b6-109">DisconnectPhoneCall response example</span></span>

### <a name="description"></a><span data-ttu-id="e99b6-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e99b6-110">Description</span></span>

<span data-ttu-id="e99b6-111">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die **DisconnectPhoneCall** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e99b6-111">The following example shows a successful response to the **DisconnectPhoneCall** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="e99b6-112">Code</span><span class="sxs-lookup"><span data-stu-id="e99b6-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="20" 
                         Version="Exchange2010" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <DisconnectPhoneCallResponse ResponseClass="Success" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
    </DisconnectPhoneCallResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="e99b6-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e99b6-113">See also</span></span>

- [<span data-ttu-id="e99b6-114">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="e99b6-114">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md) 
- [<span data-ttu-id="e99b6-115">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e99b6-115">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

