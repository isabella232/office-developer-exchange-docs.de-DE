---
title: TargetAutodiscoverEpr (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fdb9cc7a-cf0a-431b-9f6f-5f1db1792db7
description: Das TargetAutodiscoverEpr-Element stellt die TargetAutodiscoverEpr-Eigenschaft dar. Das TargetAutodiscoverEpr-Element ist nur für die interne Verwendung. Dieses Element wird nicht von Clients verwendet.
ms.openlocfilehash: f8609f61021d5701f7a8fa2590a85824caf296c6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530289"
---
# <a name="targetautodiscoverepr-soap"></a>TargetAutodiscoverEpr (SOAP)

Das **TargetAutodiscoverEpr** -Element stellt die **TargetAutodiscoverEpr** -Eigenschaft dar. Das **TargetAutodiscoverEpr** -Element ist nur für die interne Verwendung. Dieses Element wird nicht von Clients verwendet. 
  
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
|[OrganizationRelationshipSettings (SOAP)](organizationrelationshipsettings-soap.md) <br/> |Stellt eine Liste von Organisationsbeziehungen für eine einzelne Organisation dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert für dieses Element ist ein URI (Uniform Resource Identifier) für die Organisationsbeziehung.
  
## <a name="remarks"></a>Bemerkungen

Dieses Element gibt die Auto Ermittlungs-URL des Servers für die externe Organisation an. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |Auto Ermittlungs Schema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

