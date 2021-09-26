---
title: Anforderung (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 75696436-997e-49f1-a31b-eb9a8c3526f3
description: Das Request-Element enthält die angeforderten Konfigurationseinstellungen und die Zielbenutzer.
ms.openlocfilehash: 533419d6e622bb1d415f739868aaf30c79c41635
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542805"
---
# <a name="request-soap"></a>Anforderung (SOAP)

Das **Request-Element** enthält die angeforderten Konfigurationseinstellungen und die Zielbenutzer. 
  
```XML
<Request>
   <Users/>
   <RequestedSettings/>
   <RequestedVersion/>
</Request>
```

 **GetUserSettingsRequest**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Benutzer (SOAP)](users-soap.md) <br/> |Stellt eine Auflistung von E-Mail-Adressen der Benutzer dar, für die Einstellungen abgerufen werden sollen.  <br/> |
|[RequestedSettings (SOAP)](requestedsettings-soap.md) <br/> |Enthält die Namen der angeforderten Konfigurationseinstellungen.  <br/> |
|[RequestedVersion (SOAP)](requestedversion-soap.md) <br/> |Gibt die spezifische Serverversion an, die der Anbieter verwenden möchte.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetUserSettingsRequestMessage (SOAP)](getusersettingsrequestmessage-soap.md) <br/> |Stellt eine [SOAP-Anforderung (GetUserSettings-Vorgang)](getusersettings-operation-soap.md) dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)

