---
title: ExternalAudience
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ExternalAudience
api_type:
- schema
ms.assetid: 79dc2a4c-f7dd-46d1-8f31-149116e1f76e
description: Das ExternalAudience-Element legt einen Wert fest oder enthält einen Wert, der bestimmt, an wen externe OOF-Nachrichten (Out of Office) gesendet werden.
ms.openlocfilehash: da318bfcf4a43d880b86379364c6e40aa9861f83
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545139"
---
# <a name="externalaudience"></a>ExternalAudience

Das **ExternalAudience-Element** legt einen Wert fest oder enthält einen Wert, der bestimmt, an wen externe OOF-Nachrichten (Out of Office) gesendet werden. 
  
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
|[UserOofSettings](useroofsettings.md) <br/> |Gibt die OOF-Einstellungen an.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[OofSettings](oofsettings.md) <br/> |Enthält die OOF-Einstellungen.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/GetUserOofSettingsResponse/OofSettings` <br/> |
   
## <a name="text-value"></a>Textwert

Für dieses Element ist ein Textwert erforderlich. In der folgenden Tabelle sind die möglichen Werte für dieses Element aufgeführt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|**Keine** <br/> |E-Mail-Absender außerhalb der Organisation des Postfachbenutzers, die Nachrichten an den Benutzer senden, erhalten keine externe OOF-Nachrichtenantwort.  <br/> |
|**Bekannt** <br/> |E-Mail-Absender außerhalb der Organisation des Postfachbenutzers, die Nachrichten an den Benutzer senden, erhalten nur dann eine externe OOF-Nachrichtenantwort, wenn sich der Absender in der Exchange Store-Kontaktliste des Benutzers befindet.  <br/> |
|**All** <br/> |E-Mail-Absender außerhalb der Organisation des Postfachbenutzers, die Nachrichten an den Benutzer senden, erhalten eine externe OOF-Nachrichtenantwort.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element hat den gleichen Typ wie das [AllowExternalOof-Element.](allowexternaloof.md) 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel einer SetUserOofSettings-Anforderung wird "OoFState" auf **"Aktiviert"** festgelegt, die externe Zielgruppe auf **"Alle"** festgelegt, die Dauer von OOF auf 10 Tage und die internen und externen OOF-Nachrichten festgelegt.
  
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

