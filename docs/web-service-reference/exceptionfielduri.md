---
title: ExceptionFieldURI
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExceptionFieldURI
api_type:
- schema
ms.assetid: 7afda93a-0f8c-4c9e-8e09-f1b0bfc928bf
description: Das ExceptionFieldURI -Element identifiziert bestimmte Fehlern in einer Anforderung. Dieses Element ist nur im Rahmen einer Fehlerantwort im Knoten MessageXml verwendet.
ms.openlocfilehash: a47d44098f85d8bacb1e7a2c48a33e478e56c7ac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44454344"
---
# <a name="exceptionfielduri"></a>ExceptionFieldURI

Das **ExceptionFieldURI** -Element identifiziert bestimmte Fehlern in einer Anforderung. Dieses Element ist nur im Rahmen einer Fehlerantwort im Knoten [MessageXml](messagexml.md) verwendet. 
  
```xml
<ExceptionFieldURI FieldURI="" />
```

 **ExceptionPropertyURIType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**FieldURI** <br/> |Identifiziert eine Eigenschaft für das Vorkommen einer Terminserie. Dieses Attribut ist erforderlich.  <br/> |
   
#### <a name="fielduri-attribute"></a>FieldURI Attribute

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Name der Anlage:  <br/> |Gibt den Anlagennamen enthält einen Fehler.  <br/> |
|Anlage: ContentType  <br/> |Identifiziert den Inhaltstyp enthält einen Fehler.  <br/> |
|Anlageninhalt:  <br/> |Identifiziert den Inhalt, der einen Fehler enthält.  <br/> |
|Serie Monat:  <br/> |Gibt das Feld Monat enthält einen Fehler.  <br/> |
|Serie: DayOfWeekIndex  <br/> |Identifiziert den Tag der Wochentagindex enthält einen Fehler.  <br/> |
|Serie: DaysOfWeek  <br/> |Bezeichnet die DaysOfWeek-Eigenschaft enthält einen Fehler.  <br/> |
|Serie: DAYOFMONTH  <br/> |Identifiziert die DayOfMonth enthält einen Fehler.  <br/> |
|Wiederholungsintervall:  <br/> |Gibt das Intervall enthält einen Fehler.  <br/> |
|Serie: NumberOfOccurrences  <br/> |Feststellen der Anzahl von vorkommen, dass Sie einen Fehler enthält.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Messagexml verwendet](messagexml.md) <br/> |Bietet zusätzliche Fehlerantwortinformationen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

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

