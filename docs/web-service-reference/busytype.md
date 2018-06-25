---
title: BusyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BusyType
api_type:
- schema
ms.assetid: 26d4fae0-8c78-4705-b5e8-d6033712c41e
description: Das BusyType-Element darstellt, den Frei/Gebucht-Status für ein Ereignis im Kalender festgelegt.
ms.openlocfilehash: 6484bc70c6a05084e5d2bc1738b575fbebe4c132
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757519"
---
# <a name="busytype"></a>BusyType

Das **BusyType** -Element darstellt, den Frei/Gebucht-Status für ein Ereignis im Kalender festgelegt. 
  
```xml
<BusyType>Free or Tentative or Busy or OOF or NoData</BusyType>
```

 **BusyType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[IndividualAttendeeConflictData](individualattendeeconflictdata.md) <br/> |Enthält eines Benutzers oder Kontakts Frei/Gebucht-Status für ein Zeitfenster, das zur selben Zeit als die Uhrzeit der vorgeschlagenen Besprechung auftritt.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/IndividualAttendeeConflictData` <br/> |
|[CalendarEvent](calendarevent.md) <br/> |Stellt eine einzelne Kalender Element vorkommen.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a>Textwert

Es wird ein Textwert für dieses Element erforderlich. Der Wert ist eine Zeichenfolge. Es folgen die möglichen Werte für das [BusyType](busytype.md) -Element: 
  
- Kostenlos
    
- Mit Vorbehalt
    
- Gebucht
    
- ABWESEND
    
- NoData
    
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserAvailability-Vorgang](getuseravailability-operation.md)
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)


[Erste Benutzer Verfügbarkeit](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

