---
title: MailTipsConfiguration (MailTipsServiceConfiguration)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MailTipsConfiguration
api_type:
- schema
ms.assetid: 9a34515e-815b-4c61-b118-d5f66b80238f
description: Das MailTipsConfiguration-Element enthält Dienstkonfigurationsinformationen für den E-Mail-Tipps-Dienst.
ms.openlocfilehash: eb86291572f6854710d01badcee2db24406844c6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524035"
---
# <a name="mailtipsconfiguration-mailtipsserviceconfiguration"></a>MailTipsConfiguration (MailTipsServiceConfiguration)

Das **MailTipsConfiguration-Element** enthält Dienstkonfigurationsinformationen für den E-Mail-Tipps-Dienst. 
  
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
|[MailTipsEnabled](mailtipsenabled.md) <br/> |Gibt an, ob der E-Mail-Tipps-Dienst verfügbar ist. Dieses Element ist erforderlich.  <br/> |
|[MaxRecipientsPerGetMailTipsRequest](maxrecipientspergetmailtipsrequest.md) <br/> |Gibt die maximale Anzahl von Empfängern an, die an den [GetMailTips-Vorgang](getmailtips-operation.md)übergeben werden können. Dieses Element ist erforderlich.  <br/> |
|[MaxMessageSize](maxmessagesize.md) <br/> |Stellt die maximale Nachrichtengröße dar, die ein Empfänger annehmen kann. Dieses Element ist erforderlich.  <br/> |
|[LargeAudienceThreshold](largeaudiencethreshold.md) <br/> |Stellt den Schwellenwert für große Benutzergruppen für einen Client dar. Dieses Element ist erforderlich.  <br/> |
|[ShowExternalRecipientCount](showexternalrecipientcount.md) <br/> |Gibt an, ob Consumer des [GetMailTips-Vorgangs](getmailtips-operation.md) E-Mail-Tipps anzeigen müssen, die die Anzahl der externen Empfänger angeben, an die eine Nachricht adressiert ist. Dieses Element ist erforderlich.  <br/> |
|[InternalDomains (SmtpDomainList)](internaldomains-smtpdomainlist.md) <br/> |Identifiziert die Liste der internen SMTP-Domänen der Organisation. Dieses Element ist erforderlich.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md) <br/> |Enthält Dienstkonfigurationseinstellungen.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

