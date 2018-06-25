---
title: DLExpansion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DLExpansion
api_type:
- schema
ms.assetid: 9e50278d-fe6a-45e2-a72b-0fb06809e128
description: Das DLExpansion-Element enthält ein Array von Postfächern, die in einer Verteilerliste enthalten sind.
ms.openlocfilehash: 06081b4aba761a7137f921b3bc1c8d6b2afab88c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758083"
---
# <a name="dlexpansion"></a>DLExpansion

Das **DLExpansion** -Element enthält ein Array von Postfächern, die in einer Verteilerliste enthalten sind. 
  
- [ExpandDLResponse](expanddlresponse.md) 
- [ResponseMessages](responsemessages.md) 
- [ExpandDLResponseMessage](expanddlresponsemessage.md)
- [DLExpansion](dlexpansion.md)
  
```xml
<DLExpansion AbsoluteDenominator"" IncludesLastItemInRange="" IndexedPagingOffset="" NumeratorOffset="" TotalItemsInView="">
   <Mailbox/>
</DLExpansion>
```

 **ArrayOfDLExpansionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**IndexedPagingOffset** <br/> |Stellt den Index, der bei Verwendung einer indizierten Seitenansicht für die nächste Anforderung verwendet werden soll.  <br/> |
|**NumeratorOffset** <br/> |Den neue Zähler-Wert, für die nächste Anforderung verwendet wird, bei Verwendung der Seitenansichten Bruch darstellt.  <br/> |
|**AbsoluteDenominator** <br/> |Die nächste Nenner für die nächste Anforderung verwendet wird, bei Verwendung der Seitenansichten Bruch darstellt.  <br/> |
|**IncludesLastItemInRange** <br/> |Gibt an, ob die aktuellen Ergebnisse das letzte Element in der Abfrage enthalten, sodass zusätzliche Paging nicht mehr benötigt wird.  <br/> |
|**TotalItemsInView** <br/> |Die Gesamtanzahl der Elemente in der Ansicht darstellt.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Postfach](mailbox.md) <br/> |Ein e-Mail-aktivierten Active Directory Directory Service-Objekt identifiziert.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ExpandDLResponseMessage](expanddlresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer Anforderung der ExpandDL.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Der ExpandDL-Vorgang](expanddl-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md) 
- [EWS-Referenz für Exchange](ews-reference-for-exchange.md)

