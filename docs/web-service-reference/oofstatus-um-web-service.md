---
title: OofStatus (um-Webdienst)
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
description: Das OofStatus-Element enthält einen Wert, der den Abwesenheitsstatus des Unified Messaging-Diensts für den Benutzer angibt, der einen GetUMProperties-Vorgang (um-Webdienst) anfordert.
ms.openlocfilehash: 80b1d5aa508579eec14637ed10c322b5fbb670da
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460575"
---
# <a name="oofstatus-um-web-service"></a>OofStatus (um-Webdienst)

Das **OofStatus** -Element enthält einen Wert, der den Abwesenheitsstatus des Unified Messaging-Diensts für den Benutzer angibt, der einen [GetUMProperties-Vorgang (um-Webdienst)](getumproperties-operation-um-web-service.md) anfordert. 
  
[GetUMPropertiesResponse (um-Webdienst)](getumpropertiesresponse-um-web-service.md)
  
[OofStatus (um-Webdienst)](oofstatus-um-web-service.md)
  
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
|[GetUMPropertiesResponse (um-Webdienst)](getumpropertiesresponse-um-web-service.md) <br/> |Definiert eine Antwort auf eine [GetUMProperties-Vorgangsanforderung (um-Webdienst)](getumproperties-operation-um-web-service.md) .  <br/> |
   
## <a name="text-value"></a>Textwert

Ein boolescher Textwert ist erforderlich. Im Folgenden sind die möglichen Werte aufgeführt:
  
- Wahr
    
- Falsch
    
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichten  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUMProperties-Vorgang (um-Webdienst)](getumproperties-operation-um-web-service.md)
  
[GetUMPropertiesResponse (um-Webdienst)](getumpropertiesresponse-um-web-service.md)

