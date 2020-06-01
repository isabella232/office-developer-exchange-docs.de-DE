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
# <a name="settelephoneaccessfolderemail-operation-um-web-service"></a>SetTelephoneAccessFolderEmail-Vorgang (um-Webdienst)

Mit dem SetTelephoneAccessFolderEmail-Vorgang wird der Ordner festgelegt, aus dem Unified Messaging Nachrichten über das Telefon an den Benutzer zurückliest.
  
## <a name="settelephoneaccessfolderemail-request-example"></a>SetTelephoneAccessFolderEmail-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer SetTelephoneAccessFolderEmail-Anforderung wird gezeigt, wie Sie eine Anforderung zum Festlegen des Ordners erstellen, von dem Unified Messaging über das Telefon an den Benutzer zurückgelesen wird.
  
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

## <a name="successful-settelephoneaccessfolderemail-response-example"></a>Erfolgreiches SetTelephoneAccessFolderEmail-Antwortbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer SetTelephoneAccessFolderEmail-Antwort wird eine Antwort auf die SetTelephoneAccessFolderEmail-Anforderung angezeigt.
  
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



[SetTelephoneAccessFolderEmail (um-Webdienst)](settelephoneaccessfolderemail-um-web-service.md)
  
[SetTelephoneAccessFolderEmailResponse (um-Webdienst)](settelephoneaccessfolderemailresponse-um-web-service.md)
  
[base64FolderId (um-Webdienst)](base64folderid-um-web-service.md)

