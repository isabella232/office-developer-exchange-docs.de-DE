---
title: AbsoluteMonthlyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AbsoluteMonthlyRecurrence
api_type:
- schema
ms.assetid: 178fa0ae-9dfc-417f-933c-d657d31c2161
description: Das AbsoluteMonthlyRecurrence-Element stellt ein monatliches Serienmuster dar.
ms.openlocfilehash: 7fcc1811a7c42fc653344fb3c052adac820d6a5d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546917"
---
# <a name="absolutemonthlyrecurrence"></a>AbsoluteMonthlyRecurrence

Das **AbsoluteMonthlyRecurrence-Element** stellt ein monatliches Serienmuster dar. 
  
```xml
<AbsoluteMonthlyRecurrence>
   <Interval/>
   <DayOfMonth/>
</AbsoluteMonthlyRecurrence>
```

 **AbsoluteMonthlyRecurrencePatternType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DayOfMonth](dayofmonth.md) <br/> |Beschreibt den Tag in einem Monat, an dem ein wiederkehrendes Element auftritt. Der Wertebereich für diese Eigenschaft ist 1 bis 31. Wenn dieser Wert für einen bestimmten Monat größer als die Anzahl der Tage im Monat ist, wird der letzte Tag des Monats für diese Eigenschaft angenommen.  <br/> |
|[Intervall](interval.md) <br/> |Definiert das Intervall zwischen zwei aufeinander folgenden wiederkehrenden Elementen. Wenn das **Interval-Element** beispielsweise den Wert 5 aufweist, tritt die Terminserie alle 5 Monate auf. Der Bereich gültiger Werte liegt zwischen 1 und 99.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Serie (TaskRecurrenceType)](recurrence-taskrecurrencetype.md) <br/> |Enthält Serieninformationen für wiederkehrende Vorgänge.  <br/> |
|[Serie (RecurrenceType)](recurrence-recurrencetype.md) <br/> |Enthält das Serienmuster für Kalenderelemente und Besprechungsanfragen.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

