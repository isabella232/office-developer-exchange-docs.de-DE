---
title: AllowExternalOof
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AllowExternalOof
api_type:
- schema
ms.assetid: e5387172-5b92-4bb1-8394-180e9c7ff771
description: Das AllowExternalOof-Element enthält einen Wert, der angibt, den externe Out of Office (OOF) Testnachrichten gesendet werden.
ms.openlocfilehash: 1c87a51676bf6e44b2e650a4e973d0ab89a52e31
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757258"
---
# <a name="allowexternaloof"></a>AllowExternalOof

Das **AllowExternalOof** -Element enthält einen Wert, der angibt, den externe Out of Office (OOF) Testnachrichten gesendet werden. 
  
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
|[GetUserOofSettingsResponse](getuseroofsettingsresponse.md) <br/> |Enthält die Antwort Ergebnisse und OOF-Einstellungen für einen Benutzer.  <br/> |
   
## <a name="text-value"></a>Textwert

Es wird ein Textwert für dieses Element erforderlich. Die folgende Tabelle enthält die möglichen Werte für dieses Element.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|**None** <br/> |E-Mail-Absender außerhalb der Organisation das des Postfachbenutzers, die Senden von Nachrichten an die Benutzer werden keine externe OOF Nachricht beantwortet.  <br/> |
|**Bekannte** <br/> |E-Mail-Absender außerhalb der Organisation das des Postfachbenutzers, die Senden von Nachrichten an den Benutzer nur eine externe OOF Nachrichtenantwort erhält, wenn der Absender in Exchange des Benutzers ist speichern Kontaktliste.  <br/> |
|**All** <br/> |E-Mail-Absender außerhalb der Organisation das des Postfachbenutzers, die Senden von Nachrichten an die Benutzer erhalten eine externe OOF Nachrichtenantwort.  <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element gibt den gleichen Datentyp wie das [ExternalAudience](externalaudience.md) -Element. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserOofSettings-Vorgang](getuseroofsettings-operation.md) 
- [SetUserOofSettings-Vorgang](setuseroofsettings-operation.md)

