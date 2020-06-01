---
title: TimeWindow
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeWindow
api_type:
- schema
ms.assetid: 49c79266-353a-4036-a8e2-8a4660d0d8ea
description: Das Window-Element gibt die Zeitspanne an, die für die Informationen zur Benutzerverfügbarkeit abgefragt wird.
ms.openlocfilehash: 5c66614520f9d616687d67ad609b3d55d9cf6571
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458929"
---
# <a name="timewindow"></a>TimeWindow

Das **Window** -Element gibt die Zeitspanne an, die für die Informationen zur Benutzerverfügbarkeit abgefragt wird. 
  
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
|[StartTime](starttime.md) <br/> |Stellt den Beginn einer Zeitspanne dar, die für die Informationen zur Benutzerverfügbarkeit abgefragt wird.  <br/> |
|[EndTime](endtime.md) <br/> |Stellt das Ende einer Zeitspanne dar, die für die Informationen zur Benutzerverfügbarkeit abgefragt wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FreeBusyViewOptions](freebusyviewoptions.md) <br/> |Gibt den Typ der Frei/Gebucht-Informationen an, die in der Antwort zurückgegeben werden.  <br/> Es folgt der XPath für dieses Element:  <br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions` <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der maximale Wert für diesen Zeitraum beträgt 42 Tage. Dieser Maximalwert kann geändert werden. Bei Anforderungen für Benutzer Verfügbarkeitsinformationen, die über den Maximalwert hinausgehen, wird ein Fehler zurückgegeben. Wenn Termine teilweise in der von den Elementen "StartTime" [und "](starttime.md) [EndTime](endtime.md) " definierten Zeitspanne liegen, ist dieser Termin vollständig enthalten. 
  
> [!NOTE]
> Das Schema, das dieses Element beschreibt, befindet sich im/EWS/"aus-Verzeichnis des Computers, auf dem Microsoft® Exchange Server 2007 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserAvailability-Vorgang](getuseravailability-operation.md)


[Verfügbarkeit von Benutzern wird abgerufen](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

