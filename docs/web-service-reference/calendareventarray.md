---
title: CalendarEventArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CalendarEventArray
api_type:
- schema
ms.assetid: a00f7f56-d7f1-429d-ae02-97043718c864
description: Das CalendarEventArray-Element enthält eine Reihe eindeutiger Kalenderelementvorkommen, die die Verfügbarkeit des angeforderten Benutzers darstellen.
ms.openlocfilehash: 6faf9d85139ce99a6a60da5a05f171a229843b92
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59526834"
---
# <a name="calendareventarray"></a>CalendarEventArray

Das **CalendarEventArray-Element** enthält eine Reihe eindeutiger Kalenderelementvorkommen, die die Verfügbarkeit des angeforderten Benutzers darstellen. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[FreeBusyResponseArray](freebusyresponsearray.md)
  
[FreeBusyResponse](freebusyresponse.md)
  
[FreeBusyView](freebusyview.md)
  
[CalendarEventArray](calendareventarray.md)
  
```xml
<CalendarEventArray>
   <CalendarEvent>...</CalendarEvent>
</CalendarEventArray>
```

 **ArrayOfCalendarEvent**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarEvent](calendarevent.md) <br/> |Stellt ein eindeutiges Kalenderelement dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FreeBusyView](freebusyview.md) <br/> |Enthält Verfügbarkeitsinformationen für einen bestimmten Benutzer.  <br/> Es folgt der XPath 2.0-Ausdruck für dieses Element:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die Detailebene, die von diesem Element bereitgestellt wird, hängt von den Berechtigungen ab, die dem Anforderer erteilt wurden. Dieses Element ist enthalten, wenn das [FreeBusyViewType](freebusyviewtype.md) -Element auf **FreeBusy**, **FreeBusyMerged**, **Detailed** oder **DetailedMerged** festgelegt ist. Dieses Element enthält keine untergeordneten Elemente, wenn im angeforderten Zeitfenster keine Kalenderelemente vorhanden sind. 
  
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

