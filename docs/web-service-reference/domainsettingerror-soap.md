---
title: DomainSettingError (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 48c3f7b5-2ee0-42ce-97a1-a881e2f60327
description: Das DomainSettingError-Element stellt einen Fehler dar, der beim Abrufen einer Domäneneinstellung aufgetreten ist. Dies stellt einen Fehler aus einer GetDomainSettings-Anforderung dar.
ms.openlocfilehash: 189a614e7629033c8db2f60b8fd3679835a696ed
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530712"
---
# <a name="domainsettingerror-soap"></a>DomainSettingError (SOAP)

Das **DomainSettingError** -Element stellt einen Fehler dar, der beim Abrufen einer Domäneneinstellung aufgetreten ist. Dies stellt einen Fehler aus einer **GetDomainSettings** -Anforderung dar. 
  
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
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Gibt den Fehlercode an, der der spezifischen Anforderung zugeordnet ist.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Enthält die Fehlermeldung, die der spezifischen Anforderung zugeordnet ist.  <br/> |
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
|Name des Schemas  <br/> |Auto Ermittlungs Schema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)

