---
title: DomainSetting (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: bad5399c-0762-4979-9c15-58cf4b7b6278
description: Das DomainSetting-Element enthält Domäneneinstellungen, die von der SOAP-Vorgangsanforderung (GetDomainSettings-Vorgang) zurückgegeben werden.
ms.openlocfilehash: 19c88e6f3f517d012a5c51f548da3d3776770444
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541448"
---
# <a name="domainsetting-soap"></a>DomainSetting (SOAP)

Das **DomainSetting-Element** enthält Domäneneinstellungen, die von der [SOAP-Vorgangsanforderung (GetDomainSettings-Vorgang)](getdomainsettings-operation-soap.md) zurückgegeben werden. 
  
```XML
<DomainSetting>
   <Name/>
</DomainSetting>
```

 **DomainSetting**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Name (SOAP)](name-soap.md) <br/> |Stellt den Namen einer Einstellung dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DomainSettings (SOAP)](domainsettings-soap.md) <br/> |Stellt die Domäneneinstellungen dar, die in einer AutoErmittlungsanforderung übermittelt oder von einer AutoErmittlungsantwort zurückgegeben wurden.  <br/> |
   
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

- [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)

