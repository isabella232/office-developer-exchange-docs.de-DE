---
title: GetCallInfoResponse (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- GetCallInfoResponse
api_type:
- schema
ms.assetid: aa5196bf-f5f3-455c-94ea-304fb7920c79
description: Das GetCallInfoResponse-Element definiert eine Antwort auf eine GetCallInfo-Vorgangsanforderung (UM-Webdienst).
ms.openlocfilehash: 4b631bdee87e57c1612e906c725adabb9f9ce63e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59526189"
---
# <a name="getcallinforesponse-um-web-service"></a>GetCallInfoResponse (UM-Webdienst)

Das **GetCallInfoResponse-Element** definiert eine Antwort auf eine [GetCallInfo-Vorgangsanforderung (UM-Webdienst).](getcallinfo-operation-um-web-service.md) 
  
[GetCallInfoResponse (UM-Webdienst)](getcallinforesponse-um-web-service.md)
  
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
|CallState  <br/> |Enthält einen Wert, der den Status eines Aufrufs angibt, für den der [GetCallInfo-Vorgang (UM-Webdienst)](getcallinfo-operation-um-web-service.md) Informationen angefordert hat.  <br/> |
|EventCause  <br/> |Enthält einen Wert, der die Ursache eines Ereignisses für einen Aufruf angibt, für den der [GetCallInfo-Vorgang (UM-Webdienst)](getcallinfo-operation-um-web-service.md) Informationen angefordert hat.  <br/> |
   
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



[GetCallInfo-Vorgang (UM-Webdienst)](getcallinfo-operation-um-web-service.md)
  
[CallState (UM-Webdienst)](callstate-um-web-service.md)
  
[EventCause (UM-Webdienst)](eventcause-um-web-service.md)

