---
title: ConfigurationName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ConfigurationName
api_type:
- schema
ms.assetid: 3b524a2f-9c6b-4550-9f3d-f78d176b0f7b
description: Das ConfigurationName-Element gibt die angeforderten Dienstkonfigurationen anhand des Namens an.
ms.openlocfilehash: 39f847c256614cd0c207f440691bd87d09ed237b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523125"
---
# <a name="configurationname"></a>ConfigurationName

Das **ConfigurationName-Element** gibt die angeforderten Dienstkonfigurationen anhand des Namens an. 
  
```xml
<ConfigurationName>MailTips or UnifiedMessagingConfiguration or ProtectionRules</ConfigurationName>
```

 **ServiceConfigurationType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[RequestedConfiguration](requestedconfiguration.md) <br/> |Enthält die angeforderten Dienstkonfigurationen.  <br/> |
   
## <a name="text-value"></a>Textwert

In der folgenden Tabelle sind die möglichen Werte für das **ConfigurationName-Element** aufgeführt. 
  
**ConfigurationName-Elementwerte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|MailTips  <br/> |Identifies the MailTips service configuration.  <br/> |
|UnifiedMessagingConfiguration  <br/> |Identifiziert die Unified Messaging-Dienstkonfiguration.  <br/> |
|ProtectionRules  <br/> |Identifiziert die Dienstkonfiguration für Schutzregeln.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

