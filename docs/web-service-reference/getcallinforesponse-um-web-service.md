---
title: GetCallInfoResponse (um-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- GetCallInfoResponse
api_type:
- schema
ms.assetid: aa5196bf-f5f3-455c-94ea-304fb7920c79
description: Das GetCallInfoResponse-Element definiert eine Antwort auf eine Anforderung des GetCallInfo-Vorgangs (um-Webdienst).
ms.openlocfilehash: 6e54ec61a9a5ebecd96bbd39dad68f8cc011b8a1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461205"
---
# <a name="getcallinforesponse-um-web-service"></a>GetCallInfoResponse (um-Webdienst)

Das **GetCallInfoResponse** -Element definiert eine Antwort auf eine Anforderung des [GetCallInfo-Vorgangs (um-Webdienst)](getcallinfo-operation-um-web-service.md) . 
  
[GetCallInfoResponse (um-Webdienst)](getcallinforesponse-um-web-service.md)
  
```xml
<GetCallInfoResponse>
  <CallState/>
  <EventCause/>
</GetCallInfoResponse>
```

 **UMCallInfo**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|CallState  <br/> |Enthält einen Wert, der den Status eines Anrufs angibt, für den der [GetCallInfo-Vorgang (um-Webdienst)](getcallinfo-operation-um-web-service.md) Informationen angefordert hat.  <br/> |
|EventCause  <br/> |Enthält einen Wert, der die Ursache eines Ereignisses für einen Anruf angibt, für den der [GetCallInfo-Vorgang (um-Webdienst)](getcallinfo-operation-um-web-service.md) Informationen angefordert hat.  <br/> |
   
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



[GetCallInfo-Vorgang (um-Webdienst)](getcallinfo-operation-um-web-service.md)
  
[CallState (um-Webdienst)](callstate-um-web-service.md)
  
[EventCause (um-Webdienst)](eventcause-um-web-service.md)

