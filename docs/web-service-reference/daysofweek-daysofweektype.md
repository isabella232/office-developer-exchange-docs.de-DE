---
title: DaysOfWeek (DaysOfWeekType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DaysOfWeek
api_type:
- schema
ms.assetid: c56f997d-28f3-4590-97b0-cb71f016dbe4
description: Das DaysOfWeek-Element beschreibt die Wochentage, die in Artikel Serienmuster verwendet werden.
ms.openlocfilehash: 0b730ff5a7bc9aa6b324fc080022d056c5342296
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757887"
---
# <a name="daysofweek-daysofweektype"></a>DaysOfWeek (DaysOfWeekType)

Das **DaysOfWeek** -Element beschreibt die Wochentage, die in Artikel Serienmuster verwendet werden. 
  
```XML
<DaysOfWeek/>
```

**DaysOfWeekType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[WeeklyRecurrence](weeklyrecurrence.md) <br/> |Beschreibt ein wöchentliches Serienmuster.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Im Folgenden sind die möglichen Werte aufgeführt:
  
- Sonntag    
- Montag    
- Dienstag    
- Mittwoch    
- Donnerstag    
- Freitag    
- Samstag    
- Tag (dieser Wert ist nicht gültig für ein wöchentliches Serienmuster)    
- Weekday (dieser Wert ist nicht gültig für ein wöchentliches Serienmuster)    
- (Dieser Wert ist nicht gültig für ein wöchentliches Serienmuster) WeekendDay
    
Ein wöchentliches Serienmuster kann mehrere Werte enthalten. Werte werden durch ein Leerzeichen voneinander getrennt. Beispielsweise wird der Textwert für eine wöchentliche Serie dienstags und donnerstags, "Dienstag Donnerstag" sein.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

