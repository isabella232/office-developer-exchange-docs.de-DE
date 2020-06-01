---
title: GetCallInfo-Vorgang (um-Webdienst)
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
description: Der GetCallInfo-Vorgang gibt den Status des ausgehenden Anrufs zurück, der von der "Calling"-Dienst (um-Webdienst) angegeben wird.
ms.openlocfilehash: 6b5664dfe16f9c74cc7175098145141b815a6355
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461240"
---
# <a name="getcallinfo-operation-um-web-service"></a><span data-ttu-id="75199-103">GetCallInfo-Vorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="75199-103">GetCallInfo operation (UM web service)</span></span>

<span data-ttu-id="75199-104">Der GetCallInfo-Vorgang gibt den Status des ausgehenden Anrufs zurück, der von der ["Calling"-Dienst (um-Webdienst)](callid-um-web-service.md)angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="75199-104">The GetCallInfo operation returns the status of the outbound call that is specified by [CallId (UM web service)](callid-um-web-service.md).</span></span>
  
## <a name="getcallinfo-request-example"></a><span data-ttu-id="75199-105">GetCallInfo-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="75199-105">GetCallInfo request example</span></span>

### <a name="description"></a><span data-ttu-id="75199-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75199-106">Description</span></span>

<span data-ttu-id="75199-107">Im folgenden Beispiel einer GetCallInfo-Anforderung wird gezeigt, wie eine Anforderung zum Abrufen von Informationen zu einem angegebenen ausgehenden Aufruf bildet.</span><span class="sxs-lookup"><span data-stu-id="75199-107">The following example of a GetCallInfo request shows how to form a request to get information about a specified outbound call.</span></span>
  
### <a name="code"></a><span data-ttu-id="75199-108">Code</span><span class="sxs-lookup"><span data-stu-id="75199-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetCallInfo xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <CallId>MDlkZjllZGMtNGUyMy00NzA5LWJkYWYtN2JlMjBjYjBhZTU2QGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</CallId>
    </GetCallInfo>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-getcallinfo-response-example"></a><span data-ttu-id="75199-109">Erfolgreiches GetCallInfo-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="75199-109">Successful GetCallInfo response example</span></span>

### <a name="description"></a><span data-ttu-id="75199-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75199-110">Description</span></span>

<span data-ttu-id="75199-111">Im folgenden Beispiel einer GetCallInfo-Antwort wird eine Antwort auf eine GetCallInfo-Anforderung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="75199-111">The following example of a GetCallInfo response shows a response to a GetCallInfo request.</span></span>
  
### <a name="code"></a><span data-ttu-id="75199-112">Code</span><span class="sxs-lookup"><span data-stu-id="75199-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <GetCallInfoResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <GetCallInfoResponse>
        <CallState>Connected</CallState> 
        <EventCause>None</EventCause> 
      </GetCallInfoResponse>
    </GetCallInfoResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="75199-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75199-113">See also</span></span>



[<span data-ttu-id="75199-114">GetCallInfo (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="75199-114">GetCallInfo (UM web service)</span></span>](getcallinfo-um-web-service.md)
  
[<span data-ttu-id="75199-115">GetCallInfoResponse (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="75199-115">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)
  
[<span data-ttu-id="75199-116">Anrufdienst (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="75199-116">CallId (UM web service)</span></span>](callid-um-web-service.md)
  
[<span data-ttu-id="75199-117">CallState (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="75199-117">CallState (UM web service)</span></span>](callstate-um-web-service.md)
  
[<span data-ttu-id="75199-118">EventCause (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="75199-118">EventCause (UM web service)</span></span>](eventcause-um-web-service.md)

