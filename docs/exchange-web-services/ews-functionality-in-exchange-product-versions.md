---
title: EWS-Funktionalität in Exchange-Produktversionen
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 186c51dc-ec33-4a5d-b739-c9fcb1d4cdd3
description: EWS implementiert neue Funktionen in neuen Produktversionen. Verwenden Sie die Informationen in diesem Artikel, um zu ermitteln, ob die von Ihnen verwendete Exchange-Version Unterstützung für die Daten oder Features bietet, auf die Sie Zugriff benötigen.
ms.openlocfilehash: a8032e16cdd9100289666d8f2ce742fe054ede2e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456031"
---
# <a name="ews-functionality-in-exchange-product-versions"></a>EWS-Funktionalität in Exchange-Produktversionen

EWS implementiert neue Funktionen in neuen Produktversionen. Verwenden Sie die Informationen in diesem Artikel, um zu ermitteln, ob die von Ihnen verwendete Exchange-Version Unterstützung für die Daten oder Features bietet, auf die Sie Zugriff benötigen. 
  
In der folgenden Tabelle sind die Exchange-Versionen mit EWS und die wichtigsten Features aufgeführt, die in jeder Version eingeführt wurden.
  
## <a name="ews-features-by-product-version"></a>EWS-Features nach Produktversion

|**Produktversion**|**Features**|
|:-----|:-----|
|Office 365 und Exchange Online |Enthält alle Features in der aktuellen Version von Exchange sowie alle neuen Features, die für Online Clients hinzugefügt werden.  |
|Exchange 2013 SP1 | Enthält alle Features, die in Exchange 2013 eingeführt wurden. Die folgenden Features wurden in Exchange 2013 SP1 eingeführt:<ul><li>Lesebestätigungen können jetzt für Aktualisierungen und Löschungen angehalten werden.</li><li>Sie können Informationen zu [moderierten Transport](https://msdn.microsoft.com/library/43a89f71-8002-4cb0-b3c8-1c2b2597f227%28Office.15%29.aspx) Genehmigungen erhalten.</li><li>Abstimmungsantworten können angezeigt werden.</li><li>Die [SetHoldOnMailboxes](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.setholdonmailboxes%28v=exchg.80%29.aspx) -Methode und der [SetHoldOnMailboxes](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) -Vorgang akzeptieren alle Parameter in einem einzelnen Objekt.</li><li>eDiscovery-suchen können eine Sprache für Suchabfragen und ein kulturspezifisches Format für Datumsbereiche angeben.</li><li>Das [StreamingSubscriptionConnection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection%28v=exchg.80%29.aspx) -Objekt kann nun auf die [StreamingSubscription](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscription%28v=exchg.80%29.aspx) -Objekte zugreifen.</li><li>Unterhaltungen haben eine Einstellung, um anzugeben, ob Sie e-Mail-Nachrichten enthalten, die durch IRM geschützt sind.</li><li>Besprechungsteilnehmer können neue Start-und Endzeit für Besprechungen vorschlagen und diese in Ihre Besprechungsantwort einbeziehen.</li><li>Die [GetUserSettings](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice.getusersettings%28v=exchg.80%29.aspx) -Methode der SOAP-AutoErmittlung gibt jetzt die [GroupingInformation](https://msdn.microsoft.com/library/office/dn529149%28v=exchg.150%29.aspx) -Einstellung zurück, die verwendet wird, um die Affinität für ein Mehrfaches Post Fach Ereignisabonnement beizubehalten.</li></ul> |
|Exchange 2013  | Enthält alle Features, die in Exchange 2010 SP2 eingeführt wurden. Die folgenden Features wurden in Exchange 2013 eingeführt:  <ul><li>  Archivierung</li><li>eDiscovery</li><li>Personas</li><li>Aufbewahrungsrichtlinien</li><li>Einheitlicher Kontaktspeicher</li><li>Benutzerfotos</li></ul> |
|Exchange 2010 SP2  | Enthält alle Features, die in Exchange 2010 SP1 eingeführt wurden. Die folgenden Features wurden in Exchange 2010 SP2 eingeführt:  <ul><li>  Abrufen des Kennwortablaufs</li><li>DateTime-Genauigkeit</li><li>Aktualisierte Eigenschaftenbezeichner für Kontakte</li><li>Neue Szenarien für Identitätswechsel</li></ul> |
|Exchange 2010 SP1  | Enthält alle Features, die in Exchange 2010 eingeführt wurden. Die folgenden Features wurden in Exchange 2010 SP1 eingeführt:  <ul><li>  Erstellen, abrufen und Ändern von Posteingangsregeln</li><li>Programmgesteuerten Zugriff auf Archivpostfach</li><li>Konversations Aktionen</li><li>Firewall durchlaufen von Benachrichtigungen</li><li>Verbesserte Verwaltungsfunktionen</li><li>Verbesserte Unterstützung für gemischte Versionen</li><li>Unterstützung des Einschränkungs Schutzes</li><li>Steuerung des Anwendungszugriffs auf EWS</li><li>Unterstützung der Client Zertifikatauthentifizierung</li></ul> |
|Exchange 2010  | Enthält alle Features, die in Exchange 2007 SP1 eingeführt wurden. Die folgenden Features wurden in der ersten Version von Exchange 2010 eingeführt: <ul> <li>  Vollständige private Verteilerliste</li><li>Benutzer Konfigurationsobjekte</li><li>Ordner zugeordnete Elemente</li><li>Nachrichtenverfolgung</li><li>Unified Messaging</li><li>SOAP-AutoErmittlung  </li><li>Erweiterte Zeitzonenunterstützung</li><li>Informationen zur Raum Ressourcenverfügbarkeit</li><li>Indizierte Suche</li><li>Zugriff auf den Papierkorb</li><li>E-Mail-Infos</li></ul> |
|Exchange 2007 SP1  | Enthält alle Features, die in Exchange 2007 eingeführt wurden. Die folgenden Features wurden in Exchange 2007 SP1 eingeführt:  <ul><li>  Delegieren der Verwaltung</li><li>Ordnerberechtigungen</li><li>Öffentliche Ordner</li><li>Bereitstellungselemente</li><li>ID-Konvertierung</li></ul> |
|Exchange 2007  | Die folgenden Features wurden in der ersten Version von Exchange 2007 eingeführt:  <ul><li>  Vollzugriff auf Elemente, Ordner und Anlagen (erstellen, abrufen, aktualisieren, löschen)</li><li>Verfügbarkeit</li><li>Abwesenheitseinstellungen</li><li>Benachrichtigungen</li><li>Synchronisierung</li><li>Namensauflösung</li><li>Verteilerliste (DL)-Erweiterung</li><li>Suchen</li></ul> |
   
## <a name="see-also"></a>Siehe auch

- [Verwenden von Webdiensten in Exchange](start-using-web-services-in-exchange.md)
- [Migration zu Exchange-Technologien](../migrating-to-exchange-online-and-exchange-2013-technologies.md)
- [Erkunden von verwalteter EWS-API, EWS und Webdiensten in Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)  
    

