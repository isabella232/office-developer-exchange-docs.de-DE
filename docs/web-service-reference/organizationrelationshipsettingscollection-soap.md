---
title: OrganizationRelationshipSettingsCollection (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 33456abf-a1b6-46da-a864-3ec8af2780de
description: Das OrganizationRelationshipSettingsCollection-Element stellt eine Liste der Organisationsbeziehungen dar, die der Abfrage entsprechen. Das OrganizationRelationshipSettingsCollection-Element ist nur für die interne Verwendung vorgesehen. Dieses Element wird von Clients nicht verwendet.
ms.openlocfilehash: e3bb4c21e77bc22af051c63b714aaaef4d883609
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514235"
---
# <a name="organizationrelationshipsettingscollection-soap"></a>OrganizationRelationshipSettingsCollection (SOAP)

Das **OrganizationRelationshipSettingsCollection-Element** stellt eine Liste der Organisationsbeziehungen dar, die der Abfrage entsprechen. Das **OrganizationRelationshipSettingsCollection-Element** ist nur für die interne Verwendung vorgesehen. Dieses Element wird von Clients nicht verwendet. 
  
```XML
<OrganizationRelationshipSettingsCollection>
   <OrganizationRelationshipSettings/>
</OrganizationRelationshipSettingsCollection>
```

 **OrganizationRelationshipSettingsCollection**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[OrganizationRelationshipSettings (SOAP)](organizationrelationshipsettings-soap.md) <br/> |Stellt die Liste der Organisationsbeziehungen für die ausgewählte Organisation und SMTP-Adressen dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Antwort (GetOrganizationRelationship) (SOAP)](response-getorganizationrelationshipsoap.md) <br/> |Enthält die [SOAP-Antwortinformationen (GetOrganizationRelationshipSettings-Vorgang).](getorganizationrelationshipsettings-operation-soap.md)  <br/> |
   
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



[GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

