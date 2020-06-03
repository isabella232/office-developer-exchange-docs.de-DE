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
description: Das PendingMailTips-Element gibt an, dass die e-Mail-Tipps in diesem Element nicht ausgewertet werden konnten, bevor das Verarbeitungstimeout des Servers abgelaufen ist.
ms.openlocfilehash: 715d68b367c3b7251c7406c10c1ec52dcd992a59
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529966"
---
# <a name="pendingmailtips"></a>PendingMailTips

Das **PendingMailTips** -Element gibt an, dass die e-Mail-Tipps in diesem Element nicht ausgewertet werden konnten, bevor das Verarbeitungstimeout des Servers abgelaufen ist. 
  
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
|[E-Mail-Info](mailtips.md) <br/> |Stellt Werte für verschiedene Arten von e-Mail-Tipps dar.  <br/> |
   
## <a name="text-value"></a>Textwert

In der folgenden Tabelle sind die möglichen Werte für das **PendingMailTips** -Element aufgeführt. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|Alle  <br/> |Stellt alle verfügbaren e-Mail-Tipps dar.  <br/> |
|OutOfOfficeMessage  <br/> |Stellt die Abwesenheit (Out of Office, OOF) Meldung dar.  <br/> |
|MailboxFullStatus  <br/> |Stellt den Status für ein Postfach dar, das voll ist.  <br/> |
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
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

