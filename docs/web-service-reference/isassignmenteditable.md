---
title: IsAssignmentEditable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsAssignmentEditable
api_type:
- schema
ms.assetid: 0ddf9181-f65e-4ad6-ad69-7b074ea0f2e7
description: Das IsAssignmentEditable-Element stellt den Vorgangstyp dar.
ms.openlocfilehash: 5eb091b24e2c97f7aa6072044fed998b6c9c1651
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468054"
---
# <a name="isassignmenteditable"></a>IsAssignmentEditable

Das **IsAssignmentEditable** -Element stellt den Vorgangstyp dar. 
  
```xml
<IsAssignmentEditable/>
```

 **Integer**
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
|1   <br/> |Eine Aufgabenanforderung.  <br/> |
|2  <br/> |Eine Aufgaben Akzeptanz durch einen Empfänger einer Aufgabenanfrage.  <br/> |
|3  <br/> |Eine Aufgabe, die von einem Empfänger einer Aufgabenanfrage abnimmt.  <br/> |
|4   <br/> |Eine Aktualisierung einer vorherigen Aufgabenanforderung.  <br/> |
|5   <br/> |Nicht verwendet.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

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

