---
title: EWS-Funktionalität in Exchange-Produktversionen
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 186c51dc-ec33-4a5d-b739-c9fcb1d4cdd3
description: EWS implementiert neuen Funktionen in neue Produktversionen. Verwenden Sie die Informationen in diesem Artikel, um festzustellen, ob die Version von Exchange Sie vorgesehenen bietet Unterstützung für die Daten oder Features, die Sie Zugriff auf.
ms.openlocfilehash: 6b676781f25eeeb90fd9ab075fbe63198766bd99
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756831"
---
# <a name="ews-functionality-in-exchange-product-versions"></a>EWS-Funktionalität in Exchange-Produktversionen

EWS implementiert neuen Funktionen in neue Produktversionen. Verwenden Sie die Informationen in diesem Artikel, um festzustellen, ob die Version von Exchange Sie vorgesehenen bietet Unterstützung für die Daten oder Features, die Sie Zugriff auf. 
  
Die folgende Tabelle enthält die Versionen von Exchange, die Exchange-Webdienste und die wichtigsten Features, die eingeführt wurden in jeder Version enthalten.
  
## <a name="ews-features-by-product-version"></a>EWS-Features von Produktversion

|**Version des Produkts**|**Features**|
|:-----|:-----|
|Office 365 und Exchange Online |Enthält alle Features in der aktuellen Version von Exchange neben alle neuen Features, die für online-Clients hinzugefügt werden.  |
|Exchange 2013 SP1 | Enthält alle Features in Exchange 2013 eingeführt. Die folgenden Funktionen wurden in Exchange 2013 SP1 eingeführt:<ul><li>Lesebestätigungen können nun für Aktualisierungen und Löschvorgänge angehalten werden.</li><li>Sie können [moderiert Transport](http://msdn.microsoft.com/library/43a89f71-8002-4cb0-b3c8-1c2b2597f227%28Office.15%29.aspx) Genehmigungsinformationen abrufen.</li><li>Abstimmungsantworten kann angezeigt werden.</li><li>Die [SetHoldOnMailboxes](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.setholdonmailboxes%28v=exchg.80%29.aspx) -Methode und den Betrieb von [SetHoldOnMailboxes](http://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) akzeptieren alle Parameter in ein einzelnes Objekt aus.</li><li>eDiscovery-suchen können eine Sprache für Suchabfragen und ein kulturspezifische Format für Datumsbereiche angeben.</li><li>Das Objekt [StreamingSubscriptionConnection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection%28v=exchg.80%29.aspx) kann nun die Objekte [StreamingSubscription](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.streamingsubscription%28v=exchg.80%29.aspx) zugreifen.</li><li>Unterhaltungen haben eine Einstellung, um anzugeben, ob sie e-Mail-Nachrichten enthalten, die durch IRM geschützt sind.</li><li>Besprechungsteilnehmer kann neue Anfangs- und Endzeit für Besprechungen vorschlagen und in ihre Besprechungsantwort einbinden.</li><li>Die SOAP-AutoErmittlung [GetUserSettings](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice.getusersettings%28v=exchg.80%29.aspx) -Methode jetzt gibt den [Werten "groupinginformation"](http://msdn.microsoft.com/EN-US/library/office/dn529149%28v=exchg.150%29.aspx) festlegen, die verwendeten verwalten Affinität für ein Abonnement der mehrere Postfach-Ereignis.</li></ul> |
|Exchange 2013  | Enthält alle Features, die in Exchange 2010 SP2. Die folgenden Funktionen wurden in Exchange 2013 eingeführt:  <ul><li>  Archivierung</li><li>eDiscovery</li><li>Personas</li><li>Aufbewahrungsrichtlinien</li><li>Einheitlicher Kontaktspeicher</li><li>Benutzerfotos</li></ul> |
|Exchange 2010 SP2  | Enthält alle Features, die in Exchange 2010 SP1 eingeführt. Die folgenden Funktionen wurden in Exchange 2010 SP2 eingeführt:  <ul><li>  Abrufen des Kennwortablaufs</li><li>DateTime mit doppelter Genauigkeit</li><li>Aktualisierte Eigenschaftenbezeichner für Kontakte</li><li>Neue Szenarien der Identitätswechsel</li></ul> |
|Exchange 2010 SP1  | Enthält alle Features, die in Exchange 2010 eingeführt. Die folgenden Funktionen wurden in Exchange 2010 SP1 eingeführt:  <ul><li>  Erstellen, abrufen und Ändern von Posteingangsregeln</li><li>Den programmgesteuerten Zugriff auf Archivpostfach</li><li>Unterhaltungen Aktionen</li><li>Durchlaufen von Benachrichtigungen der Firewall</li><li>Verbesserte Verwaltungsfeatures</li><li>Verbesserte Unterstützung für gemischte version</li><li>Drosselung Protection-Unterstützung</li><li>Steuerung der Anwendungszugriff auf Exchange-Webdienste</li><li>Clientunterstützung Zertifikat-Authentifizierung</li></ul> |
|Exchange 2010  | Enthält alle Features in Exchange 2007 SP1 eingeführt. Die folgenden Funktionen wurden in der ursprünglich freigegebenen Version von Exchange 2010 eingeführt: <ul> <li>  Vollständige Private Verteilerliste</li><li>Konfiguration der Benutzerobjekte</li><li>Ordner zugewiesene Elemente</li><li>Nachrichtenverfolgung</li><li>Unified Messaging</li><li>SOAP-AutoErmittlung  </li><li>Verbesserte Unterstützung der Zeitzone</li><li>Informationen zur Verfügbarkeit Raum Ressource</li><li>Indizierte Suche</li><li>Dumpster Zugriff</li><li>E-Mail-Infos Informationen</li></ul> |
|Exchange 2007 SP1  | Enthält alle Features, die in Exchange 2007 eingeführt. Die folgenden Funktionen wurden in Exchange 2007 SP1 eingeführt:  <ul><li>  Delegieren der Verwaltung</li><li>Berechtigungen für Ordner</li><li>Öffentliche Ordner</li><li>Bereitstellungselemente</li><li>ID-Konvertierung</li></ul> |
|Exchange 2007  | Die folgenden Funktionen wurden in der ursprünglich freigegebenen Version von Exchange 2007 eingeführt:  <ul><li>  Vollzugriff auf den Elemente, Ordner und Anlagen (erstellen, abrufen, Update, Delete)</li><li>Verfügbarkeit</li><li>Nicht genügend Einstellungen für Office</li><li>Benachrichtigungen</li><li>Synchronisierung</li><li>Namensauflösung</li><li>Erweiterung der Verteilerliste (DL)</li><li>Suchen</li></ul> |
   
## <a name="see-also"></a>Siehe auch

- [Erste Schritte mit Webdiensten in Exchange](start-using-web-services-in-exchange.md)
- [Migration zu Exchange-Technologien](../migrating-to-exchange-online-and-exchange-2013-technologies.md)
- [Erkunden von verwalteter EWS-API, EWS und Webdiensten in Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)  
    

