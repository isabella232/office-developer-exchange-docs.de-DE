---
title: OofSettings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- OofSettings
api_type:
- schema
ms.assetid: 8f37d174-db11-427c-bbed-fdde754a60c7
description: Das OofSettings-Element enthält die OOF-Einstellungen (Out of Office).
ms.openlocfilehash: 0a612cacb69464dfda3c1f235c32f569d3e45775
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543170"
---
# <a name="oofsettings"></a>OofSettings

Das **OofSettings-Element** enthält die OOF-Einstellungen (Out of Office). 
  
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
|[OofState](oofstate.md) <br/> |Enthält den OOF-Status des Benutzers.  <br/> |
|[ExternalAudience](externalaudience.md) <br/> |Enthält einen Wert, der bestimmt, an wen externe OOF-Nachrichten gesendet werden.  <br/> |
|[Dauer (UserOofSettings)](duration-useroofsettings.md) <br/> |Enthält die Dauer, für die der OOF-Status aktiviert ist, wenn das [OofState-Element](oofstate.md) auf **Geplant** festgelegt ist. Wenn das [OofState-Element](oofstate.md) auf **"Enabled"** oder **"Disabled"** festgelegt ist, wird der Wert dieses Elements ignoriert.  <br/> |
|[InternalReply](internalreply.md) <br/> |Enthält die OOF-Antwort, die an andere Benutzer in der Domäne oder vertrauenswürdigen Domäne des Benutzers gesendet wird.  <br/> |
|[ExternalReply](externalreply.md) <br/> |Enthält die OOF-Antwort, die an Adressen außerhalb der Domäne oder der vertrauenswürdigen Domänen des Empfängers gesendet wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetUserOofSettingsResponse](getuseroofsettingsresponse.md) <br/> |Enthält die Antwortergebnisse und die OOF-Einstellungen für einen Benutzer.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/GetUserOofSettingsResponse` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserOofSettings-Vorgang](getuseroofsettings-operation.md)
  
[SetUserOofSettings-Vorgang](setuseroofsettings-operation.md)

