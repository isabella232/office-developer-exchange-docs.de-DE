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
description: Das ExternalAudience-Element legt fest oder enthält einen Wert, der bestimmt, an wen externe Abwesenheit (Out of Office, OOF) Nachrichten gesendet werden.
ms.openlocfilehash: b3fcebd9042b07bb9a8294196799ef2a13d78bdd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530600"
---
# <a name="externalaudience"></a>ExternalAudience

Das **ExternalAudience** -Element legt fest oder enthält einen Wert, der bestimmt, an wen externe Abwesenheit (Out of Office, OOF) Nachrichten gesendet werden. 
  
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
|[UserOofSettings](useroofsettings.md) <br/> |Gibt die Abwesenheitseinstellungen an.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[OofSettings](oofsettings.md) <br/> |Enthält die OOF-Einstellungen.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/GetUserOofSettingsResponse/OofSettings` <br/> |
   
## <a name="text-value"></a>Textwert

Für dieses Element ist ein Textwert erforderlich. In der folgenden Tabelle sind die möglichen Werte für dieses Element aufgeführt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|**Keine** <br/> |E-Mail-Absender außerhalb der Organisation des Postfachbenutzers, die Nachrichten an den Benutzer senden, erhalten keine externe Abwesenheitsnachrichten Antwort.  <br/> |
|**Bezeichnet** <br/> |E-Mail-Absender außerhalb der Organisation des Postfachbenutzers, die Nachrichten an den Benutzer senden, erhalten nur dann eine externe Abwesenheitsnachrichten Antwort, wenn sich der Absender in der Exchange-Informationsspeicher Kontaktliste des Benutzers befindet.  <br/> |
|**All** <br/> |E-Mail-Absender außerhalb der Organisation des Postfachbenutzers, die Nachrichten an den Benutzer senden, erhalten eine externe Abwesenheitsnachrichten Antwort.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieses Element hat denselben Typ wie das [AllowExternalOof](allowexternaloof.md) -Element. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel einer SetUserOofSettings-Anforderung wird die OoFState auf " **aktiviert**" festgelegt, die externe Benutzergruppe auf " **all**" festgelegt, die Dauer von OOF auf 10 Tage festgelegt und die internen und externen Abwesenheitsnachrichten festgelegt.
  
```
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserOofSettings-Vorgang](getuseroofsettings-operation.md)
  
[SetUserOofSettings-Vorgang](setuseroofsettings-operation.md)

