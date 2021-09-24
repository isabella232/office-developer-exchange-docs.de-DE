---
title: Wert
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Value
api_type:
- schema
ms.assetid: 9a30cadd-909e-41b1-b4e9-291643dd89c6
description: Das Value-Element enthält den Wert einer erweiterten Eigenschaft.
ms.openlocfilehash: dc9d81a17896e730a5140a097574faa7619576d1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513948"
---
# <a name="value"></a>Wert

Das **Value-Element** enthält den Wert einer erweiterten Eigenschaft. 
  
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
|[Werte](values.md) <br/> |Enthält eine Auflistung von Werten für eine erweiterte Eigenschaft.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Erweiterte Eigenschaften für Ordner und Elemente identifiziert.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert muss mit dem Typ kompatibel sein, der durch das PropertyType-Attribut des ExtendedFieldURI angegeben wird.
  
## <a name="remarks"></a>HinwBemerkungeneise

Ein **Value-Element** kann sowohl in einzelnen als auch in mehrwertigen erweiterten Eigenschaftsinstanzen auftreten. Bei einzelwertigen Instanzen ist sie als direktes untergeordnetes Element des [ExtendedProperty-Elements](extendedproperty.md) vorhanden. Bei mehrwertigen Instanzen ist sie als direktes untergeordnetes Element der **Values** -Auflistung vorhanden. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

