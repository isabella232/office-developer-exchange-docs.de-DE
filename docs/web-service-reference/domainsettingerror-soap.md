---
title: DomainSettingError (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 48c3f7b5-2ee0-42ce-97a1-a881e2f60327
description: Das DomainSettingError-Element stellt einen Fehler dar, der beim Abrufen einer Domäneneinstellung aufgetreten ist. Dies stellt einen Fehler aus einer GetDomainSettings-Anforderung dar.
ms.openlocfilehash: d2d7e1fc1509ade88de0013cb9e4ff54712d0f56
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59530147"
---
# <a name="domainsettingerror-soap"></a>DomainSettingError (SOAP)

Das **DomainSettingError-Element** stellt einen Fehler dar, der beim Abrufen einer Domäneneinstellung aufgetreten ist. Dies stellt einen Fehler aus einer **GetDomainSettings-Anforderung** dar. 
  
```XML
<DomainSettingError>
   <ErrorCode/>
   <ErrorMessage/>
   <SettingName/>
</DomainSettingError>
```

 **DomainSettingError**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Identifiziert den Fehlercode, der der bestimmten Anforderung zugeordnet ist.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Enthält die Fehlermeldung, die der jeweiligen Anforderung zugeordnet ist.  <br/> |
|[SettingName (SOAP)](settingname-soap.md) <br/> |Stellt den Namen der Einstellung dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DomainSettingErrors (SOAP)](domainsettingerrors-soap.md) <br/> |Enthält Fehlerinformationen für Einstellungen, die nicht zurückgegeben werden konnten.  <br/> |
   
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

