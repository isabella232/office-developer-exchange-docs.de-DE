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
description: Rule-Element enthält eine einzige Regel und eine Regel im Postfach des Benutzers darstellt.
ms.openlocfilehash: b1f9f058213543633335db11f03729964baf98ad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831259"
---
# <a name="rule-ruletype"></a>Regel (RuleType)

**Rule** -Element enthält eine einzige Regel und eine Regel im Postfach des Benutzers darstellt. 
  
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
|[Regel-ID](ruleid.md) <br/> |Gibt die Kennung für die Regel an.  <br/> |
|[DisplayName (Zeichenfolge)](displayname-string.md) <br/> |Enthält den Anzeigenamen einer Regel an.  <br/> |
|[Priority](priority.md) <br/> |Gibt die Reihenfolge, in der ist eine Regel ausgeführt werden soll.  <br/> |
|[IsEnabled](isenabled.md) <br/> |Gibt an, ob die Regel aktiviert ist.  <br/> |
|[IsNotSupported](isnotsupported.md) <br/> |Gibt an, ob die Regel mit dem verwalteten Code-APIs nicht geändert werden kann.  <br/> |
|[IsInError](isinerror.md) <br/> |Gibt an, ob sich die Regel in einem Fehlerzustand befindet.  <br/> |
|[Bedingungen](conditions.md) <br/> |Identifiziert die Bedingungen, die beim erfüllt, Regelaktionen für eine Regel ausgelöst wird.  <br/> |
|[Ausnahmen](exceptions.md) <br/> |Identifiziert die Ausnahmen, die alle verfügbaren Regel Ausnahmebedingungen für die Posteingangsregel an darstellen.  <br/> |
|[Aktionen](actions.md) <br/> |Stellt die Aktionen, die auf eine Nachricht durchgeführt werden, wenn die Bedingungen erfüllt sind.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CreateRuleOperation](createruleoperation.md) <br/> |Stellt einen Vorgang zum Erstellen einer neuen Regel dar.  <br/> |
|[InboxRules](inboxrules.md) <br/> |Stellt ein Array von Regeln in das Postfach des Benutzers an.  <br/> |
|[SetRuleOperation](setruleoperation.md) <br/> |Stellt einen Vorgang zum Aktualisieren einer vorhandenen Regel dar.  <br/> |
   
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



[UpdateInboxRules](updateinboxrules.md)
  
[SetRuleOperation](setruleoperation.md)
  
[CreateRuleOperation](createruleoperation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

