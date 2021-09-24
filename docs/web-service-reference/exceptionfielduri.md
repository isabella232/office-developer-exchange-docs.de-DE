---
title: ExceptionFieldURI
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ExceptionFieldURI
api_type:
- schema
ms.assetid: 7afda93a-0f8c-4c9e-8e09-f1b0bfc928bf
description: Das ExceptionFieldURI -Element identifiziert bestimmte Fehlern in einer Anforderung. Dieses Element ist nur im Rahmen einer Fehlerantwort im Knoten MessageXml verwendet.
ms.openlocfilehash: 7368fd51e8eca2081b1fd50c86bce9ffa469c6b1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524329"
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
|attachment:ContentType  <br/> |Identifiziert den Inhaltstyp enthält einen Fehler.  <br/> |
|Anlageninhalt:  <br/> |Identifiziert den Inhalt, der einen Fehler enthält.  <br/> |
|Serie Monat:  <br/> |Gibt das Feld Monat enthält einen Fehler.  <br/> |
|recurrence:DayOfWeekIndex  <br/> |Identifiziert den Tag der Wochentagindex enthält einen Fehler.  <br/> |
|recurrence:DaysOfWeek  <br/> |Bezeichnet die DaysOfWeek-Eigenschaft enthält einen Fehler.  <br/> |
|recurrence:DayOfMonth  <br/> |Identifiziert die DayOfMonth enthält einen Fehler.  <br/> |
|Wiederholungsintervall:  <br/> |Gibt das Intervall enthält einen Fehler.  <br/> |
|recurrence:NumberOfOccurrences  <br/> |Feststellen der Anzahl von vorkommen, dass Sie einen Fehler enthält.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MessageXml](messagexml.md) <br/> |Bietet zusätzliche Fehlerantwortinformationen.  <br/> |
   
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

