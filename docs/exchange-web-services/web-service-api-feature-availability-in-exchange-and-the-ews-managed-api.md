---
title: Verfügbarkeit von Web Service-API in Exchange und die EWS Managed API
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 07d3e6e8-d549-4ad7-baa4-bc531dfb7dd2
description: Erfahren Sie, welche EWS-und Webdienst-API-Features in jeder Version von Exchange und der verwaltete EWS-API zur Verfügung stehen.
ms.openlocfilehash: f15cf4784a59c18d1bb9ae20af378baed084acc3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529847"
---
# <a name="web-service-api-feature-availability-in-exchange-and-the-ews-managed-api"></a>Verfügbarkeit von Web Service-API in Exchange und die EWS Managed API

Erfahren Sie, welche EWS-und Webdienst-API-Features in jeder Version von Exchange und der verwaltete EWS-API zur Verfügung stehen.
  
Exchange-Clientanwendungen Zielen häufig auf viele Versionen von Exchange ab. Aus diesem Grund sollten Sie Ihre Anwendung so entwerfen, dass Sie die [EWS-Clientfunktionen](ews-client-design-overview-for-exchange.md#EWSFeatures) basierend auf der Exchange-Version, die das Postfach ihrer Benutzer hostet, ein-und ausschalten können. Dieser Artikel enthält Informationen darüber, welche Dienst-API-Features in verschiedenen Versionen von Exchange und im verwaltete EWS-API zur Verfügung stehen. Verwenden Sie diese Informationen, um Ihre Anwendung so zu entwerfen, dass Sie umfassend auf Kunden angewendet wird, die mehrere Versionen von Exchange verwenden. 
  
Ausführliche Informationen zu den Unterschieden zwischen Versionen von Exchange finden Sie in den EWS-Schemadateien und der zugehörigen [Referenzdokumentation](https://msdn.microsoft.com/library/6c969133-6036-448b-af39-a3caf9917e98%28Office.15%29.aspx).
  
## <a name="api-features-by-exchange-version"></a>API-Features nach Exchange-Version
<a name="bk_apifeatures"> </a>

Die Exchange-Webdienst-APIs, einschließlich EWS und AutoErmittlung, werden im Hinblick auf Kompatibilität mit mehreren Versionen entwickelt. Daher funktioniert eine Anwendung, die auf Exchange 2007 zielt, auch gegen Versionen von Exchange, beginnend mit Exchange 2013, einschließlich Exchange Online und Exchange Online als Teil von Office 365. 
  
In der folgenden Tabelle wird angegeben, welche API-Features in jeder Version von Exchange verfügbar sind und welche Versionen der verwaltete EWS-API ab Version 2,0. Da Ihre Anwendung möglicherweise auf mehrere Versionen von Exchange abzielt, ist es hilfreich, wenn Sie wissen, welche Versionen die von Ihrem Client implementierten Features unterstützen. Sie können den AutoErmittlungsdienst verwenden, um zu ermitteln, welche Version von Exchange ein Client für einen Benutzer abzielt, sodass Sie Features in Abhängigkeit davon, ob Sie für Ihre Benutzer verfügbar sind, ein-und ausschalten können.
  
**Tabelle 1. Verfügbarkeit von Webdienstfeatures in Exchange-Versionen und verwaltete EWS-API**

|API-Feature|Exchange Online (Office 365)|Verwaltete EWS-API|Exchange 2013|Exchange 2010 SP2|Exchange 2010 SP1|Exchange 2010|Exchange 2007 SP1|Exchange 2007|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Auflösung nicht eindeutiger Namen  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Apps für Outlook-Verwaltung  <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|[Archivieren des Postfachzugriffs](archiving-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|[AutoErmittlung (POX)](autodiscover-for-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[AutoErmittlung (SOAP)](autodiscover-for-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|Automatische Antworten (OOF)  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Verfügbarkeit  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Verfügbarkeit (Räume)  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|Massenübertragung  <br/> |X  <br/> ||X  <br/> |X  <br/> |X  <br/> ||||
|Kontaktgruppen  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|Unterhaltungs Verwaltung  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|DateTime-Genauigkeit  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||||
|Delegieren der Verwaltung  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|Verteilerlistenerweiterung  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Zugriff auf den Papierkorb](deleting-items-by-using-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[eDiscovery](ediscovery-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|Erweiterte Zeitzonen  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|Ordnerberechtigungen  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[Bezeichner-Konvertierung](ews-identifiers-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[Posteingangsverwaltung](inbox-management-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|[Zugriff auf Elemente und Ordner](folders-and-items-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Mailbox-Ereignisse (Pull und Push)](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Post Fach Ereignisse (Streaming)](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|MailTips  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|Kennwortablauf  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||||
|[Personas](people-and-contacts-in-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
|Bereitstellungselemente  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[Zugriff auf Öffentliche Ordner](public-folder-access-with-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|Aufbewahrungsrichtlinien  <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|[Suche (indiziert)](search-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[Suche (Store)](search-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Synchronisierung](mailbox-synchronization-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Einheitlicher Kontaktspeicher](people-and-contacts-in-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
|[Unified Messaging-Webdienst](https://msdn.microsoft.com/library/83afea8a-c716-41df-9eb2-e1000357afb6%28Office.15%29.aspx) <br/> |X  <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Unified Messaging (EWS-basiert)  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[Benutzer Konfigurationsobjekte](persistent-application-settings-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[Benutzerfotos](how-to-get-user-photos-by-using-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
   
Weitere Informationen zu den Webdienstfeatures, die in verschiedenen Versionen von Exchange zur Verfügung stehen, finden Sie unter Lesen der [EWS-Vorgänge](https://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx), des [AutoErmittlungsdiensts](https://msdn.microsoft.com/library/a01124a8-a8cf-4b80-8625-d7ee05690bca%28Office.15%29.aspx)und der [Datei "ExchangeService-Methoden](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice_methods%28v=exchg.80%29.aspx).
  
## <a name="to-learn-more"></a>Weitere Informationen
<a name="bk_apifeatures"> </a>

Wenn Sie tiefer gehen möchten, um die spezifischen Unterschiede zwischen Exchange-Versionen zu verstehen, können Sie eine der folgenden Aktionen ausführen:
  
- Erkunden Sie das [EWS-Schema](https://msdn.microsoft.com/library/6c969133-6036-448b-af39-a3caf9917e98%28Office.15%29.aspx) , um die Unterschiede zwischen den einzelnen Versionen von EWS detaillierter zu untersuchen. 
    
- [EWSEditor](http://ewseditor.codeplex.com/)herunterladen. Sie können EWSEditor verwenden, um unterschiedliche Zielschema Versionen anzugeben und Abfragen basierend auf der Zielschema Version zu übermitteln.
    
## <a name="see-also"></a>Siehe auch

- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)   
- [Erste Schritte mit verwalteten EWS-API-Clientanwendungen](get-started-with-ews-managed-api-client-applications.md) 
- [Neuerungen in EWS und anderen Webdiensten in Exchange](whats-new-in-ews-and-other-web-services-in-exchange.md)
    

