---
title: ResetPIN-Vorgang (um-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- ResetPIN
api_type:
- schema
ms.assetid: c0f14a15-3389-4311-8bac-f87930c5f5d4
description: Der ResetPIN-Vorgang ändert die PIN (TUI Password) in einen neuen Zufallswert.
ms.openlocfilehash: 8de64ce7a47e9c426f8eb9298e1ca00508fb616c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465492"
---
# <a name="resetpin-operation-um-web-service"></a><span data-ttu-id="b0084-103">ResetPIN-Vorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="b0084-103">ResetPIN operation (UM web service)</span></span>

<span data-ttu-id="b0084-104">Der ResetPIN-Vorgang ändert die PIN (TUI Password) in einen neuen Zufallswert.</span><span class="sxs-lookup"><span data-stu-id="b0084-104">The ResetPIN operation changes the PIN (TUI password) to a new random value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b0084-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0084-105">Remarks</span></span>

<span data-ttu-id="b0084-106">Mit dem ResetPIN-Vorgang wird eine neue PIN basierend auf den PIN-Richtlinien erstellt.</span><span class="sxs-lookup"><span data-stu-id="b0084-106">The ResetPIN operation creates a new PIN based on the PIN policies.</span></span> <span data-ttu-id="b0084-107">Wenn der Vorgang erfolgreich war, wird eine e-Mail-Nachricht mit der neuen PIN an das Postfach des Benutzers gesendet.</span><span class="sxs-lookup"><span data-stu-id="b0084-107">If the operation is successful, an e-mail message that contains the new PIN is sent to the mailbox of the user.</span></span> <span data-ttu-id="b0084-108">Wenn der Vorgang fehlschlägt, wird eine Ausnahme ausgelöst, die Informationen über den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="b0084-108">If the operation fails, it will throw an exception that contains information about the failure.</span></span>
  
## <a name="resetpin-request-example"></a><span data-ttu-id="b0084-109">ResetPIN-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="b0084-109">ResetPIN request example</span></span>

### <a name="description"></a><span data-ttu-id="b0084-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0084-110">Description</span></span>

<span data-ttu-id="b0084-111">Das folgende Beispiel einer ResetPIN-Anforderung zeigt, wie Sie eine Anforderung zum Zurücksetzen der PIN für ein Postfach bilden.</span><span class="sxs-lookup"><span data-stu-id="b0084-111">The following example of a ResetPIN request shows how to form a request to reset the PIN for a mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="b0084-112">Code</span><span class="sxs-lookup"><span data-stu-id="b0084-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <ResetPIN xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-resetpin-response-example"></a><span data-ttu-id="b0084-113">Erfolgreiches ResetPIN-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="b0084-113">Successful ResetPIN response example</span></span>

### <a name="description"></a><span data-ttu-id="b0084-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0084-114">Description</span></span>

<span data-ttu-id="b0084-115">Im folgenden Beispiel einer ResetPIN-Antwort wird eine Antwort auf die ResetPIN-Anforderung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b0084-115">The following example of a ResetPIN response shows a response to the ResetPIN request.</span></span>
  
### <a name="code"></a><span data-ttu-id="b0084-116">Code</span><span class="sxs-lookup"><span data-stu-id="b0084-116">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResetPINResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="b0084-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0084-117">See also</span></span>



[<span data-ttu-id="b0084-118">ResetPIN (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="b0084-118">ResetPIN (UM web service)</span></span>](resetpin-um-web-service.md)
  
[<span data-ttu-id="b0084-119">ResetPINResponse (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="b0084-119">ResetPINResponse (UM web service)</span></span>](resetpinresponse-um-web-service.md)

