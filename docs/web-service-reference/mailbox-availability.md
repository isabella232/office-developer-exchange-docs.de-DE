---
title: Postfach (Verfügbarkeit)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Mailbox
api_type:
- schema
ms.assetid: affd192e-8914-473f-9098-d9bdf898de2c
description: Das Mailbox-Element stellt den Postfachbenutzer für eine SetUserOofSettings- oder GetUserOofSettings-Anforderung dar.
ms.openlocfilehash: 5e32c4be807dae92b27df7012caa8eb1b295b26c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522922"
---
# <a name="mailbox-availability"></a>Postfach (Verfügbarkeit)

Das **Mailbox-Element** stellt den Postfachbenutzer für eine SetUserOofSettings- oder GetUserOofSettings-Anforderung dar. 
  
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
|[Name (EmailAddress)](name-emailaddress.md) <br/> |Stellt den Anzeigenamen des Postfachbenutzers dar. Dieses Element ist optional in "SetUserOofSettingsRequest". GetUserOofSettingsRequest gibt dieses Element zurück.  <br/> |
|[Adresse (Zeichenfolge)](address-string.md) <br/> |Stellt die E-Mail-Adresse des Postfachbenutzers dar. Dieses Element ist erforderlich.  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |Stellt das Routingprotokoll für die Nachricht dar. Dieses Element ist optional in "SetUserOofSettingsRequest". GetUserOofSettingsRequest gibt dieses Element zurück.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetUserOofSettingsRequest](getuseroofsettingsrequest.md) <br/> |Wird verwendet, um die OOF-Einstellungen und -Nachrichten (Out of Office) eines Postfachbenutzers abzurufen.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/GetUserOofSettingsRequest` <br/> |
|[SetUserOofSettingsRequest](setuseroofsettingsrequest.md) <br/> |Wird verwendet, um die OOF-Einstellungen und -Nachrichten eines Postfachbenutzers festzulegen.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/SetUserOofSettingsRequest` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die E-Mail-Adresse wird verwendet, um den Kalenderordner zu identifizieren, der die OOF-Einstellungen enthält. 
  
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

