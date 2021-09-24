---
title: CalendarEventDetails
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CalendarEventDetails
api_type:
- schema
ms.assetid: 2dca0192-b91b-4154-aa09-84da74e875e9
description: Das CalendarEventDetails-Element stellt zusätzliche Informationen zu einem Kalenderereignis bereit.
ms.openlocfilehash: c332d17b1bb630b9635e64c484b4c5fd989f9845
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516090"
---
# <a name="calendareventdetails"></a>CalendarEventDetails

Das **CalendarEventDetails-Element** stellt zusätzliche Informationen zu einem Kalenderereignis bereit. 
  
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
|[Location (CalendarEventDetails)](location-calendareventdetails.md) <br/> |Represents the location field of the calendar item.  <br/> |
|[IsMeeting (CalendarEventDetails)](ismeeting-calendareventdetails.md) <br/> |Gibt an, ob das Kalenderereignis eine Besprechung oder ein Termin ist.  <br/> |
|[IsRecurring (CalendarEventDetails)](isrecurring-calendareventdetails.md) <br/> |Gibt an, ob es sich bei dem Kalenderereignis um eine Instanz eines wiederkehrenden Kalenderelements oder eines einzelnen Kalenderelements handelt.  <br/> |
|[IsException](isexception.md) <br/> |Gibt an, ob eine Instanz eines Terminserien-Kalenderelements vom Master geändert wird.  <br/> |
|[IsReminderSet](isreminderset.md) <br/> |Gibt an, ob eine Erinnerung für das Kalenderereignis festgelegt wurde.  <br/> |
|[IsPrivate](isprivate.md) <br/> |Gibt an, ob das Kalenderelement privat ist.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarEvent](calendarevent.md) <br/> |Stellt ein eindeutiges Kalenderelement dar.  <br/> Es folgt der XPath 2.0-Ausdruck für dieses Element:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Alle untergeordneten Elemente werden in der Reihenfolge aufgelistet, in der sie auftreten. 
  
Wenn das [IsPrivate-Element](isprivate.md) **"true"** ist, werden alle anderen Elemente im [CalendarEventDetails-Element](calendareventdetails.md) nicht in der Antwort zurückgegeben. 
  
Der GetUserAvailability-Vorgang gibt keine detaillierten Aufruferinformationen zurück, es sei denn, der Aufrufer hat Lesezugriff auf den Kalender des Zielbenutzers. Sie können Zugriffsberechtigungen mithilfe der Exchange-Verwaltungsshell festlegen.
  
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


[Abrufen der Benutzerverfügbarkeit](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

