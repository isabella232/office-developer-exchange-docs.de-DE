---
title: GetMailTips-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetMailTips
api_type:
- schema
ms.assetid: 025483ec-a9f3-4735-8a95-d26e30ea7974
description: Der GetMailTips-Vorgang ruft die E-Mail-Tipps für das angegebene Postfach ab.
ms.openlocfilehash: ec139f7a1a464aa8c30d8dd2043f441874231dc2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59533794"
---
# <a name="getmailtips-operation"></a>GetMailTips-Vorgang

Der **GetMailTips-Vorgang** ruft die E-Mail-Tipps für das angegebene Postfach ab. 
  
## <a name="getmailtips-request-example"></a>GetMailTips-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Der Client erstellt die Anforderungs-XML und sendet sie an den Server. Die Anforderung gibt an, an wen der Client gesendet wird, das Postfach zum Abrufen der E-Mail-Tipps und welche E-Mail-Tipps angefordert werden. In diesem Beispiel fordert der Client an, dass alle E-Mail-Tipps für das ausgewählte Postfach zurückgegeben werden.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"> 
  <soap:Header> 
    <t:RequestServerVersion Version="Exchange2010" /> 
  </soap:Header> 
  <soap:Body> 
    <GetMailTips xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"> 
      <SendingAs> 
        <t:EmailAddress> user1@contoso.com </t:EmailAddress> 
        <t:RoutingType>SMTP</t:RoutingType> 
      </SendingAs> 
      <Recipients> 
        <t:Mailbox> 
          <t:EmailAddress> user2@contoso.com </t:EmailAddress> 
          <t:RoutingType>SMTP</t:RoutingType> 
        </t:Mailbox> 
      </Recipients> 
      <MailTipsRequested>All</MailTipsRequested> 
    </GetMailTips> 
  </soap:Body> 
</soap:Envelope>
```

### <a name="request-elements"></a>Anfordern von Elementen

Die folgenden Elemente sind in der Anforderung enthalten:
  
- [GetMailTips](getmailtips.md)
    
- [SendingAs](sendingas.md)
    
- [Empfänger (ArrayOfRecipientsType)](recipients-arrayofrecipientstype.md)
    
- [MailTipsRequested](mailtipsrequested.md)
    
## <a name="successful-getmailtips-response-example"></a>Beispiel für erfolgreiche GetMailTips-Antwort

### <a name="description"></a>Beschreibung

Der folgende SOAP-Text (Simple Object Access Protocol) zeigt eine erfolgreiche Antwort auf die **GetMailTips-Anforderung.** 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?> 
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/"> 
  <s:Header> 
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="0" MajorBuildNumber="536" MinorBuildNumber="0" Version="Exchange2010" 
xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xmlns:xsd="http://www.w3.org/2001/XMLSchema"/> 
  </s:Header> 
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"> 
    <GetMailTipsResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"> 
      <ResponseCode>NoError</ResponseCode> 
      <ResponseMessages> 
        <MailTipsResponseMessageType ResponseClass="Success"> 
        <ResponseCode>NoError</ResponseCode> 
        <m:MailTips xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"> 20 / 29 [MS-OXWMT] — v20100517 Mail Tips Web Service Extensions Copyright © 2010 Microsoft Corporation. Release: Monday, May 17, 2010 
          <t:RecipientAddress xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"> 
          <t:Name/> 
          <t:EmailAddress>user2@contoso.com</t:EmailAddress> 
          <t:RoutingType>SMTP</t:RoutingType> 
          </t:RecipientAddress> 
          <t:PendingMailTips xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/> 
          <t:OutOfOffice xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"> 
            <t:ReplyBody> 
              <t:Message/> 
            </t:ReplyBody> 
          </t:OutOfOffice> 
          <t:MailboxFull xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">false</t:MailboxFull> 
          <t:CustomMailTip xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">Hello World Mailtips</t:CustomMailTip> 
          <t:TotalMemberCount xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">1</t:TotalMemberCount> 
          <t:ExternalMemberCount xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">0</t:ExternalMemberCount> 
          <t:MaxMessageSize xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">10485760</t:MaxMessageSize> 
          <t:DeliveryRestricted xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">false</t:DeliveryRestricted> 
          <t:IsModerated xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">false</t:IsModerated> 
          <t:InvalidRecipient xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">false</t:InvalidRecipient> 
        </m:MailTips> 
        </MailTipsResponseMessageType> 
      </ResponseMessages> 
    </GetMailTipsResponse> 
  </s:Body> 
</s:Envelope>
```

### <a name="response-elements"></a>Antwortelemente

Die folgenden Elemente sind in der Antwort enthalten:
  
- [ResponseCode](responsecode.md)
    
- [E-Mail-Info](mailtips.md)
    
## <a name="see-also"></a>Siehe auch



[EWS-Operationen in Exchange](ews-operations-in-exchange.md)
  
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

