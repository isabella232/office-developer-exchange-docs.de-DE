---
title: MergedFreeBusy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MergedFreeBusy
api_type:
- schema
ms.assetid: ea45590d-476e-4b68-9fe8-ae392feadfea
description: Das MergedFreeBusy-Element enthält den zusammengeführten Frei/Gebucht-Datenstrom.
ms.openlocfilehash: db451d6b2e67313836771604fae57b14b6b3db10
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511030"
---
# <a name="mergedfreebusy"></a>MergedFreeBusy

Das **MergedFreeBusy-Element** enthält den zusammengeführten Frei/Gebucht-Datenstrom. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[FreeBusyResponseArray](freebusyresponsearray.md)
  
[FreeBusyResponse](freebusyresponse.md)
  
[FreeBusyView](freebusyview.md)
  
[MergedFreeBusy](mergedfreebusy.md)
  
```xml
<MergedFreeBusy>...</MergedFreeBusy>
```

 **Zeichenfolge**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FreeBusyView](freebusyview.md) <br/> |Enthält Verfügbarkeitsinformationen für einen bestimmten Benutzer.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert wird vom Server bereitgestellt, wenn der Wert für das [FreeBusyViewType-Element](freebusyviewtype.md) einer der folgenden ist: 
  
- DetailedMerged
    
- FreeBusyMerged
    
- MergedOnly
    
Der Textwert ist ein Stream von Frei/Gebucht-Informationen. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Der von diesem Element bereitgestellte Datenstrom wird durch die Elemente [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) und [TimeWindow](timewindow.md) definiert. Das [TimeWindow-Element](timewindow.md) definiert die Zeitspanne, die auf Verfügbarkeit abgefragt wird. Das [MergedFreeBusyIntervalInMinutes-Element](mergedfreebusyintervalinminutes.md) definiert, wie die Zeit aus dem [TimeWindow-Element](timewindow.md) in Intervalle aufgeteilt wird, die im **MergedFreeBusy-Element** zurückgegeben werden. Jede Zahl im **MergedFreeBusy-Datenstrom** stellt ein einzelnes Intervall dar, das durch das [MergedFreeBusyIntervalInMinutes-Element](mergedfreebusyintervalinminutes.md) definiert wird. In der folgenden Tabelle sind die möglichen Werte für ein einzelnes Intervall aufgeführt. 
  
|**Ziffer**|**Verfügbarkeit**|
|:-----|:-----|
|0  <br/> |Frei  <br/> |
|1  <br/> |Vorläufige  <br/> |
|2  <br/> |Gebucht  <br/> |
|3  <br/> |Abwesend  <br/> |
|4   <br/> |Keine Daten  <br/> |
   
Eine Anforderung für Frei/Gebucht-Daten umfasst beispielsweise ein [TimeWindow-Element,](timewindow.md) das vier Stunden darstellt, und ein [MergedFreeBusyIntervalInMinutes-Element,](mergedfreebusyintervalinminutes.md) das 60 Minuten darstellt. Wenn der Kalender des angeforderten Benutzers OOF für die ersten 60 Minuten ist, für die folgenden 90 Minuten ausgelastet und für die letzten 90 Minuten im Zeitfenster ungeplant ist, ist der **MergedFreeBusy-Datenstrom** 3220. Wenn ein Intervall mehrere Verfügbarkeitsklassifizierungen enthält, wird die höchste Zahl verwendet, um dieses Intervall zu klassifizieren. 
  
Die Detailebene, die von diesem Element bereitgestellt wird, hängt von den Berechtigungen ab, die dem Anforderer erteilt wurden.
  
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

