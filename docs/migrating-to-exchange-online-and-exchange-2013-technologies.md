---
title: Migrieren zu Exchange-Technologien
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 946a722f-0892-4a59-9e58-a291bfb6834a
description: Wenn Sie von einer früheren Version von Exchange migrieren, anhand der Informationen in diesem Artikel, um zu ermitteln, welche Entwicklungstechnologien im aktuellen Produktversionen unterstützt werden und welche Technologie zu migrieren.
ms.openlocfilehash: 82362b7bcdb79d6ca43603335d51a8bd8c1df239
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757168"
---
# <a name="migrating-to-exchange-technologies"></a>Migrieren zu Exchange-Technologien

Wenn Sie von einer früheren Version von Exchange migrieren, anhand der Informationen in diesem Artikel, um zu ermitteln, welche Entwicklungstechnologien im aktuellen Produktversionen unterstützt werden und welche Technologie zu migrieren.
  
## <a name="determine-if-your-technology-is-available-in-current-versions"></a>Bestimmen Sie, ob Ihre Technologie in den aktuellen Versionen verfügbar ist

Verwenden Sie in der folgenden Tabelle, um zu bestimmen, ob eine Development-Technologie im Exchange Online unterstützt wird oder Exchange 2013. Wenn die Technologie nicht unterstützt wird, finden Sie unter [Choose eine entwicklungstechnologie zu migrieren](#bk_choose).

<br/> 

**Exchange-Entwicklungstechnologien und Produktversionen**

|Technologie|Office 365 und Exchange Online|Exchange 2013|Exchange 2010|Exchange 2007|
|:-----|:-----:|:-----:|:-----:|:-----:|
|[Office 365-APIs Plattform (Übersicht)](http://msdn.microsoft.com/library/16fbf0c0-5470-466b-aab8-a0c9074c94e2%28Office.15%29.aspx) <br/> |X  <br/> ||||
|[EWS Managed API](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Exchange-Webdienste (EWS)](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Mail-apps für Outlook](exchange-web-services/mail-apps-for-outlook-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |||
|[Outlook-Objektmodell (OOM)](http://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Exchange-Verwaltungsshell](management/exchange-management-shell.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Sicherung und Wiederherstellung](backup-restore/backup-and-restore-for-exchange-2013.md) <br/> ||X  <br/> |X  <br/> |X  <br/> |
|[Transport-agents](transport-agents/transport-agents-in-exchange-2013.md) <br/> ||X  <br/> |X  <br/> |X  <br/> |
|Active Directory Services Interfaces (ADSI)  <br/> ||||X  <br/> |
|Collaboration Data Objects for Exchange (CDOEX)  <br/> ||||X  <br/> |
|Collaboration Data Objects für Windows 2000 (CDOSYS)  <br/> ||||X  <br/> |
|Exchange OLE DB-Anbieter (EXOLEDB)  <br/> ||||X  <br/> |
|Exchange-Speicher-Ereignisempfängern  <br/> ||||X  <br/> |
|Schrittweite Synchronisierung (ICS)  <br/> ||||X  <br/> |
|Lightweight Directory Access-Protokoll (LDAP)  <br/> ||||X  <br/> |
|[Messaging-API (MAPI)](http://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Outlook Web App-Anpassung  <br/> |||X  <br/> ||
|Web Distributed Authoring and Versioning (WebDAV)  <br/> ||||X  <br/> |

<a name="bk_choose"> </a>

## <a name="choose-a-development-technology-to-migrate-to"></a>Wählen Sie eine entwicklungstechnologie zu migrieren

Wenn die von die Anwendung verwendeten Technologie nicht unterstützt wird oder deemphasized im Exchange Online oder Exchange 2013, anhand der folgenden Tabelle entscheiden, welche Technologie zu migrieren.
  
**Empfohlene Technologie Migrationspfade**

|**Technologie**|**In Office 365, Exchange Online und Exchange 2013 unterstützt?**|**Migrieren zu**|**Weitere Informationen**|
|:-----|:-----|:-----|:-----|
|ADSI  <br/> |Ja, aber deemphasized <br/>|[Exchange-Verwaltungsshell](management/exchange-management-shell.md)<br/> |Keine.  <br/> |
|CDOEX  <br/> |Nein  <br/> |[EWS Managed API oder EWS](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |Die EWS Managed API und EWS können den gleichen Exchange-Speicher CDOEX bereitgestellten zugreifen. Im Gegensatz zu Clientanwendungen mithilfe von CDOEX erstellt können Sie EWS-Anwendungen auf einem Computer lokal oder remote ausführen.  <br/> |
|CDOEXM  <br/> |Nein <br/> |[Exchange-Verwaltungsshell](management/exchange-management-shell.md) <br/> |Exchange-Verwaltungsshell Befehle wird Exchange Server, Speichergruppen, Datenbanken und Benutzer einfacher als die entsprechende CDOEXM-APIs. Darüber hinaus Ihre Anwendung CDOEXM Exchange-Verwaltungsshell-Befehle können auf einfache Weise migriert werden.  <br/> |
|CDOSYS<br/> |Nein<br/> |[Transport-agents](transport-agents/transport-agents-in-exchange-2013.md)   <br/> |Verwenden Sie Transport-Agents für die Benachrichtigung-basierte Anwendungen, die Versionen von Exchange, beginnend mit Exchange 2010 entwickelt.<br/><br/> CDOSYS ist in den aktuellen Versionen von Windows enthalten. Die Funktionalität in CDOSYS steht in .NET Framework.  <br/> |
|CDOWF  <br/> |Nein  <br/> |[Windows Workflow Foundation (WWF)](http://msdn.microsoft.com/en-us/library/vstudio/ms735967%28v=vs.90%29.aspx) <br/> |WWF können Sie erweiterte workflowanwendungen erstellen, die mit Exchange 2007 arbeiten.   <br/> |
|ExOLEDB  <br/> |Nein  <br/> |[EWS Managed API oder EWS](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |Die EWS Managed API und EWS bieten den gleichen Zugriff auf die Exchange-Speicher, den ExOLEDB bereitstellt. Im Gegensatz zu Clientanwendungen mithilfe von ExOLEDB erstellt können Sie EWS-Anwendungen auf einem Computer lokal oder remote ausführen.  <br/> |
|ICS  <br/> |Ja, aber deemphasized  <br/> |EWS Managed API oder EWS<br/> |Sie können die EWS Managed API oder EWS [Abonnieren von Benachrichtigungen](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md) und [Synchronisieren von Postfachdaten](exchange-web-services/mailbox-synchronization-and-ews-in-exchange.md)verwenden.  <br/> |
|LDAP  <br/> |Ja, aber deemphasized  <br/> |[Exchange-Verwaltungsshell](management/exchange-management-shell.md) <br/> |Keine.  <br/> |
|MAPI  <br/> |Ja, aber deemphasized  <br/> |Office 365-APIs Plattform (Übersicht), EWS Managed API, Exchange-Webdienste <br/> |Obwohl MAPI derzeit unterstützte Development-Technologie ist, müssen Sie schließlich Umgestalten der MAPI-Anwendungen verwenden eine neuere Technologie.<br/><br/>Wenn die MAPI-Anwendung einfache lesen, schreiben und Aktualisierungsvorgänge auf e-Mail, Kalender, oder Contact-Objekte und Zielen Office 365 ausgeführt wird, können Sie die [Office 365-REST-APIs für e-Mail, Kalender und Kontakte](exchange-web-services/office-365-rest-apis-for-mail-calendars-and-contacts.md).<br/><br/>Wenn Sie verwenden lokale Exchange-Organisation Inhaltsadressierung und müssen Sie auf alle Eigenschaften zugreifen, die MAPI zugreifen kann, können Sie die EWS Managed API oder EWS und entweder [Schematisierte Eigenschaften oder erweiterte Eigenschaften](http://msdn.microsoft.com/library/68623048-060e-4602-b3fa-62617a94cf72%28Office.15%29.aspx).<br/><br/>**Hinweis**: die [ExtendedPropertyDefinition](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) -Klasse bietet Zugriff auf MAPI aus der EWS Managed API, und das [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) -Element bietet Zugriff zu MAPI-Eigenschaften von EWS.           |
|Outlook Web App-Anpassung  <br/> |Nein  <br/> |[Mail-apps](exchange-web-services/mail-apps-for-outlook-and-ews-in-exchange.md) <br/> |Keine.  <br/> |
|Store-Ereignisempfängern  <br/> |Nein  <br/> |EWS Managed API oder EWS <br/> |Sie können die EWS Managed API oder EWS [Abonnieren von Benachrichtigungen](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md) und [Synchronisieren von Postfachdaten](exchange-web-services/mailbox-synchronization-and-ews-in-exchange.md)verwenden.<br/><br/>Die Benachrichtigungen in EWS bieten dem gleichen Zugriff auf Exchange-Speicher, dass Store-Ereignisempfängern bereitstellen. Visual Studio-Tools können Sie um die Entwicklung von Store-Ereignis-fähigen-Clientanwendungen zu optimieren, die Exchange-Webdienste verwenden.  <br/> |
|Streaming-Sicherung und Wiederherstellung  <br/> |Nein  <br/> |[Volume Shadow Copy Service (VSS) writer](backup-restore/backup-and-restore-for-exchange-2013.md) <br/> |Keine.  <br/> |
|WebDAV  <br/> |Nein  <br/> |Office 365-APIs Plattform (Übersicht), EWS Managed API oder EWS <br/> |Wenn Ihre Anwendung WebDAV einfache lesen, schreiben und Aktualisierungsvorgänge auf e-Mail, Kalender oder Contact-Objekte führt, und Sie Office 365 abzielen, verwenden Sie die [Office 365-REST-APIs für e-Mail, Kalender und Kontakte](exchange-web-services/office-365-rest-apis-for-mail-calendars-and-contacts.md).<br/><br/>Andernfalls, wenn Sie verwenden lokale Exchange-Organisation Inhaltsadressierung, und Sie Zugriff auf die gleichen Eigenschaften im Exchange-Speicher benötigen, die WebDAV enthält, verwenden Sie die EWS Managed API oder EWS.  <br/> |
|WebDAV-Benachrichtigungen  <br/> |Nein  <br/> |EWS Managed API oder EWS<br/> |Der EWS Managed API oder EWS können [auf Benachrichtigungen](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md)abonnieren.  <br/> |
|Webformulare  <br/> |Nein  <br/> |[ASP.NET](http://www.asp.net/web-forms) <br/> |Wechseln Sie zu ASP.NET und Aktualisieren von Clientanwendungen auf Postfach-und Server mithilfe der Exchange-Webdienste zugreifen.  <br/> |
|WMI-Anbieter  <br/> |Nein  <br/> |[Exchange-Verwaltungsshell](management/exchange-management-shell.md) <br/> |None.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Auswählen einer API oder Technologie zum Entwickeln von Lösungen für Outlook](http://msdn.microsoft.com/library/01a46083-03d0-4333-920c-01a9f17f68cb%28Office.15%29.aspx)
    

