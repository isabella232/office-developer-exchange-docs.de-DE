---
title: Und
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- And
api_type:
- schema
ms.assetid: 790246c2-37ad-49a8-91b9-6186d743b011
description: Das Element und stellt einen Search-Ausdruck, der Sie einen Vorgang vom Typ Boolean und zwischen zwei oder mehr Suchausdrücke ausführen kann. Das Ergebnis der AND-Operation ist True, wenn alle dem And-Element enthaltenen Suchausdrücke zutreffen.
ms.openlocfilehash: d287d57d68aeca7127325dc8fb65fd0190e5b5eb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757265"
---
# <a name="and"></a>Und

Das Element **und** stellt einen Search-Ausdruck, der eine Boolean **und** -Operation zwischen zwei oder mehr Suchausdrücke ausgeführt werden können. Das Ergebnis der **AND** -Operation ist **true** , wenn **alle enthaltenen das Element **und** Suchausdrücke zutreffen**.
  
```xml
<And>
   <SearchExpression/>
   <SearchExpression/>
</And>
```

 **AndType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SearchExpression](searchexpression.md) <br/> | Stellt die Basisklasse für Ausdrücke innerhalb einer Einschränkung dar. Es muss mindestens zwei Suchausdrücke in eine And-Operation.<br/><br/>  Eines der folgenden Elemente muss für das Element **SearchExpression** ersetzt werden:<ul><li> [Exists](exists.md)</li><li>[Schließt](excludes.md)</li><li>["IsEqualTo"](isequalto.md)</li><li>[IsNotEqualTo](isnotequalto.md)</li><li>[IsGreaterThan](isgreaterthan.md)</li><li>[IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</li><li>[IsLessThan](islessthan.md)</li><li>[IsLessThanOrEqualTo](islessthanorequalto.md)</li><li>[Enthält](contains.md)</li><li>[not](not.md)</li><li>**Und**</li><li>[- oder -](or.md) </li></ul> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Einschränkung](restriction.md) <br/> |Stellt die Einschränkung oder die Abfrage, die zum Filtern von Elementen oder Ordner in FindItem/FindFolder, und suchen Sie Ordner Vorgänge verwendet wird.  <br/> |
|[not](not.md) <br/> |Stellt einen Search-Ausdruck, der den booleschen Wert des Suchbegriffs negiert, die er enthält.  <br/> |
|**Und** <br/> |Stellt einen Search-Ausdruck, der eine Boolean **und** -Operation zwischen zwei oder mehr Suchausdrücke ausgeführt werden können. Das Ergebnis der **AND** -Operation ist **true** , wenn **Alle Suchausdrücke **und** -Element enthaltenen zutreffen**.  <br/> |
|[- oder -](or.md) <br/> |Stellt einen Search-Ausdruck, der eine logische **OR** -Operation für den Suchbegriff durchführt, die er enthält. **Oder** gibt **true** zurück, wenn einer der untergeordneten **true**zurückgegeben. **Oder** muss mindestens zwei untergeordnete Elemente aufweisen.  <br/> |
   
## <a name="remarks"></a>Hinweise

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

