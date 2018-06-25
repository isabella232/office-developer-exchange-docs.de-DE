---
title: OofStatus (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- OofStatus
api_type:
- schema
ms.assetid: 0ba4225a-784e-4e6e-bd20-be45f0f7597c
description: Das OofStatus-Element enthält einem Wert, Indicaties der Unified Messaging nicht im Büro Status für den Benutzer, der eine GetUMProperties-Vorgang (UM-Webdienst) Anforderung gesendet hat.
ms.openlocfilehash: 1fe358a8bfea3c509220d6705a238ae832de37e8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830650"
---
# <a name="oofstatus-um-web-service"></a>OofStatus (UM-Webdienst)

Das **OofStatus** -Element enthält einen Wert, Indicaties der Unified Messaging nicht im Büro Status für den Benutzer, der eine [GetUMProperties-Vorgang (UM-Webdienst)](getumproperties-operation-um-web-service.md) Anforderung gesendet hat. 
  
[GetUMPropertiesResponse (UM-Webdienst)](getumpropertiesresponse-um-web-service.md)
  
[OofStatus (UM-Webdienst)](oofstatus-um-web-service.md)
  
```xml
<GetUMPropertiesResponse>
    <OofStatus/>
  <MissedCallNotificationEnabled/>
  <PlayOnPhoneDialString/>
  <TelephoneAccessNumbers/>
  <TelephoneAccessFolderEmail/>
</GetUMPropertiesResponse>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetUMPropertiesResponse (UM-Webdienst)](getumpropertiesresponse-um-web-service.md) <br/> |Definiert eine Antwort auf eine [GetUMProperties-Vorgang (UM-Webdienst)](getumproperties-operation-um-web-service.md) an.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Boolean-Textwert ist erforderlich. Im Folgenden sind die möglichen Werte aufgeführt:
  
- True
    
- False
    
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichten  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUMProperties-Vorgang (UM-Webdienst)](getumproperties-operation-um-web-service.md)
  
[GetUMPropertiesResponse (UM-Webdienst)](getumpropertiesresponse-um-web-service.md)

