---
title: Routingtype (e-mailemailtype)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RoutingType
api_type:
- schema
ms.assetid: 683216be-9972-4f48-a148-c34bfe7f53e5
description: Das Routing Type-Element definiert den Adresstyp für das Postfach.
ms.openlocfilehash: d4229f2857a5c99cc9bb7ff9b9b103de099a0055
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465086"
---
# <a name="routingtype-emailaddresstype"></a>Routingtype (e-mailemailtype)

Das **Routing** Type-Element definiert den Adresstyp für das Postfach. 
  
```XML
<RoutingType/>
```

 **NonEmptyStringType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Actingies](actingas.md) <br/> |Gibt an, wen der Anrufer sendet.  <br/> |
|[Postfach](mailbox.md) <br/> |Identifiziert eine vollständig aufgelöste e-Mail-Adresse.  <br/> |
|[RoomList](roomlist.md) <br/> |Gibt eine Liste von Besprechungsräumen an.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Wert Text stellt einen Routingtyp dar. SMTP ist der typische Textwert für dieses Element.
  
## <a name="remarks"></a>Bemerkungen

Dieses Element ist im [Post Fach](mailbox.md) Element optional. Für Verfügbarkeits Vorgänge wird ein anderes [Routing Type-Element (Email)](routingtype-emailaddress.md) verwendet. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

