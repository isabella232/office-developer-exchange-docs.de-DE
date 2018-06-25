---
title: DomainNames (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 79ffc3f9-25c4-40b5-84ce-09a3c5f892fa
description: Das Element DomainNames stellt die Domain Names-Auflistung dar. Das DomainNames-Element ist nur zur internen Verwendung. Dieses Element wird von Clients nicht verwendet.
ms.openlocfilehash: 45d256f3d5a57028a04572ad67d4be0786ca39e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758089"
---
# <a name="domainnames-soap"></a>DomainNames (SOAP)

Das Element **DomainNames** stellt die Domain Names-Auflistung dar. Das **DomainNames** -Element ist nur zur internen Verwendung. Dieses Element wird von Clients nicht verwendet. 
  
```XML
<DomainNames>
    <Domains/>
</DomainNames>
```

 **DomainNames**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Domänen (SOAP)](domains-soap.md) <br/> |Stellt eine Sammlung von Domänen, die von den [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md), [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)oder den [GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md)zurückgegeben werden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[OrganizationRelationshipSettings (SOAP)](organizationrelationshipsettings-soap.md) <br/> |Stellt eine Liste von organisationsbeziehungen für eine einzelne Organisation.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Dieses Element stellt die SMTP-Domänen der externen Organisationen.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlung-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

