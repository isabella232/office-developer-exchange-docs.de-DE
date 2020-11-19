---
title: Authentifizieren einer IMAP-, Pop-oder SMTP-Verbindung mit OAuth
description: Erfahren Sie, wie Sie die OAuth-Authentifizierung mit ihren IMAP-, Pop-und SMTP-Anwendungen verwenden.
author: svpsiva
ms.date: 02/19/2020
ms.audience: Developer
ms.openlocfilehash: 4662aa904ed162edcced6c096eac8cf636180f6a
ms.sourcegitcommit: 37d4ecd4f469690ba1de87baad2f2f58c40c96ba
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "49348815"
---
# <a name="authenticate-an-imap-pop-or-smtp-connection-using-oauth"></a><span data-ttu-id="8cb93-103">Authentifizieren einer IMAP-, Pop-oder SMTP-Verbindung mit OAuth</span><span class="sxs-lookup"><span data-stu-id="8cb93-103">Authenticate an IMAP, POP or SMTP connection using OAuth</span></span>

<span data-ttu-id="8cb93-104">Erfahren Sie, wie Sie mit der OAuth-Authentifizierung eine Verbindung mit IMAP-, Pop-oder SMTP-Protokollen herstellen und auf e-Mail-Daten für Office 365 Benutzer zugreifen.</span><span class="sxs-lookup"><span data-stu-id="8cb93-104">Learn how to use OAuth authentication to connect with IMAP, POP or SMTP protocols and access email data for Office 365 users.</span></span>

> <span data-ttu-id="8cb93-105">Die OAuth2-Unterstützung für IMAP-, Pop-und SMTP-Protokolle wie unten beschrieben wird sowohl für Microsoft 365 (einschließlich Office im Internet) als auch für Outlook.com-Benutzer unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8cb93-105">OAuth2 support for IMAP, POP, SMTP protocols as described below is supported for both Microsoft 365 (which includes Office on the web) and Outlook.com users.</span></span>

<span data-ttu-id="8cb93-106">Wenn Sie mit dem OAuth 2,0-Protokoll nicht vertraut sind, lesen Sie zunächst das [OAuth 2,0-Protokoll unter Microsoft Identity Platform Overview](/azure/active-directory/develop/active-directory-v2-protocols).</span><span class="sxs-lookup"><span data-stu-id="8cb93-106">If you're not familiar with the OAuth 2.0 protocol, start by reading the [OAuth 2.0 protocol on Microsoft identity platform overview](/azure/active-directory/develop/active-directory-v2-protocols).</span></span> <span data-ttu-id="8cb93-107">Weitere Informationen zur Microsoft-Authentifizierung libariers (MSAL), die das OAuth 2,0-Protokoll zur Authentifizierung von Benutzern und zum Zugriff auf sichere APIs implementieren, finden Sie in der [MSAL-Übersicht](/azure/active-directory/develop/msal-overview).</span><span class="sxs-lookup"><span data-stu-id="8cb93-107">To learn more about the Microsoft Authentication Libariers (MSAL), which implement the OAuth 2.0 protocol to authenticate users and access secure APIs, read the [MSAL overview](/azure/active-directory/develop/msal-overview).</span></span>

<span data-ttu-id="8cb93-108">Sie können den von Azure Active Directory bereitgestellten OAuth-Authentifizierungsdienst verwenden, um Ihrer Anwendung die Verbindung mit IMAP-, Pop-oder SMTP-Protokollen für den Zugriff auf Exchange Online in Office 365 zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="8cb93-108">You can use the OAuth authentication service provided by Azure Active Directory to enable your application to connect with IMAP, POP or SMTP protocols to access Exchange Online in Office 365.</span></span> <span data-ttu-id="8cb93-109">Um OAuth mit Ihrer Anwendung zu verwenden, müssen Sie Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="8cb93-109">To use OAuth with your application you need to:</span></span>

1. <span data-ttu-id="8cb93-110">[Registrieren Sie Ihre Anwendung](#register-your-application) bei Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8cb93-110">[Register your application](#register-your-application) with Azure Active Directory.</span></span>
1. <span data-ttu-id="8cb93-111">[Konfigurieren Sie Ihre Anwendung](#configure-your-application) in Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8cb93-111">[Configure your application](#configure-your-application) in Azure Active Directory.</span></span>
1. <span data-ttu-id="8cb93-112">[Rufen Sie ein Zugriffstoken](#get-an-access-token) von einem tokenserver ab.</span><span class="sxs-lookup"><span data-stu-id="8cb93-112">[Get an access token](#get-an-access-token) from a token server.</span></span>
1. <span data-ttu-id="8cb93-113">[Authentifizierung von Verbindungsanforderungen](#authenticate-connection-requests) mit einem Zugriffstoken.</span><span class="sxs-lookup"><span data-stu-id="8cb93-113">[Authenticate connection requests](#authenticate-connection-requests) with an access token.</span></span>

## <a name="register-your-application"></a><span data-ttu-id="8cb93-114">Registrieren der App</span><span class="sxs-lookup"><span data-stu-id="8cb93-114">Register your application</span></span>

<span data-ttu-id="8cb93-115">Um OAuth verwenden zu können, muss eine Anwendung mit Azure Active Directory registriert sein.</span><span class="sxs-lookup"><span data-stu-id="8cb93-115">To use OAuth, an application must be registered with Azure Active Directory.</span></span>

<span data-ttu-id="8cb93-116">Befolgen Sie die Anweisungen unter [Registrieren einer Anwendung mit der Microsoft Identity-Plattform](/azure/active-directory/develop/quickstart-register-app) , um eine neue Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8cb93-116">Follow the instructions listed in [Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to create a new application.</span></span>

## <a name="configure-your-application"></a><span data-ttu-id="8cb93-117">Konfigurieren der Anwendung</span><span class="sxs-lookup"><span data-stu-id="8cb93-117">Configure your application</span></span>

<span data-ttu-id="8cb93-118">Befolgen Sie die Anweisungen unter [Konfigurieren einer Clientanwendung für den Zugriff auf webapin](/azure/active-directory/develop/quickstart-configure-app-access-web-apis) aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8cb93-118">Follow the instructions listed in [Configure a client application to access web APIs](/azure/active-directory/develop/quickstart-configure-app-access-web-apis)</span></span>

<span data-ttu-id="8cb93-119">Stellen Sie sicher, dass Sie mindestens einen der folgenden Berechtigungs Bereiche hinzufügen, die den Protokollen entsprechen, die Sie integrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="8cb93-119">Make sure to add one or more of the following permission scopes that correspond to the protocols you would like to integrate with.</span></span> <span data-ttu-id="8cb93-120">Wählen Sie im Assistenten zum **Hinzufügen** von Berechtigungen **Microsoft Graph** und dann **Delegierte Berechtigungen** aus, um die folgenden Berechtigungs Bereiche zu finden.</span><span class="sxs-lookup"><span data-stu-id="8cb93-120">In the **Add a permission** wizard, select **Microsoft Graph** and then **Delegated permissions** to find the following permission scopes listed.</span></span>

| <span data-ttu-id="8cb93-121">Protokoll</span><span class="sxs-lookup"><span data-stu-id="8cb93-121">Protocol</span></span>  | <span data-ttu-id="8cb93-122">Berechtigungsbereich</span><span class="sxs-lookup"><span data-stu-id="8cb93-122">Permission scope</span></span>        |
|-----------|-------------------------|
| <span data-ttu-id="8cb93-123">IMAP</span><span class="sxs-lookup"><span data-stu-id="8cb93-123">IMAP</span></span>      | `IMAP.AccessAsUser.All` |
| <span data-ttu-id="8cb93-124">POP</span><span class="sxs-lookup"><span data-stu-id="8cb93-124">POP</span></span>       | `POP.AccessAsUser.All`  |
| <span data-ttu-id="8cb93-125">SMTP-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="8cb93-125">SMTP AUTH</span></span> | `SMTP.Send`             |

## <a name="get-an-access-token"></a><span data-ttu-id="8cb93-126">Abrufen eines Zugriffstokens</span><span class="sxs-lookup"><span data-stu-id="8cb93-126">Get an access token</span></span>

<span data-ttu-id="8cb93-127">Sie können eine unserer MSAL- [Clientbibliotheken](/azure/active-directory/develop/msal-overview) verwenden, um ein Zugriffstoken aus Ihrer Clientanwendung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8cb93-127">You can use one of our [MSAL client libraries](/azure/active-directory/develop/msal-overview) to fetch an access token from your client application.</span></span>

<span data-ttu-id="8cb93-128">Alternativ können Sie einen geeigneten Fluss aus der folgenden Liste auswählen und die entsprechenden Schritte ausführen, um die zugrunde liegenden Identity Platform-Rest-APIs aufzurufen und ein Zugriffstoken abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8cb93-128">Alternatively, you can select an appropriate flow from the following list and follow the corresponding steps to call the underlying identity platform REST APIs and retrieve an access token.</span></span>

1. [<span data-ttu-id="8cb93-129">OAuth2-Autorisierungscode Fluss</span><span class="sxs-lookup"><span data-stu-id="8cb93-129">OAuth2 authorization code flow</span></span>](/azure/active-directory/develop/v2-oauth2-auth-code-flow)
1. [<span data-ttu-id="8cb93-130">OAuth2-Zuteilungs Fluss für Geräteautorisierung</span><span class="sxs-lookup"><span data-stu-id="8cb93-130">OAuth2 Device authorization grant flow</span></span>](/azure/active-directory/develop/v2-oauth2-device-code)

<span data-ttu-id="8cb93-131">OAuth-Zugriff auf IMAP-, Pop-, SMTP-AUTH-Protokolle über OAuth2-Clientanmeldeinformationen Grant Flow wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8cb93-131">OAuth access to IMAP, POP, SMTP AUTH protocols via OAuth2 client credentials grant flow is not supported.</span></span> <span data-ttu-id="8cb93-132">Wenn Ihre Anwendung beständigen Zugriff auf alle Postfächer in einer Microsoft 365-Organisation benötigt, wird empfohlen, dass Sie die Microsoft Graph-APIs verwenden, die den Zugriff ohne Benutzer erlauben, granulare Berechtigungen aktivieren und Administratoren den Zugriff auf bestimmte Postfächer gewähren lassen.</span><span class="sxs-lookup"><span data-stu-id="8cb93-132">If your application needs persistent access to all mailboxes in a Microsoft 365 organization, we recommend that you use the Microsoft Graph APIs which allow access without a user, enable granular permissions and let administrators scope such access to a specific set of mailboxes.</span></span>

<span data-ttu-id="8cb93-133">Stellen Sie sicher, dass Sie die vollständigen Bereiche angeben, einschließlich der Outlook-Ressourcen-URLs, wenn Sie Ihre Anwendung autorisieren und ein Zugriffstoken anfordern.</span><span class="sxs-lookup"><span data-stu-id="8cb93-133">Make sure to specify the full scopes, including Outlook resource URLs, when authorizing your application and requesting an access token.</span></span>

| <span data-ttu-id="8cb93-134">Protokoll</span><span class="sxs-lookup"><span data-stu-id="8cb93-134">Protocol</span></span>  | <span data-ttu-id="8cb93-135">Zeichenfolge für Berechtigungs Bereiche</span><span class="sxs-lookup"><span data-stu-id="8cb93-135">Permission scope string</span></span> |
|-----------|-------------------------|
| <span data-ttu-id="8cb93-136">IMAP</span><span class="sxs-lookup"><span data-stu-id="8cb93-136">IMAP</span></span>      | `https://outlook.office.com/IMAP.AccessAsUser.All` |
| <span data-ttu-id="8cb93-137">POP</span><span class="sxs-lookup"><span data-stu-id="8cb93-137">POP</span></span>       | `https://outlook.office.com/POP.AccessAsUser.All`  |
| <span data-ttu-id="8cb93-138">SMTP-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="8cb93-138">SMTP AUTH</span></span> | `https://outlook.office.com/SMTP.Send`             |

<span data-ttu-id="8cb93-139">Darüber hinaus können Sie [offline_access](/azure/active-directory/develop/v2-permissions-and-consent#offline_access) Bereich anfordern.</span><span class="sxs-lookup"><span data-stu-id="8cb93-139">In addition, you can request for [offline_access](/azure/active-directory/develop/v2-permissions-and-consent#offline_access) scope.</span></span> <span data-ttu-id="8cb93-140">Wenn ein Benutzer den offline_access Bereich genehmigt, kann die APP Aktualisierungstoken vom Microsoft Identity Platform-Token-Endpunkt empfangen.</span><span class="sxs-lookup"><span data-stu-id="8cb93-140">When a user approves the offline_access scope, your app can receive refresh tokens from the Microsoft identity platform token endpoint.</span></span> <span data-ttu-id="8cb93-141">Aktualisierungstoken sind langlebig.</span><span class="sxs-lookup"><span data-stu-id="8cb93-141">Refresh tokens are long-lived.</span></span> <span data-ttu-id="8cb93-142">Ihre APP kann neue Zugriffstoken erhalten, wenn ältere abgelaufen sind.</span><span class="sxs-lookup"><span data-stu-id="8cb93-142">Your app can get new access tokens as older ones expire.</span></span>

## <a name="authenticate-connection-requests"></a><span data-ttu-id="8cb93-143">Authentifizieren von Verbindungsanforderungen</span><span class="sxs-lookup"><span data-stu-id="8cb93-143">Authenticate connection requests</span></span>

<span data-ttu-id="8cb93-144">Sie können eine Verbindung mit Office 365 e-Mail-Servern mit den [IMAP-und Pop-e-Mail-Einstellungen für Office 365](https://support.office.com/article/pop-and-imap-email-settings-for-outlook-8361e398-8af4-4e97-b147-6c6c4ac95353)initiieren.</span><span class="sxs-lookup"><span data-stu-id="8cb93-144">You can initiate a connection to Office 365 mail servers using the [IMAP and POP email settings for Office 365](https://support.office.com/article/pop-and-imap-email-settings-for-outlook-8361e398-8af4-4e97-b147-6c6c4ac95353).</span></span>

### <a name="sasl-xoauth2"></a><span data-ttu-id="8cb93-145">SASL XOAUTH2</span><span class="sxs-lookup"><span data-stu-id="8cb93-145">SASL XOAUTH2</span></span>

<span data-ttu-id="8cb93-146">Für die OAuth-Integration mit muss Ihre Anwendung das SASL-XOAUTH2-Format für die Codierung und Übertragung des Zugriffstokens verwenden.</span><span class="sxs-lookup"><span data-stu-id="8cb93-146">OAuth integration with requires your application to use SASL XOAUTH2 format for encoding and transmitting the access token.</span></span> <span data-ttu-id="8cb93-147">SASL XOAUTH2 codiert den Benutzernamen und das Zugriffstoken in folgendem Format:</span><span class="sxs-lookup"><span data-stu-id="8cb93-147">SASL XOAUTH2 encodes the username, access token together in the following format:</span></span>

```text
base64("user=" + userName + "^Aauth=Bearer " + accessToken + "^A^A")
```

<span data-ttu-id="8cb93-148">`^A`stellt ein **Steuerelement**  +  **a** ( `%x01` ) dar.</span><span class="sxs-lookup"><span data-stu-id="8cb93-148">`^A` represents a **Control** + **A** (`%x01`).</span></span>

<span data-ttu-id="8cb93-149">Das SASL-XOAUTH2-Format für den Zugriff `test@contoso.onmicrosoft.com` mit Zugriffstoken `EwBAAl3BAAUFFpUAo7J3Ve0bjLBWZWCclRC3EoAA` lautet beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="8cb93-149">For example, the SASL XOAUTH2 format to access `test@contoso.onmicrosoft.com` with access token `EwBAAl3BAAUFFpUAo7J3Ve0bjLBWZWCclRC3EoAA` is:</span></span>

```text
base64("user=test@contoso.onmicrosoft.com^Aauth=Bearer EwBAAl3BAAUFFpUAo7J3Ve0bjLBWZWCclRC3EoAA^A^A")
```

<span data-ttu-id="8cb93-150">Nach Base64-Codierung wird dies in die folgende Zeichenfolge übersetzt.</span><span class="sxs-lookup"><span data-stu-id="8cb93-150">After base64 encoding, this translates to the following string.</span></span> <span data-ttu-id="8cb93-151">Beachten Sie, dass Zeilenumbrüche zur Lesbarkeit eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="8cb93-151">Note that line breaks are inserted for readability.</span></span>

```text
dXNlcj10ZXN0QGNvbnRvc28ub25taWNyb3NvZnQuY29tAWF1dGg9QmVhcmVy
IEV3QkFBbDNCQUFVRkZwVUFvN0ozVmUwYmpMQldaV0NjbFJDM0VvQUEBAQ==
```

### <a name="sasl-xoauth2-authentication-for-shared-mailboxes-in-office-365"></a><span data-ttu-id="8cb93-152">SASL XOAUTH2-Authentifizierung für freigegebene Postfächer in Office 365</span><span class="sxs-lookup"><span data-stu-id="8cb93-152">SASL XOAUTH2 authentication for shared mailboxes in Office 365</span></span>

<span data-ttu-id="8cb93-153">Für den Zugriff auf freigegebene Postfächer mithilfe von OAuth muss die Anwendung das Zugriffstoken im Namen eines Benutzers abrufen, aber das Benutzername-Feld in der codierten SASL XOAUTH2-Zeichenfolge durch die e-Mail-Adresse des freigegebenen Postfachs ersetzen.</span><span class="sxs-lookup"><span data-stu-id="8cb93-153">In case of shared mailbox access using OAuth, application needs to obtain the access token on behalf of a user but replace the userName field in the SASL XOAUTH2 encoded string with the email address of the shared mailbox.</span></span> 

### <a name="imap-protocol-exchange"></a><span data-ttu-id="8cb93-154">IMAP-Protokollaustausch</span><span class="sxs-lookup"><span data-stu-id="8cb93-154">IMAP Protocol Exchange</span></span>

<span data-ttu-id="8cb93-155">Damit eine IMAP-Serververbindung authentifiziert werden kann, muss der Client mit einem `AUTHENTICATE` Befehl im folgenden Format Antworten:</span><span class="sxs-lookup"><span data-stu-id="8cb93-155">To authenticate a IMAP server connection, the client will have to respond with an `AUTHENTICATE` command in the following format:</span></span>

```text
AUTHENTICATE XOAUTH2 <base64 string in XOAUTH2 format>
```

<span data-ttu-id="8cb93-156">Beispiel für einen Client-Server-Nachrichtenaustausch, der zu einem Authentifizierungs Erfolg führt:</span><span class="sxs-lookup"><span data-stu-id="8cb93-156">Sample client-server message exchange that results in an authentication success:</span></span>

```text
[connection begins]
C: C01 CAPABILITY
S: * CAPABILITY … AUTH=XOAUTH2
S: C01 OK Completed
C: A01 AUTHENTICATE XOAUTH2 dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlYXJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMjl0Q2cBAQ==
S: A01 OK AUTHENTICATE completed.
```

<span data-ttu-id="8cb93-157">Beispiel für einen Client-Server-Nachrichtenaustausch, der zu einem Authentifizierungsfehler führt:</span><span class="sxs-lookup"><span data-stu-id="8cb93-157">Sample client-server message exchange that results in an authentication failure:</span></span>

```text
[connection begins]
S: * CAPABILITY … AUTH=XOAUTH2
S: C01 OK Completed
C: A01 AUTHENTICATE XOAUTH2 dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlYXJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMjl0Q2cBAQ==
S: A01 NO AUTHENTICATE failed.
```

### <a name="pop-protocol-exchange"></a><span data-ttu-id="8cb93-158">Austausch von Pop-Protokollen</span><span class="sxs-lookup"><span data-stu-id="8cb93-158">POP Protocol Exchange</span></span>

<span data-ttu-id="8cb93-159">Zur Authentifizierung einer Pop-Serververbindung muss der Client mit einem Befehl Antworten, der `AUTH` in zwei Zeilen im folgenden Format aufgeteilt wird:</span><span class="sxs-lookup"><span data-stu-id="8cb93-159">To authenticate a POP server connection, the client will have to respond with an `AUTH` command split into two lines in the following format:</span></span>    

```text 
AUTH XOAUTH2 
<base64 string in XOAUTH2 format>   
``` 

<span data-ttu-id="8cb93-160">Beispiel für einen Client-Server-Nachrichtenaustausch, der zu einem Authentifizierungs Erfolg führt:</span><span class="sxs-lookup"><span data-stu-id="8cb93-160">Sample client-server message exchange that results in an authentication success:</span></span>    

```text 
[connection begins] 
C: AUTH XOAUTH2     
S: +    
C: dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlYX   
JlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMjl0  
Q2cBAQ==    
S: +OK User successfully authenticated. 
[connection continues...]   
``` 

<span data-ttu-id="8cb93-161">Beispiel für einen Client-Server-Nachrichtenaustausch, der zu einem Authentifizierungsfehler führt:</span><span class="sxs-lookup"><span data-stu-id="8cb93-161">Sample client-server message exchange that results in an authentication failure:</span></span>    

```text 
[connection begins] 
C: AUTH XOAUTH2     
S: +    
C: dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlY    
XJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMj   
l0Q2cBAQ=   
S: -ERR Authentication failure: unknown user name or bad password.  
```

### <a name="smtp-protocol-exchange"></a><span data-ttu-id="8cb93-162">SMTP-Protokollaustausch</span><span class="sxs-lookup"><span data-stu-id="8cb93-162">SMTP Protocol Exchange</span></span>

<span data-ttu-id="8cb93-163">Zur Authentifizierung einer SMTP-Serververbindung muss der Client mit einem `AUTH` Befehl im folgenden Format Antworten:</span><span class="sxs-lookup"><span data-stu-id="8cb93-163">To authenticate a SMTP server connection, the client will have to respond with an `AUTH` command in the following format:</span></span>

```text
AUTH XOAUTH2 <base64 string in XOAUTH2 format>
```

<span data-ttu-id="8cb93-164">Beispiel für einen Client-Server-Nachrichtenaustausch, der zu einem Authentifizierungs Erfolg führt:</span><span class="sxs-lookup"><span data-stu-id="8cb93-164">Sample client-server message exchange that results in an authentication success:</span></span>

```text
[connection begins]
C: auth xoauth2
S: 334
C: dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlY
XJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMj
l0Q2cBAQ==
S: 235 2.7.0 Authentication successful
[connection continues...]
```

<span data-ttu-id="8cb93-165">Beispiel für einen Client-Server-Nachrichtenaustausch, der zu einem Authentifizierungsfehler führt:</span><span class="sxs-lookup"><span data-stu-id="8cb93-165">Sample client-server message exchange that results in an authentication failure:</span></span>

```text
[connection begins]
C: auth xoauth2
S: 334
C: dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlY
XJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMj
l0Q2cBAQ==
S: 535 5.7.3 Authentication unsuccessful [SN2PR00CA0018.namprd00.prod.outlook.com]
```

## <a name="see-also"></a><span data-ttu-id="8cb93-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8cb93-166">See also</span></span>

- [<span data-ttu-id="8cb93-167">Authentifizierung und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="8cb93-167">Authentication and EWS in Exchange</span></span>](../exchange-web-services/authentication-and-ews-in-exchange.md)
- [<span data-ttu-id="8cb93-168">IMAP-, Pop-Verbindungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="8cb93-168">IMAP, POP Connection settings</span></span>](https://support.office.com/article/pop-and-imap-email-settings-for-outlook-8361e398-8af4-4e97-b147-6c6c4ac95353)
- [<span data-ttu-id="8cb93-169">Internet-Nachrichtenzugriffs Protokoll</span><span class="sxs-lookup"><span data-stu-id="8cb93-169">Internet Message Access Protocol</span></span>](https://tools.ietf.org/html/rfc3501)
- [<span data-ttu-id="8cb93-170">Post Office-Protokoll</span><span class="sxs-lookup"><span data-stu-id="8cb93-170">Post Office Protocol</span></span>](https://tools.ietf.org/html/rfc1081)
- [<span data-ttu-id="8cb93-171">SMTP-Diensterweiterung für die Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="8cb93-171">SMTP Service extension for Authentication</span></span>](https://tools.ietf.org/html/rfc4954)
