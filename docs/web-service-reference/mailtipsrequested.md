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
description: Das MailTipsRequested-Element enthält die Arten von e-Mail-Infos aus dem Dienst angefordert.
ms.openlocfilehash: fa2bef394ea8473aa65bdc2f1d39c0794186fdc6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830348"
---
# <a name="mailtipsrequested"></a>MailTipsRequested

Das **MailTipsRequested** -Element enthält die Arten von e-Mail-Infos aus dem Dienst angefordert. 
  
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
|[GetMailTips](getmailtips.md) <br/> |Enthält die Empfänger und Typen von e-Mail-Infos abgerufen.  <br/> |
   
## <a name="text-value"></a>Textwert

Die folgende Tabelle enthält die möglichen Werte für das **MailTipsRequested** -Element. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|Alle  <br/> |Stellt alle verfügbaren e-Mail-Infos.  <br/> |
|OutOfOfficeMessage  <br/> |Stellt die Nachricht Out of Office (OOF) dar.  <br/> |
|MailboxFullStatus  <br/> |Stellt den Status für ein Postfach, das voll ist.  <br/> |
|CustomMailTip  <br/> |Stellt eine benutzerdefinierte e-Mail-Info.  <br/> |
|ExternalMemberCount  <br/> |Die Anzahl der externen Elemente darstellt.  <br/> |
|TotalMemberCount  <br/> |Stellt die Anzahl aller Elemente.  <br/> |
|MaxMessageSize  <br/> |Stellt die maximale Größe von Nachrichten, die ein Empfänger akzeptieren kann.  <br/> |
|DeliveryRestriction  <br/> |Gibt an, ob Einschränkungen Übermittlung des Absenders der Nachricht verhindern Erreichen des Empfängers.  <br/> |
|ModerationStatus  <br/> |Gibt an, ob der Absender der Nachricht von einem Moderator überprüft werden.  <br/> |
|InvalidRecipient  <br/> |Gibt an, ob der Empfänger ungültig ist.  <br/> |
   
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

