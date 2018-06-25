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
description: Das DomainResponses-Element enthält ein Array von Antworten für jede angeforderte Domäne Einstellungen.
ms.openlocfilehash: 77a3efc1605337ab436f6aea2b61a67f22e4f8ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758097"
---
# <a name="domainresponses-soap"></a>DomainResponses (SOAP)

Das **DomainResponses** -Element enthält ein Array von Antworten für jede angeforderte Domäne Einstellungen. 
  
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
|[GetDomainSettingsResponse (SOAP)](getdomainsettingsresponse-soap.md) <br/> |Stellt die Antwort auf eine Anforderung [(SOAP) GetDomainSettings-Vorgang](getdomainsettings-operation-soap.md) für eine Domäne, und die domäneneinstellungen zurückgegeben.  <br/> |
|[Antwort (GetDomainSettings) (SOAP)](response-getdomainsettingssoap.md) <br/> |Die Antwort zu einem Anruf [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md) für eine einzelne Domäne darstellt.  <br/> |
   
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

- [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)

