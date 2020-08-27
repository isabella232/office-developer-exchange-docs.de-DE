---
title: Authentifizieren einer IMAP-, Pop-oder SMTP-Verbindung mit OAuth
description: Erfahren Sie, wie Sie die OAuth-Authentifizierung mit ihren IMAP-, Pop-und SMTP-Anwendungen verwenden.
author: svpsiva
ms.date: 02/19/2020
ms.audience: Developer
ms.openlocfilehash: e1bef8e35d78c35693dadc94b24b6aeecaf4e439
ms.sourcegitcommit: 636c05a929279812c6ef87d75b01c166a4a05584
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2020
ms.locfileid: "47254986"
---
# <a name="authenticate-an-imap-pop-or-smtp-connection-using-oauth"></a>Authentifizieren einer IMAP-, Pop-oder SMTP-Verbindung mit OAuth

Erfahren Sie, wie Sie mit der OAuth-Authentifizierung eine Verbindung mit IMAP-, Pop-oder SMTP-Protokollen herstellen und auf e-Mail-Daten für Office 365 Benutzer zugreifen.

> Die OAuth2-Unterstützung für IMAP-, Pop-und SMTP-Protokolle wie unten beschrieben wird sowohl für Microsoft 365 (einschließlich Office im Internet) als auch für Outlook.com-Benutzer unterstützt.

Wenn Sie mit OAuth 2,0 nicht vertraut sind, lesen Sie zunächst die [Microsoft Identity Platform (v 2.0)-Übersicht](/azure/active-directory/develop/v2-overview). In diesem Dokument werden verschiedene Komponenten der Microsoft Identity-Plattform vorgestellt, einschließlich SDKs.

Sie können den von Azure Active Directory bereitgestellten OAuth-Authentifizierungsdienst verwenden, um Ihrer Anwendung die Verbindung mit IMAP-, Pop-oder SMTP-Protokollen für den Zugriff auf Exchange Online in Office 365 zu ermöglichen. Um OAuth mit Ihrer Anwendung zu verwenden, müssen Sie Folgendes tun:

1. [Registrieren Sie Ihre Anwendung](#register-your-application) mit Azure Active Directory.
1. [Konfigurieren Sie Ihre Anwendung](#configure-your-application) in Azure Active Directory.
1. [Rufen Sie ein Zugriffstoken](#get-an-access-token) von einem tokenserver ab.
1. [Authentifizierung von Verbindungsanforderungen](#authenticate-connection-requests) mit einem Zugriffstoken.

## <a name="register-your-application"></a>Registrieren Ihrer Anwendung

Um OAuth verwenden zu können, muss eine Anwendung mit Azure Active Directory registriert sein.

Befolgen Sie die Anweisungen unter [Registrieren einer Anwendung mit der Microsoft Identity-Plattform](/azure/active-directory/develop/quickstart-register-app) , um eine neue Anwendung zu erstellen.

## <a name="configure-your-application"></a>Konfigurieren der Anwendung

Befolgen Sie die Anweisungen unter [Konfigurieren einer Clientanwendung für den Zugriff auf webapin](/azure/active-directory/develop/quickstart-configure-app-access-web-apis) aufgeführt.

Stellen Sie sicher, dass Sie mindestens einen der folgenden Berechtigungs Bereiche hinzufügen, die den Protokollen entsprechen, die Sie integrieren möchten. Wählen Sie im Assistenten zum **Hinzufügen** von Berechtigungen **Microsoft Graph** und dann **Delegierte Berechtigungen** aus, um die folgenden Berechtigungs Bereiche zu finden.

| Protokoll  | Berechtigungsbereich        |
|-----------|-------------------------|
| IMAP      | `IMAP.AccessAsUser.All` |
| POP       | `POP.AccessAsUser.All`  |
| SMTP-Authentifizierung | `SMTP.Send`             |

## <a name="get-an-access-token"></a>Abrufen eines Zugriffstokens

Sie können eine unserer MSAL- [Clientbibliotheken](/azure/active-directory/develop/msal-overview) verwenden, um ein Zugriffstoken aus Ihrer Clientanwendung abzurufen.

Alternativ können Sie einen geeigneten Fluss aus der folgenden Liste auswählen und die entsprechenden Schritte ausführen, um die zugrunde liegenden Identity Platform-Rest-APIs aufzurufen und ein Zugriffstoken abzurufen.

1. [OAuth2-Autorisierungscode Fluss](/azure/active-directory/develop/v2-oauth2-auth-code-flow)
1. [OAuth2-Zuteilungs Fluss für Geräteautorisierung](/azure/active-directory/develop/v2-oauth2-device-code)

OAuth-Zugriff auf IMAP-, Pop-, SMTP-AUTH-Protokolle über OAuth2-Clientanmeldeinformationen Grant Flow wird nicht unterstützt. Wenn Ihre Anwendung beständigen Zugriff auf alle Postfächer in einer Microsoft 365-Organisation benötigt, wird empfohlen, dass Sie die Microsoft Graph-APIs verwenden, die den Zugriff ohne Benutzer erlauben, granulare Berechtigungen aktivieren und Administratoren den Zugriff auf bestimmte Postfächer gewähren lassen.

Stellen Sie sicher, dass Sie die vollständigen Bereiche angeben, einschließlich der Outlook-Ressourcen-URLs, wenn Sie Ihre Anwendung autorisieren und ein Zugriffstoken anfordern.

| Protokoll  | Zeichenfolge für Berechtigungs Bereiche |
|-----------|-------------------------|
| IMAP      | `https://outlook.office.com/IMAP.AccessAsUser.All` |
| POP       | `https://outlook.office.com/POP.AccessAsUser.All`  |
| SMTP-Authentifizierung | `https://outlook.office.com/SMTP.Send`             |

Darüber hinaus können Sie [offline_access](/azure/active-directory/develop/v2-permissions-and-consent#offline_access) Bereich anfordern. Wenn ein Benutzer den offline_access Bereich genehmigt, kann die APP Aktualisierungstoken vom Microsoft Identity Platform-Token-Endpunkt empfangen. Aktualisierungstoken sind langlebig. Ihre APP kann neue Zugriffstoken erhalten, wenn ältere abgelaufen sind.

## <a name="authenticate-connection-requests"></a>Authentifizieren von Verbindungsanforderungen

Sie können eine Verbindung mit Office 365 e-Mail-Servern mit den [IMAP-und Pop-e-Mail-Einstellungen für Office 365](https://support.office.com/article/pop-and-imap-email-settings-for-outlook-8361e398-8af4-4e97-b147-6c6c4ac95353)initiieren.

### <a name="sasl-xoauth2"></a>SASL XOAUTH2

Für die OAuth-Integration mit muss Ihre Anwendung das SASL-XOAUTH2-Format für die Codierung und Übertragung des Zugriffstokens verwenden. SASL XOAUTH2 codiert den Benutzernamen und das Zugriffstoken in folgendem Format:

```text
base64("user=" + userName + "^Aauth=Bearer " + accessToken + "^A^A")
```

`^A`stellt ein **Steuerelement**  +  **a** ( `%x01` ) dar.

Das SASL-XOAUTH2-Format für den Zugriff `test@contoso.onmicrosoft.com` mit Zugriffstoken `EwBAAl3BAAUFFpUAo7J3Ve0bjLBWZWCclRC3EoAA` lautet beispielsweise:

```text
base64("user=test@contoso.onmicrosoft.com^Aauth=Bearer EwBAAl3BAAUFFpUAo7J3Ve0bjLBWZWCclRC3EoAA^A^A")
```

Nach Base64-Codierung wird dies in die folgende Zeichenfolge übersetzt. Beachten Sie, dass Zeilenumbrüche zur Lesbarkeit eingefügt werden.

```text
dXNlcj10ZXN0QGNvbnRvc28ub25taWNyb3NvZnQuY29tAWF1dGg9QmVhcmVy
IEV3QkFBbDNCQUFVRkZwVUFvN0ozVmUwYmpMQldaV0NjbFJDM0VvQUEBAQ==
```

### <a name="sasl-xoauth2-authentication-for-shared-mailboxes-in-office-365"></a>SASL XOAUTH2-Authentifizierung für freigegebene Postfächer in Office 365

Für den Zugriff auf freigegebene Postfächer mithilfe von OAuth muss die Anwendung das Zugriffstoken im Namen eines Benutzers abrufen, aber das Benutzername-Feld in der codierten SASL XOAUTH2-Zeichenfolge durch die e-Mail-Adresse des freigegebenen Postfachs ersetzen. 

### <a name="imap-protocol-exchange"></a>IMAP-Protokollaustausch

Damit eine IMAP-Serververbindung authentifiziert werden kann, muss der Client mit einem `AUTHENTICATE` Befehl im folgenden Format Antworten:

```text
AUTHENTICATE XOAUTH2 <base64 string in XOAUTH2 format>
```

Beispiel für einen Client-Server-Nachrichtenaustausch, der zu einem Authentifizierungs Erfolg führt:

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

### <a name="pop-protocol-exchange"></a>Austausch von Pop-Protokollen

Zur Authentifizierung einer Pop-Serververbindung muss der Client mit einem Befehl Antworten, der `AUTH` in zwei Zeilen im folgenden Format aufgeteilt wird:    

```text 
AUTH XOAUTH2 
<base64 string in XOAUTH2 format>   
``` 

Beispiel für einen Client-Server-Nachrichtenaustausch, der zu einem Authentifizierungs Erfolg führt:    

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

### <a name="smtp-protocol-exchange"></a>SMTP-Protokollaustausch

Zur Authentifizierung einer SMTP-Serververbindung muss der Client mit einem `AUTH` Befehl im folgenden Format Antworten:

```text
AUTH XOAUTH2 <base64 string in XOAUTH2 format>
```

Beispiel für einen Client-Server-Nachrichtenaustausch, der zu einem Authentifizierungs Erfolg führt:

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
- [IMAP-, Pop-Verbindungseinstellungen](https://support.office.com/article/pop-and-imap-email-settings-for-outlook-8361e398-8af4-4e97-b147-6c6c4ac95353)
- [Internet-Nachrichtenzugriffs Protokoll](https://tools.ietf.org/html/rfc3501)
- [Post Office-Protokoll](https://tools.ietf.org/html/rfc1081)
- [SMTP-Diensterweiterung für die Authentifizierung](https://tools.ietf.org/html/rfc4954)
