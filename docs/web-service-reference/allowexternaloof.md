---
title: AllowExternalOof
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AllowExternalOof
api_type:
- schema
ms.assetid: e5387172-5b92-4bb1-8394-180e9c7ff771
description: Das AllowExternalOof-Element enthält einen Wert, der angibt, an wen externe OOF-Nachrichten (Out of Office) gesendet werden.
ms.openlocfilehash: 7d2e34797af8a9e9d11570a5ea2e618db7630f0c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523224"
---
# <a name="allowexternaloof"></a>AllowExternalOof

Das **AllowExternalOof-Element** enthält einen Wert, der angibt, an wen externe OOF-Nachrichten (Out of Office) gesendet werden. 
  
- [GetUserOofSettingsResponse](getuseroofsettingsresponse.md)
  
- [AllowExternalOof](allowexternaloof.md)
  
```xml
<AllowExternalOof>None or Known or All</AllowExternalOof>
```

 **ExternalAudience**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetUserOofSettingsResponse](getuseroofsettingsresponse.md) <br/> |Enthält die Antwortergebnisse und die OOF-Einstellungen für einen Benutzer.  <br/> |
   
## <a name="text-value"></a>Textwert

Für dieses Element ist ein Textwert erforderlich. In der folgenden Tabelle sind die möglichen Werte für dieses Element aufgeführt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|**Keine** <br/> |E-Mail-Absender außerhalb der Organisation des Postfachbenutzers, die Nachrichten an den Benutzer senden, erhalten keine externe OOF-Nachrichtenantwort.  <br/> |
|**Bekannt** <br/> |E-Mail-Absender außerhalb der Organisation des Postfachbenutzers, die Nachrichten an den Benutzer senden, erhalten nur dann eine externe OOF-Nachrichtenantwort, wenn sich der Absender in der Exchange Store-Kontaktliste des Benutzers befindet.  <br/> |
|**All** <br/> |E-Mail-Absender außerhalb der Organisation des Postfachbenutzers, die Nachrichten an den Benutzer senden, erhalten eine externe OOF-Nachrichtenantwort.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element hat den gleichen Typ wie das [ExternalAudience-Element.](externalaudience.md) 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserOofSettings-Vorgang](getuseroofsettings-operation.md) 
- [SetUserOofSettings-Vorgang](setuseroofsettings-operation.md)

