---
title: DomainSettings (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: f3d37f5a-c9ea-4ed9-a011-94d33bda64d1
description: Das DomainSettings-Element stellt die Domäneneinstellungen dar, die in einer AutoErmittlungsanforderung übermittelt oder von einer AutoErmittlungsantwort zurückgegeben wurden.
ms.openlocfilehash: 9024421eed20b9a9e642b3b0147699c57fcaaa79
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544178"
---
# <a name="domainsettings-soap"></a>DomainSettings (SOAP)

Das **DomainSettings-Element** stellt die Domäneneinstellungen dar, die in einer AutoErmittlungsanforderung übermittelt oder von einer AutoErmittlungsantwort zurückgegeben wurden. 
  
```XML
<DomainSettings>
   <DomainSetting/>
</DomainSettings>
```

 **DomainSettings**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DomainSetting (SOAP)](domainsetting-soap.md) <br/> |Enthält Domäneneinstellungen, die von einer [SOAP-Anforderung (GetDomainSettings-Vorgang)](getdomainsettings-operation-soap.md) zurückgegeben werden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DomainResponse (SOAP)](domainresponse-soap.md) <br/> |Enthält die angeforderten Einstellungen für die angegebene Domäne.  <br/> |
   
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

