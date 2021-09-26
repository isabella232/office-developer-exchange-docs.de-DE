---
title: Standard
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Standard
api_type:
- schema
ms.assetid: d598f0a6-e296-423f-8ce5-3da57cfd8189
description: Das Standard-Element stellt das Datum und die Uhrzeit dar, zu der sich die Uhrzeit von Sommerzeit zu Standardzeit ändert.
ms.openlocfilehash: 8e44bc458f109975acd3d48c80726654b70373e8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544668"
---
# <a name="standard"></a>Standard

Das **Standard-Element** stellt das Datum und die Uhrzeit dar, zu der sich die Uhrzeit von Sommerzeit zu Standardzeit ändert. 
  
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
|**Timezonename** <br/> |Beschreibt den Namen der Zeitzone.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Offset](offset.md) <br/> |Beschreibt den Offset von [BaseOffset](baseoffset.md). Zusammen mit dem **BaseOffset-Element** gibt das **Offset-Element** an, ob die Zeit Standardzeit oder Sommerzeit ist.  <br/> |
|[RelativeYearlyRecurrence](relativeyearlyrecurrence.md) <br/> |Beschreibt ein relatives jährliches Serienmuster für ein Zeitzonenübergangsdatum.  <br/> |
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

