---
title: GetAppMarketplaceUrl-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2c016fc3-0e13-4624-9a5b-d3e84577a860
description: Hier finden Sie Informationen über die GetAppMarketplaceUrl EWS Vorgang.
ms.openlocfilehash: 616e7f571ba5283a773e51d611cd18bb37b5bc8b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758573"
---
# <a name="getappmarketplaceurl-operation"></a>GetAppMarketplaceUrl-Vorgang

Hier finden Sie Informationen zum **GetAppMarketplaceUrl** EWS-Vorgang. 
  
Der Vorgang **GetAppMarketplaceUrl** Ruft die URL für den app-Marketplace, den ein Client besuchen dürfen, zum Erwerben von apps in einem Postfach zu installieren. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-getappmarketplaceurl-operation"></a>Verwenden des GetAppMarketplaceUrl-Vorgangs

Der Vorgang **GetAppMarketplaceUrl** ist keine Argumente So fordern Sie die URL für den Marketplace an, von dem ein Client-apps installieren kann. Die Antwort enthält eine URL zu den app-Marketplace. 
  
### <a name="getappmarketplaceurl-operation-soap-headers"></a>GetAppMarketplaceUrl Vorgang SOAP-Header

Der Vorgang **GetAppMarketplaceUrl** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Diese Kopfzeile gilt für eine Antwort.  <br/> |
   
## <a name="getappmarketplaceurl-operation-request-example-get-the-app-marketplace-url-for-a-mailbox"></a>GetAppMarketplaceUrl Vorgang-anforderungsbeispiel: Abrufen die app Marketplace-URL für ein Postfach

Im folgenden Beispiel wird eine **GetAppMarketplaceUrl** Vorgang Anforderung veranschaulicht die app Marketplace-URL für ein Postfach abzurufen. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

Die Anforderung SOAP-Text enthält die folgenden Elemente:
  
- [GetAppMarketplaceUrl](getappmarketplaceurl.md)
    
- [ApiVersionSupported](apiversionsupported.md)
    
- [SchemaVersionSupported](schemaversionsupported.md)
    
## <a name="successful-getappmarketplaceurl-operation-response"></a>Erfolgreiche GetAppMarketplaceUrl Vorgangsantwort

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung **GetAppMarketplaceUrl** Vorgang, um die app Marketplace-URL für ein Postfach abzurufen. 
  
> [!NOTE]
> Die URL der app-Marketplace wurde geändert, um die Lesbarkeit zu erhalten. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="918" 
                           MinorBuildNumber="7" 
                           Version="V2_10" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetAppMarketplaceUrlResponse ResponseClass="Success" 
                                    xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <AppMarketplaceUrl>http://marketplace.contoso.com</AppMarketplaceUrl>
      </GetAppMarketplaceUrlResponse>
   </s:Body>
</s:Envelope>

```

Die Antwort SOAP-Text enthält die folgenden Elemente:
  
- [GetAppMarketplaceUrlResponse](getappmarketplaceurlresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [AppMarketplaceUrl](appmarketplaceurl.md)
    
## <a name="getappmarketplaceurl-operation-error-response"></a>GetAppMarketPlaceUrl Vorgang Fehlerantwort

Fehler, die für diesen Vorgang zurückgegeben werden entweder im Zusammenhang mit der eine falsche Konfiguration oder generische EWS-Fehler sind. Fehlercodes, die für EWS generisch und für diese Operation spezifisch sind, finden Sie unter [ResponseCode](responsecode.md). 
  
Das folgende Beispiel zeigt eine Fehlerantwort an, die zurückgegeben wird, wenn externe Exchange Steuerelement Systemsteuerung nicht konfiguriert ist.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="918" 
                           MinorBuildNumber="7" 
                           Version="V2_10" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetAppMarketplaceUrlResponse ResponseClass="Error" 
                                    xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Cannot get external ECP URL. This might happen if external ECP URL isn't configured.</MessageText>
         <ResponseCode>ErrorCannotGetExternalEcpUrl</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetAppMarketplaceUrlResponse>
   </s:Body>
</s:Envelope>
```

Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:
  
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
    

