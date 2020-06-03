---
title: Domänen (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 5f81d1b7-c6a4-456f-9935-13d04a3d92d7
description: Das Domains-Element stellt die Domänen Sammlung dar, die in einem GetDomainSettings-Vorgang (SOAP), die Domänen, die die Organisation in einen GetFederationInformation-Vorgang (SOAP) integriert hat, oder die Domänen mit einer Organisationsbeziehung zurückgegeben werden, die von GetOrganizationRelationshipSettings-Vorgang (SOAP) zurückgegeben werden.
ms.openlocfilehash: c56fb72841776c0060c1300b52b2f6a06b1ec0ed
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526305"
---
# <a name="domains-soap"></a>Domänen (SOAP)

Das **Domains** -Element stellt die Domänen Sammlung dar, die in einem [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md), die Domänen, die die Organisation in einen [GetFederationInformation-Vorgang (](getfederationinformation-operation-soap.md)SOAP) integriert hat, oder die Domänen mit einer Organisationsbeziehung zurückgegeben werden, die von [GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md)zurückgegeben werden.
  
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
|[GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md) <br/> |Stellt eine [SOAP-Anforderung (GetDomainSettings Operation)](getdomainsettings-operation-soap.md) dar.  <br/> |
|[Antwort (GetFederationInformation) (SOAP)](response-getfederationinformationsoap.md) <br/> |Enthält die Antwortinformationen für den [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md) .  <br/> |
|[GetOrganizationRelationshipSettingsRequest (SOAP)](getorganizationrelationshipsettingsrequest-soap.md) <br/> |Stellt eine [SOAP-Anforderung (GetOrganizationRelationshipSettings Operation)](getorganizationrelationshipsettings-operation-soap.md) dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |Auto Ermittlungs Schema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md)  
- [GetFederationInformationResponse (SOAP)](getfederationinformationresponse-soap.md)

