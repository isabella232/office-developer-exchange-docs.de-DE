---
title: Vorkommen (Zeitzonenübergang)
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
description: Das Vorkommen-Element stellt das Vorkommen des Wochentags in dem Monat dar, in dem der Zeitzonenübergang erfolgt.
ms.openlocfilehash: 846f6b22f43bcda07b9408d768d0845a5acfe668
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467977"
---
# <a name="occurrence-time-zone-transition"></a>Vorkommen (Zeitzonenübergang)

Das **vorkommen** -Element stellt das Vorkommen des Wochentags in dem Monat dar, in dem der Zeitzonenübergang erfolgt. 
  
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
|[RecurringDayTransition](recurringdaytransition.md) <br/> |Stellt einen Zeitzonenübergang dar, der an demselben Tag jedes Jahr erfolgt.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert ist eine ganze Zahl, die das Vorkommen des Wochentags in dem Monat darstellt, an dem der Zeitzonenübergang erfolgt. In der folgenden Tabelle sind die möglichen Werte aufgeführt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|1  <br/> |Das erste Vorkommen des angegebenen Wochentags vom Anfang des Monats.  <br/> |
|2  <br/> |Das zweite Vorkommen des angegebenen Wochentags vom Anfang des Monats.  <br/> |
|3  <br/> |Das dritte Vorkommen des angegebenen Wochentags vom Anfang des Monats.  <br/> |
|4   <br/> |Das vierte Vorkommen des angegebenen Wochentags vom Anfang des Monats.  <br/> |
|-1  <br/> |Das erste Vorkommen des angegebenen Wochentags am Ende des Monats.  <br/> |
|-2  <br/> |Das zweite Vorkommen des angegebenen Wochentags am Ende des Monats.  <br/> |
|-3  <br/> |Das dritte Vorkommen des angegebenen Wochentags am Ende des Monats.  <br/> |
|-4  <br/> |Das vierte Vorkommen des angegebenen Wochentags am Ende des Monats.  <br/> |
   
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

