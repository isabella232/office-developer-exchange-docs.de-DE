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
description: Das Interval-Element definiert das Intervall zwischen zwei aufeinander folgenden wiederkehrenden Elementen.
ms.openlocfilehash: 70a41cfc438f057cbe11d792f0004d46d0abcc85
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526564"
---
# <a name="interval"></a>Intervall

Das **Interval** -Element definiert das Intervall zwischen zwei aufeinander folgenden wiederkehrenden Elementen. 
  
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
|[DailyRegeneration](dailyregeneration.md) <br/> |Beschreibt die Häufigkeit in Tagen, in der eine Aufgabe neu generiert wird.  <br/> |
|[DailyRecurrence](dailyrecurrence.md) <br/> |Beschreibt die Häufigkeit in Tagen, in der eine Aufgabe erneut auftritt.  <br/> |
|[MonthlyRegeneration](monthlyregeneration.md) <br/> |Beschreibt die Häufigkeit in Monaten, in der eine Aufgabe neu generiert wird.  <br/> |
|[RelativeMonthlyRecurrence](relativemonthlyrecurrence.md) <br/> |Beschreibt ein relatives monatliches Muster für eine wiederkehrende Aufgabe.  <br/> |
|[WeeklyRecurrence](weeklyrecurrence.md) <br/> |Beschreibt die Häufigkeit in Wochen, in der und in welchen Tagen eine Aufgabe erneut auftritt.  <br/> |
|[WeeklyRegeneration](weeklyregeneration.md) <br/> |Beschreibt die Häufigkeit in Wochen, in der eine Aufgabe neu generiert wird.  <br/> |
|[YearlyRegeneration](yearlyregeneration.md) <br/> |Beschreibt die Häufigkeit in Jahren, in der eine Aufgabe neu generiert wird.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der eine ganze Zahl darstellt, ist erforderlich.
  
## <a name="remarks"></a>Bemerkungen

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

