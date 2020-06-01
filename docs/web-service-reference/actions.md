---
title: Aktionen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Actions
api_type:
- schema
ms.assetid: c5aa96b1-2d8b-422f-8c2f-f118572ab23f
description: Das Actions-Element stellt die Gruppe von Aktionen dar, die für eine Nachricht zur Verfügung stehen, wenn die Bedingungen erfüllt sind.
ms.openlocfilehash: 2ac53778b583595fa8be07f2c5110a9e2df16eca
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465065"
---
# <a name="actions"></a>Aktionen

Das **Actions** -Element stellt die Gruppe von Aktionen dar, die für eine Nachricht zur Verfügung stehen, wenn die Bedingungen erfüllt sind. 
  
[Regel (RuleType)](rule-ruletype.md)
  
```XML
<Actions>
    <AssignCategories>
    <CopyToFolder>
    <Delete>
    <ForwardAsAttachmentToRecipients>
    <ForwardToRecipients>
    <MarkImportance>
    <MarkAsRead>
    <MoveToFolder>
    <PermanentDelete>
    <RedirectToRecipients>
    <SendSMSAlertToRecipients>
    <ServerReplyWithMessage>
    <StopProcessingRules>
</Actions>
```

 **RuleActionsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AssignCategories](assigncategories.md) <br/> |Stellt die Kategorien dar, die auf e-Mail-Nachrichten gestempelt werden.  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |Gibt die ID des Ordners an, in den e-Mail-Elemente kopiert werden.  <br/> |
|[Löschen](delete.md) <br/> |Gibt an, ob Nachrichten in den Ordner "Gelöschte Elemente" verschoben werden sollen.  <br/> |
|[ForwardAsAttachmentToRecipients](forwardasattachmenttorecipients.md) <br/> |Gibt die e-Mail-Adressen an, an die Nachrichten als Anlagen weitergeleitet werden sollen.  <br/> |
|[ForwardToRecipients](forwardtorecipients.md) <br/> |Gibt die e-Mail-Adressen an, an die Nachrichten weitergeleitet werden sollen.  <br/> |
|[MarkImportance](markimportance.md) <br/> |Gibt die Wichtigkeit an, die für Nachrichten gestempelt werden soll.  <br/> |
|[MarkAsRead](markasread.md) <br/> |Gibt an, ob Nachrichten als gelesen markiert werden sollen.  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |Gibt die ID des Ordners an, in den e-Mail-Elemente verschoben werden.  <br/> |
|[PermanentDelete](permanentdelete.md) <br/> |Gibt an, ob Nachrichten endgültig gelöscht und nicht im Ordner "Gelöschte Elemente" gespeichert werden sollen.  <br/> |
|[RedirectToRecipients](redirecttorecipients.md) <br/> |Gibt die e-Mail-Adressen an, an die Nachrichten umgeleitet werden sollen.  <br/> |
|[SendSMSAlertToRecipients](sendsmsalerttorecipients.md) <br/> |Gibt die Mobiltelefon Nummern an, an die eine SMS-Benachrichtigung (Short Message Service) gesendet werden soll.  <br/> |
|[ServerReplyWithMessage](serverreplywithmessage.md) <br/> |Gibt an. die ID der Vorlagen Nachricht, die als Antwort auf eingehende Nachrichten gesendet werden soll.  <br/> |
|[StopProcessingRules](stopprocessingrules.md) <br/> |Gibt an, ob nachfolgende Regeln ausgewertet werden sollen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Regel (RuleType)](rule-ruletype.md) <br/> |Stellt eine einzelne Regel im Postfach eines Benutzers dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Bedingungen:](conditions.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

