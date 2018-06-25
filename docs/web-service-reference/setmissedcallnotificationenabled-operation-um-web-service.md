---
title: SetMissedCallNotificationEnabled-Vorgang (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetMissedCallNotificationEnabled
api_type:
- schema
ms.assetid: 6693b5db-ac6b-43bc-af83-a9c94fc425bf
description: Der Vorgang SetMissedCallNotificationEnabled aktiviert oder deaktiviert die Benachrichtigungen über verpasste Anrufe.
ms.openlocfilehash: be9479d6ed2c5238ed19c3d22e028fca62b8deed
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831434"
---
# <a name="setmissedcallnotificationenabled-operation-um-web-service"></a><span data-ttu-id="20802-103">SetMissedCallNotificationEnabled-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="20802-103">SetMissedCallNotificationEnabled operation (UM web service)</span></span>

<span data-ttu-id="20802-104">Der Vorgang SetMissedCallNotificationEnabled aktiviert oder deaktiviert die Benachrichtigungen über verpasste Anrufe.</span><span class="sxs-lookup"><span data-stu-id="20802-104">The SetMissedCallNotificationEnabled operation enables or disables missed call notifications.</span></span>
  
## <a name="setmissedcallnotificationenabled-request-example"></a><span data-ttu-id="20802-105">Anforderungsbeispiel SetMissedCallNotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="20802-105">SetMissedCallNotificationEnabled request example</span></span>

### <a name="description"></a><span data-ttu-id="20802-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20802-106">Description</span></span>

<span data-ttu-id="20802-107">Im folgenden Beispiel wird eine Anforderung SetMissedCallNotificationEnabled veranschaulicht eine Anforderung zum Aktivieren von Benachrichtigungen über verpasste Anrufe bilden.</span><span class="sxs-lookup"><span data-stu-id="20802-107">The following example of a SetMissedCallNotificationEnabled request shows how to form a request to enable missed call notifications.</span></span>
  
### <a name="code"></a><span data-ttu-id="20802-108">Code</span><span class="sxs-lookup"><span data-stu-id="20802-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetMissedCallNotificationEnabled xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
        <status>true</status>
    </SetMissedCallNotificationEnabled>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setmissedcallnotificationenabled-response-example"></a><span data-ttu-id="20802-109">Erfolgreiche SetMissedCallNotificationEnabled antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="20802-109">Successful SetMissedCallNotificationEnabled response example</span></span>

### <a name="description"></a><span data-ttu-id="20802-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20802-110">Description</span></span>

<span data-ttu-id="20802-111">Das folgende Beispiel einer Antwort PlayOnPhoneGreeting zeigt eine Antwort auf die Anforderung SetMissedCallNotificationEnabled.</span><span class="sxs-lookup"><span data-stu-id="20802-111">The following example of a PlayOnPhoneGreeting response shows a response to the SetMissedCallNotificationEnabled request.</span></span>
  
### <a name="code"></a><span data-ttu-id="20802-112">Code</span><span class="sxs-lookup"><span data-stu-id="20802-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetMissedCallNotificationEnabledResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="20802-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20802-113">See also</span></span>



[<span data-ttu-id="20802-114">SetMissedCallNotificationEnabled (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="20802-114">SetMissedCallNotificationEnabled (UM web service)</span></span>](setmissedcallnotificationenabled-um-web-service.md)
  
[<span data-ttu-id="20802-115">SetMissedCallNotificationEnabledResponse (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="20802-115">SetMissedCallNotificationEnabledResponse (UM web service)</span></span>](setmissedcallnotificationenabledresponse-um-web-service.md)
  
[<span data-ttu-id="20802-116">Status (UM-Webdienst - SetMissedCallNotificationEnabled)</span><span class="sxs-lookup"><span data-stu-id="20802-116">Status (UM web service - SetMissedCallNotificationEnabled)</span></span>](status-um-web-servicesetmissedcallnotificationenabled.md)

