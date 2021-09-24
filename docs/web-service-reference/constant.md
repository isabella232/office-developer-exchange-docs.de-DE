---
title: Konstante
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Constant
api_type:
- schema
ms.assetid: 340af0cd-9f12-44ab-b8f1-21d107c8d0c9
description: Das Constant-Element identifiziert einen Konstantenwert in einer Einschränkung.
ms.openlocfilehash: 9d727b41d7d18537758eae7f144832b041757d4b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511979"
---
# <a name="constant"></a>Konstante

Das **Constant-Element** identifiziert einen Konstantenwert in einer Einschränkung. 
  
```xml
<Constant Value="" />
```

 **ConstantValueType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Wert** <br/> |Gibt den Wert an, der in der Einschränkung verglichen werden soll.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Enthält](contains.md) <br/> |Stellt einen Suchausdruck dar, der bestimmt, ob eine angegebene Eigenschaft den angegebenen konstanten Zeichenfolgewert enthält.  <br/> |
|[FieldURIOrConstant](fielduriorconstant.md) <br/> |Stellt eine Eigenschaft oder einen konstanten Wert dar, der beim Vergleich mit einer anderen Eigenschaft verwendet werden soll.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Zeichenfolgenwert im **Value-Attribut** muss in den Typ umgewandelt werden, mit dem Sie vergleichen möchten. Wenn Sie beispielsweise eine Date/Time-Eigenschaft mit einem Konstantenwert vergleichen, muss der Zeichenfolgenwert ein Datum/eine Uhrzeit darstellen. 
  
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

