---
title: DistinguishedGroupBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DistinguishedGroupBy
api_type:
- schema
ms.assetid: 6ff3ac48-02ba-40ec-a71b-c401bb2b127c
description: Das DistinguishedGroupBy-Element stellt Standardgruppierungen für FindItem-Abfragen bereit.
ms.openlocfilehash: 8b6001994603e49cd1c77288a93cfb9270d51e21
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511836"
---
# <a name="distinguishedgroupby"></a>DistinguishedGroupBy

Das **DistinguishedGroupBy-Element** stellt Standardgruppierungen für FindItem-Abfragen bereit. 
  
- [FindItem](finditem.md) 
- [DistinguishedGroupBy](distinguishedgroupby.md)
  
```xml
<DistinguishedGroupBy>
   <StandardGroupBy/>
</DistinguishedGroupBy>
```

 **DistinguishedGroupByType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[StandardGroupBy](standardgroupby.md) <br/> |Stellt die standardmäßigen Gruppierungs- und Aggregierungsmechanismen für einen gruppierten FindItem-Vorgang dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung zum Suchen von Elementen in einem Postfach.<br/><br/>Es folgt der XPath-Ausdruck für dieses Element:  `/FindItem` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das **DistinguishedGroupBy-Element** kann einem FindItem-Vorgang hinzugefügt werden, wenn die Ergebnisse gruppiert zurückgegeben werden müssen und eine der Standardgruppen die Gruppierungsanforderungen erfüllt. Wenn weder das **DistinguishedGroupBy-Element** noch das [GroupBy-Element](groupby.md) angegeben ist, werden findItem-Ergebnisse ohne Gruppierung zurückgegeben. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [FindItem-Vorgang](finditem-operation.md)
- [Suchen von Elementen](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

