---
title: DeliveryReportEnabled (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 2ab522bc-40ea-4e43-aa57-6d2562db35e9
description: Das DeliveryReportEnabled-Element stellt das DeliveryReportEnabled()-Flag dar. Das DeliveryReportEnabled-Element ist nur für die interne Verwendung vorgesehen. Dieses Element wird von Clients nicht verwendet.
ms.openlocfilehash: 95fe62e25ca871171b398b17f3d03dff9235001b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510169"
---
# <a name="deliveryreportenabled-soap"></a>DeliveryReportEnabled (SOAP)

Das **DeliveryReportEnabled-Element** stellt das **DeliveryReportEnabled()-Flag** dar. Das **DeliveryReportEnabled-Element** ist nur für die interne Verwendung vorgesehen. Dieses Element wird von Clients nicht verwendet. 
  
```XML
<DeliveryReportEnabled>true | false</DeliveryReportEnabled>
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

Der Textwert "true" für das DeliveryReportEnabled-Element gibt an, dass die Übermittlungsberichte von Benutzern in der Organisation verwendet werden können. Der Wert "false" gibt an, dass die Übermittlungsberichte unterdrückt werden sollen.
  
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie dieses Element, um Übermittlungsberichte vom Server zuzulassen oder zu unterdrücken.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

