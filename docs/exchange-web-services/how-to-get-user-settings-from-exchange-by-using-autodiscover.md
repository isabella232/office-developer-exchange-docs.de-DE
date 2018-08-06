---
title: Abrufen von Benutzereinstellungen von Exchange mithilfe der AutoErmittlung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6d90c305-4802-4e18-8d52-f60349feaa8d
description: Erfahren Sie, wie Sie Benutzerkonfigurationseinstellungen von einem Exchange-Server mithilfe der AutoErmittlung abrufen.
ms.openlocfilehash: f37de55d6681bcdef381561b166adf209d3919a9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756898"
---
# <a name="get-user-settings-from-exchange-by-using-autodiscover"></a>Abrufen von Benutzereinstellungen von Exchange mithilfe der AutoErmittlung

Erfahren Sie, wie Sie Benutzerkonfigurationseinstellungen von einem Exchange-Server mithilfe der AutoErmittlung abrufen.
  
Die AutoErmittlung vereinfacht die Anwendungskonfiguration, indem sie einfachen Zugriff auf die Benutzerkonfigurationsinformationen bietet und dabei nur die E-Mail-Adresse und das Kennwort des Benutzers verwendet. Über die AutoErmittlung [steht eine Reihe von Benutzerkonfigurationseinstellungen](http://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) zur Verfügung, beispielsweise der Anzeigenamen des Benutzers oder eine externe Webdienst-URL. 
  
Sie können eine der folgenden Entwicklungstechnologien verwenden, um Benutzereinstellungen über den AutoErmittlungsdienst abzurufen:
  
- [Erste Schritte mit verwalteten EWS-API-Clientanwendungen](get-started-with-ews-managed-api-client-applications.md)
    
- [SOAP-AutoErmittlungswebdienst](http://msdn.microsoft.com/library/61c21ea9-7fea-4f56-8ada-bf80e1e6b074%28Office.15%29.aspx)
    
- [POX-AutoErmittlungswebdienst](http://msdn.microsoft.com/library/877152f0-f4b1-4f63-b2ce-924f4bdf2d20%28Office.15%29.aspx)
    
Die verwaltete EWS-API bietet eine objektbasierte Oberfläche zum Abrufen von Benutzereinstellungen. Wenn Ihre Clientanwendung verwalteten Code verwendet, empfehlen wir, dass Sie die verwaltete EWS-API verwenden. Wenn Sie die verwaltete EWS-API verwenden, ermitteln Sie, ob die von Ihnen benötigten Einstellungen in der [Microsoft.Exchange.WebServices.Autodiscover.UserSettingName](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.autodiscover.usersettingname%28v=EXCHG.80%29.aspx)-Enumeration verfügbar sind. Ist dies nicht der Fall, können Sie den SOAP- oder POX-AutoErmittlungsdienst verwenden. 
  
Bei Verwendung eines Webdiensts empfehlen wir die Verwendung des SOAP-AutoErmittlungsdiensts, da dieser eine umfassendere Sammlung von Funktionen als der POX-AutoErmittlungsdienst unterstützt. Wenn der SOAP-AutoErmittlungsdienst nicht verfügbar ist, ist der POX-AutoErmittlungsdienst eine gute Alternative.
  
## <a name="set-up-to-get-user-settings"></a>Einrichtung zum Abrufen der Benutzereinstellungen
<a name="bk_Prereq"> </a>

Bevor Sie mithilfe des AutoErmittlungsdiensts Benutzereinstellungen abrufen, stellen Sie sicher, dass Sie Zugriff auf Folgendes haben:
  
- Bei Verwendung der EWS-API oder des POX-basierten AutoErmittlungsdienst Exchange Online, Exchange Online als Teil von Office 365 oder einen Server mit einer Version von Exchange ab Exchange 2007 SP1. 
    
- Bei Verwendung des SOAP-basierten AutoErmittlungsdiensts Exchange Online oder eine Version von Exchange ab Exchange 2010.
    
> [!NOTE]
> Wenn Sie die verwaltete EWS-API verwenden, müssen Sie in einigen Fällen eine [Methode für den Zertifikatüberprüfungsrückruf](how-to-validate-a-server-certificate-for-the-ews-managed-api.md) bereitstellen. Auch bei einigen generierten Proxybibliotheken, wie den von Visual Studio erstellten, benötigen Sie möglicherweise eine Methode für den Zertifikatüberprüfungsrückruf. 
  
## <a name="get-user-settings-by-using-the-ews-managed-api"></a>Abrufen von Benutzereinstellungen mithilfe der verwalteten EWS-API
<a name="bk_Managed"> </a>

Sie können die [GetUserSettings](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice.getusersettings%28v=exchg.80%29.aspx)-Methode zum Abrufen von Konfigurationsinformationen für einen Benutzer verwenden, wie im folgenden Beispiel gezeigt. In diesem Beispiel können Sie (aus den in der [UserSettingName](http://msdn.microsoft.com/de-DE/library/exchange/microsoft.exchange.webservices.autodiscover.usersettingname%28v=exchg.80%29.aspx)-Enumeration verfügbaren Einstellungen) ein Array von Benutzereinstellungen angeben, die zurückgegeben werden sollen. Die Methode folgt daraufhin den Umleitungsantworten des Exchange-Servers. 
  
```cs
using System;
using System.Net;
using Microsoft.Exchange.WebServices.Autodiscover;
public static GetUserSettingsResponse GetUserSettings(
    AutodiscoverService service,
    string emailAddress,
    int maxHops,
    params UserSettingName[] settings)
{
    Uri url = null;
    GetUserSettingsResponse response = null;
    for (int attempt = 0; attempt < maxHops; attempt++)
    {
        service.Url = url;
        service.EnableScpLookup = (attempt < 2);
        response = service.GetUserSettings(emailAddress, settings);
        if (response.ErrorCode == AutodiscoverErrorCode.RedirectAddress)
        {
            url = new Uri(response.RedirectTarget);
        }
        else if (response.ErrorCode == AutodiscoverErrorCode.RedirectUrl)
        {
            url = new Uri(response.RedirectTarget);
        }
        else
        {
            return response;
        }
    }
    throw new Exception("No suitable Autodiscover endpoint was found.");
}
```

Sie können die zurückgegebene Sammlung analysieren, um auf die einzelnen Schlüssel-Wert-Paare im Benutzereinstellungsarray zuzugreifen. Das folgende Beispiel zeigt, wie Sie die einzelnen zurückgegebenen Elemente analysieren und den Namen und Wert der einzelnen Schlüssel-Wert-Paare anzeigen.
  
```cs
// Display each retrieved value. The settings are part of a key/value pair.
// userresponse is a GetUserSettingsResonse object.
foreach (KeyValuePair<UserSettingName, Object> usersetting in userresponse.Settings)
{
    Console.WriteLine(usersetting.Key.ToString() + ": " + usersetting.Value);
}
```

Alternativ können Sie den Wert einer bestimmten Einstellung abrufen. Im folgenden Beispiel soll die Einstellung **ExternalEwsUrl** angezeigt werden. 
  
```cs
// Display a specific setting, such as UserDisplayName.
Console.WriteLine(userresponse.Settings[UserSettingName.UserDisplayName]);
```

## <a name="get-user-settings-by-using-soap-autodiscover"></a>Abrufen von Benutzereinstellungen mithilfe der SOAP-AutoErmittlung
<a name="bk_SOAP"> </a>

Wenn Sie nicht die verwaltete EWS-API verwenden, empfehlen wir, dass Sie den SOAP-AutoErmittlungswebdienst verwenden. Verwenden Sie den POX-AutoErmittlungswebdienst nur, wenn der SOAP-AutoErmittlungswebdienst fehlschlägt oder nicht verfügbar ist. 
  
Um Benutzereinstellungen abzurufen, verwenden Sie den [GetUserSettings-Vorgang (SOAP)](http://msdn.microsoft.com/library/758d965c-ef63-4de4-9120-e293abf14ff8%28Office.15%29.aspx). Die angeforderten Einstellungen werden als [UserSetting-Elemente](http://msdn.microsoft.com/library/aac6dc31-edd2-49d7-b845-1df4d77da58c%28Office.15%29.aspx) zurückgegeben.
  
Das folgende Beispiel zeigt eine Anforderung der SOAP-AutoErmittlung zum Abrufen von Benutzereinstellungen vom Server.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>http://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://autodiscover.exchange.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Users>
          <a:User>
            <a:Mailbox>mara@contoso.com</a:Mailbox>
          </a:User>
        </a:Users>
        <a:RequestedSettings>
          <a:Setting>UserDisplayName</a:Setting>
          <a:Setting>UserDN</a:Setting>
          <a:Setting>UserDeploymentId</a:Setting>
          <a:Setting>InternalMailboxServer</a:Setting>
          <a:Setting>MailboxDN</a:Setting>
          <a:Setting>PublicFolderServer</a:Setting>
          <a:Setting>ActiveDirectoryServer</a:Setting>
          <a:Setting>ExternalMailboxServer</a:Setting>
          <a:Setting>EcpDeliveryReportUrlFragment</a:Setting>
          <a:Setting>EcpPublishingUrlFragment</a:Setting>
          <a:Setting>EcpTextMessagingUrlFragment</a:Setting>
          <a:Setting>ExternalEwsUrl</a:Setting>
          <a:Setting>CasVersion</a:Setting>
          <a:Setting>EwsSupportedSchemas</a:Setting>
          <a:Setting>GroupingInformation</a:Setting>
        </a:RequestedSettings>
      </a:Request>
    </a:GetUserSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>
```

Das folgende Beispiel zeigt die SOAP-Antwort, die vom Server zurückgegeben wird, nachdem die Anforderung vom Client analysiert wurde. Die Antwort enthält nur die Einstellungen, die angefordert werden, wenn diese vorhanden sind.
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" xmlns:a="http://www.w3.org/2005/08/addressing">
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
                <Name>UserDisplayName</Name>
                <Value>Mara Whitley</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>UserDN</Name>
                <Value>/o=microsoft/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/cn=mara</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>UserDeploymentId</Name>
                <Value>649d50b8-a1ce-4bac-8ace-2321   e463f701</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>CasVersion</Name>
                <Value>15.01.0160.004</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>EwsSupportedSchemas</Name>
                <Value>Exchange2007, Exchange2007_SP1, Exchange2010, Exchange2010_SP1, Exchange2010_SP2, Exchange2013</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>InternalMailboxServer</Name>
                <Value>mail.contoso.com</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>ActiveDirectoryServer</Name>
                <Value>dc.contoso.com</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>MailboxDN</Name>
                <Value>/o=microsoft/ou=Exchange Administrative Group 
                  (FYDIBOHF23SPDLT)/cn=Configuration/cn=Servers/cn=mail.contoso.com/cn=Contoso Private MDB</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>PublicFolderServer</Name>
                <Value>public.contoso.com</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>EcpDeliveryReportUrlFragment</Name>
                <Value>PersonalSettings/DeliveryReport.aspx?exsvurl=1&amp;amp;IsOWA=&amp;lt;IsOWA&amp;gt;&amp;amp;MsgID=&amp;lt;MsgID&amp;gt;&amp;amp;Mbx=&amp;lt;Mbx&amp;gt;</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>EcpTextMessagingUrlFragment</Name>
                <Value>?p=sms/textmessaging.slab&amp;amp;exsvurl=1</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>EcpPublishingUrlFragment</Name>
                <Value>customize/calendarpublishing.slab?exsvurl=1&amp;amp;FldID=&amp;lt;FldID&amp;gt;</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>ExternalEwsUrl</Name>
                <Value>https://mail.contoso.com/EWS/Exchange.asmx</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>ExternalMailboxServer</Name>
                <Value>mail.contoso.com</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>GroupingInformation</Name>
                <Value>CONTOSO-1</Value>
              </UserSetting>
            </UserSettings>
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope
```

## <a name="get-user-settings-by-using-pox-autodiscover"></a>Abrufen von Benutzereinstellungen mithilfe der POX-AutoErmittlung
<a name="bk_POX"> </a>

Wir empfehlen zwar die Verwendung des SOAP-AutoErmittlungswebdiensts, der POX-AutoErmittlungswebdienst ist aber eine gute Sicherungsoption für Fälle, in denen SOAP nicht verfügbar ist. Exchange 2007 unterstützt den SOAP-AutoErmittlungswebdienst beispielsweise nicht, wenn Sie also auf Exchange 2007 abzielen, müssen Sie den POX-AutoErmittlungswebdienst verwenden. Im Gegensatz zum SOAP-AutoErmittlungswebdienst ist es beim POX-AutoErmittlungswebdienst nicht zulässig, bestimmte Einstellungen anzufordern. Stattdessen gibt der Server eine vollständige Liste verfügbarer Einstellungen als untergeordnete Elemente des [Protocol-Elements](http://msdn.microsoft.com/library/f77e4d66-6fdd-4999-9339-f7d7f9c86f44%28Office.15%29.aspx) zurück.
  
Das folgende Beispiel zeigt eine Anforderung der POX-AutoErmittlung zum Abrufen von Benutzereinstellungen vom Server. Der folgende XML-Code wird über eine HTTP-POST-Nachricht an den Server gesendet.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
  <Request>
    <EMailAddress>mara@contoso.com</EMailAddress>
    <AcceptableResponseSchema>http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
  </Request>
</Autodiscover>
```

Das folgende Beispiel zeigt die POX-Antwort, die vom Server zurückgegeben wird.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a">
    <User>
      <DisplayName>Mara Whitley</DisplayName>
      <LegacyDN>/o=First Organization/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/cn=f5eeabead90d4b6fb51d6379474692cd-Mara</LegacyDN>
      <AutoDiscoverSMTPAddress>mara@contoso.com</AutoDiscoverSMTPAddress>
      <DeploymentId>50817eff-b925-4578-a0db-13bfc635e7a5</DeploymentId>
    </User>
    <Account>
      <AccountType>email</AccountType>
      <Action>settings</Action>
      <MicrosoftOnline>False</MicrosoftOnline>
      <Protocol>
        <Type>EXCH</Type>
        <Server>5f76be3c-9138-4f66-85e0-21bc23ca35f0@contoso.com</Server>
        <ServerDN>/o=First Organization/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Configuration/cn=Servers/cn=5f76be3c-9138-4f66-85e0-21bc23ca35f0@contoso.com</ServerDN>
        <ServerVersion>73C08204</ServerVersion>
        <MdbDN>/o=First Organization/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Configuration/cn=Servers/cn=5f76be3c-9138-4f66-85e0-21bc23ca35f0@contoso.com/cn=Microsoft Private MDB</MdbDN>
        <PublicFolderServer>public.contoso.com</PublicFolderServer>
        <AD>dc.contoso.com</AD>
        <ASUrl>https://mail.contoso.com/EWS/Exchange.asmx</ASUrl>
        <EwsUrl>https://mail.contoso.com/EWS/Exchange.asmx</EwsUrl>
        <EmwsUrl>https://mail.contoso.com/EWS/Exchange.asmx</EmwsUrl>
        <EcpUrl>https://mail.contoso.com/ecp/</EcpUrl>
        <EcpUrl-um>?rfr=olk&amp;amp;p=customize/voicemail.aspx&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-um>
        <EcpUrl-aggr>?rfr=olk&amp;amp;p=personalsettings/EmailSubscriptions.slab&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-aggr>
        <EcpUrl-mt>PersonalSettings/DeliveryReport.aspx?rfr=olk&amp;amp;exsvurl=1&amp;amp;IsOWA=&amp;lt;IsOWA&amp;gt;&amp;amp;MsgID=&amp;lt;MsgID&amp;gt;&amp;amp;Mbx=&amp;lt;Mbx&amp;gt;&amp;amp;realm=contoso.com</EcpUrl-mt>
        <EcpUrl-ret>?rfr=olk&amp;amp;p=organize/retentionpolicytags.slab&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-ret>
        <EcpUrl-sms>?rfr=olk&amp;amp;p=sms/textmessaging.slab&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-sms>
        <EcpUrl-publish>customize/calendarpublishing.slab?rfr=olk&amp;amp;exsvurl=1&amp;amp;FldID=&amp;lt;FldID&amp;gt;&amp;amp;realm=contoso.com</EcpUrl-publish>
        <EcpUrl-photo>PersonalSettings/EditAccount.aspx?rfr=olk&amp;amp;chgPhoto=1&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-photo>
        <EcpUrl-tm>?rfr=olk&amp;amp;ftr=TeamMailbox&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-tm>
        <EcpUrl-tmCreating>?rfr=olk&amp;amp;ftr=TeamMailboxCreating&amp;amp;SPUrl=&amp;lt;SPUrl&amp;gt;&amp;amp;Title=&amp;lt;Title&amp;gt;&amp;amp;SPTMAppUrl=&amp;lt;SPTMAppUrl&amp;gt;&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-tmCreating>
        <EcpUrl-tmEditing>?rfr=olk&amp;amp;ftr=TeamMailboxEditing&amp;amp;Id=&amp;lt;Id&amp;gt;&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-tmEditing>
        <EcpUrl-extinstall>Extension/InstalledExtensions.slab?rfr=olk&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-extinstall>
        <OOFUrl>https://mail.contoso.com/EWS/Exchange.asmx</OOFUrl>
        <UMUrl>https://mail.contoso.com/EWS/UM2007Legacy.asmx</UMUrl>
        <OABUrl>https://mail.contoso.com/OAB/c21c7bc2-53b3-4ddc-ad89-1219b486c37c/</OABUrl>
        <ServerExclusiveConnect>off</ServerExclusiveConnect>
      </Protocol>
      <Protocol>
        <Type>EXPR</Type>
        <Server>mail.contoso.com</Server>
        <SSL>Off</SSL>
        <AuthPackage>Ntlm</AuthPackage>
        <ServerExclusiveConnect>on</ServerExclusiveConnect>
        <CertPrincipalName>None</CertPrincipalName>
      </Protocol>
      <Protocol>
        <Type>WEB</Type>
        <Internal>
          <OWAUrl AuthenticationMethod="Basic, Fba">https://mail.contoso.com/owa/</OWAUrl>
          <Protocol>
            <Type>EXCH</Type>
            <ASUrl>https://mail.contoso.com/EWS/Exchange.asmx</ASUrl>
          </Protocol>
        </Internal>
      </Protocol>
    </Account>
  </Response>
</Autodiscover>
```

## <a name="next-steps"></a>Nächste Schritte
<a name="bk_Next"> </a>

Nachdem Sie die erforderlichen Konfigurationsdetails für Ihren Benutzer vom Server abgerufen haben, können Sie mit Exchange kommunizieren, damit die Aktionen ausgeführt werden, die Ihre Anwendung ausführen soll. Ihre nächste Aktion ist davon abhängig, wie Sie mit Exchange kommunizieren und was Sie erzielen möchten. Wenn Sie ein wenig Inspiration benötigen und EWS verwenden, können Sie sich in den [101 Codebeispielen für Exchange](http://code.msdn.microsoft.com/exchange/Exchange-2013-101-Code-3c38582c) einige Anregungen holen. 
  
## <a name="see-also"></a>Siehe auch


- [AutoErmittlung für Exchange](autodiscover-for-exchange.md)
    
- [Verwaltete API der Exchange-Webdienste (Exchange Web Services, EWS)](http://msdn.microsoft.com/de-DE/library/exchange/jj220535%28v=exchg.80%29.aspx)
    
- [Referenz zum SOAP-AutoErmittlungwebdienst für Exchange](http://msdn.microsoft.com/library/61c21ea9-7fea-4f56-8ada-bf80e1e6b074%28Office.15%29.aspx)
    
- [Referenz zum POX-AutoErmittlungwebdienst für Exchange](http://msdn.microsoft.com/library/877152f0-f4b1-4f63-b2ce-924f4bdf2d20%28Office.15%29.aspx)
    

