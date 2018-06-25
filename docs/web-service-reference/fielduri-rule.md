---
title: FieldUri (Regel)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecdea78-de9c-48be-ae31-03877feafeec
description: Das FieldURI-Element gibt den URI für die Regel dar, das den Validierungsfehler verursacht hat.
ms.openlocfilehash: 88ba54994625d3a950b58e900f28c986c31eddac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758411"
---
# <a name="fielduri-rule"></a>FieldUri (Regel)

Das **FieldURI** -Element gibt den URI für die Regel dar, das den Validierungsfehler verursacht hat. 
  
```XML
<FieldURI/>
```

 **RuleFieldURIType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Fehler](error.md) <br/> |Stellt einen einzelnen Gültigkeitsprüfungsfehler auf eine bestimmte Regel Eigenschaftswert, Prädikat Eigenschaftswert oder Aktionswert-Eigenschaft.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert für dieses Element ist auf eine der folgenden Zeichenfolgen beschränkt:
  
- Regel-ID
    
- DisplayName
    
- Priorität
    
- IsNotSupported
    
- Aktionen
    
- Bedingung: Kategorien
    
- Bedingung: ContainsBodyStrings
    
- Bedingung: ContainsHeaderStrings
    
- Bedingung: ContainsRecipientStrings
    
- Bedingung: ContainsSenderStrings
    
- Bedingung: ContainsSubjectOrBodyStrings
    
- Bedingung: ContainsSubjectStrings
    
- Bedingung: FlaggedForAction
    
- Bedingung: FromAddresses
    
- Bedingung: FromConnectedAccounts
    
- Bedingung: HasAttachments
    
- Bedingung: Wichtigkeit
    
- Bedingung: IsApprovalRequest
    
- Bedingung: IsAutomaticForward
    
- Bedingung: IsAutomaticReply
    
- Bedingung: IsEncrypted
    
- Bedingung: IsMeetingRequest
    
- Bedingung: IsMeetingResponse
    
- Bedingung: IsNDR
    
- Bedingung: IsPermissionControlled
    
- Bedingung: IsReadReceipt
    
- Bedingung: IsSigned
    
- Bedingung: IsVoicemail
    
- Bedingung: ItemClasses
    
- Bedingung: MessageClassifications
    
- Bedingung: NotSentToMe
    
- Bedingung: SentCcMe
    
- Bedingung: SentOnlyToMe
    
- Bedingung: SentToAddresses
    
- Bedingung: SentToMe
    
- Bedingung: SentToOrCcMe
    
- Bedingung: Vertraulichkeit
    
- Bedingung: WithinDateRange
    
- Bedingung: WithinSizeRange
    
- Ausnahme: Kategorien
    
- Ausnahme: ContainsBodyStrings
    
- Ausnahme: ContainsHeaderStrings
    
- Ausnahme: ContainsRecipientStrings
    
- Ausnahme: ContainsSenderStrings
    
- Ausnahme: ContainsSubjectOrBodyStrings
    
- Ausnahme: ContainsSubjectStrings
    
- Ausnahme: FlaggedForAction
    
- Ausnahme: FromAddresses
    
- Ausnahme: FromConnectedAccounts
    
- Ausnahme: HasAttachments
    
- Ausnahme: Wichtigkeit
    
- Ausnahme: IsApprovalRequest
    
- Ausnahme: IsAutomaticForward
    
- Ausnahme: IsAutomaticReply
    
- Ausnahme: IsEncrypted
    
- Ausnahme: IsMeetingRequest
    
- Ausnahme: IsMeetingResponse
    
- Ausnahme: IsNDR
    
- Ausnahme: IsPermissionControlled
    
- Ausnahme: IsReadReceipt
    
- Ausnahme: IsSigned
    
- Ausnahme: IsVoicemail
    
- Ausnahme: ItemClasses
    
- Ausnahme: MessageClassifications
    
- Ausnahme: NotSentToMe
    
- Ausnahme: SentCcMe
    
- Ausnahme: SentOnlyToMe
    
- Ausnahme: SentToAddresses
    
- Ausnahme: SentToMe
    
- Ausnahme: SentToOrCcMe
    
- Ausnahme: Vertraulichkeit
    
- Ausnahme: WithinDateRange
    
- Ausnahme: WithinSizeRange
    
- Aktion: AssignCategories
    
- Aktion: CopyToFolder
    
- Löschen der Aktion:
    
- Aktion: ForwardAsAttachmentToRecipients
    
- Aktion: ForwardToRecipients
    
- Aktion: MarkImportance
    
- Aktion: MarkAsRead
    
- Aktion: MoveToFolder
    
- Aktion: PermanentDelete
    
- Aktion: RedirectToRecipients
    
- Aktion: SendSMSAlertToRecipients
    
- Aktion: ServerReplyWithMessage
    
- Aktion: StopProcessingRules
    
- IsEnabled
    
- IsInError
    
- Bedingungen
    
- Ausnahmen
    
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

