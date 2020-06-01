---
title: AggregationRestriction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d05044f9-d2ff-4aca-956c-20c9cb2f7709
description: Das AggregationRestriction-Element gibt einen Wert an, der auf eine Gruppe von Persona-Eigenschaften angewendet wird, die sich aus einer FindPeople-Anforderung ergeben, und filtert das Ergebnis entsprechend der angegebenen Einschränkung.
ms.openlocfilehash: f07e54235cf13b43da26ed1c56596d3c7c357bf2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463524"
---
# <a name="aggregationrestriction"></a>AggregationRestriction

Das **AggregationRestriction** -Element gibt einen Wert an, der auf eine Gruppe von Persona-Eigenschaften angewendet wird, die sich aus einer FindPeople-Anforderung ergeben, und filtert das Ergebnis entsprechend der angegebenen Einschränkung. 
  
```XML
<AggregationRestriction>
   <SearchExpression/>
</AggregationRestriction>
```

 **Restrictiontype**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[SearchExpression](searchexpression.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[FindPeople](findpeople.md)
  
## <a name="remarks"></a>Bemerkungen

Das **AggregationRestriction** -Element kann ein beliebiges untergeordnetes Element enthalten, das die **Such** Satz Ersetzungsgruppe verwendet. Die Elemente, die Bestandteil der Substitutions Gruppe für die **Suche** sind, sind: [Contains](contains.md), [excludes](excludes.md), [EXISTS](exists.md), [Not](not.md), [or](or.md), [and](and.md), [IsEqualTo](isequalto.md), [IsNotEqualTo](isnotequalto.md), [isgreaterthan](isgreaterthan.md), [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md), [IsLessThan](islessthan.md)und [IsLessThanOrEqualTo](islessthanorequalto.md).
  
Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

