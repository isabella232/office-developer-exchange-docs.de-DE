---
title: RootFolder (FindItemResponseMessage)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RootFolder
api_type:
- schema
ms.assetid: 187e009f-efaa-42a8-8962-329a645213ab
description: Das RootFolder-Element enthält die Ergebnisse einer Suche eines einzelnen Stammordners während eines FindItem-Vorgangs.
ms.openlocfilehash: 96fa9e162dde34394e7c34543dd25a6f018ae7de
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59527537"
---
# <a name="rootfolder-finditemresponsemessage"></a>RootFolder (FindItemResponseMessage)

Das **RootFolder -Element** enthält die Ergebnisse einer Suche eines einzelnen Stammordners während eines [FindItem-Vorgangs.](finditem-operation.md)
  
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
|**IndexedPagingOffset** <br/> |Stellt den nächsten Index dar, der bei Verwendung einer indizierten Seitenansicht für die nächste Anforderung verwendet werden soll.  <br/> |
|**NumeratorOffset** <br/> |Stellt den neuen Zählerwert dar, der für die nächste Anforderung verwendet werden soll, wenn Seitenansichten für Bruchzahlen verwendet werden.  <br/> |
|**AbsoluteDenominator** <br/> |Stellt den nächsten Nenner dar, der für die nächste Anforderung beim Auslagern von Bruchzahlen verwendet werden soll.  <br/> |
|**IncludesLastItemInRange** <br/> |Gibt an, ob die aktuellen Ergebnisse das letzte Element in der Abfrage enthalten, sodass keine weitere Auslagerung erforderlich ist.  <br/> |
|**TotalItemsInView** <br/> |Stellt die Gesamtzahl der Elemente dar, die die Einschränkung bestehen. In einem gruppierten [FindItem-Vorgang](finditem-operation.md)gibt das **TotalItemsInView-Attribut** die Gesamtanzahl der Elemente in der Ansicht plus die Gesamtzahl der Gruppen zurück.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Items](items.md) <br/> |Enthält ein Array von Gefundenen Elementen, deren Suchkriterien in der [FindItem-Vorgangsanforderung](finditem-operation.md) angegeben sind.  <br/> |
|[Gruppen](groups.md) <br/> |Enthält eine Auflistung von gefundenen Gruppen, deren Such- und Aggregationskriterien in der [FindItem-Vorgangsanforderung](finditem-operation.md) angegeben sind.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindItemResponseMessage](finditemresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer [FindItem-Vorgangsanforderung.](finditem-operation.md)  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server mit installierter Clientzugriffsserverrolle ausgeführt wird.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
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


[Suchen von Elementen](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

