---
title: RootFolder (FindItemResponseMessage)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RootFolder
api_type:
- schema
ms.assetid: 187e009f-efaa-42a8-8962-329a645213ab
description: Das RootFolder-Element enthält die Ergebnisse der Suche in der ein einzelner Stammordner während eines Vorgangs FindItem.
ms.openlocfilehash: ea17369ef4efc4112a738b430c8f0dbab3886341
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831254"
---
# <a name="rootfolder-finditemresponsemessage"></a>RootFolder (FindItemResponseMessage)

Das **RootFolder** -Element enthält die Ergebnisse der Suche in der ein einzelner Stammordner während einer [FindItem Vorgang](finditem-operation.md).
  
```xml
<RootFolder IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Items/>
   <Groups/>
</RootFolder>
```

 **FindItemParentType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**IndexedPagingOffset** <br/> |Stellt den Index, der bei Verwendung eine indizierten Paging-Ansicht für die nächste Anforderung verwendet werden soll.  <br/> |
|**NumeratorOffset** <br/> |Steht für den neuen Zähler-Wert für die nächste Anforderung verwendet werden soll, wenn Teiler Seitenansichten verwenden.  <br/> |
|**AbsoluteDenominator** <br/> |Verwenden Sie für die nächste Anforderung bei Bruchzahlen Paging die nächste Nenner darstellt.  <br/> |
|**IncludesLastItemInRange** <br/> |Gibt an, ob die aktuellen Ergebnisse das letzte Element in der Abfrage enthalten, so dass weitere paging nicht mehr benötigt wird.  <br/> |
|**TotalItemsInView** <br/> |Stellt die Gesamtzahl der Elemente, die die Einschränkung übergeben. In einem gruppierten [FindItem Vorgang](finditem-operation.md)gibt das **TotalItemsInView** -Attribut die Gesamtanzahl der Elemente in der Ansicht plus die Gesamtzahl der Gruppen zurück.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Elemente](items.md) <br/> |Enthält ein Array von Elemente gefunden, die die Suchkriterien entsprechen, die in der Anforderung [FindItem Operation](finditem-operation.md) angegeben haben.  <br/> |
|[Gruppen](groups.md) <br/> |Enthält eine Auflistung von Gruppen gefunden, die die Suche und Aggregation Kriterien, die in der Anforderung [FindItem Vorgang](finditem-operation.md) identifiziert haben.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindItemResponseMessage](finditemresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer Anforderung [FindItem Vorgang](finditem-operation.md) .  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, der Exchange-Server, mit die Clientzugriffs-Serverrolle installiert ausgeführt wird.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindItem-Vorgang](finditem-operation.md)
  
[IndexedPagingOffset](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.IndexedPagingOffset.aspx)
  
[NumeratorOffset](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.NumeratorOffset.aspx)
  
[AbsoluteDenominator](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.AbsoluteDenominator.aspx)
  
[IncludesLastItemInRange](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.IncludesLastItemInRange.aspx)
  
[TotalItemsInView](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.TotalItemsInView.aspx)


[Finding Items](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

