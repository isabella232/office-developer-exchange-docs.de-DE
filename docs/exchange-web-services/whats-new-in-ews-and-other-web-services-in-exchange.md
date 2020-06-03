---
title: Neuerungen in EWS und anderen Webdiensten in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: aff6328f-cff1-42a6-9a4d-ea4d2d0461cf
description: Informieren Sie sich über Neuigkeiten in EWS und Webdiensten in Exchange und die verwaltete EWS-API.
localization_priority: Priority
ms.openlocfilehash: 5e74ad9d4cf5083983c28e477fd50d48e2d7fbb6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529840"
---
# <a name="whats-new-in-ews-and-other-web-services-in-exchange"></a>Neuerungen in EWS und anderen Webdiensten in Exchange

Informieren Sie sich über Neuigkeiten in EWS und Webdiensten in Exchange und die verwaltete EWS-API.
  
Webdienste in Exchange wurden aktualisiert und enthalten neue Features. 
  
**Tabelle 1. Neue Webdienstfeatures in Exchange Online, Exchange 2013 und verwaltete EWS-API**

|Feature|Implementiert in Exchange Online|Implementiert in Exchange 2013|Implementiert im verwaltete EWS-API|
|:-----|:-----:|:-----:|:-----:|
|[eDiscovery](#eDisc) <br/> |Ja  <br/> |Ja  <br/> |Ja  <br/> |
|[Archivierung](#arch) <br/> |Ja  <br/> |Ja  <br/> |Ja  <br/> |
|[Personas](#personas) <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|[Einheitlicher Kontaktspeicher](#unified) <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|[Aufbewahrungsrichtlinien](#retentionpolicy) <br/> |Ja  <br/> |Ja  <br/> |Ja  <br/> |
|[Benutzerfotos](#userphoto) <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|[Mail-Apps für Outlook-Verwaltung](#ewsmailapps) <br/> |Ja  <br/> |Ja  <br/> |Ja  <br/> |
|[Vorschlagen einer neuen Besprechungszeit](#propose) <br/> |Ja  <br/> |Nein  <br/> |Nein  <br/> |

<a name="eDisc"> </a>

## <a name="ediscovery-in-ews"></a>eDiscovery in EWS

eDiscovery ist ein Webdienst für die Verbund Abfrage, mit dem externe Anwendungen wie SharePoint 2013 Abfragen von Exchange-Daten ausführen können. Die Ermittlung umfasst mehrere Phasen, darunter das identifizieren und beibehalten von Schlüsseldaten, das Ausmerzen und Überprüfen der Daten und das Erstellen von Daten vor Gericht. eDiscovery-Abfragen erleichtern den Ermittlungsprozess durch Bereitstellen eines einzelnen Discovery-Workflows in Exchange und SharePoint.
  
**Tabelle 2. EWS-Vorgänge und verwaltete EWS-API Methoden für die Verwendung von eDiscovery**

|**Name des Vorgangs**|**Von EWS verwaltete API-Methode**|**Beschreibung**|
|:-----|:-----|:-----|
|[GetDiscoverySearchConfiguration-Vorgang](https://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) <br/> |[Datei "ExchangeService. GetDiscoverySearchConfiguration ()](https://msdn.microsoft.com/library/jj670206%28v=exchg.80%29.aspx) <br/> |Ruft Konfigurationsinformationen für in-Place-Speicher, gespeicherte Ermittlungs suchen und die für die Ermittlungs Suche aktivierten Postfächer ab.  <br/> |
|[GetHoldOnMailboxes-Vorgang](https://msdn.microsoft.com/library/9157f329-80b4-4cd0-a158-378064966ae6%28Office.15%29.aspx) <br/> |[Datei "ExchangeService. GetHoldOnMailboxes ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getholdonmailboxes%28v=exchg.80%29.aspx) <br/> |Ruft den Status eines abfragebasierten haltebereichs ab, der mithilfe des **SetHoldOnMailboxes** -Vorgangs festgelegt wird.  <br/> |
|[GetNonIndexableItemDetails-Vorgang](https://msdn.microsoft.com/library/9279c3ad-f7c8-4bbc-b0a7-2c78416cb39a%28Office.15%29.aspx) <br/> |[Datei "ExchangeService. GetNonIndexableItemDetails ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getnonindexableitemdetails%28v=exchg.80%29.aspx) <br/> |Ruft Details zu Elementen ab, die nicht indiziert werden können. Dies umfasst, jedoch nicht auf die Element-ID, einen Fehlercode, eine Fehlerbeschreibung, bei dem Versuch, das Element zu indizieren, sowie zusätzliche Informationen zu dem Element.  <br/> |
|[GetNonIndexableItemStatistics-Vorgang](https://msdn.microsoft.com/library/ed077877-9d98-4434-b8b6-a4a905e7f7a6%28Office.15%29.aspx) <br/> |[Datei "ExchangeService. GetNonIndexableItemStatistics ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getnonindexableitemstatistics%28v=exchg.80%29.aspx) <br/> |Ruft die Anzahl der Elemente ab, die nicht in einem Postfach indiziert werden können.  <br/> |
|[GetSearchableMailboxes-Vorgang](https://msdn.microsoft.com/library/47f8ff57-4835-4d2d-9136-44afb31a4cbe%28Office.15%29.aspx) <br/> |[Datei "ExchangeService. GetSearchableMailboxes ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getsearchablemailboxes%28v=exchg.80%29.aspx) <br/> |Ruft eine Liste von Postfächern ab, für die der Client über die Berechtigung zum Durchsuchen oder Ausführen von eDiscovery verfügt.  <br/> |
|[SearchMailboxes-Vorgang](https://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |[Datei "ExchangeService. SearchMailboxes ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.searchmailboxes%28v=exchg.80%29.aspx) <br/> |Sucht nach Elementen in bestimmten Postfächern, die Abfrageschlüsselwörtern entsprechen.  <br/> |
|[SetHoldOnMailboxes-Vorgang](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) <br/> |[Datei "ExchangeService. SetHoldOnMailboxes ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.setholdonmailboxes%28v=exchg.80%29.aspx) <br/> |Legt einen abfragebasierten Haltebereich für Elemente fest.  <br/> |

<a name="arch"> </a>

## <a name="archiving-in-ews"></a>Archivierung in EWS

Archivpostfächer sind sekundäre Postfächer, die einem Benutzer zugeordnet sind. Archivpostfächer werden in der Regel zum Verwalten von e-Mail-Speichergrenzwerten verwendet. Beispielsweise können ältere e-Mail-Elemente in regelmäßigen Abständen aus dem Posteingang in das Archivpostfach verschoben werden. 
  
Exchange stellt zwei neue EWS-Vorgänge vor, die Sie zum Archivieren einer Gruppe von e-Mail-Elementen aus einem primären Postfach verwenden können. Wenn Sie Posteingangs Elemente auf diese Weise archivieren, wird die Ordnerhierarchie der Elemente beibehalten. Darüber hinaus können Archivpostfächer nun entweder lokal auf einem Client oder Remote in einer für einen Benutzer undurchsichtigen Weise gespeichert werden, indem ein Ordnerpfad verwendet wird, um auf den Inhalt des Archivs zu deuten.
  
**Tabelle 3. EWS-Vorgänge und verwaltete EWS-API Methoden für das Arbeiten mit der Archivierung**

|**Name des Vorgangs**|**Von EWS verwaltete API-Methode**|**Beschreibung**|
|:-----|:-----|:-----|
|[ArchiveItem-Vorgang](https://msdn.microsoft.com/library/1af216b3-13ea-498e-b4fc-23513755d731%28Office.15%29.aspx) <br/> |[Datei "ExchangeService. ArchiveItems ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.archiveitems%28v=exchg.80%29.aspx) <br/> |Verschiebt ein Element aus dem primären Postfach in das Archivpostfach.  <br/> |
|[CreateFolderPath-Vorgang](https://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |Nicht implementiert.  <br/> |Erstellt eine Ordnerhierarchie in einem primären oder Archivpostfach.  <br/> |

<a name="personas"> </a>

## <a name="personas-in-ews"></a>Personas in EWS

Eine *Persona* ist eine Sammlung von Daten, die einer einzelnen Person zugeordnet ist. Die Daten können aus einer oder mehreren Quellen stammen und der Persona mithilfe einer gemeinsamen Link-ID zugeordnet werden. Mit Personas in EWS können Sie Informationen zu einer Person aus mehreren Quellen verknüpfen, suchen, durchsuchen und Abrufen und diese Informationen in einer einzigen logischen Entität organisieren. Personas unterscheiden sich von Kontakten darin, dass ein Kontakt eine Sammlung von Daten aus einer einzigen Quelle ist, die einer einzelnen Person zugeordnet ist. beispielsweise ein persönlicher Outlook-Kontakt oder ein Eintrag in einer globalen Adressliste (GAL). 
  
Die verwaltete EWS-API implementiert diese Funktion nicht.
  
> [!NOTE]
> Der einheitliche Kontaktspeicher macht auch die Persona-Funktionalität über die Vorgänge verfügbar, die dieses Feature unterstützen. 
  
**Tabelle 4. EWS-Vorgänge für das Arbeiten mit Personas**

|**Name des Vorgangs**|**Beschreibung**|
|:-----|:-----|
|[FindPeople-Vorgang](https://msdn.microsoft.com/library/446106b7-ff2d-4107-90c1-29f4d38ba128%28Office.15%29.aspx) <br/> |Gibt alle Persona-Objekte aus einem angegebenen Kontaktordner zurück oder ruft alle Kontakte ab, die mit einer angegebenen Abfragezeichenfolge übereinstimmen.  <br/> |
|[GetPersona-Vorgang](https://msdn.microsoft.com/library/e2146df0-53d0-4caf-9758-b600bbc14b6a%28Office.15%29.aspx) <br/> |Ruft eine Person ab.  <br/> |

<a name="unified"> </a>

## <a name="unified-contact-store-in-ews"></a>Einheitlicher Kontaktspeicher in EWS

Der einheitliche Kontaktspeicher ist ein Feature, das eine konsistente Kontakt Umgebung für Office-Produkte bietet und als Integrationspunkt für Drittanbieteranwendungen fungiert, um denselben Kontaktspeicher zu verwenden. Sie ermöglicht Benutzern und Anwendungen das Speichern, verwalten und Zugreifen auf Kontaktinformationen sowie die globale Verfügbarkeit zwischen lync, Exchange 2013, Outlook, Outlook Web App und allen anderen Anwendungen, die den Zugriff auf den einheitlichen Kontaktspeicher implementieren. Exchange ist der Kontaktspeicher für die Benutzeroberfläche für den einheitlichen Kontaktspeicher. 
  
Die verwaltete EWS-API implementiert diese Funktion nicht.
  
**Tabelle 5. EWS-Vorgänge für das Arbeiten mit dem einheitlichen Kontaktspeicher**

|**Name des Vorgangs**|**Beschreibung**|
|:-----|:-----|
|[AddNewImContactToGroup-Vorgang](https://msdn.microsoft.com/library/0cb5525f-faa3-48f1-9551-df55ffc26f46%28Office.15%29.aspx) <br/> |Fügt einer Gruppe einen neuen Chat Kontakt hinzu. Der einheitliche Kontaktspeicher kann maximal 1000 Kontakte enthalten.  <br/> |
|[AddImContactToGroup-Vorgang](https://msdn.microsoft.com/library/376acc42-2684-4596-aca1-82a4a10865c9%28Office.15%29.aspx) <br/> |Fügt einer Gruppe einen vorhandenen Chat Kontakt hinzu. Der einheitliche Kontaktspeicher kann maximal 1000 Kontakte enthalten.  <br/> |
|[AddImGroup-Vorgang](https://msdn.microsoft.com/library/6df6e504-b7c8-4773-b10f-ffa5defac229%28Office.15%29.aspx) <br/> |Fügt eine neue Chatgruppe hinzu. Der einheitliche Kontaktspeicher kann maximal 64 Gruppen enthalten.  <br/> |
|[AddNewTelUriContactToGroup-Vorgang](https://msdn.microsoft.com/library/c9688ce8-2465-45bb-8bd2-94b32ed4885c%28Office.15%29.aspx) <br/> |Fügt einer Gruppe basierend auf der Telefonnummer eines Kontakts einen neuen Kontakt hinzu.  <br/> |
|[AddDistributionGroupToImList-Vorgang](https://msdn.microsoft.com/library/5aa9bec8-71cf-4a6e-8ec8-b4965b40fd4a%28Office.15%29.aspx) <br/> |Fügt eine neue verteilerlistengruppe hinzu. Der einheitliche Kontaktspeicher kann maximal 64 Gruppen enthalten.  <br/> |
|[GetImItemList-Vorgang](https://msdn.microsoft.com/library/e31d14e1-0c1f-4b69-98b7-157d59c13698%28Office.15%29.aspx) <br/> |Ruft eine Liste von Chatgruppen und Chat Kontaktpersonen ab.  <br/> |
|[GetImItems-Vorgang](https://msdn.microsoft.com/library/51186691-46d2-4d5c-b8bc-4ee2bb20fbe7%28Office.15%29.aspx) <br/> |Ruft Informationen zu den angegebenen Chatgruppen und Chat Kontaktpersonen ab.  <br/> |
|[RemoveContactFromImList-Vorgang](https://msdn.microsoft.com/library/28ec96c3-45af-48ff-9f17-718a527dc0ad%28Office.15%29.aspx) <br/> |Entfernt den angegebenen Kontakt aus allen Chatgruppen.  <br/> |
|[RemoveImContactFromGroup-Vorgang](https://msdn.microsoft.com/library/a190bbec-c71b-4e6a-880b-55854c724d8c%28Office.15%29.aspx) <br/> |Entfernt einen Chat Kontakt aus einer Gruppe.  <br/> |
|[RemoveDistributionGroupFromImList-Vorgang](https://msdn.microsoft.com/library/252bddf2-98b6-4824-b548-2fba2bda5384%28Office.15%29.aspx) <br/> |Entfernt die angegebene Chat verteilerlistengruppe.  <br/> |
|[RemoveImGroup-Vorgang](https://msdn.microsoft.com/library/5e788016-68e0-4a3f-9243-03f6b6c6b389%28Office.15%29.aspx) <br/> |Entfernt die angegebene Chatgruppe.  <br/> |
|[SetImGroup-Vorgang](https://msdn.microsoft.com/library/2d48aa07-8152-4c3d-a519-061253e80174%28Office.15%29.aspx) <br/> |Ändert den Anzeigenamen einer Gruppe.  <br/> |

<a name="retentionpolicy"> </a>
  
## <a name="retention-policies-in-ews"></a>Aufbewahrungsrichtlinien in EWS

Aufbewahrungsrichtlinien sind Richtlinien, die in Exchange verwendet werden, um ein oder mehrere Aufbewahrungstags zu gruppieren, Aufbewahrungseinstellungen auf Ordner oder einzelne Elemente wie e-Mail-und Voicemailnachrichten anzuwenden und Aufbewahrungseinstellungen auf ein Postfach anzuwenden.
  
Exchange umfasst drei Typen von Aufbewahrungstags:
  
- Standardrichtlinientags, die für Postfachelemente gelten, für die kein anderer Aufbewahrungs tagstyp angewendet wurde.
    
- Richtlinien Tags für System Ordner, die auf Standardordner wie den Posteingang angewendet werden.
    
- Persönliche Tags, die ein Benutzer auf von Ihnen erstellte Ordner oder auf einzelne Elemente anwenden kann.
    
Einem Postfach kann nur eine Aufbewahrungsrichtlinie zugewiesen werden, aber die Richtlinie kann ein oder mehrere Aufbewahrungstags verschiedener Typen enthalten, die mit ihr verknüpft sind. Aufbewahrungstags können jederzeit mit einer Aufbewahrungsrichtlinie verknüpft oder mit ihr verknüpft werden. EWS in Exchange macht einen neuen Vorgang verfügbar, [GetUserRetentionPolicyTags](https://msdn.microsoft.com/library/57c6ff23-5c2c-42ee-824b-5a1b6dafab8c%28Office.15%29.aspx)und das verwaltete EWS-API eine neue Methode implementiert, [Datei "ExchangeService. GetUserRetentionPolicyTags ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getuserretentionpolicytags%28v=exchg.80%29.aspx), die eine Liste aller Tags bereitstellt, die mit einer Aufbewahrungsrichtlinie verknüpft sind. Sie können Aufbewahrungsrichtlinientags für Elemente und Ordner mithilfe der Vorgänge **CreateItem**, **CreateFolder**, **UpdateItem**, **UpdateFolder**, **GetItem**und **GetFolder** festlegen und abrufen. 

<a name="userphoto"> </a>

## <a name="requesting-user-photos"></a>Anfordern von Benutzer Fotos

Sie können Benutzer Fotos vom Exchange-Server anfordern, indem Sie eine der beiden Implementierungen des [GetUserPhoto-Vorgangs](https://msdn.microsoft.com/library/f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e%28Office.15%29.aspx)verwenden: [Rest](how-to-get-user-photos-by-using-ews-in-exchange.md) oder SOAP. Der Rest-Endpunkt verwendet eine standardmäßige HTTPS **Get** -Anforderung, um das Benutzer Foto zu erhalten. Der Dienst gibt entweder ein in Exchange gespeichertes Benutzer Foto oder ein Foto aus Active Directory-Domänendienste (AD DS) zurück. 
  
Die verwaltete EWS-API implementiert diese Funktion nicht. Sie können jedoch die verwaltete EWS-API verwenden, um Benutzer Fotos zurückzugeben, die in einem Postfach gespeichert sind, indem Sie das Foto abrufen, das an einen Kontakt angefügt ist.

<a name="blocksender"> </a>

## <a name="block-senders-and-mark-email-as-junk-in-ews"></a>Blockieren von Absendern und Markieren von e-Mails als Junk in EWS

Sie können jetzt Absender blockieren und e-Mails als Junk markieren, indem Sie den neuen [MarkAsJunk-Vorgang](https://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) in EWS oder die [Datei "ExchangeService. MarkAsJunk ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx) -Methode im verwaltete EWS-API verwenden. 

<a name="ewsmailapps"> </a>

## <a name="mail-apps-for-outlook"></a>Mail-Apps für Outlook

EWS bietet jetzt Unterstützung für die Verwaltung von Mail-Apps für Outlook. 
  
**Tabelle 6. EWS-Vorgänge und verwaltete EWS-API Methoden zum Arbeiten mit Mail-Apps für Outlook**

|**Name des Vorgangs**|**Von EWS verwaltete API-Methode**|**Beschreibung**|
|:-----|:-----|:-----|
|[DisableApp-Vorgang](https://msdn.microsoft.com/library/211731a3-2470-49af-bda3-1ddfc15a8e46%28Office.15%29.aspx) <br/> |[Datei "ExchangeService. DisableApp ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.disableapp%28v=exchg.80%29.aspx) <br/> |Deaktiviert eine installierte app.  <br/> |
|[GetAppManifests-Vorgang](https://msdn.microsoft.com/library/21a4987c-c24d-4a6e-ace4-e81edcda6303%28Office.15%29.aspx) <br/> |[Datei "ExchangeService. GetAppManifests ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getappmanifests%28v=exchg.80%29.aspx) <br/> |Ruft die APP-Manifeste für ein Postfach ab.  <br/> |
|[GetAppMarketplaceUrl-Vorgang](https://msdn.microsoft.com/library/2c016fc3-0e13-4624-9a5b-d3e84577a860%28Office.15%29.aspx) <br/> |[Datei "ExchangeService. GetAppMarketplaceUrl ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getappmarketplaceurl%28v=exchg.80%29.aspx) <br/> |Ruft die URL des App-Marktplatzes ab.  <br/> |
|[GetClientAccessToken-Vorgang](https://msdn.microsoft.com/library/086876cc-e22c-4e89-89f9-19e78af51217%28Office.15%29.aspx) <br/> |[Datei "ExchangeService. GetClientAccessToken ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getclientaccesstoken%28v=exchg.80%29.aspx) <br/> |Ruft Clientzugriffs Token ab.  <br/> |
|[InstallApp-Vorgang](https://msdn.microsoft.com/library/596eae95-3e78-489a-8bb2-d2dd4a026405%28Office.15%29.aspx) <br/> |[Datei "ExchangeService. InstallApp ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.installapp%28v=exchg.80%29.aspx) <br/> |Installiert eine APP für ein Postfach.  <br/> |
|[UninstallApp-Vorgang](https://msdn.microsoft.com/library/7707aa6a-381d-43f7-a454-54f6343ed127%28Office.15%29.aspx) <br/> |[Datei "ExchangeService. UninstallApp](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.uninstallapp%28v=exchg.80%29.aspx) <br/> |Deinstalliert eine APP aus einem Postfach.  <br/> |

<a name="propose"> </a>

## <a name="propose-new-meeting-time"></a>Vorschlagen einer neuen Besprechungszeit

Das Feature "neue Zeit vorschlagen" wurde in Version 15.00.0800.007 von Exchange eingeführt. Dadurch können Besprechungsteilnehmer [neue Besprechungszeiten](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md) für den Besprechungsorganisator vorschlagen. 
  
Die verwaltete EWS-API implementiert diese Funktion nicht.
  
## <a name="see-also"></a>Siehe auch

- [Erkunden von verwalteter EWS-API, EWS und Webdiensten in Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)  
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)
- [Mail-Apps für Outlook und EWS in Exchange](mail-apps-for-outlook-and-ews-in-exchange.md)
- [Archivierung in EWS in Exchange](archiving-in-ews-in-exchange.md)
- [eDiscovery in EWS in Exchange](ediscovery-in-ews-in-exchange.md)
- [Personen und Kontakte in EWS in Exchange](people-and-contacts-in-ews-in-exchange.md)
    

