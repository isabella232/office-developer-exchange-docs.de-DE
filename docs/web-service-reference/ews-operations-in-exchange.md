---
title: EWS-Operationen in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- Exchange
api_type:
- schema
ms.assetid: cf6fd871-9a65-4f34-8557-c8c71dd7ce09
description: Suchen nach Informationen zu in Exchange verfügbaren EWS-Vorgängen
localization_priority: Priority
ms.openlocfilehash: 143903d9198a7e31e876adcbbb336df34ecf01fa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526123"
---
# <a name="ews-operations-in-exchange"></a>EWS-Operationen in Exchange

Suchen nach Informationen zu in Exchange verfügbaren EWS-Vorgängen
  
Exchange-Webdienste stellen viele Vorgänge bereit, mit denen Sie auf Informationen aus dem Exchange-Speicher zugreifen können. Die Artikel in diesem Abschnitt stellen Informationen zur Gesamtstruktur der Anforderungen, Antworten und Fehlerantwortnachrichten für EWS-Vorgänge und XML-Beispiele für die einzelnen Vorgänge bereit. Sie stellen eine Übersicht zu den Nachrichtenstrukturen bereit, die zwischen Client und Server gesendet werden. Sie können diese Informationen zu Debuggen von Nachrichtenstrukturen und zum Suchen von Informationen darüber verwenden, was Sie in einer EWS-Anforderung ausführen können. Weitere Informationen dazu, was die XML-Struktur darstellt, finden Sie unter [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md).
  
Alle EWS-Funktionen beziehen sich auf eine Version des Schemas. In neuen Versionen von Exchange Server oder Exchange Online werden neue EWS-Schemaversionen eingeführt. Das [RequestServerVersion](requestserverversion.md)-Element enthält ein **Version**-Attribut, das der Schemaversion die Serverversion zuordnet. In diesem Artikel werden Informationen dazu bereitgestellt, wann die einzelnen Vorgänge eingeführt wurden. Für bestimmte Funktionen innerhalb eines Vorgangs ist möglicherweise eine spätere Version des Diensts erforderlich. Die Schemas mit Versionsangabe sind so implementiert, dass Clients, die für eine ältere Version von EWS vorgesehen sind, auch mit neueren EWS-Versionen funktionieren. 
  
Diese Vorgänge können auf den EW-Endpunkt abzielen, der Ihrem Postfach dient. Sie können zu dem EWS-Endpunkt navigieren, indem Sie eine URL verwenden, die der Struktur unter http://<clientaccessserver>.com/ews/exchange.asmx ähnelt, <clientaccessserver> steht dabei für den Exchange-Clientzugriffsserver, der Ihrem Postfach dient. Sie können diese AutoErmittlung zum Abrufen der URL auf dem Clientzugriffsserver verwenden, der Ihrem Postfach dient. Weitere Informationen zur AutoErmittlung finden Sie unter [AutoErmittlung für Exchange](../exchange-web-services/autodiscover-for-exchange.md).
  
## <a name="ediscovery-operations"></a>eDiscovery-Vorgänge
<a name="bk_eDiscovery"> </a>

Die eDiscovery-Vorgänge stellen Suchvorgänge für Legal Holds und zum Bezeichnen von Postfachdaten, die in discovery-Suchergebnissen nicht indiziert und zurückgegeben werden können.
  
In der folgenden Tabelle sind die eDiscovery-Vorgänge aufgeführt.
  
|**Name des Vorgangs**|**Eingeführt in**|
|:-----|:-----|
|[GetDiscoverySearchConfiguration-Vorgang](getdiscoverysearchconfiguration-operation.md) <br/> |Exchange 2013  <br/> |
|[GetHoldOnMailboxes-Vorgang](getholdonmailboxes-operation.md) <br/> |Exchange 2013  <br/> |
|[GetNonIndexableItemDetails-Vorgang](getnonindexableitemdetails-operation.md) <br/> |Exchange 2013  <br/> |
|[GetNonIndexableItemStatistics-Vorgang](getnonindexableitemstatistics-operation.md) <br/> |Exchange 2013  <br/> |
|[GetSearchableMailboxes-Vorgang](getsearchablemailboxes-operation.md) <br/> |Exchange 2013  <br/> |
|[SearchMailboxes-Vorgang](searchmailboxes-operation.md) <br/> |Exchange 2013  <br/> |
|[SetHoldOnMailboxes-Vorgang](setholdonmailboxes-operation.md) <br/> |Exchange 2013  <br/> |
   
## <a name="exchange-mailbox-data-operations"></a>Exchange-Postfachdatenvorgänge
<a name="bk_Exchange_mailbox_data"> </a>

Mit den Exchange-Postfachdatenvorgängen können Clients Elemente, Ordner und Anlagen sowie die Auflösung mehrdeutiger Namen und die Erweiterung von Verteilerlisten verarbeiten. Zu den Exchange-Postfachdatenvorgängen gehören Element-, Ordner-, Anlagen- und Hilfsprogrammvorgänge.
  
In der folgenden Tabelle sind die Exchange-Postfachdatenvorgänge aufgeführt.
  
|**Name des Vorgangs**|**Eingeführt in**|
|:-----|:-----|
|[ArchiveItem-Vorgang](archiveitem-operation.md) <br/> |Exchange 2013  <br/> |
|[CreateItem Operation](createitem-operation.md) <br/> |Exchange 2007  <br/> |
|[CopyItem Operation](copyitem-operation.md) <br/> |Exchange 2007  <br/> |
|[DeleteItem-Operation](deleteitem-operation.md) <br/> |Exchange 2007  <br/> |
|[FindItem-Vorgang](finditem-operation.md) <br/> |Exchange 2007  <br/> |
|[GetItem Operation](getitem-operation.md) <br/> |Exchange 2007  <br/> |
|[MarkAllItemsAsRead-Vorgang](markallitemsasread-operation.md) <br/> |Exchange 2013  <br/> |
|[MoveItem Operation](moveitem-operation.md) <br/> |Exchange 2007  <br/> |
|[SendItem Operation](senditem-operation.md) <br/> |Exchange 2007  <br/> |
|[UpdateItem Operation](updateitem-operation.md) <br/> |Exchange 2007  <br/> |
   
In der folgenden Tabelle sind die Exchange-Postfachdatenordnervorgänge aufgeführt.
  
|**Name des Vorgangs**|**Eingeführt in**|
|:-----|:-----|
|[CreateFolder Operation](createfolder-operation.md) <br/> |Exchange 2007  <br/> |
|[CreateFolderPath-Vorgang](createfolderpath-operation.md) <br/> |Exchange 2013  <br/> |
|[CreateManagedFolder-Vorgang](createmanagedfolder-operation.md) <br/> |Exchange 2007. Diese Funktion wurde in Versionen von Exchange ab Exchange 2010 herabgestuft. Informationen zur Migration hin zur Verwendung von Aufbewahrungstags und -richtlinien für die Verwaltung von Nachrichtendatensätzen finden Sie unter [Migrieren von verwalteten Ordnern](https://technet.microsoft.com/library/dd298032%28v=exchg.141%29.aspx).  <br/> |
|[CopyFolder-Vorgang](copyfolder-operation.md) <br/> |Exchange 2007  <br/> |
|[DeleteFolder-Vorgang](deletefolder-operation.md) <br/> |Exchange 2007  <br/> |
|[EmptyFolder-Vorgang](emptyfolder-operation.md) <br/> |Exchange 2010  <br/> |
|[FindFolder Operation](findfolder-operation.md) <br/> |Exchange 2007  <br/> |
|[GetFolder Operation](getfolder-operation.md) <br/> |Exchange 2007  <br/> |
|[MoveFolder-Vorgang](movefolder-operation.md) <br/> |Exchange 2007  <br/> |
|[UpdateFolder-Vorgang](updatefolder-operation.md) <br/> |Exchange 2007  <br/> |
   
In der folgenden Tabelle sind die Exchange-Postfachdatenanlagenvorgänge aufgeführt.
  
|**Name des Vorgangs**|**Eingeführt in**|
|:-----|:-----|
|[CreateAttachment-Vorgang](createattachment-operation.md) <br/> |Exchange 2007  <br/> |
|[GetAttachment-Vorgang](getattachment-operation.md) <br/> |Exchange 2007  <br/> |
|[DeleteAttachment-Vorgang](deleteattachment-operation.md) <br/> |Exchange 2007  <br/> |
   
In der folgenden Tabelle sind die Exchange-Postfacherinnerungsvorgänge aufgeführt.
  
|**Name des Vorgangs**|**Eingeführt in**|
|:-----|:-----|
|[GetReminders-Vorgang](getreminders-operation.md) <br/> |Exchange 2013  <br/> |
|[PerformReminderAction-Vorgang](performreminderaction-operation.md) <br/> |Exchange 2013  <br/> |
   
In der folgenden Tabelle sind die Exchange-Postfachdatenkonvertierungsvorgänge aufgeführt.
  
|**Name des Vorgangs**|**Eingeführt in**|
|:-----|:-----|
|[ApplyConversationAction-Vorgang](applyconversationaction-operation.md) <br/> |Exchange 2010 Service Pack 1 (SP1)  <br/> |
|[FindConversation Operation](findconversation-operation.md) <br/> |Exchange 2010 SP1  <br/> |
|[GetConversationItems operation](getconversationitems-operation.md) <br/> |Exchange 2013  <br/> |
   
In der folgenden Tabelle sind die Exchange-Postfachdatenhilfsprogrammvorgänge aufgeführt.
  
|**Name des Vorgangs**|**Eingeführt in**|
|:-----|:-----|
|[ConvertId-Vorgang](convertid-operation.md) <br/> |Exchange 2007 Service Pack 1  <br/> |
|[Der ExpandDL-Vorgang](expanddl-operation.md) <br/> |Exchange 2007  <br/> |
|[GetUserPhoto-Vorgang](getuserphoto-operation.md) <br/> |Exchange 2013. Dieser Vorgang besitzt eine REST- und SOAP-Implementierung.  <br/> |
|[MarkAsJunk Operation](markasjunk-operation.md) <br/> |Exchange 2013  <br/> |
|[ResolveNames-Vorgang](resolvenames-operation.md) <br/> |Exchange 2007  <br/> |
|[GetPasswordExpirationDate-Vorgang](getpasswordexpirationdate-operation.md) <br/> |Exchange 2010 SP1  <br/> |
   
## <a name="availability-operations"></a>Verfügbarkeitsvorgänge
<a name="bk_Availability"> </a>

Verfügbarkeitsvorgänge verbessern den Kalender und die gemeinsame Nutzungserfahrung, indem sichere, aktuelle und umfangreiche Informationen bereitgestellt werden. Daten zur Belegung von Räumen sind eine wichtige Komponente bei der Planung von Besprechungen. Verfügbarkeitsvorgänge bieten eine zuverlässige Grundlage für eine effektive Planung. 
  
In der folgenden Tabelle werden die Verfügbarkeitsvorgänge aufgeführt.
  
|**Name des Vorgangs**|**Eingeführt in**|
|:-----|:-----|
|[GetUserAvailability-Vorgang](getuseravailability-operation.md) <br/> |Exchange 2007  <br/> |
|[GetRoomLists-Vorgang](getroomlists-operation.md) <br/> |Exchange 2010  <br/> |
|[GetRooms-Vorgang](getrooms-operation.md) <br/> |Exchange 2010  <br/> |
|[GetUserOofSettings-Vorgang](getuseroofsettings-operation.md) <br/> |Exchange 2007  <br/> |
|[SetUserOofSettings-Vorgang](setuseroofsettings-operation.md) <br/> |Exchange 2007  <br/> |
   
## <a name="bulk-transfer-operations"></a>Massenübertragungsvorgänge
<a name="bk_bulk_transfer"> </a>

Mit Massenübertragungsvorgängen können Clients Elemente in einem oder aus einem Postfach streamen. 
  
In der folgenden Tabelle werden die Massenübertragungsvorgänge aufgeführt.
  
|**Name des Vorgangs**|**Eingeführt in**|
|:-----|:-----|
|[UploadItems-Vorgang](uploaditems-operation.md) <br/> |Exchange 2010 SP1  <br/> |
|[ExportItems-Vorgang](exportitems-operation.md) <br/> |Exchange 2010 SP1  <br/> |
   
## <a name="delegate-management-operations"></a>Stellvertreter-Verwaltungsvorgänge
<a name="bk_delegate_management"> </a>

Mit Stellvertreter-Verwaltungsvorgängen können Clients Stellvertreter hinzufügen, abrufen, aktualisieren und Stellvertreter aus ihren Postfächern entfernen. 
  
In der folgenden Tabelle werden die Stellvertreter-Verwaltungsvorgänge aufgeführt.
  
|**Name des Vorgangs**|**Eingeführt in**|
|:-----|:-----|
|[AddDelegate-Vorgang](adddelegate-operation.md) <br/> |Exchange 2007 Service Pack 1 (SP1)  <br/> |
|[GetDelegate-Vorgang](getdelegate-operation.md) <br/> |Exchange 2007 SP1  <br/> |
|[UpdateDelegate-Vorgang](updatedelegate-operation.md) <br/> |Exchange 2007 SP1  <br/> |
|[RemoveDelegate-Vorgang](removedelegate-operation.md) <br/> |Exchange 2007 SP1  <br/> |
   
## <a name="inbox-rules-operations"></a>Posteingangsregelvorgänge
<a name="bk_inbox_rules"> </a>

Mit Posteingangsregelvorgängen können Clients Posteingangsregeln abrufen und sie für Nachrichten auf dem Server aktualisieren. Posteingangsregeln sind Bedingungssätze und zugeordnete Aktionen, mit denen Clients Nachrichten bei Zustellung im Ordner automatisch sortieren, kategorisieren und Vorgänge zu Nachrichten ausführen können. 
  
In der folgenden Tabelle werden die Posteingangsregelvorgänge aufgeführt.
  
|**Name des Vorgangs**|**Eingeführt in**|
|:-----|:-----|
|[GetInboxRules-Vorgang](getinboxrules-operation.md) <br/> |Exchange 2010 SP1  <br/> |
|[UpdateInboxRules-Vorgang](updateinboxrules-operation.md) <br/> |Exchange 2010 SP1  <br/> |
   
## <a name="mail-app-management-operations"></a>Mail-App-Verwaltungsvorgänge
<a name="bk_mail_apps"> </a>

Mit Mail-App-Verwaltungsvorgängen können Sie Mail-Apps für Outlook verwalten. Sie können diese Vorgänge zum Installieren, Deinstallieren, Deaktivieren und zum Abrufen von Informationen über Mail-Apps verwenden, die für Outlook Web App und Outlook 2013 verfügbar sind.
  
In der folgenden Tabelle sind die Mail-App-Verwaltungsvorgänge aufgeführt.
  
|**Name des Vorgangs**|**Eingeführt in**|
|:-----|:-----|
|[DisableApp-Vorgang](disableapp-operation.md) <br/> |Exchange 2013  <br/> |
|[GetAppManifests-Vorgang](getappmanifests-operation.md) <br/> |Exchange 2013  <br/> |
|[GetAppMarketplaceUrl-Vorgang](getappmarketplaceurl-operation.md) <br/> |Exchange 2013  <br/> |
|[GetClientAccessToken-Vorgang](getclientaccesstoken-operation.md) <br/> |Exchange 2013  <br/> |
|[InstallApp-Vorgang](installapp-operation.md) <br/> |Exchange 2013  <br/> |
|[UninstallApp-Vorgang](uninstallapp-operation.md) <br/> |Exchange 2013  <br/> |
   
## <a name="mail-tips-operation"></a>E-Mail-Tipps-Vorgänge
<a name="bk_mail_tips"> </a>

Mit dem E-Mail-Tipps-Vorgang können Clients Informationen zu Empfängerpostfächern vom Server abrufen, wenn ein Autor eine Nachricht verfasst. In der folgenden Tabelle ist der E-Mail-Tipps-Vorgang aufgeführt.
  
|**Name des Vorgangs**|**Eingeführt in**|
|:-----|:-----|
|[GetMailTips-Vorgang](getmailtips-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="message-tracking-operations"></a>Nachrichtenverfolgungsvorgänge
<a name="bk_message_tracking"> </a>

Mit Nachrichtenverfolgungsvorgängen können Clients nach Nachrichten suchen, die bestimmte Kriterien erfüllen und detaillierte Informationen zu den Nachrichten in einem Nachrichtenverfolgungsbericht abrufen. 
  
In der folgenden Tabelle sind die Nachrichtenverfolgungsvorgänge aufgeführt.
  
|**Name des Vorgangs**|**Eingeführt in**|
|:-----|:-----|
|[FindMessageTrackingReport-Vorgang](findmessagetrackingreport-operation.md) <br/> |Exchange 2010  <br/> |
|[GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="notification-operations"></a>Benachrichtigungsvorgänge
<a name="bk_notification"> </a>

Benachrichtigungsvorgänge melden der Clientanwendung Ereignisse, die Elementen und Ordnern in einem bestimmten Postfach zugeordnet sind. Das Abonnementmodell können Push-, Pull- oder Streaming-basiert sein. 
  
In der folgenden Tabelle sind die Benachrichtigungsvorgänge aufgeführt.
  
|**Name des Vorgangs**|**Eingeführt in**|
|:-----|:-----|
|[GetEvents-Vorgang](getevents-operation.md) <br/> |Exchange 2007  <br/> |
|[GetStreamingEvents-Vorgang](getstreamingevents-operation.md) <br/> |Exchange 2010 SP1  <br/> |
|[Vorgang abonnieren](subscribe-operation.md) <br/> |Exchange 2007  <br/> |
|[Vorgang des Kündigens von Abonnements](unsubscribe-operation.md) <br/> |Exchange 2007  <br/> |
   
## <a name="persona-operations"></a>Persona-Vorgänge
<a name="bk_personas"> </a>

Die Persona-Vorgänge stellen eine Oberfläche zum Suchen und Abrufen von Informationen zu einem verknüpften Kontakt bereit. In der folgenden Tabelle sind die Persona-Vorgänge aufgeführt.
  
|**Name des Vorgangs**|**Eingeführt in**|
|:-----|:-----|
|[FindPeople-Vorgang](findpeople-operation.md) <br/> |Exchange 2013  <br/> |
|[GetPersona-Vorgang](getpersona-operation.md) <br/> |Exchange 2013  <br/> |
   
## <a name="retention-policy-operation"></a>Beibehaltungsrichtlinien-Vorgänge
<a name="bk_retention_policy"> </a>

Die Beibehaltungsrichtlinien-Vorgänge stellen eine Liste aller Beibehaltungstags bereit, die mit der Beibehaltungsrichtlinie eines Benutzers verknüpft sind. 
  
In der folgenden Tabelle sind die Beibehaltungsrichtlinien-Vorgänge aufgeführt.
  
|**Name des Vorgangs**|**Eingeführt in**|
|:-----|:-----|
|[GetUserRetentionPolicyTags-Vorgang](getuserretentionpolicytags-operation.md) <br/> |Exchange 2013  <br/> |
   
## <a name="service-configuration-operation"></a>Dienstkonfigurationsvorgänge
<a name="bk_service_config"> </a>

Mit Dienstkonfigurationsvorgängen können Clients Konfigurationsinformationen für Unified Messaging-, Schutzregel-, Richtlinientipps- und E-Mail-Tipps-Dienste abrufen. 
  
In der folgenden Tabelle sind die Dienstkonfigurationsvorgänge aufgeführt.
  
|**Name des Vorgangs**|**Eingeführt in**|
|:-----|:-----|
|[GetServiceConfiguration-Vorgang](getserviceconfiguration-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="sharing-operations"></a>Freigabevorgänge
<a name="bk_sharing"> </a>

Mit Freigabevorgängen können Clients Kalender- und Kontaktdaten freigeben. 
  
In der folgenden Tabelle sind die Freigabevorgänge aufgeführt.
  
|**Name des Vorgangs**|**Eingeführt in**|
|:-----|:-----|
|[CreateItem (AcceptSharingInvitation)](createitem-acceptsharinginvitation.md) <br/> |Exchange 2010. Obwohl der **CreateItem**-Vorgang für alle EWS-Versionen zutreffend ist, ist das **AcceptSharingInvitation**-Antwortobjekt nur auf EWS in Exchange-Versionen ab Exchange 2010 anwendbar.  <br/> |
|[GetSharingFolder-Vorgang](getsharingfolder-operation.md) <br/> |Exchange 2010  <br/> |
|[GetSharingMetadata-Vorgang](getsharingmetadata-operation.md) <br/> |Exchange 2010  <br/> |
|[RefreshSharingFolder-Vorgang](refreshsharingfolder-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="synchronization-operations"></a>Synchronisierungsvorgänge
<a name="bk_synchronization"> </a>

Synchronisierungsvorgänge stellen eine einseitig synchronisierte, zwischengespeicherte Kopie von Ordnern und Elementen eines Benutzers bereit. 
  
In der folgenden Tabelle sind die Synchronisierungsvorgänge aufgeführt.
  
|**Name des Vorgangs**|**Eingeführt in**|
|:-----|:-----|
|[SyncFolderHierarchy-Vorgang](syncfolderhierarchy-operation.md) <br/> |Exchange 2007  <br/> |
|[SyncFolderItems-Vorgang](syncfolderitems-operation.md) <br/> |Exchange 2007  <br/> |
   
## <a name="time-zone-operation"></a>Zeitzonenvorgänge
<a name="bk_timezone"> </a>

Mit Zeitzonenvorgängen können Clients eine Liste von Zeitzonendefinitionen abrufen, die vom Server unterstützt werden. 
  
In der folgenden Tabelle sind die Zeitzonenvorgänge aufgeführt.
  
|**Name des Vorgangs**|**Eingeführt in**|
|:-----|:-----|
|[GetServerTimeZones-Vorgang](getservertimezones-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="unified-messaging-operations"></a>Unified Messaging-Vorgänge
<a name="bk_um"> </a>

Mit Unified Messaging-Vorgängen können Clients Informationen zu Unified Messaging-Eigenschaften auslesen und Voicemailnachrichten über das Telefon wiedergeben. 
  
In der folgenden Tabelle sind die Unified Messaging-Vorgänge aufgeführt.
  
|**Name des Vorgangs**|**Eingeführt in**|
|:-----|:-----|
|[DisconnectPhoneCall-Vorgang](disconnectphonecall-operation.md) <br/> |Exchange 2010  <br/> |
|[GetPhoneCallInformation-Vorgang](getphonecallinformation-operation.md) <br/> |Exchange 2010  <br/> |
|[PlayOnPhone-Vorgang (EWS)](playonphone-operation-ews.md) <br/> |Exchange 2010  <br/> |
   
Verwenden Sie den [GetServiceConfiguration-Vorgang](getserviceconfiguration-operation.md), um Unified Messaging-Konfigurationsinformationen für ein Postfach abzurufen. Verwenden Sie den Unified Messaging-Webdienst für Unified Messaging-Anwendungen, die für Exchange 2007 bestimmt sind. Weitere Informationen dazu finden Sie unter [Unified Messaging-webdienstreferenz für Exchange](unified-messaging-web-service-reference-for-exchange.md).
  
## <a name="unified-contact-store-operations"></a>Vorgänge zum einheitlichen Kontaktspeicher
<a name="bk_ucs"> </a>

Vorgänge zum einheitlichen Kontaktspeicher bieten eine konsistente Kontakterfahrung in verschiedenen Office-Produkten und agieren als Integrationspunkt für Drittanbieter-Anwendungen, damit sie denselben Kontaktspeicher verwenden. Damit können Benutzer und Anwendungen Kontaktinformationen speichern, verwalten und darauf zugreifen und sie global in Lync, Exchange 2013, Outlook, Outlook Web App und beliebigen anderen Anwendungen zur Verfügung stellen, bei denen ein Zugriff auf den einheitlichen Kontaktspeicher implementiert ist. Exchange ist der Inhaltsspeicher für die einheitliche Kontaktspeicheroberfläche.
  
In der folgenden Tabelle sind Vorgänge zum einheitlichen Kontaktspeicher aufgeführt.
  
|**Name des Vorgangs**|**Eingeführt in**|
|:-----|:-----|
|[AddNewImContactToGroup-Vorgang](addnewimcontacttogroup-operation.md) <br/> |Exchange 2013  <br/> |
|[AddImContactToGroup-Vorgang](addimcontacttogroup-operation.md) <br/> |Exchange 2013  <br/> |
|[AddImGroup-Vorgang](addimgroup-operation.md) <br/> |Exchange 2013  <br/> |
|[AddNewTelUriContactToGroup-Vorgang](addnewteluricontacttogroup-operation.md) <br/> |Exchange 2013  <br/> |
|[AddDistributionGroupToImList-Vorgang](adddistributiongrouptoimlist-operation.md) <br/> |Exchange 2013  <br/> |
|[GetImItemList-Vorgang](getimitemlist-operation.md) <br/> |Exchange 2013  <br/> |
|[GetImItems-Vorgang](getimitems-operation.md) <br/> |Exchange 2013  <br/> |
|[RemoveContactFromImList-Vorgang](removecontactfromimlist-operation.md) <br/> |Exchange 2013  <br/> |
|[RemoveImContactFromGroup-Vorgang](removeimcontactfromgroup-operation.md) <br/> |Exchange 2013  <br/> |
|[RemoveDistributionGroupFromImList-Vorgang](removedistributiongroupfromimlist-operation.md) <br/> |Exchange 2013  <br/> |
|[RemoveImGroup-Vorgang](removeimgroup-operation.md) <br/> |Exchange 2013  <br/> |
|[SetImGroup-Vorgang](setimgroup-operation.md) <br/> |Exchange 2013  <br/> |
   
## <a name="user-configuration-operations"></a>Benutzerkonfigurationsvorgänge
<a name="bk_user_config"> </a>

Mit Benutzerkonfigurationsvorgängen können Clients Konfigurationsinformationen von Benutzern erstellen, löschen, abrufen und aktualisieren. 
  
In der folgenden Tabelle sind die Benutzerkonfigurationsvorgänge aufgeführt.
  
|**Name des Vorgangs**|**Eingeführt in**|
|:-----|:-----|
|[CreateUserConfiguration-Vorgang](createuserconfiguration-operation.md) <br/> |Exchange 2010  <br/> |
|[DeleteUserConfiguration-Vorgang](deleteuserconfiguration-operation.md) <br/> |Exchange 2010  <br/> |
|[GetUserConfiguration-Vorgang](getuserconfiguration-operation.md) <br/> |Exchange 2010  <br/> |
|[UpdateUserConfiguration-Vorgang](updateuserconfiguration-operation.md) <br/> |Exchange 2010  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Erkunden von verwalteter EWS-API, EWS und Webdiensten in Exchange](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [Erste Schritte mit Webdiensten in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
- [AutoErmittlung für Exchange](../exchange-web-services/autodiscover-for-exchange.md)
    

