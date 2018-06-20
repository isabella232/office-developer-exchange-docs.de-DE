---
title: Intervall
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Interval
api_type:
- schema
ms.assetid: d0c97a5f-96be-40c6-b7d4-abf4c3870adf
description: Das Intervall-Element definiert das Intervall zwischen zwei aufeinander folgenden Terminserien.
ms.openlocfilehash: 55d26b5b1b51aca3effa93a2e6852c1ae57ef4b0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829962"
---
# <a name="interval"></a>Intervall

Das **Intervall** -Element definiert das Intervall zwischen zwei aufeinander folgenden Terminserien. 
  
```xml
<Interval/>
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
|[AbsoluteMonthlyRecurrence](absolutemonthlyrecurrence.md) <br/> |Stellt ein monatliches Serienmuster dar.  <br/> |
|[DailyRegeneration](dailyregeneration.md) <br/> |Beschreibt die Häufigkeit in Tagen, in denen eine Aufgabe neu erstellt wird.  <br/> |
|[DailyRecurrence](dailyrecurrence.md) <br/> |Beschreibt die Häufigkeit in Tagen, in denen eine Aufgabe wiederholt ausgeführt.  <br/> |
|[MonthlyRegeneration](monthlyregeneration.md) <br/> |Beschreibt die Häufigkeit in Monaten, in denen eine Aufgabe neu erstellt wird.  <br/> |
|[RelativeMonthlyRecurrence](relativemonthlyrecurrence.md) <br/> |Beschreibt ein relativen Monatliches Muster für einen sich wiederholenden Vorgang.  <br/> |
|[WeeklyRecurrence](weeklyrecurrence.md) <br/> |Beschreibt die Häufigkeit in Wochen, in dem die Tage, an denen eine Aufgabe wiederholt ausgeführt.  <br/> |
|[WeeklyRegeneration](weeklyregeneration.md) <br/> |Beschreibt die Häufigkeit in Wochen, in denen eine Aufgabe neu erstellt wird.  <br/> |
|[YearlyRegeneration](yearlyregeneration.md) <br/> |Beschreibt die Häufigkeit in Jahre, in denen eine Aufgabe neu erstellt wird.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der eine ganze Zahl darstellt, ist erforderlich.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

