---
title: DomainSetting (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: bad5399c-0762-4979-9c15-58cf4b7b6278
description: Das DomainSetting-Element enthält Domäneneinstellungen, die von der Vorgangsanforderung des GetDomainSettings-Vorgangs (SOAP) zurückgegeben werden.
ms.openlocfilehash: 54441dd7cfcf7372807a1e6bfd8ea5d26805bffc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526298"
---
# <a name="domainsetting-soap"></a>DomainSetting (SOAP)

Das **DomainSetting** -Element enthält Domäneneinstellungen, die von der Vorgangsanforderung des [GetDomainSettings-Vorgangs (SOAP)](getdomainsettings-operation-soap.md) zurückgegeben werden. 
  
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
|[DomainSettings (SOAP)](domainsettings-soap.md) <br/> |Stellt die Domäneneinstellungen dar, die in einer Auto Ermittlungsanforderung übermittelt oder von einer Auto Ermittlungs Antwort zurückgegeben wurden.  <br/> |
   
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

- [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)

