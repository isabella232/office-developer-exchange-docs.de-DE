---
title: ChangeHighlights
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9bd7323-44db-4d2f-aaaa-94c2dfdeead6
description: Das ChangeHighlights-Element gibt an, was zwischen zwei Versionen einer Besprechungsanfrage Nachricht geändert wurde.
ms.openlocfilehash: 6c78d2c96449ee41032859f90bf51d6e0faa92ae
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463279"
---
# <a name="changehighlights"></a>ChangeHighlights

Das **ChangeHighlights** -Element gibt an, was zwischen zwei Versionen einer Besprechungsanfrage Nachricht geändert wurde. 
  
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
|[Standort](location.md) <br/> |Stellt den Ort einer Besprechung oder eines Termins dar.  <br/> |
|[HasStartTimeChanged](hasstarttimechanged.md) <br/> |Gibt an, ob die Startzeit für eine Besprechung geändert wurde.  <br/> |
|[Start](start.md) <br/> |Stellt den Anfang einer Dauer dar.  <br/> |
|[HasEndTimeChanged](hasendtimechanged.md) <br/> |Gibt an, ob die Endzeit für eine Besprechung geändert wurde.  <br/> |
|[End](end-ex15websvcsotherref.md) <br/> |Stellt das Ende einer Dauer dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types. xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

