---
title: MailTipsRequested
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailTipsRequested
api_type:
- schema
ms.assetid: 8037bbe5-a37f-4f77-8209-27a94f9095ef
description: Das MailTipsRequested-Element enthält die Typen von e-Mail-Tipps, die vom Dienst angefordert werden.
ms.openlocfilehash: bcb2ebf15e628a04e8507f938d385cf113f2f2a3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465898"
---
# <a name="mailtipsrequested"></a>MailTipsRequested

Das **MailTipsRequested** -Element enthält die Typen von e-Mail-Tipps, die vom Dienst angefordert werden. 
  
```XML
<MailTipsRequested/>
```

 **MailTipTypes**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetMailTips](getmailtips.md) <br/> |Enthält die Empfänger und Typen von e-Mail-Tipps, die abgerufen werden sollen.  <br/> |
   
## <a name="text-value"></a>Textwert

In der folgenden Tabelle sind die möglichen Werte für das **MailTipsRequested** -Element aufgeführt. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|Alle  <br/> |Stellt alle verfügbaren e-Mail-Tipps dar.  <br/> |
|OutOfOfficeMessage  <br/> |Stellt die Abwesenheit (Out of Office, OOF) Meldung dar.  <br/> |
|MailboxFullStatus  <br/> |Stellt den Status für ein vollständiges Postfach dar.  <br/> |
|CustomMailTip  <br/> |Stellt einen benutzerdefinierten e-Mail-Tipp dar.  <br/> |
|ExternalMemberCount  <br/> |Stellt die Anzahl externer Member dar.  <br/> |
|TotalMemberCount  <br/> |Stellt die Anzahl aller Elemente dar.  <br/> |
|MaxMessageSize  <br/> |Stellt die maximale Nachrichtengröße dar, die ein Empfänger annehmen kann.  <br/> |
|DeliveryRestriction  <br/> |Gibt an, ob durch Übermittlungseinschränkungen verhindert wird, dass die Nachricht des Absenders den Empfänger erreicht.  <br/> |
|ModerationStatus  <br/> |Gibt an, ob die Nachricht des Absenders von einem Moderator überprüft wird.  <br/> |
|InvalidRecipient  <br/> |Gibt an, ob der Empfänger ungültig ist.  <br/> |
   
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

