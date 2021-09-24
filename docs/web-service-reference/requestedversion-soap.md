---
title: RequestedVersion (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 962036c9-9b13-4669-bed2-2502c0f5aabe
description: Das RequestedVersion-Element gibt die Mindestdienstversion an, für die der Client die Anforderung verarbeiten möchte.
ms.openlocfilehash: 390dee362bf2e6c2bdeac4e0e5564ecbd59b7319
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513332"
---
# <a name="requestedversion-soap"></a>RequestedVersion (SOAP)

Das **RequestedVersion-Element** gibt die Mindestdienstversion an, für die der Client die Anforderung verarbeiten möchte. 
  
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
|[Anforderung (GetDomainSettings) (SOAP)](request-getdomainsettingssoap.md) <br/> |Stellt eine Anforderung zum Abrufen von Domäneneinstellungen dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert für das **RequestedVersion-Element** kann Exchange2010, Exchange2010_SP1, Exchange2010_SP2 oder Exchange2013 sein.
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn dieses Element nicht vorhanden ist, wird die neueste Dienstversion verwendet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
  
[GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)

