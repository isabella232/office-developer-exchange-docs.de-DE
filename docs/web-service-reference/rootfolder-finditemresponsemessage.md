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
description: Das RootFolder-Element enthält die Ergebnisse einer Suche eines einzelnen Stammordners während eines FindItem-Vorgangs.
ms.openlocfilehash: 3bbab325dff26139739c50ef519b215aea620a0b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457130"
---
# <a name="rootfolder-finditemresponsemessage"></a>RootFolder (FindItemResponseMessage)

Das **RootFolder** -Element enthält die Ergebnisse einer Suche eines einzelnen Stammordners während eines [FindItem-Vorgangs](finditem-operation.md).
  
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
|**IndexedPagingOffset** <br/> |Stellt den nächsten Index dar, der bei der Verwendung einer indizierten Auslagerungs Ansicht für die nächste Anforderung verwendet werden soll.  <br/> |
|**NumeratorOffset** <br/> |Stellt den neuen Zählerwert dar, der für die nächste Anforderung verwendet werden soll, wenn Bruch Seitenansichten verwendet werden.  <br/> |
|**AbsoluteDenominator** <br/> |Stellt den nächsten Nenner dar, der für die nächste Anforderung bei Bruchzahlen verwendet wird.  <br/> |
|**IncludesLastItemInRange** <br/> |Gibt an, ob die aktuellen Ergebnisse das letzte Element in der Abfrage enthalten, sodass kein weiteres Paging erforderlich ist.  <br/> |
|**TotalItemsInView** <br/> |Stellt die Gesamtzahl der Elemente dar, die die Einschränkung übergeben. In einem gruppierten [FindItem-Vorgang](finditem-operation.md)gibt das **TotalItemsInView** -Attribut die Gesamtanzahl der Elemente in der Ansicht sowie die Gesamtzahl der Gruppen zurück.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Elemente](items.md) <br/> |Enthält ein Array mit gefundenen Elementen, die die in der FindItem- [Vorgangs](finditem-operation.md) Anforderung angegebenen Suchkriterien aufweisen.  <br/> |
|[Groups](groups.md) <br/> |Enthält eine Auflistung von Gruppen, die die Such-und Aggregations Kriterien aufweisen, die in der [FindItem-Vorgangs](finditem-operation.md) Anforderung angegeben sind.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindItemResponseMessage](finditemresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer [FindItem-Vorgangs](finditem-operation.md) Anforderung.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server mit installierter Client Zugriffs-Server Rolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindItem-Vorgang](finditem-operation.md)
  
[IndexedPagingOffset](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.IndexedPagingOffset.aspx)
  
[NumeratorOffset](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.NumeratorOffset.aspx)
  
[AbsoluteDenominator](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.AbsoluteDenominator.aspx)
  
[IncludesLastItemInRange](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.IncludesLastItemInRange.aspx)
  
[TotalItemsInView](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.TotalItemsInView.aspx)


[Suchen von Elementen](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

