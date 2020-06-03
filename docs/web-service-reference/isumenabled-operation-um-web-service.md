---
title: IsUMEnabled-Vorgang (um-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- IsUMEnabled
api_type:
- schema
ms.assetid: fbe6cd95-f7a5-42b9-8a9d-b6159a269d55
description: Der IsUMEnabled-Vorgang bestimmt, ob ein Postfach für Unified Messaging aktiviert ist.
ms.openlocfilehash: b1478f5a113059251fe1b036ac7d77e5a4ab4f50
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458236"
---
# <a name="isumenabled-operation-um-web-service"></a><span data-ttu-id="ffbdd-103">IsUMEnabled-Vorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="ffbdd-103">IsUMEnabled operation (UM web service)</span></span>

<span data-ttu-id="ffbdd-104">Der IsUMEnabled-Vorgang bestimmt, ob ein Postfach für Unified Messaging aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-104">The IsUMEnabled operation determines whether a mailbox is enabled for Unified Messaging.</span></span>
  
## <a name="isumenabled-request-example"></a><span data-ttu-id="ffbdd-105">IsUMEnabled-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="ffbdd-105">IsUMEnabled request example</span></span>

### <a name="description"></a><span data-ttu-id="ffbdd-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ffbdd-106">Description</span></span>

<span data-ttu-id="ffbdd-107">Im folgenden Beispiel einer IsUMEnabled-Anforderung wird gezeigt, wie Sie eine Anforderung zum bestimmen, ob ein Postfach für Unified Messaging aktiviert ist, bilden.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-107">The following example of an IsUMEnabled request shows how to form a request to determine whether a mailbox is enabled for Unified Messaging.</span></span>
  
### <a name="code"></a><span data-ttu-id="ffbdd-108">Code</span><span class="sxs-lookup"><span data-stu-id="ffbdd-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <IsUMEnabled xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-isumenabled-response-example"></a><span data-ttu-id="ffbdd-109">Erfolgreiches IsUMEnabled-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="ffbdd-109">Successful IsUMEnabled response example</span></span>

### <a name="description"></a><span data-ttu-id="ffbdd-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ffbdd-110">Description</span></span>

<span data-ttu-id="ffbdd-111">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine IsUMEnabled-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-111">The following example shows a successful response to an IsUMEnabled request.</span></span>
  
### <a name="code"></a><span data-ttu-id="ffbdd-112">Code</span><span class="sxs-lookup"><span data-stu-id="ffbdd-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <IsUMEnabledResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <IsUMEnabledResponse>true</IsUMEnabledResponse> 
    </IsUMEnabledResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="ffbdd-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ffbdd-113">See also</span></span>



[<span data-ttu-id="ffbdd-114">IsUMEnabled (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="ffbdd-114">IsUMEnabled (UM web service)</span></span>](isumenabled-um-web-service.md)
  
[<span data-ttu-id="ffbdd-115">IsUMEnabledResponse (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="ffbdd-115">IsUMEnabledResponse (UM web service)</span></span>](isumenabledresponse-um-web-service.md)


[<span data-ttu-id="ffbdd-116">XML-Elemente des Unified Messaging-Webdiensts für Exchange</span><span class="sxs-lookup"><span data-stu-id="ffbdd-116">Unified Messaging web service XML elements for Exchange</span></span>](unified-messaging-web-service-xml-elements-for-exchange.md)

