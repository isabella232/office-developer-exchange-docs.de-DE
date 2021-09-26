---
title: Aktionen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Actions
api_type:
- schema
ms.assetid: c5aa96b1-2d8b-422f-8c2f-f118572ab23f
description: Das Actions-Element stellt den Satz von Aktionen dar, die für eine Nachricht verfügbar sind, wenn die Bedingungen erfüllt sind.
ms.openlocfilehash: 7f6608af5b8a9eb2772228a638fc42b9558f1e42
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546861"
---
# <a name="actions"></a>Aktionen

Das  Actions-Element stellt den Satz von Aktionen dar, die für eine Nachricht verfügbar sind, wenn die Bedingungen erfüllt sind. 
  
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
|[AssignCategories](assigncategories.md) <br/> |Stellt die Kategorien dar, die für E-Mail-Nachrichten gestempelt werden.  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |Gibt die ID des Ordners an, in den E-Mail-Elemente kopiert werden.  <br/> |
|[Löschen](delete.md) <br/> |Gibt an, ob Nachrichten in den Ordner "Gelöschte Elemente" verschoben werden sollen.  <br/> |
|[ForwardAsAttachmentToRecipients](forwardasattachmenttorecipients.md) <br/> |Gibt die E-Mail-Adressen an, an die Nachrichten als Anlagen weitergeleitet werden sollen.  <br/> |
|[ForwardToRecipients](forwardtorecipients.md) <br/> |Gibt die E-Mail-Adressen an, an die Nachrichten weitergeleitet werden sollen.  <br/> |
|[MarkImportance](markimportance.md) <br/> |Gibt die Wichtigkeit an, die nachrichtenstempelt werden soll.  <br/> |
|[MarkAsRead](markasread.md) <br/> |Gibt an, ob Nachrichten als gelesen markiert werden sollen.  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |Gibt die ID des Ordners an, in den E-Mail-Elemente verschoben werden.  <br/> |
|[PermanentDelete](permanentdelete.md) <br/> |Gibt an, ob Nachrichten dauerhaft gelöscht und nicht im Ordner "Gelöschte Elemente" gespeichert werden sollen.  <br/> |
|[RedirectToRecipients](redirecttorecipients.md) <br/> |Gibt die E-Mail-Adressen an, an die Nachrichten umgeleitet werden sollen.  <br/> |
|[SendSMSAlertToRecipients](sendsmsalerttorecipients.md) <br/> |Gibt die Mobiltelefonnummern an, an die eine SMS-Warnung (Short Message Service) gesendet werden soll.  <br/> |
|[ServerReplyWithMessage](serverreplywithmessage.md) <br/> |Angibt. Die ID der Vorlagennachricht, die als Antwort auf eingehende Nachrichten gesendet werden soll.  <br/> |
|[StopProcessingRules](stopprocessingrules.md) <br/> |Gibt an, ob nachfolgende Regeln ausgewertet werden sollen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Regel (RuleType)](rule-ruletype.md) <br/> |Stellt eine einzelne Regel im Postfach eines Benutzers dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

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

