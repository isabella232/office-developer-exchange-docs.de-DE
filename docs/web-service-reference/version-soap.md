---
title: Version (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 47c9216e-6bfe-48c8-a27a-26f70db8e8d5
description: Das Version-Element stellt eine Beschreibung der Serverproduktversion dar.
ms.openlocfilehash: 67935bb97ce5a6faab3ae26ec03a842794d539e0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541630"
---
# <a name="version-soap"></a>Version (SOAP)

Das **Version-Element** stellt eine Beschreibung der Serverproduktversion dar. 
  
```XML
<Version/>
```

 **Zeichenfolge**
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

Der Wert des **Version-Elements** ist eine Beschreibung der Serverproduktversion. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Das **Version-Element** ist im SOAP-Header einer Antwort enthalten. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
  
[GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)
  
[GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)

