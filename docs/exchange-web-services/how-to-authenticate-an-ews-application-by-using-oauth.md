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
# <a name="authenticate-an-ews-application-by-using-oauth"></a><span data-ttu-id="a5a71-103">Authentifizieren einer EWS-Anwendung mit OAuth</span><span class="sxs-lookup"><span data-stu-id="a5a71-103">Authenticate an EWS application by using OAuth</span></span>
<!-- markdownlint-enable MD025 -->

<span data-ttu-id="a5a71-104">Erfahren Sie, wie Sie die OAuth-Authentifizierung mit ihren verwaltete EWS-API Anwendungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="a5a71-104">Learn how to use OAuth authentication with your EWS Managed API applications.</span></span>

<span data-ttu-id="a5a71-105">Sie können den von Azure Active Directory bereitgestellten OAuth-Authentifizierungsdienst verwenden, um Ihren verwaltete EWS-API-Anwendungen den Zugriff auf Exchange Online in Office 365 zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="a5a71-105">You can use the OAuth authentication service provided by Azure Active Directory to enable your EWS Managed API applications to access Exchange Online in Office 365.</span></span> <span data-ttu-id="a5a71-106">Um OAuth mit Ihrer Anwendung zu verwenden, müssen Sie Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="a5a71-106">To use OAuth with your application you will need to:</span></span>

1. <span data-ttu-id="a5a71-107">[Registrieren Sie Ihre Anwendung](#register-your-application) mit Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a5a71-107">[Register your application](#register-your-application) with Azure Active Directory.</span></span>

2. <span data-ttu-id="a5a71-108">[Fügen Sie Code hinzu, um ein Authentifizierungstoken](#add-code-to-get-an-authentication-token) zum Abrufen eines Authentifizierungstokens von einem tokenserver abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a5a71-108">[Add code to get an authentication token](#add-code-to-get-an-authentication-token) to get an authentication token from a token server.</span></span>

3. <span data-ttu-id="a5a71-109">[Hinzufügen eines Authentifizierungstokens zu von](#add-an-authentication-token-to-ews-requests) Ihnen gesendeten EWS-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="a5a71-109">[Add an authentication token to EWS requests](#add-an-authentication-token-to-ews-requests) that you send.</span></span>

> [!NOTE]
> <span data-ttu-id="a5a71-110">Die OAuth-Authentifizierung für EWS steht nur in Exchange als Teil von Office 365 zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="a5a71-110">OAuth authentication for EWS is only available in Exchange as part of Office 365.</span></span> <span data-ttu-id="a5a71-111">EWS-Anwendungen, die OAuth verwenden, müssen mit Azure Active Directory registriert werden.</span><span class="sxs-lookup"><span data-stu-id="a5a71-111">EWS applications that use OAuth must be registered with Azure Active Directory.</span></span>

<span data-ttu-id="a5a71-112">Um den Code in diesem Artikel verwenden zu können, benötigen Sie Zugriff auf Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a5a71-112">To use the code in this article, you will need to have access to the following:</span></span>

- <span data-ttu-id="a5a71-113">Ein Office 365 Konto mit einem Exchange Online Postfach.</span><span class="sxs-lookup"><span data-stu-id="a5a71-113">An Office 365 account with an Exchange Online mailbox.</span></span> <span data-ttu-id="a5a71-114">Wenn Sie kein Office 365 Konto haben, können Sie [sich für das Office 365-Entwicklerprogramm registrieren](https://developer.microsoft.com/office/dev-program) , um ein kostenloses Office 365-Abonnement zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a5a71-114">If you do not have an Office 365 account, you can [sign up for the Office 365 Developer Program](https://developer.microsoft.com/office/dev-program) to get a free Office 365 subscription.</span></span>

- <span data-ttu-id="a5a71-115">Die [Microsoft-Authentifizierungsbibliothek für .net](/dotnet/api/microsoft.identity.client?view=azure-dotnet).</span><span class="sxs-lookup"><span data-stu-id="a5a71-115">The [Microsoft Authentication Library for .NET](/dotnet/api/microsoft.identity.client?view=azure-dotnet).</span></span>

- <span data-ttu-id="a5a71-116">Die [verwaltete EWS-API](https://github.com/officedev/ews-managed-api).</span><span class="sxs-lookup"><span data-stu-id="a5a71-116">The [EWS Managed API](https://github.com/officedev/ews-managed-api).</span></span>


<span data-ttu-id="a5a71-117">Es gibt zwei Arten von OAuth-Berechtigungen, die für den Zugriff auf EWS-APIs in Exchange Online verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a5a71-117">There are two types of OAuth permissions that can be used to access EWS APIs in Exchange Online.</span></span> <span data-ttu-id="a5a71-118">Bevor Sie mit dem Lernprogramm fortfahren, müssen Sie den jeweiligen Berechtigungstyp auswählen, der verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a5a71-118">Before you proceed with the tutorial, you will need to choose the specific permission type to use.</span></span>

* <span data-ttu-id="a5a71-119">**Delegierte Berechtigungen** werden von Apps verwendet, die mit angemeldetem Benutzer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a5a71-119">**Delegated permissions** are used by apps that have a signed-in user present.</span></span> <span data-ttu-id="a5a71-120">Für diese apps stimmt der Benutzer oder ein Administrator den Berechtigungen zu, die die APP-Anforderungen und die APP beim Ausführen von API-Aufrufen als angemeldeter Benutzer ausführen können.</span><span class="sxs-lookup"><span data-stu-id="a5a71-120">For these apps, either the user or an administrator consents to the permissions that the app requests and the app can act as the signed-in user when making API calls.</span></span> 
* <span data-ttu-id="a5a71-121">**Anwendungsberechtigungen** werden von apps verwendet, die ausgeführt werden, ohne dass ein angemeldeter Benutzer anwesend ist; beispielsweise apps, die als Hintergrunddienste oder Daemons ausgeführt werden und auf mehrere Postfächer zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="a5a71-121">**Application permissions** are used by apps that run without a signed-in user present; for example, apps that run as background services or daemons and can access multiple mailboxes.</span></span>

## <a name="register-your-application"></a><span data-ttu-id="a5a71-122">Registrieren Ihrer Anwendung</span><span class="sxs-lookup"><span data-stu-id="a5a71-122">Register your application</span></span>

<span data-ttu-id="a5a71-123">Für die Verwendung von OAuth muss eine Anwendung über eine Anwendungs-ID verfügen, die von Azure Active Directory ausgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a5a71-123">To use OAuth, an application must have an application ID issued by Azure Active Directory.</span></span> <span data-ttu-id="a5a71-124">In diesem Lernprogramm wird davon ausgegangen, dass es sich bei der Anwendung um eine Konsolenanwendung handelt, daher müssen Sie Ihre Anwendung als öffentlichen Client mit Azure Active Directory registrieren.</span><span class="sxs-lookup"><span data-stu-id="a5a71-124">In this tutorial, it is assumed that the application is a console application, so you need to register your application as a public client with Azure Active Directory.</span></span>

1. <span data-ttu-id="a5a71-125">Öffnen Sie einen Browser, und navigieren Sie zum [Azure Active Directory Admin Center](https://aad.portal.azure.com). Melden Sie sich mit einem **persönlichen Konto** (auch: Microsoft-Konto) oder einem **Geschäfts- oder Schulkonto** an.</span><span class="sxs-lookup"><span data-stu-id="a5a71-125">Open a browser and navigate to the [Azure Active Directory admin center](https://aad.portal.azure.com) and login using a **personal account** (aka: Microsoft Account) or **Work or School Account**.</span></span>

1. <span data-ttu-id="a5a71-126">Wählen Sie in der linken Navigationsleiste **Azure Active Directory** aus, und wählen Sie dann **App-Registrierungen** unter **Verwalten** aus.</span><span class="sxs-lookup"><span data-stu-id="a5a71-126">Select **Azure Active Directory** in the left-hand navigation, then select **App registrations** under **Manage**.</span></span>

1. <span data-ttu-id="a5a71-127">Wählen Sie **Neue Registrierung** aus.</span><span class="sxs-lookup"><span data-stu-id="a5a71-127">Select **New registration**.</span></span> <span data-ttu-id="a5a71-128">Legen Sie auf der Seite **Anwendung registrieren** die Werte wie folgt fest.</span><span class="sxs-lookup"><span data-stu-id="a5a71-128">On the **Register an application** page, set the values as follows.</span></span>

    - <span data-ttu-id="a5a71-129">Legen Sie **Name** auf einen Anzeigenamen für Ihre APP fest.</span><span class="sxs-lookup"><span data-stu-id="a5a71-129">Set **Name** to a friendly name for your app.</span></span>
    - <span data-ttu-id="a5a71-130">Legen Sie die **unterstützten Kontotypen** auf die Auswahl fest, die für Ihr Szenario sinnvoll ist.</span><span class="sxs-lookup"><span data-stu-id="a5a71-130">Set **Supported account types** to the choice that makes sense for your scenario.</span></span>
    - <span data-ttu-id="a5a71-131">Ändern Sie für **Umleitungs-URI**das Dropdown-Menü auf **Public Client (Mobile & Desktop)** , und legen Sie den Wert auf fest `urn:ietf:wg:oauth:2.0:oob` .</span><span class="sxs-lookup"><span data-stu-id="a5a71-131">For **Redirect URI**, change the dropdown to **Public client (mobile & desktop)** and set the value to `urn:ietf:wg:oauth:2.0:oob`.</span></span>

1. <span data-ttu-id="a5a71-132">Wählen Sie **Registrieren** aus.</span><span class="sxs-lookup"><span data-stu-id="a5a71-132">Choose **Register**.</span></span> <span data-ttu-id="a5a71-133">Kopieren Sie auf der nächsten Seite den Wert der **Anwendungs-ID (Client)** , und speichern Sie ihn, dann benötigen Sie ihn später.</span><span class="sxs-lookup"><span data-stu-id="a5a71-133">On the next page, copy the value of the **Application (client) ID** and save it, you will need it later.</span></span>

1. <span data-ttu-id="a5a71-134">Wählen Sie **API-Berechtigungen** in der linken Navigationsleiste unter **Manage**aus.</span><span class="sxs-lookup"><span data-stu-id="a5a71-134">Select **API permissions** in the left-hand navigation under **Manage**.</span></span> 

1. <span data-ttu-id="a5a71-135">Wählen Sie **Berechtigung hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="a5a71-135">Select **Add a permission**.</span></span> <span data-ttu-id="a5a71-136">Wählen Sie auf der Seite Berechtigungen für die **Anforderungs-API** unter **unterstützte Legacy-APIs** **Exchange** aus.</span><span class="sxs-lookup"><span data-stu-id="a5a71-136">On the **Request API permissions** page, select **Exchange** under **Supported legacy APIs**.</span></span> 

1. <span data-ttu-id="a5a71-137">Um Delegierte Berechtigungen zu verwenden, wählen Sie **Delegierte Berechtigungen** aus, und wählen Sie dann **EWS aus. AccessAsUser. all** unter **EWS**.</span><span class="sxs-lookup"><span data-stu-id="a5a71-137">To use Delegated permissions, select **Delegated permissions** and then select **EWS.AccessAsUser.All** under **EWS**.</span></span> <span data-ttu-id="a5a71-138">Klicken Sie auf **Berechtigungen hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a5a71-138">Click on **Add permissions**.</span></span> 

<span data-ttu-id="a5a71-139">Führen Sie die folgenden zusätzlichen Schritte aus, um Anwendungsberechtigungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a5a71-139">To use Application permissions, follow these additional steps.</span></span>

1. <span data-ttu-id="a5a71-140">Wählen Sie **Anwendungsberechtigungen** aus, und wählen Sie dann **full_access_as_app**aus.</span><span class="sxs-lookup"><span data-stu-id="a5a71-140">Select **Application permissions** and then select **full_access_as_app**.</span></span> <span data-ttu-id="a5a71-141">Klicken Sie auf **Berechtigungen hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a5a71-141">Click on **Add permissions**.</span></span>

1. <span data-ttu-id="a5a71-142">Wählen Sie **Administrator Zustimmung für org erteilen** aus, und akzeptieren Sie das Zustimmungsdialogfeld.</span><span class="sxs-lookup"><span data-stu-id="a5a71-142">Select **Grant admin consent for org** and accept the consent dialog.</span></span> 

1. <span data-ttu-id="a5a71-143">Wählen Sie **Zertifikate & Geheimnisse** in der linken Navigationsleiste unter **Manage**aus.</span><span class="sxs-lookup"><span data-stu-id="a5a71-143">Select **Certificates & Secrets** in the left-hand navigation under **Manage**.</span></span> 

1. <span data-ttu-id="a5a71-144">Wählen Sie **neuer Client Schlüssel**aus, geben Sie eine kurze Beschreibung ein, und wählen Sie **Hinzufügen**aus.</span><span class="sxs-lookup"><span data-stu-id="a5a71-144">Select **New client secret**, enter a short description and select **Add**.</span></span>

1. <span data-ttu-id="a5a71-145">Kopieren Sie den **Wert** des neu hinzugefügten geheimen Client Schlüssels, und speichern Sie ihn, dann benötigen Sie ihn später.</span><span class="sxs-lookup"><span data-stu-id="a5a71-145">Copy the **Value** of the newly added client secret and save it, you will need it later.</span></span> 

## <a name="add-code-to-get-an-authentication-token"></a><span data-ttu-id="a5a71-146">Hinzufügen von Code zum Abrufen eines Authentifizierungstokens</span><span class="sxs-lookup"><span data-stu-id="a5a71-146">Add code to get an authentication token</span></span>

<span data-ttu-id="a5a71-147">Die folgenden Codeausschnitte veranschaulichen die Verwendung der Microsoft-Authentifizierungsbibliothek zum Abrufen von Authentifizierungstoken für Delegierte Berechtigungen und Anwendungsberechtigungen.</span><span class="sxs-lookup"><span data-stu-id="a5a71-147">The following code snippets show how to use the Microsoft Authentication Library to get authentication tokens for delegated permissions and application permissions.</span></span> <span data-ttu-id="a5a71-148">Bei diesen Codeausschnitten wird davon ausgegangen, dass die für die Authentifizierungsanforderung erforderlichen Informationen in der **App.config** Datei der Anwendung gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="a5a71-148">These snippets assume that the information required to make the authentication request is stored in the application's **App.config** file.</span></span> <span data-ttu-id="a5a71-149">Diese Beispiele enthalten keine Fehlerüberprüfung, siehe [Codebeispiele](#code-samples) für den vollständigen Code.</span><span class="sxs-lookup"><span data-stu-id="a5a71-149">These examples do not include error checking, see the [Code samples](#code-samples) for the complete code.</span></span>

### <a name="delegated-permissions"></a><span data-ttu-id="a5a71-150">Delegierte Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="a5a71-150">Delegated permissions</span></span>

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

### <a name="application-permissions"></a><span data-ttu-id="a5a71-151">Anwendungsberechtigungen</span><span class="sxs-lookup"><span data-stu-id="a5a71-151">Application permissions</span></span>

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

## <a name="add-an-authentication-token-to-ews-requests"></a><span data-ttu-id="a5a71-152">Hinzufügen eines Authentifizierungstokens zu EWS-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5a71-152">Add an authentication token to EWS requests</span></span>

<span data-ttu-id="a5a71-153">Nachdem Sie das **AuthenticationResult** -Objekt empfangen haben, können Sie die **Access Token** -Eigenschaft verwenden, um das vom Tokendienst ausgestellte Token abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a5a71-153">After you've received the **AuthenticationResult** object you can use the **AccessToken** property to get the token issued by the token service.</span></span>

```cs
// Configure the ExchangeService with the access token
var ewsClient = new ExchangeService();
ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
ewsClient.Credentials = new OAuthCredentials(authResult.AccessToken);
```

<span data-ttu-id="a5a71-154">Um Anwendungsberechtigungen zu verwenden, müssen Sie auch explizit ein Postfach annehmen, auf das Sie zugreifen möchten.</span><span class="sxs-lookup"><span data-stu-id="a5a71-154">To use Application permissions, you will also need to explictly impersonate a mailbox that you would like to access.</span></span> 

```cs
//Impersonate the mailbox you'd like to access.
ewsClient.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SmtpAddress, "test@demotenant.onmicrosoft.com");
```

## <a name="code-samples"></a><span data-ttu-id="a5a71-155">Codebeispiele</span><span class="sxs-lookup"><span data-stu-id="a5a71-155">Code samples</span></span>

### <a name="delegated-permissions"></a><span data-ttu-id="a5a71-156">Delegierte Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="a5a71-156">Delegated permissions</span></span>

<span data-ttu-id="a5a71-157">Im folgenden finden Sie das vollständige Codebeispiel, das das Erstellen einer OAuth-authentifizierten EWS-Anforderung mithilfe von Delegierten Berechtigungen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="a5a71-157">The following is the complete code sample that demonstrates making an OAuth-authenticated EWS request using Delegated permissions.</span></span>

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

### <a name="application-permissions"></a><span data-ttu-id="a5a71-158">Anwendungsberechtigungen</span><span class="sxs-lookup"><span data-stu-id="a5a71-158">Application permissions</span></span>

<span data-ttu-id="a5a71-159">Im folgenden finden Sie das vollständige Codebeispiel, das das Erstellen einer OAuth-authentifizierten EWS-Anforderung mithilfe von Anwendungsberechtigungen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="a5a71-159">The following is the complete code sample that demonstrates making an OAuth-authenticated EWS request using Application permissions.</span></span>

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

<span data-ttu-id="a5a71-160">Für den Beispielcode in beiden Fällen ist eine **App.config** Datei mit den folgenden Einträgen erforderlich:</span><span class="sxs-lookup"><span data-stu-id="a5a71-160">The sample code in both cases requires an **App.config** file with the following entries:</span></span>

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

## <a name="see-also"></a><span data-ttu-id="a5a71-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5a71-161">See also</span></span>

- [<span data-ttu-id="a5a71-162">Authentifizierung und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="a5a71-162">Authentication and EWS in Exchange</span></span>](authentication-and-ews-in-exchange.md)
