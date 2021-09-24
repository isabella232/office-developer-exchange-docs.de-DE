---
title: SearchExpression
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SearchExpression
api_type:
- schema
ms.assetid: daa179b6-8c7f-4268-a312-c2acc67fa7c3
description: Das SearchExpression-Element ist ein abstraktes Element, das das ersetzte Element innerhalb einer Einschränkung darstellt. Alle Suchausdrücke sind von diesem Basistyp abgeleitet. Dieses Element wird in einem XML-Instanzdokument nicht verwendet.
ms.openlocfilehash: e8047d333b36d77bc6823efd6488a15a6d2501a4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517847"
---
# <a name="searchexpression"></a>SearchExpression

Das **SearchExpression-Element** ist ein abstraktes Element, das das ersetzte Element innerhalb einer Einschränkung darstellt. Alle Suchausdrücke sind von diesem Basistyp abgeleitet. Dieses Element wird in einem XML-Instanzdokument nicht verwendet. 
  
```xml
<SearchExpression/>
```

 **SearchExpressionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Stellt die Einschränkung oder Abfrage dar, die zum Filtern von Elementen oder Ordnern in FindItem/FindFolder und Suchordnervorgängen verwendet wird.  <br/> |
|[not](not.md) <br/> |Stellt einen Suchausdruck dar, der den booleschen Wert des darin enthaltenen Suchausdrucks negiert.  <br/> |
|[Und](and.md) <br/> |Stellt einen Suchausdruck dar, mit dem Sie einen booleschen **AND-Vorgang** zwischen zwei oder mehr Suchausdrücken ausführen können. The result of the **AND** operation is **true** if all the search expressions contained within the **And** element are **true**.  <br/> |
|[- oder -](or.md) <br/> |Stellt einen Suchausdruck dar, der einen logischen **OR-Vorgang** für den darin enthaltenen Suchausdruck ausführt. **Or** will return **true** if any of its children return **true**. **Oder** es müssen zwei oder mehr untergeordnete Elemente vorhanden sein.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Jedes Filterelement, das Teil der Suchexpression-Ersetzungsgruppe ist, kann anstelle des SearchExpression-Elements angezeigt werden.
  
> [!NOTE]
> Dieses Element tritt nie direkt in einem Instanzdokument auf. 
  
Die folgenden Elemente sind Mitglieder der SearchExpression-Ersetzungsgruppe:
  
- [Exists](exists.md)
    
- [Schließt](excludes.md)
    
- [IsEqualTo](isequalto.md)
    
- [IsNotEqualTo](isnotequalto.md)
    
- [IsGreaterThan](isgreaterthan.md)
    
- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)
    
- [IsLessThan](islessthan.md)
    
- [IsLessThanOrEqualTo](islessthanorequalto.md)
    
- [Contains](contains.md)
    
- [not](not.md)
    
- [Und](and.md)
    
- [- oder -](or.md)
    
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

