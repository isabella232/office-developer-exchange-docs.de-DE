---
title: Vorkommen (Zeitzonenübergang)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Occurrence
api_type:
- schema
ms.assetid: 5c1142b1-c51f-42e1-bbb2-57e00cad0fdb
description: Das Occurrence-Element stellt das Vorkommen des Wochentags in dem Monat dar, in dem der Zeitzonenübergang erfolgt.
ms.openlocfilehash: 9790b0e9541da0c22f2eac59850b8a361645c7b4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539277"
---
# <a name="occurrence-time-zone-transition"></a>Vorkommen (Zeitzonenübergang)

Das  Occurrence-Element stellt das Vorkommen des Wochentags in dem Monat dar, in dem der Zeitzonenübergang erfolgt. 
  
```xml
<Occurrence/>
```

**int**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[RecurringDayTransition](recurringdaytransition.md) <br/> |Stellt einen Zeitzonenübergang dar, der jedes Jahr am selben Tag erfolgt.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert ist eine ganze Zahl, die das Auftreten des Wochentags in dem Monat darstellt, in dem der Zeitzonenübergang erfolgt. In der folgenden Tabelle sind die möglichen Werte aufgeführt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|1  <br/> |Das erste Vorkommen des angegebenen Wochentags ab dem Anfang des Monats.  <br/> |
|2  <br/> |Das zweite Vorkommen des angegebenen Wochentags ab dem Anfang des Monats.  <br/> |
|3  <br/> |Das dritte Vorkommen des angegebenen Wochentags ab dem Anfang des Monats.  <br/> |
|4   <br/> |Das vierte Vorkommen des angegebenen Wochentags ab dem Anfang des Monats.  <br/> |
|-1  <br/> |Das erste Vorkommen des angegebenen Wochentags am Monatsende.  <br/> |
|-2  <br/> |Das zweite Vorkommen des angegebenen Wochentags vom Monatsende.  <br/> |
|-3  <br/> |Das dritte Vorkommen des angegebenen Wochentags am Monatsende.  <br/> |
|-4  <br/> |Das vierte Vorkommen des angegebenen Wochentags am Monatsende.  <br/> |
   
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

