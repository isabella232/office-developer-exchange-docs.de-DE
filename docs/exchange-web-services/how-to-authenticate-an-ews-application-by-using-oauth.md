---
title: Authentifizieren einer EWS-Anwendung mit OAuth
manager: sethgros
ms.date: 07/27/2018
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1d8d57f9-4df5-4f21-9bbb-a89e0e259052
description: Erfahren Sie, wie OAuth-Authentifizierung mit der Anwendung EWS Managed API verwenden.
ms.openlocfilehash: 8b6a3fd72e42a36e31f261205292de28ef341270
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353581"
---
# <a name="authenticate-an-ews-application-by-using-oauth"></a>Authentifizieren einer EWS-Anwendung mit OAuth

Erfahren Sie, wie OAuth-Authentifizierung mit der Anwendung EWS Managed API verwenden.
  
Den OAuth-Authentifizierungsdienst von Azure Active Directory können Sie die gleichen Authentifizierungsmodell von Office 365-REST-APIs verwendet EWS Managed API Anwendungen integrieren. Um OAuth mit der Anwendung, die Sie benötigen, verwenden Sie Folgendes:
  
1. [Registrieren Sie Ihre Anwendung](#bk_register) Azure Active Directory. 
    
2. [Hinzufügen von Code ein Authentifizierungstoken abzurufenden](#bk_getToken) eine Authentifizierung auf einem Server für token token abrufen. 
    
3. [Hinzufügen einer Authentifizierungstoken EWS-Anforderungen](#bk_useToken) , die Sie senden. 
    
> [!NOTE]
> OAuth-Authentifizierung für Exchange-Webdienste ist nur in Exchange als Bestandteil von Office 365 verfügbar. EWS-Clientanwendungen erfordern die Berechtigung "Vollzugriff auf Postfach des Benutzers". 
  
Zum Verwenden des Codes in diesem Artikel müssen Sie den Zugriff auf die folgenden:
  
- Ein [Office 365-Entwicklerkonto](https://docs.microsoft.com/en-us/office/developer-program/office-365-developer-program). Ein Testkonto können Sie um Ihre Anwendung zu testen.
    
- Der [Azure AD Authentication Bibliothek für .NET](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-authentication-libraries).
    
- [Die EWS Managed API](https://github.com/officedev/ews-managed-api.aspx).

<a name="bk_register"> </a>

## <a name="register-your-application"></a>Registrieren Sie Ihre Anwendung

Um OAuth verwenden, müssen eine Anwendung eine Client-ID und eine Anwendung URI, der die Anwendung identifiziert. Wenn Sie die Anwendung noch nicht mit Azure Active Directory Services registriert haben, müssen Sie manuell die Anwendung gemäß die Schritten unter [Registrieren Sie Ihre app](https://apps.dev.microsoft.com/#/appList)hinzufügen.

<a name="bk_getToken"> </a>

## <a name="add-code-to-get-an-authentication-token"></a>Hinzufügen von Code zum Abrufen von ein Authentifizierungstoken

Der Azure AD Authentication-Bibliothek für .NET vereinfacht das Abrufen von ein Authentifizierungstoken aus Azure Active Directory, damit Sie das Token in der Anwendung verwenden können. Sie müssen vier Arten von Informationen das Token Abrufen bereitzustellen:
  
1. Der URI der token-Server. Der token-Server ist die **Zertifizierungsstelle** , die den Benutzer authentifiziert und gibt ein Token, das die Anwendung mit Exchange-Webdienste zugreifen kann. 
    
2. Die Client-ID erstellt, wenn Sie die Anwendung mit Azure Active Directory registriert.
    
3. Der Anwendungsclient URI erstellt, wenn Sie die Anwendung mit Azure Active Directory registriert.
    
4. Der URI des EWS-Servers und der URI des EWS-Endpunkts. In Exchange als Bestandteil von Office 365, ist das `https://<server name>/ews/exchange.asmx`.
    
Der folgende Code veranschaulicht die Azure AD Authentication-Bibliothek verwenden, um ein Authentifizierungstoken abzurufen. Es wird davon ausgegangen, dass die erforderlichen Informationen zum Stellen der Authentifizierungsanforderung in App.config-Datei der Anwendung gespeichert ist. In diesem Beispiel wird nicht enthalten, Fehler zu überprüfen, finden Sie im [Codebeispiel](#bk_codeSample) für den vollständigen Code. 
  
```cs
string authority = ConfigurationManager.AppSettings["authority"];
string clientID = ConfigurationManager.AppSettings["clientID"];
Uri clientAppUri = new Uri(ConfigurationManager.AppSettings["clientAppUri"];
string serverName = ConfigurationManager.AppSettings["serverName"];
AuthenticationContext authenticationContext = new AuthenticationContext(authority, false);
AuthenticationResult authenticationResult = authenticationContext.AcquireToken(serverName, clientId, clientAppUri);

```

<a name="bk_useToken"> </a>

## <a name="add-an-authentication-token-to-ews-requests"></a>Fügen Sie ein Authentifizierungstoken auf EWS-Anforderungen

Nachdem Sie das Objekt **AuthenticationResult** erhalten haben, das Sie die **AccessToken** -Eigenschaft verwenden können, um den der Sicherheitstokendienst ausgestellten Token abzurufen. 
  
```cs
ExchangeService exchangeService = new ExchangeService(ExchangeVersion.Exchange2013);
exchangeService.Url = new Uri(ConfigurationManager.AppSettings["serverName"]+"ews/exchange.asmx");
exchangeService.TraceEnabled = true;
exchangeService.TraceFlags = TraceFlags.All;
exchangeService.Credentials = new OAuthCredentials(authenticationResult.AccessToken));
exchangeService.FindFolders(WellKnownFolderName.Root, new Folderview(10));
```

<a name="bk_codeSample"> </a>

## <a name="code-sample"></a>Codebeispiel

Es folgt der vollständige Beispielcode, die wird gezeigt, wie eine OAuth-Authentifizierung webdienstanforderung.
  
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

Der Beispielcode erfordert eine App, durch die folgenden Einträge:
  
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

## <a name="see-also"></a>Siehe auch

- [Authentifizierung und EWS in Exchange](authentication-and-ews-in-exchange.md)    

    

