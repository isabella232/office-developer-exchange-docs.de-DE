---
title: RootFolder (FindFolderResponseMessage)
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
ms.assetid: 5089c815-663f-46be-bc59-aed9ee20f94a
description: Das RootFolder-Element enthält die Ergebnisse einer Suche eines einzelnen Stammordners während eines FindFolder-Vorgangs.
ms.openlocfilehash: 582d4642bb4ecd2816beba6df863eb274762f804
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512275"
---
# <a name="rootfolder-findfolderresponsemessage"></a>RootFolder (FindFolderResponseMessage)

Das **RootFolder -Element** enthält die Ergebnisse einer Suche eines einzelnen Stammordners während eines [FindFolder-Vorgangs.](findfolder-operation.md)
  
```xml
<RootFolder IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Folders/>
</RootFolder>
```

 **FindFolderParentType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|IndexedPagingOffset  <br/> |Stellt den nächsten Index dar, der bei Verwendung einer indizierten Seitenansicht für die nächste Anforderung verwendet werden soll.  <br/> |
|NumeratorOffset  <br/> |Stellt den neuen Zählerwert dar, der für die nächste Anforderung bei Verwendung von Seitenbruchansichten verwendet werden soll.  <br/> |
|AbsoluteDenominator  <br/> |Stellt den nächsten Nenner dar, der für die nächste Anforderung beim Auslagern von Bruchzahlen verwendet werden soll.  <br/> |
|IncludesLastItemInRange  <br/> |Gibt an, ob die aktuellen Ergebnisse den letzten Ordner in der Abfrage enthalten, sodass keine weitere Auslagerung erforderlich ist.  <br/> |
|TotalItemsInView  <br/> |Stellt die Gesamtanzahl der Ordner dar, die die Einschränkung bestehen.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Ordner](folders-ex15websvcsotherref.md) <br/> |Enthält ein Array von Ordnern, die mithilfe des [FindFolder-Vorgangs](findfolder-operation.md)gefunden wurden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindFolderResponseMessage](findfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer [FindFolder-Vorgangsanforderung.](findfolder-operation.md)  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindFolder-Vorgang](findfolder-operation.md)


[Suchen von Ordnern](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

