---
title: Verfügbarkeit von Web Service-API in Exchange und die EWS Managed API
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 07d3e6e8-d549-4ad7-baa4-bc531dfb7dd2
description: Erfahren Sie, welche EWS- und Webdienst-API-Features in jeder Version von Exchange und der verwalteten EWS-API verfügbar sind.
ms.openlocfilehash: 6fc0c40410be543b149885c7b0785a2c6c8828af
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544472"
---
# <a name="web-service-api-feature-availability-in-exchange-and-the-ews-managed-api"></a>Verfügbarkeit von Web Service-API in Exchange und die EWS Managed API

Erfahren Sie, welche EWS- und Webdienst-API-Features in jeder Version von Exchange und der verwalteten EWS-API verfügbar sind.
  
Exchange Clientanwendungen zielen häufig auf viele Versionen von Exchange ab. Aus diesem Grund sollten Sie Ihre Anwendung so entwerfen, dass Sie [EWS-Clientfeatures](ews-client-design-overview-for-exchange.md#EWSFeatures) basierend auf der Version von Exchange aktivieren und deaktivieren können, die das Postfach Ihrer Benutzer hostet. Dieser Artikel enthält Informationen darüber, welche Dienst-API-Features in verschiedenen Versionen von Exchange und der verwalteten EWS-API verfügbar sind. Verwenden Sie diese Informationen, um Ihre Anwendung so zu gestalten, dass sie allgemein auf Kunden angewendet wird, die mehrere Versionen von Exchange ausführen. 
  
Ausführliche Informationen zu den Unterschieden zwischen versionen von Exchange finden Sie in den EWS-Schemadateien und der zugehörigen [Referenzdokumentation.](https://msdn.microsoft.com/library/6c969133-6036-448b-af39-a3caf9917e98%28Office.15%29.aspx)
  
## <a name="api-features-by-exchange-version"></a>API-Features nach Exchange Version
<a name="bk_apifeatures"> </a>

Die Exchange Webdienst-APIs, einschließlich EWS und AutoErmittlung, werden unter Berücksichtigung der Kompatibilität mit mehreren Versionen entwickelt. Daher funktioniert eine Anwendung, die auf Exchange 2007 ausgerichtet ist, auch mit Versionen von Exchange ab Exchange 2013, einschließlich Exchange Online und Exchange Online als Teil der Office 365. 
  
Die folgende Tabelle gibt an, welche API-Features in jeder Version von Exchange und Versionen der verwalteten EWS-API ab Version 2.0 verfügbar sind. Da Ihre Anwendung möglicherweise auf mehrere Versionen von Exchange ausgerichtet ist, ist es hilfreich, dass Sie wissen, welche Versionen die features unterstützen, die Ihr Client implementiert. Sie können den AutoErmittlungsdienst verwenden, um zu ermitteln, welche Version von Exchange ein Client für einen Benutzer bestimmt ist, sodass Sie Features aktivieren und deaktivieren können, je nachdem, ob sie für Ihre Benutzer verfügbar sind.
  
**Tabelle 1. Verfügbarkeit von Webdienstfeatures in Versionen von Exchange und der verwalteten EWS-API**

|API-Feature|Exchange Online (Office 365)|Verwaltete EWS-API|Exchange 2013|Exchange 2010 SP2|Exchange 2010 SP1|Exchange 2010|Exchange 2007 SP1|Exchange 2007|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Mehrdeutige Namensauflösung  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Apps für Outlook-Verwaltung  <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|[Archivpostfachzugriff](archiving-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|[AutoErmittlung (POX)](autodiscover-for-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[AutoErmittlung (SOAP)](autodiscover-for-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|Automatische Antworten (OOF)  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Verfügbarkeit  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Verfügbarkeit (Räume)  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|Massenübertragung  <br/> |X  <br/> ||X  <br/> |X  <br/> |X  <br/> ||||
|Kontaktgruppen  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|Unterhaltungsverwaltung  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|DateTime-Genauigkeit  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||||
|Stellvertretungsverwaltung  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|Erweiterung der Verteilerliste  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Dumpsterzugriff](deleting-items-by-using-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[eDiscovery](ediscovery-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|Erweiterte Zeitzonen  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|Ordnerberechtigungen  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[Bezeichnerkonvertierung](ews-identifiers-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[Posteingangsverwaltung](inbox-management-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|[Element- und Ordnerzugriff](folders-and-items-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Postfachereignisse (Pull und Push)](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Postfachereignisse (Streaming)](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|E-Mail-Info  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|Kennwortablauf  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||||
|[Personas](people-and-contacts-in-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
|Bereitstellungselemente  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[Zugriff auf öffentliche Ordner](public-folder-access-with-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|Aufbewahrungsrichtlinien  <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|[Suche (indiziert)](search-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[Suche (Store)](search-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Synchronisierung](mailbox-synchronization-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Einheitlicher Kontaktspeicher](people-and-contacts-in-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
|[Unified Messaging-Webdienst](https://msdn.microsoft.com/library/83afea8a-c716-41df-9eb2-e1000357afb6%28Office.15%29.aspx) <br/> |X  <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Unified Messaging (EWS-basiert)  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[Benutzerkonfigurationsobjekte](persistent-application-settings-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[Benutzerfotos](how-to-get-user-photos-by-using-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
   
Weitere Informationen zu den Webdienstfeatures, die in verschiedenen Versionen von Exchange verfügbar sind, finden Sie unter den [EWS-Vorgängen,](https://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx)dem [AutoErmittlungsdienst](https://msdn.microsoft.com/library/a01124a8-a8cf-4b80-8625-d7ee05690bca%28Office.15%29.aspx)und den [ExchangeService-Methoden.](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice_methods%28v=exchg.80%29.aspx)
  
## <a name="to-learn-more"></a>Weitere Informationen
<a name="bk_apifeatures"> </a>

Wenn Sie die spezifischen Unterschiede zwischen Exchange Versionen genauer verstehen möchten, können Sie eine der folgenden Aktionen ausführen:
  
- Erkunden Sie das [EWS-Schema,](https://msdn.microsoft.com/library/6c969133-6036-448b-af39-a3caf9917e98%28Office.15%29.aspx) um die Unterschiede zwischen den einzelnen Versionen von EWS genauer zu untersuchen. 
    
- Laden Sie [EWSEditor herunter.](http://ewseditor.codeplex.com/) Sie können EWSEditor verwenden, um verschiedene Zielschemaversionen anzugeben und Abfragen basierend auf der Zielschemaversion zu senden.
    
## <a name="see-also"></a>Siehe auch

- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)   
- [Erste Schritte mit verwalteten EWS-API-Clientanwendungen](get-started-with-ews-managed-api-client-applications.md) 
- [Neuerungen in EWS und anderen Webdiensten in Exchange](whats-new-in-ews-and-other-web-services-in-exchange.md)
    

