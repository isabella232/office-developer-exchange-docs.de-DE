---
title: Regel (RuleType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Rule
api_type:
- schema
ms.assetid: 259a1f62-b235-4964-88bf-2d1f1c05a563
description: Das Rule-Element enthält eine einzelne Regel und stellt eine Regel im Postfach eines Benutzers dar.
ms.openlocfilehash: cdbd21df235a62a9e201e1eaae1d82a8ac10cdd2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "44465079"
---
# <a name="rule-ruletype"></a>Regel (RuleType)

Das **rule** -Element enthält eine einzelne Regel und stellt eine Regel im Postfach eines Benutzers dar. 
  
```XML
<Rule>
    <RuleId>
    <DisplayName>
    <Priority>
    <IsEnabled>
    <IsNotSupported>
    <IsInError>
    <Conditions>
    <Exceptions>
    <Actions>
</Rule>
```

 **RuleType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[RuleId](ruleid.md) <br/> |Gibt die Regel-ID an.  <br/> |
|[DisplayName (Zeichenfolge)](displayname-string.md) <br/> |Enthält den Anzeigenamen einer Regel.  <br/> |
|[Priority](priority.md) <br/> |Gibt die Reihenfolge an, in der eine Regel ausgeführt werden soll.  <br/> |
|[IsEnabled](isenabled.md) <br/> |Gibt an, ob die Regel aktiviert ist.  <br/> |
|[IsNotSupported](isnotsupported.md) <br/> |Gibt an, ob die Regel mit den APIs für verwalteten Code nicht geändert werden kann.  <br/> |
|[IsInError](isinerror.md) <br/> |Gibt an, ob sich die Regel in einem Fehlerzustand befindet.  <br/> |
|[Bedingungen:](conditions.md) <br/> |Gibt die Bedingungen an, die bei der Erfüllung der Regelaktionen für eine Regel ausgelöst werden.  <br/> |
|[Ausnahmen](exceptions.md) <br/> |Identifiziert die Ausnahmen, die alle verfügbaren Regel Ausnahmebedingungen für die Posteingangsregel darstellen.  <br/> |
|[Aktionen](actions.md) <br/> |Stellt die Aktionen dar, die für eine Nachricht ausgeführt werden sollen, wenn die Bedingungen erfüllt sind.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CreateRuleOperation](createruleoperation.md) <br/> |Stellt einen Vorgang zum Erstellen einer neuen Regel dar.  <br/> |
|[InboxRules](inboxrules.md) <br/> |Stellt ein Array von Regeln im Postfach des Benutzers dar.  <br/> |
|[SetRuleOperation](setruleoperation.md) <br/> |Stellt einen Vorgang zum Aktualisieren einer vorhandenen Regel dar.  <br/> |
   
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



[UpdateInboxRules](updateinboxrules.md)
  
[SetRuleOperation](setruleoperation.md)
  
[CreateRuleOperation](createruleoperation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

