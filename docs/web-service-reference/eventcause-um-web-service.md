---
title: EventCause (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- EventCause
api_type:
- schema
ms.assetid: 7b3c1db8-cad4-4050-a50d-b06f065db530
description: Das EventCause-Element enthält einen Wert, der angibt, die Ursache für ein Aufrufereignis in eine Antwort auf eine GetCallInfo-Vorgang (UM-Webdienst) an.
ms.openlocfilehash: dd73d93527bebb3b522ad0a6cdae5b9faee1a6a9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758277"
---
# <a name="eventcause-um-web-service"></a>EventCause (UM-Webdienst)

Das **EventCause** -Element enthält einen Wert, der die Ursache für einen Anruf-Ereignis in einer Antwort auf eine Anforderung [GetCallInfo-Vorgang (UM-Webdienst)](getcallinfo-operation-um-web-service.md) angibt. 
  
[GetCallInfoResponse (UM-Webdienst)](getcallinforesponse-um-web-service.md)
  
[EventCause (UM-Webdienst)](eventcause-um-web-service.md)
  
```xml
<GetCallInfoResponse>
  <EventCause/>
</GetCallInfoResponse>
```

 **UMEventCause**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetCallInfoResponse (UM-Webdienst)](getcallinforesponse-um-web-service.md) <br/> |Definiert eine Antwort auf eine [GetCallInfo-Vorgang (UM-Webdienst)](getcallinfo-operation-um-web-service.md) an.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Im Folgenden sind die möglichen Werte aufgeführt:
  
- Keine
    
- UserBusy
    
- NoAnswer
    
- Andere
    
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichten  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetCallInfo-Vorgang (UM-Webdienst)](getcallinfo-operation-um-web-service.md)
  
[GetCallInfoResponse (UM-Webdienst)](getcallinforesponse-um-web-service.md)

