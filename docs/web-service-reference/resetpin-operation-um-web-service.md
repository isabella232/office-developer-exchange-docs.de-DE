---
title: ResetPIN-Vorgang (UM-Webdienst)
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
description: Der Vorgang ResetPIN die PIN-Nummer (TUI Kennwort) in einen neuen zufällig ausgewählten Wert geändert.
ms.openlocfilehash: e6417b86ce17c0d34fe857cf1209a18972cbef63
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831146"
---
# <a name="resetpin-operation-um-web-service"></a><span data-ttu-id="a25d8-103">ResetPIN-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="a25d8-103">ResetPIN operation (UM web service)</span></span>

<span data-ttu-id="a25d8-104">Der Vorgang ResetPIN die PIN-Nummer (TUI Kennwort) in einen neuen zufällig ausgewählten Wert geändert.</span><span class="sxs-lookup"><span data-stu-id="a25d8-104">The ResetPIN operation changes the PIN (TUI password) to a new random value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a25d8-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a25d8-105">Remarks</span></span>

<span data-ttu-id="a25d8-106">Der Vorgang ResetPIN erstellt eine neue PIN basierend auf PIN-Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="a25d8-106">The ResetPIN operation creates a new PIN based on the PIN policies.</span></span> <span data-ttu-id="a25d8-107">Wenn der Vorgang erfolgreich ist, wird eine E-mail-Nachricht, die die neue PIN an das Postfach des Benutzers gesendet.</span><span class="sxs-lookup"><span data-stu-id="a25d8-107">If the operation is successful, an e-mail message that contains the new PIN is sent to the mailbox of the user.</span></span> <span data-ttu-id="a25d8-108">Wenn der Vorgang fehlschlägt, wird eine Ausnahme ausgelöst, die Informationen über den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="a25d8-108">If the operation fails, it will throw an exception that contains information about the failure.</span></span>
  
## <a name="resetpin-request-example"></a><span data-ttu-id="a25d8-109">Anforderungsbeispiel ResetPIN</span><span class="sxs-lookup"><span data-stu-id="a25d8-109">ResetPIN request example</span></span>

### <a name="description"></a><span data-ttu-id="a25d8-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a25d8-110">Description</span></span>

<span data-ttu-id="a25d8-111">Im folgenden Beispiel wird eine Anforderung ResetPIN veranschaulicht eine Anforderung zum Zurücksetzen der PIN für ein Postfach zu bilden.</span><span class="sxs-lookup"><span data-stu-id="a25d8-111">The following example of a ResetPIN request shows how to form a request to reset the PIN for a mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="a25d8-112">Code</span><span class="sxs-lookup"><span data-stu-id="a25d8-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <ResetPIN xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-resetpin-response-example"></a><span data-ttu-id="a25d8-113">Erfolgreiche ResetPIN antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="a25d8-113">Successful ResetPIN response example</span></span>

### <a name="description"></a><span data-ttu-id="a25d8-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a25d8-114">Description</span></span>

<span data-ttu-id="a25d8-115">Das folgende Beispiel einer Antwort ResetPIN zeigt eine Antwort auf die Anforderung ResetPIN.</span><span class="sxs-lookup"><span data-stu-id="a25d8-115">The following example of a ResetPIN response shows a response to the ResetPIN request.</span></span>
  
### <a name="code"></a><span data-ttu-id="a25d8-116">Code</span><span class="sxs-lookup"><span data-stu-id="a25d8-116">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResetPINResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="a25d8-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a25d8-117">See also</span></span>



[<span data-ttu-id="a25d8-118">ResetPIN (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="a25d8-118">ResetPIN (UM web service)</span></span>](resetpin-um-web-service.md)
  
[<span data-ttu-id="a25d8-119">ResetPINResponse (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="a25d8-119">ResetPINResponse (UM web service)</span></span>](resetpinresponse-um-web-service.md)

