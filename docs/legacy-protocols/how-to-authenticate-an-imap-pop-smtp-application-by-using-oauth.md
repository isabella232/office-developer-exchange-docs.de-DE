---
title: Authentifizieren einer IMAP-, POP- oder SMTP-Verbindung mithilfe von OAuth
description: Erfahren Sie, wie Sie die OAuth-Authentifizierung mit Ihren IMAP-, POP- und SMTP-Anwendungen verwenden.
author: svpsiva
ms.date: 07/08/2021
ms.audience: Developer
ms.openlocfilehash: cfc9de18a53ce4cfdd8535f26fe3b04aab9cde55
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531323"
---
# <a name="authenticate-an-imap-pop-or-smtp-connection-using-oauth"></a>Authentifizieren einer IMAP-, POP- oder SMTP-Verbindung mithilfe von OAuth

Erfahren Sie, wie Sie die OAuth-Authentifizierung verwenden, um eine Verbindung mit IMAP-, POP- oder SMTP-Protokollen herzustellen und auf E-Mail-Daten für Office 365 Benutzer zuzugreifen.

> OAuth2-Unterstützung für IMAP-, POP- und SMTP-Protokolle wie unten beschrieben wird sowohl für Microsoft 365 (einschließlich Office im Web) als auch für Outlook.com-Benutzer unterstützt.

Wenn Sie mit dem OAuth 2.0-Protokoll nicht vertraut sind, lesen Sie zunächst das [OAuth 2.0-Protokoll auf Microsoft Identity Platform Übersicht.](/azure/active-directory/develop/active-directory-v2-protocols) Weitere Informationen zu den Microsoft Authentication Libraries (MSAL), die das OAuth 2.0-Protokoll implementieren, um Benutzer zu authentifizieren und auf sichere APIs zuzugreifen, finden Sie in der [MSAL-Übersicht.](/azure/active-directory/develop/msal-overview)

Sie können den von Azure Active Directory bereitgestellten OAuth-Authentifizierungsdienst verwenden, damit Ihre Anwendung eine Verbindung mit IMAP-, POP- oder SMTP-Protokollen herstellen kann, um auf Exchange Online in Office 365 zuzugreifen. Um OAuth mit Ihrer Anwendung zu verwenden, müssen Sie Folgendes ausführen:

1. [Registrieren Sie Ihre Anwendung](#register-your-application) bei Azure Active Directory.
1. [Konfigurieren Sie Ihre Anwendung](#configure-your-application) in Azure Active Directory.
1. [Rufen Sie ein Zugriffstoken](#get-an-access-token) von einem Tokenserver ab.
1. [Authentifizieren von Verbindungsanforderungen](#authenticate-connection-requests) mit einem Zugriffstoken.

## <a name="register-your-application"></a>Registrieren der App

Um OAuth verwenden zu können, muss eine Anwendung bei Azure Active Directory registriert werden.

Folgen Sie den Anweisungen unter [Registrieren einer Anwendung mit dem Microsoft Identity Platform,](/azure/active-directory/develop/quickstart-register-app) um eine neue Anwendung zu erstellen.

## <a name="get-an-access-token"></a>Abrufen eines Zugriffstokens

Sie können eine unserer [MSAL-Clientbibliotheken](/azure/active-directory/develop/msal-overview) verwenden, um ein Zugriffstoken von Ihrer Clientanwendung abzurufen.

Alternativ können Sie einen geeigneten Fluss aus der folgenden Liste auswählen und die entsprechenden Schritte ausführen, um die zugrunde liegenden Identitätsplattform-REST-APIs aufzurufen und ein Zugriffstoken abzurufen.

1. [OAuth2-Autorisierungscodefluss](/azure/active-directory/develop/v2-oauth2-auth-code-flow)
1. [OAuth2-Geräte-Autorisierungsgenehmigungsfluss](/azure/active-directory/develop/v2-oauth2-device-code)

Der OAuth-Zugriff auf IMAP-, POP- und SMTP-AUTH-Protokolle über den Fluss zur Gewährung von OAuth2-Clientanmeldeinformationen wird nicht unterstützt. Wenn Ihre Anwendung beständigen Zugriff auf alle Postfächer in einer Microsoft 365 Organisation benötigt, wird empfohlen, dass Sie die Microsoft Graph-APIs verwenden, die den Zugriff ohne Benutzer ermöglichen, granulare Berechtigungen aktivieren und Administratoren den Zugriff auf einen bestimmten Satz von Postfächern gestatten.

Achten Sie darauf, die vollständigen Bereiche, einschließlich Outlook Ressourcen-URLs, anzugeben, wenn Sie Ihre Anwendung autorisieren und ein Zugriffstoken anfordern.

| Protokoll  | Berechtigungsbereichszeichenfolge |
|-----------|-------------------------|
| IMAP      | `https://outlook.office.com/IMAP.AccessAsUser.All` |
| POP       | `https://outlook.office.com/POP.AccessAsUser.All`  |
| SMTP AUTH | `https://outlook.office.com/SMTP.Send`             |

Darüber hinaus können Sie [offline_access](/azure/active-directory/develop/v2-permissions-and-consent#offline_access) Bereich anfordern. Wenn ein Benutzer den offline_access Bereich genehmigt, kann Ihre App Aktualisierungstoken vom Microsoft Identity Platform Tokenendpunkt empfangen. Aktualisierungstoken sind langlebig. Ihre App kann neue Zugriffstoken abrufen, da ältere Ablauftoken ablaufen.

## <a name="authenticate-connection-requests"></a>Authentifizieren von Verbindungsanforderungen

Sie können eine Verbindung mit Office 365 E-Mail-Servern mithilfe der [IMAP- und POP-E-Mail-Einstellungen für Office 365](https://support.office.com/article/pop-and-imap-email-settings-for-outlook-8361e398-8af4-4e97-b147-6c6c4ac95353)initiieren.

### <a name="sasl-xoauth2"></a>SASL XOAUTH2

Die OAuth-Integration erfordert, dass Ihre Anwendung das SASL XOAUTH2-Format zum Codieren und Übertragen des Zugriffstokens verwendet. SASL XOAUTH2 codiert den Benutzernamen, zugriffstoken zusammen im folgenden Format:

```text
base64("user=" + userName + "^Aauth=Bearer " + accessToken + "^A^A")
```

`^A`stellt ein **Steuerelement**  +  **A** ( `%x01` ) dar.

Beispielsweise lautet das SASL XOAUTH2-Format für den Zugriff `test@contoso.onmicrosoft.com` mit zugriffstoken `EwBAAl3BAAUFFpUAo7J3Ve0bjLBWZWCclRC3EoAA` wie folgt:

```text
base64("user=test@contoso.onmicrosoft.com^Aauth=Bearer EwBAAl3BAAUFFpUAo7J3Ve0bjLBWZWCclRC3EoAA^A^A")
```

Nach der Base64-Codierung wird dies in die folgende Zeichenfolge übersetzt. Beachten Sie, dass Zur besseren Lesbarkeit Zeilenumbrüche eingefügt werden.

```text
dXNlcj10ZXN0QGNvbnRvc28ub25taWNyb3NvZnQuY29tAWF1dGg9QmVhcmVy
IEV3QkFBbDNCQUFVRkZwVUFvN0ozVmUwYmpMQldaV0NjbFJDM0VvQUEBAQ==
```

### <a name="sasl-xoauth2-authentication-for-shared-mailboxes-in-office-365"></a>SASL XOAUTH2-Authentifizierung für freigegebene Postfächer in Office 365

Im Fall des freigegebenen Postfachzugriffs mit OAuth muss die Anwendung das Zugriffstoken im Namen eines Benutzers abrufen, aber das Feld "userName" in der SASL XOAUTH2-codierten Zeichenfolge durch die E-Mail-Adresse des freigegebenen Postfachs ersetzen. 

### <a name="imap-protocol-exchange"></a>IMAP-Protokoll Exchange

Um eine IMAP-Serververbindung zu authentifizieren, muss der Client mit einem `AUTHENTICATE` Befehl im folgenden Format antworten:

```text
AUTHENTICATE XOAUTH2 <base64 string in XOAUTH2 format>
```

Beispiel für einen Client-Server-Nachrichtenaustausch, der zu einem Erfolg der Authentifizierung führt:

```text
[connection begins]
C: C01 CAPABILITY
S: * CAPABILITY … AUTH=XOAUTH2
S: C01 OK Completed
C: A01 AUTHENTICATE XOAUTH2 dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlYXJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMjl0Q2cBAQ==
S: A01 OK AUTHENTICATE completed.
```

Beispiel für einen Client-Server-Nachrichtenaustausch, der zu einem Authentifizierungsfehler führt:

```text
[connection begins]
S: * CAPABILITY … AUTH=XOAUTH2
S: C01 OK Completed
C: A01 AUTHENTICATE XOAUTH2 dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlYXJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMjl0Q2cBAQ==
S: A01 NO AUTHENTICATE failed.
```

### <a name="pop-protocol-exchange"></a>POP-Protokoll Exchange

Um eine POP-Serververbindung zu authentifizieren, muss der Client mit einem Befehl antworten, `AUTH` der in zwei Zeilen im folgenden Format aufgeteilt ist:    

```text 
AUTH XOAUTH2 
<base64 string in XOAUTH2 format>   
``` 

Beispiel für einen Client-Server-Nachrichtenaustausch, der zu einem Erfolg der Authentifizierung führt:    

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

Beispiel für einen Client-Server-Nachrichtenaustausch, der zu einem Authentifizierungsfehler führt:    

```text 
[connection begins] 
C: AUTH XOAUTH2     
S: +    
C: dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlY    
XJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMj   
l0Q2cBAQ=   
S: -ERR Authentication failure: unknown user name or bad password.  
```

### <a name="smtp-protocol-exchange"></a>SMTP-Protokoll Exchange

Um eine SMTP-Serververbindung zu authentifizieren, muss der Client mit einem `AUTH` Befehl im folgenden Format antworten:

```text
AUTH XOAUTH2 <base64 string in XOAUTH2 format>
```

Beispiel für einen Client-Server-Nachrichtenaustausch, der zu einem Erfolg der Authentifizierung führt:

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

Beispiel für einen Client-Server-Nachrichtenaustausch, der zu einem Authentifizierungsfehler führt:

```text
[connection begins]
C: auth xoauth2
S: 334
C: dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlY
XJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMj
l0Q2cBAQ==
S: 535 5.7.3 Authentication unsuccessful [SN2PR00CA0018.namprd00.prod.outlook.com]
```

## <a name="see-also"></a>Siehe auch

- [Authentifizierung und EWS in Exchange](../exchange-web-services/authentication-and-ews-in-exchange.md)
- [IMAP- und POP-Verbindungseinstellungen](https://support.office.com/article/pop-and-imap-email-settings-for-outlook-8361e398-8af4-4e97-b147-6c6c4ac95353)
- [Internet Message Access Protocol](https://tools.ietf.org/html/rfc3501)
- [Post Office Protocol](https://tools.ietf.org/html/rfc1081)
- [SMTP-Diensterweiterung für die Authentifizierung](https://tools.ietf.org/html/rfc4954)
