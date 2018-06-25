---
title: SearchExpression
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SearchExpression
api_type:
- schema
ms.assetid: daa179b6-8c7f-4268-a312-c2acc67fa7c3
description: Das SearchExpression-Element ist ein abstraktes Element, das das ersetzte Element innerhalb einer Einschränkung darstellt. Alle Suchausdrücke werden von diesem Basistyp abgeleitet. Dieses Element wird in einem XML-Instanzendokument nicht verwendet.
ms.openlocfilehash: 8e0d09aec079280816cd9dfe2c1a55c88bb959a7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831286"
---
# <a name="searchexpression"></a>SearchExpression

Das **SearchExpression** -Element ist ein abstraktes Element, das das ersetzte Element innerhalb einer Einschränkung darstellt. Alle Suchausdrücke werden von diesem Basistyp abgeleitet. Dieses Element wird in einem XML-Instanzendokument nicht verwendet. 
  
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
|[Einschränkung](restriction.md) <br/> |Stellt die Einschränkung oder die Abfrage, die zum Filtern von Elementen oder Ordner in FindItem/FindFolder, und suchen Sie Ordner Vorgänge verwendet wird.  <br/> |
|[not](not.md) <br/> |Stellt einen Search-Ausdruck, der den booleschen Wert des Suchbegriffs negiert, die er enthält.  <br/> |
|[Und](and.md) <br/> |Stellt einen Search-Ausdruck, der eine Boolean **und** -Operation zwischen zwei oder mehr Suchausdrücke ausgeführt werden können. Das Ergebnis der **AND** -Operation ist **true** , wenn **alle enthaltenen das Element **und** Suchausdrücke zutreffen**.  <br/> |
|[- oder -](or.md) <br/> |Stellt einen Search-Ausdruck, der eine logische **OR** -Operation für den Suchbegriff durchführt, die er enthält. **Oder** gibt **true** zurück, wenn einer der untergeordneten **true**zurückgegeben. **Oder** muss mindestens zwei untergeordnete Elemente aufweisen.  <br/> |
   
## <a name="remarks"></a>Hinweise

Alle Filterelement, das Teil der Ersetzungsgruppe SearchExpression ist kann anstelle der SearchExpression-Element angezeigt werden.
  
> [!NOTE]
> Dieses Element wird nie direkt in einem Instanzendokument auftreten. 
  
Die folgenden Elemente sind Mitglieder der Ersetzungsgruppe SearchExpression:
  
- [Exists](exists.md)
    
- [Schließt](excludes.md)
    
- ["IsEqualTo"](isequalto.md)
    
- [IsNotEqualTo](isnotequalto.md)
    
- [IsGreaterThan](isgreaterthan.md)
    
- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)
    
- [IsLessThan](islessthan.md)
    
- [IsLessThanOrEqualTo](islessthanorequalto.md)
    
- [Enthält](contains.md)
    
- [not](not.md)
    
- [Und](and.md)
    
- [- oder -](or.md)
    
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

