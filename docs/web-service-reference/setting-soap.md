---
title: Einstellung (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 43db26e1-f7be-49fd-b26b-fc1b10bd3458
description: Das Setting-Element stellt eine zurückzugebende Konfigurationseinstellung dar.
ms.openlocfilehash: df3b55fe7ba2c5ae92f8c31ec0643dbe100fa072
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466745"
---
# <a name="setting-soap"></a>Einstellung (SOAP)

Das **Setting** -Element stellt eine zurückzugebende Konfigurationseinstellung dar. 
  
```XML
<Setting/>
```

 **Zeichenfolge**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[RequestedSettings (SOAP)](requestedsettings-soap.md) <br/> |Enthält die Namen der angeforderten Konfigurationseinstellungen.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert für dieses Element ist die Konfigurationseinstellung. In der folgenden Tabelle sind die möglichen Konfigurationseinstellungen aufgeführt.
  
|**Konfigurationseinstellung**|**Beschreibung**|
|:-----|:-----|
|UserDisplayName  <br/> |Der Anzeigename des Benutzers.  <br/> |
|BenutzerDN  <br/> |Der Distinguished Name der Vorgängerversion des Benutzers.  <br/> |
|UserDeploymentId  <br/> |Die Bereitstellungs-ID des Benutzers.  <br/> |
|InternalMailboxServer  <br/> |Der vollqualifizierte Domänenname (FQDN) des Postfachservers.  <br/> |
|InternalRpcClientServer  <br/> |Der vollqualifizierte Domänenname des RPC-Clientservers.  <br/> |
|InternalMailboxServerDN  <br/> |Der Distinguished Name des Legacy-Postfachservers.  <br/> |
|InternalEcpUrl  <br/> |Die interne URL der Exchange-Systemsteuerung.  <br/> |
|InternalEcpVoicemailUrl  <br/> |Die interne URL der Exchange-Systemsteuerung für die Voicemail-Anpassung.  <br/> |
|InternalEcpEmailSubscriptionsUrl  <br/> |Die interne URL der Exchange-Systemsteuerung für e-Mail-Abonnements.  <br/> |
|InternalEcpTextMessagingUrl  <br/> |Die interne URL der Exchange-Systemsteuerung für Text Nachrichten.  <br/> |
|InternalEcpDeliveryReportUrl  <br/> |Die interne URL der Exchange-Systemsteuerung für Zustellungsberichte.  <br/> |
|InternalEcpRetentionPolicyTagsUrl  <br/> |Die interne URL der Exchange-Systemsteuerung für RetentionPolicy-Tags.  <br/> |
|InternalEcpPublishingUrl  <br/> |Die interne URL der Exchange-Systemsteuerung für die Veröffentlichung.  <br/> |
|InternalEwsUrl  <br/> |Die interne URL von Exchange Webdienste.  <br/> |
|InternalOABUrl  <br/> |Die interne URL des Offlineadressbuchs (OAB).  <br/> |
|InternalUMUrl  <br/> |Die interne URL der Unified Messaging-Dienste.  <br/> |
|InternalWebClientUrls  <br/> |Die internen URLs des Exchange-Webclients.  <br/> |
|MailboxDN  <br/> |Der Distinguished Name der Postfachdatenbank des Postfachs des Benutzers.  <br/> |
|PublicFolderServer  <br/> |Der Name des Servers für Öffentliche Ordner.  <br/> |
|ActiveDirectoryServer  <br/> |Der Name des Active Directory Servers.  <br/> |
|ExternalMailboxServer  <br/> |Der Name des RPC-über-HTTP-Servers.  <br/> |
|ExternalMailboxServerRequiresSSL  <br/> |Das Kennzeichen, ob der RPC-über-HTTP-Server SSL erfordert.  <br/> |
|ExternalMailboxServerAuthenticationMethods  <br/> |Die vom RPC-über-HTTP-Server unterstützten Authentifizierungsmethoden.  <br/> |
|EcpVoicemailUrlFragment,  <br/> |Das URL-Fragment der Exchange-Systemsteuerung für die Voicemail-Anpassung.  <br/> |
|EcpEmailSubscriptionsUrlFragment  <br/> |Das URL-Fragment der Exchange-Systemsteuerung für e-Mail-Abonnements.  <br/> |
|EcpTextMessagingUrlFragment  <br/> |Das URL-Fragment der Exchange-Systemsteuerung für Text Nachrichten.  <br/> |
|EcpDeliveryReportUrlFragment  <br/> |Das URL-Fragment der Exchange-Systemsteuerung für Zustellungsberichte.  <br/> |
|EcpRetentionPolicyTagsUrlFragment  <br/> |Das URL-Fragment der Exchange-Systemsteuerung für RetentionPolicy-Tags.  <br/> |
|EcpPublishingUrlFragment  <br/> |Das URL-Fragment der Exchange-Systemsteuerung für die Veröffentlichung.  <br/> |
|ExternalEcpUrl  <br/> |Die externe URL der Exchange-Systemsteuerung.  <br/> |
|ExternalEcpVoicemailUrl  <br/> |Die externe URL der Exchange-Systemsteuerung für die Voicemail-Anpassung.  <br/> |
|ExternalEcpEmailSubscriptionsUrl  <br/> |Die externe URL der Exchange-Systemsteuerung für e-Mail-Abonnements.  <br/> |
|ExternalEcpTextMessagingUrl  <br/> |Die externe URL der Exchange-Systemsteuerung für Text Nachrichten.  <br/> |
|ExternalEcpDeliveryReportUrl  <br/> |Die externe URL der Exchange-Systemsteuerung für Zustellungsberichte.  <br/> |
|ExternalEcpRetentionPolicyTagsUrl  <br/> |Die externe URL der Exchange-Systemsteuerung für RetentionPolicy-Tags.  <br/> |
|ExternalEcpPublishingUrl  <br/> |Die externe URL der Exchange-Systemsteuerung für die Veröffentlichung.  <br/> |
|ExternalEwsUrl  <br/> |Die externe URL der Exchange-Webdienste.  <br/> |
|ExternalOABUrl  <br/> |Die externe URL des OAB.  <br/> |
|ExternalUMUrl  <br/> |Die externe URL der Unified Messaging-Dienste.  <br/> |
|ExternalWebClientUrls  <br/> |Die externen URLs des Exchange-Webclients.  <br/> |
|CrossOrganizationSharingEnabled  <br/> |Gibt an, dass die organisationsübergreifende Freigabe aktiviert ist.  <br/> |
|AlternateMailboxes  <br/> |Auflistung von alternativen Postfächern.  <br/> |
|CasVersion  <br/> |Die Version des Client Zugriffsservers, der die Anforderung bedient (beispielsweise 14. xx. JJJJ. ZZZ  <br/> |
|EwsSupportedSchemas  <br/> |Eine durch trennzeichengetrennte Liste von Schemaversionen, die von Exchange Webdienste unterstützt werden. Die Schema Versionswerte sind identisch mit den Werten der **ExchangeServerVersion** -Aufzählung.  <br/> |
|InternalPop3Connections  <br/> |Die Liste der internen Verbindungseinstellungen für POP3-Protokoll Verbindungen.  <br/> |
|ExternalPop3Connections  <br/> |Die Liste Externe Verbindungseinstellungen für POP3-Protokoll Verbindungen.  <br/> |
|InternalImap4Connections  <br/> |Die Liste der internen Verbindungseinstellungen für IMAP4-Protokoll Verbindungen.  <br/> |
|ExternalImap4Connections  <br/> |Die Liste Externe Verbindungseinstellungen für IMAP4-Protokoll Verbindungen.  <br/> |
|InternalSmtpConnections  <br/> |Die Liste der internen Verbindungseinstellungen für SMTP-Verbindungen.  <br/> |
|ExternalSmtpConnections  <br/> |Die Liste Externe Verbindungseinstellungen für SMTP-Verbindungen.  <br/> |
|InternalServerExclusiveConnect  <br/> |Das exklusive Connect-Flag für interne Server. Bei Festlegung auf "aus" sollten Clients nicht über dieses Protokoll eine Verbindung herstellen.  <br/> |
|ExternalServerExclusiveConnect  <br/> |Das exklusive Connect-Flag für externe Server. Bei Festlegung auf "on" sollten Clients über dieses Protokoll eine Verbindung herstellen.  <br/> |
|ExchangeRpcUrl  <br/> |Die URL, die für Remote Prozeduraufrufe verwendet wurde. Diese URL ist auf dem Server intern und darf nicht von Clients verwendet werden.  <br/> |
|ShowGalAsDefaultView  <br/> |Gibt einen booleschen Wert an, der angibt, ob die GAL als Adressbuch angezeigt werden soll. Der Textwert "true" gibt an, dass die GAL standardmäßig angezeigt werden soll. Der Textwert "false" gibt an, dass die Kontaktlisteangezeigt werden soll.  <br/> |
|AutoDiscoverSMTPAddress  <br/> |Die primäre SMTP-Adresse der AutoErmittlung für den Benutzer. Dies ist die Proxyadresse anstelle der e-Mail-Adresse des Benutzers, wenn eine Proxyadresse vorhanden ist.  <br/> |
|InteropExternalEwsUrl  <br/> |Die externe URL des Webdienst-Endpunkts des Servers. Dies ist die URL zu einem Server, der Postfächer bereitstellen kann, die auf einem Server gehostet werden, der nicht über die Webdienste verfügt.  <br/> |
|ExternalEwsVersion  <br/> |Die Version des Webdienste-Servers, der die angegebene Anforderung abgibt.  <br/> |
|InteropExternalEwsVersion  <br/> |Die Version des Servers InteropExternalEwsUrl zeigt auf.  <br/> |
|MobileMailboxPolicyInterop  <br/> |Die Einstellungen für Mobile Postfachrichtlinien.  <br/> |
|GroupingInformation  <br/> |Ein Wert, der in Verbindung mit der ExternalEwsUrl-Einstellung verwendet wird, um mehrere Postfächer zusammen zu gruppieren, um die Affinität beim Abonnieren von Benachrichtigungen [beizubehalten](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx) .  <br/> |
|UserMSOnline  <br/> |Ein boolescher Wert, der angibt, ob das Postfach des Benutzers in Exchange Online oder Exchange Online als Teil Office 365 gehostet wird.  <br/> |
|MapiHttpEnabled  <br/> |Ein boolescher Wert, der angibt, ob über das MAPI/http-Protokoll auf das Postfach des Benutzers zugegriffen werden kann.  <br/> |
   
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |Auto Ermittlungs Schema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
  
[GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)

