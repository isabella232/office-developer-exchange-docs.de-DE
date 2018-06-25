---
title: PlayOnPhoneGreeting-Vorgang (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- PlayOnPhoneGreeting
api_type:
- schema
ms.assetid: 6deafc40-290b-4bce-9914-b6bcc529f38a
description: Der Vorgang PlayOnPhoneGreeting macht einen ausgehenden Anruf und eine der zwei Begrüßung angezeigt am Telefon abgespielt.
ms.openlocfilehash: 85ba76c7638911678c1ef1aef88f47fdab2c6a4e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830828"
---
# <a name="playonphonegreeting-operation-um-web-service"></a><span data-ttu-id="095bd-103">PlayOnPhoneGreeting-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="095bd-103">PlayOnPhoneGreeting operation (UM web service)</span></span>

<span data-ttu-id="095bd-104">Der Vorgang PlayOnPhoneGreeting macht einen ausgehenden Anruf und eine der zwei Begrüßung angezeigt am Telefon abgespielt.</span><span class="sxs-lookup"><span data-stu-id="095bd-104">The PlayOnPhoneGreeting operation makes an outbound call and plays one of the two greeting messages on the telephone.</span></span>
  
## <a name="playonphonegreeting-request-example"></a><span data-ttu-id="095bd-105">Anforderungsbeispiel PlayOnPhoneGreeting</span><span class="sxs-lookup"><span data-stu-id="095bd-105">PlayOnPhoneGreeting request example</span></span>

### <a name="description"></a><span data-ttu-id="095bd-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="095bd-106">Description</span></span>

<span data-ttu-id="095bd-107">Im folgenden Beispiel wird eine Anforderung PlayOnPhoneGreeting bilden eine Anforderung zum Tätigen eines ausgehenden Anrufs und Wiedergabe der Nachricht normal Ansage über ein Telefon veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="095bd-107">The following example of a PlayOnPhoneGreeting request shows how to form a request to make an outbound call and play the normal greeting message on a telephone.</span></span>
  
### <a name="code"></a><span data-ttu-id="095bd-108">Code</span><span class="sxs-lookup"><span data-stu-id="095bd-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <PlayOnPhoneGreeting xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <GreetingType>NormalCustom</GreetingType>
      <DialString>12345</DialString>
    </PlayOnPhoneGreeting>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-playonphonegreeting-response-example"></a><span data-ttu-id="095bd-109">Erfolgreiche PlayOnPhoneGreeting antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="095bd-109">Successful PlayOnPhoneGreeting response example</span></span>

### <a name="description"></a><span data-ttu-id="095bd-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="095bd-110">Description</span></span>

<span data-ttu-id="095bd-111">Das folgende Beispiel einer Antwort PlayOnPhoneGreeting zeigt eine Antwort auf die Anforderung PlayOnPhoneGreeting.</span><span class="sxs-lookup"><span data-stu-id="095bd-111">The following example of a PlayOnPhoneGreeting response shows a response to the PlayOnPhoneGreeting request.</span></span>
  
### <a name="code"></a><span data-ttu-id="095bd-112">Code</span><span class="sxs-lookup"><span data-stu-id="095bd-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <PlayOnPhoneGreetingResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
    <PlayOnPhoneGreetingResponse>MjA4MTQ5MmItMTBmZC00ZGFmLThiMzEtNDllNDJjM2Y3MjIxQGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</PlayOnPhoneGreetingResponse> 
    </PlayOnPhoneGreetingResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="095bd-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="095bd-113">See also</span></span>



[<span data-ttu-id="095bd-114">PlayOnPhoneGreeting (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="095bd-114">PlayOnPhoneGreeting (UM web service)</span></span>](playonphonegreeting-um-web-service.md)
  
[<span data-ttu-id="095bd-115">PlayOnPhoneGreetingResponse (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="095bd-115">PlayOnPhoneGreetingResponse (UM web service)</span></span>](playonphonegreetingresponse-um-web-service.md)
  
[<span data-ttu-id="095bd-116">GreetingType (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="095bd-116">GreetingType (UM web service)</span></span>](greetingtype-um-web-service.md)
  
[<span data-ttu-id="095bd-117">DialString (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="095bd-117">dialString (UM web service)</span></span>](dialstring-um-web-service.md)

