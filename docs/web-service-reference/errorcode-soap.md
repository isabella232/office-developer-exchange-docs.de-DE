---
title: ErrorCode (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 5e5ec861-0191-4ecb-a906-47ce8ed96381
description: Das ErrorCode-Element stellt einen Fehlercode dar, der vom AutoErmittlungsdienst zurückgegeben wird.
ms.openlocfilehash: fa40cb8b7a2ec80ecf752058f540969013748d39
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59530773"
---
# <a name="errorcode-soap"></a>ErrorCode (SOAP)

Das **ErrorCode-Element** stellt einen Fehlercode dar, der vom AutoErmittlungsdienst zurückgegeben wird. 
  
```XML
<ErrorCode/>
```

 **Zeichenfolge**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AutodiscoverResponse (SOAP)](autodiscoverresponse-soap.md) <br/> |Stellt den Basistyp für alle Antworten dar, die vom AutoErmittlungsdienst zurückgegeben werden.  <br/> |
|[DomainResponse (SOAP)](domainresponse-soap.md) <br/> |Enthält die angeforderten Einstellungen für die angegebene Domäne.  <br/> |
|[GetDomainSettingsResponse (SOAP)](getdomainsettingsresponse-soap.md) <br/> |Enthält die Antwort auf einen [SOAP-Aufruf (GetDomainSettings-Vorgang)](getdomainsettings-operation-soap.md) für eine einzelne Domäne.  <br/> |
|[GetFederationInformationResponse (SOAP)](getfederationinformationresponse-soap.md) <br/> |Enthält die Antwort auf eine [SOAP-Anforderung (GetFederationInformation-Vorgang).](getfederationinformation-operation-soap.md)  <br/> |
|[Antwort (SOAP)](response-soap.md) <br/> |Enthält die Antwort auf eine [SOAP-Anforderung (GetUserSettings-Vorgang).](getusersettings-operation-soap.md)  <br/> |
|[UserSettingError (SOAP)](usersettingerror-soap.md) <br/> |Stellt einen Fehler dar, der beim Abrufen einer Benutzereinstellung zurückgegeben wird.  <br/> |
|[UserResponse (SOAP)](userresponse-soap.md) <br/> |Stellt eine Antwort auf eine [SOAP-Anforderung (GetUserSettings)-Operation](getusersettings-operation-soap.md) für einen einzelnen Benutzer dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt den Fehlercode für eine Fehlerantwort der AutoErmittlung dar. In der folgenden Tabelle sind die möglichen Textwerte für das **ErrorCode-Element** aufgeführt. 
  
|**Fehlercodetextwert**|**Beschreibung**|
|:-----|:-----|
|NoError  <br/> |Es ist kein Fehler aufgetreten.  <br/> |
|RedirectAddress  <br/> |Der Anrufer muss der Umleitung der E-Mail-Adresse folgen, die von der AutoErmittlung zurückgegeben wurde.  <br/> |
|RedirectUrl  <br/> |Der Aufrufer muss der URL-Umleitung folgen, die von der AutoErmittlung zurückgegeben wurde.  <br/> |
|InvalidUser  <br/> |Der Benutzer, der in der Anforderung übergeben wurde, ist ungültig.  <br/> |
|InvalidRequest  <br/> |Die Anforderung ist ungültig.  <br/> |
|InvalidSetting  <br/> |Eine angegebene Einstellung ist ungültig.  <br/> |
|SettingIsNotAvailable  <br/> |Eine angegebene Einstellung ist nicht verfügbar.  <br/> |
|ServerBusy  <br/> |Der Server ist zu ausgelastet, um die Anforderung zu verarbeiten.  <br/> |
|InvalidDomain  <br/> |Die angeforderte Domäne ist ungültig.  <br/> |
|NotFederated  <br/> |Die Organisation ist nicht verbunden.  <br/> |
|InternalServerError  <br/> |Es tritt ein interner Serverfehler auf.  <br/> |
   
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
  
[GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)
  
[GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)

