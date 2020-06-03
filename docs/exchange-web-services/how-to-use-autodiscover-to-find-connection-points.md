---
title: Verwenden der AutoErmittlung für die Suche nach Verbindungspunkten
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 03896542-549b-4c45-973c-98f9025ea26c
description: Erfahren Sie, wie Sie den AutoErmittlungsdienst verwenden, um Ihre Clientanwendung an den richtigen Exchange-Server weiterzuleiten.
localization_priority: Priority
ms.openlocfilehash: c1895fa0d2cce489467a726614e9457052624ef6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527593"
---
# <a name="use-autodiscover-to-find-connection-points"></a>Verwenden der AutoErmittlung für die Suche nach Verbindungspunkten

Erfahren Sie, wie Sie den AutoErmittlungsdienst verwenden, um Ihre Clientanwendung an den richtigen Exchange-Server weiterzuleiten.
  
Der Exchange-AutoErmittlungsdienst stellt Ihrer Clientanwendung Konfigurationseinstellungen für e-Mail-Konten zur Verfügung, die auf Exchange Online gehostet werden, Exchange Online im Rahmen von Office 365 oder einem Exchange-Server, auf dem eine Exchange-Version mit Exchange 2013 ausgeführt wird. Der AutoErmittlungsdienst ist ein Webdienst, der Konfigurationseinstellungen bereitstellt. Der AutoErmittlungsdienst ist ein Webdienst, der Exchange Server-Konfigurationsinformationen für Ihre Clientanwendung bereitstellt. Client Anwendungen verwenden AutoErmittlung, um den Endpunkt des AutoErmittlungsdiensts für ein bestimmtes Postfach zu ermitteln. In diesem Artikel wird erläutert, wie Sie die Antworten von einem Exchange-Server zum Ermitteln des richtigen Endpunkts befolgten. 
  
Informationen zum Abrufen von Konfigurationseinstellungen für e-Mail-Adressen finden Sie unter [Abrufen von Benutzereinstellungen von Exchange mithilfe der AutoErmittlung](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) und [Abrufen von Domäneneinstellungen von einem Exchange-Server](how-to-get-domain-settings-from-an-exchange-server.md).
  
> [!NOTE]
> Der Vorgang zum Suchen des richtigen Endpunkts ist Teil der Anforderung für Benutzer-oder Domäneneinstellungen. Der AutoErmittlungsdienst verwendet eine Reihe von Umleitungsantworten, um die Clientanwendung an den richtigen Endpunkt für eine e-Mail-Adresse zu senden. 
  
Sie können eine der folgenden Exchange-Entwicklungstechnologien für den Zugriff auf den AutoErmittlungsdienst verwenden:

- Die verwaltete API der Exchange-Webdienste (Exchange Web Services, EWS)
    
- EWS
    
Bei Verwendung von EWS können Sie die folgenden Methoden zum Abrufen von Benutzereinstellungen verwenden:
    
- Den SOAP-basierten AutoErmittlungsdienst
    
- Den XML-AutoErmittlungsdienst (POX)
    
- Einen automatisch vom SOAP- oder XML-AutoErmittlungdienst generierten Proxy
    
Weitere Informationen zu diesen Methoden finden Sie unter [AutoErmittlung für Exchange](autodiscover-for-exchange.md).

Weitere Informationen zu diesen Exchange-Entwicklungstechnologien finden Sie unter [Explore the verwaltete EWS-API, EWS, and Webservices in Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md). 

Die verwaltete EWS-API stellt eine objektbasierte Schnittstelle für das Abrufen von Benutzereinstellungen bereit. Wenn die Clientanwendung verwalteten Code verwendet, wird empfohlen, die verwaltete EWS-API zu verwenden. Die verwaltete EWS-API-Schnittstelle ist besser für ein einfaches Objektmodell optimiert als der typische automatisch generierte Webdienstproxy. 
  
Bei Verwendung von EWS empfehlen wir die Verwendung des SOAP-AutoErmittlungsdiensts, da dieser eine umfassendere Sammlung von Funktionen als der POX-AutoErmittlungsdienst unterstützt.
  
## <a name="prerequisites-for-finding-an-endpoint"></a>Voraussetzungen für die Suche nach einem Endpunkt
<a name="bk_Prereq"> </a>

Bevor Sie eine Clientanwendung erstellen können, die den AutoErmittlungsdienst verwendet, benötigen Sie Zugriff auf Folgendes:
  
- Exchange Online oder ein Server, auf dem eine Version von Exchange mit Exchange 2007 SP1 gestartet wird. Wenn Sie den SOAP-basierten AutoErmittlungsdienst verwenden: Exchange Online oder eine Version von Exchange ab Exchange 2010
    
- Einen Exchange-Server, der Verbindungen von Ihrer Clientanwendung akzeptiert. Informationen zum Konfigurieren des Exchange-Servers finden Sie unter [Steuern des Clientanwendungszugriffs auf EWS in Exchange](controlling-client-application-access-to-ews-in-exchange.md).
    
- Ein Konto, das berechtigt ist, EWS zu verwenden. Informationen zum Konfigurieren eines Kontos finden Sie unter [Steuern des Clientanwendungszugriffs auf EWS in Exchange](controlling-client-application-access-to-ews-in-exchange.md).
    
> [!NOTE]
> Wenn Sie die verwaltete EWS-API verwenden, müssen Sie in einigen Fällen einen Zertifikatüberprüfungsrückruf bereitstellen. Auch bei einigen generierten Proxybibliotheken, wie den von Visual Studio erstellten, benötigen Sie möglicherweise einen Zertifikatüberprüfungsrückruf. Weitere Informationen finden Sie unter [Überprüfen eines Serverzertifikats für die verwaltete EWS-API](how-to-validate-a-server-certificate-for-the-ews-managed-api.md). 
  
### <a name="core-concepts-for-finding-an-endpoint"></a>Kernkonzepte für die Suche nach einem Endpunkt
<a name="bk_Core"> </a>

Bevor Sie die AutoErmittlung zum Auffinden eines Endpunkts verwenden, sollten Sie mit den in der folgenden Tabelle aufgelisteten Konzepten vertraut sein.
  
|**Konzept**|**Beschreibung**|
|:-----|:-----|
|[AutoErmittlung für Exchange](autodiscover-for-exchange.md) <br/> |Bietet eine Übersicht über die Funktionsweise des AutoErmittlungsdiensts.  <br/> |
   
Wenn Sie die verwaltete EWS-API benutzen, verwenden Sie die Klasse [Microsoft.Exchange.WebServices.Data.ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) im Namespace [Microsoft.Exchange.WebServices.Data](https://msdn.microsoft.com/library/dd633907%28v=exchg.80%29.aspx), um Ihre Verbindungen mit EWS zu verwalten. Um die verwaltete EWS-API Codebeispiele in diesem Artikel zu verwenden, müssen Sie in Ihrem Code auf die folgenden Namespaces verweisen: 
  
- **System.Net**
    
- **Microsoft.Exchange.WebServices.Data.ExchangeService**
    
## <a name="find-the-correct-endpoint-by-using-the-ews-managed-api"></a>Suchen des richtigen Endpunkts mithilfe der verwaltete EWS-API
<a name="bk_Managed"> </a>

Wenn Sie die verwaltete EWS-API verwenden, werden Aufrufe des AutoErmittlungsdiensts von der **Datei "ExchangeService** -Klasse verarbeitet. Um den richtigen Endpunkt für ein e-Mail-Konto zu ermitteln, rufen Sie die **AutodiscoverUrl** -Methode für ein **[Datei "ExchangeService]** -Objekt auf. Im folgenden Codebeispiel wird gezeigt, wie der EWS-Webdienstendpunkt für eine e-Mail-Adresse auf der Exchange. asmx-Datei auf dem richtigen Client Zugriffsserver mithilfe der verwaltete EWS-API festgelegt wird. 
  
```cs
NetworkCredential credentials = new NetworkCredential(securelyStoredEmail, securelyStoredPassword);
ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2013);
service.Credentials = credentials;
service.AutodiscoverUrl("User1@contoso.com");
```

## <a name="find-the-correct-endpoint-by-using-ews"></a>Suchen des richtigen Endpunkts mithilfe von EWS
<a name="bk_SOAP"> </a>

Der SOAP-AutoErmittlungsdienst verwendet möglicherweise eine Reihe von Anforderungen und Antworten, um Ihre Anwendung an den richtigen Endpunkt für EWS weiterzuleiten. Informationen zum Prozess zum Ermitteln des richtigen Endpunkts für ein e-Mail-Konto finden Sie unter [AutoErmittlung für Exchange](autodiscover-for-exchange.md). Die folgenden XML-Beispiele zeigen die Reihe von Anforderungen und Antworten, die Sie bei der Suche nach dem richtigen Endpunkt für eine SOAP-Auto Ermittlungsanforderung erwarten können.
  
### <a name="soap-autodiscover-endpoint-request"></a>SOAP-Auto ermittlungsendpunkt-Anforderung

Das folgende Beispiel zeigt eine XML-Anforderung, die an den AutoErmittlungsdienst gesendet wird, um den richtigen Endpunkt zu finden.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://mail.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Users>
          <a:User>
            <a:Mailbox>User1@Contoso.com</a:Mailbox>
          </a:User>
        </a:Users>
        <a:RequestedSettings>
          <a:Setting>InternalEwsUrl</a:Setting>
          <a:Setting>ExternalEwsUrl</a:Setting>
        </a:RequestedSettings>
      </a:Request>
    </a:GetUserSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>

```

### <a name="soap-autodiscover-redirection-response"></a>SOAP-AutoErmittlung-Umleitungsantwort

Der AutoErmittlungsdienst antwortet möglicherweise mit einer von zwei Umleitungsantworten: einer HTTP 302-Umleitung oder einer SOAP-Umleitungsantwort. Wenn die Antwort vom Exchange-Server eine HTTP 302-Umleitung ist, sollte die Clientanwendung überprüfen, ob die Umleitungsadresse akzeptabel ist, und dann die Umleitungsantwort verfolgen.
  
> [!IMPORTANT]
> Kriterien für die Validierung einer Umleitungsantwort finden Sie unter [AutoErmittlung für Exchange](autodiscover-for-exchange.md). 
  
Wenn der AutoErmittlungsdienst eine Umleitungsantwort zurückgibt, die durch das [errorCode](https://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx) -Element des **User Response** -Elements angegeben wird, sollte Ihre Clientanwendung das **RedirectTarget** -Element verwenden, um eine neue Einstellungs Anforderung zu erstellen, die an den in der Umleitungsantwort angegebenen Server gesendet wird. Das folgende Beispiel zeigt eine Umleitungsantwort vom Server. 
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/" xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>15</h:MajorVersion>
      <h:MinorVersion>0</h:MinorVersion>
      <h:MajorBuildNumber>682</h:MajorBuildNumber>
      <h:MinorBuildNumber>1</h:MinorBuildNumber>
      <h:Version>Exchange2013</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover">
      <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
        <ErrorCode>NoError</ErrorCode>
        <ErrorMessage />
        <UserResponses>
          <UserResponse>
            <ErrorCode>RedirectAddress</ErrorCode>
            <ErrorMessage>Redirection address.</ErrorMessage>
            <RedirectTarget>User1@mail.Contoso.com</RedirectTarget>
            <UserSettingErrors />
            <UserSettings />
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope>

```

Nach einer Umleitung verwendet der Client die Umleitungs-URL, um eine weitere Anforderung vorzubereiten. Der folgende Code zeigt ein Beispiel für die Anforderung, die Sie aus der Umleitungsantwort erstellen.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>https://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://autodiscover.exchange.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Users>
          <a:User>
            <a:Mailbox>User1@mail.Contoso.com</a:Mailbox>
          </a:User>
        </a:Users>
        <a:RequestedSettings>
          <a:Setting>InternalEwsUrl</a:Setting>
          <a:Setting>ExternalEwsUrl</a:Setting>
        </a:RequestedSettings>
      </a:Request>
    </a:GetUserSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>

```

Wenn die Clientanwendung an den richtigen Endpunkt für den AutoErmittlungsdienst umgeleitet wurde, sendet der Server eine Antwort, wobei das [errorCode](https://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx) -Element des **User Response** -Elements auf **noError** festgelegt und die angeforderten Benutzereinstellungen enthält. Nur die angeforderten Benutzereinstellungen **InternalEwsUrl** und **ExternalEwsUrl**werden zurückgegeben. Das folgende Beispiel zeigt die Antwort vom Server. 
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/" 
        xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>15</h:MajorVersion>
      <h:MinorVersion>0</h:MinorVersion>
      <h:MajorBuildNumber>160</h:MajorBuildNumber>
      <h:MinorBuildNumber>4</h:MinorBuildNumber>
      <h:Version>Exchange2013</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover">
      <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
        <ErrorCode>NoError</ErrorCode>
        <ErrorMessage />
        <UserResponses>
          <UserResponse>
            <ErrorCode>NoError</ErrorCode>
            <ErrorMessage>No error.</ErrorMessage>
            <RedirectTarget i:nil="true" />
            <UserSettingErrors />
            <UserSettings>
              <UserSetting i:type="StringSetting">
                <Name>InternalEwsUrl</Name>
                <Value>https://server.Contoso.com/ews/exchange.asmx</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>ExternalEwsUrl</Name>
                <Value>https://server.Contoso.com/ews/exchange.asmx</Value>
              </UserSetting>
            </UserSettings>
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope>
```

## <a name="next-steps"></a>Nächste Schritte
<a name="bk_Next"> </a>

Durchsuchen des Endpunkts nach dem Auto Ermittlungsprozess werden die angeforderten Domänen-oder Benutzereinstellungen zurückgegeben. Informationen zum Erstellen einer Anforderung für bestimmte Einstellungen finden Sie in den folgenden Artikeln:
  
- [Abrufen von Domäneneinstellungen von einem Exchange-Server](how-to-get-domain-settings-from-an-exchange-server.md)    
- [Abrufen von Benutzereinstellungen von Exchange mithilfe der AutoErmittlung](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
## <a name="see-also"></a>Siehe auch

- [Einrichten Ihrer EWS-Anwendung](setting-up-your-ews-application.md)   
- [AutoErmittlung für Exchange](autodiscover-for-exchange.md)    
- [AutoErmittlung Webdienstverweis für Exchange](https://msdn.microsoft.com/library/a01124a8-a8cf-4b80-8625-d7ee05690bca%28Office.15%29.aspx)    
- [EWS-Referenz für Exchange](https://msdn.microsoft.com/library/2a873474-1bb2-4cb1-a556-40e8c4159f4a%28Office.15%29.aspx)
    

