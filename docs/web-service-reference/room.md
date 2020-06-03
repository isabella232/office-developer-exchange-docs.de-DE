---
title: Raum
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Room
api_type:
- schema
ms.assetid: a2cde8b8-2d31-4ebf-8171-f4dfd650d079
description: Das Room-Element stellt einen Besprechungsraum dar.
ms.openlocfilehash: 3d5d587853e435016fdff6b9d268892a35fea825
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460533"
---
# <a name="room"></a>Raum

Das **Room** -Element stellt einen Besprechungsraum dar. 
  
[Chatrooms](rooms.md)
  
[Raum](room.md)
  
```XML
<Room>
   <Id/>
</Room>
```

 **Zimmertyp**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ID (e-mailemailtype)](id-emailaddresstype.md) <br/> |Ein Bezeichner, der eine e-Mail-Adresse und einen Anzeigenamen enthält, der den Besprechungsraum darstellt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Chatrooms](rooms.md) <br/> |Definiert eine Liste von Besprechungsräumen, die einem gemeinsamen Feature zugeordnet sind, beispielsweise sich im selben Gebäude befinden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetRooms-Vorgang](getrooms-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

