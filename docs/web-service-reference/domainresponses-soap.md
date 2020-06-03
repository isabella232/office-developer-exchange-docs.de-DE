---
title: DomainResponses (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: d9c7fd91-22cd-4c72-a841-25cb9d415e0c
description: Das DomainResponses-Element enthält ein Array von Antworten für die Einstellungen jeder angeforderten Domäne.
ms.openlocfilehash: 2c76b9691fe88657a65130ef6829e5af64380d95
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526319"
---
# <a name="domainresponses-soap"></a>DomainResponses (SOAP)

Das **DomainResponses** -Element enthält ein Array von Antworten für die Einstellungen jeder angeforderten Domäne. 
  
```XML
<DomainResponses>
   <DomainResponse/>
</DomainResponses>
```

 **ArrayOfDomainResponse**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DomainResponse (SOAP)](domainresponse-soap.md) <br/> |Enthält die angeforderten Einstellungen für die angegebene Domäne.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetDomainSettingsResponse (SOAP)](getdomainsettingsresponse-soap.md) <br/> |Stellt die Antwort auf eine [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md) -Anforderung für eine Domäne dar und gibt die Domäneneinstellungen zurück.  <br/> |
|[Antwort (GetDomainSettings) (SOAP)](response-getdomainsettingssoap.md) <br/> |Stellt die Antwort auf einen [GetDomainSettings-Vorgang (SOAP)-](getdomainsettings-operation-soap.md) Aufruf für eine einzelne Domäne dar.  <br/> |
   
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

