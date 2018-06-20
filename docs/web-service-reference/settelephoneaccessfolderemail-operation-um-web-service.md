---
title: SetTelephoneAccessFolderEmail-Vorgang (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetTelephoneAccessFolderEmail
api_type:
- schema
ms.assetid: 2c92d914-bdee-4337-b3ea-0655fdb658e9
description: Der Vorgang SetTelephoneAccessFolderEmail legt fest, den Ordner aus dem Unified Messaging Back Nachrichten an den Benutzer über das Telefon gelesen werden.
ms.openlocfilehash: 9497e58f66b8efcf7e358aa529223942298a3bed
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831459"
---
# <a name="settelephoneaccessfolderemail-operation-um-web-service"></a><span data-ttu-id="74e8f-103">SetTelephoneAccessFolderEmail-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="74e8f-103">SetTelephoneAccessFolderEmail operation (UM web service)</span></span>

<span data-ttu-id="74e8f-104">Der Vorgang SetTelephoneAccessFolderEmail legt fest, den Ordner aus dem Unified Messaging Back Nachrichten an den Benutzer über das Telefon gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="74e8f-104">The SetTelephoneAccessFolderEmail operation sets the folder from which Unified Messaging will read back messages to the user over the telephone.</span></span>
  
## <a name="settelephoneaccessfolderemail-request-example"></a><span data-ttu-id="74e8f-105">Anforderungsbeispiel SetTelephoneAccessFolderEmail</span><span class="sxs-lookup"><span data-stu-id="74e8f-105">SetTelephoneAccessFolderEmail request example</span></span>

### <a name="description"></a><span data-ttu-id="74e8f-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="74e8f-106">Description</span></span>

<span data-ttu-id="74e8f-107">Im folgenden Beispiel wird eine Anforderung SetTelephoneAccessFolderEmail veranschaulicht das Formular einer Anforderung an den Ordner festlegen aus dem Unified Messaging zurück an dem Benutzer über das Telefon gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="74e8f-107">The following example of a SetTelephoneAccessFolderEmail request shows how to form a request to set the folder from which Unified Messaging will read back to the user over the telephone.</span></span>
  
### <a name="code"></a><span data-ttu-id="74e8f-108">Code</span><span class="sxs-lookup"><span data-stu-id="74e8f-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetTelephoneAccessFolderEmail xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <base64FolderID>AAAAAGsd2rbQLVtLobUGbrq/9IUBAEX2ikn/L8JJtI5WHI0FAW8AAAFXHhsAAA==</base64FolderID>
    </SetTelephoneAccessFolderEmail>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-settelephoneaccessfolderemail-response-example"></a><span data-ttu-id="74e8f-109">Erfolgreiche SetTelephoneAccessFolderEmail antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="74e8f-109">Successful SetTelephoneAccessFolderEmail response example</span></span>

### <a name="description"></a><span data-ttu-id="74e8f-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="74e8f-110">Description</span></span>

<span data-ttu-id="74e8f-111">Das folgende Beispiel einer Antwort SetTelephoneAccessFolderEmail zeigt eine Antwort auf die Anforderung SetTelephoneAccessFolderEmail.</span><span class="sxs-lookup"><span data-stu-id="74e8f-111">The following example of a SetTelephoneAccessFolderEmail response shows a response to the SetTelephoneAccessFolderEmail request.</span></span>
  
### <a name="code"></a><span data-ttu-id="74e8f-112">Code</span><span class="sxs-lookup"><span data-stu-id="74e8f-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetTelephoneAccessFolderEmailResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="74e8f-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74e8f-113">See also</span></span>



[<span data-ttu-id="74e8f-114">SetTelephoneAccessFolderEmail (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="74e8f-114">SetTelephoneAccessFolderEmail (UM web service)</span></span>](settelephoneaccessfolderemail-um-web-service.md)
  
[<span data-ttu-id="74e8f-115">SetTelephoneAccessFolderEmailResponse (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="74e8f-115">SetTelephoneAccessFolderEmailResponse (UM web service)</span></span>](settelephoneaccessfolderemailresponse-um-web-service.md)
  
[<span data-ttu-id="74e8f-116">base64FolderId (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="74e8f-116">base64FolderId (UM web service)</span></span>](base64folderid-um-web-service.md)

