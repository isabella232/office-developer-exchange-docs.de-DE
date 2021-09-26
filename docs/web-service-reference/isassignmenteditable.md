---
title: IsAssignmentEditable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IsAssignmentEditable
api_type:
- schema
ms.assetid: 0ddf9181-f65e-4ad6-ad69-7b074ea0f2e7
description: Das IsAssignmentEditable-Element stellt den Vorgangstyp dar.
ms.openlocfilehash: 10676cc8c6196a7294f3550856a47dce7d717e6a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544950"
---
# <a name="isassignmenteditable"></a>IsAssignmentEditable

Das **IsAssignmentEditable-Element** stellt den Vorgangstyp dar. 
  
```xml
<IsAssignmentEditable/>
```

 **Ganzzahl**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Aufgabe](task.md) <br/> |Stellt eine Aufgabe im Exchange-Informationsspeicher dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Diese Eigenschaft ist schreibgeschützt. In der folgenden Tabelle sind die möglichen Werte aufgeführt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Der Standardwert für alle Aufgabenelemente.  <br/> |
|1  <br/> |Eine Aufgabenanforderung.  <br/> |
|2  <br/> |Eine Aufgabenakzeptanz von einem Empfänger einer Aufgabenanfrage.  <br/> |
|3  <br/> |Eine Vorgangsdegression von einem Empfänger einer Aufgabenanforderung.  <br/> |
|4   <br/> |Eine Aktualisierung einer vorherigen Aufgabenanforderung.  <br/> |
|5  <br/> |Nicht verwendet.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

