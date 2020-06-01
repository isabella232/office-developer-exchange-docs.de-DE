---
title: SetPlayOnPhoneDialString-Vorgang (um-Webdienst)
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
description: Mit dem SetPlayOnPhoneDialString-Vorgang wird die Wählzeichenfolge festgelegt, die als Standard für den PlayOnPhone-Vorgang (um-Webdienst) und den PlayOnPhoneGreeting-Vorgang (um-Webdienst) verwendet werden soll.
ms.openlocfilehash: 7df806eedc2d6d037394f31ec4ccbfe28aaf3372
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458642"
---
# <a name="setplayonphonedialstring-operation-um-web-service"></a><span data-ttu-id="38576-103">SetPlayOnPhoneDialString-Vorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="38576-103">SetPlayOnPhoneDialString operation (UM web service)</span></span>

<span data-ttu-id="38576-104">Mit dem SetPlayOnPhoneDialString-Vorgang wird die Wählzeichenfolge festgelegt, die als Standard für den [PlayOnPhone-Vorgang (um-Webdienst)](playonphone-operation-um-web-service.md) und den [PlayOnPhoneGreeting-Vorgang (um-Webdienst)](playonphonegreeting-operation-um-web-service.md)verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="38576-104">The SetPlayOnPhoneDialString operation sets the dial string to use as the default for the [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) and the [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md).</span></span>
  
## <a name="setplayonphonedialstring-request-example"></a><span data-ttu-id="38576-105">SetPlayOnPhoneDialString-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="38576-105">SetPlayOnPhoneDialString request example</span></span>

### <a name="description"></a><span data-ttu-id="38576-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38576-106">Description</span></span>

<span data-ttu-id="38576-107">Das folgende Beispiel einer SetPlayOnPhoneDialString-Anforderung zeigt, wie Sie eine Anforderung zum Festlegen der standardmäßigen Wählzeichenfolge für ein Postfach bilden.</span><span class="sxs-lookup"><span data-stu-id="38576-107">The following example of a SetPlayOnPhoneDialString request shows how to form a request to set the default dial string for a mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="38576-108">Code</span><span class="sxs-lookup"><span data-stu-id="38576-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetPlayOnPhoneDialString xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
        <dialString>12345</dialString>
    </SetPlayOnPhoneDialString>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setplayonphonedialstring-response-example"></a><span data-ttu-id="38576-109">Erfolgreiches SetPlayOnPhoneDialString-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="38576-109">Successful SetPlayOnPhoneDialString response example</span></span>

### <a name="description"></a><span data-ttu-id="38576-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38576-110">Description</span></span>

<span data-ttu-id="38576-111">Im folgenden Beispiel einer SetPlayOnePhoneDialString-Antwort wird eine Antwort auf die SetPlayOnPhoneDialString-Anforderung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="38576-111">The following example of a SetPlayOnePhoneDialString response shows a response to the SetPlayOnPhoneDialString request.</span></span>
  
### <a name="code"></a><span data-ttu-id="38576-112">Code</span><span class="sxs-lookup"><span data-stu-id="38576-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetPlayOnPhoneDialStringResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="38576-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38576-113">See also</span></span>



[<span data-ttu-id="38576-114">SetPlayOnPhoneDialString (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="38576-114">SetPlayOnPhoneDialString (UM web service)</span></span>](setplayonphonedialstring-um-web-service.md)
  
[<span data-ttu-id="38576-115">SetPlayOnPhoneDialStringResponse (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="38576-115">SetPlayOnPhoneDialStringResponse (UM web service)</span></span>](setplayonphonedialstringresponse-um-web-service.md)
  
[<span data-ttu-id="38576-116">Wähl Dienst (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="38576-116">dialString (UM web service)</span></span>](dialstring-um-web-service.md)

