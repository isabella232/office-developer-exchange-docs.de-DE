---
title: Gruppen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Groups
api_type:
- schema
ms.assetid: 6b6b2d67-219d-4dfb-a4ed-d627b1cfb33f
description: Das Groups-Element enthält eine Auflistung von Gruppen, die mit den Such- und Aggregationskriterien gefunden werden, die in der FindItem-Vorgangsanforderung identifiziert werden.
ms.openlocfilehash: f47ab4111137d2e5d98fcc6dcf40fadc073b7af9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539682"
---
# <a name="groups"></a>Gruppen

Das **Groups-Element** enthält eine Auflistung von Gruppen, die mit den Such- und Aggregationskriterien gefunden werden, die in der [FindItem-Vorgangsanforderung](finditem-operation.md) identifiziert werden. 
  
```xml
<Groups>
   <GroupedItems/>
</Groups>
```

 **ArrayOfGroupedItemsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GroupedItems](groupeditems.md) <br/> |Stellt eine Auflistung von Elementen dar, die das Ergebnis eines gruppierten [FindItem-Vorgangsaufrufs](finditem-operation.md) sind.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[RootFolder (FindItemResponseMessage)](rootfolder-finditemresponsemessage.md) <br/> |Enthält die Ergebnisse einer Suche eines einzelnen Stammordners während eines [FindItem-Vorgangs.](finditem-operation.md)  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Eine [GroupedItems-Instanz](groupeditems.md) tritt für jede unterschiedliche Gruppe innerhalb des Ergebnisses auf. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindItem-Vorgang](finditem-operation.md)


[Suchen von Elementen](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

