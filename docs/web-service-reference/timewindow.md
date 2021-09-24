---
title: TimeWindow
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- TimeWindow
api_type:
- schema
ms.assetid: 49c79266-353a-4036-a8e2-8a4660d0d8ea
description: Das TimeWindow-Element gibt die Zeitspanne an, die für die Benutzerverfügbarkeitsinformationen abgefragt wird.
ms.openlocfilehash: 93a486a5bc2306cfa61b74de82d795a711dbbceb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531344"
---
# <a name="timewindow"></a>TimeWindow

Das **TimeWindow-Element** gibt die Zeitspanne an, die für die Benutzerverfügbarkeitsinformationen abgefragt wird. 
  
[GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
[FreeBusyViewOptions](freebusyviewoptions.md)
  
[TimeWindow](timewindow.md)
  
```xml
<TimeWindow>
   <StartTime>dateTime</StartTime>
   <EndTime>dateTime</EndTime>
</TimeWindow>
```

 **Duration**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[StartTime](starttime.md) <br/> |Stellt den Anfang einer Zeitspanne dar, die nach den Informationen zur Benutzerverfügbarkeit abgefragt wird.  <br/> |
|[EndTime](endtime.md) <br/> |Stellt das Ende einer Zeitspanne dar, die nach den Informationen zur Benutzerverfügbarkeit abgefragt wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FreeBusyViewOptions](freebusyviewoptions.md) <br/> |Gibt den Typ der Frei/Gebucht-Informationen an, die in der Antwort zurückgegeben werden.  <br/> Es folgt der XPath für dieses Element:  <br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Höchstwert für diesen Zeitraum beträgt 42 Tage. Dieser Maximalwert kann geändert werden. Alle Anforderungen für Benutzerverfügbarkeitsinformationen, die über den Maximalwert hinausgehen, geben einen Fehler zurück. Wenn Termine teilweise in der durch die [Elemente StartTime](starttime.md) und [EndTime](endtime.md) definierten Zeitspanne liegen, ist dieser Termin vollständig enthalten. 
  
> [!NOTE]
> Das Schema, das dieses Element beschreibt, befindet sich im Verzeichnis /EWS/ des Computers, auf dem Microsoft ausgeführt wird® Exchange Server 2007, auf dem die Clientzugriffsserverrolle installiert ist. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserAvailability-Vorgang](getuseravailability-operation.md)


[Abrufen der Benutzerverfügbarkeit](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

