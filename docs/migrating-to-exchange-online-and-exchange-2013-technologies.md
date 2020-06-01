---
title: Migration zu Exchange-Technologien
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 946a722f-0892-4a59-9e58-a291bfb6834a
description: Wenn Sie von einer früheren Version von Exchange migrieren, verwenden Sie die Informationen in diesem Artikel, um herauszufinden, welche Entwicklungstechnologien in den aktuellen Produktversionen unterstützt werden und welche Technologie migriert werden soll.
ms.openlocfilehash: d82f1b305fd1cc30e48cddbf9bf2981d3d829a5c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459153"
---
# <a name="migrating-to-exchange-technologies"></a>Migration zu Exchange-Technologien

Wenn Sie von einer früheren Version von Exchange migrieren, verwenden Sie die Informationen in diesem Artikel, um herauszufinden, welche Entwicklungstechnologien in den aktuellen Produktversionen unterstützt werden und welche Technologie migriert werden soll.
  
## <a name="determine-if-your-technology-is-available-in-current-versions"></a>Ermitteln, ob Ihre Technologie in aktuellen Versionen verfügbar ist

Verwenden Sie die folgende Tabelle, um zu ermitteln, ob eine Entwicklungstechnologie in Exchange Online oder Exchange 2019 unterstützt wird. Wenn die Technologie nicht unterstützt wird, finden Sie unter [Choose a Development Technology to migrate](#bk_choose)to.

<br/> 

**Exchange-Entwicklungstechnologien und Produktversionen**

|Technologie|Office 365 und Exchange Online|Exchange 2019|Exchange 2016|Exchange 2013|Exchange 2010|Exchange 2007|
|:-----|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|[Office 365-APIs – Plattformübersicht](https://msdn.microsoft.com/library/16fbf0c0-5470-466b-aab8-a0c9074c94e2%28Office.15%29.aspx) <br/> |X  <br/> |X ²  <br/> |X ¹ ²  <br/> ||
|[EWS Managed API](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Exchange-Webdienste (Exchange Web Services, EWS)](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Mail-Apps für Outlook](exchange-web-services/mail-apps-for-outlook-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[Outlook-Objektmodell](https://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Exchange-Verwaltungsshell](management/exchange-management-shell.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Backup and restore](backup-restore/backup-and-restore-for-exchange-2013.md) <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Transport-Agents](transport-agents/transport-agents-in-exchange-2013.md) <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Active Directory-Schnittstellen (ADSI)  <br/> ||||||X  <br/> |
|Kollaborative Datenobjekte für Exchange (CDOEX)  <br/> ||||||X  <br/> |
|Kollaborative Datenobjekte für Windows 2000 (CDOSYS)  <br/> ||||||X  <br/> |
|Exchange OLE DB-Anbieter (OleDb)  <br/> ||||||X  <br/> |
|Ereignissenken des Exchange-Informationsspeichers  <br/> ||||||X  <br/> |
|ICS (Incremental Change Synchronization)  <br/> ||||||X  <br/> |
|Lightweight Directory Access-Protokoll (LDAP)  <br/> ||||||X  <br/> |
|[Messaging-API (MAPI)](https://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> | 
|Outlook Web App Anpassung  <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|WebDAV (Internet Distributed Authoring and Versioning)  <br/> ||||||X  <br/> |

<a name="bk_choose"> </a>

¹ Rest-API und Graph-API erfordern das kumulative Update 3 für Exchange 2016.

² nur Hybrid Kunden können die Rest-APIs sowohl für Office 365 als auch für lokale Postfächer nutzen.

## <a name="choose-a-development-technology-to-migrate-to"></a>Auswählen einer zu migrierenden Entwicklungstechnologie

Wenn die von Ihrer Anwendung verwendete Technologie in Exchange Online oder Exchange 2013 nicht unterstützt oder nicht betont wird, entscheiden Sie anhand der folgenden Tabelle, welche Technologie migriert werden soll.
  
**Empfohlene Migrationspfade für die Technologie**

|**Technologie**|**Unterstützt in Office 365, Exchange Online und Exchange 2019?**|**Migrieren zu**|**Weitere Informationen**|
|:-----|:-----|:-----|:-----|
|ADSI  <br/> |Ja, aber unbetont <br/>|[Exchange-Verwaltungsshell](management/exchange-management-shell.md)<br/> |Keine.  <br/> |
|CDOEX  <br/> |Nein  <br/> |[Verwaltete EWS-API oder EWS](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |Die verwaltete EWS-API und EWS können auf dieselbe Exchange-Informationsspeicher zugreifen, die CDOEX bereitstellt. Im Gegensatz zu Clientanwendungen, die mit CDOEX erstellt wurden, können Sie EWS-Anwendungen auf einem lokalen oder Remotecomputer ausführen.  <br/> |
|CDOEXM  <br/> |Nein <br/> |[Exchange-Verwaltungsshell](management/exchange-management-shell.md) <br/> |Mit Exchange-Verwaltungsshell Befehlen werden Exchange-Server, Speichergruppen, Datenbanken und Benutzer einfacher gesteuert als die entsprechenden CDOEXM-APIs. Außerdem können Sie Ihre CDOEXM-Anwendungen ganz einfach zu Exchange-Verwaltungsshell-Befehlen migrieren.  <br/> |
|CDOSYS<br/> |Nein<br/> |[Transport-Agents](transport-agents/transport-agents-in-exchange-2013.md)   <br/> |Verwenden Sie Transport-Agents für Benachrichtigungs basierte Anwendungen, die mit Exchange-Versionen ab Exchange 2010 funktionieren.<br/><br/> CDOSYS ist in aktuellen Versionen von Windows enthalten. Die Funktionen in CDOSYS stehen im .NET Framework zur Verfügung.  <br/> |
|CDOWF  <br/> |Nein  <br/> |[Windows Workflow Foundation (WWF)](https://msdn.microsoft.com/library/vstudio/ms735967%28v=vs.90%29.aspx) <br/> |Sie können mit dem WWF erweiterte Workflowanwendungen erstellen, die mit Exchange 2007 zusammenarbeiten.   <br/> |
|ExOLEDB  <br/> |Nein  <br/> |[Verwaltete EWS-API oder EWS](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |Die verwaltete EWS-API und EWS bieten den gleichen Zugriff auf das Exchange-Informationsspeicher, das von der codeoledb bereitgestellt wird. Im Gegensatz zu Clientanwendungen, die mithilfe von "OleDb" erstellt wurden, können Sie EWS-Anwendungen auf einem lokalen oder Remotecomputer ausführen.  <br/> |
|ICS  <br/> |Ja, aber unbetont  <br/> |Verwaltete EWS-API oder EWS<br/> |Sie können die verwaltete EWS-API oder EWS verwenden, um [Benachrichtigungen zu abonnieren](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md) und [Postfachdaten zu synchronisieren](exchange-web-services/mailbox-synchronization-and-ews-in-exchange.md).  <br/> |
|LDAP  <br/> |Ja, aber unbetont  <br/> |[Exchange-Verwaltungsshell](management/exchange-management-shell.md) <br/> |Keine.  <br/> |
|MAPI  <br/> |Ja, aber unbetont  <br/> |Office 365-APIs-Plattformübersicht, verwaltete EWS-API, EWS <br/> |Obwohl MAPI derzeit eine unterstützte Entwicklungstechnologie ist, müssen Sie Ihre MAPI-Anwendungen schließlich neu entwerfen, um eine neuere Technologie zu verwenden.<br/><br/>Wenn Ihre MAPI-Anwendung einfache Lese-, Schreib-und Aktualisierungsvorgänge für e-Mails, Kalender-oder Kontaktobjekte und Ziel Office 365, Exchange 2019 ² oder Exchange 2016 ¹ ² ausführt, können Sie die [Office 365-Rest-APIs für e-Mail, Kalender und Kontakte](exchange-web-services/office-365-rest-apis-for-mail-calendars-and-contacts.md)verwenden.<br/><br/>Wenn Sie Exchange lokal ausrichten und auf alle Eigenschaften zugreifen müssen, auf die MAPI zugreifen kann, können Sie die verwaltete EWS-API-oder EWS-und entweder schematisierten- [Eigenschaften oder erweiterte Eigenschaften](https://msdn.microsoft.com/library/68623048-060e-4602-b3fa-62617a94cf72%28Office.15%29.aspx)verwenden.<br/><br/>**Hinweis**: die [ExtendedPropertyDefinition](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) -Klasse bietet Zugriff auf MAPI aus dem verwaltete EWS-API, und das [ExtendedFieldURI](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) -Element bietet Zugriff auf MAPI-Eigenschaften von EWS.           |
|Outlook Web App Anpassung  <br/> |Nein  <br/> |[Mail-Apps](exchange-web-services/mail-apps-for-outlook-and-ews-in-exchange.md) <br/> |Keine.  <br/> |
|Speichern von Ereignissenken  <br/> |Nein  <br/> |Verwaltete EWS-API oder EWS <br/> |Sie können die verwaltete EWS-API oder EWS verwenden, um [Benachrichtigungen zu abonnieren](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md) und [Postfachdaten zu synchronisieren](exchange-web-services/mailbox-synchronization-and-ews-in-exchange.md).<br/><br/>Die Benachrichtigungen in EWS bieten denselben Zugriff auf die Exchange-Informationsspeicher, die von Store-Ereignissenken bereitgestellt werden. Sie können Visual Studio Tools verwenden, um die Entwicklung von Ereignis fähigen Store-Clientanwendungen zu rationalisieren, die EWS verwenden.  <br/> |
|Streaming-Sicherung und-Wiederherstellung  <br/> |Nein  <br/> |[VSS-Writer (Volume Shadow Copy Service, Volumeschattenkopie-Dienst)](backup-restore/backup-and-restore-for-exchange-2013.md) <br/> |Keine.  <br/> |
|WebDAV  <br/> |Nein  <br/> |Office 365-APIs Plattformübersicht, verwaltete EWS-API oder EWS <br/> |Wenn Ihre WebDAV-Anwendung einfache Lese-, Schreib-und Aktualisierungsvorgänge für e-Mail-, Kalender-oder Kontaktobjekte ausführt und Sie Office 365, Exchange 2019 ² oder Exchange 2016 ¹ ² verwenden, können Sie die [Office 365-Rest-APIs für e-Mail, Kalender und Kontakte](exchange-web-services/office-365-rest-apis-for-mail-calendars-and-contacts.md)verwenden.<br/><br/>Wenn Sie Exchange lokal anvisieren und Zugriff auf dieselben Eigenschaften in der Exchange-Informationsspeicher benötigen, die WebDAV bereitstellt, verwenden Sie die verwaltete EWS-API oder EWS.  <br/> |
|WebDAV-Benachrichtigungen  <br/> |Nein  <br/> |Verwaltete EWS-API oder EWS<br/> |Sie können die verwaltete EWS-API oder EWS verwenden, um [Benachrichtigungen zu abonnieren](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md).  <br/> |
|Webformulare  <br/> |Nein  <br/> |[ASP.NET](http://www.asp.net/web-forms) <br/> |Wechseln Sie zu ASP.net, und aktualisieren Sie Anwendungen, um mithilfe von EWS auf Post Fach-und Server Informationen zuzugreifen.  <br/> |
|WMI-Anbieter  <br/> |Nein  <br/> |[Exchange-Verwaltungsshell](management/exchange-management-shell.md) <br/> |Keine.  <br/> |
   
¹ Rest-API und Graph-API erfordern das kumulative Update 3 für Exchange 2016.

² nur Hybrid Kunden können die Rest-APIs sowohl für Office 365 als auch für lokale Postfächer nutzen.

## <a name="see-also"></a>Siehe auch

- [Auswählen einer API oder Technologie für die Entwicklung von Lösungen für Outlook](https://msdn.microsoft.com/library/01a46083-03d0-4333-920c-01a9f17f68cb%28Office.15%29.aspx)
- [Anforderungen an die lokale Architektur für die REST-API](https://blogs.technet.microsoft.com/exchange/2016/09/26/on-premises-architectural-requirements-for-the-rest-api/)    
