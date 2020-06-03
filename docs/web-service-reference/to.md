---
title: An
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- To
api_type:
- schema
ms.assetid: d14e46da-14bd-4a33-a78e-8ee314d9c1d8
description: Das to-Element gibt das Ziel des Zeit Zonen Übergangs an. Das Ziel ist entweder eine Zeit Zonen Periode oder eine Gruppe von Zeit Zonen Übergängen.
ms.openlocfilehash: 8cce700eedd64035f2e21be4db6b517f3f85d98d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/02/2020
ms.locfileid: "44468796"
---
# <a name="to"></a>An

Das **to** -Element gibt das Ziel des Zeit Zonen Übergangs an. Das Ziel ist entweder eine Zeit Zonen Periode oder eine Gruppe von Zeit Zonen Übergängen. 
  
```xml
<To Kind=""/>
```

 **TransitionTargetType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Art  <br/> |Gibt an, ob das Zeit Zonen Übergangs Ziel eine Zeit Zonen Periode oder eine Gruppe von Zeit Zonen Übergängen ist.  <br/> |
   
#### <a name="kind-attribute-values"></a>Kind-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Punkt  <br/> |Gibt an, dass das Zeit Zonen Übergangs Ziel eine Zeit Zonen Periode ist.  <br/> |
|Gruppe  <br/> |Gibt an, dass das Zeit Zonen Übergangs Ziel eine Gruppe von Zeit Zonen Übergängen ist.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AbsoluteDateTransition](absolutedatetransition.md) <br/> |Stellt einen Zeitzonenübergang dar, der zu einem bestimmten Datum und zu einem bestimmten Zeitpunkt erfolgt.  <br/> |
|[RecurringDayTransition](recurringdaytransition.md) <br/> |Stellt einen Zeitzonenübergang dar, der an demselben Tag jedes Jahr erfolgt.  <br/> |
|[RecurringDateTransition](recurringdatetransition.md) <br/> |Stellt einen Zeitzonenübergang dar, der an einem angegebenen Tag des Jahres erfolgt.  <br/> |
|[Übergang](transition.md) <br/> |Stellt einen Zeitzonenübergang dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert ist eine Zeichenfolge, die den eindeutigen Bezeichner des [Zeitraums](period.md) oder der [Transitions](transitionsgroup.md) angibt, der das Ziel des Zeit Zonen Übergangs darstellt. 
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

