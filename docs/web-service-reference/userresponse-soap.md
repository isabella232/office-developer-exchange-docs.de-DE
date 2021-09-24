---
title: UserResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd
description: Das UserResponse-Element stellt eine Antwort auf eine GetUserSettings-Anforderung für einen einzelnen Benutzer dar.
ms.openlocfilehash: 8def0183a5c2e212e80699a3c2f58c64f67ce690
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538541"
---
# <a name="userresponse-soap"></a>UserResponse (SOAP)

Das **UserResponse-Element** stellt eine Antwort auf eine GetUserSettings-Anforderung für einen einzelnen Benutzer dar. 
  
```XML
<UserResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <RedirectTarget/>
   <UserSettingErrors/>
   <UserSettings/>
</UserResponse>
```

 **UserResponse**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Stellt einen Fehlercode dar, der vom AutoErmittlungsdienst zurückgegeben wird.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Stellt eine Meldung dar, die einem Fehlercode zugeordnet ist, der vom AutoErmittlungsdienst zurückgegeben wird.  <br/> |
|[RedirectTarget (SOAP)](redirecttarget-soap.md) <br/> |Enthält das Ziel der Umleitungs-URL oder E-Mail-Adresse.  <br/> |
|[UserSettingErrors (SOAP)](usersettingerrors-soap.md) <br/> |Stellt eine Auflistung von Informationen zu Einstellungen dar, die nicht zurückgegeben werden konnten.  <br/> |
|[UserSettings (SOAP)](usersettings-soap.md) <br/> |Die angeforderten Einstellungen für den Benutzer.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ArrayOfUserResponse (SOAP)](arrayofuserresponse-soap.md) <br/> |Enthält ein Array von Benutzerantworten.  <br/> |
|[UserResponses (SOAP)](userresponses-soap.md) <br/> |Enthält die Konfigurationseinstellungen für jeden angeforderten Benutzer.  <br/> |
   
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SOAP AutoDiscover XML-Elemente für Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

