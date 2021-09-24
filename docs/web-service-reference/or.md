---
title: 'Oder:'
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Or
api_type:
- schema
ms.assetid: 4876d83a-73a3-4953-9d95-3048e6b76ccb
description: Das Or-Element stellt einen Suchausdruck dar, der ein logisches OR für den darin enthaltenen Suchausdruck ausführt. Oder gibt "true" zurück, wenn eines seiner untergeordneten Elemente "true" zurückgibt. Oder es müssen zwei oder mehr untergeordnete Elemente vorhanden sein.
ms.openlocfilehash: 70cf76d98f019887fea2ed8fe8f082f20fbcde37
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59529557"
---
# <a name="or"></a>Oder:

Das **Or-Element** stellt einen Suchausdruck dar, der ein logisches **OR** für den darin enthaltenen Suchausdruck ausführt. **Or** will return **true** if any of its children return **true**. **Oder** es müssen zwei oder mehr untergeordnete Elemente vorhanden sein. 
  
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
|[SearchExpression](searchexpression.md) <br/> | Stellt die Basisklasse für Ausdrücke innerhalb einer Einschränkung dar. <br/><br/>Eines der folgenden Elemente muss durch das **SearchExpression-Element** ersetzt werden: <br/> <br/>- [Existiert](exists.md) <br/>- [Schließt](excludes.md) <br/>- [IsEqualTo](isequalto.md) <br/>- [IsNotEqualTo](isnotequalto.md) <br/>- [IsGreaterThan](isgreaterthan.md) <br/>- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md) <br/>- [IsLessThan](islessthan.md) <br/>- [IsLessThanOrEqualTo](islessthanorequalto.md) <br/>- [Enthält](contains.md) <br/>- [Nicht](not.md) <br/>- [Und](and.md) <br/>- **Oder** <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Stellt die Einschränkung oder Abfrage dar, die zum Filtern von Elementen oder Ordnern in FindItem/FindFolder und Suchordnervorgängen verwendet wird.  <br/> |
|[not](not.md) <br/> |Stellt einen Suchausdruck dar, der den booleschen Wert des darin enthaltenen Suchausdrucks negiert.  <br/> |
|[Und](and.md) <br/> |Stellt einen Suchausdruck dar, mit dem Sie einen booleschen **AND-Vorgang** zwischen zwei oder mehr Suchausdrücken ausführen können. The result of the **AND** operation is **true** if all the search expressions contained within the **And** element are **true**.  <br/> |
|**- oder -** <br/> |Stellt einen Suchausdruck dar, der einen logischen **OR-Vorgang** für den darin enthaltenen Suchausdruck ausführt. **Or** will return **true** if any of its children return **true**. **Oder** es müssen zwei oder mehr untergeordnete Elemente vorhanden sein.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

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

