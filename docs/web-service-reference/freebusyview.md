---
title: FreeBusyView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeBusyView
api_type:
- schema
ms.assetid: cb18434f-5f41-4e05-a5ce-d921b2721a8c
description: Das FreeBusyView-Element enthält Informationen zur Verfügbarkeit für einen bestimmten Benutzer.
ms.openlocfilehash: d0d603f18642a94e841a1a6bb8e8849aa6b5b273
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758544"
---
# <a name="freebusyview"></a>FreeBusyView

Das **FreeBusyView** -Element enthält Informationen zur Verfügbarkeit für einen bestimmten Benutzer. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[FreeBusyResponseArray](freebusyresponsearray.md)
  
[FreeBusyResponse](freebusyresponse.md)
  
[FreeBusyView](freebusyview.md)
  
```xml
<FreeBusyView>
   <FreeBusyViewType>...</FreeBusyViewType>
   <MergedFreeBusy>...</MergedFreeBusy>
   <CalendarEventArray>...</CalendarEventArray>
   <WorkingHours>...</WorkingHours>
</FreeBusyView>
```

 **FreeBusyView**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FreeBusyViewType](freebusyviewtype.md) <br/> |Stellt den Typ des angeforderten Frei/Gebucht-Informationen in der Antwort zurückgegeben.  <br/> |
|[MergedFreeBusy](mergedfreebusy.md) <br/> |Enthält den zusammengeführten Frei/Gebucht-Datenstrom.  <br/> |
|[CalendarEventArray](calendareventarray.md) <br/> |Enthält einen Satz von eindeutigen Kalender Element vorkommen, die den angeforderten Benutzer Verfügbarkeit darstellen.  <br/> |
|[WorkingHours](workinghours-ex15websvcsotherref.md) <br/> |Stellt die Zeitzone Einstellungen und Arbeitszeiten für den angeforderten Postfachbenutzer.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FreeBusyResponse](freebusyresponse.md) <br/> |Die Frei/Gebucht-Informationen für ein einzelnes Postfachbenutzer enthält.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse` <br/> |
   
## <a name="remarks"></a>Hinweise

All die untergeordneten Elemente sind in der Reihenfolge aufgeführt, in denen sie anfallen. Die von diesem Element bereitgestellte Detailebene, hängt von der Requestor gewährten Berechtigungen.
  
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

