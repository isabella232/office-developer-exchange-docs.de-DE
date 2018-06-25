---
title: GetDomainSettingsResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 43ebd17b-3a70-4878-9254-97a4c2c87b77
description: Das GetDomainSettingsResponse-Element darstellt, die Antwort auf eine Operation GetDomainSettings (SOAP), die die domäneneinstellungen zurückgibt.
ms.openlocfilehash: c4984c2c6c532fcbd45c1a75733e578f6d9491fa
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758642"
---
# <a name="getdomainsettingsresponse-soap"></a>GetDomainSettingsResponse (SOAP)

Das **GetDomainSettingsResponse** -Element darstellt, die Antwort auf eine [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md), die die domäneneinstellungen zurückgibt.
  
```XML
<GetDomainSettingsResponse>
   <DomainResponses/>
   <ErrorCode/>
   <ErrorMessage/>
</GetDomainSettingsResponse>
```

 **GetDomainSettingsResponse**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DomainResponses (SOAP)](domainresponses-soap.md) <br/> |Enthält ein Array von Antworten für jede angeforderte Domäne Einstellungen.  <br/> |
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Stellt einen Fehlercode, der von den AutoErmittlungsdienst zurückgegeben wird.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Stellt eine Nachricht, die ein Fehlercode zugeordnet ist, die von den AutoErmittlungsdienst zurückgegeben wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
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



[GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)

