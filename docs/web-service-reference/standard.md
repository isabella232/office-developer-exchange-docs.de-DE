---
title: Standard
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Standard
api_type:
- schema
ms.assetid: d598f0a6-e296-423f-8ce5-3da57cfd8189
description: Das Standard-Element darstellt, Datum und Uhrzeit, wann die Zeit von Sommerzeit zu Normalzeit wechselt.
ms.openlocfilehash: c121e959f243d982cfe50ed6b4ef39a82dae2cc8
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353434"
---
# <a name="standard"></a>Standard

Das **Standard** -Element darstellt, Datum und Uhrzeit, wann die Zeit von Sommerzeit zu Normalzeit wechselt. 
  
```xml
<Standard TimeZoneName="">
   <Offset/>
   <RelativeYearlyRecurrence/>
   <Time/>
</Standard>
```

```xml
<Standard TimeZoneName="">
   <Offset/>
   <AbsoluteDate/>
   <Time/>
</Standard>
```

**TimeChangeType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**TimeZoneName** <br/> |Beschreibt den Namen der Zeitzone.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Offset](offset.md) <br/> |Beschreibt die [BaseOffset](baseoffset.md)-Offset. Zusammen mit dem **BaseOffset** -Element identifiziert das **Offset** -Element an, ob die Zeit Standardzeit oder Sommerzeit.  <br/> |
|[RelativeYearlyRecurrence](relativeyearlyrecurrence.md) <br/> |Ein relative jährliches Serienmuster beschrieben für eine Zeitzone Übergangsdatum.  <br/> |
|[AbsoluteDate](absolutedate.md) <br/> |Stellt dar, wenn die Zeit von Standardzeit oder Sommerzeit geändert wird.  <br/> |
|[Zeit (TimeChangeType)](time-timechangetype.md) <br/> |Beschreibt, wenn die Zeit zwischen Standardzeit und Sommerzeit geändert wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MeetingTimeZone](meetingtimezone.md) <br/> |Stellt die Zeitzone des Speicherorts, in die Besprechung gehostet wird.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

