---
title: Enthält
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
description: Das Contains-Element stellt einen Search-Ausdruck, der bestimmt, ob eine bestimmte Eigenschaft den angegebenen Konstante String-Wert enthält.
ms.openlocfilehash: 083efdf32cd32bea6964361b5b558480aa937280
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757642"
---
# <a name="contains"></a>Enthält

Das **Contains** -Element stellt einen Search-Ausdruck, der bestimmt, ob eine bestimmte Eigenschaft den angegebenen Konstante String-Wert enthält. 
  
```xml
<Contains ContainmentMode="" ContainmentComparison="">
   <FieldURI/>
   <Constant/>
</Contains>
```

 **ContainsExpressionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**ContainmentMode** <br/> |Identifiziert die Grenzen einer Suche an.  <br/> |
|**ContainmentComparison** <br/> |Bestimmt, ob die Suche Anfragen und Leerzeichen werden ignoriert.  <br/> |
   
#### <a name="containmentmode-attribute-values"></a>Attributwerte ContainmentMode

|**Wert**|**Beschreibung**|
|:-----|:-----|
|FullString  <br/> |Vergleich wird zwischen der vollständigen Zeichenfolge sowie die Konstante. Wert der Eigenschaft und die angegebene Konstante sind exakt identisch.  <br/> |
|Das Präfix  <br/> |Vergleich wird zwischen dem Präfix Zeichenfolge sowie die Konstante.  <br/> |
|Teilzeichenfolge  <br/> |Vergleich wird zwischen der Zeichenfolge eine Teilzeichenfolge sowie die Konstante.  <br/> |
|PrefixOnWords  <br/> |Vergleich wird zwischen einem Präfix auf einzelne Wörter in der Zeichenfolge und die Konstante die.  <br/> |
|ExactPhrase  <br/> |Vergleich wird zwischen einem exakten Wortlaut in der Zeichenfolge sowie die Konstante die.  <br/> |
   
#### <a name="containmentcomparison-attribute-values"></a>Attributwerte ContainmentComparison

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Exact  <br/> |Der Vergleich muss exakt sein.  <br/> |
|IgnoreCase  <br/> |Der Vergleich wird zur Groß-und Kleinschreibung ignoriert.  <br/> |
|IgnoreNonSpacingCharacters  <br/> |Der Vergleich ignoriert nicht-gesperrte Zeichen.  <br/> |
|Weit  <br/> |Entfernt werden soll.  <br/> |
|IgnoreCaseAndNonSpacingCharacters  <br/> |Der Vergleich wird die Groß-/Kleinschreibung sowie nicht-gesperrte Zeichen ignoriert.  <br/> |
|LooseAndIgnoreCase  <br/> |Entfernt werden soll.  <br/> |
|LooseAndIgnoreNonSpace  <br/> |Entfernt werden soll.  <br/> |
|LooseAndIgnoreCaseAndIgnoreNonSpace  <br/> |Entfernt werden soll.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifiziert die Eigenschaften von URI häufig verwiesen wird.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Einzelne Elemente eines Wörterbuchs identifiziert.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |MAPI-Eigenschaften identifiziert.  <br/> |
|[Konstante](constant.md) <br/> |Gibt einen konstanten Wert in einer Einschränkung.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Einschränkung](restriction.md) <br/> |Stellt die Einschränkung oder die Abfrage, die zum Filtern von Elementen oder Ordner in FindItem/FindFolder, und suchen Sie Ordner Vorgänge verwendet wird.  <br/> |
|[not](not.md) <br/> |Stellt einen Search-Ausdruck, der den booleschen Wert des Suchbegriffs negiert darin enthaltenen dar.  <br/> |
|[Und](and.md) <br/> |Stellt einen Search-Ausdruck, der Sie einen Vorgang vom Typ Boolean und zwischen zwei oder mehr Suchausdrücke ausführen kann. Das Ergebnis der And-Operation ist **true** , wenn **alle enthaltenen das And Search Ausdrücke zutreffen**.  <br/> |
|[- oder -](or.md) <br/> |Stellt einen Suche Ausdruck, der ein logisches OR Suchbegriffs durchführt darin enthaltenen dar. Das Element [oder](or.md) gibt **true** zurück, wenn ein untergeordnetes Element **true**zurück.  <br/> |
   
## <a name="remarks"></a>Hinweise

Die Attribute werden verwendet, um zu bestimmen, wie die Elemente zugeordnet sind.
  
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

