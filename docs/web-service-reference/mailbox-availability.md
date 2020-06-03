---
title: Postfach (Verfügbarkeit)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Mailbox
api_type:
- schema
ms.assetid: affd192e-8914-473f-9098-d9bdf898de2c
description: Das Mailbox-Element stellt den Postfachbenutzer für eine SetUserOofSettings-oder GetUserOofSettings-Anforderung dar.
ms.openlocfilehash: 1bda6e8b90551b86b4e1c2711ac25693a65e5410
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458075"
---
# <a name="mailbox-availability"></a>Postfach (Verfügbarkeit)

Das **Mailbox** -Element stellt den Postfachbenutzer für eine SetUserOofSettings-oder GetUserOofSettings-Anforderung dar. 
  
```xml
<Mailbox>
   <Name>...</Name>
   <Address>...</Address>
   <RoutingType>...</RoutingType>
</Mailbox>
```

**EmailAddressType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Name (e-mailemail)](name-emailaddress.md) <br/> |Stellt den Anzeigenamen des Postfachbenutzers dar. Dieses Element ist in der SetUserOofSettingsRequest optional. Das GetUserOofSettingsRequest-Objekt gibt dieses Element zurück.  <br/> |
|[Address (Zeichenfolge)](address-string.md) <br/> |Stellt die e-Mail-Adresse des Postfachbenutzers dar. Dieses Element ist erforderlich.  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |Stellt das Routingprotokoll für die Nachricht dar. Dieses Element ist in der SetUserOofSettingsRequest optional. Das GetUserOofSettingsRequest-Objekt gibt dieses Element zurück.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetUserOofSettingsRequest](getuseroofsettingsrequest.md) <br/> |Dient zum Abrufen der Abwesenheit (Out of Office, OOF) Einstellungen und Nachrichten eines Postfachbenutzers.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/GetUserOofSettingsRequest` <br/> |
|[SetUserOofSettingsRequest](setuseroofsettingsrequest.md) <br/> |Wird verwendet, um die Abwesenheitseinstellungen und-Nachrichten eines Postfachbenutzers festzulegen.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/SetUserOofSettingsRequest` <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die e-Mail-Adresse wird verwendet, um den Kalenderordner zu identifizieren, der die Abwesenheitseinstellungen enthält. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserOofSettings-Vorgang](getuseroofsettings-operation.md)
- [SetUserOofSettings-Vorgang](setuseroofsettings-operation.md)

