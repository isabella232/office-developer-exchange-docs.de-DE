---
title: User Response (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd
description: Das User Response-Element stellt eine Antwort auf eine GetUserSettings-Anforderung für einen einzelnen Benutzer dar.
ms.openlocfilehash: 73848cb19d9c859e07216f354965ac4051d0d20c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468901"
---
# <a name="userresponse-soap"></a>User Response (SOAP)

Das **User Response** -Element stellt eine Antwort auf eine GetUserSettings-Anforderung für einen einzelnen Benutzer dar. 
  
```XML
<UserResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <RedirectTarget/>
   <UserSettingErrors/>
   <UserSettings/>
</UserResponse>
```

 **User Response**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Stellt einen Fehlercode dar, der vom AutoErmittlungsdienst zurückgegeben wird.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Stellt eine Meldung dar, die einem Fehlercode zugeordnet ist, der vom AutoErmittlungsdienst zurückgegeben wird.  <br/> |
|[RedirectTarget (SOAP)](redirecttarget-soap.md) <br/> |Enthält das Ziel der Umleitungs-URL oder e-Mail-Adresse.  <br/> |
|[UserSettingErrors (SOAP)](usersettingerrors-soap.md) <br/> |Stellt eine Sammlung von Informationen zu Einstellungen dar, die nicht zurückgegeben werden konnten.  <br/> |
|[UserSettings (SOAP)](usersettings-soap.md) <br/> |Die angeforderten Einstellungen für den Benutzer.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ArrayOfUserResponse (SOAP)](arrayofuserresponse-soap.md) <br/> |Enthält ein Array von Benutzer Antworten.  <br/> |
|[UserResponses (SOAP)](userresponses-soap.md) <br/> |Enthält die Konfigurationseinstellungen für jeden angeforderten Benutzer.  <br/> |
   
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |Auto Ermittlungs Schema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[XML-Elemente der SOAP-AutoErmittlung für Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

