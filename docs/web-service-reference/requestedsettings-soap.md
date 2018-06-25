---
title: RequestedSettings (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 8d713d22-580c-49a5-99f5-ee532443e89a
description: Das RequestedSettings-Element enthält die Namen der angeforderten Konfigurationseinstellungen für die.
ms.openlocfilehash: 025f86d417ea2041a3247ac67b065d75c8f75599
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831136"
---
# <a name="requestedsettings-soap"></a>RequestedSettings (SOAP)

Das **RequestedSettings** -Element enthält die Namen der angeforderten Konfigurationseinstellungen für die. 
  
```XML
<RequestedSettings>
   <Setting/>
</RequestedSettings>
```

 **RequestedSettings**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Einstellung (SOAP)](setting-soap.md) <br/> |Stellt eine Konfigurationseinstellung zurückgegeben werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetUserSettingsRequest (SOAP)](getusersettingsrequest-soap.md) <br/> |Stellt eine Anforderung an die angegebene Einstellungen für einen oder mehrere Benutzer abzurufen.  <br/> |
|[Anforderung (SOAP)](request-soap.md) <br/> |Enthält die angeforderten Konfigurationseinstellungen und die Zielbenutzer.  <br/> |
|[GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md) <br/> |Stellt eine Anforderung [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md) .  <br/> |
   
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlung-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
  
[GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)

