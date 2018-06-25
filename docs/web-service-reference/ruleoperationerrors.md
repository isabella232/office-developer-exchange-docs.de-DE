---
title: RuleOperationErrors
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f15c7b9e-a670-4a11-bb62-2a298c91f142
description: Das RuleOperationErrors -Element stellt ein Array der Regel Validierungsfehler auf jede Regel dar, die einen Fehler aufweist.
ms.openlocfilehash: 7dc85b5cd84af5ad00511a3df2b31ee3541e12b7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831261"
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
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[UpdateInboxRules](updateinboxrules.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

