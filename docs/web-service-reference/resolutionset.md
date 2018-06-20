---
title: ResolutionSet
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResolutionSet
api_type:
- schema
ms.assetid: 43d5b876-0e87-4414-9b1d-bff1c1ec825c
description: Das ResolutionSet-Element enthält ein Array von Lösungen für ein mehrdeutiger Name.
ms.openlocfilehash: ad7bd31c85051e8c80aea25aa9e6f2914cf0ad01
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831160"
---
# <a name="resolutionset"></a>ResolutionSet

Das **ResolutionSet** -Element enthält ein Array von Lösungen für ein mehrdeutiger Name. 
  
[ResolveNamesResponse](resolvenamesresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[ResolveNamesResponseMessage](resolvenamesresponsemessage.md)
  
[ResolutionSet](resolutionset.md)
  
```xml
<ResolutionSet IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Resolution/>
</ResolutionSet>
```

 **ArrayOfResolutionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**IndexedPagingOffset** <br/> |Stellt den Index, der bei Verwendung einer indizierten Seitenansicht für die nächste Anforderung verwendet werden soll.  <br/> |
|**NumeratorOffset** <br/> |Den neue Zähler-Wert, für die nächste Anforderung verwendet wird, bei Verwendung der Seitenansichten Bruch darstellt.  <br/> |
|**AbsoluteDenominator** <br/> |Die nächste Nenner für die nächste Anforderung verwendet wird, bei Verwendung der Seitenansichten Bruch darstellt.  <br/> |
|**IncludesLastItemInRange** <br/> |Dieses Attribut wird true, wenn die aktuellen Ergebnisse das letzte Element in der Abfrage enthalten sein, sodass zusätzliche Paging nicht mehr benötigt wird.  <br/> |
|**TotalItemsInView** <br/> |Die Gesamtanzahl der Elemente in der Ansicht darstellt.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Lösung](resolution.md) <br/> |Enthält eine einzelne aufgelöste Entität.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ResolveNamesResponseMessage](resolvenamesresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer Anforderung ResolveNames.  <br/> |
   
## <a name="remarks"></a>Hinweise

Ein **ResolutionSet** -Element kann maximal 100 aufgelöst Entitäten enthalten. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ResolveNames](resolvenames.md)
  
[ResolveNamesResponse](resolvenamesresponse.md)
  
[ResolveNames-Vorgang](resolvenames-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

