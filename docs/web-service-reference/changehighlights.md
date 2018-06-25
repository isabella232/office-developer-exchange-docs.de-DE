---
title: ChangeHighlights
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9bd7323-44db-4d2f-aaaa-94c2dfdeead6
description: Die ChangeHighlights-Element gibt Änderungen zwischen zwei Versionen einer Besprechung anfordern Nachricht.
ms.openlocfilehash: 5fe7aa95f60ae95f1af24e8f7a0463ad49716f65
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757559"
---
# <a name="changehighlights"></a>ChangeHighlights

Das Element **ChangeHighlights** gibt Änderungen zwischen zwei Versionen einer Besprechung Request-Nachricht. 
  
```XML
<ChangeHighlights>
    <HasLocationChanged></HasLocationChanged>
    <Location></Location>
    <HasStartTimeChanged></HasStartTimeChanged>
    <Start></Start>
    <HasEndTimeChanged></HasEndTimeChanged>
    <End></End>
</ChangeHighlights>
```

 **ChangeHighlightsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[HasLocationChanged](haslocationchanged.md) <br/> |Gibt an, ob die Location-Eigenschaft einer Besprechung geändert wurde.  <br/> |
|[Ort](location.md) <br/> |Stellt den Speicherort einer Besprechung oder eines Termins.  <br/> |
|[HasStartTimeChanged](hasstarttimechanged.md) <br/> |Gibt an, ob die Startzeit für eine Besprechung geändert wurde.  <br/> |
|[Start](start.md) <br/> |Stellt den Anfang des eine Dauer dar.  <br/> |
|[HasEndTimeChanged](hasendtimechanged.md) <br/> |Gibt an, ob die Endzeit für eine Besprechung geändert wurde.  <br/> |
|[Ende](end-ex15websvcsotherref.md) <br/> |Stellt das Ende einer Dauer dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

