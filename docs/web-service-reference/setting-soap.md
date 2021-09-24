---
title: Einstellung (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 43db26e1-f7be-49fd-b26b-fc1b10bd3458
description: Das Setting-Element stellt eine zurückzugebende Konfigurationseinstellung dar.
ms.openlocfilehash: 2e03bfacaf36676ee4687c148f3b08732a9f17b1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539143"
---
# <a name="setting-soap"></a>Einstellung (SOAP)

Das **Setting-Element** stellt eine zurückzugebende Konfigurationseinstellung dar. 
  
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
|UserDN  <br/> |Der alte Distinguished Name des Benutzers.  <br/> |
|UserDeploymentId  <br/> |Der Bereitstellungsbezeichner des Benutzers.  <br/> |
|InternalMailboxServer  <br/> |Der vollqualifizierte Domänenname (FQDN) des Postfachservers.  <br/> |
|InternalRpcClientServer  <br/> |Der vollqualifizierte Domänenname des RPC-Clientservers.  <br/> |
|InternalMailboxServerDN  <br/> |Der alte Distinguished Name des Postfachservers.  <br/> |
|InternalEcpUrl  <br/> |Die interne URL der Exchange Systemsteuerung.  <br/> |
|InternalEcpVoicemailUrl  <br/> |Die interne URL der Exchange Systemsteuerung für die Anpassung von VoiceMail.  <br/> |
|InternalEcpEmailSubscriptionsUrl  <br/> |Die interne URL der Exchange Systemsteuerung für E-Mail-Abonnements.  <br/> |
|InternalEcpTextMessagingUrl  <br/> |Die interne URL der Exchange Systemsteuerung für Textnachrichten.  <br/> |
|InternalEcpDeliveryReportUrl  <br/> |Die interne URL der Exchange Systemsteuerung für Übermittlungsberichte.  <br/> |
|InternalEcpRetentionPolicyTagsUrl  <br/> |Die interne URL der Exchange-Systemsteuerung für RetentionPolicy-Tags.  <br/> |
|InternalEcpPublishingUrl  <br/> |Die interne URL der Exchange Systemsteuerung für die Veröffentlichung.  <br/> |
|InternalEwsUrl  <br/> |Die interne URL von Exchange Webdiensten.  <br/> |
|InternalOABUrl  <br/> |Die interne URL des Offlineadressbuchs (OAB).  <br/> |
|InternalUMUrl  <br/> |Die interne URL der Unified Messaging-Dienste.  <br/> |
|InternalWebClientUrls  <br/> |Die internen URLs des Exchange Webclients.  <br/> |
|MailboxDN  <br/> |Der Distinguished Name der Postfachdatenbank des Postfachs des Benutzers.  <br/> |
|PublicFolderServer  <br/> |Der Name des Servers für öffentliche Ordner.  <br/> |
|ActiveDirectoryServer  <br/> |Der Name des Active Directory-Servers.  <br/> |
|ExternalMailboxServer  <br/> |Der Name des RPC über HTTP-Server.  <br/> |
|ExternalMailboxServerRequiresSSL  <br/> |Der Indikator dafür, ob der RPC über HTTP-Server SSL erfordert.  <br/> |
|ExternalMailboxServerAuthenticationMethods  <br/> |Die Authentifizierungsmethoden, die vom RPC über HTTP-Server unterstützt werden.  <br/> |
|EcpVoicemailUrlFragment,  <br/> |Das URL-Fragment der Exchange Systemsteuerung für die VoiceMailanpassung.  <br/> |
|EcpEmailSubscriptionsUrlFragment  <br/> |Das URL-Fragment der Exchange Systemsteuerung für E-Mail-Abonnements.  <br/> |
|EcpTextMessagingUrlFragment  <br/> |Das URL-Fragment der Exchange Systemsteuerung für Textnachrichten.  <br/> |
|EcpDeliveryReportUrlFragment  <br/> |Das URL-Fragment der Exchange Systemsteuerung für Übermittlungsberichte.  <br/> |
|EcpRetentionPolicyTagsUrlFragment  <br/> |Das URL-Fragment der Exchange Systemsteuerung für RetentionPolicy-Tags.  <br/> |
|EcpPublishingUrlFragment  <br/> |Das URL-Fragment der Exchange Systemsteuerung für die Veröffentlichung.  <br/> |
|ExternalEcpUrl  <br/> |Die externe URL der Exchange Systemsteuerung.  <br/> |
|ExternalEcpVoicemailUrl  <br/> |Die externe URL der Exchange Systemsteuerung für die VoiceMailanpassung.  <br/> |
|ExternalEcpEmailSubscriptionsUrl  <br/> |Die externe URL der Exchange Systemsteuerung für E-Mail-Abonnements.  <br/> |
|ExternalEcpTextMessagingUrl  <br/> |Die externe URL der Exchange Systemsteuerung für Textnachrichten.  <br/> |
|ExternalEcpDeliveryReportUrl  <br/> |Die externe URL der Exchange Systemsteuerung für Übermittlungsberichte.  <br/> |
|ExternalEcpRetentionPolicyTagsUrl  <br/> |Die externe URL der Exchange-Systemsteuerung für RetentionPolicy-Tags.  <br/> |
|ExternalEcpPublishingUrl  <br/> |Die externe URL der Exchange-Systemsteuerung für die Veröffentlichung.  <br/> |
|ExternalEwsUrl  <br/> |Die externe URL der Exchange Webdienste.  <br/> |
|ExternalOABUrl  <br/> |Die externe URL des OAB.  <br/> |
|ExternalUMUrl  <br/> |Die externe URL der Unified Messaging-Dienste.  <br/> |
|ExternalWebClientUrls  <br/> |Die externen URLs des Exchange Webclients.  <br/> |
|CrossOrganizationSharingEnabled  <br/> |Gibt an, dass die organisationsübergreifende Freigabe aktiviert ist.  <br/> |
|AlternateMailboxes  <br/> |Sammlung alternativer Postfächer.  <br/> |
|CasVersion  <br/> |Die Version des Clientzugriffsservers, der die Anforderung bedient (z. B. 14.XX.YYYY. ZZZ)  <br/> |
|EwsSupportedSchemas  <br/> |Eine durch Trennzeichen getrennte Liste von Schemaversionen, die von Exchange Webdiensten unterstützt werden. Die Schemaversionswerte entsprechen den Werten der **ExchangeServerVersion-Enumeration.**  <br/> |
|InternalPop3Connections  <br/> |Die interne Verbindungseinstellungsliste für POP3-Protokollverbindungen.  <br/> |
|ExternalPop3Connections  <br/> |Die Liste der externen Verbindungseinstellungen für POP3-Protokollverbindungen.  <br/> |
|InternalImap4Connections  <br/> |Die interne Verbindungseinstellungsliste für IMAP4-Protokollverbindungen.  <br/> |
|ExternalImap4Connections  <br/> |Die Liste der externen Verbindungseinstellungen für IMAP4-Protokollverbindungen.  <br/> |
|InternalSmtpConnections  <br/> |Die interne Verbindungseinstellungsliste für SMTP-Verbindungen.  <br/> |
|ExternalSmtpConnections  <br/> |Die Liste der externen Verbindungseinstellungen für SMTP-Verbindungen.  <br/> |
|InternalServerExclusiveConnect  <br/> |Das flag für die exklusive Verbindung des internen Servers. Wenn der Wert auf "Aus" festgelegt ist, SOLLTEN Clients keine Verbindung über dieses Protokoll herstellen.  <br/> |
|ExternalServerExclusiveConnect  <br/> |Das Flag für die exklusive Verbindung des externen Servers. Wenn der Wert auf "Ein" festgelegt ist, SOLLTEN Clients über dieses Protokoll eine Verbindung herstellen.  <br/> |
|ExchangeRpcUrl  <br/> |Die URL, die für Remoteprozeduraufrufe verwendet wurde. Diese URL ist serverintern und darf nicht von Clients verwendet werden.  <br/> |
|ShowGalAsDefaultView  <br/> |Gibt einen booleschen Wert, der angibt, ob die GAL als Adressbuch angezeigt werden soll. Der Textwert "true" gibt an, dass die GAL standardmäßig angezeigt werden soll. Der Textwert "false" gibt an, dass die Kontaktliste angezeigt werden soll.  <br/> |
|AutoDiscoverSMTPAddress  <br/> |Die primäre SMTP-Adresse der AutoErmittlung für den Benutzer. Dies ist die Proxyadresse anstelle der E-Mail-Adresse des Benutzers, wenn eine Proxyadresse vorhanden ist.  <br/> |
|InteropExternalEwsUrl  <br/> |Die externe URL des Webdienstendpunkts des Servers. Dies ist die URL zu einem Server, der Postfächer bereitstellen kann, die auf einem Server gehostet werden, der nicht über die Webdienste verfügt.  <br/> |
|ExternalEwsVersion  <br/> |Die Version des Webdienstservers, der die angegebene Anforderung übermittelt.  <br/> |
|InteropExternalEwsVersion  <br/> |Die Version des Servers InteropExternalEwsUrl verweist auf.  <br/> |
|MobileMailboxPolicyInterop  <br/> |Die Richtlinieneinstellungen für mobile Postfächer.  <br/> |
|GroupingInformation  <br/> |Ein Wert, der in Verbindung mit der ExternalEwsUrl-Einstellung verwendet wird, um mehrere Postfächer zu gruppieren, um die [Affinität](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx) beim Abonnieren von Benachrichtigungen beizubehalten.  <br/> |
|UserMSOnline  <br/> |Ein boolescher Wert, der angibt, ob das Postfach des Benutzers in Exchange Online oder Exchange Online als Teil Office 365 gehostet wird.  <br/> |
|MapiHttpEnabled  <br/> |Ein boolescher Wert, der angibt, ob auf das Postfach des Benutzers über das MAPI/HTTP-Protokoll zugegriffen werden kann.  <br/> |
   
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
  
[GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)

