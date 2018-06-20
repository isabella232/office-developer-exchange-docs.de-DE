---
title: PendingMailTips
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PendingMailTips
api_type:
- schema
ms.assetid: 0cd70eea-8d36-4b1b-bf80-5edf359e7ba7
description: Das PendingMailTips-Element gibt an, dass die e-Mail-Infos in diesem Element nicht ausgewertet werden konnte, bevor die Verarbeitung der Servertimeout abgelaufen.
ms.openlocfilehash: 73d597f6534ea29f7d26d6526c48631251521ae5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830704"
---
# <a name="pendingmailtips"></a>PendingMailTips

Das **PendingMailTips** -Element gibt an, dass die e-Mail-Infos in diesem Element nicht ausgewertet werden konnte, bevor die Verarbeitung der Servertimeout abgelaufen. 
  
```XML
<PendingMailTips>All | OutOfOfficeMessage | MailboxFullStatus | CustomMailTip | ExternalMemberCount | TotalMemberCount | MaxMessageSize | DeliveryRestriction | ModerateStatus | InvalidRecipient</PendingMailTips>
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
|[E-Mail-Infos](mailtips.md) <br/> |Stellt Werte für verschiedene Arten von e-Mail-Infos.  <br/> |
   
## <a name="text-value"></a>Textwert

Die folgende Tabelle enthält die möglichen Werte für das **PendingMailTips** -Element. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|Alle  <br/> |Stellt alle verfügbaren e-Mail-Infos.  <br/> |
|OutOfOfficeMessage  <br/> |Stellt die Nachricht Out of Office (OOF) dar.  <br/> |
|MailboxFullStatus  <br/> |Stellt den Status für ein volles Postfach an.  <br/> |
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
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

