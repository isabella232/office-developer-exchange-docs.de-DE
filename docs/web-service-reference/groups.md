---
title: Gruppen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Groups
api_type:
- schema
ms.assetid: 6b6b2d67-219d-4dfb-a4ed-d627b1cfb33f
description: Das groups-Element enthält eine Auflistung von Gruppen, die mit den Such-und Aggregations Kriterien gefunden werden, die in der FindItem-Vorgangsanforderung angegeben werden.
ms.openlocfilehash: 915d9dffd6d8cec1def6634e6b70642d563b5242
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530789"
---
# <a name="groups"></a>Gruppen

Das **Groups** -Element enthält eine Auflistung von Gruppen, die mit den Such-und Aggregations Kriterien gefunden werden, die in der [FindItem-Vorgangs](finditem-operation.md) Anforderung angegeben werden. 
  
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
|[GroupedItems](groupeditems.md) <br/> |Stellt eine Auflistung von Elementen dar, die das Ergebnis eines Aufrufs einer gruppierten [FindItem-Operation](finditem-operation.md) sind.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[RootFolder (FindItemResponseMessage)](rootfolder-finditemresponsemessage.md) <br/> |Enthält die Ergebnisse aus der Suche eines einzelnen Stammordners während eines Vorgangs des [FindItem-Vorgangs](finditem-operation.md) .  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Für jede unterschiedliche Gruppe innerhalb des Ergebnisses wird eine [GroupedItems](groupeditems.md) -Instanz ausgeführt. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.
  
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

