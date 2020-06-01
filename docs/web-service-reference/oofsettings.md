---
title: OofSettings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OofSettings
api_type:
- schema
ms.assetid: 8f37d174-db11-427c-bbed-fdde754a60c7
description: Das OofSettings-Element enthält die Abwesenheit (Out of Office, OOF) Einstellungen.
ms.openlocfilehash: c1b214fd8bfab5b7a82d41a5187cf6e0fc4ba79c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467193"
---
# <a name="oofsettings"></a>OofSettings

Das **OofSettings** -Element enthält die Abwesenheit (Out of Office, OOF) Einstellungen. 
  
[GetUserOofSettingsResponse](getuseroofsettingsresponse.md)
  
[OofSettings](oofsettings.md)
  
```xml
<OofSettings>
   <OofState>...</OofState>
   <ExternalAudience>...</ExternalAudience>
   <Duration>...</Duration>
   <InternalReply>...</InternalReply>
   <ExternalReply>...</ExternalReply>
</OofSettings>
```

 **UserOofSettings**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[OofState](oofstate.md) <br/> |Enthält den Abwesenheitsstatus des Benutzers.  <br/> |
|[ExternalAudience](externalaudience.md) <br/> |Enthält einen Wert, der bestimmt, an wen externe Abwesenheitsnachrichten gesendet werden.  <br/> |
|[Dauer (UserOofSettings)](duration-useroofsettings.md) <br/> |Enthält die Dauer, für die der Abwesenheitsstatus aktiviert ist, wenn das [OofState](oofstate.md) -Element auf **Scheduled**festgelegt ist. Wenn das [OofState](oofstate.md) -Element auf **aktiviert** oder **deaktiviert**festgelegt ist, wird der Wert dieses Elements ignoriert.  <br/> |
|[InternalReply](internalreply.md) <br/> |Enthält die Abwesenheitsantwort, die an andere Benutzer in der Domäne des Benutzers oder der vertrauenswürdigen Domäne gesendet wurde.  <br/> |
|[ExternalReply](externalreply.md) <br/> |Enthält die Abwesenheitsantwort, die an Adressen außerhalb der Domäne des Empfängers oder vertrauenswürdiger Domänen gesendet wurde.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetUserOofSettingsResponse](getuseroofsettingsresponse.md) <br/> |Enthält die Antwortergebnisse und die Abwesenheitseinstellungen für einen Benutzer.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/GetUserOofSettingsResponse` <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserOofSettings-Vorgang](getuseroofsettings-operation.md)
  
[SetUserOofSettings-Vorgang](setuseroofsettings-operation.md)

