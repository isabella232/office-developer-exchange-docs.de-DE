---
title: GetUMProperties-Vorgang (um-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- GetUMProperties
api_type:
- schema
ms.assetid: 301fb9a3-67df-44c4-8ffe-0600237fc344
description: Der GetUMProperties-Vorgang ruft alle Unified Messaging-Eigenschaften für das Postfach des Benutzers ab, der die Anforderung macht.
ms.openlocfilehash: 42176d9cd0288af6515aeea616a4f216a419410c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462472"
---
# <a name="getumproperties-operation-um-web-service"></a><span data-ttu-id="5f68e-103">GetUMProperties-Vorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="5f68e-103">GetUMProperties operation (UM web service)</span></span>

<span data-ttu-id="5f68e-104">Der GetUMProperties-Vorgang ruft alle Unified Messaging-Eigenschaften für das Postfach des Benutzers ab, der die Anforderung macht.</span><span class="sxs-lookup"><span data-stu-id="5f68e-104">The GetUMProperties operation gets all the Unified Messaging properties for the mailbox of the user who is making the request.</span></span>
  
## <a name="getumproperties-request-example"></a><span data-ttu-id="5f68e-105">GetUMProperties-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="5f68e-105">GetUMProperties request example</span></span>

### <a name="description"></a><span data-ttu-id="5f68e-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f68e-106">Description</span></span>

<span data-ttu-id="5f68e-107">Im folgenden Beispiel einer GetUMProperties-Anforderung wird gezeigt, wie Sie eine Anforderung zum Abrufen der Unified Messaging-Eigenschaften eines Postfachs bilden.</span><span class="sxs-lookup"><span data-stu-id="5f68e-107">The following example of a GetUMProperties request shows how to form a request to get the Unified Messaging properties of a mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="5f68e-108">Code</span><span class="sxs-lookup"><span data-stu-id="5f68e-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetUMProperties xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-getumproperties-response-example"></a><span data-ttu-id="5f68e-109">Erfolgreiches GetUMProperties-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="5f68e-109">Successful GetUMProperties response example</span></span>

### <a name="description"></a><span data-ttu-id="5f68e-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f68e-110">Description</span></span>

<span data-ttu-id="5f68e-111">Im folgenden Beispiel einer GetUMProperties-Antwort wird eine Antwort auf die GetUMProperties-Anforderung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5f68e-111">The following example of a GetUMProperties response shows a response to the GetUMProperties request.</span></span>
  
### <a name="code"></a><span data-ttu-id="5f68e-112">Code</span><span class="sxs-lookup"><span data-stu-id="5f68e-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <GetUMPropertiesResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <GetUMPropertiesResponse>
        <OofStatus>false</OofStatus> 
        <MissedCallNotificationEnabled>true</MissedCallNotificationEnabled> 
        <PlayOnPhoneDialString>12345</PlayOnPhoneDialString> 
        <TelephoneAccessNumbers>54321</TelephoneAccessNumbers> 
        <TelephoneAccessFolderEmail>AAAAAGsd2rbQLVtLobUGbrq/9IUBAEX2ikn/L8JJtI5WHI0FAW8AAAFXHhsAAA==</TelephoneAccessFolderEmail> 
      </GetUMPropertiesResponse>
    </GetUMPropertiesResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="5f68e-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f68e-113">See also</span></span>



[<span data-ttu-id="5f68e-114">GetUMProperties (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="5f68e-114">GetUMProperties (UM web service)</span></span>](getumproperties-um-web-service.md)
  
[<span data-ttu-id="5f68e-115">GetUMPropertiesResponse (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="5f68e-115">GetUMPropertiesResponse (UM web service)</span></span>](getumpropertiesresponse-um-web-service.md)

