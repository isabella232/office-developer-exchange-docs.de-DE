---
title: Anforderung (GetOrganizationRelationship) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 85dc155c-fad0-4756-b9a8-dedf5040a7c6
description: Das Request-Element stellt eine SOAP-Anforderung (GetOrganizationRelationshipSettingsRequest) dar. Das Request-Element ist nur für die interne Verwendung vorgesehen. Dieses Element wird von Clients nicht verwendet.
ms.openlocfilehash: 06af9ca1067407f7fac9db3ff7c5b4e0fbe8a108
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512366"
---
# <a name="request-getorganizationrelationship-soap"></a>Anforderung (GetOrganizationRelationship) (SOAP)

Das **Request-Element** stellt eine [SOAP-Anforderung (GetOrganizationRelationshipSettingsRequest)](getorganizationrelationshipsettingsrequest-soap.md) dar. Das **Request-Element** ist nur für die interne Verwendung vorgesehen. Dieses Element wird von Clients nicht verwendet. 
  
```XML
<Request>
   <Domains/>
</Request>
```

 **GetOrganizationRelationshipSettingsRequest**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Domänen (SOAP)](domains-soap.md) <br/> |Stellt die Domänen dar, für die die AutoErmittlung ausgeführt werden soll und die in einer Abfrage verwendet werden sollen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetOrganizationRelationshipSettingsRequestMessage (SOAP)](getorganizationrelationshipsettingsrequestmessage-soap.md) <br/> |Stellt eine [SOAP-Vorgangsanforderung (GetOrganizationRelationshipSettings)](getorganizationrelationshipsettings-operation-soap.md) dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetOrganizationRelationshipSettingsRequest (SOAP)](getorganizationrelationshipsettingsrequest-soap.md)


[Arbeiten mit AutoErmittlung](https://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx)

