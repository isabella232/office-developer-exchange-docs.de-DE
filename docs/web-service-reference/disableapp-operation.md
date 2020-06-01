---
title: DisableApp-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 211731a3-2470-49af-bda3-1ddfc15a8e46
description: Hier finden Sie Informationen zum DisableApp-EWS-Vorgang.
ms.openlocfilehash: 8e1f3a257a70c042a01ed70da97cfa0573a2d454
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462066"
---
# <a name="disableapp-operation"></a>DisableApp-Vorgang

Hier finden Sie Informationen zum **DisableApp** -EWS-Vorgang. 
  
Der **DisableApp** -Vorgang deaktiviert eine Mail-App für Outlook. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-disableapp-operation"></a>Verwenden des DisableApp-Vorgangs

Der **DisableApp** -Vorgang benötigt zwei Argumente in der Anforderung, die die zu deaktivierende Mail-APP und den Grund für die Deaktivierung identifizieren. 
  
### <a name="disableapp-operation-soap-headers"></a>SOAP-Header des DisableApp-Vorgangs

Der **DisableApp** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Diese Kopfzeile gilt für eine Antwort.  <br/> |
   
## <a name="disableapp-operation-request-example-disable-a-mail-app-installed-in-a-mailbox"></a>DisableApp-Vorgangs Anforderungs Beispiel: Deaktivieren einer in einem Postfach installierten Mail-App

Im folgenden Beispiel einer **DisableApp** -Vorgangsanforderung wird gezeigt, wie eine Mail-App deaktiviert wird. Der APP-Bezeichner befindet sich im App-Manifest, das in einer [GetAppManifests-Vorgangs](getappmanifests-operation.md) Antwort zurückgegeben wird. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
      <t:TimeZoneContext>
         <t:TimeZoneDefinition Id="GMT Standard Time"/>
      </t:TimeZoneContext>
   </soap:Header>
   <soap:Body >
      <m:DisableApp>
         <m:ID>1C50226D-04B5-4AB2-9FCD-42E236B59E4B</m:ID>
         <m:DisableReason>NoReason</m:DisableReason>
      </m:DisableApp>
   </soap:Body>
</soap:Envelope>
```

Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:
  
- [DisableApp](disableapp.md)
    
- [ID (Zeichenfolge)](id-string.md)
    
- [DisableReason](disablereason.md)
    
## <a name="successful-disableapp-operation-response"></a>Erfolgreiche Reaktion des DisableApp-Vorgangs

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **DisableApp** -Vorgangsanforderung zum Deaktivieren einer Mail-app. 
  
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
      <DisableAppResponse ResponseClass="Success" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </DisableAppResponse>
   </s:Body>
</s:Envelope>
```

Der SOAP-Antworttext Körper enthält die folgenden Elemente:
  
- [DisableAppResponse](disableappresponse.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="disableapp-operation-error-response"></a>Fehlerantwort des DisableApp-Vorgangs

Das folgende Beispiel zeigt eine Fehlerantwort auf eine **DisableApp** -Vorgangsanforderung. Dies ist eine Antwort auf eine Anforderung zum Deaktivieren einer Mail-APP, die nicht in einem Postfach installiert ist. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="556" MinorBuildNumber="14" Version="Exchange2013" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <DisableAppResponse ResponseClass="Error" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Extension ID 1C50226D-04B5-4AB2-9FCD-42E236B59E4A can't be found.</MessageText>
         <ResponseCode>ErrorExtensionNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </DisableAppResponse>
   </s:Body>
</s:Envelope>
```

Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:
  
- [DisableAppResponse](disableappresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
Weitere Fehlercodes, die für EWS allgemein und spezifisch für diesen Vorgang sind, finden Sie unter [Response Code](responsecode.md).
  
## <a name="see-also"></a>Siehe auch

- [EWS-Operationen in Exchange](ews-operations-in-exchange.md)   
- [InstallApp-Vorgang](installapp-operation.md)   
- [UninstallApp-Vorgang](uninstallapp-operation.md)   
- [GetAppManifests](getappmanifests.md)   
- [GetAppMarketplaceUrl-Vorgang](getappmarketplaceurl-operation.md)   
- [Outlook-Add-Ins](https://msdn.microsoft.com/library/71e64bc9-e347-4f5d-8948-0a47b5dd93e6%28Office.15%29.aspx)
    

