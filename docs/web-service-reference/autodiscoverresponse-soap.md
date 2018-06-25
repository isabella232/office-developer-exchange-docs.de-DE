---
title: AutodiscoverResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 203a5ac3-ebd0-4514-acbe-bc1c74638127
description: Das AutodiscoverResponse (SOAP)-Element darstellt, das Basiselement für alle Antworten, die von den AutoErmittlungsdienst zurückgegeben werden.
ms.openlocfilehash: b92a71deb77e2b1dee42d970e2dc43a56044487a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757418"
---
# <a name="autodiscoverresponse-soap"></a>AutodiscoverResponse (SOAP)

Das **AutodiscoverResponse (SOAP)** -Element darstellt, das Basiselement für alle Antworten, die von den AutoErmittlungsdienst zurückgegeben werden. 
  
- [AutodiscoverResponse (SOAP)](autodiscoverresponse-soap.md)
  
```XML
<AutodiscoverResponse>
    <UserResponses/>
    <UserSettingErrors/>
    <UserSettings/>
</AutodiscoverResponse>

```

 **AutodiscoverResponse**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[UserResponses (SOAP)](userresponses-soap.md) <br/> |Stellt eine Auflistung von Elementen [UserResponse (SOAP)](userresponse-soap.md) .  <br/> |
|[UserSettingErrors (SOAP)](usersettingerrors-soap.md) <br/> |Stellt eine Auflistung von Elementen [UserSettingError (SOAP)](usersettingerror-soap.md) .  <br/> |
|[UserSettings (SOAP)](usersettings-soap.md) <br/> |Stellt eine Auflistung von Elementen [UserSetting (SOAP)](usersetting-soap.md) .  <br/> |
   
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

- [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
- [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)
- [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)

