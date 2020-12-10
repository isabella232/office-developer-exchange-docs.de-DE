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
# <a name="authenticate-an-ews-application-by-using-oauth"></a><span data-ttu-id="1ee07-103">Authentifizieren einer EWS-Anwendung mit OAuth</span><span class="sxs-lookup"><span data-stu-id="1ee07-103">Authenticate an EWS application by using OAuth</span></span>
<!-- markdownlint-enable MD025 -->

<span data-ttu-id="1ee07-104">Erfahren Sie, wie Sie die OAuth-Authentifizierung mit Ihren von EWS verwalteten API-Anwendungen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="1ee07-104">Learn how to use OAuth authentication with your EWS Managed API applications.</span></span>

<span data-ttu-id="1ee07-105">Sie können den von Azure Active Directory bereitgestellten OAuth-Authentifizierungsdienst verwenden, um Ihren von EWS verwalteten API-Anwendungen den Zugriff auf Exchange Online in Office 365 zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="1ee07-105">You can use the OAuth authentication service provided by Azure Active Directory to enable your EWS Managed API applications to access Exchange Online in Office 365.</span></span> <span data-ttu-id="1ee07-106">Um OAuth mit Ihrer Anwendung zu verwenden, müssen Sie Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="1ee07-106">To use OAuth with your application you will need to:</span></span>

1. <span data-ttu-id="1ee07-107">[Registrieren Sie Ihre Anwendung](#register-your-application) bei Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1ee07-107">[Register your application](#register-your-application) with Azure Active Directory.</span></span>
1. <span data-ttu-id="1ee07-108">[Fügen Sie Code zum Abrufen eines Authentifizierungstokens hinzu](#add-code-to-get-an-authentication-token), um ein Authentifizierungstoken von einem Tokenserver zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1ee07-108">[Add code to get an authentication token](#add-code-to-get-an-authentication-token) to get an authentication token from a token server.</span></span>
1. <span data-ttu-id="1ee07-109">[Fügen Sie ein Authentifizierungstoken zu EWS-Anfragen hinzu](#add-an-authentication-token-to-ews-requests), die Sie senden.</span><span class="sxs-lookup"><span data-stu-id="1ee07-109">[Add an authentication token to EWS requests](#add-an-authentication-token-to-ews-requests) that you send.</span></span>

> [!NOTE]
> <span data-ttu-id="1ee07-110">Die OAuth-Authentifizierung für EWS ist in Exchange Online nur im Rahmen von Microsoft 365 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1ee07-110">OAuth authentication for EWS is only available in Exchange Online as part of Microsoft 365.</span></span> <span data-ttu-id="1ee07-111">EWS-Anwendungen, die OAuth verwenden, müssen bei Azure Active Directory registriert werden.</span><span class="sxs-lookup"><span data-stu-id="1ee07-111">EWS applications that use OAuth must be registered with Azure Active Directory.</span></span>

<span data-ttu-id="1ee07-112">Um den Code in diesem Artikel zu verwenden, benötigen Sie Zugriff auf die folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="1ee07-112">To use the code in this article, you will need to have access to the following:</span></span>

- <span data-ttu-id="1ee07-113">Ein Microsoft 365-Konto mit einem Exchange Online-Postfach.</span><span class="sxs-lookup"><span data-stu-id="1ee07-113">A Microsoft 365 account with an Exchange Online mailbox.</span></span> <span data-ttu-id="1ee07-114">Wenn Sie kein Microsoft 365-Konto haben, können Sie sich für das [Microsoft 365-Entwicklerprogramm](https://developer.microsoft.com/microsoft-365/dev-program) anmelden, um ein kostenloses Microsoft 365-Abonnement zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1ee07-114">If you do not have a Microsoft 365 account, you can [sign up for the Microsoft 365 Developer Program](https://developer.microsoft.com/microsoft-365/dev-program) to get a free Microsoft 365 subscription.</span></span>
- <span data-ttu-id="1ee07-115">[Microsoft Authentication Library für .NET](/dotnet/api/microsoft.identity.client).</span><span class="sxs-lookup"><span data-stu-id="1ee07-115">The [Microsoft Authentication Library for .NET](/dotnet/api/microsoft.identity.client).</span></span>
- <span data-ttu-id="1ee07-116">Die [von EWS verwaltete API](https://github.com/officedev/ews-managed-api).</span><span class="sxs-lookup"><span data-stu-id="1ee07-116">The [EWS Managed API](https://github.com/officedev/ews-managed-api).</span></span>

<span data-ttu-id="1ee07-117">Es gibt zwei Arten von OAuth-Berechtigungen, die für den Zugriff auf EWS-APIs in Exchange Online verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="1ee07-117">There are two types of OAuth permissions that can be used to access EWS APIs in Exchange Online.</span></span> <span data-ttu-id="1ee07-118">Bevor Sie mit dem Tutorial fortfahren, müssen Sie den zu verwendenden bestimmten Berechtigungstyp auswählen.</span><span class="sxs-lookup"><span data-stu-id="1ee07-118">Before you proceed with the tutorial, you will need to choose the specific permission type to use.</span></span>

- <span data-ttu-id="1ee07-119">**Delegierte Berechtigungen** werden von Apps verwendet, die mit angemeldetem Benutzer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1ee07-119">**Delegated permissions** are used by apps that have a signed-in user present.</span></span> <span data-ttu-id="1ee07-120">Bei diesen Apps stimmt der Benutzer oder ein Administrator den von der App angeforderten Berechtigungen zu, und die App kann als angemeldeter Benutzer agieren, wenn sie API-Aufrufe sendet.</span><span class="sxs-lookup"><span data-stu-id="1ee07-120">For these apps, either the user or an administrator consents to the permissions that the app requests and the app can act as the signed-in user when making API calls.</span></span>
- <span data-ttu-id="1ee07-121">**Anwendungsberechtigungen** werden von Apps verwendet, die keinen angemeldeten Benutzer erfordern, z. B. Apps, die als Hintergrunddienste oder Daemons ausgeführt werden und auf mehrere Postfächer zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="1ee07-121">**Application permissions** are used by apps that run without a signed-in user present; for example, apps that run as background services or daemons and can access multiple mailboxes.</span></span>

## <a name="register-your-application"></a><span data-ttu-id="1ee07-122">Registrieren der App</span><span class="sxs-lookup"><span data-stu-id="1ee07-122">Register your application</span></span>

<span data-ttu-id="1ee07-123">Um OAuth verwenden zu können, muss eine Anwendung über eine von Azure Active Directory ausgegebene Anwendungs-ID verfügen.</span><span class="sxs-lookup"><span data-stu-id="1ee07-123">To use OAuth, an application must have an application ID issued by Azure Active Directory.</span></span> <span data-ttu-id="1ee07-124">In diesem Tutorial wird davon ausgegangen, dass es sich bei der Anwendung um eine Konsolenanwendung handelt, daher müssen Sie Ihre Anwendung als öffentlicher Client bei Azure Active Directory registrieren.</span><span class="sxs-lookup"><span data-stu-id="1ee07-124">In this tutorial, it is assumed that the application is a console application, so you need to register your application as a public client with Azure Active Directory.</span></span> <span data-ttu-id="1ee07-125">Sie können eine Anwendung im Azure Active Directory Admin Center oder mithilfe von Microsoft Graph registrieren.</span><span class="sxs-lookup"><span data-stu-id="1ee07-125">You can register an application in the Azure Active Directory admin center or by using Microsoft Graph.</span></span>

1. <span data-ttu-id="1ee07-126">Öffnen Sie einen Browser, und navigieren Sie zum [Azure Active Directory Admin Center](https://aad.portal.azure.com). Melden Sie sich mit einem **persönlichen Konto** (auch: Microsoft-Konto) oder einem **Geschäfts- oder Schulkonto** an.</span><span class="sxs-lookup"><span data-stu-id="1ee07-126">Open a browser and navigate to the [Azure Active Directory admin center](https://aad.portal.azure.com) and login using a **personal account** (aka: Microsoft Account) or **Work or School Account**.</span></span>

1. <span data-ttu-id="1ee07-127">Wählen Sie in der linken Navigationsleiste **Azure Active Directory** aus, und wählen Sie dann **App-Registrierungen** unter **Verwalten** aus.</span><span class="sxs-lookup"><span data-stu-id="1ee07-127">Select **Azure Active Directory** in the left-hand navigation, then select **App registrations** under **Manage**.</span></span>

1. <span data-ttu-id="1ee07-128">Wählen Sie **Neue Registrierung** aus.</span><span class="sxs-lookup"><span data-stu-id="1ee07-128">Select **New registration**.</span></span> <span data-ttu-id="1ee07-129">Legen Sie auf der Seite **Anwendung registrieren** die Werte wie folgt fest.</span><span class="sxs-lookup"><span data-stu-id="1ee07-129">On the **Register an application** page, set the values as follows.</span></span>

    - <span data-ttu-id="1ee07-130">Geben Sie unter **Name** einen Anzeigenamen für Ihre App an.</span><span class="sxs-lookup"><span data-stu-id="1ee07-130">Set **Name** to a friendly name for your app.</span></span>
    - <span data-ttu-id="1ee07-131">Legen Sie **Unterstützte Kontotypen** auf den Wert fest, der für Ihr Szenario sinnvoll sind.</span><span class="sxs-lookup"><span data-stu-id="1ee07-131">Set **Supported account types** to the choice that makes sense for your scenario.</span></span>
    - <span data-ttu-id="1ee07-132">Ändern Sie für **URI umleiten** die Dropdownliste in **Öffentlicher Client (mobil & Desktop)**, und legen Sie den Wert auf `urn:ietf:wg:oauth:2.0:oob` fest.</span><span class="sxs-lookup"><span data-stu-id="1ee07-132">For **Redirect URI**, change the dropdown to **Public client (mobile & desktop)** and set the value to `urn:ietf:wg:oauth:2.0:oob`.</span></span>

1. <span data-ttu-id="1ee07-133">Wählen Sie **Registrieren** aus.</span><span class="sxs-lookup"><span data-stu-id="1ee07-133">Choose **Register**.</span></span> <span data-ttu-id="1ee07-134">Kopieren Sie auf der nächsten Seite die Werte der **Anwendungs-ID (Client)** und der **Verzeichnis-ID (Mandant)** und speichern Sie diese. Sie werden sie später benötigen.</span><span class="sxs-lookup"><span data-stu-id="1ee07-134">On the next page, copy the values of the **Application (client) ID** and **Directory (tenant) ID** and save them, you will need them later.</span></span>

### <a name="configure-for-delegated-authentication"></a><span data-ttu-id="1ee07-135">Für delegierte Authentifizierung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="1ee07-135">Configure for delegated authentication</span></span>

<span data-ttu-id="1ee07-136">Wenn Ihre Anwendung eine delegierte Authentifizierung verwendet, ist keine weitere Konfiguration erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ee07-136">If your application uses delegated authentication, no further configuration is required.</span></span> <span data-ttu-id="1ee07-137">Auf der [Microsoft Identity Platform](/azure/active-directory/develop/v2-overview) können Apps dynamisch Berechtigungen anfordern, so dass Sie die Berechtigungen bei der App-Registrierung nicht vorkonfigurieren müssen.</span><span class="sxs-lookup"><span data-stu-id="1ee07-137">The [Microsoft identity platform](/azure/active-directory/develop/v2-overview) allows apps to request permissions dynamically, so you do not have to pre-configure permissions on the app registration.</span></span> <span data-ttu-id="1ee07-138">In einigen Szenarien (wie dem [On-Behalf-of-Flow](/azure/active-directory/develop/v2-oauth2-on-behalf-of-flow)) sind jedoch vorkonfigurierte Berechtigungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ee07-138">However, in some scenarios (like the [on-behalf-of flow](/azure/active-directory/develop/v2-oauth2-on-behalf-of-flow)) pre-configuring permissions is required.</span></span> <span data-ttu-id="1ee07-139">Verwenden Sie die folgenden Schritte zur Vorkonfiguration von EWS-Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="1ee07-139">Use the following steps to pre-configure EWS permissions.</span></span>

1. <span data-ttu-id="1ee07-140">Wählen Sie **Manifest** in der linken Navigation unter **Verwalten** aus.</span><span class="sxs-lookup"><span data-stu-id="1ee07-140">Select **Manifest** in the left-hand navigation under **Manage**.</span></span>

1. <span data-ttu-id="1ee07-141">Suchen Sie die Eigenschaft `requiredResourceAccess` im Manifest und fügen Sie Folgendes in eckigen Klammern (`[]`) hinzu:</span><span class="sxs-lookup"><span data-stu-id="1ee07-141">Locate the `requiredResourceAccess` property in the manifest, and add the following inside the square brackets (`[]`):</span></span>

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

1. <span data-ttu-id="1ee07-142">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="1ee07-142">Select **Save**.</span></span>

1. <span data-ttu-id="1ee07-143">Wählen Sie **API-Berechtigungen** unter **Verwalten** aus.</span><span class="sxs-lookup"><span data-stu-id="1ee07-143">Select **API permissions** under **Manage**.</span></span> <span data-ttu-id="1ee07-144">Bestätigen Sie, dass die Berechtigung **EWS AccessAsUser All** aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="1ee07-144">Confirm that the **EWS.AccessAsUser.All** permission is listed.</span></span>

### <a name="configure-for-app-only-authentication"></a><span data-ttu-id="1ee07-145">Nur-App-Authentifizierung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="1ee07-145">Configure for app-only authentication</span></span>

<span data-ttu-id="1ee07-146">Um Anwendungsberechtigungen zu verwenden, folgen Sie diesen zusätzlichen Schritten.</span><span class="sxs-lookup"><span data-stu-id="1ee07-146">To use application permissions, follow these additional steps.</span></span>

1. <span data-ttu-id="1ee07-147">Wählen Sie **Manifest** in der linken Navigation unter **Verwalten** aus.</span><span class="sxs-lookup"><span data-stu-id="1ee07-147">Select **Manifest** in the left-hand navigation under **Manage**.</span></span>

1. <span data-ttu-id="1ee07-148">Suchen Sie die Eigenschaft `requiredResourceAccess` im Manifest und fügen Sie Folgendes in eckigen Klammern (`[]`) hinzu:</span><span class="sxs-lookup"><span data-stu-id="1ee07-148">Locate the `requiredResourceAccess` property in the manifest, and add the following inside the square brackets (`[]`):</span></span>

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

1. <span data-ttu-id="1ee07-149">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="1ee07-149">Select **Save**.</span></span>

1. <span data-ttu-id="1ee07-150">Wählen Sie **API-Berechtigungen** unter **Verwalten** aus.</span><span class="sxs-lookup"><span data-stu-id="1ee07-150">Select **API permissions** under **Manage**.</span></span> <span data-ttu-id="1ee07-151">Bestätigen Sie, dass die Berechtigung **full_access_as_app** aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="1ee07-151">Confirm that the **full_access_as_app** permission is listed.</span></span>

1. <span data-ttu-id="1ee07-152">Wählen Sie **Administratorzustimmung für Organisation gewähren** aus, und bestätigen Sie Ihre Auswahl im Dialogfeld "Zustimmung".</span><span class="sxs-lookup"><span data-stu-id="1ee07-152">Select **Grant admin consent for org** and accept the consent dialog.</span></span>

1. <span data-ttu-id="1ee07-153">Wählen Sie in der linken Navigation unter **Verwalten** die Option **Zertifikate und Geheimnisse** aus.</span><span class="sxs-lookup"><span data-stu-id="1ee07-153">Select **Certificates & Secrets** in the left-hand navigation under **Manage**.</span></span>

1. <span data-ttu-id="1ee07-154">Wählen Sie **Neuer geheimer Clientschlüssel** aus, geben Sie eine kurze Beschreibung ein, und wählen Sie dann **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="1ee07-154">Select **New client secret**, enter a short description and select **Add**.</span></span>

1. <span data-ttu-id="1ee07-155">Kopieren Sie den **Wert** des neu hinzugefügten geheimen Clientschlüssels, und speichern Sie ihn. Sie benötigen ihn später.</span><span class="sxs-lookup"><span data-stu-id="1ee07-155">Copy the **Value** of the newly added client secret and save it, you will need it later.</span></span>

## <a name="add-code-to-get-an-authentication-token"></a><span data-ttu-id="1ee07-156">Hinzufügen von Code zum Abrufen eines Authentifizierungstokens</span><span class="sxs-lookup"><span data-stu-id="1ee07-156">Add code to get an authentication token</span></span>

<span data-ttu-id="1ee07-157">In den folgenden Codeausschnitten wird gezeigt, wie Sie mithilfe der Microsoft-Authentifizierungsbibliothek Authentifizierungstoken für delegierte Berechtigungen und Anwendungsberechtigungen abrufen.</span><span class="sxs-lookup"><span data-stu-id="1ee07-157">The following code snippets show how to use the Microsoft Authentication Library to get authentication tokens for delegated permissions and application permissions.</span></span> <span data-ttu-id="1ee07-158">Bei diesen Codeausschnitten wird davon ausgegangen, dass die für die Authentifizierungsanforderung erforderlichen Informationen in der Datei **App.config** der Anwendung gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="1ee07-158">These snippets assume that the information required to make the authentication request is stored in the application's **App.config** file.</span></span> <span data-ttu-id="1ee07-159">Diese Beispiele enthalten keine Fehlerprüfung. Den vollständigen Code finden Sie unter [Codebeispiele](#code-samples).</span><span class="sxs-lookup"><span data-stu-id="1ee07-159">These examples do not include error checking, see the [Code samples](#code-samples) for the complete code.</span></span>

### <a name="get-a-token-with-delegated-auth"></a><span data-ttu-id="1ee07-160">Token mit delegierter Authentifizierung anfordern</span><span class="sxs-lookup"><span data-stu-id="1ee07-160">Get a token with delegated auth</span></span>

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

### <a name="get-a-token-with-app-only-auth"></a><span data-ttu-id="1ee07-161">Token mit Nur-App-Authentifizierung anfordern</span><span class="sxs-lookup"><span data-stu-id="1ee07-161">Get a token with app-only auth</span></span>

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

## <a name="add-an-authentication-token-to-ews-requests"></a><span data-ttu-id="1ee07-162">Hinzufügen eines Authentifizierungstokens zu EWS-Anfragen</span><span class="sxs-lookup"><span data-stu-id="1ee07-162">Add an authentication token to EWS requests</span></span>

<span data-ttu-id="1ee07-163">Nachdem Sie das **AuthenticationResultat**-Objekt erhalten haben, können Sie die **AccessToken**-Eigenschaft verwenden, um das vom Tokendienst ausgegebene Token abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1ee07-163">After you've received the **AuthenticationResult** object you can use the **AccessToken** property to get the token issued by the token service.</span></span>

```cs
// Configure the ExchangeService with the access token
var ewsClient = new ExchangeService();
ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
ewsClient.Credentials = new OAuthCredentials(authResult.AccessToken);
```

<span data-ttu-id="1ee07-164">Um Anwendungsberechtigungen zu verwenden, müssen Sie die Identität eines Postfaches annehmen, auf das Sie zugreifen möchten.</span><span class="sxs-lookup"><span data-stu-id="1ee07-164">To use application permissions, you will also need to explicitly impersonate a mailbox that you would like to access.</span></span>

```cs
//Impersonate the mailbox you'd like to access.
ewsClient.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SmtpAddress, "test@demotenant.onmicrosoft.com");
```

## <a name="code-samples"></a><span data-ttu-id="1ee07-165">Codebeispiele</span><span class="sxs-lookup"><span data-stu-id="1ee07-165">Code samples</span></span>

### <a name="delegated-authentication"></a><span data-ttu-id="1ee07-166">Delegierte Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="1ee07-166">Delegated authentication</span></span>

<span data-ttu-id="1ee07-167">Im Folgenden finden Sie ein vollständiges Codebeispiel, das die Erstellung einer OAuth-authentifizierten EWS-Anforderung unter Verwendung der delegierten Authentifizierung demonstriert.</span><span class="sxs-lookup"><span data-stu-id="1ee07-167">The following is the complete code sample that demonstrates making an OAuth-authenticated EWS request using delegated authentication.</span></span>

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

### <a name="app-only-authentication"></a><span data-ttu-id="1ee07-168">Nur-App-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="1ee07-168">App-only authentication</span></span>

<span data-ttu-id="1ee07-169">Nachfolgend finden Sie ein vollständiges Codebeispiel, das die Erstellung einer OAuth-authentifizierten EWS-Anforderung unter Verwendung einer Nur-App-Authentifizierung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="1ee07-169">The following is the complete code sample that demonstrates making an OAuth-authenticated EWS request using app-only authentication.</span></span>

> [!NOTE]
> <span data-ttu-id="1ee07-170">Wenn Sie die Identitätsnachahmung verwenden, müssen Sie immer den X-AnchorMailbox-Anforderungs-Header verwenden, der auf die SMTP-Adresse des imitierten Postfachs gesetzt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="1ee07-170">When using impersonation you must always use the X-AnchorMailbox request header, which should be set to the SMTP address of the impersonated mailbox.</span></span>

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

<span data-ttu-id="1ee07-171">Für den Beispielcode ist in beiden Fällen eine **App.config**-Datei mit den folgenden Einträgen erforderlich:</span><span class="sxs-lookup"><span data-stu-id="1ee07-171">The sample code in both cases requires an **App.config** file with the following entries:</span></span>

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

## <a name="see-also"></a><span data-ttu-id="1ee07-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ee07-172">See also</span></span>

- [<span data-ttu-id="1ee07-173">Authentifizierung und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="1ee07-173">Authentication and EWS in Exchange</span></span>](authentication-and-ews-in-exchange.md)
