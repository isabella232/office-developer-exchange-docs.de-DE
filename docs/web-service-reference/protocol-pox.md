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
description: Das Protokoll-Element enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.
ms.openlocfilehash: e58ae82ea5ec9d39db0f9219f6019df7da24a343
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830926"
---
# <a name="protocol-pox"></a>Protokoll (POX)

Das **Protokoll** -Element enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist. 
  
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
|Typ  <br/> |Gibt den Typ des Protokolls durch dieses **Protokoll** -Elements beschrieben. Der einzige gültige Wert für dieses Attribut ist "MapiHttp". Dieses Attribut ist, dass ist nur vorhanden, wenn die AutoErmittlung, anfordern, die dieser Antwort [eine X-MapiHttpCapability-Kopfzeile enthalten](pox-autodiscover-request-for-exchange.md)entspricht. Dieses Attribut gilt für Clients, mit die die MAPI/HTTP-Protokoll und das Ziel Exchange Online, Exchange Online als Teil von Office 365, implementiert oder lokale Versionen von Exchange, beginnend mit 15.00.0847.032 (Exchange Server 2013 SP1) erstellen.  <br/> |
|Version  <br/> |Gibt die Version des Protokolls durch dieses **Protokoll** -Elements beschrieben. Der einzige gültige Wert für dieses Attribut ist "1". Dieses Attribut ist nur vorhanden, wenn die Anforderung der AutoErmittlung, die dieser Antwort entspricht, ein **X MapiHttpCapability** Header enthalten. Dieses Attribut gilt für Clients, mit die die MAPI/HTTP-Protokoll und das Ziel Exchange Online, Exchange Online als Teil von Office 365, implementiert oder lokale Versionen von Exchange, beginnend mit 15.00.0847.032 (Exchange Server 2013 SP1) erstellen.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Typ (POX)](type-pox.md) <br/> |Identifiziert den Typ des konfigurierten e-Mail-Kontos.  <br/> |
|[Interne (POX)](internal-pox.md) <br/> |Enthält eine Auflistung von URLs, die ein Client zum Verbinden mit Exchange von innerhalb des Netzwerks der Organisation verwenden können.  <br/> |
|[Externe (POX)](external-pox.md) <br/> |Enthält eine Auflistung von URLs, die ein Client zum Verbinden mit Exchange von außerhalb des Netzwerks der Organisation verwenden können.  <br/> |
|[TTL (POX)](ttl-pox.md) <br/> |Gibt die Gültigkeitsdauer, in Stunden, in denen die Einstellungen gültig.  <br/> |
|[Server (POX)](server-pox.md) <br/> |Gibt den Namen des e-Mail-Servers.  <br/> |
|[ServerDN (POX)](serverdn-pox.md) <br/> |Gibt den distinguished Name des Exchange-Server an.  <br/> |
|[ServerVersion (POX)](serverversion-pox.md) <br/> |Stellt die Versionsnummer von Exchange Server.  <br/> |
|[MdbDN (POX)](mdbdn-pox.md) <br/> |Stellt den distinguished Name der Postfachdatenbank an.  <br/> |
|[PublicFolderServer (POX)](publicfolderserver-pox.md) <br/> |Enthält den vollqualifizierten Domänennamen (FQDN) des Servers für Öffentliche Ordner für den Benutzer.  <br/> |
|[Port (POX)](port-pox.md) <br/> |Gibt den Port, der Verbindung mit dem Speicher verwendet wird.  <br/> |
|[DirectoryPort (POX)](directoryport-pox.md) <br/> |Gibt den Port, mit der Netzwerkfirewall auf das Verzeichnis, wenn das Protokoll (NSPI = Name Service Provider Interface) verwendet wird.  <br/> |
|[ReferralPort (POX)](referralport-pox.md) <br/> |Gibt den Port, der zum Abrufen eines Verweises auf ein Verzeichnis verwendet wird.  <br/> |
|[ASUrl (POX)](asurl-pox.md) <br/> |Gibt die URL der Exchange-Webdienste für einen e-Mail-aktivierten Benutzer best-Instanz.  <br/> |
|["Ewsurl" (POX)](ewsurl-pox.md) <br/> |Gibt die URL der besten Endpunktinstanz für die Exchange-Webdienste (EWS) für einen e-Mail-aktivierten Benutzer an.  <br/> |
|[EmwsUrl (POX)](emwsurl-pox.md) <br/> |Gibt die URL der besten Endpunktinstanz für die Exchange-Webdienste (EWS) für einen e-Mail-aktivierten Benutzer an.  <br/> |
|[SharingUrl (POX)](sharingurl-pox.md) <br/> |Enthält die URL des sharing-Servers für die organisationsübergreifende Freigabe von Kalendern und Kontakten verwendet.  <br/> |
|[EcpUrl (POX)](ecpurl-pox.md) <br/> |Gibt die URL der Exchange-Systemsteuerung für einen e-Mail-aktivierten Benutzer.  <br/> |
|[EcpUrl-um (POX)](ecpurl-um-pox.md) <br/> |Gibt eine partielle URL, die mit dem [EcpUrl (POX)](ecpurl-pox.md) Elementwert generiert eine URL, die verwendet werden können, Voicemail-Einstellungen für einen e-Mail-aktivierten Benutzer Zugriff auf kombiniert werden kann.  <br/> |
|[EcpUrl-Aggr (POX)](ecpurl-aggr-pox.md) <br/> |Gibt eine partielle URL, die mit dem [EcpUrl (POX)](ecpurl-pox.md) Elementwert generiert eine URL, die verwendet werden können, für den e-Mail-aggregationseinstellungen für einen e-Mail-aktivierten Benutzer Zugriff auf kombiniert werden kann.  <br/> |
|[EcpUrl-Mt (POX)](ecpurl-mt-pox.md) <br/> |Gibt eine partielle URL, die mit dem [EcpUrl (POX)](ecpurl-pox.md) Elementwert generiert eine URL, die verwendet werden können, für den e-Mail-Nachricht Nachverfolgen der Einstellungen für einen e-Mail-aktivierten Benutzer Zugriff auf kombiniert werden kann.  <br/> |
|[EcpUrl-ret (POX)](ecpurl-ret-pox.md) <br/> |Gibt eine partielle URL, die kombiniert werden kann, mit dem [EcpUrl (POX)](ecpurl-pox.md) Elementwert generiert eine URL, die Einstellungen für einen e-Mail-aktivierten Benutzer Zugriff auf verwendet werden können.  <br/> |
|[EcpUrl-Sms (POX)](ecpurl-sms-pox.md) <br/> |Gibt eine partielle URL, die mit dem [EcpUrl (POX)](ecpurl-pox.md) Elementwert generiert eine URL, die verwendet werden können, auf Short Message Service (SMS) die Einstellungen für einen e-Mail-aktivierten Benutzer zugreifen kombiniert werden kann.  <br/> |
|[EcpUrl-veröffentlichen (POX)](ecpurl-publish-pox.md) <br/> |Gibt eine partielle URL, die kombiniert werden kann, mit dem [EcpUrl (POX)](ecpurl-pox.md) Elementwert generiert eine URL, die Veröffentlichung kalendereinstellungen für einen e-Mail-aktivierten Benutzer Zugriff auf verwendet werden können.  <br/> |
|[EcpUrl-Foto (POX)](ecpurl-photo-pox.md) <br/> |Gibt eine partielle URL, die kombiniert werden kann, mit dem [EcpUrl (POX)](ecpurl-pox.md) Elementwert generiert eine URL, die zum Anzeigen oder Ändern des aktuellen Foto einen e-Mail-aktivierten Benutzer verwendet werden kann.  <br/> |
|[EcpUrl-tm (POX)](ecpurl-tm-pox.md) <br/> |Gibt eine partielle URL, die mit dem [EcpUrl (POX)](ecpurl-pox.md) Elementwert generiert eine URL, die verwendet werden können, greifen Sie auf eine Liste aller Postfächer für Website, ein e-Mail-aktivierten Benutzer derzeit gehört kombiniert werden kann.  <br/> |
|[EcpUrl-TmCreating (POX)](ecpurl-tmcreating-pox.md) <br/> |Gibt eine partielle URL, die kombiniert werden kann, mit dem [EcpUrl (POX)](ecpurl-pox.md) Elementwert generiert eine URL, die zum Erstellen eines neuen Postfachs für die Website verwendet werden können.  <br/> |
|[EcpUrl-TmHiding (POX)](ecpurl-tmhiding-pox.md) <br/> |Gibt eine partielle URL, die kombiniert werden kann, mit dem [EcpUrl (POX)](ecpurl-pox.md) Elementwert generiert eine URL, die die Benutzer von einem websitepostfach Kündigen des Abonnements verwendet werden können.  <br/> |
|[EcpUrl-TmEditing (POX)](ecpurl-tmediting-pox.md) <br/> |Gibt eine partielle URL, die kombiniert werden kann, mit dem [EcpUrl (POX)](ecpurl-pox.md) Elementwert generiert eine URL, die zum Bearbeiten eines vorhandenen Website-Postfachs verwendet werden kann.  <br/> |
|[EcpUrl-Extinstall (POX)](ecpurl-extinstall-pox.md) <br/> |Gibt eine partielle URL, die zusammen mit dem [EcpUrl (POX)](ecpurl-pox.md) Elementwert generiert eine URL, die verwendet werden kann, anzeigen oder ändern die Mail-apps, die derzeit im Postfach des Benutzers installiert werden kann.  <br/> |
|[OOFUrl (POX)](oofurl-pox.md) <br/> |Gibt die URL der besten Instanz des Verfügbarkeitsdiensts für einen e-Mail-aktivierten Benutzer.  <br/> |
|[OABUrl (POX)](oaburl-pox.md) <br/> |Gibt die URL des Offlineadressbuchs Konfiguration Server, für eine Exchange-Topologie.  <br/> |
|[UMUrl (POX)](umurl-pox.md) <br/> |Gibt die URL der besten Instanz des Unified Messaging-Webdiensts für einen e-Mail-aktivierten Benutzer.  <br/> |
|[EwsPartnerUrl (POX)](ewspartnerurl-pox.md) <br/> |Gibt die URL der besten Endpunktinstanz für die Exchange-Webdienste (EWS) für einen e-Mail-aktivierten Benutzer an.  <br/> |
|[LoginName (POX)](loginname-pox.md) <br/> |Gibt den Namen des Benutzers anmelden.  <br/> |
|[Erforderlicher (POX)](domainrequired-pox.md) <br/> |Gibt an, ob die Domäne für die Authentifizierung erforderlich ist.  <br/> |
|[DomainName (POX)](domainname-pox.md) <br/> |Gibt die Domäne des Benutzers an.  <br/> |
|[SPA (POX)](spa-pox.md) <br/> |Gibt an, ob gesicherte Kennwortauthentifizierung erforderlich ist.  <br/> |
|[AuthPackage (POX)](authpackage-pox.md) <br/> |Gibt das Authentifizierungsschema, das verwendet wird, wenn der Exchange 2007-Computer authentifiziert, die die Postfach-Serverrolle installiert ist.  <br/> |
|[CertPrincipalName (POX)](certprincipalname-pox.md) <br/> |Gibt den Prinzipal Secure Sockets Layer (SSL) Zertifikat-Namen, der von der Microsoft Exchange-Organisation Herstellen einer Verbindung mit SSL erforderlich ist.  <br/> |
|[SSL (POX)](ssl-pox.md) <br/> |Gibt an, ob die sichere Anmeldung erforderlich ist.  <br/> |
|[AuthRequired (POX)](authrequired-pox.md) <br/> |Gibt an, ob die Authentifizierung erforderlich ist.  <br/> |
|[UsePOPAuth (POX)](usepopauth-pox.md) <br/> |Gibt an, ob die Authentifizierungsinformationen angeben, die für einen POP3-Konto bereitgestellt wird auch für Simple Mail Transfer Protocol (SMTP) verwendet wird.  <br/> |
|[SMTPLast (POX)](smtplast-pox.md) <br/> |Gibt an, ob der SMTP-Server erfordert, dass E-mail heruntergeladen werden, bevor es e-Mail-Nachrichten mithilfe des SMTP-Servers sendet.  <br/> |
|[NetworkRequirements (POX)](networkrequirements-pox.md) <br/> |Enthält die Kriterien, die verwendet werden, um festzustellen, ob der Client-Computer in einem Netzwerk, die den Internetdienstanbieter erfüllt befindet, mit dem Server herstellen.  <br/> |
|[AddressBook (POX)](addressbook-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit der Adressbuchserver mithilfe des MAPI/HTTP-Protokolls. Dieses Element ist nur vorhanden, wenn das **Type** -Attribut für das **Protokoll** Element vorhanden und ist auf "MapiHttp". **AddressBook** -Element ist für Clients, mit die die MAPI/HTTP-Protokoll und Exchange Online Ziel und Versionen von Exchange, beginnend mit 15.00.0847.032 implementiert.  <br/> |
|[Postspeicher weitergeleitet (POX)](mailstore-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients an das Postfach des Benutzers mithilfe des MAPI/HTTP-Protokolls. Dieses Element ist nur vorhanden, wenn das **Type** -Attribut für das **Protokoll** Element vorhanden und ist auf "MapiHttp". Das Element **Postspeicher bezeichnet** gilt für Clients, mit die die MAPI/HTTP-Protokoll und Exchange Online Ziel und Versionen von Exchange, beginnend mit 15.00.0847.032 implementiert.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Konto (POX)](account-pox.md) <br/> |Gibt die kontoeinstellungen für den Benutzer an.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das **Protokoll** -Element ist in einer Antwort, die einen [Aktion (POX)](action-pox.md) Wert aufweist, der **Einstellungen**entspricht vorhanden.
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

