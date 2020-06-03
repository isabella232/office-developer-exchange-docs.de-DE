---
title: Schließt
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Excludes
api_type:
- schema
ms.assetid: bbaeddf6-9a67-4ee0-af99-7a7a5bbdc0e1
description: Das excludes-Element führt eine bitweise Maske der angegebenen Eigenschaft und eines angegebenen Werts aus.
ms.openlocfilehash: d5fcd8b86b454aa731bd43974b5b7d674fe76ed6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530614"
---
# <a name="excludes"></a>Schließt

Das **excludes** -Element führt eine bitweise Maske der angegebenen Eigenschaft und eines angegebenen Werts aus. 
  
```xml
<Excludes>
   <FieldURI/>
   <Bitmask/>
</Excludes>
```

```xml
<Excludes>
   <ExtendedFieldURI/> 
   <Bitmask/>
</Excludes>
```

```xml
<Excludes>
   <IndexedFieldURI/> 
   <Bitmask/>
</Excludes>
```

**ExcludesType**

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
|[Bitmaske](bitmask.md) <br/> |Stellt eine Hexadezimal-oder Dezimal Maske dar, die während eines [Exclude](excludes.md) -Einschränkungs Vorgangs verwendet werden soll. Wenn die Bitmaske eine Hexadezimalzahl darstellt, muss Ihr das Präfix 0x oder 0x vorangestellt werden. Andernfalls wird Sie als Dezimalzahl betrachtet.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Einschränkung](restriction.md) <br/> |Stellt die Einschränkung oder Abfrage dar, die zum Filtern von Elementen oder Ordnern in FindItem/FindFolder und Suchordner Vorgängen verwendet wird.  <br/> |
|[not](not.md) <br/> |Stellt einen Suchausdruck dar, der den booleschen Wert des darin enthaltenen Suchausdrucks negiert.  <br/> |
|[Und](and.md) <br/> |Stellt einen Suchausdruck dar, mit dem Sie einen booleschen Wert und eine Operation zwischen zwei oder mehr Suchausdrücken ausführen können. Das Ergebnis der and-Operation ist **true** , wenn alle in der enthaltenen Suchausdrücke auf **true**festgelegt sind.  <br/> |
|[- oder -](or.md) <br/> |Stellt einen Suchausdruck dar, der eine logische OR-Anweisung für den darin enthaltenen Suchausdruck ausführt. Das [or](or.md) -Element gibt **true** zurück, wenn eines der untergeordneten Elemente **true**zurückgibt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

" **Excludes** " wird in " **true** " aufgelöst, wenn ein-und-Vorgang, der für Folgendes ausgeführt wird, in 0 aufgelöst wird: 
  
1. Der bitweise Wert für die Eigenschaft
    
2. Der Wert der Bitmaske für die Eigenschaft
    
**Excludes** können nur auf eine Eigenschaft angewendet werden, die einen ganzzahligen Wert aufweist. Wenn der Eigenschaftentyp etwas anderes als eine ganze Zahl ist, wird ein Fehlercode von **ErrorUnsupportedPathForQuery** in der Antwort zurückgegeben. 
  
Sie können den Reverse-Vorgang durchführen, indem Sie Not (excludes) aufrufen.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

