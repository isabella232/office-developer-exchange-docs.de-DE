---
title: Verfügbarkeit von Web Service-API in Exchange und die EWS Managed API
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 07d3e6e8-d549-4ad7-baa4-bc531dfb7dd2
description: Hier erfahren Sie, welche EWS und-Webdienst API-Features in den einzelnen Versionen von Exchange und die EWS Managed API verfügbar sind.
ms.openlocfilehash: d19ab062c8d418e373e8268b1ab039e5436e71bf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757134"
---
# <a name="web-service-api-feature-availability-in-exchange-and-the-ews-managed-api"></a>Verfügbarkeit von Web Service-API in Exchange und die EWS Managed API

Hier erfahren Sie, welche EWS und-Webdienst API-Features in den einzelnen Versionen von Exchange und die EWS Managed API verfügbar sind.
  
Exchange-Clientanwendungen Ziel häufig viele Versionen von Exchange. Aus diesem Grund sollten Sie Ihre Anwendung so entwerfen, dass Sie [EWS-Client-Funktionen](ews-client-design-overview-for-exchange.md#EWSFeatures) aktivieren und deaktivieren basierend auf der Exchange-Version können, die Postfach des Benutzers hostet. Dieser Artikel enthält Informationen zu den neuen Dienst-API-Funktionen in verschiedenen Versionen von Exchange und die EWS Managed API zur Verfügung stehen. Anhand dieser Informationen zum Entwerfen der Anwendung auf Allgemein gelten für Kunden, die mehrere Versionen von Exchange ausführen. 
  
Ausführliche Informationen zu den Unterschieden zwischen Versionen von Exchange überprüfen Sie die EWS-Schemadateien und der zugehörigen [Referenzdokumentation](http://msdn.microsoft.com/library/6c969133-6036-448b-af39-a3caf9917e98%28Office.15%29.aspx).
  
## <a name="api-features-by-exchange-version"></a>API-Funktionen von Exchange-version
<a name="bk_apifeatures"> </a>

Der Exchange-Webdienst-APIs, einschließlich EWS und AutoErmittlung, werden bei der Versionsübergreifende Kompatibilität im Hinterkopf entwickelt. Aus diesem Grund kann eine Anwendung, die auf Exchange 2007 abzielt auch gegen Versionen von Exchange, beginnend mit Exchange 2013, einschließlich Exchange Online und Exchange Online als Teil von Office 365. 
  
Die folgende Tabelle gibt an, welche API-Features in jeder Version von Exchange und Versionen von EWS Managed API ab Version 2.0 zur Verfügung stehen. Da Ihre Anwendung mehrere Versionen von Exchange möglicherweise, wird es hilfreich sein für Sie wissen, welche Versionen der Features unterstützt, die der Client implementiert wird. Sie können den AutoErmittlungsdienst verwenden, ermitteln können, welche Version von Exchange beruht auf ein Client für einen Benutzer, damit Sie umwandeln können Features ein- und ausschalten, je nachdem, ob sie für die Benutzer verfügbar sind.
  
**In Tabelle 1. Web-Service-Verfügbarkeit in Versionen von Exchange und die EWS Managed API**

|API-Funktion|Exchange Online (Office 365)|Verwaltete EWS-API|Exchange 2013|Exchange 2010 SP2|Exchange 2010 SP1|Exchange 2010|Exchange 2007 SP1|Exchange 2007|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Auflösung nicht eindeutiger Namen  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Apps für Outlook-Verwaltung  <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|[Archiv Postfachzugriff](archiving-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|[AutoErmittlung (POX)](autodiscover-for-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[AutoErmittlung (SOAP)](autodiscover-for-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|Automatische Antworten (ABWESEND)  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Verfügbarkeit  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Verfügbarkeit (Chatrooms)  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|Massen-Übertragung  <br/> |X  <br/> ||X  <br/> |X  <br/> |X  <br/> ||||
|Kontaktgruppen  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|Unterhaltungsverwaltung  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|DateTime mit doppelter Genauigkeit  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||||
|Delegieren der Verwaltung  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|Die Erweiterung der Verteilerliste  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Dumpster Zugriff](deleting-items-by-using-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[eDiscovery](ediscovery-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|Erweiterte Zeitzonen  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|Berechtigungen für Ordner  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[Bezeichner Konvertierung](ews-identifiers-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[Posteingang management](inbox-management-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|[Zugriff auf Element und Ordner](folders-and-items-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Postfach-Ereignisse ("Pull" und "Push")](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Postfach-Ereignisse (streaming)](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|E-Mail-Infos  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|Kennwortablauf  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||||
|[Rollen](people-and-contacts-in-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
|Bereitstellungselemente  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[Zugriff auf Öffentliche Ordner](public-folder-access-with-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|Aufbewahrungsrichtlinien  <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|[Suche (indiziert)](search-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[Suche (Anmelden)](search-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Synchronisierung](mailbox-synchronization-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Einheitlicher Kontaktspeicher](people-and-contacts-in-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
|[Unified Messaging-Webdienst](http://msdn.microsoft.com/library/83afea8a-c716-41df-9eb2-e1000357afb6%28Office.15%29.aspx) <br/> |X  <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Unified Messaging (EWS-basiert)  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[Konfiguration der Benutzerobjekte](persistent-application-settings-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[Benutzerfotos](how-to-get-user-photos-by-using-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
   
Sie können weitere Informationen im Web Servicefunktionen finden, die durch das Lesen über die [EWS-Vorgänge](http://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx), der [AutoErmittlungsdienst](http://msdn.microsoft.com/library/a01124a8-a8cf-4b80-8625-d7ee05690bca%28Office.15%29.aspx)und die [ExchangeService Methoden](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice_methods%28v=exchg.80%29.aspx)in verschiedenen Versionen von Exchange verfügbar sind.
  
## <a name="to-learn-more"></a>Um mehr zu erfahren
<a name="bk_apifeatures"> </a>

Wenn Sie tiefer zu verstehen, die Unterschiede zwischen Exchange-Versionen wechseln möchten, können Sie die folgenden Aufgaben ausführen:
  
- Verwenden Sie die [EWS-Schema](http://msdn.microsoft.com/library/6c969133-6036-448b-af39-a3caf9917e98%28Office.15%29.aspx) , um die Unterschiede zwischen den einzelnen Versionen von EWS ausführlicher untersuchen. 
    
- Laden Sie [EWSEditor](http://ewseditor.codeplex.com/). EWSEditor können Sie die unterschiedlichen Zielelement Schemaversionen angeben, und Übermitteln von Abfragen auf die Zielversion Schema basieren.
    
## <a name="see-also"></a>Siehe auch

- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)   
- [Erste Schritte mit verwalteten EWS-API-Clientanwendungen](get-started-with-ews-managed-api-client-applications.md) 
- [What's new in Exchange-Webdienste und andere Webdienste in Exchange](whats-new-in-ews-and-other-web-services-in-exchange.md)
    

