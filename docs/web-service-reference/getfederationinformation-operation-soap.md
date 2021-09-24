---
title: GetFederationInformation-Vorgang (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: c6666a42-a18f-4e4b-beb6-b25ff62cfcc5
description: Der GetFederationInformation-Vorgang stellt Informationen über den Verbundstatus der Organisation bereit, z. B. den Ziel-URI, der beim Anfordern von Token verwendet werden soll, die für diese Organisation bestimmt sind, und die anderen Domänen, die die Organisation ebenfalls verbunden hat.
ms.openlocfilehash: 915498440e4bc3d7262ed3a55350f7d3723d47d8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59529954"
---
# <a name="getfederationinformation-operation-soap"></a>GetFederationInformation-Vorgang (SOAP)

Der **GetFederationInformation-Vorgang** stellt Informationen über den Verbundstatus der Organisation bereit, z. B. den Ziel-URI, der beim Anfordern von Token verwendet werden soll, die für diese Organisation bestimmt sind, und die anderen Domänen, die die Organisation ebenfalls verbunden hat. 
  
Nur Verbundorganisationen können Kalender, Kontakte und Nachrichten für externe Benutzer freigeben.
  
## <a name="getfederationinformation-request-example"></a>GetFederationInformation-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer **GetFederationInformation-Anforderung** zeigt eine Anforderung für die Verbundinformationen eines Benutzers. Der Client sendet diese Anforderung an den Server. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?> 
<soap:Envelope xmlns:exm="https://schemas.microsoft.com/exchange/services/2006/messages"
           xmlns:ext="https://schemas.microsoft.com/exchange/services/2006/types"
           xmlns:a="http://www.w3.org/2005/08/addressing"
           xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema"> 
    <soap:Header> 
        <a:MessageID>urn:uuid:6389558d-9e05-465e-ade9-aae14c4bcd10</a:MessageID> 
        <a:Action soap:mustUnderstand="1">https://schemas.microsoft.com/
            exchange/2010/Autodiscover/Autodiscover/GetFederationInformation
        </a:Action> 
        <a:To soap:mustUnderstand="1">https://autodiscover.byfcxu-
            dom.extest.microsoft.com/autodiscover/autodiscover.svc</a:To> 
        <a:ReplyTo>
            <a:Address>http://www.w3.org/2005/08/addressing/anonymous</a:Address> 
        </a:ReplyTo> 
    </soap:Header> 
    <soap:Body> 
        <GetFederationInformationRequestMessage 
            xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover"> 
            <Request> 
                <Domain>contoso.com</Domain> 
            </Request> 
        </GetFederationInformationRequestMessage>
    </soap:Body> 
</soap:Envelope>
```

### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [GetFederationInformationRequestMessage (SOAP)](getfederationinformationrequestmessage-soap.md)
    
- [Anforderung (SOAP)](request-soap.md)
    
- [Domäne (SOAP)](domain-soap.md)
    
## <a name="getfederationinformation-response-example"></a>GetFederationInformation-Antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die **GetFederationInformation-Anforderung,** die der Server an den Client sendet. 
  
### <a name="code"></a>Code

```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" 
xmlns:a="http://www.w3.org/2005/08/addressing"> 
    <s:Header> 
        <a:Action s:mustUnderstand="1">
            https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetFederationInformationResponse
        </a:Action> 
        <a:RelatesTo>urn:uuid:6389558d-9e05-465e-ade9-aae14c4bcd10</a:RelatesTo> 
    </s:Header> 
    <s:Body> 
        <GetFederationInformationResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover"> 
            <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance"> 
                <ErrorCode>NoError</ErrorCode> 
                <ErrorMessage/> 
                <ApplicationUri>BYFCXU-DOM.EXTEST.MICROSOFT.COM</ApplicationUri> 
                <Domains> 
                    <Domain>contoso.com</Domain> 
                    <Domain>europe.contoso.com</Domain> 
                    <Domain>americas.contoso.com</Domain> 
                    <Domain>contosolive.com</Domain> 
                </Domains> 
            </Response> 
        </GetFederationInformationResponseMessage> 
    </s:Body> 
</s:Envelope>
```

### <a name="response-elements"></a>Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [GetFederationInformationResponseMessage (SOAP)](getfederationinformationresponsemessage-soap.md)
    
- [Antwort (SOAP)](response-soap.md)
    
- [ErrorCode (SOAP)](errorcode-soap.md)
    
- [ErrorMessage (SOAP)](errormessage-soap.md)
    
- [ApplicationUri (SOAP)](applicationuri-soap.md)
    
- [Domänen (SOAP)](domains-soap.md)
    
- [Domäne (SOAP)](domain-soap.md)
    
## <a name="see-also"></a>Siehe auch

- [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
- [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)

