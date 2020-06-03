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
description: Das Vorkommen-Element stellt ein einzelnes geändertes Vorkommen eines wiederkehrenden Kalenderelements dar.
ms.openlocfilehash: c3a6bcce23f0bb1125dbd2a5bb86e9b20039a4e1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466318"
---
# <a name="occurrence"></a>Vorkommen

Das **vorkommen** -Element stellt ein einzelnes geändertes Vorkommen eines wiederkehrenden Kalenderelements dar. 
  
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
|[ItemId](itemid.md) <br/> |Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines geänderten Vorkommens eines wiederkehrenden Kalenderelements.  <br/> |
|[Start](start.md) <br/> |Stellt die Startzeit eines geänderten Vorkommens eines wiederkehrenden Kalenderelements dar.  <br/> |
|[End](end-ex15websvcsotherref.md) <br/> |Stellt die Endzeit eines geänderten Vorkommens eines wiederkehrenden Kalenderelements dar.  <br/> |
|[OriginalStart](originalstart.md) <br/> |Stellt die ursprüngliche Startzeit eines geänderten Vorkommens eines wiederkehrenden Kalenderelements dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ModifiedOccurrences](modifiedoccurrences.md) <br/> |Enthält eine Auflistung von wiederkehrenden Kalenderelement vorkommen, die geändert wurden, sodass Sie sich vom Serienmasterelement unterscheiden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

