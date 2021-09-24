---
title: OofStatus (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- OofStatus
api_type:
- schema
ms.assetid: 0ba4225a-784e-4e6e-bd20-be45f0f7597c
description: Das OofStatus-Element enthält einen Wert, der den Status "Unified Messaging Out of Office" für den Benutzer ausgibt, der eine GetUMProperties-Vorgangsanforderung (UM-Webdienst) sendet.
ms.openlocfilehash: 4e899317defdb4ac4c27c3fdc17d7b7222dff6a7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539269"
---
# <a name="oofstatus-um-web-service"></a>OofStatus (UM-Webdienst)

Das **OofStatus-Element** enthält einen Wert, der den Status "Unified Messaging Out of Office" für den Benutzer zurückgibt, der eine [GetUMProperties-Vorgangsanforderung (UM-Webdienst)](getumproperties-operation-um-web-service.md) sendet. 
  
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
|[GetUMPropertiesResponse (UM-Webdienst)](getumpropertiesresponse-um-web-service.md) <br/> |Definiert eine Antwort auf eine [GetUMProperties-Vorgangsanforderung (UM-Webdienst).](getumproperties-operation-um-web-service.md)  <br/> |
   
## <a name="text-value"></a>Textwert

Ein boolescher Textwert ist erforderlich. Im Folgenden sind die möglichen Werte aufgeführt:
  
- Richtig
    
- Nicht richtig
    
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichten  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUMProperties-Vorgang (UM-Webdienst)](getumproperties-operation-um-web-service.md)
  
[GetUMPropertiesResponse (UM-Webdienst)](getumpropertiesresponse-um-web-service.md)

