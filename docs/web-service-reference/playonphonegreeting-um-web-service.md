---
title: PlayOnPhoneGreeting (um-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- PlayOnPhoneGreeting
api_type:
- schema
ms.assetid: 43eda596-3609-4e1b-8502-1db2636535cf
description: Das PlayOnPhoneGreeting-Element definiert eine Anforderung zum Abspielen einer Unified Messaging-Begrüßung auf einem Telefon.
ms.openlocfilehash: 197e4ba671e1711b73b1e7c239339db589357581
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529924"
---
# <a name="playonphonegreeting-um-web-service"></a>PlayOnPhoneGreeting (um-Webdienst)

Das **PlayOnPhoneGreeting** -Element definiert eine Anforderung zum Abspielen einer Unified Messaging-Begrüßung auf einem Telefon. 
  
[PlayOnPhoneGreeting (um-Webdienst)](playonphonegreeting-um-web-service.md)
  
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
|[Greetingtype (um-Webdienst)](greetingtype-um-web-service.md) <br/> |Definiert die Art der Begrüßung, die in einer [PlayOnPhoneGreeting-Operation (um-Webdienst)](playonphonegreeting-operation-um-web-service.md) verwendet werden soll.  <br/> |
|[Wähl Dienst (um-Webdienst)](dialstring-um-web-service.md) <br/> |Enthält den Wert für die Telefonnummer, die gewählt werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichten  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[PlayOnPhoneGreeting-Vorgang (um-Webdienst)](playonphonegreeting-operation-um-web-service.md)

