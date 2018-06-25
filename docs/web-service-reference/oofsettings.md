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
description: Das OofSettings-Element enthält die Einstellungen von Office (OOF).
ms.openlocfilehash: d71f068ff24af22da98b6b4de090ab26d3f74f26
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830649"
---
# <a name="oofsettings"></a>OofSettings

Das **OofSettings** -Element enthält die Einstellungen von Office (OOF). 
  
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

 **' UserOofSettings '**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[OofState](oofstate.md) <br/> |Enthält den Status des Benutzers OOF.  <br/> |
|[ExternalAudience](externalaudience.md) <br/> |Enthält einen Wert, der bestimmt, denen externe OOF Testnachrichten gesendet werden.  <br/> |
|[Dauer (' UserOofSettings ')](duration-useroofsettings.md) <br/> |Enthält die Dauer, für die der Status ABWESEND aktiviert ist, wenn das Element [OofState](oofstate.md) **geplant**festgelegt ist. Wenn das Element [OofState](oofstate.md) auf **aktiviert** oder **deaktiviert**festgelegt ist, wird der Wert der dieses Element ignoriert.  <br/> |
|[InternalReply](internalreply.md) <br/> |Enthält die OOF Antwort an andere Benutzer in der Domäne oder der vertrauenswürdigen Domäne des Benutzers gesendet.  <br/> |
|[ExternalReply](externalreply.md) <br/> |Enthält die OOF Antwort an Adressen außerhalb der Domäne oder der vertrauenswürdigen Domänen des Empfängers gesendet.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetUserOofSettingsResponse](getuseroofsettingsresponse.md) <br/> |Enthält die Antwort Ergebnisse und OOF-Einstellungen für einen Benutzer.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/GetUserOofSettingsResponse` <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserOofSettings-Vorgang](getuseroofsettings-operation.md)
  
[SetUserOofSettings-Vorgang](setuseroofsettings-operation.md)

