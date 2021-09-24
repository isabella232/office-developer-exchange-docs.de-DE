---
title: An
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- To
api_type:
- schema
ms.assetid: d14e46da-14bd-4a33-a78e-8ee314d9c1d8
description: Das To-Element gibt das Ziel des Zeitzonenübergangs an. Das Ziel ist entweder ein Zeitzonenzeitraum oder eine Gruppe von Zeitzonenübergängen.
ms.openlocfilehash: 64f3f3258fd7c2bad051eabb1b33617bb056ab39
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522551"
---
# <a name="to"></a>An

Das **To-Element** gibt das Ziel des Zeitzonenübergangs an. Das Ziel ist entweder ein Zeitzonenzeitraum oder eine Gruppe von Zeitzonenübergängen. 
  
```xml
<To Kind=""/>
```

 **TransitionTargetType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Art  <br/> |Gibt an, ob das Zeitzonenübergangsziel ein Zeitzonenzeitraum oder eine Gruppe von Zeitzonenübergängen ist.  <br/> |
   
#### <a name="kind-attribute-values"></a>Kind-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Zeitraum  <br/> |Gibt an, dass das Zeitzonenübergangsziel ein Zeitzonenzeitraum ist.  <br/> |
|Gruppe  <br/> |Gibt an, dass das Zeitzonenübergangsziel eine Gruppe von Zeitzonenübergängen ist.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AbsoluteDateTransition](absolutedatetransition.md) <br/> |Stellt einen Zeitzonenübergang dar, der an einem bestimmten Datum und zu einer bestimmten Zeit erfolgt.  <br/> |
|[RecurringDayTransition](recurringdaytransition.md) <br/> |Stellt einen Zeitzonenübergang dar, der jedes Jahr am selben Tag erfolgt.  <br/> |
|[RecurringDateTransition](recurringdatetransition.md) <br/> |Stellt einen Zeitzonenübergang dar, der an einem angegebenen Tag des Jahres stattfindet.  <br/> |
|[Übergang](transition.md) <br/> |Stellt einen Zeitzonenübergang dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert ist eine Zeichenfolge, die den eindeutigen Bezeichner des [Zeitraums](period.md) oder der [TransitionsGroup](transitionsgroup.md) angibt, der das Ziel des Zeitzonenübergangs ist. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

