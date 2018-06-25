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
description: Das Element IsAssignmentEditable stellt den Aufgabentyp.
ms.openlocfilehash: 91922c4d6abd4d88ac9e36dd3d4c0224fc1ee716
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829992"
---
# <a name="isassignmenteditable"></a>IsAssignmentEditable

Das Element **IsAssignmentEditable** stellt den Aufgabentyp. 
  
```xml
<IsAssignmentEditable/>
```

 **ganze Zahl**
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
|0  <br/> |Die Standardeinstellung für alle Aufgabenelemente.  <br/> |
|1  <br/> |Eine Aufgabenanfrage.  <br/> |
|2  <br/> |Die Annahme einer Aufgabe aus einem Empfänger eine Aufgabenanfrage.  <br/> |
|3  <br/> |Eine Aufgabe Ablehnung von einem Empfänger eine Aufgabenanfrage.  <br/> |
|4  <br/> |Ein Update auf eine vorherige Aufgabenanfrage.  <br/> |
|5  <br/> |Nicht verwendet.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

