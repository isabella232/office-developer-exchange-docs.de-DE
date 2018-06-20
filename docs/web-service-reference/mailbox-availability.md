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
description: Das Postfach-Element stellt den Postfachbenutzer für eine SetUserOofSettings oder GetUserOofSettings anfordern.
ms.openlocfilehash: 2e901ae0df56542f56f247184254294735018468
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830254"
---
# <a name="mailbox-availability"></a>Postfach (Verfügbarkeit)

Das **Postfach** -Element stellt den Postfachbenutzer für eine SetUserOofSettings oder GetUserOofSettings anfordern. 
  
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
|[Name (EmailAddress)](name-emailaddress.md) <br/> |Stellt den Anzeigenamen des Postfachbenutzers an. Dieses Element ist in der SetUserOofSettingsRequest optional. Die GetUserOofSettingsRequest gibt dieses Element zurück.  <br/> |
|[Adresse (Zeichenfolge)](address-string.md) <br/> |Stellt die e-Mail-Adresse des Postfachbenutzers an. Dieses Element ist erforderlich.  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |Stellt das routing-Protokoll für die Nachricht an. Dieses Element ist in der SetUserOofSettingsRequest optional. Die GetUserOofSettingsRequest gibt dieses Element zurück.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetUserOofSettingsRequest](getuseroofsettingsrequest.md) <br/> |Zum Abrufen von Einstellungen von Office (ABWESEND) und Nachrichten eines Postfachbenutzers verwendet.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/GetUserOofSettingsRequest` <br/> |
|[SetUserOofSettingsRequest](setuseroofsettingsrequest.md) <br/> |Verwendet, um eines Postfachbenutzers OOF Einstellungen und Nachrichten festzulegen.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/SetUserOofSettingsRequest` <br/> |
   
## <a name="remarks"></a>Hinweise

Die E-mail-Adresse wird verwendet, um den Kalenderordner zu identifizieren, der die OOF Einstellungen enthält. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserOofSettings-Vorgang](getuseroofsettings-operation.md)
- [SetUserOofSettings-Vorgang](setuseroofsettings-operation.md)

