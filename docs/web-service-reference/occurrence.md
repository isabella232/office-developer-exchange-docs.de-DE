---
title: Vorkommen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Occurrence
api_type:
- schema
ms.assetid: d292b99c-b896-40b7-be5d-2cb314c9481f
description: Das Vorkommen-Element repräsentiert ein geändertes Auftreten eines sich wiederholenden Kalenderelements.
ms.openlocfilehash: 5a40faa9b885a235d30e7f41830d1eefe2ed23c3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830653"
---
# <a name="occurrence"></a>Vorkommen

Das **Vorkommen** -Element repräsentiert ein geändertes Auftreten eines sich wiederholenden Kalenderelements. 
  
```xml
<Occurrence>
   <ItemId/>
   <Start/>
   <End/>
   <OriginalStart/>
</Occurrence>
```

**OccurrenceInfoType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ItemId](itemid.md) <br/> |Enthält den eindeutigen Schlüssel-ID und ein Änderungsprotokoll für ein geänderte Auftreten eines sich wiederholenden Kalenderelements an.  <br/> |
|[Start](start.md) <br/> |Die Anfangszeit der eine geänderte Vorkommen eines sich wiederholenden Kalenderelements darstellt.  <br/> |
|[Ende](end-ex15websvcsotherref.md) <br/> |Die Endzeit der eine geänderte Vorkommen eines sich wiederholenden Kalenderelements darstellt.  <br/> |
|[OriginalStart](originalstart.md) <br/> |Stellt die ursprünglichen Anfangszeit der eine geänderte Vorkommen eines sich wiederholenden Kalenderelements an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ModifiedOccurrences](modifiedoccurrences.md) <br/> |Enthält eine Auflistung von sich wiederholenden Kalender Element vorkommen, die geändert wurden, damit diese als das Master-Shape Recurrence-Element unterschiedlich sind.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

