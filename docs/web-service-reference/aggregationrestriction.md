---
title: AggregationRestriction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d05044f9-d2ff-4aca-956c-20c9cb2f7709
description: Das AggregationRestriction-Element gibt einen Wert, der einen Satz von Persona Eigenschaften entsteht eine Anforderung FindPeople angewendet wird, und das Ergebnis entsprechend der angegebenen Einschränkung filtert.
ms.openlocfilehash: 8b4d5952dedb4de0201d2ecf2219c69f65f7dc09
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757251"
---
# <a name="aggregationrestriction"></a>AggregationRestriction

Das **AggregationRestriction** -Element gibt einen Wert, der einen Satz von Persona Eigenschaften entsteht eine Anforderung FindPeople angewendet wird, und das Ergebnis entsprechend der angegebenen Einschränkung filtert. 
  
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
  
## <a name="remarks"></a>Hinweise

Das **AggregationRestriction** -Element kann ein untergeordnetes Element enthalten, die die Ersetzungsgruppe **SearchExpression** verwendet. Sind die Elemente, die Teil der Ersetzungsgruppe **SearchExpression** sind: [enthält](contains.md), [ausgeschlossen](excludes.md), [Exists](exists.md), [nicht](not.md), [oder](or.md), [und](and.md), ["IsEqualTo"](isequalto.md), [IsNotEqualTo](isnotequalto.md), [IsGreaterThan ](isgreaterthan.md), [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md), [IsLessThan](islessthan.md)und [IsLessThanOrEqualTo](islessthanorequalto.md).
  
Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

