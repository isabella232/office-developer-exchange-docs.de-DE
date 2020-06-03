---
title: SendItem-Vorgang
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
description: Der SendItem-Vorgang wird zum Senden von e-Mail-Nachrichten verwendet, die sich im Exchange-Informationsspeicher befinden.
ms.openlocfilehash: 9136379e50723211fe5a483c7f113da4fa125fc1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530338"
---
# <a name="senditem-operation"></a>SendItem-Vorgang

Der SendItem-Vorgang wird zum Senden von e-Mail-Nachrichten verwendet, die sich im Exchange-Informationsspeicher befinden.
  
## <a name="senditem-e-mail-message-request-example"></a>SendItem (e-Mail-Nachricht)-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt, wie Sie eine e-Mail-Nachricht senden.
  
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

Die Element-ID wurde verkürzt, um die Lesbarkeit beizubehalten.
  
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [SendItem](senditem.md)
    
- [ItemIds](itemids.md)
    
- [ItemId](itemid.md)
    
## <a name="successful-senditem-e-mail-message-response"></a>Erfolgreiche SendItem-Antwort (e-Mail-Nachricht)

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

Ein Stellvertreter, der versucht, eine e-Mail-Nachricht zu senden, die sich im Ordner "Entwürfe" des Prinzipals befindet, wobei die Option SendAndSaveCopy, um eine Kopie im Distinguished Folder gesendete Elemente zu speichern, automatisch fehlschlägt, um eine Kopie des gesendeten Elements in den Distinguished Folder für gesendete Elemente zu verlegen. Das Element bleibt im Ordner Entwürfe des Prinzipals erhalten. Die Problemumgehung für dieses Problem besteht darin, das Postfach des Prinzipals im [DistinguishedFolderId](distinguishedfolderid.md) -Element anzugeben. 
  
Ein weiteres zu berücksichtigender Fall ist, wenn eine Stellvertretung eine e-Mail-Nachricht erstellt und im Ordner "Entwürfe" des Postfachs des Stellvertreters speichert. Wenn der Stellvertreter versucht, das Element zu senden und eine Kopie im Distinguished Items-Ordner des Prinzipals zu speichern, die Nachricht ordnungsgemäß gesendet wird, die Entwurfsnachricht im Ordner "Entwürfe" des Stellvertreters verbleibt, wird die gesendete Nachricht nicht im Ordner "Gesendete Elemente" des Stellvertreters oder des Prinzipals angezeigt, und die Antwort ist erfolgreich.
  
## <a name="invalid-senditem-e-mail-message-request-example"></a>Ungültiges SendItem (e-Mail-Nachricht)-Anforderungs Beispiel

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

## <a name="senditem-e-mail-message-error-response"></a>SendItem (e-Mail-Nachricht)-Fehlerantwort

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

