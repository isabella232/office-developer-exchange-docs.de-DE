---
title: RoutingType (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RoutingType
api_type:
- schema
ms.assetid: 683216be-9972-4f48-a148-c34bfe7f53e5
description: Das RoutingType-Element definiert den Adresstyp für das Postfach.
ms.openlocfilehash: fdbe40bd74debe517739e0fe0c47ed108bd614c6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509367"
---
# <a name="routingtype-emailaddresstype"></a>RoutingType (EmailAddressType)

Das **RoutingType-Element** definiert den Adresstyp für das Postfach. 
  
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
|[ActingAs](actingas.md) <br/> |Gibt an, an wen der Anrufer gesendet wird.  <br/> |
|[Postfach](mailbox.md) <br/> |Identifiziert eine vollständig aufgelöste E-Mail-Adresse.  <br/> |
|[RoomList](roomlist.md) <br/> |Identifiziert eine Liste von Besprechungsräumen.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt einen Routingtyp dar. SMTP ist der typische Textwert für dieses Element.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element ist optional im [Mailbox-Element.](mailbox.md) Ein weiteres [RoutingType-Element (EmailAddress)](routingtype-emailaddress.md) wird für Verfügbarkeitsvorgänge verwendet. 
  
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

