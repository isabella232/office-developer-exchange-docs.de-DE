---
title: IsRecurring (CalendarEventDetails)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsRecurring
api_type:
- schema
ms.assetid: 42323940-0ccb-4a05-86e4-262bde5e41b0
description: IsRecurring-Element gibt an, ob das Kalenderereignis eine Instanz eines sich wiederholenden Kalenderelements oder ein einzelnes Kalenderelement ist.
ms.openlocfilehash: 87a168dc48bdd5ba2ea9398dd84f696e7729db44
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830103"
---
# <a name="isrecurring-calendareventdetails"></a>IsRecurring (CalendarEventDetails)

**IsRecurring** -Element gibt an, ob das Kalenderereignis eine Instanz eines sich wiederholenden Kalenderelements oder ein einzelnes Kalenderelement ist. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[FreeBusyResponseArray](freebusyresponsearray.md)
  
[FreeBusyResponse](freebusyresponse.md)
  
[FreeBusyView](freebusyview.md)
  
[CalendarEventArray](calendareventarray.md)
  
[CalendarEvent](calendarevent.md)
  
[CalendarEventDetails](calendareventdetails.md)
  
[IsRecurring (CalendarEventDetails)](isrecurring-calendareventdetails.md)
  
```xml
<IsRecurring>true or false</IsRecurring>
```

 **boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarEventDetails](calendareventdetails.md) <br/> |Zusätzliche Informationen zu einem Kalenderereignis.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]/CalendarEventDetails` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich, wenn dieses Element in der Antwort zurückgegeben wird. Dieses Element ist erforderlich, wenn das [CalendarEventDetails](calendareventdetails.md) -Element verwendet wird. 
  
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

