---
title: Contains
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Contains
api_type:
- schema
ms.assetid: 476d059d-c243-43e9-b475-319fc413ade2
description: Das Contains-Element stellt einen Suchausdruck dar, der bestimmt, ob eine bestimmte Eigenschaft den angegebenen Konstanten Zeichenfolgenwert enthält.
ms.openlocfilehash: 79529bd752bcbce954ae3c8b0085c203b4eb8777
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527117"
---
# <a name="contains"></a>Contains

Das **Contains** -Element stellt einen Suchausdruck dar, der bestimmt, ob eine bestimmte Eigenschaft den angegebenen Konstanten Zeichenfolgenwert enthält. 
  
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
|**ContainmentMode** <br/> |Gibt die Grenzen einer Suche an.  <br/> |
|**ContainmentComparison** <br/> |Bestimmt, ob die Suche Fälle und Leerzeichen ignoriert.  <br/> |
   
#### <a name="containmentmode-attribute-values"></a>ContainmentMode-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Vollständig  <br/> |Der Vergleich erfolgt zwischen der vollständigen Zeichenfolge und der Konstanten. Der Eigenschaftswert und die angegebene Konstante sind exakt identisch.  <br/> |
|Präfix visobjtype  <br/> |Der Vergleich erfolgt zwischen dem Zeichenfolgen Präfix und der Konstanten.  <br/> |
|Teilzeichenfolge  <br/> |Der Vergleich besteht zwischen einer Teilzeichenfolge der Zeichenfolge und der Konstanten.  <br/> |
|PrefixOnWords  <br/> |Der Vergleich besteht zwischen einem Präfix für einzelne Wörter in der Zeichenfolge und der Konstante.  <br/> |
|ExactPhrase  <br/> |Der Vergleich beruht auf einem exakten Ausdruck in der Zeichenfolge und der Konstanten.  <br/> |
   
#### <a name="containmentcomparison-attribute-values"></a>ContainmentComparison-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Genauen  <br/> |Der Vergleich muss exakt sein.  <br/> |
|IgnoreCase  <br/> |Der Vergleich ignoriert die Groß-/Kleinschreibung.  <br/> |
|IgnoreNonSpacingCharacters  <br/> |Der Vergleich ignoriert Zeichen ohne Zeilenabstand.  <br/> |
|Weit  <br/> |Entfernt werden soll.  <br/> |
|IgnoreCaseAndNonSpacingCharacters  <br/> |Der Vergleich ignoriert Groß-/Kleinschreibung und Zeichen ohne Zeilenabstand.  <br/> |
|LooseAndIgnoreCase  <br/> |Entfernt werden soll.  <br/> |
|LooseAndIgnoreNonSpace  <br/> |Entfernt werden soll.  <br/> |
|LooseAndIgnoreCaseAndIgnoreNonSpace  <br/> |Entfernt werden soll.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifiziert häufig referenzierte Eigenschaften nach URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifiziert einzelne Member eines Wörterbuchs.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifiziert MAPI-Eigenschaften.  <br/> |
|[Konstante](constant.md) <br/> |Gibt einen konstanten Wert in einer Einschränkung an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Einschränkung](restriction.md) <br/> |Stellt die Einschränkung oder Abfrage dar, die zum Filtern von Elementen oder Ordnern in FindItem/FindFolder und Suchordner Vorgängen verwendet wird.  <br/> |
|[not](not.md) <br/> |Stellt einen Suchausdruck dar, der den booleschen Wert des darin enthaltenen Suchausdrucks negiert.  <br/> |
|[Und](and.md) <br/> |Stellt einen Suchausdruck dar, mit dem Sie einen booleschen Wert und eine Operation zwischen zwei oder mehr Suchausdrücken ausführen können. Das Ergebnis der and-Operation ist **true** , wenn alle in der enthaltenen Suchausdrücke auf **true**festgelegt sind.  <br/> |
|[- oder -](or.md) <br/> |Stellt einen Suchausdruck dar, der eine logische OR-Anweisung für den darin enthaltenen Suchausdruck ausführt. Das [or](or.md) -Element gibt **true** zurück, wenn eines der untergeordneten Elemente **true**zurückgibt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

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

