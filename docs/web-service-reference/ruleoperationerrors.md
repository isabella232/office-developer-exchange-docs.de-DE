---
title: RuleOperationErrors
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f15c7b9e-a670-4a11-bb62-2a298c91f142
description: Das RuleOperationErrors -Element stellt ein Array der Regel Validierungsfehler auf jede Regel dar, die einen Fehler aufweist.
ms.openlocfilehash: 2428d68719e7d9ef5d1fdf87ec94f1f9390bf631
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524497"
---
# <a name="ruleoperationerrors"></a>RuleOperationErrors

Das **RuleOperationErrors** -Element stellt ein Array der Regel Validierungsfehler auf jede Regel dar, die einen Fehler aufweist. 
  
[UpdateInboxRulesResponse](updateinboxrulesresponse.md)
  
[RuleOperationErrors](ruleoperationerrors.md)
  
```XML
<RuleOperationErrors>
    <RuleOperationError>
</RuleOperationErrors>
```

 **ArrayOfRuleOperationErrorsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[RuleOperationError](ruleoperationerror.md) <br/> |Stellt einen Regel Vorgang-Fehler dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[UpdateInboxRulesResponse](updateinboxrulesresponse.md) <br/> |Definiert eine Antwort auf eine Anforderung [UpdateInboxRules](updateinboxrules.md) .  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[UpdateInboxRules](updateinboxrules.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

