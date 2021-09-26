---
title: DeleteRuleOperation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DeleteRuleOperation
api_type:
- schema
ms.assetid: c5e251af-f795-43cc-baaf-95d84475677c
description: Das DeleteRuleOperation-Element enthält einen Vorgang zum Löschen einer vorhandenen Posteingangsregel.
ms.openlocfilehash: 089b888f57b5d8048db0dfb0193d7f4c0804e81e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542442"
---
# <a name="deleteruleoperation"></a>DeleteRuleOperation

Das **DeleteRuleOperation-Element** enthält einen Vorgang zum Löschen einer vorhandenen Posteingangsregel. 
  
- [UpdateInboxRules](updateinboxrules.md)
- [Operations](operations.md)
  
```XML
<DeleteRuleOperation>
    <RuleId/>
</DeleteRuleOperation>
```

 **DeleteRuleOperationType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[RuleId](ruleid.md) <br/> |Gibt den Bezeichner der zu löschenden Regel an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Betrieb](operations.md) <br/> |Enthält ein Array der Regelvorgänge, die für ein Postfach ausgeführt werden können.  <br/> |
   
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
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [UpdateInboxRules](updateinboxrules.md) 
- [SetRuleOperation](setruleoperation.md) 
- [CreateRuleOperation](createruleoperation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

