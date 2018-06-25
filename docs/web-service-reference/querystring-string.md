---
title: QueryString (Zeichenfolge)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f81b1b3d-9fe4-4ab3-b517-42e4207fa596
description: Das QueryString-Element gibt einen Satz von Werten, die die Abfragezeichenfolge in einer FindPeople Vorgang Anforderung entsprechen zurückgegeben werden soll. Eine Suche mit keine angegebenen QueryString gibt alle Elemente aus dem angegebenen Ordner zurück.
ms.openlocfilehash: 9c5c733adcec1496e36986fd720b56b0a0274593
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830935"
---
# <a name="querystring-string"></a>QueryString (Zeichenfolge)

Das **QueryString** -Element gibt einen Satz von Werten, die die Abfragezeichenfolge in einer Anforderung [FindPeople Vorgang](findpeople-operation.md) entsprechen zurückgegeben werden soll. Eine Suche mit keine **QueryString** angegeben gibt alle Elemente aus dem angegebenen Ordner zurück. 
  
```XML
<QueryString/> 
```

 **string**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindPeople](findpeople.md) <br/> |Enthält die Argumente für eine Suche [FindPeople Vorgang](findpeople-operation.md) .  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **QueryString** stellt eine Abfrage Postfach mithilfe einer Teilmenge der [(Erweiterte Query Syntax, AQS)](http://msdn.microsoft.com/en-us/library/aa965711%28VS.85%29.aspx). Informationen zur Syntax für dieses Elements finden Sie unter [QueryString (QueryStringType)](querystring-querystringtype.md).
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindPeople-Vorgang](findpeople-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

