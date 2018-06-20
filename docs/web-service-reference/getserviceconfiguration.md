---
title: GetServiceConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetServiceConfiguration
api_type:
- schema
ms.assetid: acbb29e4-d853-4302-8e32-7018775d54e4
description: Das GetServiceConfiguration-Element definiert eine GetServiceConfiguration-Anforderung.
ms.openlocfilehash: 7ff7124ff062f21a02fc69b86b7cc7367ba3fcb6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829666"
---
# <a name="getserviceconfiguration"></a>GetServiceConfiguration

Das **GetServiceConfiguration** -Element definiert eine GetServiceConfiguration-Anforderung. 
  
```XML
<GetServiceConfiguration>
   <ActingAs/>
   <RequestedConfiguration/>
</GetServiceConfiguration>
```

 **GetServiceConfigurationType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ActingAs](actingas.md) <br/> |Identifiziert, die der Anrufer als sendet. Dieses Element ist optional. Wenn dieses Element nicht vorhanden ist, wird davon ausgegangen, dass der authentifizierte Benutzer die Absender werden. Das **ActingAs** -Element muss für die Anforderung des Absenders Hinweise eingeschlossen werden. Fehler ErrorInvalidArgument kann in einer Antwort zurückgegeben werden soll, wenn das **ActingAs** -Element nicht vorhanden ist, enthält keine Routingtyp, eine e-Mail-Adresse nicht umfasst, eine ungültige e-Mail-Adresse enthält, nicht an einen Benutzer in Active Directory-Domäne löst Services (AD DS), oder auf mehrere Benutzer in AD DS aufgelöst wird.  <br/> |
|[RequestedConfiguration](requestedconfiguration.md) <br/> |Enthält die Konfigurationen für den angeforderten Dienst. Dieses Element ist erforderlich.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

