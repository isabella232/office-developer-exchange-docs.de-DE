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
description: Das Actions-Element repräsentiert den Satz von Aktionen, die sind verfügbar, die auf eine Nachricht durchgeführt werden, wenn die Bedingungen erfüllt sind.
ms.openlocfilehash: 093d2f28135c6077b6cea488591573af0182934b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757214"
---
# <a name="actions"></a>Aktionen

Das **Actions** -Element repräsentiert den Satz von Aktionen, die sind verfügbar, die auf eine Nachricht durchgeführt werden, wenn die Bedingungen erfüllt sind. 
  
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
|[AssignCategories](assigncategories.md) <br/> |Stellt die Kategorien, die auf E-mail-Nachrichten gekennzeichnet sind.  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |Identifiziert die ID des Ordners, den e-Mail-Elemente kopiert werden.  <br/> |
|[Delete](delete.md) <br/> |Gibt an, ob Nachrichten werden in den Ordner Gelöschte Objekte verschoben werden soll.  <br/> |
|[ForwardAsAttachmentToRecipients](forwardasattachmenttorecipients.md) <br/> |Gibt die E-mail-Adressen, an die Nachrichten als Anlage weitergeleitet werden sollen.  <br/> |
|[ForwardToRecipients](forwardtorecipients.md) <br/> |Gibt die E-mail-Adressen, werden Nachrichten weitergeleitet werden.  <br/> |
|[MarkImportance](markimportance.md) <br/> |Gibt die Wichtigkeit, die auf Nachrichten versehen werden.  <br/> |
|[MarkAsRead](markasread.md) <br/> |Gibt an, ob Nachrichten als gelesen markiert werden sollen.  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |Identifiziert die ID des Ordners, den e-Mail-Elemente in verschoben werden sollen.  <br/> |
|[PermanentDelete](permanentdelete.md) <br/> |Gibt an, ob Nachrichten werden dauerhaft gelöscht und nicht in den Ordner Gelöschte Objekte gespeichert werden.  <br/> |
|[RedirectToRecipients](redirecttorecipients.md) <br/> |Gibt die E-mail-Adressen, werden Nachrichten weitergeleitet werden.  <br/> |
|[SendSMSAlertToRecipients](sendsmsalerttorecipients.md) <br/> |Gibt die Mobiltelefonnummer, die ist eine Warnung Short Message Service (SMS) gesendet werden.  <br/> |
|[ServerReplyWithMessage](serverreplywithmessage.md) <br/> |Gibt an. die ID der Vorlagennachricht, die als Antwort auf eingehende Nachrichten gesendet werden sollen.  <br/> |
|[StopProcessingRules](stopprocessingrules.md) <br/> |Gibt an, ob die nachfolgende Regeln sind ausgewertet werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Regel (RuleType)](rule-ruletype.md) <br/> |Stellt eine einzelne Regel im Postfach des Benutzers an.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Bedingungen](conditions.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

