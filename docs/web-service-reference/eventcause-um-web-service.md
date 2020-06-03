---
title: EventCause (um-Webdienst)
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
description: Das EventCause-Element enthält einen Wert, der die Ursache für ein Anruf Ereignis in einer Antwort auf eine Anforderung des GetCallInfo-Vorgangs (um-Webdienst) angibt.
ms.openlocfilehash: 9d49fd4b16236d0dd87889fbbd039f2e271a5968
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458677"
---
# <a name="eventcause-um-web-service"></a>EventCause (um-Webdienst)

Das **EventCause** -Element enthält einen Wert, der die Ursache für ein Anruf Ereignis in einer Antwort auf eine Anforderung des [GetCallInfo-Vorgangs (um-Webdienst)](getcallinfo-operation-um-web-service.md) angibt. 
  
[GetCallInfoResponse (um-Webdienst)](getcallinforesponse-um-web-service.md)
  
[EventCause (um-Webdienst)](eventcause-um-web-service.md)
  
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
|[GetCallInfoResponse (um-Webdienst)](getcallinforesponse-um-web-service.md) <br/> |Definiert eine Antwort auf eine [GetCallInfo-Vorgangsanforderung (um-Webdienst)](getcallinfo-operation-um-web-service.md) .  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Im Folgenden sind die möglichen Werte aufgeführt:
  
- Keine
    
- UserBusy
    
- Noanswer
    
- Andere
    
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichten  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetCallInfo-Vorgang (um-Webdienst)](getcallinfo-operation-um-web-service.md)
  
[GetCallInfoResponse (um-Webdienst)](getcallinforesponse-um-web-service.md)

