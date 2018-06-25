---
title: Wert
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Value
api_type:
- schema
ms.assetid: 9a30cadd-909e-41b1-b4e9-291643dd89c6
description: Das Value-Element enthält den Wert einer erweiterten Eigenschaft.
ms.openlocfilehash: 4b8674d267b78f0384f9457e794e88ace8234826
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839496"
---
# <a name="value"></a>Wert

Das **Value** -Element enthält den Wert einer erweiterten Eigenschaft. 
  
```xml
<Value/>
```

**String**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Values](values.md) <br/> |Enthält eine Auflistung von Werten für eine erweiterte Eigenschaft.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Erweiterte Eigenschaften für Ordner und Elemente identifiziert.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert muss mit dem Typ kompatibel sein, die vom PropertyType-Attribut des der ExtendedFieldURI angegeben wird.
  
## <a name="remarks"></a>Hinweise

**Value** -Element kann in beiden Fällen ein- und mehrwertige erweiterte Eigenschaft auftreten. Für ein einwertiges Instanzen vorhanden ist es als direktes untergeordnetes Element des [ExtendedProperty](extendedproperty.md) -Elements. Für mehrwertige Instanz ist es als ein direktes untergeordnetes Element der Auflistung **Werte** vorhanden. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

