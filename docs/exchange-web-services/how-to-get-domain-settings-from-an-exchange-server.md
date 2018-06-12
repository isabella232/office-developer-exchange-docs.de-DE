---
title: Abrufen von domäneneinstellungen aus einem Exchange-server
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2f9acb81-5135-4f72-94e8-65c235d725e6
description: Erfahren Sie, wie Sie Domäneneinstellungen von einem Exchange-Server mithilfe des AutoErmittlungsdiensts abrufen.
ms.openlocfilehash: 0dd990cc82762936e7827115685ce0178eafb5ae
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756896"
---
# <a name="get-domain-settings-from-an-exchange-server"></a>Abrufen von domäneneinstellungen aus einem Exchange-server

Erfahren Sie, wie Sie Domäneneinstellungen von einem Exchange-Server mithilfe des AutoErmittlungsdiensts abrufen.
  
Sie können Konfigurationsinformationen für eine E-Mail-Domäne mithilfe des AutoErmittlungsdiensts abrufen. Der AutoErmittlungsdienst stellt Ihrer Anwendung einen Prozess für die Herstellung einer Verbindung mit dem richtigen Dienstendpunkt für eine bestimmte Domäne bereit.
  
Sie können eine der folgenden Entwicklungstechnologien verwenden, um auf den AutoErmittlungsdienst zuzugreifen:
  
- Die verwaltete API der Exchange-Webdienste (Exchange Web Services, EWS)
    
- EWS
    
    Bei Verwendung von EWS können Sie die folgenden Methoden zum Abrufen von Benutzereinstellungen verwenden:
    
  - Den SOAP-basierten AutoErmittlungsdienst
    
  - Den XML-AutoErmittlungsdienst (POX)
    
  - Einen automatisch vom SOAP- oder XML-AutoErmittlungdienst generierten Proxy
    
    Weitere Informationen zu diesen Methoden finden Sie unter [AutoErmittlung für Exchange](autodiscover-for-exchange.md).
    
Die verwaltete EWS-API stellt eine objektbasierte Schnittstelle für das Abrufen von Benutzereinstellungen bereit. Wenn die Clientanwendung verwalteten Code verwendet, wird empfohlen, die verwaltete EWS-API zu verwenden. Die verwaltete EWS-API-Schnittstelle ist besser für ein einfaches Objektmodell optimiert als der typische automatisch generierte Webdienstproxy. 
  
Bei Verwendung von EWS empfehlen wir die Verwendung des SOAP-AutoErmittlungsdiensts, da dieser eine umfassendere Sammlung von Funktionen als der POX-AutoErmittlungsdienst unterstützt.
  
Der AutoErmittlungsdienst gibt nur die angeforderten Konfigurationseinstellungen zurück. Die folgende Tabelle enthält die Domänenkonfigurationseinstellungen, die der AutoErmittlungsdienst zurückgeben kann.
  
**Tabelle 1: Domänenkonfigurationseinstellungen**

|**Konfigurationseinstellung**|**Beschreibung**|
|:-----|:-----|
|ExternalEwsUrl  <br/> |Die externe URL für EWS  <br/> |
|ExternalEwsVersion  <br/> |Die Version des Exchange-Servers, auf dem die EWS-URL gehostet wird  <br/> |
   
## <a name="prerequisites-for-getting-domain-settings"></a>Voraussetzungen für das Abrufen von Domäneneinstellungen
<a name="bk_Prereq"> </a>

Bevor Sie eine Anwendung erstellen, die eine Verbindung mit dem AutoErmittlungsdienst zum Abrufen von Domäneneinstellungen herstellt, stellen Sie sicher, dass Sie auf Folgendes zugreifen können:
  
- Exchange Online, Exchange Online als Teil von Office 365 oder einen Server mit einer Version von Exchange ab Exchange 2007. Bei Verwendung des SOAP-basierten EWS-AutoErmittlungsdiensts einen Server mit einer Version von Exchange ab Exchange 2010.
    
- Einen Exchange-Server, der Verbindungen von Ihrer Clientanwendung akzeptiert. Informationen zum Konfigurieren des Exchange-Servers finden Sie unter [Steuern des Clientanwendungszugriffs auf EWS in Exchange](controlling-client-application-access-to-ews-in-exchange.md).
    
- Ein Konto, das berechtigt ist, EWS zu verwenden. Informationen zum Konfigurieren eines Kontos finden Sie unter [Steuern des Clientanwendungszugriffs auf EWS in Exchange](controlling-client-application-access-to-ews-in-exchange.md).
    
> [!NOTE]
> [!HINWEIS] Wenn Sie die verwaltete EWS-API verwenden, müssen Sie in einigen Fällen einen Zertifikatüberprüfungsrückruf bereitstellen. Auch bei einigen generierten Proxybibliotheken, wie den von Visual Studio erstellten, benötigen Sie möglicherweise einen Zertifikatüberprüfungsrückruf. Weitere Informationen finden Sie unter [Validate ein Serverzertifikat für die EWS Managed API](how-to-validate-a-server-certificate-for-the-ews-managed-api.md). 
  
### <a name="core-concepts-for-getting-domain-settings"></a>Kernkonzepte für das Abrufen von Domäneneinstellungen
<a name="bk_Core"> </a>

Bevor Sie den AutoErmittlungsdienst zum Abrufen von Domäneneinstellungen verwenden, sollten Sie sich mit den Konzepten in der folgenden Tabelle vertraut machen.
  
|**Konzept**|**Beschreibung**|
|:-----|:-----|
|[AutoErmittlung für Exchange](autodiscover-for-exchange.md) <br/> |Bietet eine Übersicht über die Funktionsweise des AutoErmittlungsdiensts.  <br/> |
|[Mithilfe von AutoErmittlung Verbindungspunkte suchen](how-to-use-autodiscover-to-find-connection-points.md) <br/> |Beschreibt den vom AutoErmittlungsdienst verwendeten Prozess zum Umleiten Ihrer Clientanwendung an den richtigen Dienstendpunkt.  <br/> |
   
Wenn Sie die verwaltete EWS-API benutzen, verwenden Sie die Klasse [Microsoft.Exchange.WebServices.Data.ExchangeService](http://msdn.microsoft.com/en-us/library/exchange/dd635811%28v=exchg.80%29.aspx) im Namespace [Microsoft.Exchange.WebServices.Data](http://msdn.microsoft.com/en-us/library/exchange/dd633907%28v=exchg.80%29.aspx), um Ihre Verbindungen mit EWS zu verwalten. In den Codebeispielen in diesem Abschnitt wird davon ausgegangen, dass Sie in Ihrem Code auf die folgenden Namespaces verweisten: 
  
- **System.Net**
    
- **Microsoft.Exchange.WebServices.Data.ExchangeService**
    
## <a name="get-domain-settings-by-using-the-ews-managed-api"></a>Abrufen von Domäneneinstellungen mithilfe der verwalteten EWS-API
<a name="bk_Managed"> </a>

Wenn Sie die verwaltete EWS-API benutzen, können Sie die Methode [Microsoft.Exchange.WebServices.Data.AutodiscoverSettings.GetUserSettings](http://msdn.microsoft.com/en-us/library/exchange/microsoft.exchange.webservices.autodiscover.autodiscoverservice.getusersettings%28v=exchg.80%29.aspx) des Objekts [Microsoft.Exchange.WebServices.Data.AutodiscoverService](http://msdn.microsoft.com/en-us/library/exchange/dd634321%28v=exchg.80%29.aspx) verwenden, um die Anforderung zu generieren, mit der Konfigurationsinformationen für eine Domäne abgerufen werden, wie im folgenden Beispiel gezeigt. In diesem Beispiel werden nur einige der möglichen Domäneneinstellungen abgerufen und nur die abgerufenen Einstellungen vom Server zurückgegeben. 
  
```cs
AutodiscoverService autodiscoverService = new AutodiscoverService("domain.contoso.com");
autodiscoverService.Credentials = new NetworkCredential("User1", "password", "domain.contoso.com");
// Submit a request and get the settings. The response contains only the
// settings that are requested, if they exist.
GetDomainSettingsResponse domainresponse = autodiscoverService.GetDomainSettings(
    "domain",
    ExchangeVersion.Exchang2013,
    DomainSettingName.ExternalEwsUrl,
    DomainSettingName.ExternalEwsVersion);
```

Sie können die zurückgegebene Sammlung analysieren, um auf die einzelnen Schlüssel-Wert-Paare zuzugreifen. Das folgende Beispiel zeigt, wie Sie die einzelnen zurückgegebenen Elemente analysieren und den Namen und Wert der einzelnen Schlüssel-Wert-Paare anzeigen.
  
```cs
// Display each retrieved value. The settings are part of a key/value pair.
foreach (KeyValuePair<DomainSettingName, Object> domainsetting in domainresponse.Settings)
{
    Console.WriteLine(domainsetting.Key.ToString() + ": " + domainsetting.Value.ToString());
}
```

Alternativ können Sie den Wert einer bestimmten Einstellung abrufen. Im folgenden Beispiel soll die Einstellung **ExternalEwsUrl** angezeigt werden. 
  
```cs
// Display a specific setting, such as ExternalEwsUrl.
Console.WriteLine(domainresponse.Settings[DomainSettingName.ExternalEwsUrl]);
```

## <a name="get-user-settings-by-using-ews-soap-autodiscover"></a>Abrufen von Benutzereinstellungen mithilfe der EWS-SOAP-AutoErmittlung
<a name="bk_SOAP"> </a>

Das folgende Beispiel zeigt eine SOAP-XML-Anforderung zum Abrufen beider Domäneneinstellungen vom AutoErmittlungsdienst.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>http://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetDomainSettings</wsa:Action>
    <wsa:To>https://autodiscover.exchange.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetDomainSettingsRequestMessage xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Domains>
          <a:Domain>domain</a:Domain>
        </a:Domains>
        <a:RequestedSettings>
          <a:Setting>ExternalEwsUrl</a:Setting>
          <a:Setting>ExternalEwsVersion</a:Setting>
        </a:RequestedSettings>
        <a:RequestedVersion>Exchange2013</a:RequestedVersion>
      </a:Request>
    </a:GetDomainSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>
```

Das folgende Beispiel zeigt die XML-Antwort, die vom Server zurückgegeben wird, nachdem die Anforderung vom Client analysiert wurde.
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" 
        xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">http://schemas.microsoft.com/exchange/2010/
          Autodiscover/Autodiscover/GetDomainSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
          xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>15</h:MajorVersion>
      <h:MinorVersion>0</h:MinorVersion>
      <h:MajorBuildNumber>160</h:MajorBuildNumber>
      <h:MinorBuildNumber>4</h:MinorBuildNumber>
      <h:Version>Exchange2013</h:Version>
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
                <Value>https://failover.exchange.microsoft.com/ews/exchange.asmx</Value>
              </DomainSetting>
              <DomainSetting i:type="DomainStringSetting">
                <Name>ExternalEwsVersion</Name>
                <Value>15.00.0085.000</Value>
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

## <a name="next-steps"></a>Nächste Schritte
<a name="bk_Next"> </a>

Domäneneinstellungen stellen die grundlegenden Informationen bereit, die der Client für die Verbindung mit EWS benötigt. Sie können diese Informationen verwenden, um eine Verbindung mit EWS herzustellen, oder Sie können zusätzliche Konfigurationseinstellungen für ein E-Mail-Konto vom Server abrufen. Weitere Informationen finden Sie im folgenden Artikel:
  
- [Abrufen von benutzereinstellungen aus Exchange mithilfe der AutoErmittlung](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
## <a name="see-also"></a>Siehe auch


- [Einrichten Ihrer EWS-Anwendung](setting-up-your-ews-application.md)
    
- [AutoErmittlung Webdienstverweis für Exchange](http://msdn.microsoft.com/library/a01124a8-a8cf-4b80-8625-d7ee05690bca%28Office.15%29.aspx)
    
- [EWS-Referenz für Exchange](http://msdn.microsoft.com/library/2a873474-1bb2-4cb1-a556-40e8c4159f4a%28Office.15%29.aspx)
    

