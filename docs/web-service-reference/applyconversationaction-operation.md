---
title: ApplyConversationAction-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ApplyConversationAction
api_type:
- schema
ms.assetid: 73d7943d-d361-4f8b-9948-d85f886efa1a
description: Der ApplyConversationAction-Vorgang legt eine einmalige oder Nachverfolgungsaktion für alle Elemente in einer Unterhaltung fest. Mit dem ApplyConversationAction-Vorgang können Sie den Status "lesen" für alle Elemente in einer Unterhaltung kategorisieren, verlagern, kopieren, löschen und festlegen. Aktionen können auch für neue Nachrichten in einer Unterhaltung festgelegt werden.
ms.openlocfilehash: cdab239a5b0b1406d2ce31f4604e4737d037cd7e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463503"
---
# <a name="applyconversationaction-operation"></a>ApplyConversationAction-Vorgang

Der **ApplyConversationAction** -Vorgang legt eine einmalige oder Nachverfolgungsaktion für alle Elemente in einer Unterhaltung fest. Mit dem **ApplyConversationAction** -Vorgang können Sie den Status "lesen" für alle Elemente in einer Unterhaltung kategorisieren, verlagern, kopieren, löschen und festlegen. Aktionen können auch für neue Nachrichten in einer Unterhaltung festgelegt werden. 
  
## <a name="applyconversationaction-request-example"></a>ApplyConversationAction-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer **ApplyConversationAction** -Anforderung wird gezeigt, wie die Elemente in der angegebenen Unterhaltung in einen anderen Ordner verschoben werden. Elemente, die der Unterhaltung hinzugefügt werden, werden ebenfalls in den angegebenen Ordner verschoben. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:ApplyConversationAction>
      <m:ConversationActions>
        <t:ConversationAction>
          <t:Action>AlwaysMove</t:Action>
          <t:ConversationId Id="AAQkADVkNjM1EH39AWcDUGrnrnJ32hHpdc="/>
          <t:DestinationFolderId>
            <t:FolderId Id="AAMkADVkNjM1ODI3LTEwYTAtNDUBTTT6tWal35iSoKAAAABZZWAAA="/>
          </t:DestinationFolderId>
        </t:ConversationAction>
      </m:ConversationActions>
    </m:ApplyConversationAction>
  </soap:Body>
</soap:Envelope>
```

### <a name="remarks"></a>Bemerkungen

Die Konversations-und Ordner Bezeichner wurden verkürzt, um die Lesbarkeit zu erhalten.
  
## <a name="applyconversationaction-response-example"></a>ApplyConversationAction-Antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **ApplyConversationAction** -Anforderung. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="1" 
                         MajorBuildNumber="91" 
                         MinorBuildNumber="0" 
                         Version="Exchange2010_SP1" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:ApplyConversationActionResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:ApplyConversationActionResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:ApplyConversationActionResponseMessage>
      </m:ResponseMessages>
    </m:ApplyConversationActionResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a>Siehe auch

- [ApplyConversationAction-Vorgang](applyconversationaction-operation.md)
- [EWS-Operationen in Exchange](ews-operations-in-exchange.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Conversations in EWS](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

