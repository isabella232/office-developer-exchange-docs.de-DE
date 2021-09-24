---
title: GetDomainSettingsResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 43ebd17b-3a70-4878-9254-97a4c2c87b77
description: Das GetDomainSettingsResponse-Element stellt die Antwort auf einen GetDomainSettings-Vorgang (SOAP) dar, der die Domäneneinstellungen zurückgibt.
ms.openlocfilehash: e723942ab2691d97729db24c0862af00843e3729
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538131"
---
# <a name="getdomainsettingsresponse-soap"></a>GetDomainSettingsResponse (SOAP)

Das **GetDomainSettingsResponse-Element** stellt die Antwort auf einen [Soap-Vorgang (GetDomainSettings)](getdomainsettings-operation-soap.md)dar, der die Domäneneinstellungen zurückgibt.
  
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
|[DomainResponses (SOAP)](domainresponses-soap.md) <br/> |Enthält ein Array von Antworten für die Einstellungen jeder angeforderten Domäne.  <br/> |
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Stellt einen Fehlercode dar, der vom AutoErmittlungsdienst zurückgegeben wird.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Stellt eine Meldung dar, die einem Fehlercode zugeordnet ist, der vom AutoErmittlungsdienst zurückgegeben wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine
  
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

