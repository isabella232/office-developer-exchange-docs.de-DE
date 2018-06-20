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
# <a name="settelephoneaccessfolderemail-operation-um-web-service"></a>SetTelephoneAccessFolderEmail-Vorgang (UM-Webdienst)

Der Vorgang SetTelephoneAccessFolderEmail legt fest, den Ordner aus dem Unified Messaging Back Nachrichten an den Benutzer über das Telefon gelesen werden.
  
## <a name="settelephoneaccessfolderemail-request-example"></a>Anforderungsbeispiel SetTelephoneAccessFolderEmail

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine Anforderung SetTelephoneAccessFolderEmail veranschaulicht das Formular einer Anforderung an den Ordner festlegen aus dem Unified Messaging zurück an dem Benutzer über das Telefon gelesen werden.
  
### <a name="code"></a>Code

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

## <a name="successful-settelephoneaccessfolderemail-response-example"></a>Erfolgreiche SetTelephoneAccessFolderEmail antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer Antwort SetTelephoneAccessFolderEmail zeigt eine Antwort auf die Anforderung SetTelephoneAccessFolderEmail.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetTelephoneAccessFolderEmailResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Siehe auch



[SetTelephoneAccessFolderEmail (UM-Webdienst)](settelephoneaccessfolderemail-um-web-service.md)
  
[SetTelephoneAccessFolderEmailResponse (UM-Webdienst)](settelephoneaccessfolderemailresponse-um-web-service.md)
  
[base64FolderId (UM-Webdienst)](base64folderid-um-web-service.md)

