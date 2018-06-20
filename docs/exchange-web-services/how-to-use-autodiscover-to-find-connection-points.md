---
title: Mithilfe von AutoErmittlung Verbindungspunkte suchen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03896542-549b-4c45-973c-98f9025ea26c
description: Erfahren Sie, wie Sie den AutoErmittlungsdienst verwenden, um die Clientanwendung an den richtigen Exchange-Server zu leiten.
ms.openlocfilehash: 653fcd1c094c23c3e89e903b7194b96720802b51
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757011"
---
# <a name="use-autodiscover-to-find-connection-points"></a>Mithilfe von AutoErmittlung Verbindungspunkte suchen

Erfahren Sie, wie Sie den AutoErmittlungsdienst verwenden, um die Clientanwendung an den richtigen Exchange-Server zu leiten.
  
Der Exchange-AutoErmittlungsdienst stellt die Clientanwendung mit Konfigurationseinstellungen für e-Mail-Konten, die gehostet werden auf Exchange Online, Exchange Online als Teil von Office 365 oder Exchange-Server eine Version von Exchange beginnend mit Exchange 2013. Der AutoErmittlungsdienst ist ein Webdienst, der Konfigurationseinstellungen bereitstellt. Der AutoErmittlungsdienst ist ein Webdienst, der Exchange Server-Konfigurationsinformationen an die Clientanwendung bereitstellt. -Clientanwendungen verwenden AutoErmittlung, um den Endpunkt des AutoErmittlungsdiensts für ein bestimmtes Postfach zu bestimmen. In diesem Artikel wird erläutert, wie die Antworten von einem Exchange-Server den richtigen Endpunkt gefunden folgen. 
  
Informationen zum e-Mail-Adresse Konfigurationseinstellungen erhalten möchten finden Sie unter [benutzereinstellungen aus Exchange mithilfe der AutoErmittlung](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) [rufen](how-to-get-domain-settings-from-an-exchange-server.md)und domäneneinstellungen von einem Exchange-Server.
  
> [!NOTE]
> Der Prozess für die Suche nach den richtigen Endpunkt ist Teil der Anforderung für Benutzer oder eine domäneneinstellungen. Der AutoErmittlungsdienst verwendet eine Reihe von Antworten umleiten, um die Clientanwendung auf den richtigen Endpunkt für eine e-Mail-Adresse zu senden. 
  
Eines der folgenden Exchange-Entwicklungstechnologien können Sie den AutoErmittlungsdienst zugreifen:
  
> [!NOTE]
> Weitere Informationen über diese Exchange-Entwicklungstechnologien finden Sie unter [Durchsuchen die EWS Managed API, EWS, und Web services im Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md). 
  
- Die verwaltete API der Exchange-Webdienste (Exchange Web Services, EWS)
    
- EWS
    
    Bei Verwendung von EWS können Sie die folgenden Methoden zum Abrufen von Benutzereinstellungen verwenden:
    
  - Den SOAP-basierten AutoErmittlungsdienst
    
  - Den XML-AutoErmittlungsdienst (POX)
    
  - Einen automatisch vom SOAP- oder XML-AutoErmittlungdienst generierten Proxy
    
    Weitere Informationen zu diesen Methoden finden Sie unter [AutoErmittlung für Exchange](autodiscover-for-exchange.md).
    
Die verwaltete EWS-API stellt eine objektbasierte Schnittstelle für das Abrufen von Benutzereinstellungen bereit. Wenn die Clientanwendung verwalteten Code verwendet, wird empfohlen, die verwaltete EWS-API zu verwenden. Die verwaltete EWS-API-Schnittstelle ist besser für ein einfaches Objektmodell optimiert als der typische automatisch generierte Webdienstproxy. 
  
Bei Verwendung von EWS empfehlen wir die Verwendung des SOAP-AutoErmittlungsdiensts, da dieser eine umfassendere Sammlung von Funktionen als der POX-AutoErmittlungsdienst unterstützt.
  
## <a name="prerequisites-for-finding-an-endpoint"></a>Erforderliche Komponenten für die Suche nach einem Endpunkt
<a name="bk_Prereq"> </a>

Bevor Sie eine Clientanwendung, die den AutoErmittlungsdienst verwendet erstellen können, müssen Sie haben Zugriff auf die folgenden:
  
- Exchange Online oder einem Server, der eine Version von Exchange ausgeführt wird, beginnend mit Exchange 2007 SP1. Wenn Sie die SOAP-basierte AutoErmittlungsdienst, Exchange Online oder eine Version von Exchange, beginnend mit Exchange 2010 verwenden.
    
- Einen Exchange-Server, der Verbindungen von Ihrer Clientanwendung akzeptiert. Informationen zum Konfigurieren des Exchange-Servers finden Sie unter [Steuern des Clientanwendungszugriffs auf EWS in Exchange](controlling-client-application-access-to-ews-in-exchange.md).
    
- Ein Konto, das berechtigt ist, EWS zu verwenden. Informationen zum Konfigurieren eines Kontos finden Sie unter [Steuern des Clientanwendungszugriffs auf EWS in Exchange](controlling-client-application-access-to-ews-in-exchange.md).
    
> [!NOTE]
> [!HINWEIS] Wenn Sie die verwaltete EWS-API verwenden, müssen Sie in einigen Fällen einen Zertifikatüberprüfungsrückruf bereitstellen. Auch bei einigen generierten Proxybibliotheken, wie den von Visual Studio erstellten, benötigen Sie möglicherweise einen Zertifikatüberprüfungsrückruf. Weitere Informationen finden Sie unter [Validate ein Serverzertifikat für die EWS Managed API](how-to-validate-a-server-certificate-for-the-ews-managed-api.md). 
  
### <a name="core-concepts-for-finding-an-endpoint"></a>Kernkonzepte für die Suche nach einem Endpunkt
<a name="bk_Core"> </a>

Bevor Sie AutoErmittlung verwenden, um einen Endpunkt zu ermitteln, sollten Sie mit den in der folgenden Tabelle aufgeführten Konzepten vertraut sein.
  
|**Konzept**|**Beschreibung**|
|:-----|:-----|
|[AutoErmittlung für Exchange](autodiscover-for-exchange.md) <br/> |Bietet eine Übersicht über die Funktionsweise des AutoErmittlungsdiensts.  <br/> |
   
Wenn Sie die verwaltete EWS-API benutzen, verwenden Sie die Klasse [Microsoft.Exchange.WebServices.Data.ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) im Namespace [Microsoft.Exchange.WebServices.Data](http://msdn.microsoft.com/en-us/library/dd633907%28v=exchg.80%29.aspx), um Ihre Verbindungen mit EWS zu verwalten. Um die EWS Managed API-Codebeispiele in diesem Artikel zu verwenden, müssen Sie die folgenden Namespaces in Ihrem Code zu verweisen: 
  
- **System.Net**
    
- **Microsoft.Exchange.WebServices.Data.ExchangeService**
    
## <a name="find-the-correct-endpoint-by-using-the-ews-managed-api"></a>Suchen Sie nach den richtigen Endpunkt mithilfe der EWS Managed API
<a name="bk_Managed"> </a>

Wenn Sie die EWS Managed API verwenden, werden Anrufe mit dem AutoErmittlungsdienst von der Klasse **ExchangeService** behandelt. Um den richtigen Endpunkt für ein e-Mail-Konto zu bestimmen, rufen Sie die **AutodiscoverUrl** -Methode für ein Objekt **[ExchangeService]** . Im folgenden Codebeispiel wird veranschaulicht, wie den EWS Webdienst-Endpunkt für eine e-Mail-Adresse an der Datei besteht, auf den entsprechenden Client Access Server festgelegt wird, wird die EWS Managed API. 
  
```cs
NetworkCredential credentials = new NetworkCredential(securelyStoredEmail, securelyStoredPassword);
ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2013);
service.Credentials = credentials;
service.AutodiscoverUrl("User1@contoso.com");
```

## <a name="find-the-correct-endpoint-by-using-ews"></a>Suchen Sie nach den richtigen Endpunkt mithilfe der Exchange-Webdienste
<a name="bk_SOAP"> </a>

Der SOAP-AutoErmittlungsdienst kann eine Reihe von Anforderungen und-Antworten verwenden, um die Anwendung der richtigen Endpunkt für EWS. Informationen zu den Prozess zur Ermittlung des richtigen Endpunkts für ein e-Mail-Konto finden Sie unter [AutoErmittlung für Exchange](autodiscover-for-exchange.md). Den folgenden XML-Beispielen, die Reihe von Anforderungen und Antworten, die Sie erwarten können, bei der eine AutoErmittlung SOAP-Anforderung an den richtigen Endpunkt finden.
  
### <a name="soap-autodiscover-endpoint-request"></a>SOAP-Anforderung der AutoErmittlung-Endpunkt

Das folgende Beispiel zeigt eine XML-Anforderung, die mit dem AutoErmittlungsdienst gesendet wird, den richtigen Endpunkt zu erhalten.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>http://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://mail.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover">
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

### <a name="soap-autodiscover-redirection-response"></a>SOAP-Antwort der AutoErmittlung-Umleitung

Der AutoErmittlungsdienst reagiert mit einem von zwei Umleitungsantworten: eine HTTP 302-Umleitung oder SOAP-Antwort-Umleitung. Wenn die Antwort vom Exchange-Server eine HTTP 302-Umleitung ist, sollte die Clientanwendung überprüfen, ob die Umleitung Adresse zulässig ist, und führen Sie dann die Umleitung Antwort.
  
> [! Sicherheitshinweis] Kriterien für die Validierung einer Antwort Umleitung finden Sie unter [AutoErmittlung für Exchange](autodiscover-for-exchange.md). 
  
Wenn der AutoErmittlungsdienst eine Umleitung Antwort vom [ErrorCode](http://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx) -Element des **UserResponse** -Elements angegeben zurückgibt sollten Ihre Client-Anwendung das **RedirectTarget** -Element verwenden, um eine neue Anforderung Einstellungen zu erstellen, die ist in der Antwort Umleitung angegebenen Server gesendet. Das folgende Beispiel zeigt eine Umleitung Antwort vom Server. 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">http://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>15</h:MajorVersion>
      <h:MinorVersion>0</h:MinorVersion>
      <h:MajorBuildNumber>682</h:MajorBuildNumber>
      <h:MinorBuildNumber>1</h:MinorBuildNumber>
      <h:Version>Exchange2013</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover">
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

Nach einer Umleitung verwendet der Client die umleitungs-URL, um eine weitere Anforderung vorbereiten. Der folgende Code zeigt ein Beispiel der Anforderung, die Sie aus der Umleitung Antwort zu erstellen.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>http://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://autodiscover.exchange.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover">
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

Wenn die Client-Anwendung an den richtigen Endpunkt für den AutoErmittlungsdienst geleitet wurde, sendet der Server eine Antwort mit dem [ErrorCode](http://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx) -Element des **UserResponse** -Elements auf **NoError** festgelegt und die angeforderte enthält benutzereinstellungen. Nur die angeforderten benutzereinstellungen für **InternalEwsUrl** und **"externalewsurl"**, zurückgegeben werden. Das folgende Beispiel zeigt die Antwort vom Server. 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" 
        xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">http://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
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
    <GetUserSettingsResponseMessage xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover">
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

Suchen den Endpunkt gemäß der AutoErmittlung-Prozesses gibt die angeforderte Domäne oder benutzereinstellungen zurück. Informationen zum Treffen einer Anforderung für spezielle Einstellungen finden Sie unter den folgenden Artikeln:
  
- [Abrufen von domäneneinstellungen aus einem Exchange-server](how-to-get-domain-settings-from-an-exchange-server.md)
    
- [Abrufen von benutzereinstellungen aus Exchange mithilfe der AutoErmittlung](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
## <a name="see-also"></a>Siehe auch


- [Einrichten Ihrer EWS-Anwendung](setting-up-your-ews-application.md)
    
- [AutoErmittlung für Exchange](autodiscover-for-exchange.md)
    
- [AutoErmittlung Webdienstverweis für Exchange](http://msdn.microsoft.com/library/a01124a8-a8cf-4b80-8625-d7ee05690bca%28Office.15%29.aspx)
    
- [EWS-Referenz für Exchange](http://msdn.microsoft.com/library/2a873474-1bb2-4cb1-a556-40e8c4159f4a%28Office.15%29.aspx)
    

