---
title: FreeBusyAccessEnabled (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8d2d3276-b180-424e-a707-7256d14a1776
description: Das FreeBusyAccessEnabled-Element darstellt, das FreeBusyAccessEnabled()-Flag. Das FreeBusyAccessEnabled-Element ist nur zur internen Verwendung. Dieses Element wird von Clients nicht verwendet.
ms.openlocfilehash: 4727e7054c02a4b5d454cb880691ecc01a075327
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758541"
---
# <a name="freebusyaccessenabled-soap"></a>FreeBusyAccessEnabled (SOAP)

Das **FreeBusyAccessEnabled** -Element darstellt, das **FreeBusyAccessEnabled()** -Flag. Das **FreeBusyAccessEnabled** -Element ist nur zur internen Verwendung. Dieses Element wird von Clients nicht verwendet. 
  
```XML
<FreeBusyAccessEnabled>true | false</FreeBusyAccessEnabled>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[OrganizationRelationshipSettings (SOAP)](organizationrelationshipsettings-soap.md) <br/> |Stellt eine Liste von organisationsbeziehungen für eine einzelne Organisation.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **true** für das Element **FreeBusyAccessEnabled** gibt an, dass die Beziehung zum Abrufen von Frei/Gebucht-Informationen von Benutzern in der Organisation verwendet werden soll. Der Wert **false** gibt an, dass die Beziehung unterdrückt werden soll. 
  
## <a name="remarks"></a>Hinweise

Verwenden Sie dieses Element zulassen oder Unterdrücken von Frei/Gebucht-Informationen vom Server. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlung-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetOrganizationRelationshipSettings-Vorgang (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

