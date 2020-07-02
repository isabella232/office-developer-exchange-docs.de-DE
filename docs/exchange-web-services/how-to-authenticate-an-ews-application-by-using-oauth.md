---
title: Authentifizieren einer EWS-Anwendung mit OAuth
manager: sethgros
ms.date: 05/17/2019
ms.audience: Developer
ms.assetid: 1d8d57f9-4df5-4f21-9bbb-a89e0e259052
description: Erfahren Sie, wie Sie die OAuth-Authentifizierung mit ihren verwaltete EWS-API Anwendungen verwenden.
localization_priority: Priority
ms.openlocfilehash: 0375095faac918859354da026118ea4ccfd6792b
ms.sourcegitcommit: eeda51cb037aa25566adb293f25574674fdb2d9e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2020
ms.locfileid: "45012566"
---
<!-- markdownlint-disable MD025 -->
# <a name="authenticate-an-ews-application-by-using-oauth"></a>Authentifizieren einer EWS-Anwendung mit OAuth
<!-- markdownlint-enable MD025 -->

Erfahren Sie, wie Sie die OAuth-Authentifizierung mit ihren verwaltete EWS-API Anwendungen verwenden.

Sie können den von Azure Active Directory bereitgestellten OAuth-Authentifizierungsdienst verwenden, um Ihren verwaltete EWS-API-Anwendungen den Zugriff auf Exchange Online in Office 365 zu ermöglichen. Um OAuth mit Ihrer Anwendung zu verwenden, müssen Sie Folgendes tun:

1. [Registrieren Sie Ihre Anwendung](#register-your-application) mit Azure Active Directory.

2. [Fügen Sie Code hinzu, um ein Authentifizierungstoken](#add-code-to-get-an-authentication-token) zum Abrufen eines Authentifizierungstokens von einem tokenserver abzurufen.

3. [Hinzufügen eines Authentifizierungstokens zu von](#add-an-authentication-token-to-ews-requests) Ihnen gesendeten EWS-Anforderungen.

> [!NOTE]
> Die OAuth-Authentifizierung für EWS steht nur in Exchange als Teil von Office 365 zur Verfügung. EWS-Anwendungen, die OAuth verwenden, müssen mit Azure Active Directory registriert werden.

Um den Code in diesem Artikel verwenden zu können, benötigen Sie Zugriff auf Folgendes:

- Ein Office 365 Konto mit einem Exchange Online Postfach. Wenn Sie kein Office 365 Konto haben, können Sie [sich für das Office 365-Entwicklerprogramm registrieren](https://developer.microsoft.com/office/dev-program) , um ein kostenloses Office 365-Abonnement zu erhalten.

- Die [Microsoft-Authentifizierungsbibliothek für .net](/dotnet/api/microsoft.identity.client?view=azure-dotnet).

- Die [verwaltete EWS-API](https://github.com/officedev/ews-managed-api).


Es gibt zwei Arten von OAuth-Berechtigungen, die für den Zugriff auf EWS-APIs in Exchange Online verwendet werden können. Bevor Sie mit dem Lernprogramm fortfahren, müssen Sie den jeweiligen Berechtigungstyp auswählen, der verwendet werden soll.

* **Delegierte Berechtigungen** werden von Apps verwendet, die mit angemeldetem Benutzer ausgeführt werden. Für diese apps stimmt der Benutzer oder ein Administrator den Berechtigungen zu, die die APP-Anforderungen und die APP beim Ausführen von API-Aufrufen als angemeldeter Benutzer ausführen können. 
* **Anwendungsberechtigungen** werden von apps verwendet, die ausgeführt werden, ohne dass ein angemeldeter Benutzer anwesend ist; beispielsweise apps, die als Hintergrunddienste oder Daemons ausgeführt werden und auf mehrere Postfächer zugreifen können.

## <a name="register-your-application"></a>Registrieren Ihrer Anwendung

Für die Verwendung von OAuth muss eine Anwendung über eine Anwendungs-ID verfügen, die von Azure Active Directory ausgestellt wurde. In diesem Lernprogramm wird davon ausgegangen, dass es sich bei der Anwendung um eine Konsolenanwendung handelt, daher müssen Sie Ihre Anwendung als öffentlichen Client mit Azure Active Directory registrieren.

1. Öffnen Sie einen Browser, und navigieren Sie zum [Azure Active Directory Admin Center](https://aad.portal.azure.com). Melden Sie sich mit einem **persönlichen Konto** (auch: Microsoft-Konto) oder einem **Geschäfts- oder Schulkonto** an.

1. Wählen Sie in der linken Navigationsleiste **Azure Active Directory** aus, und wählen Sie dann **App-Registrierungen** unter **Verwalten** aus.

1. Wählen Sie **Neue Registrierung** aus. Legen Sie auf der Seite **Anwendung registrieren** die Werte wie folgt fest.

    - Legen Sie **Name** auf einen Anzeigenamen für Ihre APP fest.
    - Legen Sie die **unterstützten Kontotypen** auf die Auswahl fest, die für Ihr Szenario sinnvoll ist.
    - Ändern Sie für **Umleitungs-URI**das Dropdown-Menü auf **Public Client (Mobile & Desktop)** , und legen Sie den Wert auf fest `urn:ietf:wg:oauth:2.0:oob` .

1. Wählen Sie **Registrieren** aus. Kopieren Sie auf der nächsten Seite den Wert der **Anwendungs-ID (Client)** , und speichern Sie ihn, dann benötigen Sie ihn später.

1. Wählen Sie **API-Berechtigungen** in der linken Navigationsleiste unter **Manage**aus. 

1. Wählen Sie **Berechtigung hinzufügen** aus. Wählen Sie auf der Seite Berechtigungen für die **Anforderungs-API** unter **unterstützte Legacy-APIs** **Exchange** aus. 

1. Um Delegierte Berechtigungen zu verwenden, wählen Sie **Delegierte Berechtigungen** aus, und wählen Sie dann **EWS aus. AccessAsUser. all** unter **EWS**. Klicken Sie auf **Berechtigungen hinzufügen**. 

Führen Sie die folgenden zusätzlichen Schritte aus, um Anwendungsberechtigungen zu verwenden.

1. Wählen Sie **Anwendungsberechtigungen** aus, und wählen Sie dann **full_access_as_app**aus. Klicken Sie auf **Berechtigungen hinzufügen**.

1. Wählen Sie **Administrator Zustimmung für org erteilen** aus, und akzeptieren Sie das Zustimmungsdialogfeld. 

1. Wählen Sie **Zertifikate & Geheimnisse** in der linken Navigationsleiste unter **Manage**aus. 

1. Wählen Sie **neuer Client Schlüssel**aus, geben Sie eine kurze Beschreibung ein, und wählen Sie **Hinzufügen**aus.

1. Kopieren Sie den **Wert** des neu hinzugefügten geheimen Client Schlüssels, und speichern Sie ihn, dann benötigen Sie ihn später. 

## <a name="add-code-to-get-an-authentication-token"></a>Hinzufügen von Code zum Abrufen eines Authentifizierungstokens

Die folgenden Codeausschnitte veranschaulichen die Verwendung der Microsoft-Authentifizierungsbibliothek zum Abrufen von Authentifizierungstoken für Delegierte Berechtigungen und Anwendungsberechtigungen. Bei diesen Codeausschnitten wird davon ausgegangen, dass die für die Authentifizierungsanforderung erforderlichen Informationen in der **App.config** Datei der Anwendung gespeichert werden. Diese Beispiele enthalten keine Fehlerüberprüfung, siehe [Codebeispiele](#code-samples) für den vollständigen Code.

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

## <a name="add-an-authentication-token-to-ews-requests"></a>Hinzufügen eines Authentifizierungstokens zu EWS-Anforderungen

Nachdem Sie das **AuthenticationResult** -Objekt empfangen haben, können Sie die **Access Token** -Eigenschaft verwenden, um das vom Tokendienst ausgestellte Token abzurufen.

```cs
// Configure the ExchangeService with the access token
var ewsClient = new ExchangeService();
ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
ewsClient.Credentials = new OAuthCredentials(authResult.AccessToken);
```

Um Anwendungsberechtigungen zu verwenden, müssen Sie auch explizit ein Postfach annehmen, auf das Sie zugreifen möchten. 

```cs
//Impersonate the mailbox you'd like to access.
ewsClient.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SmtpAddress, "test@demotenant.onmicrosoft.com");
```

## <a name="code-samples"></a>Codebeispiele

### <a name="delegated-permissions"></a>Delegierte Berechtigungen

Im folgenden finden Sie das vollständige Codebeispiel, das das Erstellen einer OAuth-authentifizierten EWS-Anforderung mithilfe von Delegierten Berechtigungen veranschaulicht.

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

Im folgenden finden Sie das vollständige Codebeispiel, das das Erstellen einer OAuth-authentifizierten EWS-Anforderung mithilfe von Anwendungsberechtigungen veranschaulicht.

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

Für den Beispielcode in beiden Fällen ist eine **App.config** Datei mit den folgenden Einträgen erforderlich:

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
