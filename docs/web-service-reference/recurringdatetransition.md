---
title: RecurringDateTransition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecurringDateTransition
api_type:
- schema
ms.assetid: 52fe1e05-3c50-40a1-8752-5c3c64c9f1ed
description: Das RecurringDateTransition-Element stellt einen Zeitzonenübergang dar, der jedes Jahr an einem bestimmten Datum auftritt.
ms.openlocfilehash: 2acbd3afb50a92d4e4f3d7b552eecb36fe59be8b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461576"
---
# <a name="recurringdatetransition"></a>RecurringDateTransition

Das **RecurringDateTransition** -Element stellt einen Zeitzonenübergang dar, der jedes Jahr an einem bestimmten Datum auftritt. 
  
```xml
<RecurringDateTransition>
   <To/>
   <TimeOffset/>
   <Month/>
   <Day/>
</RecurringDateTransition>
```

 **RecurringDateTransitionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[To](to.md) <br/> |Gibt den [Zeitraum](period.md) oder die [Transitions](transitionsgroup.md) an, der das Ziel des Zeit Zonen Übergangs darstellt.  <br/> |
|[Offset](timeoffset.md) <br/> |Stellt den Offset für die Dauer der koordinierten Weltzeit (Coordinated Universal Time, UTC) für den Zeitzonenübergang dar.  <br/> |
|[Month (Zeitzonenübergang)](month-time-zone-transition.md) <br/> |Stellt den Monat dar, in dem der Zeitzonenübergang erfolgt.  <br/> |
|[Day](day.md) <br/> |Stellt den Tag des Monats dar, in dem der Zeitzonenübergang erfolgt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Übergänge](transitions.md) <br/> |Stellt eine Auflistung von Zeit Zonen Übergängen dar.  <br/> |
|[Transitiongroup](transitionsgroup.md) <br/> |Stellt eine Auflistung von Zeit Zonen Übergängen dar.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Ein Beispiel für einen Zeitzonenübergang, der durch das [RecurringDateTransition](recurringdatetransition.md) -Element dargestellt werden kann, ist ein Übergang, der jedes Jahr am 15. März stattfindet. 
  
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

