---
title: SetPlayOnPhoneDialString-Vorgang (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetPlayOnPhoneDialString
api_type:
- schema
ms.assetid: a68479f2-d900-4dd8-a5ce-dbea8247e841
description: SetPlayOnPhoneDialString-Vorgang wird die Zugriffsnummer Zeichenfolge, die als Standard für den Vorgang PlayOnPhone (UM-Webdienst) und den PlayOnPhoneGreeting-Vorgang (UM-Webdienst) verwenden.
ms.openlocfilehash: 0d1a879784740777e5eab0cbd5f85e59a6479461
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831446"
---
# <a name="setplayonphonedialstring-operation-um-web-service"></a><span data-ttu-id="3649f-103">SetPlayOnPhoneDialString-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="3649f-103">SetPlayOnPhoneDialString operation (UM web service)</span></span>

<span data-ttu-id="3649f-104">SetPlayOnPhoneDialString-Vorgang wird die Zugriffsnummer Zeichenfolge, die als Standard für den [PlayOnPhone-Vorgang (UM-Webdienst)](playonphone-operation-um-web-service.md) und den [PlayOnPhoneGreeting-Vorgang (UM-Webdienst)](playonphonegreeting-operation-um-web-service.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="3649f-104">The SetPlayOnPhoneDialString operation sets the dial string to use as the default for the [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) and the [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md).</span></span>
  
## <a name="setplayonphonedialstring-request-example"></a><span data-ttu-id="3649f-105">Anforderungsbeispiel SetPlayOnPhoneDialString</span><span class="sxs-lookup"><span data-stu-id="3649f-105">SetPlayOnPhoneDialString request example</span></span>

### <a name="description"></a><span data-ttu-id="3649f-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3649f-106">Description</span></span>

<span data-ttu-id="3649f-107">Im folgenden Beispiel wird eine Anforderung SetPlayOnPhoneDialString veranschaulicht das Formular einer Anforderung an die Standardzeichenfolge Zugriffsnummern für ein Postfach festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3649f-107">The following example of a SetPlayOnPhoneDialString request shows how to form a request to set the default dial string for a mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="3649f-108">Code</span><span class="sxs-lookup"><span data-stu-id="3649f-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetPlayOnPhoneDialString xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
        <dialString>12345</dialString>
    </SetPlayOnPhoneDialString>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setplayonphonedialstring-response-example"></a><span data-ttu-id="3649f-109">Erfolgreiche SetPlayOnPhoneDialString antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="3649f-109">Successful SetPlayOnPhoneDialString response example</span></span>

### <a name="description"></a><span data-ttu-id="3649f-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3649f-110">Description</span></span>

<span data-ttu-id="3649f-111">Das folgende Beispiel einer Antwort SetPlayOnePhoneDialString zeigt eine Antwort auf die Anforderung SetPlayOnPhoneDialString.</span><span class="sxs-lookup"><span data-stu-id="3649f-111">The following example of a SetPlayOnePhoneDialString response shows a response to the SetPlayOnPhoneDialString request.</span></span>
  
### <a name="code"></a><span data-ttu-id="3649f-112">Code</span><span class="sxs-lookup"><span data-stu-id="3649f-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetPlayOnPhoneDialStringResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="3649f-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3649f-113">See also</span></span>



[<span data-ttu-id="3649f-114">SetPlayOnPhoneDialString (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="3649f-114">SetPlayOnPhoneDialString (UM web service)</span></span>](setplayonphonedialstring-um-web-service.md)
  
[<span data-ttu-id="3649f-115">SetPlayOnPhoneDialStringResponse (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="3649f-115">SetPlayOnPhoneDialStringResponse (UM web service)</span></span>](setplayonphonedialstringresponse-um-web-service.md)
  
[<span data-ttu-id="3649f-116">DialString (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="3649f-116">dialString (UM web service)</span></span>](dialstring-um-web-service.md)

