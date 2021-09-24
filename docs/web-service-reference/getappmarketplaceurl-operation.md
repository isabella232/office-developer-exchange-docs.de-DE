---
title: GetAppMarketplaceUrl-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 2c016fc3-0e13-4624-9a5b-d3e84577a860
description: Hier finden Sie Informationen zum EWS-Vorgang "GetAppMarketplaceUrl".
ms.openlocfilehash: f9dd41a43b92910ec596b95a0ce1e99a239ba01e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59530090"
---
# <a name="getappmarketplaceurl-operation"></a>GetAppMarketplaceUrl-Vorgang

Hier finden Sie Informationen zum EWS-Vorgang **"GetAppMarketplaceUrl".** 
  
Der **GetAppMarketplaceUrl-Vorgang** ruft die URL für den App-Marketplace ab, den ein Client besuchen kann, um Apps zum Installieren in einem Postfach zu erwerben. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-getappmarketplaceurl-operation"></a>Verwenden des GetAppMarketplaceUrl-Vorgangs

Der **GetAppMarketplaceUrl-Vorgang** verwendet keine Argumente, um die URL für den Marketplace anzufordern, von dem aus ein Client Apps installieren kann. Die Antwort enthält eine URL zum App-Marketplace. 
  
### <a name="getappmarketplaceurl-operation-soap-headers"></a>SOAP-Header des GetAppMarketplaceUrl-Vorgangs

Der **GetAppMarketplaceUrl-Vorgang** kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Dieser Header gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Dieser Header gilt für eine Antwort.  <br/> |
   
## <a name="getappmarketplaceurl-operation-request-example-get-the-app-marketplace-url-for-a-mailbox"></a>GetAppMarketplaceUrl-Vorgangsanforderungsbeispiel: Abrufen der App Marketplace-URL für ein Postfach

Das folgende Beispiel einer **GetAppMarketplaceUrl-Vorgangsanforderung** zeigt, wie Sie die App Marketplace-URL für ein Postfach abrufen. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013_SP1" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
      <t:TimeZoneContext>
         <t:TimeZoneDefinition Id="GMT Standard Time"/>
      </t:TimeZoneContext>
   </soap:Header>
   <soap:Body >
      <m:GetAppMarketplaceUrl>
        <m:ApiVersionSupported>1.0</m:ApiVersionSupported>
        <m:SchemaVersionSupported>1.0</m:SchemaVersionSupported>
      </m:GetAppMarketplaceUrl>
   </soap:Body>
</soap:Envelope>

```

Der SOAP-Anforderungstext enthält die folgenden Elemente:
  
- [GetAppMarketplaceUrl](getappmarketplaceurl.md)
    
- [ApiVersionSupported](apiversionsupported.md)
    
- [SchemaVersionSupported](schemaversionsupported.md)
    
## <a name="successful-getappmarketplaceurl-operation-response"></a>Erfolgreiche GetAppMarketplaceUrl-Vorgangsantwort

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetAppMarketplaceUrl-Vorgangsanforderung** zum Abrufen der App Marketplace-URL für ein Postfach. 
  
> [!NOTE]
> Die URL des App-Marketplace wurde geändert, um die Lesbarkeit zu gewährleisten. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="918" 
                           MinorBuildNumber="7" 
                           Version="V2_10" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetAppMarketplaceUrlResponse ResponseClass="Success" 
                                    xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <AppMarketplaceUrl>http://marketplace.contoso.com</AppMarketplaceUrl>
      </GetAppMarketplaceUrlResponse>
   </s:Body>
</s:Envelope>

```

Der SOAP-Antworttext enthält die folgenden Elemente:
  
- [GetAppMarketplaceUrlResponse](getappmarketplaceurlresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [AppMarketplaceUrl](appmarketplaceurl.md)
    
## <a name="getappmarketplaceurl-operation-error-response"></a>GetAppMarketPlaceUrl-Vorgangsfehlerantwort

Fehler, die für diesen Vorgang zurückgegeben werden, beziehen sich entweder auf eine falsche Dienstkonfiguration oder sind generische EWS-Fehler. Fehlercodes, die für EWS generisch und für diesen Vorgang spezifisch sind, finden Sie unter [ResponseCode](responsecode.md). 
  
Das folgende Beispiel zeigt eine Fehlerantwort, die zurückgegeben wird, wenn die externe Exchange Systemsteuerung (ECP) nicht konfiguriert ist.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="918" 
                           MinorBuildNumber="7" 
                           Version="V2_10" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetAppMarketplaceUrlResponse ResponseClass="Error" 
                                    xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Cannot get external ECP URL. This might happen if external ECP URL isn't configured.</MessageText>
         <ResponseCode>ErrorCannotGetExternalEcpUrl</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetAppMarketplaceUrlResponse>
   </s:Body>
</s:Envelope>
```

Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:
  
- [GetAppMarketplaceUrlResponse](getappmarketplaceurlresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Siehe auch

- [EWS-Operationen in Exchange](ews-operations-in-exchange.md)
    
- [DisableApp-Vorgang](disableapp-operation.md)
    
- [InstallApp-Vorgang](installapp-operation.md)
    
- [UninstallApp-Vorgang](uninstallapp-operation.md)
    
- [GetAppManifests-Vorgang](getappmanifests-operation.md)
    

