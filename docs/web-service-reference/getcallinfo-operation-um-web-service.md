---
title: GetCallInfo-Vorgang (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- GetCallInfo
api_type:
- schema
ms.assetid: 6bccd418-caf7-4eb9-8a6f-410e56a635c3
description: Der Vorgang GetCallInfo wird der Status über den ausgehenden Anruf, der vom CallId (UM-Webdienst) angegeben wird zurückgegeben.
ms.openlocfilehash: 36f9cba3690520ebb457a4cb2bfbcde3fea4b8dc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758591"
---
# <a name="getcallinfo-operation-um-web-service"></a><span data-ttu-id="2acfa-103">GetCallInfo-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="2acfa-103">GetCallInfo operation (UM web service)</span></span>

<span data-ttu-id="2acfa-104">Der Vorgang GetCallInfo wird der Status über den ausgehenden Anruf, der vom [CallId (UM-Webdienst)](callid-um-web-service.md)angegeben wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2acfa-104">The GetCallInfo operation returns the status of the outbound call that is specified by [CallId (UM web service)](callid-um-web-service.md).</span></span>
  
## <a name="getcallinfo-request-example"></a><span data-ttu-id="2acfa-105">Anforderungsbeispiel GetCallInfo</span><span class="sxs-lookup"><span data-stu-id="2acfa-105">GetCallInfo request example</span></span>

### <a name="description"></a><span data-ttu-id="2acfa-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2acfa-106">Description</span></span>

<span data-ttu-id="2acfa-107">Im folgenden Beispiel wird eine Anforderung GetCallInfo veranschaulicht eine Anforderung zum Abrufen von Informationen zu einem angegebenen ausgehender Anrufe bilden.</span><span class="sxs-lookup"><span data-stu-id="2acfa-107">The following example of a GetCallInfo request shows how to form a request to get information about a specified outbound call.</span></span>
  
### <a name="code"></a><span data-ttu-id="2acfa-108">Code</span><span class="sxs-lookup"><span data-stu-id="2acfa-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetCallInfo xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <CallId>MDlkZjllZGMtNGUyMy00NzA5LWJkYWYtN2JlMjBjYjBhZTU2QGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</CallId>
    </GetCallInfo>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-getcallinfo-response-example"></a><span data-ttu-id="2acfa-109">Erfolgreiche GetCallInfo antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="2acfa-109">Successful GetCallInfo response example</span></span>

### <a name="description"></a><span data-ttu-id="2acfa-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2acfa-110">Description</span></span>

<span data-ttu-id="2acfa-111">Das folgende Beispiel einer Antwort GetCallInfo zeigt eine Antwort auf eine GetCallInfo an.</span><span class="sxs-lookup"><span data-stu-id="2acfa-111">The following example of a GetCallInfo response shows a response to a GetCallInfo request.</span></span>
  
### <a name="code"></a><span data-ttu-id="2acfa-112">Code</span><span class="sxs-lookup"><span data-stu-id="2acfa-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <GetCallInfoResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <GetCallInfoResponse>
        <CallState>Connected</CallState> 
        <EventCause>None</EventCause> 
      </GetCallInfoResponse>
    </GetCallInfoResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="2acfa-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2acfa-113">See also</span></span>



[<span data-ttu-id="2acfa-114">GetCallInfo (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="2acfa-114">GetCallInfo (UM web service)</span></span>](getcallinfo-um-web-service.md)
  
[<span data-ttu-id="2acfa-115">GetCallInfoResponse (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="2acfa-115">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)
  
[<span data-ttu-id="2acfa-116">CallId (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="2acfa-116">CallId (UM web service)</span></span>](callid-um-web-service.md)
  
[<span data-ttu-id="2acfa-117">CallState (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="2acfa-117">CallState (UM web service)</span></span>](callstate-um-web-service.md)
  
[<span data-ttu-id="2acfa-118">EventCause (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="2acfa-118">EventCause (UM web service)</span></span>](eventcause-um-web-service.md)

