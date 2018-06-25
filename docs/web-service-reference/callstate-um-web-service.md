---
title: CallState (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- CallState
api_type:
- schema
ms.assetid: 88670707-12f7-41c5-ac81-dda0c354a2cb
description: Das CallState-Element enthält einen Wert, der den Status eines Aufrufs angibt.
ms.openlocfilehash: e751c2e38783c6634a44d8e1b830a9224cdf300a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757547"
---
# <a name="callstate-um-web-service"></a>CallState (UM-Webdienst)

Das **CallState** -Element enthält einen Wert, der den Status eines Aufrufs angibt. 
  
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
|[GetCallInfoResponse (UM-Webdienst)](getcallinforesponse-um-web-service.md) <br/> |Definiert eine Antwort auf eine [GetCallInfo-Vorgang (UM-Webdienst)](getcallinfo-operation-um-web-service.md).  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Im Folgenden sind die möglichen Werte aufgeführt:
  
- Im Leerlauf
    
- Connecting
    
- Benachrichtigt
    
- Verbunden
    
- Verbindung getrennt
    
- Eingehend
    
- Übertragen von
    
- Weiterleitung
    
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/message  <br/> |
|Name des Schemas  <br/> |Nachrichten  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetCallInfo-Vorgang (UM-Webdienst)](getcallinfo-operation-um-web-service.md)
  
[GetCallInfoResponse (UM-Webdienst)](getcallinforesponse-um-web-service.md)

