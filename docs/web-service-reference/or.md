---
title: Oder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Or
api_type:
- schema
ms.assetid: 4876d83a-73a3-4953-9d95-3048e6b76ccb
description: Or-Element stellt ein Suchbegriff, der ein logisches OR Suchbegriffs durchführt, die er enthält. Oder zurückgegebenen True, wenn ein untergeordnetes Element true zurückgegeben. Oder benötigen Sie mindestens zwei untergeordnete Elemente.
ms.openlocfilehash: 46cf031047aeb09e05a385150ab7587968aef345
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830661"
---
# <a name="or"></a>Oder

Das Element **oder** stellt einen Suchbegriff, der ein logisches **oder** den Ausdruck für die Suche durchführt, die er enthält. **Oder** gibt **true** zurück, wenn einer der untergeordneten **true**zurückgegeben. **Oder** muss mindestens zwei untergeordnete Elemente aufweisen. 
  
```xml
<Or>
   <SearchExpression/>
   <SearchExpression/>
</Or>
```

 **OrType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SearchExpression](searchexpression.md) <br/> | Stellt die Basisklasse für Ausdrücke innerhalb einer Einschränkung dar. <br/><br/>Eines der folgenden Elemente muss für das Element **SearchExpression** ersetzt werden: <br/> <br/>- [Vorhanden ist](exists.md) <br/>- [Schließt](excludes.md) <br/>- ["IsEqualTo"](isequalto.md) <br/>- [IsNotEqualTo](isnotequalto.md) <br/>- [IsGreaterThan](isgreaterthan.md) <br/>- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md) <br/>- [IsLessThan](islessthan.md) <br/>- [IsLessThanOrEqualTo](islessthanorequalto.md) <br/>- [Enthält](contains.md) <br/>- [Nicht](not.md) <br/>- [Und](and.md) <br/>- **Oder** <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Einschränkung](restriction.md) <br/> |Stellt die Einschränkung oder die Abfrage, die zum Filtern von Elementen oder Ordner in FindItem/FindFolder, und suchen Sie Ordner Vorgänge verwendet wird.  <br/> |
|[not](not.md) <br/> |Stellt einen Search-Ausdruck, der den booleschen Wert des Suchbegriffs negiert, die er enthält.  <br/> |
|[Und](and.md) <br/> |Stellt einen Search-Ausdruck, der eine Boolean **und** -Operation zwischen zwei oder mehr Suchausdrücke ausgeführt werden können. Das Ergebnis der **AND** -Operation ist **true** , wenn **alle enthaltenen das Element **und** Suchausdrücke zutreffen**.  <br/> |
|**- oder -** <br/> |Stellt einen Search-Ausdruck, der eine logische **OR** -Operation für den Suchbegriff durchführt, die er enthält. **Oder** gibt **true** zurück, wenn einer der untergeordneten **true**zurückgegeben. **Oder** muss mindestens zwei untergeordnete Elemente aufweisen.  <br/> |
   
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

