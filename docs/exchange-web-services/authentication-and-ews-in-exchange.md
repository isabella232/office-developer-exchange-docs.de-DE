---
title: Authentifizierung und EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9a83df96-aca0-42b3-b8f5-2b414f0363f1
description: Hier finden Sie Informationen, die Sie dabei unterstützen, den richtigen Authentifizierungsstandard für Ihre EWS-Anwendung für Exchange zu finden.
ms.openlocfilehash: a4aae4678f1d6ffa5c08350f0bcccce5a4885f20
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353665"
---
# <a name="authentication-and-ews-in-exchange"></a>Authentifizierung und EWS in Exchange

Hier finden Sie Informationen, die Sie dabei unterstützen, den richtigen Authentifizierungsstandard für Ihre EWS-Anwendung für Exchange zu finden.
  
Die Authentifizierung ist ein wichtiger Bestandteil Ihrer Exchange Web Services-Anwendung (EWS). Exchange Online, Exchange Online als Teil von Office 365 und lokale Versionen von Exchange ab Exchange Server 2013 unterstützen standardmäßige Webauthentifizierungsprotokolle, um die Sicherheit der Kommunikation zwischen Ihrer Anwendung und dem Exchange-Server zu gewährleisten.
  
Wenn Sie auf Exchange Online abzielen, muss die von Ihnen gewählte Authentifizierungsmethode HTTPS zum Verschlüsseln der Anforderungen und Antworten, die Ihre Anwendung sendet, verwenden. Auch wenn Sie auf lokalen Servern HTTP mit Exchange verwenden können, empfehlen wir die Verwendung von HTTPS für alle Anforderungen, die Ihre Anwendung an einen EWS-Endpunkt sendet, um auf diese Weise die Kommunikation zwischen der Anwendung und einem Exchange-Server zu sichern.
  
Exchange bietet die folgenden Authentifizierungsoptionen: 
  
- OAuth 2.0 (nur Exchange Online)
    
- NTLM (nur lokales Exchange)
    
- Standard (nicht mehr empfohlen)
    
Welche Authentifizierungsmethode Sie auswählen, hängt von den Sicherheitsanforderungen Ihres Unternehmens ab sowie davon, ob Sie Exchange Online oder lokales Exchange verwenden und ob Sie Zugriff auf einen Drittanbieter haben, der OAuth-Token ausstellen kann. In diesem Artikel finden Sie Informationen, die Sie bei der Auswahl des passenden Authentifizierungsstandard für Ihre Anwendung unterstützt.
  
## <a name="oauth-authentication"></a>OAuth-Authentifizierung

Wir empfehlen die Verwendung des OAuth-Standards für alle neuen Anwendungen, die sich mit Exchange Online-Diensten verbinden. Der Vorteil, den diese Authentifizierung im Vergleich zur Standardauthentifizierung bietet, rechtfertigt den zusätzlichen Aufwand, der zum Implementieren von OAuth in Ihre Anwendung notwendig ist. Beachten Sie hierbei jedoch auch, dass es durchaus einige Nachteile gibt.
  
**Tabelle 1. Vor- und Nachteile von OAuth**

|**Vorteile**|**Nachteile**|
|:-----|:-----|
| OAuth ist ein Authentifizierungsprotokoll nach Branchenstandard.<br/><br/>Die Authentifizierung wird durch einen Drittanbieter verwaltet. Ihre Anwendung muss keine Exchange-Anmeldeinformationen sammeln und speichern.<br/><br/>Hierum müssen Sie sich also nicht kümmern. Ihre Anwendung enthält nur ein verdecktes Token vom Authentifizierungsanbieter. Daher wird bei einer Sicherheitsverletzung nur das Token aufgedeckt, jedoch keine Exchange-Anmeldeinformationen des Benutzers.  <br/> | OAuth ist von einem Drittpartei-Authentifizierungsanbieter abhängig. Dies kann zusätzliche Kosten für Ihr Unternehmen oder Ihre Kunden verursachen.<br/><br/>Der OAuth-Standard ist schwieriger zu implementieren als die Standardauthentifizierung.<br/><br/>Um OAuth implementieren zu können, müssen Sie Ihre Anwendung sowohl mit dem Authentifizierungsanbieter als auch dem Exchange-Server integrieren.  <br/> |
   
Um die Nachteile zu minimieren, können Sie die [Microsoft Azure AD Authentication Library](https://docs.microsoft.com/de-DE/azure/active-directory/develop/active-directory-authentication-libraries) (ADAL) zum Authentifizieren von Benutzern bei den Active Directory Domain Services (AD DS) in der Cloud oder lokal verwenden und dann Zugriffstoken zum Sichern der Aufrufe an den Exchange-Server verwenden. Für Exchange Online sind vom Azure Active Directory-Dienst ausgegebene Token erforderlich, was von ADAL unterstützt wird. Sie können jedoch jede Drittanbieterbibliothek verwenden. 
  
Weitere Informationen über die Verwendung der OAuth-Authentifizierung in der EWS-Anwendung finden Sie in den folgenden Ressourcen:
  
- [Office 365-Testversion](https://docs.microsoft.com/de-DE/office/developer-program/office-365-developer-program) zum Einrichten eines Exchange-Servers zum Testen der Clientanwendung.
    
- [Azure AD Authentication Library für .NET](https://docs.microsoft.com/de-DE/azure/active-directory/develop/active-directory-authentication-libraries)
    
- [Konfigurieren von Azure Active Directory](http://msdn.microsoft.com/library/055e1155-2d4d-4c85-b44e-d406872ba595%28Office.15%29.aspx) zum Aktivieren Ihrer Anwendung für die Verwendung von OAuth-Tokens zur Authentifizierung.
    
- Beispielcode finden Sie unter [Authentifizieren einer EWS-Anwendung mit OAuth](how-to-authenticate-an-ews-application-by-using-oauth.md). 
    
## <a name="ntlm-authentication"></a>NTLM-Authentifizierung

Die NTLM-Authentifizierung ist nur für lokale Exchange-Server verfügbar. Für Anwendungen, die innerhalb der Unternehmensfirewall ausgeführt werden, bietet die Integration der NTLM-Authentifizierung und von .NET Framework eine integrierte Möglichkeit, Ihre Anwendung zu authentifizieren. 
  
**Tabelle 2. Vor- und Nachteile der NTLM-Authentifizierung**

|**Vorteile**|**Nachteile**|
|:-----|:-----|
| Ist sofort einsatzbereit zur Verwendung mit dem Exchange-Server. Sie können den Zugriff auf Exchange-Dienste konfigurieren, indem Sie ein [Exchange Management Shell-Cmdlet](how-to-control-access-to-ews-in-exchange.md) verwenden.  <br/><br/>Verwenden Sie das [CredentialCache](http://msdn2.microsoft.com/de-DE/library/615e0wsd)-Objekt von .NET Framework, um die Anmeldeinformationen des Benutzers automatisch abzurufen.<br/><br/>[Es sind Codebeispiele unter](http://code.msdn.microsoft.com/office/Exchange-2013-101-Code-3c38582c) verfügbar, die die Anmeldeinformationen des angemeldeten Benutzers für die Authentifizierung bei einem lokalen Exchange-Server verwenden.  <br/> | Benutzer müssen bei einer Domäne angemeldet sein, um die NTLM-Authentifizierung verwenden zu können.<br/><br/>Es kann schwierig sein, auf E-Mail-Konten zuzugreifen, die nicht dem Domänenkonto des Benutzers zugeordnet sind.<br/><br/>Dienstanwendungen müssen über ein Domänenkonto verfügen, um die NTLM-Authentifizierung nutzen zu können.  <br/> |
   
## <a name="basic-authentication"></a>Standardauthentifizierung

Die Standardauthentifizierung bietet eine grundlegende Sicherheitsebene für die Clientanwendung. Wir empfehlen, dass alle neue Anwendungen entweder NTLM oder das OAuth-Protokoll für die Authentifizierung verwenden. Die Standardauthentifizierung kann jedoch unter bestimmten Umständen die richtige Wahl für Ihre Anwendung sein.
  
**Tabelle 3. Vor- und Nachteile der Standardauthentifizierung**

|**Vorteile**|**Nachteile**|
|:-----|:-----|
| Ist sofort einsatzbereit zur Verwendung mit dem Exchange-Server. Sie können den Zugriff auf Exchange-Dienste konfigurieren, indem Sie ein [Exchange Management Shell-Cmdlet](how-to-control-access-to-ews-in-exchange.md) verwenden.  <br/><br/>Windows-Anwendungen können die standardmäßigen Anmeldeinformationen des angemeldeten Benutzers verwenden.<br/><br/>Es stehen [zahlreiche Codebeispiele zur Verfügung](http://code.msdn.microsoft.com/office/Exchange-2013-101-Code-3c38582c), die demonstrieren, wie Sie EWS mit Standardauthentifizierung aufrufen.  <br/> | Macht das Erfassen und Speichern der Anmeldeinformationen des Benutzers durch die Anwendung erforderlich.<br/><br/>Sie müssen die NTLM-Authentifizierung für alle Benutzer deaktivieren, um die Standardauthentifizierung verwenden zu können.<br/><br/>Wenn in Ihrer Anwendung eine Sicherheitsverletzung auftritt, kann dies die E-Mail-Adresse und das Kennwort des Benutzers für den Angreifer offenlegen.  <br/> |
   
Sie müssen entscheiden, ob die Standardauthentifizierung die Sicherheitsanforderungen Ihrer Organisation und Ihrer Kunden erfüllt. Die Standardauthentifizierung kann die richtige Wahl sein, wenn Sie umfangreiche Einrichtungsmaßnahmen vermeiden möchten, wenn Sie Anwendungen zum Beispiel nur zu Test- oder Demonstrationszwecken verwenden möchten.
  
## <a name="see-also"></a>Siehe auch

- [Verwenden von Webdiensten in Exchange](start-using-web-services-in-exchange.md)   
- [Hinzufügen von Anmeldungen zur Webanwendung mit Microsoft Azure AD](http://msdn.microsoft.com/library/055e1155-2d4d-4c85-b44e-d406872ba595%28Office.15%29.aspx)    
- [Steuern des Zugriffs auf EWS in Exchange](how-to-control-access-to-ews-in-exchange.md)    
- [Steuern des Clientanwendungszugriffs auf EWS in Exchange](controlling-client-application-access-to-ews-in-exchange.md)    
- [Unterstützte Token- und Anspruchstypen](http://msdn.microsoft.com/library/9d35e4bc-7b72-49d1-b723-5464eee6be2c%28Office.15%29.aspx)
    

