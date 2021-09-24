---
title: EWS-Funktionen in Exchange-Produktversionen
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 186c51dc-ec33-4a5d-b739-c9fcb1d4cdd3
description: EWS implementiert neue Funktionen in neuen Produktversionen. Verwenden Sie die Informationen in diesem Artikel, um zu bestimmen, ob die Version von Exchange, auf die Sie abzielen, Unterstützung für die Daten oder Features umfasst, auf die Sie zugreifen müssen.
ms.openlocfilehash: bccd0e84fc28f8a7366f0463e555cceec71aa181
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512282"
---
# <a name="ews-functionality-in-exchange-product-versions"></a>EWS-Funktionen in Exchange-Produktversionen

EWS implementiert neue Funktionen in neuen Produktversionen. Verwenden Sie die Informationen in diesem Artikel, um zu bestimmen, ob die Version von Exchange, auf die Sie abzielen, Unterstützung für die Daten oder Features umfasst, auf die Sie zugreifen müssen. 
  
In der folgenden Tabelle sind die Versionen von Exchange aufgeführt, die EWS und die wichtigsten Features enthalten, die in jeder Version eingeführt wurden.
  
## <a name="ews-features-by-product-version"></a>EWS-Features nach Produktversion

|**Produktversion**|**Features**|
|:-----|:-----|
|Office 365 und Exchange Online |Enthält alle Features in der aktuellen Version von Exchange zusätzlich zu allen neuen Features, die für Onlineclients hinzugefügt werden.  |
|Exchange 2013 SP1 | Enthält alle Features, die in Exchange 2013 eingeführt wurden. Die folgenden Features wurden in Exchange 2013 SP1 eingeführt:<ul><li>Lesebestätigungen können jetzt für Updates und Löschungen angehalten werden.</li><li>Sie können [moderierte](https://msdn.microsoft.com/library/43a89f71-8002-4cb0-b3c8-1c2b2597f227%28Office.15%29.aspx) Transportgenehmigungsinformationen abrufen.</li><li>Abstimmungsantworten können angezeigt werden.</li><li>Die [SetHoldOnMailboxes-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.setholdonmailboxes%28v=exchg.80%29.aspx) und der [SetHoldOnMailboxes-Vorgang](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) akzeptieren alle Parameter in einem einzelnen Objekt.</li><li>eDiscovery-Suchvorgänge können eine Sprache für Suchabfragen und ein kulturspezifisches Format für Datumsbereiche angeben.</li><li>Das [StreamingSubscriptionConnection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection%28v=exchg.80%29.aspx) -Objekt kann jetzt auf die [StreamingSubscription](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscription%28v=exchg.80%29.aspx) -Objekte zugreifen.</li><li>Unterhaltungen haben eine Einstellung, um anzugeben, ob sie E-Mail-Nachrichten enthalten, die durch IRM geschützt sind.</li><li>Besprechungsteilnehmer können neue Start- und Endzeiten für Besprechungen vorschlagen und sie in ihre Besprechungsantwort einbeziehen.</li><li>Die [GETUserSettings-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice.getusersettings%28v=exchg.80%29.aspx) der SOAP-AutoErmittlung gibt jetzt die [groupingInformation-Einstellung](https://msdn.microsoft.com/library/office/dn529149%28v=exchg.150%29.aspx) zurück, die verwendet wird, um die Affinität für ein Postfachereignisabonnement aufrechtzuerhalten.</li></ul> |
|Exchange 2013  | Enthält alle Features, die in Exchange 2010 SP2 eingeführt wurden. Die folgenden Features wurden in Exchange 2013 eingeführt:  <ul><li>  Archivierung</li><li>eDiscovery</li><li>Personas</li><li>Aufbewahrungsrichtlinien</li><li>Einheitlicher Kontaktspeicher</li><li>Benutzerfotos</li></ul> |
|Exchange 2010 SP2  | Enthält alle Features, die in Exchange 2010 SP1 eingeführt wurden. Die folgenden Features wurden in Exchange 2010 SP2 eingeführt:  <ul><li>  Kennwortablauf abrufen</li><li>DateTime-Genauigkeit</li><li>Aktualisierte Eigenschaftsbezeichner für Kontakte</li><li>Neue Identitätswechselszenarien</li></ul> |
|Exchange 2010 SP1  | Enthält alle Features, die in Exchange 2010 eingeführt wurden. Die folgenden Features wurden in Exchange 2010 SP1 eingeführt:  <ul><li>  Erstellen, Abrufen und Ändern von Posteingangsregeln</li><li>Programmgesteuerter Zugriff auf Archivpostfach</li><li>Unterhaltungsaktionen</li><li>Firewalldurchlaufbenachrichtigungen</li><li>Verbesserte Verwaltungsfunktionen</li><li>Verbesserte Unterstützung gemischter Versionen</li><li>Unterstützung des Drosselungsschutzes</li><li>Steuerung des Anwendungszugriffs auf EWS</li><li>Clientzertifikatauthentifizierungsunterstützung</li></ul> |
|Exchange 2010  | Enthält alle Features, die in Exchange 2007 SP1 eingeführt wurden. Die folgenden Features wurden in der ersten Version von Exchange 2010 eingeführt: <ul> <li>  Vollständige private Verteilerliste</li><li>Benutzerkonfigurationsobjekte</li><li>Zugeordnete Ordnerelemente</li><li>Nachrichtenverfolgung</li><li>Unified Messaging</li><li>SOAP-AutoErmittlung  </li><li>Erweiterte Zeitzonenunterstützung</li><li>Informationen zur Verfügbarkeit von Raumressourcen</li><li>Indizierte Suche</li><li>Dumpsterzugriff</li><li>E-Mail-Infos</li></ul> |
|Exchange 2007 SP1  | Enthält alle Features, die in Exchange 2007 eingeführt wurden. Die folgenden Features wurden in Exchange 2007 SP1 eingeführt:  <ul><li>  Stellvertretungsverwaltung</li><li>Ordnerberechtigungen</li><li>Öffentliche Ordner</li><li>Bereitstellungselemente</li><li>ID-Konvertierung</li></ul> |
|Exchange 2007  | Die folgenden Features wurden in der ersten Version von Exchange 2007 eingeführt:  <ul><li>  Vollzugriff auf Elemente, Ordner und Anlagen (Erstellen, Abrufen, Aktualisieren, Löschen)</li><li>Verfügbarkeit</li><li>Nicht mehr Office Einstellungen</li><li>Benachrichtigungen</li><li>Synchronisierung</li><li>Namensauflösung</li><li>Verteilerlistenerweiterung (DL)</li><li>Suche</li></ul> |
   
## <a name="see-also"></a>Siehe auch

- [Verwenden von Webdiensten in Exchange](start-using-web-services-in-exchange.md)
- [Migration zu Exchange-Technologien](../migrating-to-exchange-online-and-exchange-2013-technologies.md)
- [Erkunden von verwalteter EWS-API, EWS und Webdiensten in Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)  
    

