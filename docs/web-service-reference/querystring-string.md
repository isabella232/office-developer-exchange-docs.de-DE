---
title: QueryString (Zeichenfolge)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f81b1b3d-9fe4-4ab3-b517-42e4207fa596
description: Das QueryString-Element gibt eine Gruppe von Werten an, die zurückgegeben werden sollen, die mit der Abfragezeichenfolge in einer FindPeople-Vorgangsanforderung übereinstimmen. Bei einer Suche ohne QueryString-Angabe werden alle Elemente aus dem angegebenen Ordner zurückgegeben.
ms.openlocfilehash: ec025f86d3e6fb74810e9c539eba102d05adbb93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465324"
---
# <a name="querystring-string"></a>QueryString (Zeichenfolge)

Das **QueryString** -Element gibt eine Gruppe von Werten an, die zurückgegeben werden sollen, die mit der Abfragezeichenfolge in einer [FindPeople-Vorgangs](findpeople-operation.md) Anforderung übereinstimmen. Bei einer Suche ohne **QueryString** -Angabe werden alle Elemente aus dem angegebenen Ordner zurückgegeben. 
  
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
|[FindPeople](findpeople.md) <br/> |Enthält die Argumente für eine [FindPeople-Vorgangs](findpeople-operation.md) Suche.  <br/> |
   
## <a name="text-value"></a>Textwert

Der **QueryString** -Textwert stellt eine Post Fach Abfrage dar, die mithilfe einer Teilmenge der [erweiterten Abfrage Syntax (AQS)](https://msdn.microsoft.com/library/aa965711%28VS.85%29.aspx)erstellt wurde. Informationen zur Syntax dieses Elements finden Sie unter [QueryString (querystringtype)](querystring-querystringtype.md).
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindPeople-Vorgang](findpeople-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

