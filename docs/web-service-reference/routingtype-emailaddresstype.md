---
title: RoutingType (EmailAddressType)
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
description: Das RoutingType-Element definiert den Adresstyp für das Postfach.
ms.openlocfilehash: a02c3b5711a657311428d67cccabd9c8c231db67
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831256"
---
# <a name="routingtype-emailaddresstype"></a>RoutingType (EmailAddressType)

Das **RoutingType** -Element definiert den Adresstyp für das Postfach. 
  
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
|[ActingAs](actingas.md) <br/> |Identifiziert, die der Anrufer als sendet.  <br/> |
|[Postfach](mailbox.md) <br/> |Identifiziert eine vollständig aufgelöster E-mail-Adresse.  <br/> |
|[RoomList](roomlist.md) <br/> |Eine Liste der Besprechungsräumen identifiziert.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert darstellt einen routing Typ. SMTP ist der typische Textwert für dieses Element.
  
## <a name="remarks"></a>Hinweise

Dieses Element ist optional im [Postfach](mailbox.md) -Element. Ein anderes [RoutingType (EmailAddress)](routingtype-emailaddress.md) -Element wird für Verfügbarkeit Operationen verwendet. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

