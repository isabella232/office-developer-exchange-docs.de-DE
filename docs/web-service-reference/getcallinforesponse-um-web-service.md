---
title: GetCallInfoResponse (UM-Webdienst)
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
description: Das GetCallInfoResponse-Element definiert eine Antwort auf eine GetCallInfo-Vorgang (UM-Webdienst) an.
ms.openlocfilehash: d9658dd9cb47f925e05dc21a8651c98dce1f0a2a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758595"
---
# <a name="getcallinforesponse-um-web-service"></a>GetCallInfoResponse (UM-Webdienst)

Das **GetCallInfoResponse** -Element definiert eine Antwort auf eine [GetCallInfo-Vorgang (UM-Webdienst)](getcallinfo-operation-um-web-service.md) an. 
  
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
|CallState  <br/> |Enthält einen Wert, der den Status eines Aufrufs angibt, für die die [GetCallInfo-Vorgang (UM-Webdienst)](getcallinfo-operation-um-web-service.md) Informationen angefordert.  <br/> |
|EventCause  <br/> |Enthält einen Wert, der angibt, die Ursache eines Ereignisses für einen Anruf für die die [GetCallInfo-Vorgang (UM-Webdienst)](getcallinfo-operation-um-web-service.md) Informationen angefordert.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichten  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetCallInfo-Vorgang (UM-Webdienst)](getcallinfo-operation-um-web-service.md)
  
[CallState (UM-Webdienst)](callstate-um-web-service.md)
  
[EventCause (UM-Webdienst)](eventcause-um-web-service.md)

