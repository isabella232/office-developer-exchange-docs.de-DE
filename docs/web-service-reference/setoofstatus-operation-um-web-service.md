---
title: SetOofStatus-Vorgang (um-Webdienst)
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
description: Der SetOofStatus-Vorgang legt einen Wert fest, der angibt, ob die Abwesenheit (Out of Office, OOF) Begrüßung für den Benutzer wiedergegeben werden soll, der die Anforderung stellt.
ms.openlocfilehash: 2311b6137ac25d15ad3d06668450c1d0f7ec1fad
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467354"
---
# <a name="setoofstatus-operation-um-web-service"></a><span data-ttu-id="d94f8-103">SetOofStatus-Vorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="d94f8-103">SetOofStatus operation (UM web service)</span></span>

<span data-ttu-id="d94f8-104">Der SetOofStatus-Vorgang legt einen Wert fest, der angibt, ob die Abwesenheit (Out of Office, OOF) Begrüßung für den Benutzer wiedergegeben werden soll, der die Anforderung stellt.</span><span class="sxs-lookup"><span data-stu-id="d94f8-104">The SetOofStatus operation sets a value that indicates whether the Out of Office (OOF) greeting should be played for the user who makes the request.</span></span>
  
## <a name="setoofstatus-request-example"></a><span data-ttu-id="d94f8-105">SetOofStatus-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="d94f8-105">SetOofStatus request example</span></span>

### <a name="description"></a><span data-ttu-id="d94f8-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d94f8-106">Description</span></span>

<span data-ttu-id="d94f8-107">Im folgenden Beispiel einer SetOofStatus-Anforderung wird gezeigt, wie Sie eine Anforderung zum Aktivieren der Abwesenheits Begrüßung für ein Postfach bilden.</span><span class="sxs-lookup"><span data-stu-id="d94f8-107">The following example of a SetOofStatus request shows how to form a request to enable the Out of Office greeting for a mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="d94f8-108">Code</span><span class="sxs-lookup"><span data-stu-id="d94f8-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetOofStatus xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
        <status>true</status>
    </SetOofStatus>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setoofstatus-response-example"></a><span data-ttu-id="d94f8-109">Erfolgreiches SetOofStatus-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="d94f8-109">Successful SetOofStatus response example</span></span>

### <a name="description"></a><span data-ttu-id="d94f8-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d94f8-110">Description</span></span>

<span data-ttu-id="d94f8-111">Im folgenden Beispiel einer SetOofStatus-Antwort wird eine Antwort auf die SetOofStatus-Anforderung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d94f8-111">The following example of a SetOofStatus response shows a response to the SetOofStatus request.</span></span>
  
### <a name="code"></a><span data-ttu-id="d94f8-112">Code</span><span class="sxs-lookup"><span data-stu-id="d94f8-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetOofStatusResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="d94f8-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d94f8-113">See also</span></span>



[<span data-ttu-id="d94f8-114">SetOofStatus (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="d94f8-114">SetOofStatus (UM web service)</span></span>](setoofstatus-um-web-service.md)
  
[<span data-ttu-id="d94f8-115">SetOofStatusResponse (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="d94f8-115">SetOofStatusResponse (UM web service)</span></span>](setoofstatusresponse-um-web-service.md)
  
[<span data-ttu-id="d94f8-116">Status (um-Webdienst – SetOofStatus)</span><span class="sxs-lookup"><span data-stu-id="d94f8-116">Status (UM web service - SetOofStatus)</span></span>](status-um-web-servicesetoofstatus.md)

