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
description: Das CalendarEventDetails-Element stellt zusätzliche Informationen zu einem Calendar-Ereignis bereit.
ms.openlocfilehash: 3e1dbba00bce4a1fdc53f3330527764c516890ab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459069"
---
# <a name="calendareventdetails"></a>CalendarEventDetails

Das **CalendarEventDetails** -Element stellt zusätzliche Informationen zu einem Calendar-Ereignis bereit. 
  
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
|[ID](id.md) <br/> |Stellt die Eintrags-ID des Kalenderelements dar.  <br/> |
|[Betreff (CalendarEventDetails)](subject-calendareventdetails.md) <br/> |Stellt den Betreff des Kalenderelements dar.  <br/> |
|[Speicherort (CalendarEventDetails)](location-calendareventdetails.md) <br/> |Stellt das Feld Location des Kalenderelements dar.  <br/> |
|[Ismeeting (CalendarEventDetails)](ismeeting-calendareventdetails.md) <br/> |Gibt an, ob es sich bei dem Kalenderereignis um eine Besprechung oder einen Termin handelt.  <br/> |
|[Iswiederkehr (CalendarEventDetails)](isrecurring-calendareventdetails.md) <br/> |Gibt an, ob das Kalenderereignis eine Instanz eines wiederkehrenden Kalenderelements oder eines einzelnen Kalenderelements ist.  <br/> |
|[Isexception](isexception.md) <br/> |Gibt an, ob eine Instanz eines wiederkehrenden Kalenderelements aus dem Master geändert wird.  <br/> |
|[Reminder](isreminderset.md) <br/> |Gibt an, ob für das Calendar-Ereignis eine Erinnerung festgelegt wurde.  <br/> |
|[IsPrivate](isprivate.md) <br/> |Gibt an, ob das Kalenderelement privat ist.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarEvent](calendarevent.md) <br/> |Stellt ein eindeutiges Kalenderelement vorkommen dar.  <br/> Im folgenden finden Sie den XPath 2,0-Ausdruck für dieses Element:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="remarks"></a>Bemerkungen

Alle untergeordneten Elemente werden in der Reihenfolge aufgeführt, in der Sie auftreten. 
  
Wenn das [IsPrivate](isprivate.md) -Element auf **true**festgelegt ist, werden alle anderen Elemente im [CalendarEventDetails](calendareventdetails.md) -Element nicht in der Antwort zurückgegeben. 
  
Der GetUserAvailability-Vorgang gibt keine detaillierten Anrufer-Informationen zurück, es sei denn, der Aufrufer verfügt über Lesezugriff auf den Kalender des Zielbenutzers. Sie können Zugriffsberechtigungen mithilfe der Exchange-Verwaltungsshell festlegen.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserAvailability-Vorgang](getuseravailability-operation.md)
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)


[Verfügbarkeit von Benutzern wird abgerufen](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

