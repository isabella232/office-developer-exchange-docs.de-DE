---
title: Authentifizieren einer EWS-Anwendung mit OAuth
manager: sethgros
ms.date: 11/25/2020
ms.audience: Developer
ms.assetid: 1d8d57f9-4df5-4f21-9bbb-a89e0e259052
description: Erfahren Sie, wie Sie die OAuth-Authentifizierung mit Ihren von EWS verwalteten API-Anwendungen verwenden können.
localization_priority: Priority
ms.openlocfilehash: a7b1d2a099cf5f3c95f8453605363de12ff33c54
ms.sourcegitcommit: 843a2e030a94b12aec70c553ca4e06e39ac02d82
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "49603827"
---
<!-- markdownlint-disable MD025 -->
# <a name="authenticate-an-ews-application-by-using-oauth"></a>Authentifizieren einer EWS-Anwendung mit OAuth
<!-- markdownlint-enable MD025 -->

Erfahren Sie, wie Sie die OAuth-Authentifizierung mit Ihren von EWS verwalteten API-Anwendungen verwenden können.

Sie können den von Azure Active Directory bereitgestellten OAuth-Authentifizierungsdienst verwenden, um Ihren von EWS verwalteten API-Anwendungen den Zugriff auf Exchange Online in Office 365 zu ermöglichen. Um OAuth mit Ihrer Anwendung zu verwenden, müssen Sie Folgendes tun:

1. [Registrieren Sie Ihre Anwendung](#register-your-application) bei Azure Active Directory.
1. [Fügen Sie Code zum Abrufen eines Authentifizierungstokens hinzu](#add-code-to-get-an-authentication-token), um ein Authentifizierungstoken von einem Tokenserver zu erhalten.
1. [Fügen Sie ein Authentifizierungstoken zu EWS-Anfragen hinzu](#add-an-authentication-token-to-ews-requests), die Sie senden.

> [!NOTE]
> Die OAuth-Authentifizierung für EWS ist in Exchange Online nur im Rahmen von Microsoft 365 verfügbar. EWS-Anwendungen, die OAuth verwenden, müssen bei Azure Active Directory registriert werden.

Um den Code in diesem Artikel zu verwenden, benötigen Sie Zugriff auf die folgenden Komponenten:

- Ein Microsoft 365-Konto mit einem Exchange Online-Postfach. Wenn Sie kein Microsoft 365-Konto haben, können Sie sich für das [Microsoft 365-Entwicklerprogramm](https://developer.microsoft.com/microsoft-365/dev-program) anmelden, um ein kostenloses Microsoft 365-Abonnement zu erhalten.
- [Microsoft Authentication Library für .NET](/dotnet/api/microsoft.identity.client).
- Die [von EWS verwaltete API](https://github.com/officedev/ews-managed-api).

Es gibt zwei Arten von OAuth-Berechtigungen, die für den Zugriff auf EWS-APIs in Exchange Online verwendet werden können. Bevor Sie mit dem Tutorial fortfahren, müssen Sie den zu verwendenden bestimmten Berechtigungstyp auswählen.

- **Delegierte Berechtigungen** werden von Apps verwendet, die mit angemeldetem Benutzer ausgeführt werden. Bei diesen Apps stimmt der Benutzer oder ein Administrator den von der App angeforderten Berechtigungen zu, und die App kann als angemeldeter Benutzer agieren, wenn sie API-Aufrufe sendet.
- **Anwendungsberechtigungen** werden von Apps verwendet, die keinen angemeldeten Benutzer erfordern, z. B. Apps, die als Hintergrunddienste oder Daemons ausgeführt werden und auf mehrere Postfächer zugreifen können.

## <a name="register-your-application"></a>Registrieren der App

Um OAuth verwenden zu können, muss eine Anwendung über eine von Azure Active Directory ausgegebene Anwendungs-ID verfügen. In diesem Tutorial wird davon ausgegangen, dass es sich bei der Anwendung um eine Konsolenanwendung handelt, daher müssen Sie Ihre Anwendung als öffentlicher Client bei Azure Active Directory registrieren. Sie können eine Anwendung im Azure Active Directory Admin Center oder mithilfe von Microsoft Graph registrieren.

1. Öffnen Sie einen Browser, und navigieren Sie zum [Azure Active Directory Admin Center](https://aad.portal.azure.com). Melden Sie sich mit einem **persönlichen Konto** (auch: Microsoft-Konto) oder einem **Geschäfts- oder Schulkonto** an.

1. Wählen Sie in der linken Navigationsleiste **Azure Active Directory** aus, und wählen Sie dann **App-Registrierungen** unter **Verwalten** aus.

1. Wählen Sie **Neue Registrierung** aus. Legen Sie auf der Seite **Anwendung registrieren** die Werte wie folgt fest.

    - Geben Sie unter **Name** einen Anzeigenamen für Ihre App an.
    - Legen Sie **Unterstützte Kontotypen** auf den Wert fest, der für Ihr Szenario sinnvoll sind.
    - Ändern Sie für **URI umleiten** die Dropdownliste in **Öffentlicher Client (mobil & Desktop)**, und legen Sie den Wert auf `urn:ietf:wg:oauth:2.0:oob` fest.

1. Wählen Sie **Registrieren** aus. Kopieren Sie auf der nächsten Seite die Werte der **Anwendungs-ID (Client)** und der **Verzeichnis-ID (Mandant)** und speichern Sie diese. Sie werden sie später benötigen.

### <a name="configure-for-delegated-authentication"></a>Für delegierte Authentifizierung konfigurieren

Wenn Ihre Anwendung eine delegierte Authentifizierung verwendet, ist keine weitere Konfiguration erforderlich. Auf der [Microsoft Identity Platform](/azure/active-directory/develop/v2-overview) können Apps dynamisch Berechtigungen anfordern, so dass Sie die Berechtigungen bei der App-Registrierung nicht vorkonfigurieren müssen. In einigen Szenarien (wie dem [On-Behalf-of-Flow](/azure/active-directory/develop/v2-oauth2-on-behalf-of-flow)) sind jedoch vorkonfigurierte Berechtigungen erforderlich. Verwenden Sie die folgenden Schritte zur Vorkonfiguration von EWS-Berechtigungen.

1. Wählen Sie **Manifest** in der linken Navigation unter **Verwalten** aus.

1. Suchen Sie die Eigenschaft `requiredResourceAccess` im Manifest und fügen Sie Folgendes in eckigen Klammern (`[]`) hinzu:

    ```json
    {
        "resourceAppId": "00000002-0000-0ff1-ce00-000000000000",
        "resourceAccess": [
            {
                "id": "3b5f3d61-589b-4a3c-a359-5dd4b5ee5bd5",
                "type": "Scope"
            }
        ]
    }
    ```

1. Wählen Sie **Speichern** aus.

1. Wählen Sie **API-Berechtigungen** unter **Verwalten** aus. Bestätigen Sie, dass die Berechtigung **EWS AccessAsUser All** aufgeführt ist.

### <a name="configure-for-app-only-authentication"></a>Nur-App-Authentifizierung konfigurieren

Um Anwendungsberechtigungen zu verwenden, folgen Sie diesen zusätzlichen Schritten.

1. Wählen Sie **Manifest** in der linken Navigation unter **Verwalten** aus.

1. Suchen Sie die Eigenschaft `requiredResourceAccess` im Manifest und fügen Sie Folgendes in eckigen Klammern (`[]`) hinzu:

    ```json
    {
        "resourceAppId": "00000002-0000-0ff1-ce00-000000000000",
        "resourceAccess": [
            {
                "id": "dc890d15-9560-4a4c-9b7f-a736ec74ec40",
                "type": "Role"
            }
        ]
    }
    ```

1. Wählen Sie **Speichern** aus.

1. Wählen Sie **API-Berechtigungen** unter **Verwalten** aus. Bestätigen Sie, dass die Berechtigung **full_access_as_app** aufgeführt ist.

1. Wählen Sie **Administratorzustimmung für Organisation gewähren** aus, und bestätigen Sie Ihre Auswahl im Dialogfeld "Zustimmung".

1. Wählen Sie in der linken Navigation unter **Verwalten** die Option **Zertifikate und Geheimnisse** aus.

1. Wählen Sie **Neuer geheimer Clientschlüssel** aus, geben Sie eine kurze Beschreibung ein, und wählen Sie dann **Hinzufügen** aus.

1. Kopieren Sie den **Wert** des neu hinzugefügten geheimen Clientschlüssels, und speichern Sie ihn. Sie benötigen ihn später.

## <a name="add-code-to-get-an-authentication-token"></a>Hinzufügen von Code zum Abrufen eines Authentifizierungstokens

In den folgenden Codeausschnitten wird gezeigt, wie Sie mithilfe der Microsoft-Authentifizierungsbibliothek Authentifizierungstoken für delegierte Berechtigungen und Anwendungsberechtigungen abrufen. Bei diesen Codeausschnitten wird davon ausgegangen, dass die für die Authentifizierungsanforderung erforderlichen Informationen in der Datei **App.config** der Anwendung gespeichert sind. Diese Beispiele enthalten keine Fehlerprüfung. Den vollständigen Code finden Sie unter [Codebeispiele](#code-samples).

### <a name="get-a-token-with-delegated-auth"></a>Token mit delegierter Authentifizierung anfordern

```cs
// Using Microsoft.Identity.Client 4.22.0

// Configure the MSAL client to get tokens
var pcaOptions = new PublicClientApplicationOptions
{
    ClientId = ConfigurationManager.AppSettings["appId"],
    TenantId = ConfigurationManager.AppSettings["tenantId"]
};

var pca = PublicClientApplicationBuilder
    .CreateWithApplicationOptions(pcaOptions).Build();

// The permission scope required for EWS access
var ewsScopes = new string[] { "https://outlook.office365.com/EWS.AccessAsUser.All" };

// Make the interactive token request
var authResult = await pca.AcquireTokenInteractive(ewsScopes).ExecuteAsync();
```

### <a name="get-a-token-with-app-only-auth"></a>Token mit Nur-App-Authentifizierung anfordern

```cs
// Using Microsoft.Identity.Client 4.22.0
var cca = ConfidentialClientApplicationBuilder
    .Create(ConfigurationManager.AppSettings["appId"])
    .WithClientSecret(ConfigurationManager.AppSettings["clientSecret"])
    .WithTenantId(ConfigurationManager.AppSettings["tenantId"])
    .Build();

// The permission scope required for EWS access
var ewsScopes = new string[] { "https://outlook.office365.com/.default" };

//Make the token request
var authResult = await cca.AcquireTokenForClient(ewsScopes).ExecuteAsync();
```

## <a name="add-an-authentication-token-to-ews-requests"></a>Hinzufügen eines Authentifizierungstokens zu EWS-Anfragen

Nachdem Sie das **AuthenticationResultat**-Objekt erhalten haben, können Sie die **AccessToken**-Eigenschaft verwenden, um das vom Tokendienst ausgegebene Token abzurufen.

```cs
// Configure the ExchangeService with the access token
var ewsClient = new ExchangeService();
ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
ewsClient.Credentials = new OAuthCredentials(authResult.AccessToken);
```

Um Anwendungsberechtigungen zu verwenden, müssen Sie die Identität eines Postfaches annehmen, auf das Sie zugreifen möchten.

```cs
//Impersonate the mailbox you'd like to access.
ewsClient.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SmtpAddress, "test@demotenant.onmicrosoft.com");
```

## <a name="code-samples"></a>Codebeispiele

### <a name="delegated-authentication"></a>Delegierte Authentifizierung

Im Folgenden finden Sie ein vollständiges Codebeispiel, das die Erstellung einer OAuth-authentifizierten EWS-Anforderung unter Verwendung der delegierten Authentifizierung demonstriert.

```cs
using Microsoft.Exchange.WebServices.Data;
using Microsoft.Identity.Client;
using System;
using System.Configuration;

namespace EwsOAuth
{
    class Program
    {
        static async System.Threading.Tasks.Task Main(string[] args)
        {
            // Using Microsoft.Identity.Client 4.22.0

            // Configure the MSAL client to get tokens
            var pcaOptions = new PublicClientApplicationOptions
            {
                ClientId = ConfigurationManager.AppSettings["appId"],
                TenantId = ConfigurationManager.AppSettings["tenantId"]
            };

            var pca = PublicClientApplicationBuilder
                .CreateWithApplicationOptions(pcaOptions).Build();

            // The permission scope required for EWS access
            var ewsScopes = new string[] { "https://outlook.office365.com/EWS.AccessAsUser.All" };

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
                Console.WriteLine($"Error acquiring access token: {ex}");
            }
            catch (Exception ex)
            {
                Console.WriteLine($"Error: {ex}");
            }

            if (System.Diagnostics.Debugger.IsAttached)
            {
                Console.WriteLine("Hit any key to exit...");
                Console.ReadKey();
            }
        }
    }
}
```

### <a name="app-only-authentication"></a>Nur-App-Authentifizierung

Nachfolgend finden Sie ein vollständiges Codebeispiel, das die Erstellung einer OAuth-authentifizierten EWS-Anforderung unter Verwendung einer Nur-App-Authentifizierung veranschaulicht.

> [!NOTE]
> Wenn Sie die Identitätsnachahmung verwenden, müssen Sie immer den X-AnchorMailbox-Anforderungs-Header verwenden, der auf die SMTP-Adresse des imitierten Postfachs gesetzt werden sollte.

```cs
using Microsoft.Exchange.WebServices.Data;
using Microsoft.Identity.Client;
using System;
using System.Configuration;

namespace EwsOAuth
{
    class Program
    {
        static async System.Threading.Tasks.Task Main(string[] args)
        {
            // Using Microsoft.Identity.Client 4.22.0
            var cca = ConfidentialClientApplicationBuilder
                .Create(ConfigurationManager.AppSettings["appId"])
                .WithClientSecret(ConfigurationManager.AppSettings["clientSecret"])
                .WithTenantId(ConfigurationManager.AppSettings["tenantId"])
                .Build();

            var ewsScopes = new string[] { "https://outlook.office365.com/.default" };

            try
            {
                var authResult = await cca.AcquireTokenForClient(ewsScopes)
                    .ExecuteAsync();

                // Configure the ExchangeService with the access token
                var ewsClient = new ExchangeService();
                ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
                ewsClient.Credentials = new OAuthCredentials(authResult.AccessToken);
                ewsClient.ImpersonatedUserId =
                    new ImpersonatedUserId(ConnectingIdType.SmtpAddress, "meganb@contoso.onmicrosoft.com");

                //Include x-anchormailbox header
                ewsClient.HttpHeaders.Add("X-AnchorMailbox", "meganb@contoso.onmicrosoft.com");

                // Make an EWS call
                var folders = ewsClient.FindFolders(WellKnownFolderName.MsgFolderRoot, new FolderView(10));
                foreach(var folder in folders)
                {
                    Console.WriteLine($"Folder: {folder.DisplayName}");
                }
            }
            catch (MsalException ex)
            {
                Console.WriteLine($"Error acquiring access token: {ex}");
            }
            catch (Exception ex)
            {
                Console.WriteLine($"Error: {ex}");
            }

            if (System.Diagnostics.Debugger.IsAttached)
            {
                Console.WriteLine("Hit any key to exit...");
                Console.ReadKey();
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
    <!-- The tenant ID copied from your app registration -->
    <add key="tenantId" value="YOUR_TENANT_ID_HERE"/>
    <!-- The application's client secret from your app registration. Needed for application permission access -->
    <add key="clientSecret" value="YOUR_CLIENT_SECRET_HERE"/>
  </appSettings>
</configuration>
```

## <a name="see-also"></a>Siehe auch

- [Authentifizierung und EWS in Exchange](authentication-and-ews-in-exchange.md)
