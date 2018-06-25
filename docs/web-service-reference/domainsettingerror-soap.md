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
description: Das DomainSettingError-Element stellt einen Fehler, die beim Abrufen einer domäneneinstellung dar. Dies stellt einen Fehler aus einer Anforderung GetDomainSettings dar.
ms.openlocfilehash: 08b0a47acea8d35ec78efd701168a251771effac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758100"
---
# <a name="domainsettingerror-soap"></a>DomainSettingError (SOAP)

Das **DomainSettingError** -Element stellt einen Fehler, die beim Abrufen einer domäneneinstellung dar. Dies stellt einen Fehler aus einer Anforderung **GetDomainSettings** dar. 
  
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
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Identifiziert den Fehlercode, der bestimmte Anforderung zugeordnet ist.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Enthält die Fehlermeldung, die die spezifische Anforderung zugeordnet ist.  <br/> |
|[SettingName (SOAP)](settingname-soap.md) <br/> |Der Name der Einstellung darstellt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DomainSettingErrors (SOAP)](domainsettingerrors-soap.md) <br/> |Enthält Informationen für die Einstellungen, die nicht zurückgegeben werden kann.  <br/> |
   
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

