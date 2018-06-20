---
title: SetOofStatus-Vorgang (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetOofStatus
api_type:
- schema
ms.assetid: 97c271e9-506e-43eb-89cd-46803fc47ee5
description: Der Vorgang SetOofStatus Festlegen eines Werts, das angibt, ob die Ansage Out of Office (OOF) für den Benutzer wiedergegeben werden sollte, der die Anforderung stellt.
ms.openlocfilehash: 2bb1deeec8ddb5be56979bfb2fae3396672298a3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831445"
---
# <a name="setoofstatus-operation-um-web-service"></a><span data-ttu-id="d9cbd-103">SetOofStatus-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="d9cbd-103">SetOofStatus operation (UM web service)</span></span>

<span data-ttu-id="d9cbd-104">Der Vorgang SetOofStatus Festlegen eines Werts, das angibt, ob die Ansage Out of Office (OOF) für den Benutzer wiedergegeben werden sollte, der die Anforderung stellt.</span><span class="sxs-lookup"><span data-stu-id="d9cbd-104">The SetOofStatus operation sets a value that indicates whether the Out of Office (OOF) greeting should be played for the user who makes the request.</span></span>
  
## <a name="setoofstatus-request-example"></a><span data-ttu-id="d9cbd-105">Anforderungsbeispiel SetOofStatus</span><span class="sxs-lookup"><span data-stu-id="d9cbd-105">SetOofStatus request example</span></span>

### <a name="description"></a><span data-ttu-id="d9cbd-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9cbd-106">Description</span></span>

<span data-ttu-id="d9cbd-107">Im folgenden Beispiel wird eine Anforderung SetOofStatus veranschaulicht das Formular einer Anforderung an den abwesenheitsansage für ein Postfach zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d9cbd-107">The following example of a SetOofStatus request shows how to form a request to enable the Out of Office greeting for a mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="d9cbd-108">Code</span><span class="sxs-lookup"><span data-stu-id="d9cbd-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetOofStatus xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
        <status>true</status>
    </SetOofStatus>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setoofstatus-response-example"></a><span data-ttu-id="d9cbd-109">Erfolgreiche SetOofStatus antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="d9cbd-109">Successful SetOofStatus response example</span></span>

### <a name="description"></a><span data-ttu-id="d9cbd-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9cbd-110">Description</span></span>

<span data-ttu-id="d9cbd-111">Das folgende Beispiel einer Antwort SetOofStatus zeigt eine Antwort auf die Anforderung SetOofStatus.</span><span class="sxs-lookup"><span data-stu-id="d9cbd-111">The following example of a SetOofStatus response shows a response to the SetOofStatus request.</span></span>
  
### <a name="code"></a><span data-ttu-id="d9cbd-112">Code</span><span class="sxs-lookup"><span data-stu-id="d9cbd-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetOofStatusResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="d9cbd-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9cbd-113">See also</span></span>



[<span data-ttu-id="d9cbd-114">SetOofStatus (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="d9cbd-114">SetOofStatus (UM web service)</span></span>](setoofstatus-um-web-service.md)
  
[<span data-ttu-id="d9cbd-115">SetOofStatusResponse (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="d9cbd-115">SetOofStatusResponse (UM web service)</span></span>](setoofstatusresponse-um-web-service.md)
  
[<span data-ttu-id="d9cbd-116">Status (UM-Webdienst - SetOofStatus)</span><span class="sxs-lookup"><span data-stu-id="d9cbd-116">Status (UM web service - SetOofStatus)</span></span>](status-um-web-servicesetoofstatus.md)

