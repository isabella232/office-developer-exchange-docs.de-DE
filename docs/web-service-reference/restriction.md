---
title: Einschränkung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Restriction
api_type:
- schema
ms.assetid: 77f19014-d112-4999-8e83-ecc32a117a73
description: Das Restriction-Element stellt die Einschränkung oder Abfrage dar, die zum Filtern von Elementen oder Ordnern in FindItem/FindFolder und Suchordnervorgängen verwendet wird.
ms.openlocfilehash: 378c2d0ce7911638e5e58346de46759e7fdd87f1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540566"
---
# <a name="restriction"></a>Einschränkung

Das **Restriction-Element** stellt die Einschränkung oder Abfrage dar, die zum Filtern von Elementen oder Ordnern in FindItem/FindFolder und Suchordnervorgängen verwendet wird. 
  
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
|[Und](and.md) <br/> |Stellt einen Suchausdruck dar, mit dem Sie einen booleschen **AND-Vorgang** zwischen zwei oder mehr Suchausdrücken ausführen können.  <br/> |
|[Enthält](contains.md) <br/> |Stellt einen Suchausdruck dar, der bestimmt, ob eine angegebene Eigenschaft den angegebenen konstanten Zeichenfolgewert enthält.  <br/> |
|[Schließt](excludes.md) <br/> |Führt eine bitweise Maske der Eigenschaften aus.  <br/> |
|[Exists](exists.md) <br/> |Stellt einen Suchausdruck dar, der **true** zurückgibt, wenn die angegebene Eigenschaft zu einem Element vorhanden ist.  <br/> |
|[IsEqualTo](isequalto.md) <br/> |Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** ausgibt, wenn sie gleich sind.  <br/> |
|[IsGreaterThan](isgreaterthan.md) <br/> |Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem Konstantenwert oder einer anderen Eigenschaft vergleicht und **"true"** zurückgibt, wenn die erste Eigenschaft größer als der Wert oder die Eigenschaft ist.  <br/> |
|[IsGreaterThanOrEqualTo](isgreaterthanorequalto.md) <br/> |Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem Konstantenwert oder einer anderen Eigenschaft vergleicht und **"true"** zurückgibt, wenn die erste Eigenschaft größer oder gleich dem Wert oder der Eigenschaft ist.  <br/> |
|[IsLessThan](islessthan.md) <br/> |Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem Konstantenwert oder einer anderen Eigenschaft vergleicht und **"true"** zurückgibt, wenn die erste Eigenschaft kleiner als der Wert oder die Eigenschaft ist.  <br/> |
|[IsLessThanOrEqualTo](islessthanorequalto.md) <br/> |Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem Konstantenwert oder einer anderen Eigenschaft vergleicht und **"true"** zurückgibt, wenn die erste Eigenschaft kleiner oder gleich dem Wert oder der Eigenschaft ist.  <br/> |
|[IsNotEqualTo](isnotequalto.md) <br/> |Stellt einen Suchausdruck dar, der einer Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** zurückgibt, wenn die Wert nicht identisch sind.  <br/> |
|[not](not.md) <br/> |Stellt einen Suchausdruck dar, der den booleschen Wert des darin enthaltenen Suchausdrucks negiert.  <br/> |
|[- oder -](or.md) <br/> |Stellt einen Suchausdruck dar, der einen logischen **OR-Vorgang** für den darin enthaltenen Suchausdruck ausführt. Das **Or-Element** gibt **"true"** zurück, wenn eines seiner untergeordneten Elemente **"true"** zurückgibt.  <br/> |
|[SearchExpression](searchexpression.md) <br/> |Stellt das ersetzte Element innerhalb einer Einschränkung dar. Dieses Element wird in einem XML-Instanzdokument nicht verwendet.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Definiert eine Anforderung zum Identifizieren von Ordnern in einem Postfach.  <br/> |
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung zum Suchen von Elementen in einem Postfach.  <br/> |
|[SearchParameters](searchparameters.md) <br/> |Stellt die Parameter dar, die einen Suchordner definieren.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

