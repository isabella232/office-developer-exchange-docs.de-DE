---
title: UninstallApp-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7707aa6a-381d-43f7-a454-54f6343ed127
description: Hier finden Sie Informationen über die UninstallApp EWS Vorgang.
ms.openlocfilehash: 4f44224651993023336eef5540ec29b7f6a6e32e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839296"
---
# <a name="uninstallapp-operation"></a>UninstallApp-Vorgang

Hier finden Sie Informationen zum **UninstallApp** EWS-Vorgang. 
  
Der Vorgang **UninstallApp** deinstalliert eine Mail-app für Outlook. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-uninstallapp-operation"></a>Verwenden des UninstallApp-Vorgangs

Die **UninstallApp** Operation hat ein Argument in der Anforderung, die die Mail-app zu deinstallieren identifiziert. 
  
### <a name="uninstallapp-operation-soap-headers"></a>UninstallApp Vorgang SOAP-Header

Der Vorgang **UninstallApp** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Diese Kopfzeile gilt für eine Antwort.  <br/> |
   
## <a name="uninstallapp-operation-request-example-uninstall-a-mail-app-in-a-mailbox"></a>UninstallApp Vorgang-anforderungsbeispiel: Deinstallieren eine Mail-app in einem Postfach

Im folgenden Beispiel wird eine **UninstallApp** Operation anfordern zeigt, wie auf eine Deinstallation einer Mail-app mithilfe des app-Bezeichners. Im app-Manifest, das von der [GetAppManifests-Vorgang](getappmanifests-operation.md)zurückgegeben wird, kann die app-ID gefunden werden.
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

Die Anforderung SOAP-Text enthält die folgenden Elemente:
  
- [UninstallApp](uninstallapp.md)
    
- [ID (Zeichenfolge)](id-string.md)
    
## <a name="successful-uninstallapp-operation-response"></a>Erfolgreiche UninstallApp Vorgangsantwort

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung **UninstallApp** Vorgang, um eine Mail-app zu deinstallieren. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <UninstallAppResponse ResponseClass="Success" 
                            xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </UninstallAppResponse>
   </s:Body>
</s:Envelope>
```

Die Antwort SOAP-Text enthält die folgenden Elemente:
  
- [UninstallAppResponse](uninstallappresponse.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="uninstallapp-operation-error-response"></a>UninstallApp Vorgang Fehlerantwort

Das folgende Beispiel zeigt eine Fehlerantwort an eine **UninstallApp** Vorgang Anforderung. Dies ist eine Antwort auf eine Anforderung an eine Mail-app zu deinstallieren, die bereits deinstalliert wurde. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <UninstallAppResponse ResponseClass="Error" 
                            xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Extension ID 1c50226d-04b5-4ab2-9fcd-42e236b59e4b can't be found.</MessageText>
         <ResponseCode>ErrorInternalServerError</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </UninstallAppResponse>
   </s:Body>
</s:Envelope>
```

Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:
  
- [UninstallAppResponse](uninstallappresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
Zusätzliche Fehlercodes, die für EWS generisch und für diese Operation spezifisch sind, finden Sie unter [ResponseCode](responsecode.md).
  
## <a name="see-also"></a>Siehe auch

- [EWS-Operationen in Exchange](ews-operations-in-exchange.md)
    
- [InstallApp-Vorgang](installapp-operation.md)
    
- [DisableApp-Vorgang](disableapp-operation.md)
    
- [GetAppManifests](getappmanifests.md)
    
- [GetAppMarketplaceUrl-Vorgang](getappmarketplaceurl-operation.md)
    

