---
title: Antwort (GetDomainSettings) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: a5b052df-93bd-4fe1-ac30-83de9a3dfcd7
description: Das Response-Element stellt die Antwort auf einen GetDomainSettings-Aufruf für eine einzelne Domäne dar.
ms.openlocfilehash: e8f76127d5e812bc6805430544fe334eabd29ffa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540552"
---
# <a name="response-getdomainsettings-soap"></a>Antwort (GetDomainSettings) (SOAP)

Das **Response-Element** stellt die Antwort auf einen **GetDomainSettings-Aufruf** für eine einzelne Domäne dar. 
  
```XML
<Response>
   <DomainResponses/>
   <ErrorCode/>
   <ErrorMessage/>
</Response>
```

 **GetDomainSettingsResponse**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DomainResponses (SOAP)](domainresponses-soap.md) <br/> |Enthält die Antwort für jede in einer **GetDomainSettings-Anforderung** angeforderte Domäne.  <br/> |
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Enthält ggf. den Fehlercode, der der Antwort zugeordnet ist.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Enthält ggf. die Fehlermeldung, die der Antwort zugeordnet ist.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetDomainSettingsResponseMessage (SOAP)](getdomainsettingsresponsemessage-soap.md) <br/> |Gibt an den Aufrufer die Domänenkonfigurationseinstellungen zurück.  <br/> |
   
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



[GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)

