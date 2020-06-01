---
title: Protokoll (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: f77e4d66-6fdd-4999-9339-f7d7f9c86f44
description: Das Protocol-Element enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf dem Exchange Server ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.
ms.openlocfilehash: 6fca347f49e27958ecb16cce345387b6a2146979
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "44467760"
---
# <a name="protocol-pox"></a>Protokoll (POX)

Das **Protocol** -Element enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf dem Exchange Server ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist. 
  
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
|Typ  <br/> |Gibt den Typ des Protokolls an, der von diesem **Protokoll** Element beschrieben wird. Der einzige gültige Wert für dieses Attribut ist "mapiHttp". Dieses Attribut ist nur vorhanden, wenn die Auto Ermittlungsanforderung, die dieser Antwort entspricht, [einen X-MapiHttpCapability-Header enthielt](pox-autodiscover-request-for-exchange.md). Dieses Attribut gilt für Clients, die das MAPI/http-Protokoll und die Ziel Exchange Online implementieren, Exchange Online im Rahmen von Office 365 oder lokalen Versionen von Exchange, beginnend mit Build 15.00.0847.032 (Exchange Server 2013 SP1).  <br/> |
|Version  <br/> |Gibt die Version des Protokolls an, die von diesem **Protokoll** Element beschrieben wird. Der einzige gültige Wert für dieses Attribut ist "1". Dieses Attribut ist nur vorhanden, wenn die Auto Ermittlungsanforderung, die dieser Antwort entspricht, einen **X-MapiHttpCapability-** Header enthielt. Dieses Attribut gilt für Clients, die das MAPI/http-Protokoll und die Ziel Exchange Online implementieren, Exchange Online im Rahmen von Office 365 oder lokalen Versionen von Exchange, beginnend mit Build 15.00.0847.032 (Exchange Server 2013 SP1).  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Typ (POX)](type-pox.md) <br/> |Gibt den Typ des konfigurierten e-Mail-Kontos an.  <br/> |
|[Interne (POX)](internal-pox.md) <br/> |Enthält eine Auflistung von URLs, die ein Client verwenden kann, um eine Verbindung mit Exchange im Netzwerk der Organisation herzustellen.  <br/> |
|[Extern (POX)](external-pox.md) <br/> |Enthält eine Auflistung von URLs, die ein Client für die Verbindung mit Exchange von außerhalb des Netzwerks der Organisation verwenden kann.  <br/> |
|[TTL (POX)](ttl-pox.md) <br/> |Gibt die Uhrzeit in Stunden an, zu der die Einstellungen gültig bleiben.  <br/> |
|[Server (POX)](server-pox.md) <br/> |Gibt den Namen des e-Mail-Servers an.  <br/> |
|[ServerDN (POX)](serverdn-pox.md) <br/> |Gibt den Distinguished Name Exchange Server an.  <br/> |
|[ServerVersion (POX)](serverversion-pox.md) <br/> |Stellt die Versionsnummer Exchange Server dar.  <br/> |
|[MdbDN (POX)](mdbdn-pox.md) <br/> |Stellt den Distinguished Name der Postfachdatenbank dar.  <br/> |
|[PublicFolderServer (POX)](publicfolderserver-pox.md) <br/> |Enthält den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des Servers für Öffentliche Ordner für den Benutzer.  <br/> |
|[Port (POX)](port-pox.md) <br/> |Gibt den Port an, der zum Herstellen einer Verbindung mit dem Speicher verwendet wird.  <br/> |
|[DirectoryPort (POX)](directoryport-pox.md) <br/> |Gibt den Port an, der zum Herstellen einer Verbindung mit dem Verzeichnis verwendet wird, wenn das NSPI-Protokoll (Name Service Provider Interface) verwendet wird.  <br/> |
|[ReferralPort (POX)](referralport-pox.md) <br/> |Gibt den Port an, der verwendet wird, um einen Verweis auf ein Verzeichnis zu erhalten.  <br/> |
|[ASUrl (POX)](asurl-pox.md) <br/> |Gibt die URL der besten Instanz der Exchange-Webdienste für einen e-Mail-aktivierten Benutzer an.  <br/> |
|[EwsUrl (POX)](ewsurl-pox.md) <br/> |Gibt die URL der besten Endpunkt Instanz für Exchange-Webdienste für einen e-Mail-aktivierten Benutzer an.  <br/> |
|[EmwsUrl (POX)](emwsurl-pox.md) <br/> |Gibt die URL der besten Endpunkt Instanz für Exchange-Webdienste für einen e-Mail-aktivierten Benutzer an.  <br/> |
|[SharingUrl (POX)](sharingurl-pox.md) <br/> |Enthält die URL des Freigabe Servers, der für die organisationsübergreifende Freigabe von Kalendern und Kontakten verwendet wird.  <br/> |
|[EcpUrl (POX)](ecpurl-pox.md) <br/> |Gibt die URL der Exchange-Systemsteuerung für einen e-Mail-aktivierten Benutzer an.  <br/> |
|[EcpUrl-um (POX)](ecpurl-um-pox.md) <br/> |Gibt eine partielle URL an, die mit dem [EcpUrl (POX)](ecpurl-pox.md) -Elementwert kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf Voicemaileinstellungen für einen e-Mail-aktivierten Benutzer verwendet werden kann.  <br/> |
|[EcpUrl-aggr (POX)](ecpurl-aggr-pox.md) <br/> |Gibt eine partielle URL an, die mit dem [EcpUrl (POX)](ecpurl-pox.md) -Elementwert kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf e-Mail-Aggregationseinstellungen für einen e-Mail-aktivierten Benutzer verwendet werden kann.  <br/> |
|[EcpUrl-MT (POX)](ecpurl-mt-pox.md) <br/> |Gibt eine partielle URL an, die mit dem [EcpUrl (POX)](ecpurl-pox.md) -Elementwert kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf e-Mail-Nachrichtenverfolgungseinstellungen für einen e-Mail-aktivierten Benutzer verwendet werden kann.  <br/> |
|[EcpUrl-ret (POX)](ecpurl-ret-pox.md) <br/> |Gibt eine partielle URL an, die mit dem [EcpUrl (POX)](ecpurl-pox.md) -Elementwert kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf Aufbewahrungstags Einstellungen für einen e-Mail-aktivierten Benutzer verwendet werden kann.  <br/> |
|[EcpUrl-SMS (POX)](ecpurl-sms-pox.md) <br/> |Gibt eine partielle URL an, die mit dem [EcpUrl (POX)](ecpurl-pox.md) -Elementwert kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf SMS-Einstellungen (Short Message Service) für einen e-Mail-aktivierten Benutzer verwendet werden kann.  <br/> |
|[EcpUrl-Publish (POX)](ecpurl-publish-pox.md) <br/> |Gibt eine partielle URL an, die mit dem [EcpUrl (POX)](ecpurl-pox.md) -Elementwert kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf die Kalender Veröffentlichungseinstellungen für einen e-Mail-aktivierten Benutzer verwendet werden kann.  <br/> |
|[EcpUrl-Photo (POX)](ecpurl-photo-pox.md) <br/> |Gibt eine partielle URL an, die mit dem [EcpUrl (POX)](ecpurl-pox.md) -Elementwert kombiniert werden kann, um eine URL zu generieren, die zum Anzeigen oder Ändern des aktuellen Fotos eines e-Mail-aktivierten Benutzers verwendet werden kann.  <br/> |
|[EcpUrl-TM (POX)](ecpurl-tm-pox.md) <br/> |Gibt eine partielle URL an, die mit dem [EcpUrl (POX)](ecpurl-pox.md) -Elementwert kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf eine Liste aller Website Postfächer verwendet werden kann, in denen ein e-Mail-aktivierter Benutzer derzeit Mitglied ist.  <br/> |
|[EcpUrl-tmCreating (POX)](ecpurl-tmcreating-pox.md) <br/> |Gibt eine partielle URL an, die mit dem [EcpUrl (POX)](ecpurl-pox.md) -Elementwert kombiniert werden kann, um eine URL zu generieren, die zum Erstellen eines neuen websitepostfachs verwendet werden kann.  <br/> |
|[EcpUrl-tmHiding (POX)](ecpurl-tmhiding-pox.md) <br/> |Gibt eine partielle URL an, die mit dem [EcpUrl (POX)](ecpurl-pox.md) -Elementwert kombiniert werden kann, um eine URL zu generieren, die zum Aufheben des Abonnements des Benutzers von einem websitepostfach verwendet werden kann.  <br/> |
|[EcpUrl-tmEditing (POX)](ecpurl-tmediting-pox.md) <br/> |Gibt eine partielle URL an, die mit dem [EcpUrl (POX)](ecpurl-pox.md) -Elementwert kombiniert werden kann, um eine URL zu generieren, die zum Bearbeiten eines vorhandenen websitepostfachs verwendet werden kann.  <br/> |
|[EcpUrl-extinstall (POX)](ecpurl-extinstall-pox.md) <br/> |Gibt eine partielle URL an, die mit dem [EcpUrl (POX)](ecpurl-pox.md) -Elementwert kombiniert werden kann, um eine URL zu generieren, die zum Anzeigen oder Ändern der aktuell im Postfach des Benutzers installierten e-Mail-Apps verwendet werden kann.  <br/> |
|[OOFUrl (POX)](oofurl-pox.md) <br/> |Gibt die URL der besten Instanz des Verfügbarkeitsdiensts für einen e-Mail-aktivierten Benutzer an.  <br/> |
|[OABUrl (POX)](oaburl-pox.md) <br/> |Gibt die URL des Offline Adressbuch-Konfigurations Servers für eine Exchange-Topologie an.  <br/> |
|[UMUrl (POX)](umurl-pox.md) <br/> |Gibt die URL der besten Instanz des Unified Messaging-Webdiensts für einen e-Mail-aktivierten Benutzer an.  <br/> |
|[EwsPartnerUrl (POX)](ewspartnerurl-pox.md) <br/> |Gibt die URL der besten Endpunkt Instanz für Exchange-Webdienste für einen e-Mail-aktivierten Benutzer an.  <br/> |
|[LoginName (POX)](loginname-pox.md) <br/> |Gibt den Anmeldenamen des Benutzers an.  <br/> |
|[DomainRequired (POX)](domainrequired-pox.md) <br/> |Gibt an, ob die Domäne für die Authentifizierung erforderlich ist.  <br/> |
|[Domänenname (POX)](domainname-pox.md) <br/> |Gibt die Domäne des Benutzers an.  <br/> |
|[Spa (POX)](spa-pox.md) <br/> |Gibt an, ob eine sichere Kennwortauthentifizierung erforderlich ist.  <br/> |
|[AuthPackage (POX)](authpackage-pox.md) <br/> |Gibt das Authentifizierungsschema an, das bei der Authentifizierung mit dem Exchange 2007 Computer verwendet wird, auf dem die Postfachserverrolle installiert ist.  <br/> |
|[CertPrincipalName (POX)](certprincipalname-pox.md) <br/> |Gibt den Secure Sockets Layer (SSL) zertifikatprinzipalnamen an, der zum Herstellen einer Verbindung mit der Microsoft Exchange Organisation mithilfe von SSL erforderlich ist.  <br/> |
|[SSL (POX)](ssl-pox.md) <br/> |Gibt an, ob eine sichere Anmeldung erforderlich ist.  <br/> |
|[AuthRequired (POX)](authrequired-pox.md) <br/> |Gibt an, ob eine Authentifizierung erforderlich ist.  <br/> |
|[UsePOPAuth (POX)](usepopauth-pox.md) <br/> |Gibt an, ob die Authentifizierungsinformationen, die für einen POP3-Kontotyp bereitgestellt werden, auch für Simple Mail Transfer Protocol (SMTP) verwendet werden.  <br/> |
|[SMTPLast (POX)](smtplast-pox.md) <br/> |Gibt an, ob der SMTP-Server die e-Mail-Nachrichten heruntergeladen werden muss, bevor e-Mails mithilfe des SMTP-Servers gesendet werden.  <br/> |
|[NetworkRequirements (POX)](networkrequirements-pox.md) <br/> |Enthält die Kriterien, die verwendet werden, um zu bestimmen, ob sich der Clientcomputer in einem Netzwerk befindet, das die Anforderungen des Internet Dienstanbieters erfüllt, eine Verbindung mit dem Server herzustellen.  <br/> |
|[Adressbuch (POX)](addressbook-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Adressbuchserver mithilfe des MAPI/http-Protokolls. Dieses Element ist nur vorhanden, wenn das **Type** -Attribut für das **Protocol** -Element vorhanden und auf "mapiHttp" festgelegt ist. Das **addressbook** -Element gilt für Clients, die das MAPI/http-Protokoll und die Ziel Exchange Online und Exchange-Versionen, beginnend mit 15.00.0847.032, implementieren.  <br/> |
|[MailStore (POX)](mailstore-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Postfach des Benutzers mithilfe des MAPI/http-Protokolls. Dieses Element ist nur vorhanden, wenn das **Type** -Attribut für das **Protocol** -Element vorhanden und auf "mapiHttp" festgelegt ist. Das **MailStore** -Element gilt für Clients, die das MAPI/http-Protokoll und die Ziel Exchange Online und Exchange-Versionen, beginnend mit 15.00.0847.032, implementieren.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Konto (POX)](account-pox.md) <br/> |Gibt Kontoeinstellungen für den Benutzer an.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das **Protocol** -Element ist in einer Antwort vorhanden, die einen [Action-Wert (POX)](action-pox.md) aufweist, der den **Einstellungen**entspricht.
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

