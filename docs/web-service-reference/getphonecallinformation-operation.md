---
title: GetPhoneCallInformation-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetPhoneCallInformation
api_type:
- schema
ms.assetid: 418bd6ca-39d9-49a9-841e-7a71ede1fa51
description: Der Vorgang GetPhoneCallInformation zurückgegeben Informationen zu den angegebenen Telefonanruf.
ms.openlocfilehash: 8f98ca5dd304eadffc307fa47620b7db6401c782
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758778"
---
# <a name="getphonecallinformation-operation"></a>GetPhoneCallInformation-Vorgang

Der Vorgang **GetPhoneCallInformation** zurückgegeben Informationen zu den angegebenen Telefonanruf. 
  
## <a name="getphonecallinformation-request-example"></a>Anforderungsbeispiel GetPhoneCallInformation

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine Anforderung **GetPhoneCallInformation** veranschaulicht eine Anforderung zum Abrufen von Informationen zu einem bestimmten Anruf bilden. 
  
### <a name="code"></a>Code

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:GetPhoneCallInformation>
      <m:PhoneCallId Id="NDDY5uY29y9t"/>
    </m:GetPhoneCallInformation>
  </soap:Body>
</soap:Envelope>
```

## <a name="getphonecallinformation-response-example"></a>GetPhoneCallInformation antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung **GetPhoneCallInformation** . Die Antwort stellt einen Telefonanruf, der aktuell verbunden ist. 
  
### <a name="code"></a>Code

```xml
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="20" 
                         Version="Exchange2010" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetPhoneCallInformationResponse ResponseClass="Success" 
                                     xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <m:PhoneCallInformation xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
        <t:PhoneCallState xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">Connected</t:PhoneCallState>
        <t:ConnectionFailureCause xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">None</t:ConnectionFailureCause>
      </m:PhoneCallInformation>
    </GetPhoneCallInformationResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a>Siehe auch

- [EWS-Operationen in Exchange](ews-operations-in-exchange.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

