---
title: FreeBusyAccessEnabled (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 8d2d3276-b180-424e-a707-7256d14a1776
description: Das FreeBusyAccessEnabled-Element stellt das FreeBusyAccessEnabled()-Flag dar. Das FreeBusyAccessEnabled-Element ist nur für die interne Verwendung vorgesehen. Dieses Element wird von Clients nicht verwendet.
ms.openlocfilehash: faf51798ba211b4219a3f2abee3b3e5e9ce4ab29
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59530216"
---
# <a name="freebusyaccessenabled-soap"></a>FreeBusyAccessEnabled (SOAP)

Das **FreeBusyAccessEnabled-Element** stellt das **FreeBusyAccessEnabled()-Flag** dar. Das **FreeBusyAccessEnabled-Element** ist nur für die interne Verwendung vorgesehen. Dieses Element wird von Clients nicht verwendet. 
  
```XML
<FreeBusyAccessEnabled>true | false</FreeBusyAccessEnabled>
```

 **Boolescher Wert**
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

Der Textwert **"true"** für das **FreeBusyAccessEnabled-Element** gibt an, dass die Freigabebeziehung verwendet werden soll, um Frei/Gebucht-Informationen von Benutzern in der Organisation abzurufen. Der Wert **"false"** gibt an, dass die Freigabebeziehung unterdrückt werden soll. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie dieses Element, um Frei/Gebucht-Informationen vom Server zuzulassen oder zu unterdrücken. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

