---
title: DayOfWeekIndex
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DayOfWeekIndex
api_type:
- schema
ms.assetid: 82420338-a1f7-4887-b338-b2d93b2c2bf1
description: Das DayOfWeekIndex-Element beschreibt die Woche im Monat in ein relative Serienmuster verwendet wird.
ms.openlocfilehash: 4987685d0c3cefdfad4f5be1368776a5b859bf94
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757883"
---
# <a name="dayofweekindex"></a>DayOfWeekIndex

Das **DayOfWeekIndex** -Element beschreibt die Woche im Monat in ein relative Serienmuster verwendet wird. 
  
```xml
<DayOfWeekIndex/>
```

**DayOfWeekIndexType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[RelativeYearlyRecurrence](relativeyearlyrecurrence.md) <br/> |Wird ein relativer jährliches Serienmuster beschrieben.  <br/> |
|[RelativeMonthlyRecurrence](relativemonthlyrecurrence.md) <br/> |Beschreibt ein monatliches Serienmuster relative.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Im Folgenden sind die möglichen Werte aufgeführt:
  
- Erster    
- Zweiter    
- Dritter    
- Vier    
- Letzter
    
## <a name="remarks"></a>Hinweise

Beispielsweise kann der zweite Montag im Monat in der dritten Woche des Monats auftreten. Ein Monat an einem Freitag beginnt, wird die erste Woche des Monats nur wenige Tagen enthält und enthält keine Montag. Aus diesem Grund müssten der erste Montag in der zweiten Woche auftreten.
  
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

