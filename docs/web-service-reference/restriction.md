---
title: Einschränkung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Restriction
api_type:
- schema
ms.assetid: 77f19014-d112-4999-8e83-ecc32a117a73
description: Die Einschränkungselement stellt die Einschränkung oder die Abfrage, die zum Filtern von Elementen oder Ordner in FindItem/FindFolder, und suchen Sie Ordner Vorgänge verwendet wird.
ms.openlocfilehash: 6b5702696db29910ae476a370bf362fe6a036ae7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831213"
---
# <a name="restriction"></a>Einschränkung

**Die Einschränkungselement** stellt die Einschränkung oder die Abfrage, die zum Filtern von Elementen oder Ordner in FindItem/FindFolder, und suchen Sie Ordner Vorgänge verwendet wird. 
  
```xml
<Restriction>
   <SearchExpression/>
</Restriction>
```

 **RestrictionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Und](and.md) <br/> |Stellt einen Search-Ausdruck, der Sie einen booleschen **AND** -Vorgang zwischen zwei oder mehr Suchausdrücke ausführen kann.  <br/> |
|[Enthält](contains.md) <br/> |Stellt einen Suchausdruck dar, der bestimmt, ob eine angegebene Eigenschaft den angegebenen konstanten Zeichenfolgewert enthält.  <br/> |
|[Schließt](excludes.md) <br/> |Führt eine bitweise Maske der Eigenschaften aus.  <br/> |
|[Exists](exists.md) <br/> |Stellt einen Suchausdruck dar, der **true** zurückgibt, wenn die angegebene Eigenschaft zu einem Element vorhanden ist.  <br/> |
|["IsEqualTo"](isequalto.md) <br/> |Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** ausgibt, wenn sie gleich sind.  <br/> |
|[IsGreaterThan](isgreaterthan.md) <br/> |Stellt einen Search-Ausdruck, der eine Eigenschaft mit einem konstanten Wert oder einen anderen-Eigenschaft und gibt **true** verglichen, wenn die erste Eigenschaft größer ist als der Wert oder -Eigenschaft.  <br/> |
|[IsGreaterThanOrEqualTo](isgreaterthanorequalto.md) <br/> |Stellt einen Search-Ausdruck, der vergleicht eine Eigenschaft mit einen konstanten Wert oder einen anderen-Eigenschaft und gibt **true,** Wenn die erste Eigenschaft größer als oder gleich dem Wert oder-Eigenschaft ist.  <br/> |
|[IsLessThan](islessthan.md) <br/> |Stellt einen Search-Ausdruck, der eine Eigenschaft mit einem konstanten Wert oder einen anderen-Eigenschaft und gibt **true** vergleicht, ob die erste Eigenschaft kleiner als der Wert oder -Eigenschaft ist.  <br/> |
|[IsLessThanOrEqualTo](islessthanorequalto.md) <br/> |Stellt einen Search-Ausdruck, der eine Eigenschaft mit einem konstanten Wert oder einen anderen-Eigenschaft und gibt **true** vergleicht, ob die erste Eigenschaft kleiner oder gleich dem Wert oder-Eigenschaft ist.  <br/> |
|[IsNotEqualTo](isnotequalto.md) <br/> |Stellt einen Suchausdruck dar, der einer Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** zurückgibt, wenn die Wert nicht identisch sind.  <br/> |
|[not](not.md) <br/> |Stellt einen Search-Ausdruck, der den booleschen Wert des Suchbegriffs negiert darin enthaltenen dar.  <br/> |
|[- oder -](or.md) <br/> |Stellt einen Search-Ausdruck, der eine logische **OR** -Operation für den Suchbegriff durchführt darin enthaltenen dar. Das Element **oder** gibt **true** zurück, wenn ein untergeordnetes Element **true**zurück.  <br/> |
|[SearchExpression](searchexpression.md) <br/> |Stellt das ersetzte Element innerhalb einer Einschränkung. Dieses Element wird in einem XML-Instanzendokument nicht verwendet.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Definiert eine Anforderung zum Ordner in einem Postfach zu identifizieren.  <br/> |
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung zum Suchen von Elementen in einem Postfach an.  <br/> |
|[SearchParameters](searchparameters.md) <br/> |Stellt die Parameter, die einen Suchordner definieren.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

