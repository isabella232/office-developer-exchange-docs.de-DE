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
description: Setting-Element stellt eine Konfigurationseinstellung zurückgegeben werden soll.
ms.openlocfilehash: cb5b1d6ab2109b48810b96221b76c6b8fc9803ac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831472"
---
# <a name="setting-soap"></a>Einstellung (SOAP)

**Setting** -Element stellt eine Konfigurationseinstellung zurückgegeben werden soll. 
  
```XML
<Setting/>
```

 **string**
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

Der Textwert für dieses Element wird die Konfigurationseinstellung. Die folgende Tabelle enthält die möglichen Konfigurationseinstellungen.
  
|**Konfigurationseinstellung**|**Beschreibung**|
|:-----|:-----|
|UserDisplayName  <br/> |Der Anzeigename des Benutzers.  <br/> |
|Folgendes  <br/> |Die legacy-DN des Benutzers.  <br/> |
|UserDeploymentId  <br/> |Die bereitstellungs-ID des Benutzers.  <br/> |
|InternalMailboxServer  <br/> |Der vollqualifizierte Domänenname (FQDN) des Postfachservers an.  <br/> |
|InternalRpcClientServer  <br/> |Der vollqualifizierte Domänenname des RPC-Client-Servers.  <br/> |
|InternalMailboxServerDN  <br/> |Die legacy-DN des Postfachservers an.  <br/> |
|InternalEcpUrl  <br/> |Die interne URL von der Exchange-Systemsteuerung.  <br/> |
|InternalEcpVoicemailUrl  <br/> |Die interne URL von der Exchange-Systemsteuerung zur Anpassung von VoiceMail.  <br/> |
|InternalEcpEmailSubscriptionsUrl  <br/> |Die interne URL von der Exchange-Systemsteuerung für e-Mail-Abonnements.  <br/> |
|InternalEcpTextMessagingUrl  <br/> |Die interne URL von der Exchange-Systemsteuerung für Textnachrichten.  <br/> |
|InternalEcpDeliveryReportUrl  <br/> |Die interne URL von der Exchange-Systemsteuerung für Delivery Reports.  <br/> |
|InternalEcpRetentionPolicyTagsUrl  <br/> |Die interne URL von der Exchange-Systemsteuerung für RetentionPolicy-Tags.  <br/> |
|InternalEcpPublishingUrl  <br/> |Die interne URL von der Exchange-Systemsteuerung für die Veröffentlichung.  <br/> |
|InternalEwsUrl  <br/> |Die interne URL der Exchange-Webdienste.  <br/> |
|InternalOABUrl  <br/> |Die interne URL für das Offlineadressbuch (OAB).  <br/> |
|InternalUMUrl  <br/> |Die interne URL der Unified Messaging-Diensten.  <br/> |
|InternalWebClientUrls  <br/> |Die internen URLs des Exchange Web-Clients.  <br/> |
|MailboxDN  <br/> |Der distinguished Name der Postfachdatenbank für das Postfach des Benutzers.  <br/> |
|PublicFolderServer  <br/> |Der Name des Servers für Öffentliche Ordner.  <br/> |
|ActiveDirectoryServer  <br/> |Der Name der Active Directory-Server.  <br/> |
|ExternalMailboxServer  <br/> |Der Name der RPC-über-HTTP-Server.  <br/> |
|ExternalMailboxServerRequiresSSL  <br/> |Das Symbol für gibt an, ob der RPC-über-HTTP-Server SSL erfordert.  <br/> |
|ExternalMailboxServerAuthenticationMethods  <br/> |Die Authentifizierungsmethoden, die durch den RPC über HTTP-Server unterstützt werden.  <br/> |
|EcpVoicemailUrlFragment,  <br/> |Das URL-Fragment Exchange-Systemsteuerung zur Anpassung von VoiceMail.  <br/> |
|EcpEmailSubscriptionsUrlFragment  <br/> |Das URL-Fragment Exchange-Systemsteuerung für e-Mail-Abonnements.  <br/> |
|EcpTextMessagingUrlFragment  <br/> |Das URL-Fragment für Textnachrichten Exchange-Systemsteuerung.  <br/> |
|EcpDeliveryReportUrlFragment  <br/> |Das URL-Fragment Exchange-Systemsteuerung für Delivery Reports.  <br/> |
|EcpRetentionPolicyTagsUrlFragment  <br/> |Das URL-Fragment Exchange-Systemsteuerung für RetentionPolicy-Tags.  <br/> |
|EcpPublishingUrlFragment  <br/> |Das URL-Fragment für die Veröffentlichung Exchange-Systemsteuerung.  <br/> |
|ExternalEcpUrl  <br/> |Die externe URL von der Exchange-Systemsteuerung.  <br/> |
|ExternalEcpVoicemailUrl  <br/> |Die externe URL von der Exchange-Systemsteuerung zur Anpassung von VoiceMail.  <br/> |
|ExternalEcpEmailSubscriptionsUrl  <br/> |Die externe URL von der Exchange-Systemsteuerung für e-Mail-Abonnements.  <br/> |
|ExternalEcpTextMessagingUrl  <br/> |Die externe URL von der Exchange-Systemsteuerung für Textnachrichten.  <br/> |
|ExternalEcpDeliveryReportUrl  <br/> |Die externe URL von der Exchange-Systemsteuerung für Delivery Reports.  <br/> |
|ExternalEcpRetentionPolicyTagsUrl  <br/> |Die externe URL von der Exchange-Systemsteuerung für RetentionPolicy-Tags.  <br/> |
|ExternalEcpPublishingUrl  <br/> |Die externe URL von der Exchange-Systemsteuerung für die Veröffentlichung.  <br/> |
|ExternalEwsUrl  <br/> |Die externe URL des Exchange-Webdienste.  <br/> |
|ExternalOABUrl  <br/> |Die externe URL des OAB.  <br/> |
|ExternalUMUrl  <br/> |Die externe URL des Unified Messaging-Diensten.  <br/> |
|ExternalWebClientUrls  <br/> |Die externen URLs des Exchange Web-Clients.  <br/> |
|CrossOrganizationSharingEnabled  <br/> |Gibt an, dass organisationsübergreifende Freigabe aktiviert ist.  <br/> |
|AlternateMailboxes  <br/> |Auflistung von alternativen Postfächer.  <br/> |
|CasVersion  <br/> |Die Version des Client Access-Servers, die die Anforderung (beispielsweise 14.XX. verarbeitet wird JJJJ. ZZZ)  <br/> |
|EwsSupportedSchemas  <br/> |Eine durch Trennzeichen getrennte Liste der Schemaversionen von Exchange-Webdienste unterstützt. Die Werte für die Schema-Version werden die gleiche wie die Werte der **ExchangeServerVersion** -Enumeration.  <br/> |
|InternalPop3Connections  <br/> |Die interne Verbindung Einstellungsliste für POP3-Protokoll Verbindungen.  <br/> |
|ExternalPop3Connections  <br/> |Die Liste der externen Verbindung Einstellungen für POP3-Protokoll Verbindungen.  <br/> |
|InternalImap4Connections  <br/> |Die interne Verbindung Einstellungsliste für IMAP4-Protokoll Verbindungen.  <br/> |
|ExternalImap4Connections  <br/> |Die Liste der externen Verbindung Einstellungen für IMAP4-Protokoll Verbindungen.  <br/> |
|InternalSmtpConnections  <br/> |Die interne Verbindung Einstellungsliste für SMTP-Verbindungen.  <br/> |
|ExternalSmtpConnections  <br/> |Die Liste der externen Verbindung Einstellungen für SMTP-Verbindungen.  <br/> |
|InternalServerExclusiveConnect  <br/> |Der interne Server exklusive verbinden Kennzeichnung. Wenn legen dann Clients "Off" nicht über dieses Protokoll eine Verbindung herstellen soll.  <br/> |
|ExternalServerExclusiveConnect  <br/> |Der externe Server exklusive verbinden Kennzeichnung. Wenn es sich bei Festlegung auf "Auf" dann Clients über dieses Protokoll eine Verbindung herstellen soll.  <br/> |
|ExchangeRpcUrl  <br/> |Die URL, die für Remoteprozeduraufrufe verwendet. Diese URL ist intern auf den Server und nicht von Clients verwendet werden soll.  <br/> |
|ShowGalAsDefaultView  <br/> |Gibt einen Boolean-Wert, der angibt, ob die globalen Adressliste als Adressbuch angezeigt werden soll. Textwert "True" gibt an, dass die globalen Adressliste ist standardmäßig angezeigt werden. Der Textwert "False" gibt an, dass der Kontaktliste enthalten ist, angezeigt werden soll.  <br/> |
|AutoDiscoverSMTPAddress  <br/> |Die AutoErmittlung primäre SMTP-Adresse für den Benutzer. Dies ist die Proxyadresse anstelle der e-Mail-Adresse des Benutzers, wenn eine Proxyadresse vorhanden ist.  <br/> |
|InteropExternalEwsUrl  <br/> |Die externe URL des Webdienst-Endpunkt des Servers an. Dies ist die URL zu einem Server, der Postfächer auf einem Server, der nicht über die Webdienste verfügt dienen kann.  <br/> |
|ExternalEwsVersion  <br/> |Die Version des Web Services-Servers, der die angegebene Anforderung übermittelt.  <br/> |
|InteropExternalEwsVersion  <br/> |Zeigt die Version des Servers InteropExternalEwsUrl auf.  <br/> |
|MobileMailboxPolicyInterop  <br/> |Die Richtlinieneinstellungen für mobile Postfächer.  <br/> |
|Werten "groupinginformation"  <br/> |Ein Wert, der in Verbindung mit der Einstellung "externalewsurl" verwendet, um mehrere Postfächer zusammen, um die [Affinität verwalten](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx) zu gruppieren, wenn Benachrichtigungen abonnieren.  <br/> |
|UserMSOnline  <br/> |Ein boolescher Wert, der angibt, ob das Postfach des Benutzers im Exchange Online gehostet wird oder Exchange Online als Teil von Office 365.  <br/> |
|MapiHttpEnabled  <br/> |Ein boolescher Wert, der angibt, ob das Postfach des Benutzers über das MAPI/HTTP-Protokoll zugegriffen werden kann.  <br/> |
   
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlung-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
  
[GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)

