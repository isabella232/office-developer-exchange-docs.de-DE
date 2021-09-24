---
title: Daylight
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Daylight
api_type:
- schema
ms.assetid: ea400839-fba8-4a5e-a5d1-9b677afc0ff9
description: Das Daylight-Element stellt das Datum und die Uhrzeit dar, zu der sich die Zeit von Standardzeit zu Sommerzeit ändert.
ms.openlocfilehash: 750d7cb97d9e2967d3477a93ae833229d20619dc
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517217"
---
# <a name="daylight"></a>Daylight

Das **Daylight-Element** stellt das Datum und die Uhrzeit dar, zu der sich die Zeit von Standardzeit zu Sommerzeit ändert. 
  
```xml
<Daylight TimeZoneName="">
   <Offset/>
   <RelativeYearlyRecurrence/>
   <Time/>
</Daylight>
```

```xml
<Daylight TimeZoneName="">
   <Offset/>
   <AbsoluteDate/>
   <Time/>
</Daylight>
```

**TimeChangeType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Timezonename** <br/> |Beschreibt den Namen der Zeitzone.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Offset](offset.md) <br/> |Beschreibt den Offset von [BaseOffset](baseoffset.md). Der Basisoffset gibt zusätzlich zu diesem Offset die Zeit entsprechend der Standard- oder Sommerzeit an.  <br/> |
|[RelativeYearlyRecurrence](relativeyearlyrecurrence.md) <br/> |Beschreibt ein relatives jährliches Serienmuster für ein Zeitzonenübergangsdatumsmuster.  <br/> |
|[AbsoluteDate](absolutedate.md) <br/> |Stellt das Datum dar, an dem sich die Uhrzeit von der Standardzeit oder Sommerzeit ändert.  <br/> |
|[Zeit (TimeChangeType)](time-timechangetype.md) <br/> |Beschreibt die Zeit, zu der sich die Zeit zwischen Standardzeit und Sommerzeit ändert.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MeetingTimeZone](meetingtimezone.md) <br/> |Stellt die Zeitzone des Orts dar, an dem die Besprechung gehostet wird.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

