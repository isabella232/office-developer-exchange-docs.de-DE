---
title: DeleteItemField
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteItemField
api_type:
- schema
ms.assetid: 3893be6a-49a7-49f6-bf53-c7f819ec3f87
description: Das DeleteItemField-Element stellt einen Vorgang zum Löschen einer bestimmten Eigenschaft aus einem Element während eines Anrufs UpdateItem dar.
ms.openlocfilehash: 2388bd10379211a31890b7c4f27920431ce444c8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757928"
---
# <a name="deleteitemfield"></a>DeleteItemField

Das **DeleteItemField** -Element stellt einen Vorgang zum Löschen einer bestimmten Eigenschaft aus einem Element während eines Anrufs UpdateItem dar. 
 
- [UpdateItem](updateitem.md)  
- [ItemChanges](itemchanges.md) 
- [ItemChange](itemchange.md) 
- [Updates (Element)](updates-item.md) 
- [DeleteItemField](deleteitemfield.md)
  
```xml
<DeleteItemField>
   <FieldURI/>
</DeleteItemField>
```

 **DeleteItemFieldType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifiziert die Eigenschaften von URI häufig verwiesen wird.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Einzelne Mitglieder einer Wörterbuch-Eigenschaft identifiziert.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifiziert extended MAPI-Eigenschaften.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Updates (Element)](updates-item.md) <br/> |Enthält eine Reihe von Elementen, definieren anfügen, festlegen und Löschen von Änderungen an Elementeigenschaften.  <br/><br/>Es folgt der XPath-Ausdruck, der dieses Element:<br/>`/UpdateItem/ItemChanges/ItemChange[i]/Updates` <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typen-schema  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [UpdateItem Operation](updateitem-operation.md)

