---
title: FieldUri (Rule)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: cecdea78-de9c-48be-ae31-03877feafeec
description: Das FieldURI-Element gibt den URI für das Regelfeld an, das den Überprüfungsfehler verursacht hat.
ms.openlocfilehash: c1390f6643614216fa86053368ba012cd0883ff7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513731"
---
# <a name="fielduri-rule"></a>FieldUri (Rule)

Das **FieldURI-Element** gibt den URI für das Regelfeld an, das den Überprüfungsfehler verursacht hat. 
  
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
|[Fehler](error.md) <br/> |Stellt einen einzelnen Überprüfungsfehler für einen bestimmten Regeleigenschaftswert, einen Prädikateigenschaftenwert oder einen Aktionseigenschaftswert dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert für dieses Element ist auf eine der folgenden Zeichenfolgen beschränkt:
  
- RuleId
    
- DisplayName
    
- Priorität
    
- IsNotSupported
    
- Aktionen
    
- Bedingung:Kategorien
    
- Condition:ContainsBodyStrings
    
- Condition:ContainsHeaderStrings
    
- Condition:ContainsRecipientStrings
    
- Condition:ContainsSenderStrings
    
- Condition:ContainsSubjectOrBodyStrings
    
- Condition:ContainsSubjectStrings
    
- Bedingung:FlaggedForAction
    
- Condition:FromAddresses
    
- Bedingung:FromConnectedAccounts
    
- Condition:HasAttachments
    
- Bedingung:Wichtigkeit
    
- Condition:IsApprovalRequest
    
- Condition:IsAutomaticForward
    
- Condition:IsAutomaticReply
    
- Bedingung:IsEncrypted
    
- Condition:IsMeetingRequest
    
- Condition:IsMeetingResponse
    
- Condition:IsNDR
    
- Condition:IsPermissionControlled
    
- Condition:IsReadReceipt
    
- Bedingung:IsSigned
    
- Bedingung:IsVoicemail
    
- Condition:ItemClasses
    
- Condition:MessageClassifications
    
- Condition:NotSentToMe
    
- Condition:SentCcMe
    
- Condition:SentOnlyToMe
    
- Condition:SentToAddresses
    
- Condition:SentToMe
    
- Condition:SentToOrCcMe
    
- Bedingung:Vertraulichkeit
    
- Condition:WithinDateRange
    
- Condition:WithinSizeRange
    
- Exception:Categories
    
- Exception:ContainsBodyStrings
    
- Exception:ContainsHeaderStrings
    
- Exception:ContainsRecipientStrings
    
- Exception:ContainsSenderStrings
    
- Exception:ContainsSubjectOrBodyStrings
    
- Exception:ContainsSubjectStrings
    
- Exception:FlaggedForAction
    
- Ausnahme:FromAddresses
    
- Ausnahme:FromConnectedAccounts
    
- Exception:HasAttachments
    
- Exception:Importance
    
- Exception:IsApprovalRequest
    
- Exception:IsAutomaticForward
    
- Exception:IsAutomaticReply
    
- Ausnahme:IsEncrypted
    
- Exception:IsMeetingRequest
    
- Exception:IsMeetingResponse
    
- Ausnahme:IsNDR
    
- Exception:IsPermissionControlled
    
- Exception:IsReadReceipt
    
- Ausnahme:IsSigned
    
- Exception:IsVoicemail
    
- Exception:ItemClasses
    
- Exception:MessageClassifications
    
- Exception:NotSentToMe
    
- Exception:SentCcMe
    
- Exception:SentOnlyToMe
    
- Exception:SentToAddresses
    
- Exception:SentToMe
    
- Exception:SentToOrCcMe
    
- Exception:Sensitivity
    
- Exception:WithinDateRange
    
- Exception:WithinSizeRange
    
- Action:AssignCategories
    
- Action:CopyToFolder
    
- Action:Delete
    
- Action:ForwardAsAttachmentToRecipients
    
- Action:ForwardToRecipients
    
- Action:MarkImportance
    
- Action:MarkAsRead
    
- Action:MoveToFolder
    
- Action:PermanentDelete
    
- Action:RedirectToRecipients
    
- Action:SendSMSAlertToRecipients
    
- Action:ServerReplyWithMessage
    
- Action:StopProcessingRules
    
- IsEnabled
    
- IsInError
    
- Bedingungen
    
- Ausnahmen
    
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

