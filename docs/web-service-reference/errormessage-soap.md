---
title: ErrorMessage (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: b84dd664-4c49-42c9-a49f-2ec4a9f7588b
description: Das ErrorMessage-Element stellt eine Meldung dar, die einem Fehlercode zugeordnet ist, der vom AutoErmittlungsdienst zurückgegeben wird.
ms.openlocfilehash: 4ebaf91fe26083cf241826e1fc16ac184fddf57c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530642"
---
# <a name="errormessage-soap"></a>ErrorMessage (SOAP)

Das **ErrorMessage** -Element stellt eine Meldung dar, die einem Fehlercode zugeordnet ist, der vom AutoErmittlungsdienst zurückgegeben wird. 
  
```XML
<ErrorMessage/>
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
|[Antwort (SOAP)](response-soap.md) <br/> |Enthält die Antwort auf eine [GetUserSettings-Vorgang (SOAP)-](getusersettings-operation-soap.md) Anforderung.  <br/> |
|[UserSettingError (SOAP)](usersettingerror-soap.md) <br/> |Stellt einen Fehler dar, der beim Abrufen einer Benutzereinstellung zurückgegeben wird.  <br/> |
|[User Response (SOAP)](userresponse-soap.md) <br/> |Stellt eine Antwort auf eine [GetUserSettings-Vorgang (SOAP)-](getusersettings-operation-soap.md) Anforderung für einen einzelnen Benutzer dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Text-Wert stellt die Fehlermeldung dar.
  
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

