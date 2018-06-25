---
title: SendItem Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendItem
api_type:
- schema
ms.assetid: 337b89ef-e1b7-45ed-92f3-8abe4200e4c7
description: Den SendItem-Vorgang wird verwendet, um e-Mail-Nachrichten senden, die sich im Exchange-Speicher.
ms.openlocfilehash: 780778b1599d0d5e5f4b6e5b58b67773bbe18cda
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831336"
---
# <a name="senditem-operation"></a>SendItem Operation

Den SendItem-Vorgang wird verwendet, um e-Mail-Nachrichten senden, die sich im Exchange-Speicher.
  
## <a name="senditem-e-mail-message-request-example"></a>Anforderungsbeispiel den SendItem (e-Mail-Nachricht)

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird gezeigt, wie eine e-Mail-Nachricht senden.
  
### <a name="code"></a>Code

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SendItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
              SaveItemToFolder="true">
      <ItemIds>
        <t:ItemId Id="AAAtAEF=" ChangeKey="CQAAABY+T" />
      </ItemIds>
    </SendItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Kommentare

Der Elementbezeichner wurde gekürzt, um die Lesbarkeit zu erhalten.
  
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [SendItem](senditem.md)
    
- [Artikelnummern ein.](itemids.md)
    
- [ItemId](itemid.md)
    
## <a name="successful-senditem-e-mail-message-response"></a>Antwort von den erfolgreichen SendItem (e-Mail-Nachricht)

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort den SendItem.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SendItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SendItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:SendItemResponseMessage>
      </m:ResponseMessages>
    </SendItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a>Elemente einer erfolgreichen Antwort

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SendItemResponse](senditemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SendItemResponseMessage](senditemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
### <a name="comments"></a>Kommentare

Eine Stellvertretung, die versucht, eine E-mail-Nachricht zu senden, im Ordner "Entwürfe" des Prinzipals mit der SendAndSaveCopy Option festlegen, um eine Kopie in gesendete Objekte speichern definierter Ordner automatisch ein Fehler auftritt, um eine Kopie des Elements gesendete auf gesendete Objekte definierten verschieben Ordner. Das Element verbleibt im Ordner "Entwürfe" des Prinzipals. Die Umgehung für dieses Problem ist der Prinzipal Postfach im [DistinguishedFolderId](distinguishedfolderid.md) -Element angeben. 
  
Ein zusätzliches Szenario zu berücksichtigende ist, wenn ein Stellvertreter eine E-mail-Nachricht erstellt und ihn im Ordner "Entwürfe" des Postfachs der Stellvertretung speichert. Wenn die Stellvertretung versucht, senden das Element und Speichern einer Kopie des Prinzipals gesendete Objekte definierten Ordner, wird die Nachricht ordnungsgemäß gesendet die Entwurf einer Nachricht im Ordner Entwürfe der Stellvertretung, bleibt die gesendete Nachricht wird nicht in die Stellvertretung oder des Prinzipals angezeigt. Ordner Gesendete Objekte, und die Antwort erfolgreich ist.
  
## <a name="invalid-senditem-e-mail-message-request-example"></a>Ungültige Anforderung-Beispiel für den SendItem (e-Mail-Nachricht)

### <a name="description"></a>Beschreibung

Das folgende Codebeispiel zeigt ein Beispiel für eine Anforderung mit einem ungültigen Bezeichner.
  
### <a name="code"></a>Code

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SendItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
              SaveItemToFolder="true">
      <ItemIds>
        <t:ItemId Id="%BadItemId%" ChangeKey="CQAAABYAAA" />
      </ItemIds>
    </SendItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="senditem-e-mail-message-error-response"></a>Fehlerantwort den SendItem (e-Mail-Nachricht)

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine Fehlerantwort an eine den SendItem-Anforderung, die einen ungültigen Bezeichner enthält.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SendItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a>Fehler Antwortelemente

Folgende Elemente werden in der Fehlerantwort verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SendItemResponse](senditemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SendItemResponseMessage](senditemresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Siehe auch



[SendItem Operation](senditem-operation.md)
  
 **SendItemType**


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

