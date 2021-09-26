---
title: SetTelephoneAccessFolderEmail-Vorgang (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- SetTelephoneAccessFolderEmail
api_type:
- schema
ms.assetid: 2c92d914-bdee-4337-b3ea-0655fdb658e9
description: Der SetTelephoneAccessFolderEmail-Vorgang legt den Ordner fest, aus dem Unified Messaging Nachrichten an den Benutzer über das Telefon zurücklesen wird.
ms.openlocfilehash: cf8e80e021d6467ba3a724cc0d04e165e00e8397
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544717"
---
# <a name="settelephoneaccessfolderemail-operation-um-web-service"></a>SetTelephoneAccessFolderEmail-Vorgang (UM-Webdienst)

Der SetTelephoneAccessFolderEmail-Vorgang legt den Ordner fest, aus dem Unified Messaging Nachrichten an den Benutzer über das Telefon zurücklesen wird.
  
## <a name="settelephoneaccessfolderemail-request-example"></a>SetTelephoneAccessFolderEmail-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer SetTelephoneAccessFolderEmail-Anforderung zeigt, wie Sie eine Anforderung zum Festlegen des Ordners erstellen, aus dem Unified Messaging dem Benutzer per Telefon zurückgelesen wird.
  
### <a name="code"></a>Code

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

## <a name="successful-settelephoneaccessfolderemail-response-example"></a>Beispiel für eine erfolgreiche SetTelephoneAccessFolderEmail-Antwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer SetTelephoneAccessFolderEmail-Antwort zeigt eine Antwort auf die SetTelephoneAccessFolderEmail-Anforderung.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetTelephoneAccessFolderEmailResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Siehe auch



[SetTelephoneAccessFolderEmail (UM-Webdienst)](settelephoneaccessfolderemail-um-web-service.md)
  
[SetTelephoneAccessFolderEmailResponse (UM-Webdienst)](settelephoneaccessfolderemailresponse-um-web-service.md)
  
[base64FolderId (UM-Webdienst)](base64folderid-um-web-service.md)

