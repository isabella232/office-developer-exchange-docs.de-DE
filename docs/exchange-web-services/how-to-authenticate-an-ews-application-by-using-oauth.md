---
title: Authentifizieren einer EWS-Anwendung mithilfe von OAuth
manager: sethgros
ms.date: 1/15/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1d8d57f9-4df5-4f21-9bbb-a89e0e259052
description: Erfahren Sie, wie OAuth-Authentifizierung mit der Anwendung EWS Managed API verwenden.
ms.openlocfilehash: 66bbc0525ecf78407e853da0c8dcdec92791ca56
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756861"
---
# <a name="authenticate-an-ews-application-by-using-oauth"></a><span data-ttu-id="07824-103">Authentifizieren einer EWS-Anwendung mithilfe von OAuth</span><span class="sxs-lookup"><span data-stu-id="07824-103">Authenticate an EWS application by using OAuth</span></span>

<span data-ttu-id="07824-104">Erfahren Sie, wie OAuth-Authentifizierung mit der Anwendung EWS Managed API verwenden.</span><span class="sxs-lookup"><span data-stu-id="07824-104">Learn how to use OAuth authentication with your EWS Managed API applications.</span></span>
  
<span data-ttu-id="07824-105">Den OAuth-Authentifizierungsdienst von Azure Active Directory können Sie die gleichen Authentifizierungsmodell von Office 365-REST-APIs verwendet EWS Managed API Anwendungen integrieren.</span><span class="sxs-lookup"><span data-stu-id="07824-105">You can use the OAuth authentication service provided by Azure Active Directory to integrate your EWS Managed API applications with the same authentication model used by the Office 365 REST APIs.</span></span> <span data-ttu-id="07824-106">Um OAuth mit der Anwendung, die Sie benötigen, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="07824-106">To use OAuth with your application you will need to:</span></span>
  
1. <span data-ttu-id="07824-107">[Registrieren Sie Ihre Anwendung](#bk_register) Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="07824-107">[Register your application](#bk_register) with Azure Active Directory.</span></span> 
    
2. <span data-ttu-id="07824-108">[Hinzufügen von Code ein Authentifizierungstoken abzurufenden](#bk_getToken) eine Authentifizierung auf einem Server für token token abrufen.</span><span class="sxs-lookup"><span data-stu-id="07824-108">[Add code to get an authentication token](#bk_getToken) to get an authentication token from a token server.</span></span> 
    
3. <span data-ttu-id="07824-109">[Hinzufügen einer Authentifizierungstoken EWS-Anforderungen](#bk_useToken) , die Sie senden.</span><span class="sxs-lookup"><span data-stu-id="07824-109">[Add an authentication token to EWS requests](#bk_useToken) that you send.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="07824-110">OAuth-Authentifizierung für Exchange-Webdienste ist nur in Exchange als Bestandteil von Office 365 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="07824-110">OAuth authentication for EWS is only available in Exchange as part of Office 365.</span></span> <span data-ttu-id="07824-111">EWS-Clientanwendungen erfordern die Berechtigung "Vollzugriff auf Postfach des Benutzers".</span><span class="sxs-lookup"><span data-stu-id="07824-111">EWS applications require the "Full access to user's mailbox" permission.</span></span> 
  
<span data-ttu-id="07824-112">Zum Verwenden des Codes in diesem Artikel müssen Sie den Zugriff auf die folgenden:</span><span class="sxs-lookup"><span data-stu-id="07824-112">To use the code in this article, you will need to have access to the following:</span></span>
  
- <span data-ttu-id="07824-113">Ein [Office 365-Entwicklerkonto](http://office.microsoft.com/compare-office-365-for-business-plans-FX102918419.aspx.aspx).</span><span class="sxs-lookup"><span data-stu-id="07824-113">An [Office 365 developer account](http://office.microsoft.com/compare-office-365-for-business-plans-FX102918419.aspx.aspx).</span></span> <span data-ttu-id="07824-114">Ein Testkonto können Sie Ihre Anwendung testen</span><span class="sxs-lookup"><span data-stu-id="07824-114">You can use a trial account to test your application</span></span>
    
- <span data-ttu-id="07824-115">Der [Azure AD Authentication Bibliothek für .NET](http://msdn.microsoft.com/de-de/library/office/jj573266.aspx.aspx).</span><span class="sxs-lookup"><span data-stu-id="07824-115">The [Azure AD Authentication Library for .NET](http://msdn.microsoft.com/de-de/library/office/jj573266.aspx.aspx).</span></span>
    
- <span data-ttu-id="07824-116">[Die EWS Managed API](https://github.com/officedev/ews-managed-api.aspx).</span><span class="sxs-lookup"><span data-stu-id="07824-116">[The EWS Managed API](https://github.com/officedev/ews-managed-api.aspx).</span></span>

<span data-ttu-id="07824-117"><a name="bk_register"> </a></span><span class="sxs-lookup"><span data-stu-id="07824-117"></span></span>

## <a name="register-your-application"></a><span data-ttu-id="07824-118">Registrieren Sie Ihre Anwendung</span><span class="sxs-lookup"><span data-stu-id="07824-118">Register your application</span></span>

<span data-ttu-id="07824-119">Um OAuth verwenden, müssen eine Anwendung eine Client-ID und eine Anwendung URI, der die Anwendung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="07824-119">To use OAuth, an application must have a client identifier and an application URI that identifies the application.</span></span> <span data-ttu-id="07824-120">Wenn Sie die Anwendung noch nicht mit Azure Active Directory Services registriert haben, müssen Sie manuell die Anwendung nach der Anleitung unter [Registrieren Sie app](http://msdn.microsoft.com/en-us/office/office365/howto/test-and-deploy-apps.aspx)hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="07824-120">If you have not yet registered your application with Azure Active Directory Services, you'll need to manually add your application by following the steps under [Register you app](http://msdn.microsoft.com/en-us/office/office365/howto/test-and-deploy-apps.aspx).</span></span>

<span data-ttu-id="07824-121"><a name="bk_getToken"> </a></span><span class="sxs-lookup"><span data-stu-id="07824-121"></span></span>

## <a name="add-code-to-get-an-authentication-token"></a><span data-ttu-id="07824-122">Hinzufügen von Code zum Abrufen von ein Authentifizierungstoken</span><span class="sxs-lookup"><span data-stu-id="07824-122">Add code to get an authentication token</span></span>

<span data-ttu-id="07824-123">Der Azure AD Authentication-Bibliothek für .NET vereinfacht das Abrufen von ein Authentifizierungstoken aus Azure Active Directory, damit Sie das Token in der Anwendung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="07824-123">The Azure AD Authentication Library for .NET simplifies getting an authentication token from Azure Active Directory so that you can use the token in your application.</span></span> <span data-ttu-id="07824-124">Sie müssen vier Arten von Informationen das Token Abrufen bereitzustellen:</span><span class="sxs-lookup"><span data-stu-id="07824-124">You need to provide four pieces of information to get the token:</span></span>
  
1. <span data-ttu-id="07824-125">Der URI der token-Server.</span><span class="sxs-lookup"><span data-stu-id="07824-125">The URI of the token server.</span></span> <span data-ttu-id="07824-126">Der token-Server ist die **Zertifizierungsstelle** , die den Benutzer authentifiziert und gibt ein Token, das die Anwendung mit Exchange-Webdienste zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="07824-126">The token server is the **authority** that authenticates the user and returns a token that your application can use to access EWS.</span></span> 
    
2. <span data-ttu-id="07824-127">Die Client-ID erstellt, wenn Sie die Anwendung mit Azure Active Directory registriert.</span><span class="sxs-lookup"><span data-stu-id="07824-127">The application client ID created when you registered your application with Azure Active Directory.</span></span>
    
3. <span data-ttu-id="07824-128">Der Anwendungsclient URI erstellt, wenn Sie die Anwendung mit Azure Active Directory registriert.</span><span class="sxs-lookup"><span data-stu-id="07824-128">The application client URI created when you registered your application with Azure Active Directory.</span></span>
    
4. <span data-ttu-id="07824-129">Der URI des EWS-Servers und der URI des EWS-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="07824-129">The URI of the EWS server and the URI of the EWS endpoint.</span></span> <span data-ttu-id="07824-130">In Exchange als Bestandteil von Office 365, ist das `https://<server name>/ews/exchange.asmx`.</span><span class="sxs-lookup"><span data-stu-id="07824-130">For Exchange as part of Office 365, this will be  `https://<server name>/ews/exchange.asmx`.</span></span>
    
<span data-ttu-id="07824-131">Der folgende Code veranschaulicht die Azure AD Authentication-Bibliothek verwenden, um ein Authentifizierungstoken abzurufen.</span><span class="sxs-lookup"><span data-stu-id="07824-131">The following code shows how to use the Azure AD Authentication Library to get an authentication token.</span></span> <span data-ttu-id="07824-132">Es wird davon ausgegangen, dass die erforderlichen Informationen zum Stellen der Authentifizierungsanforderung in App.config-Datei der Anwendung gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="07824-132">It assumes that the information required to make the authentication request is stored in the application's App.config file.</span></span> <span data-ttu-id="07824-133">In diesem Beispiel wird nicht enthalten, Fehler zu überprüfen, finden Sie im [Codebeispiel](#bk_codeSample) für den vollständigen Code.</span><span class="sxs-lookup"><span data-stu-id="07824-133">This example does not include error checking, see the [Code sample](#bk_codeSample) for the complete code.</span></span> 
  
```cs
string authority = ConfigurationManager.AppSettings["authority"];
string clientID = ConfigurationManager.AppSettings["clientID"];
Uri clientAppUri = new Uri(ConfigurationManager.AppSettings["clientAppUri"];
string serverName = ConfigurationManager.AppSettings["serverName"];
AuthenticationContext authenticationContext = new AuthenticationContext(authority, false);
AuthenticationResult authenticationResult = authenticationContext.AcquireToken(serverName, clientId, clientAppUri);

```

<span data-ttu-id="07824-134"><a name="bk_useToken"> </a></span><span class="sxs-lookup"><span data-stu-id="07824-134"></span></span>

## <a name="add-an-authentication-token-to-ews-requests"></a><span data-ttu-id="07824-135">Fügen Sie ein Authentifizierungstoken auf EWS-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07824-135">Add an authentication token to EWS requests</span></span>

<span data-ttu-id="07824-136">Nachdem Sie das Objekt **AuthenticationResult** erhalten haben, das Sie die **AccessToken** -Eigenschaft verwenden können, um den der Sicherheitstokendienst ausgestellten Token abzurufen.</span><span class="sxs-lookup"><span data-stu-id="07824-136">After you've received the **AuthenticationResult** object you can use the **AccessToken** property to get the token issued by the token service.</span></span> 
  
```cs
ExchangeService exchangeService = new ExchangeService(ExchangeVersion.Exchange2013);
exchangeService.Url = new Uri(ConfigurationManager.AppSettings["serverName"]+"ews/exchange.asmx");
exchangeService.TraceEnabled = true;
exchangeService.TraceFlags = TraceFlags.All;
exchangeService.Credentials = new OAuthCredentials(authenticationResult.AccessToken));
exchangeService.FindFolders(WellKnownFolderName.Root, new Folderview(10));
```

<span data-ttu-id="07824-137"><a name="bk_codeSample"> </a></span><span class="sxs-lookup"><span data-stu-id="07824-137"></span></span>

## <a name="code-sample"></a><span data-ttu-id="07824-138">Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="07824-138">Code sample</span></span>

<span data-ttu-id="07824-139">Es folgt der vollständige Beispielcode, die wird gezeigt, wie eine OAuth-Authentifizierung webdienstanforderung.</span><span class="sxs-lookup"><span data-stu-id="07824-139">The following is the complete code sample that demonstrates making an OAuth-authenticated EWS request.</span></span>
  
```cs
using System;
using System.Collections.Generic;
using System.Configuration;
using System.Globalization;
using System.Linq;
using System.Text;
using System.Threading;
using System.Threading.Tasks;
using System.Web.Script.Serialization;
using Microsoft.Exchange.WebServices.Autodiscover;
using Microsoft.Exchange.WebServices.Data;
using Microsoft.IdentityModel.Clients.ActiveDirectory;
namespace TestV1App
{
    class Program
    {
        static void Main(string[] args)
        {
            var t = new Thread(Run);
            t.SetApartmentState(ApartmentState.STA);
            t.Start();
            t.Join();
        }
        static void Run()
        {
           string authority = ConfigurationManager.AppSettings["authority"];
           string clientID = ConfigurationManager.AppSettings["clientID"];
           Uri clientAppUri = new Uri(ConfigurationManager.AppSettings["clientAppUri"];
           string serverName = ConfigurationManager.AppSettings["serverName"];
            AuthenticationResult authenticationResult = null;
            AuthenticationContext authenticationContext = new AuthenticationContext(authority, false);
            
            string errorMessage = null;
            try
            {
                Console.WriteLine("Trying to acquire token");
                authenticationResult = authenticationContext.AcquireToken(serverName, clientId, clientAppUri);
            }
                catch (AdalException ex)
            {
                errorMessage = ex.Message;
                if (ex.InnerException != null)
                {
                    errorMessage += "\nInnerException : " + ex.InnerException.Message;
                }
            }
            catch (ArgumentException ex)
            {
                errorMessage = ex.Message;
            }
            if (!string.IsNullOrEmpty(errorMessage))
            {
                Console.WriteLine("Failed: {0}" + errorMessage);
                return;
            }
            Console.WriteLine("\nMaking the protocol call\n");
            ExchangeService exchangeService = new ExchangeService(ExchangeVersion.Exchange2013);
            exchangeService.Url = new Uri(resource + "ews/exchange.asmx");
            exchangeService.TraceEnabled = true;
            exchangeService.TraceFlags = TraceFlags.All;
            exchangeService.Credentials = new OAuthCredentials(authenticationResult.AccessToken);
            exchangeService.FindFolders(WellKnownFolderName.Root, new FolderView(10));
        }
    }
}

```

<span data-ttu-id="07824-140">Der Beispielcode erfordert eine App, durch die folgenden Einträge:</span><span class="sxs-lookup"><span data-stu-id="07824-140">The sample code requires an App.config file with the following entries:</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8" ?>
<configuration>
  <startup>
    <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5" />
  </startup>
  <appSettings>
    <add key="authority" value="http://login.windows.net/<devAccountName>.onmicrosoft.com" />
    <add key="clientId" value="<ID generated by Azure Active Directory"/>
    <add key="clientAppUri" value="<URI registered with Azure Active Directory"/>
    <add key="serverName" value="outlook.office365.com" />
  </appSettings>
</configuration>
```

## <a name="see-also"></a><span data-ttu-id="07824-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07824-141">See also</span></span>

- [<span data-ttu-id="07824-142">Authentifizierung und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="07824-142">Authentication and EWS in Exchange</span></span>](authentication-and-ews-in-exchange.md)    
- [<span data-ttu-id="07824-143">Testen und Bereitstellen von apps für Office 365</span><span class="sxs-lookup"><span data-stu-id="07824-143">Test and deploy Office 365 apps</span></span>](http://msdn.microsoft.com/en-us/office/office365/howto/test-and-deploy-apps.aspx)
    

