---
title: DayOfWeek (WorkingPeriod)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DayOfWeek
api_type:
- schema
ms.assetid: 7a8a8cc1-392b-4db5-bb76-710477e31396
description: Das DayOfWeek-Element enthält die Liste der Arbeitstage, die für den Postfachbenutzer geplant sind.
ms.openlocfilehash: 97950d7f2d6db76ac76253979e9187bddc5c99e1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59529006"
---
# <a name="dayofweek-workingperiod"></a>DayOfWeek (WorkingPeriod)

Das **DayOfWeek-Element** enthält die Liste der Arbeitstage, die für den Postfachbenutzer geplant sind. 
  
- [GetUserAvailabilityResponse](getuseravailabilityresponse.md)  
- [FreeBusyResponseArray](freebusyresponsearray.md)  
- [FreeBusyResponse](freebusyresponse.md)  
- [FreeBusyView](freebusyview.md)  
- [WorkingHours](workinghours-ex15websvcsotherref.md)  
- [WorkingPeriodArray](workingperiodarray.md) 
- [WorkingPeriod](workingperiod.md)  
- [DayOfWeek (WorkingPeriod)](dayofweek-workingperiod.md)
  
```xml
<DayOfWeek>Sunday Monday Tuesday Wednesday Thursday Friday Saturday</DayOfWeek>
```

**DaysOfWeek**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[WorkingPeriod](workingperiod.md) <br/> |Enthält die Arbeitswochentage und -stunden des Postfachbenutzers.<br/><br/>Für dieses Element wird folgender XPath-Ausdruck verwendet: <br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/WorkingPeriodArray/WorkingPeriod[i[` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert wird zurückgegeben, wenn für den Postfachbenutzer Tage festgelegt sind, die die Arbeitswoche darstellen. Es folgen die möglichen Werte für dieses Element:
  
- Sonntag    
- Montag    
- Dienstag    
- Mittwoch    
- Donnerstag    
- Freitag    
- Samstag 
    
Die Textwerte werden in dieser Reihenfolge zurückgegeben.
  
## <a name="remarks"></a>HinwBemerkungeneise

Es ist wichtig zu beachten, dass der Unterschied zwischen diesem Element und dem Availability [DayOfWeek (TimeZone)-Element](dayofweek-timezone.md) der Typ ist. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserAvailability-Vorgang](getuseravailability-operation.md)  
- [GetUserAvailabilityResponse](getuseravailabilityresponse.md)
- [Abrufen der Benutzerverfügbarkeit](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

