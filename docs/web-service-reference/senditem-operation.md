---
title: SendItem-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SendItem
api_type:
- schema
ms.assetid: 337b89ef-e1b7-45ed-92f3-8abe4200e4c7
description: Der SendItem-Vorgang wird verwendet, um E-Mail-Nachrichten zu senden, die sich im Exchange Speicher befinden.
ms.openlocfilehash: d1e43cdceb3a594c3fa2f028502a3bfedbbf85a1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521585"
---
# <a name="senditem-operation"></a>SendItem-Vorgang

Der SendItem-Vorgang wird verwendet, um E-Mail-Nachrichten zu senden, die sich im Exchange Speicher befinden.
  
## <a name="senditem-e-mail-message-request-example"></a>SendItem-Anforderungsbeispiel (E-Mail-Nachricht)

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt, wie Sie eine E-Mail-Nachricht senden.
  
### <a name="code"></a>Code

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SendItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
              SaveItemToFolder="true">
      <ItemIds>
        <t:ItemId Id="AAAtAEF=" ChangeKey="CQAAABY+T" />
      </ItemIds>
    </SendItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comments

Der Elementbezeichner wurde gekürzt, um die Lesbarkeit zu gewährleisten.
  
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [SendItem](senditem.md)
    
- [ItemIds](itemids.md)
    
- [ItemId](itemid.md)
    
## <a name="successful-senditem-e-mail-message-response"></a>Erfolgreiche SendItem-Antwort (E-Mail-Nachricht)

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche SendItem-Antwort.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SendItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SendItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:SendItemResponseMessage>
      </m:ResponseMessages>
    </SendItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a>Erfolgreiche Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SendItemResponse](senditemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SendItemResponseMessage](senditemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
### <a name="comments"></a>Kommentare

Ein Delegat, der versucht, eine E-Mail-Nachricht zu senden, die sich im Ordner "Entwürfe" des Prinzipals mit der Option "SendAndSaveCopy" befindet, um eine Kopie im Ordner "Gesendete Elemente" zu speichern, kann im Hintergrund eine Kopie des gesendeten Elements nicht in den Ordner "Gesendete Elemente" verschieben. Das Element verbleibt im Ordner "Entwürfe" des Prinzipals. Die Problemumgehung für dieses Problem besteht darin, das Postfach des Prinzipals im [DistinguishedFolderId-Element](distinguishedfolderid.md) anzugeben. 
  
Ein weiteres zu berücksichtigendes Szenario ist, wenn ein Delegat eine E-Mail-Nachricht erstellt und im Ordner "Entwürfe" des Postfachs der Stellvertretung speichert. Wenn der Delegat versucht, das Element zu senden und eine Kopie im Ordner "Gesendete Elemente" des Prinzipals zu speichern, wird die Nachricht ordnungsgemäß gesendet, die Entwurfsnachricht verbleibt im Ordner "Entwürfe", die gesendete Nachricht wird weder im Ordner "Gesendete Elemente" des Stellvertreters noch im Ordner "Gesendete Elemente" des Prinzipals angezeigt, und die Antwort ist erfolgreich.
  
## <a name="invalid-senditem-e-mail-message-request-example"></a>Ungültiges SendItem-Anforderungsbeispiel (E-Mail-Nachricht)

### <a name="description"></a>Beschreibung

Das folgende Codebeispiel zeigt ein Beispiel für eine Anforderung mit einem ungültigen Bezeichner.
  
### <a name="code"></a>Code

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SendItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
              SaveItemToFolder="true">
      <ItemIds>
        <t:ItemId Id="%BadItemId%" ChangeKey="CQAAABYAAA" />
      </ItemIds>
    </SendItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="senditem-e-mail-message-error-response"></a>SendItem -Fehlerantwort (E-Mail-Nachricht)

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine Fehlerantwort auf eine SendItem-Anforderung, die einen ungültigen Bezeichner enthält.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SendItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SendItemResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:SendItemResponseMessage>
      </m:ResponseMessages>
    </SendItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>Fehlerantwortelemente

Folgende Elemente werden in der Fehlerantwort verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SendItemResponse](senditemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SendItemResponseMessage](senditemresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Siehe auch



[SendItem-Vorgang](senditem-operation.md)
  
 **SendItemType**


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

