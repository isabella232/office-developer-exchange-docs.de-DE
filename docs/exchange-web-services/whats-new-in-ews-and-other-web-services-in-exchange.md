---
title: What's new in Exchange-Webdienste und andere Webdienste in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: aff6328f-cff1-42a6-9a4d-ea4d2d0461cf
description: Informieren Sie sich über Neuheiten in EWS- und Webdienste in Exchange und die EWS Managed API.
ms.openlocfilehash: 9e848babc96707152be767f42b561a587fc6cff0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757139"
---
# <a name="whats-new-in-ews-and-other-web-services-in-exchange"></a>What's new in Exchange-Webdienste und andere Webdienste in Exchange

Informieren Sie sich über Neuheiten in EWS- und Webdienste in Exchange und die EWS Managed API.
  
Webdienste in Exchange wurden aktualisiert, um den neuen Features gehören. 
  
**In Tabelle 1. Webdienst neue Funktionen in Exchange Online, Exchange 2013 und die EWS Managed API**

|Feature|Implementiert in Exchange Online|Implementiert in Exchange 2013|In der verwalteten EWS-API implementiert|
|:-----|:-----:|:-----:|:-----:|
|[eDiscovery](#eDisc) <br/> |Ja  <br/> |Ja  <br/> |Ja  <br/> |
|[Archivierung](#arch) <br/> |Ja  <br/> |Ja  <br/> |Ja  <br/> |
|[Rollen](#personas) <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|[Einheitlicher Kontaktspeicher](#unified) <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|[Aufbewahrungsrichtlinien](#retentionpolicy) <br/> |Ja  <br/> |Ja  <br/> |Ja  <br/> |
|[Benutzerfotos](#userphoto) <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|[Mail-apps für Outlook-Verwaltung](#ewsmailapps) <br/> |Ja  <br/> |Ja  <br/> |Ja  <br/> |
|[Neue Besprechungszeit vorschlagen](#propose) <br/> |Ja  <br/> |Nein  <br/> |Nein  <br/> |

<a name="eDisc"> </a>

## <a name="ediscovery-in-ews"></a>eDiscovery in EWS

eDiscovery ist ein Verbundpartner Query-Webdienst, mit der externe Anwendungen, wie SharePoint 2013, zum Abfragen von Exchange-Daten ausführen kann. Ermittlung besteht aus mehreren Phasen, einschließlich identifizieren und Beibehalten von wichtigen Daten, culling nach unten und Überprüfen der Daten und Daten in gerichtlichen erzeugt. eDiscovery-Abfragen erleichtern den Suchprozess durch Bereitstellen eines einzelnen Discovery Workflows über Exchange und SharePoint.
  
**In Tabelle 2. EWS-Vorgänge und EWS Managed API-Methoden zum Arbeiten mit eDiscovery**

|**Name des Vorgangs**|**EWS Managed API-Methode**|**Beschreibung**|
|:-----|:-----|:-----|
|[GetDiscoverySearchConfiguration-Vorgang](http://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) <br/> |[ExchangeService.GetDiscoverySearchConfiguration()](http://msdn.microsoft.com/en-us/library/jj670206%28v=exchg.80%29.aspx) <br/> |Ruft die Konfigurationsinformationen für Compliance-Archive, gespeicherte Discovery-Suche und die Postfächer, die für die Ermittlung Suche aktiviert sind.  <br/> |
|[GetHoldOnMailboxes-Vorgang](http://msdn.microsoft.com/library/9157f329-80b4-4cd0-a158-378064966ae6%28Office.15%29.aspx) <br/> |[ExchangeService.GetHoldOnMailboxes()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getholdonmailboxes%28v=exchg.80%29.aspx) <br/> |Ruft den Status einer abfragebasierte Aufbewahrung, die mit der Operation **SetHoldOnMailboxes** festgelegt ist.  <br/> |
|[GetNonIndexableItemDetails-Vorgang](http://msdn.microsoft.com/library/9279c3ad-f7c8-4bbc-b0a7-2c78416cb39a%28Office.15%29.aspx) <br/> |[ExchangeService.GetNonIndexableItemDetails()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getnonindexableitemdetails%28v=exchg.80%29.aspx) <br/> |Ruft die Details zu den Elementen, die nicht indiziert werden können. Dies umfasst, aber es ist nicht beschränkt auf, die Element-ID, ein Fehlercode, eine fehlerbeschreibung, wenn versucht wurde, das Element und zusätzliche Informationen zu dem Element zu indizieren.  <br/> |
|[GetNonIndexableItemStatistics-Vorgang](http://msdn.microsoft.com/library/ed077877-9d98-4434-b8b6-a4a905e7f7a6%28Office.15%29.aspx) <br/> |[ExchangeService.GetNonIndexableItemStatistics()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getnonindexableitemstatistics%28v=exchg.80%29.aspx) <br/> |Ruft die Anzahl der Elemente, die nicht indiziert werden in einem Postfach an.  <br/> |
|[GetSearchableMailboxes-Vorgang](http://msdn.microsoft.com/library/47f8ff57-4835-4d2d-9136-44afb31a4cbe%28Office.15%29.aspx) <br/> |[ExchangeService.GetSearchableMailboxes()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getsearchablemailboxes%28v=exchg.80%29.aspx) <br/> |Ruft einer Liste der Postfächer, die der Client verfügt über die Berechtigung zum Durchsuchen oder zum Ausführen von eDiscovery auf.  <br/> |
|[SearchMailboxes-Vorgang](http://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |[ExchangeService.SearchMailboxes()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.searchmailboxes%28v=exchg.80%29.aspx) <br/> |Sucht nach Elementen in bestimmte Postfächer, die von Abfrageschlüsselwörtern entsprechen.  <br/> |
|[SetHoldOnMailboxes-Vorgang](http://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) <br/> |[ExchangeService.SetHoldOnMailboxes()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.setholdonmailboxes%28v=exchg.80%29.aspx) <br/> |Legt ein abfragebasiertes enthalten Elemente.  <br/> |

<a name="arch"> </a>

## <a name="archiving-in-ews"></a>Archivierung in Exchange-Webdienste

Archivpostfächer sind sekundäre Postfächer, die einem Benutzer zugeordnet sind. Archivpostfächer sind in der Regel zum Verwalten von Speichergrenzen für e-Mail verwendet. Beispielsweise könnte der älteren e-Mail-Elemente in regelmäßigen Abständen aus dem Posteingang in das Archivpostfach verschoben werden. 
  
Exchange führt zwei neue EWS-Vorgänge, die Sie verwenden können, um eine Reihe von e-Mail-Elementen aus einem primären Postfach archivieren. Archivierung von Elementen im Posteingang auf diese Weise wird die Hierarchie der Ordner Elemente beibehalten. Darüber hinaus können archivpostfächer jetzt gespeichert werden, entweder lokal auf einem Client oder Remote, in eine Möglichkeit, die mit einem Ordnerpfad auf den Inhalt des Archivs zeigen hauptsächlich an einen Benutzer nicht transparent ist.
  
**Tabelle 3. EWS-Vorgänge und EWS Managed API-Methoden zum Arbeiten mit der Archivierung**

|**Name des Vorgangs**|**EWS Managed API-Methode**|**Beschreibung**|
|:-----|:-----|:-----|
|[ArchiveItem-Vorgang](http://msdn.microsoft.com/library/1af216b3-13ea-498e-b4fc-23513755d731%28Office.15%29.aspx) <br/> |[ExchangeService.ArchiveItems()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.archiveitems%28v=exchg.80%29.aspx) <br/> |Verschiebt ein Element aus dem Hauptpostfach in das Archivpostfach.  <br/> |
|[CreateFolderPath-Vorgang](http://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |Nicht implementiert.  <br/> |Erstellt ein Ordner-Hierarchie in einem primären oder Archivpostfach.  <br/> |

<a name="personas"> </a>

## <a name="personas-in-ews"></a>Rollen im Exchange-Webdienste

Eine *Rolle* ist eine Auflistung von Daten, die eine einzelne Person zugeordnet ist. Die Daten können von einer oder mehreren Quellen stammen und die Rolle über eine gemeinsame Link-ID zugeordnet ist Rollen im EWS können Sie verknüpfen, suchen, durchsuchen und Abrufen von Informationen über eine Person aus mehreren Quellen und organisieren, die betreffenden Informationen in einer einzigen logischen Entität. Rollen unterscheiden sich von Kontakten, ein Kontakt eine Sammlung von Daten aus einer Hand ist, die eine einzelne Person zugeordnet ist. beispielsweise einen persönlichen Outlook-Kontakt oder einen Eintrag in einer globalen Adressliste (GAL). 
  
[!HINWEIS] Die verwaltete EWS-API implementiert diese Funktion nicht.
  
> [!NOTE]
> Der einheitliche Kontaktspeicher macht Persona Funktionen auch über die Vorgänge, die dieses Feature unterstützen. 
  
**In Tabelle 4. EWS-Vorgänge für die Arbeit mit Rollen**

|**Name des Vorgangs**|**Beschreibung**|
|:-----|:-----|
|[FindPeople-Vorgang](http://msdn.microsoft.com/library/446106b7-ff2d-4107-90c1-29f4d38ba128%28Office.15%29.aspx) <br/> |Gibt alle Persona-Objekte aus einem angegebenen Kontaktordner oder ruft alle Kontakte, die mit eine Zeichenfolge der angegebenen Abfrage übereinstimmen.  <br/> |
|[GetPersona-Vorgang](http://msdn.microsoft.com/library/e2146df0-53d0-4caf-9758-b600bbc14b6a%28Office.15%29.aspx) <br/> |Ruft eine Rolle.  <br/> |

<a name="unified"> </a>

## <a name="unified-contact-store-in-ews"></a>Einheitlicher Kontaktspeicher in Exchange-Webdienste

Der einheitliche Kontaktspeicher ist ein Feature, bietet ein konsistentes Kontakt über Office-Produkte und fungiert als einen Integrationspunkt, der für Drittanbieter-Anwendungen auf dem gleichen Kontaktspeicher verwenden. Es ermöglicht den Benutzer und-Anwendungen zu speichern, verwalten und Kontaktinformationen zugreifen und zwischen Lync, Exchange 2013, Outlook, Outlook Web App und einer anderen Anwendung, die Zugriff auf der einheitliche Kontaktspeicher implementiert global zur Verfügung gestellt. Exchange ist die Kontaktspeicher für den einheitlichen Kontaktspeicher wünschen. 
  
[!HINWEIS] Die verwaltete EWS-API implementiert diese Funktion nicht.
  
**Tabelle 5. EWS-Vorgänge für die Arbeit mit der einheitliche Kontaktspeicher**

|**Name des Vorgangs**|**Beschreibung**|
|:-----|:-----|
|[AddNewImContactToGroup-Vorgang](http://msdn.microsoft.com/library/0cb5525f-faa3-48f1-9551-df55ffc26f46%28Office.15%29.aspx) <br/> |Fügt einen neuen Instant Messaging-Kontakt zu einer Gruppe. Der einheitliche Kontaktspeicher kann bis zu 1000 Kontakte enthalten.  <br/> |
|[AddImContactToGroup-Vorgang](http://msdn.microsoft.com/library/376acc42-2684-4596-aca1-82a4a10865c9%28Office.15%29.aspx) <br/> |Fügt einen vorhandenen Kontakt Sofortnachrichten zu einer Gruppe. Der einheitliche Kontaktspeicher kann bis zu 1000 Kontakte enthalten.  <br/> |
|[AddImGroup-Vorgang](http://msdn.microsoft.com/library/6df6e504-b7c8-4773-b10f-ffa5defac229%28Office.15%29.aspx) <br/> |Fügt eine neue Gruppe von Sofortnachrichten. Der einheitliche Kontaktspeicher kann maximal 64 Gruppen enthalten.  <br/> |
|[AddNewTelUriContactToGroup-Vorgang](http://msdn.microsoft.com/library/c9688ce8-2465-45bb-8bd2-94b32ed4885c%28Office.15%29.aspx) <br/> |Fügt einen neuen Kontakt zu einer Gruppe basierend auf Telefonnummer des Kontakts an.  <br/> |
|[AddDistributionGroupToImList-Vorgang](http://msdn.microsoft.com/library/5aa9bec8-71cf-4a6e-8ec8-b4965b40fd4a%28Office.15%29.aspx) <br/> |Fügt eine neue Liste Verteilergruppe an. Der einheitliche Kontaktspeicher kann maximal 64 Gruppen enthalten.  <br/> |
|[GetImItemList-Vorgang](http://msdn.microsoft.com/library/e31d14e1-0c1f-4b69-98b7-157d59c13698%28Office.15%29.aspx) <br/> |Ruft eine Liste von Instant Messaging-Gruppen und Instant Messaging-Kontakt Rollen.  <br/> |
|[GetImItems-Vorgang](http://msdn.microsoft.com/library/51186691-46d2-4d5c-b8bc-4ee2bb20fbe7%28Office.15%29.aspx) <br/> |Ruft Informationen zu den angegebenen Instant Messaging-Gruppen und Instant Messaging-Kontakt Rollen.  <br/> |
|[RemoveContactFromImList-Vorgang](http://msdn.microsoft.com/library/28ec96c3-45af-48ff-9f17-718a527dc0ad%28Office.15%29.aspx) <br/> |Entfernt den angegebenen Kontakt aus allen Gruppen von Sofortnachrichten.  <br/> |
|[RemoveImContactFromGroup-Vorgang](http://msdn.microsoft.com/library/a190bbec-c71b-4e6a-880b-55854c724d8c%28Office.15%29.aspx) <br/> |Entfernt einen Sofortnachrichten-Kontakt aus einer Gruppe.  <br/> |
|[RemoveDistributionGroupFromImList-Vorgang](http://msdn.microsoft.com/library/252bddf2-98b6-4824-b548-2fba2bda5384%28Office.15%29.aspx) <br/> |Entfernt die angegebene Verteilergruppe Liste Sofortnachrichten.  <br/> |
|[RemoveImGroup-Vorgang](http://msdn.microsoft.com/library/5e788016-68e0-4a3f-9243-03f6b6c6b389%28Office.15%29.aspx) <br/> |Entfernt die angegebene Gruppe von Instant Messaging.  <br/> |
|[SetImGroup-Vorgang](http://msdn.microsoft.com/library/2d48aa07-8152-4c3d-a519-061253e80174%28Office.15%29.aspx) <br/> |Ändert den Anzeigenamen einer Gruppe.  <br/> |

<a name="retentionpolicy"> </a>
  
## <a name="retention-policies-in-ews"></a>Aufbewahrungsrichtlinien in Exchange-Webdienste

Aufbewahrungsrichtlinien werden Richtlinien, die in Exchange, um eine Gruppe verwendet werden oder weitere aufbewahrungstags Anwenden von Einstellungen für die Aufbewahrung auf Ordner oder einzelne Elemente wie als e-Mail und Voicemail-Nachrichten und Einstellungen für die Aufbewahrung auf ein Postfach anwenden.
  
Exchange umfasst drei Typen von aufbewahrungstags:
  
- Standardrichtlinientags, die Postfachelemente liegen, die keine andere Art der zugewiesenen aufbewahrungstag aufweisen.
    
- System Ordner Richtlinie Tags, die zu Standardordnern wie beispielsweise dem Posteingang angewendet werden.
    
- Persönliche Tags, die ein Benutzer auf den Ordner, die sie erstellen oder auf einzelne Elemente anwenden können.
    
Nur eine Aufbewahrungsrichtlinie auf ein Postfach zugewiesen werden kann, aber die Richtlinie kann eine oder mehrere aufbewahrungstags der verschiedenen verknüpften aufweisen. Aufbewahrungstags können mit verknüpft oder aus einer Aufbewahrungsrichtlinie können Sie jederzeit aufgehoben werden. EWS in Exchange verfügbar macht eine neue Operation, [GetUserRetentionPolicyTags](http://msdn.microsoft.com/library/57c6ff23-5c2c-42ee-824b-5a1b6dafab8c%28Office.15%29.aspx), und die EWS Managed API implementiert eine neue Methode, [ExchangeService.GetUserRetentionPolicyTags()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getuserretentionpolicytags%28v=exchg.80%29.aspx), die eine Liste mit allen Tags bereitstellt, die mit einer Aufbewahrungsrichtlinie verknüpft sind. Sie können festlegen und Abrufen von aufbewahrungsrichtlinientags für Elemente und Ordner mithilfe der **CreateItem**, **CreateFolder**, **UpdateItem**, **UpdateFolder**, **GetItem**und **GetFolder** -Vorgänge. 

<a name="userphoto"> </a>

## <a name="requesting-user-photos"></a>Anfordern von benutzerfotos

Sie können benutzerfotos vom Exchange-Server mithilfe eines der beiden Implementierungen der [GetUserPhoto Vorgang](http://msdn.microsoft.com/library/f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e%28Office.15%29.aspx)anfordern: [Rest-](how-to-get-user-photos-by-using-ews-in-exchange.md) oder SOAP. Der REST-Endpunkt verwendet eine standard HTTPS **GET** -Anforderung, um das benutzerfoto abzurufen. Der Dienst wird entweder ein benutzerfoto in Exchange gespeichert oder Fotos aus Active Directory-Domänendienste (AD DS) zurückgeben. 
  
[!HINWEIS] Die verwaltete EWS-API implementiert diese Funktion nicht. Sie können, jedoch die EWS Managed API verwenden, um benutzerfotos zurückzugeben, die in einem Postfach gespeichert werden, indem die erste des Fotos, das die einem Kontakt zugeordnet ist.

<a name="blocksender"> </a>

## <a name="block-senders-and-mark-email-as-junk-in-ews"></a>Blockieren Sie den Absender und Markieren von e-Mails als Junk im EWS

Sie können jetzt Absender blockieren und Markieren von e-Mails als Junk-e-mit den neuen [MarkAsJunk Vorgang](http://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) im EWS oder die [ExchangeService.MarkAsJunk()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx) -Methode in die EWS Managed API. 

<a name="ewsmailapps"> </a>

## <a name="mail-apps-for-outlook"></a>Mail-Apps für Outlook

EWS bietet jetzt Unterstützung für die Verwaltung von Mail-apps für Outlook. 
  
**Tabelle 6. EWS-Vorgänge und EWS Managed API-Methoden zum Arbeiten mit mail-apps für Outlook**

|**Name des Vorgangs**|**EWS Managed API-Methode**|**Beschreibung**|
|:-----|:-----|:-----|
|[DisableApp-Vorgang](http://msdn.microsoft.com/library/211731a3-2470-49af-bda3-1ddfc15a8e46%28Office.15%29.aspx) <br/> |[ExchangeService.DisableApp()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.disableapp%28v=exchg.80%29.aspx) <br/> |Eine installierte app deaktiviert.  <br/> |
|[GetAppManifests-Vorgang](http://msdn.microsoft.com/library/21a4987c-c24d-4a6e-ace4-e81edcda6303%28Office.15%29.aspx) <br/> |[ExchangeService.GetAppManifests()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getappmanifests%28v=exchg.80%29.aspx) <br/> |Ruft die app-Manifeste für ein Postfach.  <br/> |
|[GetAppMarketplaceUrl-Vorgang](http://msdn.microsoft.com/library/2c016fc3-0e13-4624-9a5b-d3e84577a860%28Office.15%29.aspx) <br/> |[ExchangeService.GetAppMarketplaceUrl()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getappmarketplaceurl%28v=exchg.80%29.aspx) <br/> |Ruft die URL der app-Marketplace.  <br/> |
|[GetClientAccessToken-Vorgang](http://msdn.microsoft.com/library/086876cc-e22c-4e89-89f9-19e78af51217%28Office.15%29.aspx) <br/> |[ExchangeService.GetClientAccessToken()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getclientaccesstoken%28v=exchg.80%29.aspx) <br/> |Ruft Zugriffstoken ab.  <br/> |
|[InstallApp-Vorgang](http://msdn.microsoft.com/library/596eae95-3e78-489a-8bb2-d2dd4a026405%28Office.15%29.aspx) <br/> |[ExchangeService.InstallApp()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.installapp%28v=exchg.80%29.aspx) <br/> |Eine app für ein Postfach installiert.  <br/> |
|[UninstallApp-Vorgang](http://msdn.microsoft.com/library/7707aa6a-381d-43f7-a454-54f6343ed127%28Office.15%29.aspx) <br/> |[ExchangeService.UninstallApp](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.uninstallapp%28v=exchg.80%29.aspx) <br/> |Deinstalliert eine app aus einem Postfach an.  <br/> |

<a name="propose"> </a>

## <a name="propose-new-meeting-time"></a>Neue Besprechungszeit vorschlagen

Das neue Feature Zeit für vorschlagen wurde in Exchange-Version 15.00.0800.007 eingeführt. Dies ermöglicht Besprechungsteilnehmern, an den Besprechungsorganisator [Besprechungszeiten vorschlagen](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md) . 
  
[!HINWEIS] Die verwaltete EWS-API implementiert diese Funktion nicht.
  
## <a name="see-also"></a>Siehe auch

- [Erkunden von verwalteter EWS-API, EWS und Webdiensten in Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)  
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)
- [Mail-Apps für Outlook und EWS in Exchange](mail-apps-for-outlook-and-ews-in-exchange.md)
- [Archivierung in EWS in Exchange](archiving-in-ews-in-exchange.md)
- [eDiscovery in EWS in Exchange](ediscovery-in-ews-in-exchange.md)
- [Benutzer und Kontakte in EWS in Exchange](people-and-contacts-in-ews-in-exchange.md)
    

