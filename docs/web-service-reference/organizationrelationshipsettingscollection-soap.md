---
title: OrganizationRelationshipSettingsCollection (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33456abf-a1b6-46da-a864-3ec8af2780de
description: Das OrganizationRelationshipSettingsCollection-Element stellt eine Liste von Organisationsbeziehungen dar, die mit der Abfrage übereinstimmen. Das OrganizationRelationshipSettingsCollection-Element ist nur für die interne Verwendung. Dieses Element wird nicht von Clients verwendet.
ms.openlocfilehash: 52f84d932e74393a844f5f55fbd1d09bfb0a5d4e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462423"
---
# <a name="organizationrelationshipsettingscollection-soap"></a>OrganizationRelationshipSettingsCollection (SOAP)

Das **OrganizationRelationshipSettingsCollection** -Element stellt eine Liste von Organisationsbeziehungen dar, die mit der Abfrage übereinstimmen. Das **OrganizationRelationshipSettingsCollection** -Element ist nur für die interne Verwendung. Dieses Element wird nicht von Clients verwendet. 
  
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
|[Antwort (GetOrganizationRelationship) (SOAP)](response-getorganizationrelationshipsoap.md) <br/> |Enthält die Antwortinformationen für den [GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md) .  <br/> |
   
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



[GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

