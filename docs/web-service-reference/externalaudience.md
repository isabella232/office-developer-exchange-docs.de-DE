---
title: ExternalAudience
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExternalAudience
api_type:
- schema
ms.assetid: 79dc2a4c-f7dd-46d1-8f31-149116e1f76e
description: Das Element ExternalAudience legt oder enthält einen Wert, der bestimmt, denen externe Out of Office (OOF) Testnachrichten gesendet werden.
ms.openlocfilehash: 836b0f6a5140a37e1584f571cb8e26534fe7a25f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758368"
---
# <a name="externalaudience"></a>ExternalAudience

Das Element **ExternalAudience** legt oder enthält einen Wert, der bestimmt, denen externe Out of Office (OOF) Testnachrichten gesendet werden. 
  
```xml
<ExternalAudience>None or Known or All</ExternalAudience>
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
|[' UserOofSettings '](useroofsettings.md) <br/> |Gibt die OOF-Einstellungen.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[OofSettings](oofsettings.md) <br/> |Enthält die OOF-Einstellungen.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/GetUserOofSettingsResponse/OofSettings` <br/> |
   
## <a name="text-value"></a>Textwert

Es wird ein Textwert für dieses Element erforderlich. Die folgende Tabelle enthält die möglichen Werte für dieses Element.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|**None** <br/> |E-Mail-Absender außerhalb der Organisation das des Postfachbenutzers, die Senden von Nachrichten an die Benutzer werden keine externe OOF Nachricht beantwortet.  <br/> |
|**Bekannte** <br/> |E-Mail-Absender außerhalb der Organisation das des Postfachbenutzers, die Senden von Nachrichten an den Benutzer nur eine externe OOF Nachrichtenantwort erhält, wenn der Absender in Exchange des Benutzers ist speichern Kontaktliste.  <br/> |
|**All** <br/> |E-Mail-Absender außerhalb der Organisation das des Postfachbenutzers, die Senden von Nachrichten an die Benutzer erhalten eine externe OOF Nachrichtenantwort.  <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element gibt den gleichen Datentyp wie das [AllowExternalOof](allowexternaloof.md) -Element. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird eine Anforderung SetUserOofSettings legt die OoFState **aktiviert**, wird die externe Benutzergruppe auf **Alle**, wird die Dauer der OOF auf 10 Tage und die internen und externen Abwesenheitsnachrichten festgelegt.
  
```
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <OofState>Enabled</OofState>
        <ExternalAudience>All</ExternalAudience>
        <Duration>
          <StartTime>2005-10-05T00:00:00</StartTime>
          <EndTime>2005-10-25T00:00:00</EndTime>
        </Duration>
        <InternalReply>
          <Message>I am out of office.  This is my internal reply.</Message>
        </InternalReply>
        <ExternalReply>
          <Message>I am out of office. This is my external reply.</Message>
        </ExternalReply>
      </UserOofSettings>
    </SetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserOofSettings-Vorgang](getuseroofsettings-operation.md)
  
[SetUserOofSettings-Vorgang](setuseroofsettings-operation.md)

