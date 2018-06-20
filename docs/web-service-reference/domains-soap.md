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
description: Das Domänen-Element darstellt, die Domäne-Auflistung, die zurückgegeben wird, in einen GetDomainSettings-Vorgang (SOAP), die Domänen, die die Organisation in einem Vorgang GetFederationInformation (SOAP) federated hat oder die Domänen mit einer organisationsbeziehung als von GetOrganizationRelationshipSettings-Vorgang (SOAP) zurückgegeben.
ms.openlocfilehash: 7a21a3a09516de2d1c38021ca3ccd2161d9cdd1e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758098"
---
# <a name="domains-soap"></a>Domänen (SOAP)

Das **Domänen** -Element darstellt, die Domäne-Auflistung, die zurückgegeben wird, in einen [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md), die Domänen, die die Organisation in einem [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)federated hat oder die Domänen mit einer organisationsbeziehung von [GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md)zurückgegeben.
  
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
|[Domäne (SOAP)](domain-soap.md) <br/> |Stellt eine einzelne Domäne.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md) <br/> |Stellt eine Anforderung [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md) .  <br/> |
|[Antwort (GetFederationInformation) (SOAP)](response-getfederationinformationsoap.md) <br/> |Enthält die Antwort-Informationen [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md) .  <br/> |
|[GetOrganizationRelationshipSettingsRequest (SOAP)](getorganizationrelationshipsettingsrequest-soap.md) <br/> |Stellt eine Anforderung [GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md) .  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlung-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md)  
- [GetFederationInformationResponse (SOAP)](getfederationinformationresponse-soap.md)

