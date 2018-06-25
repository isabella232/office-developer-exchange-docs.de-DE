---
title: RequestedVersion (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 962036c9-9b13-4669-bed2-2502c0f5aabe
description: Das RequestedVersion-Element gibt die minimale Service-Version, die der Client die Anforderung auf verarbeitet werden möchte.
ms.openlocfilehash: 0d8682c33790d2d26001512ad9e2191ae52074d0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831134"
---
# <a name="requestedversion-soap"></a>RequestedVersion (SOAP)

Das **RequestedVersion** -Element gibt die minimale Service-Version, die der Client die Anforderung auf verarbeitet werden möchte. 
  
```XML
<RequestedVersion/>
```

 **ExchangeVersion**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Anforderung (SOAP)](request-soap.md) <br/> |Enthält die angeforderten Konfigurationseinstellungen und die Zielbenutzer.  <br/> |
|[Anforderung (GetDomainSettings) (SOAP)](request-getdomainsettingssoap.md) <br/> |Stellt eine Anforderung an die domäneneinstellungen abrufen.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert für das **RequestedVersion** -Element kann Exchange2010, Exchange2010_SP1, Exchange2010_SP2 oder Exchange2013 sein.
  
## <a name="remarks"></a>Hinweise

Wenn dieses Element nicht vorhanden ist, wird die neueste Service Version verwendet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlung-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
  
[GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)

