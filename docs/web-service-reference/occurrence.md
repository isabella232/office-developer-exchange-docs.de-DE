---
title: Vorkommen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Occurrence
api_type:
- schema
ms.assetid: d292b99c-b896-40b7-be5d-2cb314c9481f
description: Das Occurrence-Element stellt ein einzelnes geändertes Vorkommen eines Terminserienkalenderelements dar.
ms.openlocfilehash: 465c02263eadfc74629a8e21ebccf076206ec0d2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518092"
---
# <a name="occurrence"></a>Vorkommen

Das **Occurrence-Element** stellt ein einzelnes geändertes Vorkommen eines Terminserienkalenderelements dar. 
  
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
|[ItemId](itemid.md) <br/> |Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines geänderten Vorkommens eines Wiederkehrenden Kalenderelements.  <br/> |
|[Start](start.md) <br/> |Stellt die Startzeit eines geänderten Vorkommens eines Wiederkehrenden Kalenderelements dar.  <br/> |
|[Ende ](end-ex15websvcsotherref.md) <br/> |Stellt die Endzeit eines geänderten Vorkommens eines Wiederkehrenden Kalenderelements dar.  <br/> |
|[OriginalStart](originalstart.md) <br/> |Stellt die ursprüngliche Startzeit eines geänderten Vorkommens eines Wiederkehrenden Kalenderelements dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ModifiedOccurrences](modifiedoccurrences.md) <br/> |Enthält eine Auflistung wiederkehrender Kalenderelementvorkommen, die geändert wurden, sodass sie sich vom Serienmasterelement unterscheiden.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

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

