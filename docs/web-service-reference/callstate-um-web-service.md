---
title: CallState (um-Webdienst)
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
description: Das CallState-Element enthält einen Wert, der den Status eines Anrufs angibt.
ms.openlocfilehash: 44614c460286ff49ebc2373263c1827c6be5cc08
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44454610"
---
# <a name="callstate-um-web-service"></a>CallState (um-Webdienst)

Das **CallState** -Element enthält einen Wert, der den Status eines Anrufs angibt. 
  
[GetCallInfoResponse (um-Webdienst)](getcallinforesponse-um-web-service.md)
  
[CallState (um-Webdienst)](callstate-um-web-service.md)
  
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
|[GetCallInfoResponse (um-Webdienst)](getcallinforesponse-um-web-service.md) <br/> |Definiert eine Antwort auf einen [GetCallInfo-Vorgang (um-Webdienst)](getcallinfo-operation-um-web-service.md).  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Im Folgenden sind die möglichen Werte aufgeführt:
  
- Leerlauf
    
- Verbindung wird hergestellt
    
- Alarmiert
    
- Verbunden
    
- Disconnected
    
- Eingehende
    
- Transfer
    
- Weiterleitungs
    
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/message  <br/> |
|Name des Schemas  <br/> |Nachrichten  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetCallInfo-Vorgang (um-Webdienst)](getcallinfo-operation-um-web-service.md)
  
[GetCallInfoResponse (um-Webdienst)](getcallinforesponse-um-web-service.md)

