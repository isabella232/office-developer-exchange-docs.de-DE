---
title: DeletedOccurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DeletedOccurrence
api_type:
- schema
ms.assetid: ff24ea15-0cd7-407d-a378-73ec16451870
description: Das DeletedOccurrence-Element stellt ein gelöschtes Vorkommen eines Wiederkehrenden Kalenderelements dar.
ms.openlocfilehash: 69e77f86097fe7037fc217806e4ef1b33b99c549
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542484"
---
# <a name="deletedoccurrence"></a>DeletedOccurrence

Das **DeletedOccurrence-Element** stellt ein gelöschtes Vorkommen eines Wiederkehrenden Kalenderelements dar. 
  
```xml
<DeletedOccurrence>
   <Start/>
</DeletedOccurrence>
```

 **DeletedOccurrenceInfoType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Start](start.md) <br/> |Stellt die Startzeit eines gelöschten Vorkommens eines wiederkehrenden Kalenderelements dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DeletedOccurrences](deletedoccurrences.md) <br/> |Enthält ein Array gelöschter Vorkommen eines Terminserienkalenderelements.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)  
- [EWS-Referenz für Exchange](ews-reference-for-exchange.md)

