---
title: IsUMEnabled-Vorgang (UM-Webdienst)
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
description: Der Vorgang IsUMEnabled bestimmt, ob ein Postfach für Unified Messaging aktiviert ist.
ms.openlocfilehash: 9d94a359d6b11e41762d21aa2fe5501bd9f7b577
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830107"
---
# <a name="isumenabled-operation-um-web-service"></a><span data-ttu-id="e2124-103">IsUMEnabled-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="e2124-103">IsUMEnabled operation (UM web service)</span></span>

<span data-ttu-id="e2124-104">Der Vorgang IsUMEnabled bestimmt, ob ein Postfach für Unified Messaging aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e2124-104">The IsUMEnabled operation determines whether a mailbox is enabled for Unified Messaging.</span></span>
  
## <a name="isumenabled-request-example"></a><span data-ttu-id="e2124-105">Anforderungsbeispiel IsUMEnabled</span><span class="sxs-lookup"><span data-stu-id="e2124-105">IsUMEnabled request example</span></span>

### <a name="description"></a><span data-ttu-id="e2124-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2124-106">Description</span></span>

<span data-ttu-id="e2124-107">Im folgenden Beispiel wird einer Anforderung IsUMEnabled veranschaulicht das Formular einer Anforderung, um zu bestimmen, ob ein Postfach für Unified Messaging aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e2124-107">The following example of an IsUMEnabled request shows how to form a request to determine whether a mailbox is enabled for Unified Messaging.</span></span>
  
### <a name="code"></a><span data-ttu-id="e2124-108">Code</span><span class="sxs-lookup"><span data-stu-id="e2124-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <IsUMEnabled xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-isumenabled-response-example"></a><span data-ttu-id="e2124-109">Erfolgreiche IsUMEnabled antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="e2124-109">Successful IsUMEnabled response example</span></span>

### <a name="description"></a><span data-ttu-id="e2124-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2124-110">Description</span></span>

<span data-ttu-id="e2124-111">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung IsUMEnabled.</span><span class="sxs-lookup"><span data-stu-id="e2124-111">The following example shows a successful response to an IsUMEnabled request.</span></span>
  
### <a name="code"></a><span data-ttu-id="e2124-112">Code</span><span class="sxs-lookup"><span data-stu-id="e2124-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <IsUMEnabledResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <IsUMEnabledResponse>true</IsUMEnabledResponse> 
    </IsUMEnabledResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="e2124-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2124-113">See also</span></span>



[<span data-ttu-id="e2124-114">IsUMEnabled (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="e2124-114">IsUMEnabled (UM web service)</span></span>](isumenabled-um-web-service.md)
  
[<span data-ttu-id="e2124-115">IsUMEnabledResponse (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="e2124-115">IsUMEnabledResponse (UM web service)</span></span>](isumenabledresponse-um-web-service.md)


[<span data-ttu-id="e2124-116">Unified Messaging Web Service XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="e2124-116">Unified Messaging web service XML elements for Exchange</span></span>](unified-messaging-web-service-xml-elements-for-exchange.md)

