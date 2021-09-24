---
title: AutodiscoverResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 203a5ac3-ebd0-4514-acbe-bc1c74638127
description: Das SOAP-Element (AutodiscoverResponse) stellt das Basiselement für alle Antworten dar, die vom AutoErmittlungsdienst zurückgegeben werden.
ms.openlocfilehash: 71bbb0f1aa6602a260c163ccfdfd3c3d38442e31
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514872"
---
# <a name="autodiscoverresponse-soap"></a>AutodiscoverResponse (SOAP)

Das **SOAP-Element (AutodiscoverResponse)** stellt das Basiselement für alle Antworten dar, die vom AutoErmittlungsdienst zurückgegeben werden. 
  
- [AutodiscoverResponse (SOAP)](autodiscoverresponse-soap.md)
  
```XML
<AutodiscoverResponse>
    <UserResponses/>
    <UserSettingErrors/>
    <UserSettings/>
</AutodiscoverResponse>

```

 **AutoDiscoverResponse**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[UserResponses (SOAP)](userresponses-soap.md) <br/> |Stellt eine Auflistung von [UserResponse -Elementen (SOAP)](userresponse-soap.md) dar.  <br/> |
|[UserSettingErrors (SOAP)](usersettingerrors-soap.md) <br/> |Stellt eine Auflistung von [USERSettingError (SOAP)-Elementen](usersettingerror-soap.md) dar.  <br/> |
|[UserSettings (SOAP)](usersettings-soap.md) <br/> |Stellt eine Auflistung von [UserSetting (SOAP)-Elementen](usersetting-soap.md) dar.  <br/> |
   
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

- [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
- [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)
- [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)

