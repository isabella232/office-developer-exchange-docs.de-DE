---
title: Und
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- And
api_type:
- schema
ms.assetid: 790246c2-37ad-49a8-91b9-6186d743b011
description: Das And-Element stellt einen Suchausdruck dar, mit dem Sie einen booleschen AND-Vorgang zwischen zwei oder mehr Suchausdrücken ausführen können. The result of the AND operation is true if all the search expressions contained within the And element are true.
ms.openlocfilehash: b6cf8ffbb19ea3aff917493e6ae4e324025c6ac9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541532"
---
# <a name="and"></a>Und

Das **And-Element** stellt einen Suchausdruck dar, mit dem Sie einen booleschen **AND-Vorgang** zwischen zwei oder mehr Suchausdrücken ausführen können. The result of the **AND** operation is **true** if all the search expressions contained within the **And** element are **true**.
  
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
|[SearchExpression](searchexpression.md) <br/> | Stellt die Basisklasse für Ausdrücke innerhalb einer Einschränkung dar. Es müssen zwei oder mehr Suchausdrücke in einem And-Vorgang vorhanden sein.<br/><br/>  Eines der folgenden Elemente muss durch das **SearchExpression-Element** ersetzt werden:<ul><li> [Exists](exists.md)</li><li>[Schließt](excludes.md)</li><li>[IsEqualTo](isequalto.md)</li><li>[IsNotEqualTo](isnotequalto.md)</li><li>[IsGreaterThan](isgreaterthan.md)</li><li>[IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</li><li>[IsLessThan](islessthan.md)</li><li>[IsLessThanOrEqualTo](islessthanorequalto.md)</li><li>[Contains](contains.md)</li><li>[not](not.md)</li><li>**Und**</li><li>[- oder -](or.md) </li></ul> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Stellt die Einschränkung oder Abfrage dar, die zum Filtern von Elementen oder Ordnern in FindItem/FindFolder und Suchordnervorgängen verwendet wird.  <br/> |
|[not](not.md) <br/> |Stellt einen Suchausdruck dar, der den booleschen Wert des darin enthaltenen Suchausdrucks negiert.  <br/> |
|**Und** <br/> |Stellt einen Suchausdruck dar, mit dem Sie einen booleschen **AND-Vorgang** zwischen zwei oder mehr Suchausdrücken ausführen können. The result of the **AND** operation is **true** if all of the search expressions contained within the **And** element are **true**.  <br/> |
|[- oder -](or.md) <br/> |Stellt einen Suchausdruck dar, der einen logischen **OR-Vorgang** für den darin enthaltenen Suchausdruck ausführt. **Or** will return **true** if any of its children return **true**. **Oder** es müssen zwei oder mehr untergeordnete Elemente vorhanden sein.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

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

