---
title: Status (UM-Webdienst – SetOofStatus)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- Status
api_type:
- schema
ms.assetid: 893bcff1-ccdc-493f-b366-ce8a68c813bd
description: Das Status-Element definiert den Wert, der in einer SetOofStatus-Vorgangsanforderung (UM-Webdienst) verwendet werden soll.
ms.openlocfilehash: fc4806e4978ae51ec6113ff8fd45da7db223a071
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546938"
---
# <a name="status-um-web-service---setoofstatus"></a>Status (UM-Webdienst – SetOofStatus)

Das **Status-Element** definiert den Wert, der in einer [SetOofStatus-Vorgangsanforderung (UM-Webdienst)](setoofstatus-operation-um-web-service.md) verwendet werden soll. 
  
[SetOofStatus (UM-Webdienst)](setoofstatus-um-web-service.md)
  
[Status (UM-Webdienst – SetOofStatus)](status-um-web-servicesetoofstatus.md)
  
```xml
<SetOofStatus>
  <status/>
</SetOofStatus>
```

 **Boolescher Wert**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SetOofStatus (UM-Webdienst)](setoofstatus-um-web-service.md) <br/> |Definiert eine Anforderung zum Festlegen des OOF-Status (Unified Messaging Out of Office) für den Benutzer, der die Anforderung sendet.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein boolescher Wert ist erforderlich. Im Folgenden sind die möglichen Werte aufgeführt:
  
- Richtig
    
- False
    
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichten  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SetOofStatus-Vorgang (UM-Webdienst)](setoofstatus-operation-um-web-service.md)

