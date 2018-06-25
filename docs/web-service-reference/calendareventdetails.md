---
title: CalendarEventDetails
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarEventDetails
api_type:
- schema
ms.assetid: 2dca0192-b91b-4154-aa09-84da74e875e9
description: Das Element CalendarEventDetails enthält zusätzliche Informationen zu einem Kalenderereignis.
ms.openlocfilehash: 8df4f3ed4f66c7dcba00e1f0c5b0c383075da0a0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757523"
---
# <a name="calendareventdetails"></a>CalendarEventDetails

Das Element **CalendarEventDetails** enthält zusätzliche Informationen zu einem Kalenderereignis. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[FreeBusyResponseArray](freebusyresponsearray.md)
  
[FreeBusyResponse](freebusyresponse.md)
  
[FreeBusyView](freebusyview.md)
  
[CalendarEventArray](calendareventarray.md)
  
[CalendarEvent](calendarevent.md)
  
[CalendarEventDetails](calendareventdetails.md)
  
```xml
<CalendarEventDetails>
   <ID/>
   <Subject/>
   <Location/>
   <IsMeeting/>
   <IsRecurring/>
   <IsException/>
   <IsReminderSet/>
   <IsPrivate/>
</CalendarEventDetails>
```

 **CalendarEventDetails**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ID](id.md) <br/> |Stellt die Eintrags-ID des Kalenderelements an.  <br/> |
|[Betreff (CalendarEventDetails)](subject-calendareventdetails.md) <br/> |Stellt den Betreff des Kalenderelements an.  <br/> |
|[Speicherort (CalendarEventDetails)](location-calendareventdetails.md) <br/> |Stellt die Position des Kalenderelements.  <br/> |
|[IsMeeting (CalendarEventDetails)](ismeeting-calendareventdetails.md) <br/> |Gibt an, ob das Kalenderereignis gehört zu einer Besprechung oder eines Termins.  <br/> |
|[IsRecurring (CalendarEventDetails)](isrecurring-calendareventdetails.md) <br/> |Gibt an, ob das Kalenderereignis eine Instanz eines sich wiederholenden Kalenderelements oder ein einzelnes Kalenderelement ist.  <br/> |
|[IsException](isexception.md) <br/> |Gibt an, ob eine Instanz eines sich wiederholenden Kalenderelements aus der Master-Shapes geändert wird.  <br/> |
|[IsReminderSet](isreminderset.md) <br/> |Gibt an, ob eine Erinnerung für das Ereignis festgelegt wurde.  <br/> |
|[IsPrivate](isprivate.md) <br/> |Gibt an, ob das Kalenderelement privat ist.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarEvent](calendarevent.md) <br/> |Stellt eine einzelne Kalender Element vorkommen.  <br/> Es folgt der 2.0 XPath-Ausdruck, der dieses Element:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="remarks"></a>Hinweise

All die untergeordneten Elemente sind in der Reihenfolge aufgeführt, in denen sie anfallen. 
  
Wenn das Element [IsPrivate](isprivate.md) auf **true**festgelegt ist, werden alle anderen Elemente im [CalendarEventDetails](calendareventdetails.md) -Element nicht in der Antwort zurückgegeben. 
  
GetUserAvailability-Vorgang gibt keine Anrufer detaillierte Informationen zurück, wenn der Aufrufer Lesezugriff auf Kalender des Zielbenutzers verfügt. Sie können mithilfe der Exchange-Verwaltungsshell Zugriffsberechtigungen festlegen.
  
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

