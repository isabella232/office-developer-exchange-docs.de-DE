---
title: DaysOfWeek (DaysOfWeekType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DaysOfWeek
api_type:
- schema
ms.assetid: c56f997d-28f3-4590-97b0-cb71f016dbe4
description: Das DaysOfWeek-Element beschreibt Wochentage, die in Elementserienmustern verwendet werden.
ms.openlocfilehash: 9b0786149f943c47ab77bcb69b74542cbc08edd5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519870"
---
# <a name="daysofweek-daysofweektype"></a>DaysOfWeek (DaysOfWeekType)

Das **DaysOfWeek-Element** beschreibt Wochentage, die in Elementserienmustern verwendet werden. 
  
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
- Tag (dieser Wert gilt nicht für ein wöchentliches Serienmuster)    
- Wochentag (dieser Wert ist nicht gültig für ein wöchentliches Serienmuster)    
- WeekendDay (dieser Wert ist nicht gültig für ein wöchentliches Serienmuster)
    
Ein wöchentliches Serienmuster kann mehrere Werte enthalten. Werte werden durch ein Leerzeichen getrennt. For example, for a weekly recurrence on Tuesdays and Donnerstags, the text value will be "Tuesday Thursday".
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

