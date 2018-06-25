---
title: Vorkommen (Übergang Zeitzone)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Occurrence
api_type:
- schema
ms.assetid: 5c1142b1-c51f-42e1-bbb2-57e00cad0fdb
description: Das Vorkommen-Element darstellt, das Vorkommen des Tags der Woche des Monats, der der Übergang zur Zeitzone auftritt.
ms.openlocfilehash: bc5160480cc6881bb9d724aa61323f5717d1f2fa
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830636"
---
# <a name="occurrence-time-zone-transition"></a>Vorkommen (Übergang Zeitzone)

Das **Vorkommen** -Element darstellt, das Vorkommen des Tags der Woche des Monats, der der Übergang zur Zeitzone auftritt. 
  
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
|[RecurringDayTransition](recurringdaytransition.md) <br/> |Stellt einen Zeitzone Übergang dar, bei dem gleichen Tag pro Jahr auftritt.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert ist eine ganze Zahl, die das Vorkommen des Tags der Woche im Monat darstellt, das auftritt, der Übergang zur Zeitzone. In der folgenden Tabelle sind die möglichen Werte aufgeführt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|1  <br/> |Das erste Auftreten des angegebenen Tags der Woche vom Beginn des Monats.  <br/> |
|2  <br/> |Das zweite Vorkommen des angegebenen Tags der Woche vom Beginn des Monats.  <br/> |
|3  <br/> |Das dritte Vorkommen des angegebenen Tags der Woche vom Beginn des Monats.  <br/> |
|4  <br/> |Das vierte der angegebene Tag der Woche vom Beginn des Monats auftreten.  <br/> |
|-1  <br/> |Das erste Auftreten des angegebenen Tags der Woche vom Ende des Monats.  <br/> |
|-2  <br/> |Das zweite Vorkommen des angegebenen Tags der Woche vom Ende des Monats.  <br/> |
|-3  <br/> |Das dritte Vorkommen des angegebenen Tags der Woche vom Ende des Monats.  <br/> |
|-4  <br/> |Das vierte der angegebene Tag der Woche vom Ende des Monats auftreten.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

