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
ms.openlocfilehash: 79909405179cec0d0b86ad12bf52031e1daeb790
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758292"
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
   
#### <a name="fielduri-attribute"></a>FieldURI-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Name der Anlage:  <br/> |Gibt den Anlagennamen enthält einen Fehler.  <br/> |
|Anhang: ContentType  <br/> |Identifiziert den Inhaltstyp enthält einen Fehler.  <br/> |
|Anlageninhalt:  <br/> |Identifiziert den Inhalt, der einen Fehler enthält.  <br/> |
|Serie Monat:  <br/> |Gibt das Feld Monat enthält einen Fehler.  <br/> |
|Serie: DayOfWeekIndex  <br/> |Identifiziert den Tag der Wochentagindex enthält einen Fehler.  <br/> |
|Serie: DaysOfWeek  <br/> |Bezeichnet die DaysOfWeek-Eigenschaft enthält einen Fehler.  <br/> |
|Serie: DayOfMonth  <br/> |Identifiziert die DayOfMonth enthält einen Fehler.  <br/> |
|Wiederholungsintervall:  <br/> |Gibt das Intervall enthält einen Fehler.  <br/> |
|Serie: NumberOfOccurrences  <br/> |Feststellen der Anzahl von vorkommen, dass Sie einen Fehler enthält.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MessageXml](messagexml.md) <br/> |Bietet zusätzliche Fehlerantwortinformationen.  <br/> |
   
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

