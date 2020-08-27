---
title: Authentifizieren einer EWS-Anwendung mit OAuth
manager: sethgros
ms.date: 05/17/2019
ms.audience: Developer
ms.assetid: 1d8d57f9-4df5-4f21-9bbb-a89e0e259052
description: Erfahren Sie, wie Sie die OAuth-Authentifizierung mit Ihren von EWS verwalteten API-Anwendungen verwenden können.
localization_priority: Priority
ms.openlocfilehash: 795cbcc3dd1c895850086ebf0e23da905c1c99b7
ms.sourcegitcommit: 636c05a929279812c6ef87d75b01c166a4a05584
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2020
ms.locfileid: "47254965"
---
<!-- markdownlint-disable MD025 -->
# <a name="authenticate-an-ews-application-by-using-oauth"></a>Authentifizieren einer EWS-Anwendung mit OAuth
<!-- markdownlint-enable MD025 -->

Erfahren Sie, wie Sie die OAuth-Authentifizierung mit Ihren von EWS verwalteten API-Anwendungen verwenden können.

Sie können den von Azure Active Directory bereitgestellten OAuth-Authentifizierungsdienst verwenden, um Ihren von EWS verwalteten API-Anwendungen den Zugriff auf Exchange Online in Office 365 zu ermöglichen. Um OAuth mit Ihrer Anwendung zu verwenden, müssen Sie Folgendes tun:

1. [Registrieren Sie Ihre Anwendung](#register-your-application) bei Azure Active Directory.

2. [Fügen Sie Code zum Abrufen eines Authentifizierungstokens hinzu](#add-code-to-get-an-authentication-token), um ein Authentifizierungstoken von einem Tokenserver zu erhalten.

3. [Fügen Sie ein Authentifizierungstoken zu EWS-Anfragen hinzu](#add-an-authentication-token-to-ews-requests), die Sie senden.

> [!NOTE]
> Die OAuth-Authentifizierung für EWS ist in Exchange nur im Rahmen von Office 365 verfügbar. EWS-Anwendungen, die OAuth verwenden, müssen bei Azure Active Directory registriert werden.

Um den Code in diesem Artikel zu verwenden, benötigen Sie Zugriff auf die folgenden Komponenten:

- Ein Office 365-Konto mit einem Exchange Online-Postfach. Wenn Sie über kein Office 365-Abonnement verfügen, können Sie ein kostenloses Office 365-Abonnement abschließen, indem Sie sich [für das Office 365-Entwicklerprogramm registrieren](https://developer.microsoft.com/office/dev-program).

- [Microsoft Authentication Library für .NET](/dotnet/api/microsoft.identity.client?view=azure-dotnet).

- Die [von EWS verwaltete API](https://github.com/officedev/ews-managed-api).


Es gibt zwei Arten von OAuth-Berechtigungen, die für den Zugriff auf EWS-APIs in Exchange Online verwendet werden können. Bevor Sie mit dem Tutorial fortfahren, müssen Sie den zu verwendenden bestimmten Berechtigungstyp auswählen.

* **Delegierte Berechtigungen** werden von Apps verwendet, die mit angemeldetem Benutzer ausgeführt werden. Bei diesen Apps stimmt der Benutzer oder ein Administrator den von der App angeforderten Berechtigungen zu, und die App kann als angemeldeter Benutzer agieren, wenn sie API-Aufrufe sendet. 
* **Anwendungsberechtigungen** werden von Apps verwendet, die keinen angemeldeten Benutzer erfordern, z. B. Apps, die als Hintergrunddienste oder Daemons ausgeführt werden und auf mehrere Postfächer zugreifen können.

## <a name="register-your-application"></a>Registrieren der App

Um OAuth verwenden zu können, muss eine Anwendung über eine von Azure Active Directory ausgegebene Anwendungs-ID verfügen. In diesem Tutorial wird davon ausgegangen, dass es sich bei der Anwendung um eine Konsolenanwendung handelt, daher müssen Sie Ihre Anwendung als öffentlicher Client bei Azure Active Directory registrieren.

1. Öffnen Sie einen Browser, und navigieren Sie zum [Azure Active Directory Admin Center](https://aad.portal.azure.com). Melden Sie sich mit einem **persönlichen Konto** (auch: Microsoft-Konto) oder einem **Geschäfts- oder Schulkonto** an.

1. Wählen Sie in der linken Navigationsleiste **Azure Active Directory** aus, und wählen Sie dann **App-Registrierungen** unter **Verwalten** aus.

1. Wählen Sie **Neue Registrierung** aus. Legen Sie auf der Seite **Anwendung registrieren** die Werte wie folgt fest.

    - Geben Sie unter **Name** einen Anzeigenamen für Ihre App an.
    - Legen Sie **Unterstützte Kontotypen** auf den Wert fest, der für Ihr Szenario sinnvoll sind.
    - Ändern Sie für **URI umleiten** die Dropdownliste in **Öffentlicher Client (mobil & Desktop)**, und legen Sie den Wert auf `urn:ietf:wg:oauth:2.0:oob` fest.

1. Wählen Sie **Registrieren** aus. Kopieren Sie auf der nächsten Seite den Wert der **Anwendungs-ID (Client-ID)**, und speichern Sie ihn. Sie benötigen ihn im nächsten Schritt.

1. Wählen Sie in der linken Navigation unter **Verwalten** die Option **API-Berechtigungen** aus. 

1. Wählen Sie **Berechtigung hinzufügen** aus. Wählen Sie auf der Seite **API-Berechtigungen anfordern** unter **Unterstützte Legacy-APIs** die Option **Exchange** aus. 

1. Um delegierte Berechtigungen zu verwenden, wählen Sie **Delegierte Berechtigungen** und dann **EWS.AccessAsUser.All** unter **EWS** aus. Klicken Sie auf **Berechtigungen hinzufügen**. 

Um Anwendungsberechtigungen zu verwenden, befolgen Sie diese zusätzlichen Schritte.

1. Wählen Sie **Anwendungsberechtigungen** und dann **full_access_as_app** aus. Klicken Sie auf **Berechtigungen hinzufügen**.

1. Wählen Sie **Administratorzustimmung für Organisation gewähren** aus, und bestätigen Sie Ihre Auswahl im Dialogfeld "Zustimmung". 

1. Wählen Sie in der linken Navigation unter **Verwalten** die Option **Zertifikate und Geheimnisse** aus. 

1. Wählen Sie **Neuer geheimer Clientschlüssel** aus, geben Sie eine kurze Beschreibung ein, und wählen Sie dann **Hinzufügen** aus.

1. Kopieren Sie den **Wert** des neu hinzugefügten geheimen Clientschlüssels, und speichern Sie ihn. Sie benötigen ihn später. 

## <a name="add-code-to-get-an-authentication-token"></a>Hinzufügen von Code zum Abrufen eines Authentifizierungstokens

In den folgenden Codeausschnitten wird gezeigt, wie Sie mithilfe der Microsoft-Authentifizierungsbibliothek Authentifizierungstoken für delegierte Berechtigungen und Anwendungsberechtigungen abrufen. Bei diesen Codeausschnitten wird davon ausgegangen, dass die für die Authentifizierungsanforderung erforderlichen Informationen in der Datei **App.config** der Anwendung gespeichert sind. Diese Beispiele enthalten keine Fehlerprüfung. Den vollständigen Code finden Sie unter [Codebeispiele](#code-samples).

### <a name="delegated-permissions"></a>Delegierte Berechtigungen

```cs
// Configure the MSAL client to get tokens
var pcaOptions = new PublicClientApplicationOptions
{
    ClientId = ConfigurationManager.AppSettings["appId"],
    TenantId = ConfigurationManager.AppSettings["tenantId"]
};

var pca = PublicClientApplicationBuilder
    .CreateWithApplicationOptions(pcaOptions).Build();

// The permission scope required for EWS access
var ewsScopes = new string[] { "https://outlook.office.com/EWS.AccessAsUser.All" };

// Make the interactive token request
var authResult = await pca.AcquireTokenInteractive(ewsScopes).ExecuteAsync();
```

### <a name="application-permissions"></a>Anwendungsberechtigungen

```cs
// Configure the MSAL client to get tokens
var app = ConfidentialClientApplicationBuilder
    .Create(ConfigurationManager.AppSettings["appId"])
    .WithAuthority(AzureCloudInstance.AzurePublic, ConfigurationManager.AppSettings["tenantId"])
    .WithClientSecret(ConfigurationManager.AppSettings["clientSecret"]).Build();

// The permission scope required for EWS access
var ewsScopes = new string[] { "https://outlook.office.com/.default" };

//Make the token request
AuthenticationResult authResult = await app.AcquireTokenForClient(ewsScopes).ExecuteAsync();

```

## <a name="add-an-authentication-token-to-ews-requests"></a>Hinzufügen eines Authentifizierungstokens zu EWS-Anfragen

Nachdem Sie das **AuthenticationResultat**-Objekt erhalten haben, können Sie die **AccessToken**-Eigenschaft verwenden, um das vom Tokendienst ausgegebene Token abzurufen.

```cs
// Configure the ExchangeService with the access token
var ewsClient = new ExchangeService();
ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
ewsClient.Credentials = new OAuthCredentials(authResult.AccessToken);
```

Um Anwendungsberechtigungen zu verwenden, müssen Sie auch explizit ein Postfach imitieren, auf das Sie zugreifen möchten. 

```cs
//Impersonate the mailbox you'd like to access.
ewsClient.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SmtpAddress, "test@demotenant.onmicrosoft.com");
```

## <a name="code-samples"></a>Codebeispiele

### <a name="delegated-permissions"></a>Delegierte Berechtigungen

Nachfolgend finden Sie ein vollständiges Codebeispiel, das die Erstellung einer OAuth-authentifizierten EWS-Anforderung unter Verwendung delegierter Berechtigungen veranschaulicht.

```cs
using Microsoft.Exchange.WebServices.Data;
using Microsoft.Identity.Client;
using System;
using System.Configuration;

namespace EwsOAuth
{
    class Program
    {
        static void Main(string[] args)
        {
            MainAsync(args).Wait();

            if (System.Diagnostics.Debugger.IsAttached)
            {
                Console.WriteLine("Hit any key to exit...");
                Console.ReadKey();
            }
        }

        static async System.Threading.Tasks.Task MainAsync(string[] args)
        {
            // Configure the MSAL client to get tokens
            var pcaOptions = new PublicClientApplicationOptions
            {
                ClientId = ConfigurationManager.AppSettings["appId"],
                TenantId = ConfigurationManager.AppSettings["tenantId"]
            };

            var pca = PublicClientApplicationBuilder
                .CreateWithApplicationOptions(pcaOptions).Build();

            var ewsScopes = new string[] { "https://outlook.office.com/EWS.AccessAsUser.All" };

            try
            {
                // Make the interactive token request
                var authResult = await pca.AcquireTokenInteractive(ewsScopes).ExecuteAsync();

                // Configure the ExchangeService with the access token
                var ewsClient = new ExchangeService();
                ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
                ewsClient.Credentials = new OAuthCredentials(authResult.AccessToken);

                // Make an EWS call
                var folders = ewsClient.FindFolders(WellKnownFolderName.MsgFolderRoot, new FolderView(10));
                foreach(var folder in folders)
                {
                    Console.WriteLine($"Folder: {folder.DisplayName}");
                }
            }
            catch (MsalException ex)
            {
                Console.WriteLine($"Error acquiring access token: {ex.ToString()}");
            }
            catch (Exception ex)
            {
                Console.WriteLine($"Error: {ex.ToString()}");
            }
        }
    }
}
```

### <a name="application-permissions"></a>Anwendungsberechtigungen

Nachfolgend finden Sie ein vollständiges Codebeispiel, das die Erstellung einer OAuth-authentifizierten EWS-Anforderung unter Verwendung von Anwendungsberechtigungen veranschaulicht.

> [!NOTE]
> Wenn Sie einen Identitätswechsel verwenden, müssen Sie immer den X-AnchorMailbox-Anforderungsheader verwenden, der auf SMTP des imitierten Postfachs festgelegt sein sollte.

```cs
using System;
using System.Configuration;
using Microsoft.Exchange.WebServices.Data;
using Microsoft.Identity.Client;

namespace ews_oauth_samples
{
    class Program
    {
        static void Main(string[] args)
        {
            MainAsync(args).Wait();

            if (System.Diagnostics.Debugger.IsAttached)
            {
                Console.WriteLine("Hit any key to exit...");
                Console.ReadKey();
            }
        }
        
        static async System.Threading.Tasks.Task MainAsync(string[] args)
        {
            // Configure the MSAL client to get tokens
            var ewsScopes = new string[] { "https://outlook.office.com/.default" };

            var app = ConfidentialClientApplicationBuilder.Create(ConfigurationManager.AppSettings["appId"])
                .WithAuthority(AzureCloudInstance.AzurePublic, ConfigurationManager.AppSettings["tenantId"])
                .WithClientSecret(ConfigurationManager.AppSettings["clientSecret"])
                .Build();

            AuthenticationResult result = null;

            try
            {
                // Make the interactive token request
                result = await app.AcquireTokenForClient(ewsScopes)
                    .ExecuteAsync();

                // Configure the ExchangeService with the access token
                var ewsClient = new ExchangeService();
                ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
                ewsClient.Credentials = new OAuthCredentials(result.AccessToken);

                //Impersonate the mailbox you'd like to access.
                ewsClient.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SmtpAddress, "test@demotenant.onmicrosoft.com");

                //Include x-anchormailbox header
                ewsClient.HttpHeaders.Add("X-AnchorMailbox", "test@demotenant.onmicrosoft.com");

                // Make an EWS call
                var folders = ewsClient.FindFolders(WellKnownFolderName.MsgFolderRoot, new FolderView(10));
                foreach (var folder in folders)
                {
                    Console.WriteLine($"Folder: {folder.DisplayName}");
                }
            }
            catch (MsalException ex)
            {
                Console.WriteLine($"Error acquiring access token: {ex.ToString()}");
            }
            catch (Exception ex)
            {
                Console.WriteLine($"Error: {ex.ToString()}");
            }
        }
    }
}
```

Für den Beispielcode ist in beiden Fällen eine **App.config**-Datei mit den folgenden Einträgen erforderlich:

```xml
<?xml version="1.0" encoding="utf-8" ?>
<configuration>
  <startup>
    <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.7.2" />
  </startup>
  <appSettings>
    <!-- The application ID from your app registration -->
    <add key="appId" value="YOUR_APP_ID_HERE" />
    <!-- If you registered your app to support only users in your organization, change the value
           of this key to your tenant ID -->
    <add key="tenantId" value="common"/>
    <!-- The application's client secret from your app registration. Needed for application permission access -->
    <add key="clientSecret" value="YOUR_CLIENT_SECRET_HERE"/>
  </appSettings>
</configuration>
```

## <a name="see-also"></a>Siehe auch

- [Authentifizierung und EWS in Exchange](authentication-and-ews-in-exchange.md)
