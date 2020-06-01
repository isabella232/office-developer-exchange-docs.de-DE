---
title: SetTelephoneAccessFolderEmail-Vorgang (um-Webdienst)
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
description: Mit dem SetTelephoneAccessFolderEmail-Vorgang wird der Ordner festgelegt, aus dem Unified Messaging Nachrichten über das Telefon an den Benutzer zurückliest.
ms.openlocfilehash: a2bb630f812ca811b4cbe68db1308dc18e5d3ba0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467333"
---
# <a name="settelephoneaccessfolderemail-operation-um-web-service"></a><span data-ttu-id="6fdbd-103">SetTelephoneAccessFolderEmail-Vorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="6fdbd-103">SetTelephoneAccessFolderEmail operation (UM web service)</span></span>

<span data-ttu-id="6fdbd-104">Mit dem SetTelephoneAccessFolderEmail-Vorgang wird der Ordner festgelegt, aus dem Unified Messaging Nachrichten über das Telefon an den Benutzer zurückliest.</span><span class="sxs-lookup"><span data-stu-id="6fdbd-104">The SetTelephoneAccessFolderEmail operation sets the folder from which Unified Messaging will read back messages to the user over the telephone.</span></span>
  
## <a name="settelephoneaccessfolderemail-request-example"></a><span data-ttu-id="6fdbd-105">SetTelephoneAccessFolderEmail-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="6fdbd-105">SetTelephoneAccessFolderEmail request example</span></span>

### <a name="description"></a><span data-ttu-id="6fdbd-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6fdbd-106">Description</span></span>

<span data-ttu-id="6fdbd-107">Im folgenden Beispiel einer SetTelephoneAccessFolderEmail-Anforderung wird gezeigt, wie Sie eine Anforderung zum Festlegen des Ordners erstellen, von dem Unified Messaging über das Telefon an den Benutzer zurückgelesen wird.</span><span class="sxs-lookup"><span data-stu-id="6fdbd-107">The following example of a SetTelephoneAccessFolderEmail request shows how to form a request to set the folder from which Unified Messaging will read back to the user over the telephone.</span></span>
  
### <a name="code"></a><span data-ttu-id="6fdbd-108">Code</span><span class="sxs-lookup"><span data-stu-id="6fdbd-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetTelephoneAccessFolderEmail xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <base64FolderID>AAAAAGsd2rbQLVtLobUGbrq/9IUBAEX2ikn/L8JJtI5WHI0FAW8AAAFXHhsAAA==</base64FolderID>
    </SetTelephoneAccessFolderEmail>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-settelephoneaccessfolderemail-response-example"></a><span data-ttu-id="6fdbd-109">Erfolgreiches SetTelephoneAccessFolderEmail-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="6fdbd-109">Successful SetTelephoneAccessFolderEmail response example</span></span>

### <a name="description"></a><span data-ttu-id="6fdbd-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6fdbd-110">Description</span></span>

<span data-ttu-id="6fdbd-111">Im folgenden Beispiel einer SetTelephoneAccessFolderEmail-Antwort wird eine Antwort auf die SetTelephoneAccessFolderEmail-Anforderung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6fdbd-111">The following example of a SetTelephoneAccessFolderEmail response shows a response to the SetTelephoneAccessFolderEmail request.</span></span>
  
### <a name="code"></a><span data-ttu-id="6fdbd-112">Code</span><span class="sxs-lookup"><span data-stu-id="6fdbd-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetTelephoneAccessFolderEmailResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="6fdbd-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fdbd-113">See also</span></span>



[<span data-ttu-id="6fdbd-114">SetTelephoneAccessFolderEmail (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="6fdbd-114">SetTelephoneAccessFolderEmail (UM web service)</span></span>](settelephoneaccessfolderemail-um-web-service.md)
  
[<span data-ttu-id="6fdbd-115">SetTelephoneAccessFolderEmailResponse (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="6fdbd-115">SetTelephoneAccessFolderEmailResponse (UM web service)</span></span>](settelephoneaccessfolderemailresponse-um-web-service.md)
  
[<span data-ttu-id="6fdbd-116">base64FolderId (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="6fdbd-116">base64FolderId (UM web service)</span></span>](base64folderid-um-web-service.md)

