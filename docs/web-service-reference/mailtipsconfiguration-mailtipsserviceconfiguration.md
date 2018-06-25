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
description: Das MailTipsConfiguration-Element enthält Konfigurationsinformationen für den e-Mail-Dienst Tipps Service.
ms.openlocfilehash: ea92af3ebb2d2f720e5823c5317d09d5bcdb3978
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830321"
---
# <a name="mailtipsconfiguration-mailtipsserviceconfiguration"></a>MailTipsConfiguration (MailTipsServiceConfiguration)

Das **MailTipsConfiguration** -Element enthält Konfigurationsinformationen für den e-Mail-Dienst Tipps Service. 
  
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
|[MailTipsEnabled](mailtipsenabled.md) <br/> |Gibt an, ob der Mail-Tipps Dienst verfügbar ist. Dieses Element ist erforderlich.  <br/> |
|[MaxRecipientsPerGetMailTipsRequest](maxrecipientspergetmailtipsrequest.md) <br/> |Gibt die maximale Anzahl von Empfängern, die an den [GetMailTips Vorgang](getmailtips-operation.md)übergeben werden kann. Dieses Element ist erforderlich.  <br/> |
|[MaxMessageSize](maxmessagesize.md) <br/> |Stellt die maximale Größe von Nachrichten, die ein Empfänger akzeptieren kann. Dieses Element ist erforderlich.  <br/> |
|[LargeAudienceThreshold](largeaudiencethreshold.md) <br/> |Stellt den Schwellenwert für die große Benutzergruppe für einen Client an. Dieses Element ist erforderlich.  <br/> |
|[ShowExternalRecipientCount](showexternalrecipientcount.md) <br/> |Gibt an, ob Consumer der [GetMailTips Vorgang](getmailtips-operation.md) müssen e-Mail-Infos anzeigen, die die Anzahl der externe Empfänger angeben, zu denen eine Nachricht adressiert ist. Dieses Element ist erforderlich.  <br/> |
|[InternalDomains (SmtpDomainList)](internaldomains-smtpdomainlist.md) <br/> |Gibt die Liste der internen SMTP-Domänen der Organisation. Dieses Element ist erforderlich.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md) <br/> |Konfigurationseinstellungen für enthält.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

