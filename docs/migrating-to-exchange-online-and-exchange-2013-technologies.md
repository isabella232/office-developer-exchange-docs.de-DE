---
title: Migration zu Exchange-Technologien
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 946a722f-0892-4a59-9e58-a291bfb6834a
description: Wenn Sie von einer früheren Version von Exchange migrieren, verwenden Sie die Informationen in diesem Artikel, um herauszufinden, welche Entwicklungstechnologien in aktuellen Produktversionen unterstützt werden und zu welcher Technologie Sie migrieren möchten.
ms.openlocfilehash: 3885d6789cedf5de028b64a0658b336bd021b9ee
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59527001"
---
# <a name="migrating-to-exchange-technologies"></a>Migration zu Exchange-Technologien

Wenn Sie von einer früheren Version von Exchange migrieren, verwenden Sie die Informationen in diesem Artikel, um herauszufinden, welche Entwicklungstechnologien in aktuellen Produktversionen unterstützt werden und zu welcher Technologie Sie migrieren möchten.
  
## <a name="determine-if-your-technology-is-available-in-current-versions"></a>Ermitteln, ob Ihre Technologie in aktuellen Versionen verfügbar ist

Verwenden Sie die folgende Tabelle, um zu bestimmen, ob eine Entwicklungstechnologie in Exchange Online oder Exchange 2019 unterstützt wird. Wenn die Technologie nicht unterstützt wird, lesen Sie die Informationen unter ["Auswählen einer Entwicklungstechnologie", zu der migriert werden soll.](#bk_choose)

<br/> 

**Exchange Entwicklungstechnologien und Produktversionen**

|Technologie|Office 365 und Exchange Online|Exchange 2019|Exchange 2016|Exchange 2013|Exchange 2010|Exchange 2007|
|:-----|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|[Office 365-APIs – Plattformübersicht](https://msdn.microsoft.com/library/16fbf0c0-5470-466b-aab8-a0c9074c94e2%28Office.15%29.aspx) <br/> |X  <br/> |X²  <br/> |Xe ²  <br/> ||
|[EWS Managed API](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Exchange-Webdienste (Exchange Web Services, EWS)](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Mail-Apps für Outlook](exchange-web-services/mail-apps-for-outlook-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[Outlook Objektmodell (OOM)](https://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Exchange-Verwaltungsshell](management/exchange-management-shell.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Backup and restore](backup-restore/backup-and-restore-for-exchange-2013.md) <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Transport-Agents](transport-agents/transport-agents-in-exchange-2013.md) <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Active Directory-Schnittstellen (ADSI)  <br/> ||||||X  <br/> |
|Collaborative Data Objects for Exchange (CDOEX)  <br/> ||||||X  <br/> |
|Collaborative Data Objects for Windows 2000 (CDOSYS)  <br/> ||||||X  <br/> |
|Exchange OLE DB-Anbieter (EXOLEDB)  <br/> ||||||X  <br/> |
|Ereignissenken des Exchange-Informationsspeichers  <br/> ||||||X  <br/> |
|ICS (Incremental Change Synchronization)  <br/> ||||||X  <br/> |
|Lightweight Directory Access-Protokoll (LDAP)  <br/> ||||||X  <br/> |
|[Messaging-API (MAPI)](https://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> | 
|Outlook Web App Anpassung  <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|Web Distributed Authoring and Versioning (WebDAV)  <br/> ||||||X  <br/> |

<a name="bk_choose"> </a>

Für die API und Graph API ist das kumulative Update 3 für Exchange 2016 erforderlich.

²Only-Hybridkunden können die REST-APIs sowohl für Office 365 als auch für lokale Postfächer nutzen.

## <a name="choose-a-development-technology-to-migrate-to"></a>Auswählen einer Entwicklungstechnologie, zu der migriert werden soll

Wenn die von Ihrer Anwendung verwendete Technologie in Exchange Online oder Exchange 2013 nicht unterstützt oder als eingestuft wird, entscheiden Sie anhand der folgenden Tabelle, zu welcher Technologie sie migriert werden soll.
  
**Empfohlene Migrationspfade für Technologien**

|**Technologie**|**Unterstützt in Office 365, Exchange Online und Exchange 2019?**|**Migrieren zu**|**Weitere Informationen**|
|:-----|:-----|:-----|:-----|
|ADSI  <br/> |Ja, aber als "deemphasized" <br/>|[Exchange-Verwaltungsshell](management/exchange-management-shell.md)<br/> |Keine  <br/> |
|CDOEX  <br/> |Nein  <br/> |[Verwaltete EWS-API oder EWS](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |Die verwaltete EWS-API und EWS können auf den gleichen Exchange Speicher zugreifen, den CDOEX bereitstellt. Im Gegensatz zu Clientanwendungen, die mit CDOEX erstellt wurden, können Sie EWS-Anwendungen auf einem lokalen oder Remotecomputer ausführen.  <br/> |
|CDOEXM  <br/> |Nein <br/> |[Exchange-Verwaltungsshell](management/exchange-management-shell.md) <br/> |Exchange Verwaltungsshell-Befehle steuern Exchange Server, Speichergruppen, Datenbanken und Benutzer einfacher als die entsprechenden CDOEXM-APIs. Darüber hinaus können Sie Ihre CDOEXM-Anwendungen ganz einfach zu Exchange-Verwaltungsshell-Befehlen migrieren.  <br/> |
|CDOSYS<br/> |Nein<br/> |[Transport-Agents](transport-agents/transport-agents-in-exchange-2013.md)   <br/> |Verwenden Sie Transport-Agents für benachrichtigungsbasierte Anwendungen, die mit Versionen von Exchange ab Exchange 2010 arbeiten.<br/><br/> CDOSYS ist in aktuellen Versionen von Windows enthalten. Die Funktionalität in CDOSYS ist im .NET Framework verfügbar.  <br/> |
|CDOWF  <br/> |Nein  <br/> |[Windows Workflow Foundation (WWF)](https://msdn.microsoft.com/library/vstudio/ms735967%28v=vs.90%29.aspx) <br/> |Sie können WWF verwenden, um erweiterte Workflowanwendungen zu erstellen, die mit Exchange 2007 arbeiten.   <br/> |
|Exoledb  <br/> |Nein  <br/> |[Verwaltete EWS-API oder EWS](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |Die verwaltete EWS-API und EWS bieten den gleichen Zugriff auf den Exchange Speicher, den ExOLEDB bereitstellt. Im Gegensatz zu Clientanwendungen, die mithilfe von ExOLEDB erstellt wurden, können Sie EWS-Anwendungen auf einem lokalen oder Remotecomputer ausführen.  <br/> |
|ICS  <br/> |Ja, aber als "deemphasized"  <br/> |Verwaltete EWS-API oder EWS<br/> |Sie können die verwaltete EWS-API oder EWS verwenden, um [Benachrichtigungen zu abonnieren](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md) und [Postfachdaten zu synchronisieren.](exchange-web-services/mailbox-synchronization-and-ews-in-exchange.md)  <br/> |
|LDAP  <br/> |Ja, aber als "deemphasized"  <br/> |[Exchange-Verwaltungsshell](management/exchange-management-shell.md) <br/> |Keine  <br/> |
|MAPI  <br/> |Ja, aber als "deemphasized"  <br/> |Office 365 Übersicht über die APIs-Plattform, verwaltete EWS-API, EWS <br/> |Obwohl die MAPI derzeit eine unterstützte Entwicklungstechnologie ist, müssen Sie ihre MAPI-Anwendungen letztendlich neu entwerfen, um eine neuere Technologie zu verwenden.<br/><br/>Wenn Ihre MAPI-Anwendung einfache Lese-, Schreib- und Aktualisierungsvorgänge für E-Mail-, Kalender- oder Kontaktobjekte durchführt und auf Office 365 Exchange 2019² oder Exchange 2016e ² abzielt, können Sie die [Office 365 REST-APIs für E-Mails, Kalender und Kontakte](exchange-web-services/office-365-rest-apis-for-mail-calendars-and-contacts.md)verwenden.<br/><br/>Wenn Sie Exchange lokal ausrichten und auf alle Eigenschaften zugreifen müssen, auf die MAPI zugreifen kann, können Sie die verwaltete EWS-API oder EWS und entweder [schematisierte Eigenschaften oder erweiterte Eigenschaften](https://msdn.microsoft.com/library/68623048-060e-4602-b3fa-62617a94cf72%28Office.15%29.aspx)verwenden.<br/><br/>**HINWEIS:** Die [ExtendedPropertyDefinition-Klasse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) ermöglicht den Zugriff auf die MAPI über die verwaltete EWS-API, und das [ExtendedFieldURI-Element](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) bietet Zugriff auf MAPI-Eigenschaften von EWS.           |
|Anpassung von Outlook Web App  <br/> |Nein  <br/> |[Mail-Apps](exchange-web-services/mail-apps-for-outlook-and-ews-in-exchange.md) <br/> |Keine  <br/> |
|Store-Ereignissenken  <br/> |Nein  <br/> |Verwaltete EWS-API oder EWS <br/> |Sie können die verwaltete EWS-API oder EWS verwenden, um [Benachrichtigungen zu abonnieren](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md) und [Postfachdaten zu synchronisieren.](exchange-web-services/mailbox-synchronization-and-ews-in-exchange.md)<br/><br/>Die Benachrichtigungen in EWS bieten den gleichen Zugriff auf den Exchange Speicher, den die Speicherereignissenken bereitstellen. Sie können Visual Studio Tools verwenden, um die Entwicklung von Ereignis-fähigen Clientanwendungen zu optimieren, die EWS verwenden.  <br/> |
|Sicherung und Wiederherstellung des Streamings  <br/> |Nein  <br/> |[Volumeschattenkopie-Dienst -Writer (Volume Shadow Copy Service, VSS)](backup-restore/backup-and-restore-for-exchange-2013.md) <br/> |Keine  <br/> |
|Webdav  <br/> |Nein  <br/> |Office 365 Übersicht über die APIs-Plattform, verwaltete EWS-API oder EWS <br/> |Wenn Ihre WebDAV-Anwendung einfache Lese-, Schreib- und Aktualisierungsvorgänge für E-Mail-, Kalender- oder Kontaktobjekte durchführt und Sie auf Office 365 abzielen, können Sie Exchange 2019² oder Exchange 2016 das [Office 365 REST-APIs für E-Mails, Kalender und Kontakte](exchange-web-services/office-365-rest-apis-for-mail-calendars-and-contacts.md)verwenden.<br/><br/>Wenn Sie Exchange lokal ausrichten und Zugriff auf dieselben Eigenschaften im Exchange Speicher benötigen, den WebDAV bereitstellt, verwenden Sie andernfalls die verwaltete EWS-API oder EWS.  <br/> |
|WebDAV-Benachrichtigungen  <br/> |Nein  <br/> |Verwaltete EWS-API oder EWS<br/> |Sie können die verwaltete EWS-API oder EWS verwenden, um [Benachrichtigungen zu abonnieren.](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md)  <br/> |
|Webformulare  <br/> |Nein  <br/> |[ASP.NET](http://www.asp.net/web-forms) <br/> |Wechseln Sie zu ASP.NET und aktualisieren Sie Anwendungen, um mithilfe von EWS auf Postfach- und Serverinformationen zuzugreifen.  <br/> |
|WMI-Anbieter  <br/> |Nein  <br/> |[Exchange-Verwaltungsshell](management/exchange-management-shell.md) <br/> |Keine  <br/> |
   
Für die API und Graph API ist das kumulative Update 3 für Exchange 2016 erforderlich.

Hybridkunden von ²Only können die REST-APIs sowohl für Office 365 als auch für lokale Postfächer nutzen.

## <a name="see-also"></a>Siehe auch

- [Auswählen einer API oder Technologie für die Entwicklung von Lösungen für Outlook](https://msdn.microsoft.com/library/01a46083-03d0-4333-920c-01a9f17f68cb%28Office.15%29.aspx)
- [Anforderungen an die lokale Architektur für die REST-API](https://blogs.technet.microsoft.com/exchange/2016/09/26/on-premises-architectural-requirements-for-the-rest-api/)    
