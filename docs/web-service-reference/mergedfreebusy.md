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
description: Das MergedFreeBusy-Element enthält den zusammengeführten frei/gebucht-Datenstrom.
ms.openlocfilehash: a1483449534f0d886e3c97a23d28c5d78f865042
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468726"
---
# <a name="mergedfreebusy"></a>MergedFreeBusy

Das **MergedFreeBusy** -Element enthält den zusammengeführten frei/gebucht-Datenstrom. 
  
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

Ein Textwert wird vom Server bereitgestellt, wenn der Wert für das [FreeBusyViewType](freebusyviewtype.md) -Element einer der folgenden Werte ist: 
  
- DetailedMerged
    
- FreeBusyMerged
    
- MergedOnly
    
Der Textwert ist ein Stream von Frei/Gebucht-Informationen. 
  
## <a name="remarks"></a>Bemerkungen

Der Datenstrom, der von diesem Element bereitgestellt wird, wird durch die Elemente [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) und [Window](timewindow.md) definiert. Das Time [Window](timewindow.md) -Element definiert die Zeitspanne, die für die Verfügbarkeit abgefragt wird. Das [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) -Element definiert, wie die Zeit aus dem Time [Window](timewindow.md) -Element in Intervalle unterteilt wird, die im **MergedFreeBusy** -Element zurückgegeben werden. Jede Zahl im **MergedFreeBusy** -Datenstrom stellt ein einzelnes Intervall dar, das durch das [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) -Element definiert wird. In der folgenden Tabelle sind die möglichen Werte für ein individuelles Intervall aufgeführt. 
  
|**Ziffer**|**Verfügbarkeit**|
|:-----|:-----|
|0  <br/> |Frei  <br/> |
|1   <br/> |Vorläufige  <br/> |
|2  <br/> |Gebucht  <br/> |
|3  <br/> |Abwesend  <br/> |
|4   <br/> |Keine Daten  <br/> |
   
Beispielsweise enthält eine Anforderung für Frei/Gebucht-Daten ein Zeit [Fenster](timewindow.md) Element, das vier Stunden darstellt, und ein [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) -Element, das 60 Minuten darstellt. Wenn der Kalender des angeforderten Benutzers OOF für die ersten 60 Minuten ist, beschäftigt für die folgenden 90 Minuten und für die letzten 90 Minuten im Zeitfenster ungeplant ist, wird der **MergedFreeBusy** -Datenstrom 3220. Wenn ein Intervall mehr als eine Verfügbarkeits Klassifizierung enthält, wird die höchste Zahl verwendet, um das Intervall zu klassifizieren. 
  
Die von diesem Element bereitgestellte Detailebene hängt von den Berechtigungen ab, die dem Requestor erteilt werden.
  
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

