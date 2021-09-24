---
title: Aktionen (RuleActionsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 2afba70c-65f7-458c-a4e6-a2cd9bccc0f9
description: Das Actions-Element enthält eine Liste der Aktionen, die mit Posteingangsregeln verknüpft sind.
ms.openlocfilehash: d91a76889778b363ea931afb98ae9817e3b7c3c1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520178"
---
# <a name="actions-ruleactionstype"></a>Aktionen (RuleActionsType)

Das  Actions-Element enthält eine Liste der Aktionen, die mit Posteingangsregeln verknüpft sind. 
  
```XML
<Actions>
   <AssignCategories/>
   <CopyToFolder/>
   <Delete/>
   <ForwardAsAttachmentToRecipients/>
   <ForwardToRecipients/>
   <MarkImportance/>
   <MarkAsRead/>
   <MoveToFolder/>
   <PermanentDelete/>
   <RedirectToRecipients/>
   <SendSMSAlertToRecipients/>
   <ServerReplyWithMessage/>
   <StopProcessingRules/>
</Actions>
```

 **RuleActionsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[AssignCategories](assigncategories.md)  |  [CopyToFolder](copytofolder.md)  |  [Löschen](delete.md)  |  [ForwardAsAttachmentToRecipients](forwardasattachmenttorecipients.md)  |  [ForwardToRecipients](forwardtorecipients.md)  |  [MarkImportance](markimportance.md)  |  [MarkAsRead](markasread.md)  |  [MoveToFolder](movetofolder.md)  |  [PermanentDelete](permanentdelete.md)  |  [RedirectToRecipients](redirecttorecipients.md)  |  [SendSMSAlertToRecipients](sendsmsalerttorecipients.md)  |  [ServerReplyWithMessage](serverreplywithmessage.md)  |  [StopProcessingRules](stopprocessingrules.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Regel (RuleType)](rule-ruletype.md)
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

