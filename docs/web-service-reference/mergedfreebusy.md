---
title: MergedFreeBusy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MergedFreeBusy
api_type:
- schema
ms.assetid: ea45590d-476e-4b68-9fe8-ae392feadfea
description: Das MergedFreeBusy-Element enthält den zusammengeführten Frei/Gebucht-Datenstrom.
ms.openlocfilehash: 542b9fae0c36b0236bd806e8a9117753968e812c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830449"
---
# <a name="mergedfreebusy"></a>MergedFreeBusy

Das **MergedFreeBusy** -Element enthält den zusammengeführten Frei/Gebucht-Datenstrom. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[FreeBusyResponseArray](freebusyresponsearray.md)
  
[FreeBusyResponse](freebusyresponse.md)
  
[FreeBusyView](freebusyview.md)
  
[MergedFreeBusy](mergedfreebusy.md)
  
```xml
<MergedFreeBusy>...</MergedFreeBusy>
```

 **string**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FreeBusyView](freebusyview.md) <br/> |Enthält Informationen zur Verfügbarkeit für einen bestimmten Benutzer.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert wird vom Server bereitgestellt werden, wenn der Wert für das [FreeBusyViewType](freebusyviewtype.md) -Element eine der folgenden ist: 
  
- DetailedMerged
    
- FreeBusyMerged
    
- MergedOnly
    
Der Textwert ist ein Stream von Frei/Gebucht-Informationen. 
  
## <a name="remarks"></a>Hinweise

Der Datenstrom bereitgestellt durch dieses Element wird durch die [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) und [Zeitfenster](timewindow.md) Elemente definiert. Das [Zeitfenster](timewindow.md) -Element definiert die Zeitspanne für Verfügbarkeit abgefragt. Das [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) -Element definiert, wie die Zeit aus dem Element [Zeitfenster](timewindow.md) in Intervallen im **MergedFreeBusy** Element zurückgegeben aufgeteilt wird. Jede Nummer im **MergedFreeBusy** Stream-Objekt stellt ein einzelnes Intervall vom [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) -Element definiert. Die folgende Tabelle enthält die möglichen Werte für ein einzelnes Intervall. 
  
|**Ziffer**|**Verfügbarkeit**|
|:-----|:-----|
|0  <br/> |Kostenlos  <br/> |
|1  <br/> |Mit Vorbehalt  <br/> |
|2  <br/> |Gebucht  <br/> |
|3  <br/> |Abwesenheit (Out of Office, OOF)  <br/> |
|4  <br/> |Keine Daten  <br/> |
   
Beispielsweise enthält eine Anforderung für Frei/Gebucht-Daten ein, die vier Stunden darstellt [Zeitfenster](timewindow.md) -Element als auch ein [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) -Element, 60 Minuten darstellt. Wenn den angeforderten Benutzer Kalender OOF für den ersten 60 Minuten ist, für die folgenden 90 Minuten beschäftigt und ungeplante für die letzten 90 Minuten in das Zeitfenster, **MergedFreeBusy** Stream 3220 werden. Wenn ein Intervall für mehrere Verfügbarkeit Klassifizierung enthält, wird die größte Zahl dieses Intervall klassifizieren. 
  
Die von diesem Element bereitgestellte Detailebene, hängt von der Requestor gewährten Berechtigungen.
  
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

