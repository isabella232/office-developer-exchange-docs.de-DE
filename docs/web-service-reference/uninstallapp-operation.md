---
title: UninstallApp-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 7707aa6a-381d-43f7-a454-54f6343ed127
description: Hier finden Sie Informationen zum EWS-Vorgang "UninstallApp".
ms.openlocfilehash: 8a301360b2b4c38d85e8c5be2e80c79378d0fd97
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59527146"
---
# <a name="uninstallapp-operation"></a>UninstallApp-Vorgang

Hier finden Sie Informationen zum **EWS-Vorgang "UninstallApp".** 
  
Der **UninstallApp-Vorgang** deinstalliert eine Mail-App für Outlook. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-uninstallapp-operation"></a>Verwenden des UninstallApp-Vorgangs

Der **UninstallApp-Vorgang** verwendet ein Argument in der Anforderung, das die zu deinstallierende Mail-App identifiziert. 
  
### <a name="uninstallapp-operation-soap-headers"></a>SOAP-Header des UninstallApp-Vorgangs

Der **UninstallApp-Vorgang** kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Dieser Header gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Dieser Header gilt für eine Antwort.  <br/> |
   
## <a name="uninstallapp-operation-request-example-uninstall-a-mail-app-in-a-mailbox"></a>UninstallApp-Vorgangsanforderungsbeispiel: Deinstallieren einer Mail-App in einem Postfach

Das folgende Beispiel einer **UninstallApp-Vorgangsanforderung** zeigt, wie eine Mail-App mithilfe des App-Bezeichners deinstalliert wird. Der App-Bezeichner befindet sich im App-Manifest, das vom [GetAppManifests-Vorgang](getappmanifests-operation.md)zurückgegeben wird.
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:UninstallApp>
         <m:ID>1C50226D-04B5-4AB2-9FCD-42E236B59E4B</m:ID>
      </m:UninstallApp>
   </soap:Body>
</soap:Envelope>
```

Der SOAP-Anforderungstext enthält die folgenden Elemente:
  
- [UninstallApp](uninstallapp.md)
    
- [ID (Zeichenfolge)](id-string.md)
    
## <a name="successful-uninstallapp-operation-response"></a>Erfolgreiche UninstallApp-Vorgangsantwort

Das folgende Beispiel zeigt eine  erfolgreiche Antwort auf eine UninstallApp-Vorgangsanforderung zum Deinstallieren einer Mail-App. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <UninstallAppResponse ResponseClass="Success" 
                            xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </UninstallAppResponse>
   </s:Body>
</s:Envelope>
```

Der SOAP-Antworttext enthält die folgenden Elemente:
  
- [UninstallAppResponse](uninstallappresponse.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="uninstallapp-operation-error-response"></a>Fehlerantwort beim UninstallApp-Vorgang

Das folgende Beispiel zeigt eine  Fehlerantwort auf eine UninstallApp-Vorgangsanforderung. Dies ist eine Antwort auf eine Anforderung zum Deinstallieren einer Mail-App, die bereits deinstalliert wurde. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <UninstallAppResponse ResponseClass="Error" 
                            xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Extension ID 1c50226d-04b5-4ab2-9fcd-42e236b59e4b can't be found.</MessageText>
         <ResponseCode>ErrorInternalServerError</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </UninstallAppResponse>
   </s:Body>
</s:Envelope>
```

Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:
  
- [UninstallAppResponse](uninstallappresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
Weitere Fehlercodes, die für EWS generisch und für diesen Vorgang spezifisch sind, finden Sie unter [ResponseCode](responsecode.md).
  
## <a name="see-also"></a>Siehe auch

- [EWS-Operationen in Exchange](ews-operations-in-exchange.md)
    
- [InstallApp-Vorgang](installapp-operation.md)
    
- [DisableApp-Vorgang](disableapp-operation.md)
    
- [GetAppManifests](getappmanifests.md)
    
- [GetAppMarketplaceUrl-Vorgang](getappmarketplaceurl-operation.md)
    

