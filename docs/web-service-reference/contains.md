---
title: Enthält
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Contains
api_type:
- schema
ms.assetid: 476d059d-c243-43e9-b475-319fc413ade2
description: Das Contains-Element stellt einen Suchausdruck dar, der bestimmt, ob eine bestimmte Eigenschaft den angegebenen Konstantenzeichenfolgenwert enthält.
ms.openlocfilehash: 6e36ede6a10c64a4aa53e68721d9edf7893c4c05
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59547547"
---
# <a name="contains"></a>Enthält

Das **Contains-Element** stellt einen Suchausdruck dar, der bestimmt, ob eine bestimmte Eigenschaft den angegebenen Konstantenzeichenfolgenwert enthält. 
  
```xml
<Contains ContainmentMode="" ContainmentComparison="">
   <FieldURI/>
   <Constant/>
</Contains>
```

```xml
<Contains ContainmentMode="" ContainmentComparison="">
   <ExtendedFieldURI/>
   <Constant/>
</Contains>
```

```xml
<Contains ContainmentMode="" ContainmentComparison="">
   <IndexedFieldURI/>
   <Constant/>
</Contains>
```


**ContainsExpressionType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**ContainmentMode** <br/> |Identifiziert die Grenzen einer Suche.  <br/> |
|**ContainmentComparison** <br/> |Bestimmt, ob die Suche Fälle und Leerzeichen ignoriert.  <br/> |
   
#### <a name="containmentmode-attribute-values"></a>ContainmentMode-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|FullString  <br/> |Der Vergleich erfolgt zwischen der vollständigen Zeichenfolge und der Konstante. Der Eigenschaftswert und die angegebene Konstante sind genau gleich.  <br/> |
|Präfix  <br/> |Der Vergleich erfolgt zwischen dem Zeichenfolgenpräfix und der Konstante.  <br/> |
|Teilzeichenfolge  <br/> |Der Vergleich erfolgt zwischen einer Teilzeichenfolge der Zeichenfolge und der Konstante.  <br/> |
|PrefixOnWords  <br/> |Der Vergleich erfolgt zwischen einem Präfix für einzelne Wörter in der Zeichenfolge und der Konstante.  <br/> |
|ExactPhrase  <br/> |Der Vergleich erfolgt zwischen einem exakten Ausdruck in der Zeichenfolge und der Konstante.  <br/> |
   
#### <a name="containmentcomparison-attribute-values"></a>ContainmentComparison-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Genaue  <br/> |Der Vergleich muss genau sein.  <br/> |
|IgnoreCase  <br/> |Der Vergleich ignoriert die Groß-/Kleinschreibung.  <br/> |
|IgnoreNonSpacingCharacters  <br/> |Der Vergleich ignoriert Nicht-Leerzeichen.  <br/> |
|Weit  <br/> |Zu entfernen.  <br/> |
|IgnoreCaseAndNonSpacingCharacters  <br/> |Der Vergleich ignoriert Groß-/Kleinschreibung und Nicht-Leerzeichen.  <br/> |
|LooseAndIgnoreCase  <br/> |Zu entfernen.  <br/> |
|LooseAndIgnoreNonSpace  <br/> |Zu entfernen.  <br/> |
|LooseAndIgnoreCaseAndIgnoreNonSpace  <br/> |Zu entfernen.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifies frequently referenced properties by URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifiziert einzelne Mitglieder eines Wörterbuchs.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifies MAPI properties.  <br/> |
|[Konstante](constant.md) <br/> |Identifiziert einen konstanten Wert in einer Einschränkung.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Stellt die Einschränkung oder Abfrage dar, die zum Filtern von Elementen oder Ordnern in FindItem/FindFolder und Suchordnervorgängen verwendet wird.  <br/> |
|[not](not.md) <br/> |Stellt einen Suchausdruck dar, der den booleschen Wert des darin enthaltenen Suchausdrucks negiert.  <br/> |
|[Und](and.md) <br/> |Stellt einen Suchausdruck dar, mit dem Sie einen booleschen And-Vorgang zwischen zwei oder mehr Suchausdrücken ausführen können. Das Ergebnis des And-Vorgangs ist **"true",** wenn alle in "And" enthaltenen Suchausdrücke **"True"** sind.  <br/> |
|[- oder -](or.md) <br/> |Stellt einen Suchausdruck dar, der ein logisches OR für den darin enthaltenen Suchausdruck ausführt. Das [Or-Element](or.md) gibt **"true"** zurück, wenn eines seiner untergeordneten Elemente **"true"** zurückgibt.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die Attribute werden verwendet, um zu bestimmen, wie die Elemente abgeglichen werden.
  
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

