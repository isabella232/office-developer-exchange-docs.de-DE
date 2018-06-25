---
title: GetFederationInformation-Vorgang (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: c6666a42-a18f-4e4b-beb6-b25ff62cfcc5
description: Der Vorgang GetFederationInformation enthält Informationen zu den Verbund Status von der Organisation, beispielsweise die Ziel-URI verwendet werden, wenn Token an, die in der Übergangsphase sind diese Organisation und den anderen Domänen, die auch die Organisation hat Verbund.
ms.openlocfilehash: bf38b2f2b3db3e38b9b0157d1677efe4fc274e1b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758676"
---
# <a name="getfederationinformation-operation-soap"></a>GetFederationInformation-Vorgang (SOAP)

Der Vorgang **GetFederationInformation** enthält Informationen zu den Verbund Status der Organisation, beispielsweise das Ziel URI beim Anfordern Token zu verwendende sind in der Übergangsphase diese Organisation und die anderen Domänen, die der Organisation auch federated hat. 
  
Nur verbundorganisationen können freigeben, Kalender, Kontakte und Nachrichten an externe Benutzer.
  
## <a name="getfederationinformation-request-example"></a>Anforderungsbeispiel GetFederationInformation

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine Anforderung **GetFederationInformation** zeigt eine Anforderung für den Verbund-Informationen eines Benutzers. Der Client sendet diese Anforderung an den Server. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?> 
<soap:Envelope xmlns:exm="http://schemas.microsoft.com/exchange/services/2006/messages"
           xmlns:ext="http://schemas.microsoft.com/exchange/services/2006/types"
           xmlns:a="http://www.w3.org/2005/08/addressing"
           xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema"> 
    <soap:Header> 
        <a:MessageID>urn:uuid:6389558d-9e05-465e-ade9-aae14c4bcd10</a:MessageID> 
        <a:Action soap:mustUnderstand="1">http://schemas.microsoft.com/
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
            xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover"> 
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
    
## <a name="getfederationinformation-response-example"></a>GetFederationInformation antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die **GetFederationInformation** -Anforderung, die der Server an den Client sendet. 
  
### <a name="code"></a>Code

```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" 
xmlns:a="http://www.w3.org/2005/08/addressing"> 
    <s:Header> 
        <a:Action s:mustUnderstand="1">
            http://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetFederationInformationResponse
        </a:Action> 
        <a:RelatesTo>urn:uuid:6389558d-9e05-465e-ade9-aae14c4bcd10</a:RelatesTo> 
    </s:Header> 
    <s:Body> 
        <GetFederationInformationResponseMessage xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover"> 
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

