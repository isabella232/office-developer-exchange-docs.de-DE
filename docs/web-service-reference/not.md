---
title: Nicht
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Not
api_type:
- schema
ms.assetid: 1aa16318-7e90-4b19-bce8-dd1a20a66223
description: Das Element nicht stellt einen Search-Ausdruck, der den booleschen Wert des Suchbegriffs negiert, die er enthält.
ms.openlocfilehash: f5bc709d8b1e77a13b3598905651ac1750436f03
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830553"
---
# <a name="not"></a>Nicht

Das Element **nicht** stellt einen Search-Ausdruck, der den booleschen Wert des Suchbegriffs negiert, die er enthält. 
  
```xml
<Not>
   <SearchExpression/>
</Not>
```

 **NotType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SearchExpression](searchexpression.md) <br/> | Stellt die Basisklasse für Ausdrücke innerhalb einer Einschränkung dar. <br/><br/>Eines der folgenden Elemente muss für das Element **SearchExpression** ersetzt werden: <br/> <br/>- [Vorhanden ist](exists.md) <br/>- [Schließt](excludes.md) <br/>- ["IsEqualTo"](isequalto.md) <br/>- [IsNotEqualTo](isnotequalto.md) <br/>- [IsGreaterThan](isgreaterthan.md) <br/>- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md) <br/>- [IsLessThan](islessthan.md) <br/>- [IsLessThanOrEqualTo](islessthanorequalto.md) <br/>- [Enthält](contains.md) <br/>- **Nicht** <br/>- [Und](and.md) <br/>- [Oder](or.md) <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Einschränkung](restriction.md) <br/> |Stellt die Einschränkung oder die Abfrage, die zum Filtern von Elementen oder Ordner in FindItem/FindFolder, und suchen Sie Ordner Vorgänge verwendet wird.  <br/> |
|**not** <br/> |Stellt einen Search-Ausdruck, der den booleschen Wert des Suchbegriffs negiert, die er enthält.  <br/> |
|[Und](and.md) <br/> |Stellt einen Search-Ausdruck, der eine Boolean **und** -Operation zwischen zwei oder mehr Suchausdrücke ausgeführt werden können. Das Ergebnis der **AND** -Operation ist **true** , wenn **alle enthaltenen das Element **und** Suchausdrücke zutreffen**.  <br/> |
|[- oder -](or.md) <br/> |Stellt einen Search-Ausdruck, der eine logische **OR** -Operation für den Suchbegriff durchführt, die er enthält. **Oder** gibt **true** zurück, wenn einer der untergeordneten **true**zurückgegeben. **Oder** muss mindestens zwei untergeordnete Elemente aufweisen.  <br/> |
   
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

