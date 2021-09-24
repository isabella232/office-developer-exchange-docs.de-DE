---
title: QueryString (Zeichenfolge)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f81b1b3d-9fe4-4ab3-b517-42e4207fa596
description: Das QueryString-Element gibt einen Satz von Werten an, die zurückgegeben werden sollen, die der Abfragezeichenfolge in einer FindPeople-Vorgangsanforderung entsprechen. Eine Suche ohne angegebene QueryString gibt alle Elemente aus dem angegebenen Ordner zurück.
ms.openlocfilehash: 6dfd4b5552511e2551baf5ce645f82d4f74e5499
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523734"
---
# <a name="querystring-string"></a>QueryString (Zeichenfolge)

Das **QueryString-Element** gibt einen Satz von Werten an, die zurückgegeben werden sollen, die der Abfragezeichenfolge in einer [FindPeople-Vorgangsanforderung](findpeople-operation.md) entsprechen. Eine Suche ohne **angegebene QueryString** gibt alle Elemente aus dem angegebenen Ordner zurück. 
  
```XML
<QueryString/> 
```

 **Zeichenfolge**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindPeople](findpeople.md) <br/> |Enthält die Argumente für eine Suche nach [einem FindPeople-Vorgang.](findpeople-operation.md)  <br/> |
   
## <a name="text-value"></a>Textwert

Der **QueryString-Textwert** stellt eine Postfachabfrage dar, die mithilfe einer Teilmenge der [Erweiterten Abfragesyntax (Advanced Query Syntax, AQS)](https://msdn.microsoft.com/library/aa965711%28VS.85%29.aspx)ausgeführt wird. Informationen zur Syntax für dieses Element finden Sie unter [QueryString (QueryStringType)](querystring-querystringtype.md).
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindPeople-Vorgang](findpeople-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

