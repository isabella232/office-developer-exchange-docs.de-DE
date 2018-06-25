---
title: SetUserOofSettings-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetUserOofSettings
api_type:
- schema
ms.assetid: 36277ef0-18ee-4b35-9e6e-8c321d8f5433
description: Die SetUserOofSettings-Webmethode legt eines Postfachbenutzers Out of Office (OOF)-Einstellungen und Nachricht fest.
ms.openlocfilehash: 51c2f9488f38a4adb0e291c11adc2ebfe3426f25
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831469"
---
# <a name="setuseroofsettings-operation"></a>SetUserOofSettings-Vorgang

Die **SetUserOofSettings** -Webmethode legt eines Postfachbenutzers Out of Office (OOF)-Einstellungen und Nachricht fest. 
  
## <a name="soap-headers"></a>SOAP-Header

Der Vorgang **SetUserOofSettings** können die SOAP-Header, die aufgeführt und in der folgenden Tabelle beschrieben. 
  
|**Header**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|Identitätswechsel  <br/> |["ExchangeImpersonation"](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.  <br/> |
   
## <a name="setuseroofsettings-request-example"></a>Anforderungsbeispiel SetUserOofSettings

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine Anforderung **SetUserOofSettings** legt eine OOF-Einstellung für 10 Tage fest. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <Name>User1</Name>
        <Address>user1@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <OofState>Enabled</OofState>
        <ExternalAudience>All</ExternalAudience>
        <Duration>
          <StartTime>2006-10-05T00:00:00</StartTime>
          <EndTime>2006-10-25T00:00:00</EndTime>
        </Duration>
        <InternalReply>
          <Message>I am out of office.  This is my internal reply.</Message>
        </InternalReply>
        <ExternalReply>
          <Message>I am out of office. This is my external reply.</Message>
        </ExternalReply>
      </UserOofSettings>
    </SetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [SetUserOofSettingsRequest](setuseroofsettingsrequest.md)
    
- [Postfach (Verfügbarkeit)](mailbox-availability.md)
    
- [Name (EmailAddress)](name-emailaddress.md)
    
- [Adresse (Zeichenfolge)](address-string.md)
    
- [RoutingType (EmailAddress)](routingtype-emailaddress.md)
    
- [' UserOofSettings '](useroofsettings.md)
    
- [OofState](oofstate.md)
    
- [ExternalAudience](externalaudience.md)
    
- [Dauer (' UserOofSettings ')](duration-useroofsettings.md)
    
- [StartTime](starttime.md)
    
- [EndTime](endtime.md)
    
- [InternalReply](internalreply.md)
    
- [Nachricht (Verfügbarkeit)](message-availability.md)
    
- [ExternalReply](externalreply.md)
    
## <a name="successful-setuseroofsettings-response-example"></a>Erfolgreiche SetUserOofSettings antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung **SetUserOofSettings** . 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" /> 
  </soap:Header>
  <soap:Body>
    <SetUserOofSettingsResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessage ResponseClass="Success">
        <ResponseCode>NoError</ResponseCode> 
      </ResponseMessage>
    </SetUserOofSettingsResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a>Elemente einer erfolgreichen Antwort

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SetUserOofSettingsResponse](setuseroofsettingsresponse.md)
    
- [ResponseMessage](responsemessage.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

