---
title: Trennungsvorgang (um-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- Disconnect
api_type:
- schema
ms.assetid: a987000b-d6e6-49d7-944c-e9c278d0236f
description: Durch den Vorgang zum Trennen der Verbindung wird der Anruf beendet, der durch den angegebenen Aufrufer (um-Webdienst) identifiziert wird.
ms.openlocfilehash: a1268f9ea3d879f472e019bf1847fc13d65d1819
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529070"
---
# <a name="disconnect-operation-um-web-service"></a><span data-ttu-id="89a28-103">Trennungsvorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="89a28-103">Disconnect operation (UM web service)</span></span>

<span data-ttu-id="89a28-104">Durch den Vorgang zum Trennen der Verbindung wird der Anruf beendet, der durch den angegebenen [Aufrufer (um-Webdienst)](callid-um-web-service.md)identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="89a28-104">The Disconnect operation terminates the call that is identified by the specified [CallId (UM web service)](callid-um-web-service.md).</span></span>
  
## <a name="disconnect-request-example"></a><span data-ttu-id="89a28-105">Trenn Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="89a28-105">Disconnect request example</span></span>

### <a name="description"></a><span data-ttu-id="89a28-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89a28-106">Description</span></span>

<span data-ttu-id="89a28-107">Im folgenden Beispiel einer Anforderung für eine Trennung wird gezeigt, wie eine Anforderung zum Trennen eines Anrufs bildet.</span><span class="sxs-lookup"><span data-stu-id="89a28-107">The following example of a Disconnect request shows how to form a request to disconnect a call.</span></span>
  
### <a name="code"></a><span data-ttu-id="89a28-108">Code</span><span class="sxs-lookup"><span data-stu-id="89a28-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <Disconnect xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <CallId>MDlkZjllZGMtNGUyMy00NzA5LWJkYWYtN2JlMjBjYjBhZTU2QGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</CallId>
    </Disconnect>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-disconnect-response-example"></a><span data-ttu-id="89a28-109">Beispiel für erfolgreiche Trennungs Antwort</span><span class="sxs-lookup"><span data-stu-id="89a28-109">Successful Disconnect response example</span></span>

### <a name="description"></a><span data-ttu-id="89a28-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89a28-110">Description</span></span>

<span data-ttu-id="89a28-111">Das folgende Beispiel einer Disconnect-Antwort zeigt eine Antwort auf die Anforderung zum Trennen der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="89a28-111">The following example of a Disconnect response shows a response to the Disconnect request.</span></span>
  
### <a name="code"></a><span data-ttu-id="89a28-112">Code</span><span class="sxs-lookup"><span data-stu-id="89a28-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <DisconnectResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="89a28-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89a28-113">See also</span></span>

- [<span data-ttu-id="89a28-114">Trennen (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="89a28-114">Disconnect (UM web service)</span></span>](disconnect-um-web-service.md) 
- [<span data-ttu-id="89a28-115">DisconnectResponse (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="89a28-115">DisconnectResponse (UM web service)</span></span>](disconnectresponse-um-web-service.md) 
- [<span data-ttu-id="89a28-116">Anrufdienst (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="89a28-116">CallId (UM web service)</span></span>](callid-um-web-service.md)

