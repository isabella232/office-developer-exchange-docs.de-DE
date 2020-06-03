---
title: IsEqualTo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsEqualTo
api_type:
- schema
ms.assetid: 48e7e067-049c-4184-8026-071e6f558e8a
description: Das IsEqualTo-Element stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und zu true ausgewertet wird, wenn Sie gleich sind.
ms.openlocfilehash: 857192443ab0520bb26ead399bc5364cc862a4fb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455296"
---
# <a name="isequalto"></a>IsEqualTo

Das **IsEqualTo** -Element stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und zu true ausgewertet wird, wenn Sie gleich sind. 
  
```xml
<IsEqualTo>
   <FieldURI/>
   <FieldURIOrConstant/>
</IsEqualTo>
```

```xml
<IsEqualTo>
   <ExtendedFieldURI/>
   <FieldURIOrConstant/>
</IsEqualTo>
```

```xml
<IsEqualTo>
   <IndexedFieldURI/> 
   <FieldURIOrConstant/>
</IsEqualTo>
```

**IsEqualToType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifiziert häufig referenzierte Eigenschaften nach URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifiziert einzelne Member eines Wörterbuchs.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifiziert MAPI-Eigenschaften.  <br/> |
|[FieldURIOrConstant](fielduriorconstant.md) <br/> |Stellt eine Eigenschaft oder einen konstanten Wert dar, der beim Vergleich mit einer anderen Eigenschaft verwendet werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Einschränkung](restriction.md) <br/> |Stellt die Einschränkung oder Abfrage dar, die zum Filtern von Elementen oder Ordnern in FindItem/FindFolder und Suchordner Vorgängen verwendet wird.  <br/> |
|[not](not.md) <br/> |Stellt einen Suchausdruck dar, der den booleschen Wert des darin enthaltenen Suchausdrucks negiert.  <br/> |
|[Und](and.md) <br/> |Stellt einen Suchausdruck dar, mit dem Sie einen booleschen Wert und eine Operation zwischen zwei oder mehr Suchausdrücken ausführen können. Das Ergebnis der and-Operation ist **true** , wenn alle in der enthaltenen Suchausdrücke auf **true**festgelegt sind.  <br/> |
|[- oder -](or.md) <br/> |Stellt einen Suchausdruck dar, der einen logischen oder den darin enthaltenen Suchausdruck ausführt. [Oder](or.md) gibt true zurück, wenn eines der untergeordneten Elemente true zurückgibt. **Oder** muss mindestens zwei untergeordnete Elemente aufweisen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie Zeichenfolgenvergleiche durchführen möchten, verwenden Sie das [Contains](contains.md) -Element, da es Optionen für übereinstimmende Parameter bereitstellt, beispielsweise Case und Leerzeichen. Verwenden Sie das [Not](not.md) -Element in Verbindung mit dem [Contains](contains.md) -Element, um das Ergebnis zu negieren. 
  
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

