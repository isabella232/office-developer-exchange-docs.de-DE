---
title: MailTipsConfiguration (MailTipsServiceConfiguration)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailTipsConfiguration
api_type:
- schema
ms.assetid: 9a34515e-815b-4c61-b118-d5f66b80238f
description: Das MailTipsConfiguration-Element enthält Dienstkonfigurationsinformationen für den e-Mail-Spitzen Dienst.
ms.openlocfilehash: 9128ee99545066899c3b27b624f10a9f1bd36c9d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467788"
---
# <a name="mailtipsconfiguration-mailtipsserviceconfiguration"></a>MailTipsConfiguration (MailTipsServiceConfiguration)

Das **MailTipsConfiguration** -Element enthält Dienstkonfigurationsinformationen für den e-Mail-Spitzen Dienst. 
  
```XML
<MailTipsConfiguration>
   <MailTipsEnabled/>
   <MaxRecipientsPerGetMailTipsRequest/>
   <MaxMessageSize/>
   <LargeAudienceThreshold/>
   <ShowExternalRecipientCount/>
   <InternalDomains/>
</MailTipsConfiguration>
```

 **MailTipsServiceConfiguration**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MailTipsEnabled](mailtipsenabled.md) <br/> |Gibt an, ob der e-Mail-Spitzen Dienst verfügbar ist. Dieses Element ist erforderlich.  <br/> |
|[MaxRecipientsPerGetMailTipsRequest](maxrecipientspergetmailtipsrequest.md) <br/> |Gibt die maximale Anzahl von Empfängern an, die an den [GetMailTips-Vorgang](getmailtips-operation.md)übergeben werden können. Dieses Element ist erforderlich.  <br/> |
|[MaxMessageSize](maxmessagesize.md) <br/> |Stellt die maximale Nachrichtengröße dar, die ein Empfänger annehmen kann. Dieses Element ist erforderlich.  <br/> |
|[LargeAudienceThreshold](largeaudiencethreshold.md) <br/> |Stellt den Schwellenwert für hohe Benutzergruppen für einen Client dar. Dieses Element ist erforderlich.  <br/> |
|[ShowExternalRecipientCount](showexternalrecipientcount.md) <br/> |Gibt an, ob Consumer des [GetMailTips-Vorgangs](getmailtips-operation.md) e-Mail-Tipps anzeigen müssen, die die Anzahl der externen Empfänger angeben, an die eine Nachricht adressiert wird. Dieses Element ist erforderlich.  <br/> |
|[InternalDomains (SmtpDomainList)](internaldomains-smtpdomainlist.md) <br/> |Gibt die Liste der internen SMTP-Domänen der Organisation an. Dieses Element ist erforderlich.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md) <br/> |Enthält Dienst Konfigurationseinstellungen.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

