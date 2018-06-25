---
title: Exchange Online und Exchange-Entwicklung
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: f33d1093-75ba-4ff2-8d15-b0bf73a401bf
description: Sie finden eine ausführliche Entwicklerdokumentation für Exchange Server, einschließlich Exchange Online als Teil von Office 365, Exchange Online, Exchange 2013, Verwaltete EWS-API, Exchange 2010 und Exchange 2007.
ms.openlocfilehash: b933bd1bdc6dfcbe4941f23dbee9a587745c7bd7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756819"
---
# <a name="exchange-online-and-exchange-development"></a>Exchange Online und Exchange-Entwicklung

Sie finden eine ausführliche Entwicklerdokumentation für Exchange Server, einschließlich Exchange Online als Teil von Office 365, Exchange Online, Exchange 2013, Verwaltete EWS-API, Exchange 2010 und Exchange 2007. 

Sie können How to verwenden, erste Schritte, neue Features und API-Referenzdokumentation zum Entwickeln von Tools zum Zugriff auf und Verwaltung von Postfachdaten aus Dienste, Websites, Desktopcomputern und mobilen Geräten, und zum Erstellen von benutzerdefinierter Lösungen für e-Mail, Kalender, Kontakte, und andere Elemente, die in Exchange Online oder auf einem Exchange 2013-Server gespeichert sind. 

Sie können Exchange-Webdienste, AutoErmittlung, E-Mail-Apps für Office oder andere APIs zum Entwickeln Ihrer Anwendungen verwenden. Auf dieser Seite können Sie die Auswahl des richtigen Exchange-Technologie.

## <a name="exchange-developer-content"></a>Exchange Developer content  

Verwenden Sie die folgende Tabelle, um die Technologie und verwandte API-Inhalte zu identifizieren, die Ihnen helfen, Ihre Entwicklungsziele zu erreichen.  
  
|Wenn Sie Folgendes erstellen…|Starten Sie hier|
|:-----|:-----|
|Eine REST-basierte app auf Exchange Online als Teil von Office 365|[Office 365-REST-APIs für E-Mail, Kalender und Kontakte](exchange-web-services/office-365-rest-apis-for-mail-calendars-and-contacts.md) |
|Eine kontextabhängige app zum Anzeigen von Informationen in Outlook, Outlook Web App oder OWA für Geräte |[Mail-Apps für Outlook und EWS in Exchange](exchange-web-services/mail-apps-for-outlook-and-ews-in-exchange.md) |
|Ein postfachclient, der nicht auf .NET Framework oder Java basiert |[Erkunden von verwalteter EWS-API, EWS und Webdiensten in Exchange](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) |
|Ein postfachclient, der .NET Framework wird verwendet, um die Exchange-Webdienste zugreifen |[Erste Schritte mit verwalteten EWS-API-Clientanwendungen](exchange-web-services/get-started-with-ews-managed-api-client-applications.md) |
|Ein postfachclient, der Java wird verwendet, um die Exchange-Webdienste zugreifen |[EWS Java API auf GitHub](https://github.com/OfficeDev/ews-java-api) |
|Eine Anwendung, die Outlook-Benutzeroberfläche angepasst oder nutzt die Outlook-Geschäftslogik  |[Outlook VBA-Referenz](https://msdn.microsoft.com/en-us/VBA/VBA-Outlook) |
|Eine Anwendung für Exchange Online oder Exchange 2013, die Sie zum Migrieren von einer früheren Version von Exchange benötigen  |[Migration zu Exchange-Technologien](migrating-to-exchange-online-and-exchange-2013-technologies.md) |
|Ein benutzerdefiniertes Verwaltungstool, das mithilfe von Windows PowerShell aus verwaltetem code   |[Exchange-Verwaltungsshell](management/exchange-management-shell.md) |
|Eine Lösung zum Sichern oder Wiederherstellen von Exchange-Daten  |[Sicherung und Wiederherstellung für Exchange](backup-restore/backup-and-restore-for-exchange-2013.md) |
|Eine Erweiterung, um den Zugriff auf Meldungen in der Transportpipeline zu unterstützen   |[Transport-Agents in Exchange](transport-agents/transport-agents-in-exchange-2013.md)  |
|Ein postfachclient für ein mobiles Gerät   |[Exchange ActiveSync](https://technet.microsoft.com/en-us/library/aa998357.aspx) |
   
## <a name="exchange-interactions-with-custom-applications"></a>Exchange-Interaktionen mit benutzerdefinierten Anwendungen

Einige dieser Technologien ermöglichen Ihren Anwendungen, mit in Exchange gespeicherten Daten zu arbeiten, und andere werden verwendet, um den Exchange-Server zu verwalten und zu steuern. In vielen Fällen können Sie mehr als eine Programmiertechnik oder -sprache verwenden, um eine Aufgabe auszuführen, wodurch Sie die Technologien und Sprachen verwenden können, mit denen Sie sich auskennen.Sie können zum Beispiel Eigenschaften auf Elementen im Exchange-Speicher festlegen, indem Sie Mail REST API, EWS oder Verwaltete EWS-API verwenden.
  
Exchange interagiert mit benutzerdefinierten Anwendungen je nach Anwendungsarchitektur und Funktion auf verschiedene Arten. Exchange leitet Nachrichten nicht nur weiter, sondern pflegt auch Posteingänge, führt formularbasierte Anwendungen aus, usw.

|Interaktion mit Exchange|Beschreibung|
|:-----|:-----|
|**Nachrichtentransport**|Exchange dient als Standard-E-Mailserver für Anwendungen, die Nachrichten versenden.<br/>Exchange enthält verschiedene APIs, die Nachrichten weiterleiten, einschließlich REST, EWS und Verwaltete EWS-API.<br/>Zudem können Anwendungen Transportagenten für die Beantwortung verwenden, wenn Nachrichten verarbeitet und von Exchange bereitgestellt werden. |
|**Postfachspeicher** |Exchange bietet eine hierarchische Struktur aus Ordnern, Elementen und Eigenschaften für Anwendungen, die auf in Postfächern gespeicherte Daten zugreifen.<br/>Sie können auf diese gespeicherten Informationen zugreifen, indem Sie eine Kombination aus Datenbank und Komponentenobjektstilen verwenden.<br/>Sie können Abfragen auf den Daten durchführen, und Exchange verwaltet den Zugriff auf die gespeicherten Daten auf Grundlage der Benutzer- und Speicherberechtigungen.<br/>Anwendungen, die Postfachdaten verarbeiten, verwenden normalerweise REST, EWS oder Verwaltete EWS-API.|
|**Verwaltete Enterprise server** |Exchange dient als verwalteter Server für Anwendungen, die Exchange-Server und -speicher verwenden.<br/>Anwendungen können aktuelle Aktivitäten sowie den Zustand von Exchange-Servern in der Organisation konfigurieren, steuern und überwachen.<br/>Exchange -Verwaltungsanwendungen verwenden Exchange-Verwaltungsshell für die Verwaltung von Exchange-Servern. |
   
## <a name="see-also"></a>Siehe auch

- [Für Exchange Server-API-Referenz](https://msdn.microsoft.com/en-us/library/dn186243(v=exchg.150).aspx)
- [Informationen zu Exchange auf Office Blogs](https://www.microsoft.com/en-us/microsoft-365/blog/) 
- [101 Codebeispiele für Exchange 2013 abrufen](https://code.msdn.microsoft.com/office/Exchange-2013-101-Code-3c38582c)
- [Abrufen der verwalteten EWS-API (GitHub)](https://github.com/OfficeDev/ews-managed-api/blob/master/README.md)
- [Support für Exchange Server anfordern](https://support.microsoft.com/en-us/getsupport?oaspworkflow=start_1.0.0.0&wf=0&wfname=productselection&gprid=730&x=13&y=7&st=1&wfxredirect=1&sd=gn&ccsid=635890984021344661&forceorigin=esmc)


