---
title: OldItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OldItemId
api_type:
- schema
ms.assetid: fb57deee-9cc3-4730-9805-ff34f39e3ab7
description: Das OldItemId-Element enthält den eindeutigen Bezeichner des Elements, das kopiert oder verschoben wurde.
ms.openlocfilehash: 9fab14478ffbb2dd8ad013d59520af943584f2eb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467466"
---
# <a name="olditemid"></a>OldItemId

Das **OldItemId** -Element enthält den eindeutigen Bezeichner des Elements, das kopiert oder verschoben wurde. 
  
```xml
<OldItemId Id="" ChangeKey=""/>
```

 **Itemidtype**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Id** <br/> |Enthält eine Zeichenfolge, die ein Element in der Exchange-Informationsspeicher identifiziert. Dieses Attribut ist erforderlich.  <br/> |
|**ChangeKey** <br/> |Enthält eine Zeichenfolge, die eine Version eines Elements identifiziert, das durch das ID-Attribut identifiziert wird. Dieses Attribut ist optional. Verwenden Sie dieses Attribut, um sicherzustellen, dass die richtige Version eines Elements verwendet wird.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CopiedEvent](copiedevent.md) <br/> |Stellt ein Ereignis dar, in dem ein Element oder ein Ordner kopiert wird.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Stellt ein Ereignis dar, in dem ein Element oder ein Ordner von einem übergeordneten Ordner in einen anderen übergeordneten Ordner verschoben wird.  <br/> |
   
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



[Vorgang abonnieren](subscribe-operation.md)
  
[GetEvents-Vorgang](getevents-operation.md)
  
[Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

