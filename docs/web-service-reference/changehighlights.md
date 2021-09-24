---
title: ChangeHighlights
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f9bd7323-44db-4d2f-aaaa-94c2dfdeead6
description: Das ChangeHighlights-Element gibt an, was sich zwischen zwei Versionen einer Besprechungsanfrage geändert hat.
ms.openlocfilehash: 95f665f30c62d723cd97eaa2bd3eb3b2ed479967
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512212"
---
# <a name="changehighlights"></a>ChangeHighlights

Das **ChangeHighlights-Element** gibt an, was sich zwischen zwei Versionen einer Besprechungsanfrage geändert hat. 
  
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
|[HasLocationChanged](haslocationchanged.md) <br/> |Gibt an, ob sich die Standorteigenschaft einer Besprechung geändert hat.  <br/> |
|[Ort](location.md) <br/> |Stellt den Ort einer Besprechung oder eines Termins dar.  <br/> |
|[HasStartTimeChanged](hasstarttimechanged.md) <br/> |Gibt an, ob sich die Startzeit für eine Besprechung geändert hat.  <br/> |
|[Start](start.md) <br/> |Stellt den Anfang einer Dauer dar.  <br/> |
|[HasEndTimeChanged](hasendtimechanged.md) <br/> |Gibt an, ob sich die Endzeit für eine Besprechung geändert hat.  <br/> |
|[Ende ](end-ex15websvcsotherref.md) <br/> |Stellt das Ende einer Dauer dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

