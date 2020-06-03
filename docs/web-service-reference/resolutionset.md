---
title: Resolutionset
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
description: Das resolutionset-Element enthält ein Array von Auflösungen für einen eindeutigen Namen.
ms.openlocfilehash: 483a096a7fcedbabe25758ebcaa31c83405a0ad4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467172"
---
# <a name="resolutionset"></a>Resolutionset

Das **resolutionset** -Element enthält ein Array von Auflösungen für einen eindeutigen Namen. 
  
[ResolveNamesResponse](resolvenamesresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[ResolveNamesResponseMessage](resolvenamesresponsemessage.md)
  
[Resolutionset](resolutionset.md)
  
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
|**IndexedPagingOffset** <br/> |Stellt den nächsten Index dar, der für die nächste Anforderung verwendet werden soll, wenn Sie eine indizierte Seitenansicht verwenden.  <br/> |
|**NumeratorOffset** <br/> |Stellt den neuen Zählerwert dar, der für die nächste Anforderung verwendet werden soll, wenn Sie Ansichten mit Bruch Seiten verwenden.  <br/> |
|**AbsoluteDenominator** <br/> |Stellt den nächsten Nenner dar, der für die nächste Anforderung verwendet werden soll, wenn Sie Ansichten mit Bruch Seiten verwenden.  <br/> |
|**IncludesLastItemInRange** <br/> |Dieses Attribut ist true, wenn die aktuellen Ergebnisse das letzte Element in der Abfrage enthalten, sodass kein zusätzliches Paging erforderlich ist.  <br/> |
|**TotalItemsInView** <br/> |Stellt die Gesamtzahl der Elemente in der Ansicht dar.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Lösung](resolution.md) <br/> |Enthält eine einzelne aufgelöste Entität.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ResolveNamesResponseMessage](resolvenamesresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer ResolveNames-Anforderung.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Ein **resolutionset** -Element kann maximal 100 aufgelöste Entitäten enthalten. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ResolveNames](resolvenames.md)
  
[ResolveNamesResponse](resolvenamesresponse.md)
  
[ResolveNames-Vorgang](resolvenames-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

