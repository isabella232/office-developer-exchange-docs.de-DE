---
title: GetDomainSettings-Vorgang (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a6f4a53d-d7f6-4ad1-8afb-78745c500eaa
description: Der Vorgang GetDomainSettings werden die angegebenen Einstellungen der Domäne für den Benutzer abgerufen. AutoErmittlung zurückgegeben, die Domänen, die ermittelt werden und die angeforderten Einstellungen der Domänen.
ms.openlocfilehash: 09b1d610cd415d2d9d7d0098354521ece86f5184
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758649"
---
# <a name="getdomainsettings-operation-soap"></a>GetDomainSettings-Vorgang (SOAP)

Der Vorgang **GetDomainSettings** werden die angegebenen Einstellungen der Domäne für den Benutzer abgerufen. AutoErmittlung zurückgegeben, die Domänen, die ermittelt werden und die angeforderten Einstellungen der Domänen. 
  
## <a name="getdomainsettings-request-example"></a>Anforderungsbeispiel GetDomainSettings

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine Anforderung **GetDomainSettings** zeigt eine Anforderung für einen Benutzer **"externalewsurl"** domäneneinstellungen. Der Client sendet diese Anforderung an den Server. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?> 
<soap:Envelope xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover"
               xmlns:wsa="http://www.w3.org/2005/08/addressing"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
    <soap:Header> 
        <a:RequestedServerVersion>Exchange2010</a:RequestedServerVersion>
        <wsa:Action>http://schemas.microsoft.com/exchange/2010/
            Autodiscover/Autodiscover/GetDomainSettings</wsa:Action>
        <wsa:To>
            https://autodiscover.exchange.microsoft.com/autodiscover/autodiscover.svc
        </wsa:To>
    </soap:Header> 
    <soap:Body> 
        <a:GetDomainSettingsRequestMessage xmlns:a="http://schemas.microsoft.com
            /exchange/2010/Autodiscover"> 
            <a:Request> 
                <a:Domains> 
                    <a:Domain>contoso.com<</a:Domain> 
                </a:Domains> 
                <a:RequestedSettings> 
                    <a:Setting>ExternalEwsUrl</a:Setting> 
                </a:RequestedSettings> 
            </a:Request> 
        </a:GetDomainSettingsRequestMessage> 
    </soap:Body> 
</soap:Envelope>
```

### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [GetDomainSettingsRequestMessage (SOAP)](getdomainsettingsrequestmessage-soap.md)
    
- [Anforderung (SOAP)](request-soap.md)
    
- [Domänen (SOAP)](domains-soap.md)
    
- [Domäne (SOAP)](domain-soap.md)
    
- [RequestedSettings (SOAP)](requestedsettings-soap.md)
    
- [Einstellung (SOAP)](setting-soap.md)
    
## <a name="getdomainsettings-response-example"></a>GetDomainSettings antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die **GetDomainSettings** -Anforderung, die der Server an den Client sendet. 
  
### <a name="code"></a>Code

```XML
//www.w3.org/2005/08/addressing"> 
    <s:Header> 
        <a:Action s:mustUnderstand="1">http://schemas.microsoft.com/exchange/2010/ 
            Autodiscover/Autodiscover/GetDomainSettingsResponse
        </a:Action> 
        <h:ServerVersionInfo xmlns:h="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
            xmlns:i="http://www.w3.org/2001/XMLSchema-instance"> 
        <h:MajorVersion>14</h:MajorVersion> 
        <h:MinorVersion>0</h:MinorVersion> 
        <h:MajorBuildNumber>639</h:MajorBuildNumber> 
        <h:MinorBuildNumber>20</h:MinorBuildNumber> 
        <h:Version>Exchange2010</h:Version> 
        </h:ServerVersionInfo>
    </s:Header> 
    <s:Body> 
        <GetDomainSettingsResponseMessage xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover"> 
            <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance"> 
                <ErrorCode>NoError</ErrorCode> 
                <ErrorMessage /> 
                <DomainResponses> 
                    <DomainResponse> 
                        <ErrorCode>NoError</ErrorCode> 
                        <ErrorMessage>No error.</ErrorMessage> 
                        <DomainSettingErrors /> 
                        <DomainSettings> 
                            <DomainSetting i:type="DomainStringSetting"> 
                                <Name>ExternalEwsUrl</Name> 
                                <Value>https://emea.mail.microsoft.com/EWS/Exchange.asmx</Value> 
                            </DomainSetting> 
                        </DomainSettings> 
                        <RedirectTarget i:nil="true" /> 
                    </DomainResponse> 
                </DomainResponses> 
            </Response> 
        </GetDomainSettingsResponseMessage> 
    </s:Body> 
</s:Envelope>
```

### <a name="response-elements"></a>Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [GetDomainSettingsResponseMessage (SOAP)](getdomainsettingsresponsemessage-soap.md)
    
- [Antwort (SOAP)](response-soap.md)
    
- [ErrorCode (SOAP)](errorcode-soap.md)
    
- [ErrorMessage (SOAP)](errormessage-soap.md)
    
- [DomainResponses (SOAP)](domainresponses-soap.md)
    
- [DomainResponse (SOAP)](domainresponse-soap.md)
    
- [DomainSettingErrors (SOAP)](domainsettingerrors-soap.md)
    
- [DomainSettings (SOAP)](domainsettings-soap.md)
    
- [DomainSetting (SOAP)](domainsetting-soap.md)
    
- [Name (SOAP)](name-soap.md)
    
- [Wert (SOAP)](value-soap.md)
    
- [RedirectTarget (SOAP)](redirecttarget-soap.md)
    
## <a name="see-also"></a>Siehe auch



[GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
  
[GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)

