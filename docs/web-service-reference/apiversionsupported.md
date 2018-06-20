---
title: ApiVersionSupported
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d9264e74-eba7-4279-b193-af7e5130268d
description: Das ApiVersionSupported-Element enthält die Version der JavaScript-API für Office, die vom Client unterstützt.
ms.openlocfilehash: 41c3eacff65d797dfe7e8b587c50c35d8938664f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757268"
---
# <a name="apiversionsupported"></a>ApiVersionSupported

Das **ApiVersionSupported** -Element enthält die Version der JavaScript-API für Office, die vom Client unterstützt. 
  
```XML
<ApiVersionSupported />
```

 **string**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[GetAppManifests](getappmanifests.md)
  
## <a name="text-value"></a>Textwert

Der Textwert der **ApiVersionSupported** -Element enthält die Version der JavaScript-API für Office, die vom Client unterstützt. Dieser Wert gibt an, welche app Manifeste in der Antwort an den Client zurückgegeben werden sollen. 
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> | http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Nicht zutreffend  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetAppManifests](getappmanifests.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

