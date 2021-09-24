---
title: Protokoll (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: f77e4d66-6fdd-4999-9339-f7d7f9c86f44
description: Das Protokollelement enthält die Spezifikationen zum Verbinden eines Clients mit dem Computer, auf dem Exchange Server ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
ms.openlocfilehash: 4f308951c74612936755e6d4c16620e38277aecb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516398"
---
# <a name="protocol-pox"></a>Protokoll (POX)

Das **Protokollelement** enthält die Spezifikationen zum Verbinden eines Clients mit dem Computer, auf dem Exchange Server ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Protokoll (POX)](protocol-pox.md)
  
```xml
<Protocol>
   <Type/>
   <Internal/>
   <External/>
   <TTL/>
   <Server/>
   <ServerDN/>
   <ServerVersion/>
   <MdbDN/>
   <PublicFolderServer/>
   <Port/>
   <DirectoryPort/>
   <ReferralPort/>
   <ASUrl/>
   <EwsUrl/>
   <EmwsUrl/>
   <SharingUrl/>
   <EcpUrl/>
   <EcpUrl-um/>
   <EcpUrl-aggr/>
   <EcpUrl-mt/>
   <EcpUrl-ret/>
   <EcpUrl-sms/>
   <EcpUrl-publish/>
   <EcpUrl-photo/>
   <EcpUrl-tm/>
   <EcpUrl-tmCreating/>
   <EcpUrl-tmHiding/>
   <EcpUrl-tmEditing/>
   <EcpUrl-extinstall/>
   <OOFUrl/>
   <OABUrl/>
   <UMUrl/>
   <EwsPartnerUrl/>
   <LoginName/>
   <DomainRequired/>
   <DomainName/>
   <SPA/>
   <AuthPackage/>
   <CertPrincipalName/>
   <SSL/>
   <AuthRequired/>
   <UsePOPAuth/>
   <SMTPLast/>
   <NetworkRequirements/>
   <AddressBook/>
   <MailStore/>
</Protocol>
```

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Typ  <br/> |Gibt den Typ des Protokolls an, der von diesem **Protokollelement** beschrieben wird. Der einzige gültige Wert für dieses Attribut ist "mapiHttp". Dieses Attribut ist nur vorhanden, wenn die AutoErmittlungsanforderung, die dieser Antwort [entspricht, einen X-MapiHttpCapability-Header enthält.](pox-autodiscover-request-for-exchange.md) Dieses Attribut gilt für Clients, die das MAPI/HTTP-Protokoll und die Ziel-Exchange Online, Exchange Online als Teil Office 365 oder lokale Versionen von Exchange ab Build 15.00.0847.032 (Exchange Server 2013 SP1) implementieren.  <br/> |
|Version  <br/> |Gibt die Version des Protokolls an, das von diesem **Protokollelement** beschrieben wird. Der einzige gültige Wert für dieses Attribut ist "1". Dieses Attribut ist nur vorhanden, wenn die AutoErmittlungsanforderung, die dieser Antwort entspricht, einen **X-MapiHttpCapability-Header** enthält. Dieses Attribut gilt für Clients, die das MAPI/HTTP-Protokoll und die Ziel-Exchange Online, Exchange Online als Teil Office 365 oder lokale Versionen von Exchange ab Build 15.00.0847.032 (Exchange Server 2013 SP1) implementieren.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Typ (POX)](type-pox.md) <br/> |Gibt den Typ des konfigurierten E-Mail-Kontos an.  <br/> |
|[Interne (POX)](internal-pox.md) <br/> |Enthält eine Auflistung von URLs, die ein Client verwenden kann, um eine Verbindung mit Exchange aus dem Netzwerk der Organisation herzustellen.  <br/> |
|[Extern (POX)](external-pox.md) <br/> |Enthält eine Auflistung von URLs, die ein Client verwenden kann, um eine Verbindung mit Exchange von außerhalb des Netzwerks der Organisation herzustellen.  <br/> |
|[TTL (POX)](ttl-pox.md) <br/> |Gibt die Zeit bis Zum Live in Stunden an, in denen die Einstellungen gültig bleiben.  <br/> |
|[Server (POX)](server-pox.md) <br/> |Gibt den Namen des E-Mail-Servers an.  <br/> |
|[ServerDN (POX)](serverdn-pox.md) <br/> |Gibt den Exchange Server Distinguished Name an.  <br/> |
|[ServerVersion (POX)](serverversion-pox.md) <br/> |Stellt die Exchange Server Versionsnummer dar.  <br/> |
|[MdbDN (POX)](mdbdn-pox.md) <br/> |Stellt den Distinguished Name der Postfachdatenbank dar.  <br/> |
|[PublicFolderServer (POX)](publicfolderserver-pox.md) <br/> |Enthält den vollqualifizierten Domänennamen (FQDN) des Öffentlichen Ordnerservers für den Benutzer.  <br/> |
|[Port (POX)](port-pox.md) <br/> |Gibt den Port an, der zum Herstellen einer Verbindung mit dem Speicher verwendet wird.  <br/> |
|[DirectoryPort (POX)](directoryport-pox.md) <br/> |Gibt den Port an, der zum Herstellen einer Verbindung mit dem Verzeichnis verwendet wird, wenn das NSPI-Protokoll (Name Service Provider Interface) verwendet wird.  <br/> |
|[ReferralPort (POX)](referralport-pox.md) <br/> |Gibt den Port an, der verwendet wird, um einen Verweis auf ein Verzeichnis abzurufen.  <br/> |
|[ASUrl (POX)](asurl-pox.md) <br/> |Gibt die URL der besten Instanz der Exchange Webdienste für einen E-Mail-aktivierten Benutzer an.  <br/> |
|[EwsUrl (POX)](ewsurl-pox.md) <br/> |Gibt die URL der besten Endpunktinstanz für Exchange Webdienste (EWS) für einen E-Mail-aktivierten Benutzer an.  <br/> |
|[EmwsUrl (POX)](emwsurl-pox.md) <br/> |Gibt die URL der besten Endpunktinstanz für Exchange Webdienste (EWS) für einen E-Mail-aktivierten Benutzer an.  <br/> |
|[SharingUrl (POX)](sharingurl-pox.md) <br/> |Enthält die URL des Freigabeservers, der für die organisationsübergreifende Freigabe von Kalendern und Kontakten verwendet wird.  <br/> |
|[EcpUrl (POX)](ecpurl-pox.md) <br/> |Gibt die URL der Exchange Systemsteuerung für einen E-Mail-aktivierten Benutzer an.  <br/> |
|[EcpUrl-um (POX)](ecpurl-um-pox.md) <br/> |Gibt eine partielle URL an, die mit dem [PoX-Wert (EcpUrl)](ecpurl-pox.md) kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf Voicemaileinstellungen für einen E-Mail-aktivierten Benutzer verwendet werden kann.  <br/> |
|[EcpUrl-aggr (POX)](ecpurl-aggr-pox.md) <br/> |Gibt eine partielle URL an, die mit dem Wert des [EcpUrl -Elements (POX)](ecpurl-pox.md) kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf E-Mail-Aggregationseinstellungen für einen E-Mail-aktivierten Benutzer verwendet werden kann.  <br/> |
|[EcpUrl-mt (POX)](ecpurl-mt-pox.md) <br/> |Gibt eine partielle URL an, die mit dem [PoX-Wert (EcpUrl)](ecpurl-pox.md) kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf E-Mail-Nachrichtenverfolgungseinstellungen für einen E-Mail-aktivierten Benutzer verwendet werden kann.  <br/> |
|[EcpUrl-ret (POX)](ecpurl-ret-pox.md) <br/> |Gibt eine partielle URL an, die mit dem Wert des [EcpUrl -Elements (POX)](ecpurl-pox.md) kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf Aufbewahrungstageinstellungen für einen E-Mail-aktivierten Benutzer verwendet werden kann.  <br/> |
|[EcpUrl-sms (POX)](ecpurl-sms-pox.md) <br/> |Gibt eine partielle URL an, die mit dem [PoX-Wert (EcpUrl)](ecpurl-pox.md) kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf SMS-Einstellungen (Short Message Service) für einen E-Mail-aktivierten Benutzer verwendet werden kann.  <br/> |
|[EcpUrl-publish (POX)](ecpurl-publish-pox.md) <br/> |Gibt eine partielle URL an, die mit dem [PoX-Wert (EcpUrl)](ecpurl-pox.md) kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf Kalenderveröffentlichungseinstellungen für einen E-Mail-aktivierten Benutzer verwendet werden kann.  <br/> |
|[EcpUrl-photo (POX)](ecpurl-photo-pox.md) <br/> |Gibt eine partielle URL an, die mit dem [PoX-Wert (EcpUrl)](ecpurl-pox.md) kombiniert werden kann, um eine URL zu generieren, die zum Anzeigen oder Ändern des aktuellen Fotos eines E-Mail-aktivierten Benutzers verwendet werden kann.  <br/> |
|[EcpUrl-tm (POX)](ecpurl-tm-pox.md) <br/> |Gibt eine partielle URL an, die mit dem [PoX-Wert (EcpUrl)](ecpurl-pox.md) kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf eine Liste aller Websitepostfächer verwendet werden kann, deren Mitglied ein E-Mail-aktivierter Benutzer ist.  <br/> |
|[EcpUrl-tmCreating (POX)](ecpurl-tmcreating-pox.md) <br/> |Gibt eine partielle URL an, die mit dem [PoX-Wert (EcpUrl)](ecpurl-pox.md) kombiniert werden kann, um eine URL zu generieren, die zum Erstellen eines neuen Websitepostfachs verwendet werden kann.  <br/> |
|[EcpUrl-tmHiding (POX)](ecpurl-tmhiding-pox.md) <br/> |Gibt eine partielle URL an, die mit dem [PoX-Wert (EcpUrl)](ecpurl-pox.md) kombiniert werden kann, um eine URL zu generieren, die verwendet werden kann, um den Benutzer von einem Websitepostfach abzumelden.  <br/> |
|[EcpUrl-tmEditing (POX)](ecpurl-tmediting-pox.md) <br/> |Gibt eine partielle URL an, die mit dem [PoX-Wert (EcpUrl)](ecpurl-pox.md) kombiniert werden kann, um eine URL zu generieren, die zum Bearbeiten eines vorhandenen Websitepostfachs verwendet werden kann.  <br/> |
|[EcpUrl-extinstall (POX)](ecpurl-extinstall-pox.md) <br/> |Gibt eine partielle URL an, die mit dem [PoX-Wert (EcpUrl)](ecpurl-pox.md) kombiniert werden kann, um eine URL zu generieren, die zum Anzeigen oder Ändern der derzeit im Postfach des Benutzers installierten Mail-Apps verwendet werden kann.  <br/> |
|[OOFUrl (POX)](oofurl-pox.md) <br/> |Gibt die URL der besten Instanz des Verfügbarkeitsdiensts für einen E-Mail-aktivierten Benutzer an.  <br/> |
|[OABUrl (POX)](oaburl-pox.md) <br/> |Gibt die Url des Offlineadressbuch-Konfigurationsservers für eine Exchange Topologie an.  <br/> |
|[UMUrl (POX)](umurl-pox.md) <br/> |Gibt die URL der besten Instanz des Unified Messaging-Webdiensts für einen E-Mail-aktivierten Benutzer an.  <br/> |
|[EwsPartnerUrl (POX)](ewspartnerurl-pox.md) <br/> |Gibt die URL der besten Endpunktinstanz für Exchange Webdienste (EWS) für einen E-Mail-aktivierten Benutzer an.  <br/> |
|[LoginName (POX)](loginname-pox.md) <br/> |Gibt den Anmeldenamen des Benutzers an.  <br/> |
|[DomainRequired (POX)](domainrequired-pox.md) <br/> |Gibt an, ob die Domäne für die Authentifizierung erforderlich ist.  <br/> |
|[DomainName (POX)](domainname-pox.md) <br/> |Gibt die Domäne des Benutzers an.  <br/> |
|[SPA (POX)](spa-pox.md) <br/> |Gibt an, ob eine sichere Kennwortauthentifizierung erforderlich ist.  <br/> |
|[AuthPackage (POX)](authpackage-pox.md) <br/> |Gibt das Authentifizierungsschema an, das bei der Authentifizierung für den computer Exchange 2007 verwendet wird, auf dem die Postfachserverrolle installiert ist.  <br/> |
|[CertPrincipalName (POX)](certprincipalname-pox.md) <br/> |Gibt den SSL-Zertifikatprinzipalnamen (Secure Sockets Layer) an, der zum Herstellen einer Verbindung mit der Microsoft Exchange-Organisation mit ssl erforderlich ist.  <br/> |
|[SSL (POX)](ssl-pox.md) <br/> |Gibt an, ob eine sichere Anmeldung erforderlich ist.  <br/> |
|[AuthRequired (POX)](authrequired-pox.md) <br/> |Gibt an, ob eine Authentifizierung erforderlich ist.  <br/> |
|[UsePOPAuth (POX)](usepopauth-pox.md) <br/> |Gibt an, ob die Authentifizierungsinformationen, die für einen POP3-Kontotyp bereitgestellt werden, auch für SMTP (Simple Mail Transfer Protocol) verwendet werden.  <br/> |
|[SMTPLast (POX)](smtplast-pox.md) <br/> |Gibt an, ob für den SMTP-Server der Download von E-Mails erforderlich ist, bevor E-Mail-Nachrichten mithilfe des SMTP-Servers gesendet werden.  <br/> |
|[NetworkRequirements (POX)](networkrequirements-pox.md) <br/> |Enthält die Kriterien, die verwendet werden, um zu bestimmen, ob sich der Clientcomputer in einem Netzwerk befindet, das die Anforderungen des Internetdienstanbieters für die Verbindung mit dem Server erfüllt.  <br/> |
|[AddressBook (POX)](addressbook-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Adressbuchserver mithilfe des MAPI/HTTP-Protokolls. Dieses Element ist nur vorhanden, wenn das **Type-Attribut** für das **Protocol-Element** vorhanden ist und auf "mapiHttp" festgelegt ist. Das **AddressBook-Element** gilt für Clients, die das MAPI/HTTP-Protokoll und Exchange Online und Versionen von Exchange ab 15.00.0847.032 implementieren.  <br/> |
|[MailStore (POX)](mailstore-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Postfach des Benutzers mithilfe des MAPI/HTTP-Protokolls. Dieses Element ist nur vorhanden, wenn das **Type-Attribut** für das **Protocol-Element** vorhanden ist und auf "mapiHttp" festgelegt ist. Das **MailStore-Element** gilt für Clients, die das MAPI/HTTP-Protokoll implementieren und Exchange Online und Versionen von Exchange ab 15.00.0847.032 verwenden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Konto (POX)](account-pox.md) <br/> |Gibt die Kontoeinstellungen für den Benutzer an.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das **Protokollelement** ist in einer Antwort vorhanden, die einen [POX-Wert (Action)](action-pox.md) **aufweist,** der den Einstellungen entspricht.
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

