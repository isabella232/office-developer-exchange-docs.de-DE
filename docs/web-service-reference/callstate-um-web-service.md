---
title: CallState (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- CallState
api_type:
- schema
ms.assetid: 88670707-12f7-41c5-ac81-dda0c354a2cb
description: Das CallState-Element enthält einen Wert, der den Status eines Aufrufs angibt.
ms.openlocfilehash: 9435124e98cfb75beab5917c1e832096ca193e0c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519968"
---
# <a name="callstate-um-web-service"></a>CallState (UM-Webdienst)

Das **CallState-Element** enthält einen Wert, der den Status eines Aufrufs angibt. 
  
[GetCallInfoResponse (UM-Webdienst)](getcallinforesponse-um-web-service.md)
  
[CallState (UM-Webdienst)](callstate-um-web-service.md)
  
```xml
<CallState/>
```

 **UMCallState**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetCallInfoResponse (UM-Webdienst)](getcallinforesponse-um-web-service.md) <br/> |Definiert eine Antwort auf einen [GetCallInfo-Vorgang (UM-Webdienst).](getcallinfo-operation-um-web-service.md)  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Im Folgenden sind die möglichen Werte aufgeführt:
  
- Im leerlauf
    
- Verbindung wird hergestellt
    
- Alarmiert
    
- Verbunden
    
- Disconnected
    
- Eingehende
    
- Übertragen
    
- Weiterleitung
    
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/message  <br/> |
|Name des Schemas  <br/> |Nachrichten  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetCallInfo-Vorgang (UM-Webdienst)](getcallinfo-operation-um-web-service.md)
  
[GetCallInfoResponse (UM-Webdienst)](getcallinforesponse-um-web-service.md)

