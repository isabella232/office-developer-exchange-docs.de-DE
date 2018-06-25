---
title: RootFolder (FindFolderResponseMessage)
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
ms.assetid: 5089c815-663f-46be-bc59-aed9ee20f94a
description: Das RootFolder-Element enthält die Ergebnisse der Suche in der ein einzelner Stammordner während eines Vorgangs FindFolder.
ms.openlocfilehash: 1cd79d5fa34318e7fe29606df84cbf0ef0520b93
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831253"
---
# <a name="rootfolder-findfolderresponsemessage"></a>RootFolder (FindFolderResponseMessage)

Das **RootFolder** -Element enthält die Ergebnisse der Suche in der ein einzelner Stammordner während einer [FindFolder Vorgang](findfolder-operation.md).
  
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
|IndexedPagingOffset  <br/> |Stellt den Index, der bei Verwendung eine indizierten Paging-Ansicht für die nächste Anforderung verwendet werden soll.  <br/> |
|NumeratorOffset  <br/> |Steht für den neuen Wert Zähler verwenden Sie für die nächste Anforderung bei Bruchzahlen Seitenansichten Verwendung.  <br/> |
|AbsoluteDenominator  <br/> |Verwenden Sie für die nächste Anforderung bei Bruchzahlen Paging die nächste Nenner darstellt.  <br/> |
|IncludesLastItemInRange  <br/> |Gibt an, ob die aktuellen Ergebnisse der letzten Ordner in der Abfrage enthalten, so dass weitere paging nicht mehr benötigt wird.  <br/> |
|TotalItemsInView  <br/> |Stellt die Gesamtzahl der Ordner, in denen die Einschränkung übergeben.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Ordner](folders-ex15websvcsotherref.md) <br/> |Enthält ein Array von Ordnern mithilfe der [FindFolder Vorgang](findfolder-operation.md)gefunden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindFolderResponseMessage](findfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer Anforderung [FindFolder Vorgang](findfolder-operation.md) .  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindFolder Operation](findfolder-operation.md)


[Suchen nach Ordnern](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

