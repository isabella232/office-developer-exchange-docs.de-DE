---
title: TargetAutodiscoverEpr (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: fdb9cc7a-cf0a-431b-9f6f-5f1db1792db7
description: Das TargetAutodiscoverEpr-Element stellt die TargetAutodiscoverEpr-Eigenschaft dar. Das TargetAutodiscoverEpr-Element ist nur für die interne Verwendung vorgesehen. Dieses Element wird von Clients nicht verwendet.
ms.openlocfilehash: f49d7b0acc59d638f2fca993ec7d8f182cd7380a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545804"
---
# <a name="targetautodiscoverepr-soap"></a>TargetAutodiscoverEpr (SOAP)

Das **TargetAutodiscoverEpr-Element** stellt die **TargetAutodiscoverEpr-Eigenschaft** dar. Das **TargetAutodiscoverEpr-Element** ist nur für die interne Verwendung vorgesehen. Dieses Element wird von Clients nicht verwendet. 
  
```XML
<TargetAutodiscoverEpr/>
```

 **anyURI**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[OrganizationRelationshipSettings (SOAP)](organizationrelationshipsettings-soap.md) <br/> |Stellt eine Liste der Organisationsbeziehungen für eine einzelne Organisation dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert für dieses Element ist ein Uniform Resource Identifier (URI) für die Organisationsbeziehung.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element gibt die AutoErmittlungs-URL des Servers für die externe Organisation an. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

