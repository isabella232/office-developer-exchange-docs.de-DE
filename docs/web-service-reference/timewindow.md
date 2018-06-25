---
title: Zeitfenster
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
description: Das Zeitfenster-Element gibt die Zeitspanne für die Verfügbarkeit Benutzerinformationen abgefragt.
ms.openlocfilehash: 05858b4d62b72b3ff9904c90652bb1bff78ceb41
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839213"
---
# <a name="timewindow"></a>Zeitfenster

Das **Zeitfenster** -Element gibt die Zeitspanne für die Verfügbarkeit Benutzerinformationen abgefragt. 
  
[GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
[FreeBusyViewOptions](freebusyviewoptions.md)
  
[Zeitfenster](timewindow.md)
  
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
|[StartTime](starttime.md) <br/> |Stellt den Anfang des einer bestimmten Zeitspanne für die Verfügbarkeit Benutzerinformationen abgefragt.  <br/> |
|[EndTime](endtime.md) <br/> |Stellt das Ende einer bestimmten Zeitspanne für die Verfügbarkeit Benutzerinformationen abgefragt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FreeBusyViewOptions](freebusyviewoptions.md) <br/> |Gibt den Typ des Frei/Gebucht-Informationen in der Antwort zurückgegeben.  <br/> Es folgt der XPath-Ausdruck für dieses Element:  <br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions` <br/> |
   
## <a name="remarks"></a>Hinweise

Der Höchstwert für diesen Zeitraum ist 42 Tage. Dieser Höchstwert kann geändert werden. Alle Anforderungen für Verfügbarkeitsinformationen für Benutzer außerhalb der Höchstwert gibt einen Fehler zurück. Wenn keine Termine teilweise in die Zeitspanne, die durch die [Werte von StartTime](starttime.md) und [EndTime](endtime.md) Elemente definiert sind, ist in seiner Gesamtheit eines Termins enthalten. 
  
> [!NOTE]
> Das Schema, das dieses Element beschreibt befindet sich im Verzeichnis /EWS/ des Computers, auf dem Microsoft® Exchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserAvailability-Vorgang](getuseravailability-operation.md)


[Erste Benutzer Verfügbarkeit](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

