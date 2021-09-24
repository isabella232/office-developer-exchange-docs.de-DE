---
title: Domänen (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 5f81d1b7-c6a4-456f-9935-13d04a3d92d7
description: Das Domains-Element stellt die Domänensammlung dar, die in einem GetDomainSettings-Vorgang (SOAP) zurückgegeben wird, die Domänen, die die Organisation in einem GetFederationInformation-Vorgang (SOAP) verbunden hat, oder die Domänen mit einer Organisationsbeziehung, wie sie von der Soap (GetOrganizationRelationshipSettings)-Vorgang zurückgegeben werden.
ms.openlocfilehash: 667b2611ce8b393252f9bdda6dd7ec201b605047
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538323"
---
# <a name="domains-soap"></a>Domänen (SOAP)

Das **Domains-Element** stellt die Domänensammlung dar, die in einem [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)zurückgegeben wird, die Domänen, die die Organisation in einem [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)verbunden hat, oder die Domänen mit einer Organisationsbeziehung, wie sie vom [Soap-Vorgang (GetOrganizationRelationshipSettings)](getorganizationrelationshipsettings-operation-soap.md)zurückgegeben werden.
  
```XML
<Domains>
   <Domain/>
</Domains>
```

 **Domänen**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Domäne (SOAP)](domain-soap.md) <br/> |Stellt eine einzelne Domäne dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md) <br/> |Stellt eine [SOAP-Anforderung (GetDomainSettings-Vorgang)](getdomainsettings-operation-soap.md) dar.  <br/> |
|[Antwort (GetFederationInformation) (SOAP)](response-getfederationinformationsoap.md) <br/> |Enthält die [SOAP-Antwortinformationen (GetFederationInformation-Vorgang).](getfederationinformation-operation-soap.md)  <br/> |
|[GetOrganizationRelationshipSettingsRequest (SOAP)](getorganizationrelationshipsettingsrequest-soap.md) <br/> |Stellt eine [SOAP-Anforderung (GetOrganizationRelationshipSettings)](getorganizationrelationshipsettings-operation-soap.md) dar.  <br/> |
   
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

- [GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md)  
- [GetFederationInformationResponse (SOAP)](getfederationinformationresponse-soap.md)

