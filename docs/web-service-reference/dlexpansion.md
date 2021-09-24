---
title: DLExpansion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DLExpansion
api_type:
- schema
ms.assetid: 9e50278d-fe6a-45e2-a72b-0fb06809e128
description: Das DLExpansion-Element enthält ein Array von Postfächern, die in einer Verteilerliste enthalten sind.
ms.openlocfilehash: 7c214948b133ea2f30a47b2321c27b555b90e2fa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517210"
---
# <a name="dlexpansion"></a>DLExpansion

Das **DLExpansion-Element** enthält ein Array von Postfächern, die in einer Verteilerliste enthalten sind. 
  
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
|**IndexedPagingOffset** <br/> |Stellt den nächsten Index dar, der für die nächste Anforderung verwendet werden soll, wenn Sie eine indizierte Seitenansicht verwenden.  <br/> |
|**NumeratorOffset** <br/> |Stellt den neuen Zählerwert dar, der für die nächste Anforderung verwendet werden soll, wenn Sie Seitenansichten für Bruchzahlen verwenden.  <br/> |
|**AbsoluteDenominator** <br/> |Stellt den nächsten Nenner dar, der für die nächste Anforderung verwendet werden soll, wenn Sie Seitenansichten für Bruchzahlen verwenden.  <br/> |
|**IncludesLastItemInRange** <br/> |Gibt an, ob die aktuellen Ergebnisse das letzte Element in der Abfrage enthalten, sodass keine zusätzliche Auslagerung erforderlich ist.  <br/> |
|**TotalItemsInView** <br/> |Stellt die Gesamtanzahl der Elemente in der Ansicht dar.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Postfach](mailbox.md) <br/> |Ein e-Mail-aktivierten Active Directory Directory Service-Objekt identifiziert.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ExpandDLResponseMessage](expanddlresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen ExpandDL-Anforderung.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [ExpandDL-Vorgang](expanddl-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md) 
- [EWS-Referenz für Exchange](ews-reference-for-exchange.md)

