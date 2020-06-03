---
title: FreeBusyAccessEnabled (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8d2d3276-b180-424e-a707-7256d14a1776
description: Das FreeBusyAccessEnabled-Element stellt das FreeBusyAccessEnabled ()-Flag dar. Das FreeBusyAccessEnabled-Element ist nur für die interne Verwendung. Dieses Element wird nicht von Clients verwendet.
ms.openlocfilehash: c148d8fa1301339f8579884dc02b6c9e452f3035
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461296"
---
# <a name="freebusyaccessenabled-soap"></a>FreeBusyAccessEnabled (SOAP)

Das **FreeBusyAccessEnabled** -Element stellt das **FreeBusyAccessEnabled ()** -Flag dar. Das **FreeBusyAccessEnabled** -Element ist nur für die interne Verwendung. Dieses Element wird nicht von Clients verwendet. 
  
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
|[OrganizationRelationshipSettings (SOAP)](organizationrelationshipsettings-soap.md) <br/> |Stellt eine Liste von Organisationsbeziehungen für eine einzelne Organisation dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **true** für das **FreeBusyAccessEnabled** -Element gibt an, dass die Freigabebeziehung zum Abrufen von Frei/Gebucht-Informationen von Benutzern in der Organisation verwendet werden soll. Der Wert **false** gibt an, dass die Freigabebeziehung unterdrückt werden soll. 
  
## <a name="remarks"></a>Bemerkungen

Verwenden Sie dieses Element, um Frei/Gebucht-Informationen vom Server zuzulassen oder zu unterdrücken. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |Auto Ermittlungs Schema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

