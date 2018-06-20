---
title: ErrorCode (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 5e5ec861-0191-4ecb-a906-47ce8ed96381
description: ErrorCode-Element stellt einen Fehlercode, der von den AutoErmittlungsdienst zurückgegeben wird.
ms.openlocfilehash: 2dd91cec4645325c02bc8588af0ee0547909b945
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758262"
---
# <a name="errorcode-soap"></a>ErrorCode (SOAP)

**ErrorCode** -Element stellt einen Fehlercode, der von den AutoErmittlungsdienst zurückgegeben wird. 
  
```XML
<ErrorCode/>
```

 **string**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AutodiscoverResponse (SOAP)](autodiscoverresponse-soap.md) <br/> |Stellt den Basistyp für alle Antworten, die von den AutoErmittlungsdienst zurückgegeben werden.  <br/> |
|[DomainResponse (SOAP)](domainresponse-soap.md) <br/> |Enthält die angeforderten Einstellungen für die angegebene Domäne.  <br/> |
|[GetDomainSettingsResponse (SOAP)](getdomainsettingsresponse-soap.md) <br/> |Enthält die Antwort zu einem Anruf [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md) für eine einzelne Domäne.  <br/> |
|[GetFederationInformationResponse (SOAP)](getfederationinformationresponse-soap.md) <br/> |Enthält die Antwort auf eine Anforderung [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md) .  <br/> |
|[Antwort (SOAP)](response-soap.md) <br/> |Enthält die Antwort auf eine Anforderung [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md).  <br/> |
|[UserSettingError (SOAP)](usersettingerror-soap.md) <br/> |Stellt einen Fehler, der beim Abrufen einer benutzereinstellung zurückgegeben wird.  <br/> |
|[UserResponse (SOAP)](userresponse-soap.md) <br/> |Stellt eine Antwort auf eine Anforderung [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md) für einen einzelnen Benutzer dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt den Fehlercode für eine Fehlerantwort AutoErmittlung. Die folgende Tabelle enthält die möglichen Textwerte für die **ErrorCode** -Element. 
  
|**Fehlercodewert text**|**Beschreibung**|
|:-----|:-----|
|NoError  <br/> |Kein Fehler.  <br/> |
|RedirectAddress  <br/> |Der Aufrufer muss die e-Mail-Adressumleitung folgen, die von der AutoErmittlung zurückgegeben wurde.  <br/> |
|RedirectUrl  <br/> |Der Aufrufer muss die URL-Umleitung folgen, die von der AutoErmittlung zurückgegeben wurde.  <br/> |
|InvalidUser  <br/> |Der Benutzer, der in der Anforderung übergeben wurde, ist ungültig.  <br/> |
|InvalidRequest  <br/> |Die Anforderung ist ungültig.  <br/> |
|InvalidSetting  <br/> |Eine festgelegte Einstellung ist ungültig.  <br/> |
|SettingIsNotAvailable  <br/> |Eine festgelegte Einstellung ist nicht verfügbar.  <br/> |
|ServerBusy  <br/> |Der Server ist ausgelastet und die Anforderung zu verarbeiten.  <br/> |
|InvalidDomain  <br/> |Die angeforderte Domäne ist ungültig.  <br/> |
|NotFederated  <br/> |Die Organisation nicht im Verbund arbeitet.  <br/> |
|InternalServerError  <br/> |Es ist ein interner Serverfehler.  <br/> |
   
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlung-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
  
[GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)
  
[GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)

