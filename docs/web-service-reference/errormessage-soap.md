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
description: ErrorMessage-Element stellt eine Nachricht, die ein Fehlercode zugeordnet ist, die von den AutoErmittlungsdienst zurückgegeben wird.
ms.openlocfilehash: 888eedc9c7cbbd1aad5cba21e76d999699c7ed02
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758272"
---
# <a name="errormessage-soap"></a>ErrorMessage (SOAP)

**ErrorMessage** -Element stellt eine Nachricht, die ein Fehlercode zugeordnet ist, die von den AutoErmittlungsdienst zurückgegeben wird. 
  
```XML
<ErrorMessage/>
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
|[Antwort (SOAP)](response-soap.md) <br/> |Enthält die Antwort auf eine Anforderung [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md) .  <br/> |
|[UserSettingError (SOAP)](usersettingerror-soap.md) <br/> |Stellt einen Fehler, der beim Abrufen einer benutzereinstellung zurückgegeben wird.  <br/> |
|[UserResponse (SOAP)](userresponse-soap.md) <br/> |Stellt eine Antwort auf eine Anforderung [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md) für einen einzelnen Benutzer dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt die Fehlermeldung angezeigt.
  
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

