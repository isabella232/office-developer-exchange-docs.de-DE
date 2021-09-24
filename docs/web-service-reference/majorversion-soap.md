---
title: MajorVersion (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 0b2a83cf-e173-4073-9603-b2ea3b36ec1a
description: Das MajorVersion-Element stellt die Hauptversionsnummer für den Server dar.
ms.openlocfilehash: eb6bed958e36cbd3c0c35825ff10d857ea839cff
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511096"
---
# <a name="majorversion-soap"></a>MajorVersion (SOAP)

Das **MajorVersion-Element** stellt die Hauptversionsnummer für den Server dar. 
  
```XML
<MajorVersion/>
```

 **int**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ServerVersionInfo (SOAP)](serverversioninfo-soap.md) <br/> |Enthält die Version des Servers, der die Anforderung verarbeitet hat.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert für das **MajorVersion-Element** ist eine ganze Zahl, die die Hauptversionsnummer des Servers darstellt, der die Anforderung verarbeitet hat. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
  
[GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)

