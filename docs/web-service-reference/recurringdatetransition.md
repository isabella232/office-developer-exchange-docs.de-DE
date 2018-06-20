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
description: Das RecurringDateTransition-Element darstellt, den Übergang einer Zeitzone, der einem bestimmten Datum pro Jahr tritt auf.
ms.openlocfilehash: 7cd8f3452a744e0c9a98fd3698dffb9ed8721a6c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831014"
---
# <a name="recurringdatetransition"></a>RecurringDateTransition

Das **RecurringDateTransition** -Element darstellt, den Übergang einer Zeitzone, der einem bestimmten Datum pro Jahr tritt auf. 
  
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
|[To](to.md) <br/> |Gibt den [Zeitraum](period.md) oder [TransitionsGroup](transitionsgroup.md) , das das Ziel des Übergangs Zeitzone ist.  <br/> |
|[TimeOffset](timeoffset.md) <br/> |Stellt den Offset für die Dauer von koordinierte Weltzeit (UTC) für den Übergang zur Zeitzone dar.  <br/> |
|[Monat (Übergang Zeitzone)](month-time-zone-transition.md) <br/> |Stellt den Monat, in dem der Übergang zur Zeitzone auftritt.  <br/> |
|[Tag](day.md) <br/> |Stellt den Tag des Monats auf der erfolgt der Übergang zur Zeitzone.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Übergänge](transitions.md) <br/> |Stellt eine Auflistung der Zeitzone Übergänge.  <br/> |
|[TransitionsGroup](transitionsgroup.md) <br/> |Stellt eine Auflistung der Zeitzone Übergänge.  <br/> |
   
## <a name="remarks"></a>Hinweise

Ein Beispiel für einen Übergang Zeitzone, der durch das [RecurringDateTransition](recurringdatetransition.md) -Element dargestellt werden könnte ist ein Übergang, der 15. März jährlich auftritt. 
  
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

