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
description: Das ErrorCode-Element stellt einen Fehlercode dar, der vom AutoErmittlungsdienst zurückgegeben wird.
ms.openlocfilehash: d66167e51733ffcaa3d62a985d3e03e2ac80b715
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460092"
---
# <a name="errorcode-soap"></a>ErrorCode (SOAP)

Das **errorCode** -Element stellt einen Fehlercode dar, der vom AutoErmittlungsdienst zurückgegeben wird. 
  
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
|[GetDomainSettingsResponse (SOAP)](getdomainsettingsresponse-soap.md) <br/> |Enthält die Antwort auf einen [GetDomainSettings-Vorgang (SOAP)-](getdomainsettings-operation-soap.md) Aufruf für eine einzelne Domäne.  <br/> |
|[GetFederationInformationResponse (SOAP)](getfederationinformationresponse-soap.md) <br/> |Enthält die Antwort auf eine [GetFederationInformation-Vorgang (SOAP)-](getfederationinformation-operation-soap.md) Anforderung.  <br/> |
|[Antwort (SOAP)](response-soap.md) <br/> |Enthält die Antwort auf eine [GetUserSettings-Vorgang (SOAP)-](getusersettings-operation-soap.md)Anforderung.  <br/> |
|[UserSettingError (SOAP)](usersettingerror-soap.md) <br/> |Stellt einen Fehler dar, der beim Abrufen einer Benutzereinstellung zurückgegeben wird.  <br/> |
|[User Response (SOAP)](userresponse-soap.md) <br/> |Stellt eine Antwort auf eine [GetUserSettings-Vorgang (SOAP)-](getusersettings-operation-soap.md) Anforderung für einen einzelnen Benutzer dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Text-Wert stellt den Fehlercode für eine Auto Ermittlungsfehler Antwort dar. In der folgenden Tabelle sind die möglichen Text Werte für das **errorCode** -Element aufgeführt. 
  
|**Fehlercodetext Wert**|**Beschreibung**|
|:-----|:-----|
|NoError  <br/> |Es ist kein Fehler aufgetreten.  <br/> |
|RedirectAddress  <br/> |Der Anrufer muss die von der AutoErmittlung zurückgegebene e-Mail-Adress Umleitung befolgten.  <br/> |
|RedirectUrl  <br/> |Der Aufrufer muss die von der AutoErmittlung zurückgegebene URL-Umleitung befolgten.  <br/> |
|InvalidUser  <br/> |Der Benutzer, der in der Anforderung übergeben wurde, ist ungültig.  <br/> |
|InvalidRequest  <br/> |Die Anforderung ist ungültig.  <br/> |
|InvalidSetting  <br/> |Eine angegebene Einstellung ist ungültig.  <br/> |
|SettingIsNotAvailable  <br/> |Eine angegebene Einstellung ist nicht verfügbar.  <br/> |
|ServerBusy  <br/> |Der Server ist zu beschäftigt, um die Anforderung zu verarbeiten.  <br/> |
|InvalidDomain  <br/> |Die angeforderte Domäne ist ungültig.  <br/> |
|NotFederated  <br/> |Die Organisation ist nicht Verbund.  <br/> |
|InternalServerError  <br/> |Es ist ein interner Serverfehler aufgetreten.  <br/> |
   
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |Auto Ermittlungs Schema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
  
[GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)
  
[GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)

