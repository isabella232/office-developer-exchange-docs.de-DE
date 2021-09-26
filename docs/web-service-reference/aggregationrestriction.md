---
title: AggregationRestriction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d05044f9-d2ff-4aca-956c-20c9cb2f7709
description: Das AggregationRestriction-Element gibt einen Wert an, der auf eine Reihe von Persona-Eigenschaften angewendet wird, die sich aus einer FindPeople-Anforderung ergeben, und filtert das Ergebnis gemäß der angegebenen Einschränkung.
ms.openlocfilehash: 6a00035f87e0f365f4551df1a6ff570e01761770
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546791"
---
# <a name="aggregationrestriction"></a>AggregationRestriction

Das **AggregationRestriction-Element** gibt einen Wert an, der auf eine Reihe von Persona-Eigenschaften angewendet wird, die sich aus einer FindPeople-Anforderung ergeben, und filtert das Ergebnis gemäß der angegebenen Einschränkung. 
  
```XML
<AggregationRestriction>
   <SearchExpression/>
</AggregationRestriction>
```

 **RestrictionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[SearchExpression](searchexpression.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[FindPeople](findpeople.md)
  
## <a name="remarks"></a>HinwBemerkungeneise

Das **AggregationRestriction-Element** kann ein beliebiges untergeordnetes Element enthalten, das die **SearchExpression-Ersetzungsgruppe** verwendet. Die Elemente, die Teil der **Suchexpression-Ersetzungsgruppe** sind: [Contains](contains.md), [Excludes](excludes.md), [Exists](exists.md), [Not](not.md), [Or](or.md), [And](and.md), [IsEqualTo](isequalto.md), [IsNotEqualTo](isnotequalto.md), [IsGreaterThan](isgreaterthan.md), [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md), [IsLessThanOrEqualTo](islessthan.md)und [IsLessThanOrEqualTo](islessthanorequalto.md).
  
Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |messages.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

