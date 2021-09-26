---
title: PlayOnPhoneGreeting (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- PlayOnPhoneGreeting
api_type:
- schema
ms.assetid: 43eda596-3609-4e1b-8502-1db2636535cf
description: Das PlayOnPhoneGreeting-Element definiert eine Anforderung zum Wiedergeben einer Unified Messaging-Begrüßung auf einem Telefon.
ms.openlocfilehash: e3b6a7720be6d046a379af460adbcc88725c0ea3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543121"
---
# <a name="playonphonegreeting-um-web-service"></a>PlayOnPhoneGreeting (UM-Webdienst)

Das **PlayOnPhoneGreeting-Element** definiert eine Anforderung zum Wiedergeben einer Unified Messaging-Begrüßung auf einem Telefon. 
  
[PlayOnPhoneGreeting (UM-Webdienst)](playonphonegreeting-um-web-service.md)
  
```xml
<PlayOnPhoneGreeting>
  <GreetingType/>
  <DialString/>
</PlayOnPhoneGreeting>
```

 **complexType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GreetingType (UM-Webdienst)](greetingtype-um-web-service.md) <br/> |Definiert den Typ der Begrüßung, die in einer [PlayOnPhoneGreeting-Vorgangsanforderung (UM-Webdienst)](playonphonegreeting-operation-um-web-service.md) verwendet werden soll.  <br/> |
|[dialString (UM-Webdienst)](dialstring-um-web-service.md) <br/> |Enthält den Wert für die zu wählende Telefonnummer.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine
  
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichten  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[PlayOnPhoneGreeting-Vorgang (UM-Webdienst)](playonphonegreeting-operation-um-web-service.md)

