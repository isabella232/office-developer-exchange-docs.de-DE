---
title: UserOofSettings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UserOofSettings
api_type:
- schema
ms.assetid: 0a95ca63-660e-4cc0-82e4-3f74fb4ae21c
description: Das UserOofSettings-Element gibt die OOF-Einstellungen (Out of Office) an.
ms.openlocfilehash: 0fa550a97464414570faf391d3633243ff2e2144
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513969"
---
# <a name="useroofsettings"></a>UserOofSettings

Das **UserOofSettings-Element** gibt die OOF-Einstellungen (Out of Office) an. 
  
[SetUserOofSettingsRequest](setuseroofsettingsrequest.md)
  
[UserOofSettings](useroofsettings.md)
  
```xml
<UserOofSettings>
   <OofState>...</OofState>
   <ExternalAudience>...</ExternalAudience>
   <Duration>...</Duration>
   <InternalReply>...</InternalReply>
   <ExternalReply>...</ExternalReply>
</UserOofSettings>
```

 **UserOofSettings**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[OofState](oofstate.md) <br/> |Legt den OOF-Status des Benutzers fest.  <br/> |
|[ExternalAudience](externalaudience.md) <br/> |Legt einen Wert fest, der bestimmt, an wen externe OOF-Nachrichten gesendet werden, oder enthält diesen Wert.  <br/> |
|[Dauer (UserOofSettings)](duration-useroofsettings.md) <br/> |Gibt die Dauer an, für die der OOF-Status aktiviert ist, wenn das [OofState-Element](oofstate.md) auf **Geplant** festgelegt ist. Wenn das [OofState-Element](oofstate.md) auf **"Enabled"** oder **"Disabled"** festgelegt ist, wird der Wert dieses Elements ignoriert.  <br/> |
|[InternalReply](internalreply.md) <br/> |Enthält die OOF-Antwort, die an andere Benutzer in der Domäne oder vertrauenswürdigen Domänen des Benutzers gesendet wird.  <br/> |
|[ExternalReply](externalreply.md) <br/> |Enthält die OOF-Antwort, die an Adressen außerhalb der Domäne oder der vertrauenswürdigen Domänen des Empfängers gesendet wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SetUserOofSettingsRequest](setuseroofsettingsrequest.md) <br/> |Enthält die Argumente, die zum Festlegen der OOF-Einstellungen und -Nachrichten eines Postfachbenutzers verwendet werden.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/SetUserOofSettingsRequest` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel einer SetUserOofSettings-Anforderung wird "OoFState" auf **"Enabled"** festgelegt, die Dauer von OOF für 10 Tage und die internen und externen OOF-Nachrichten festgelegt.
  
```xml
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
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [SetUserOofSettings-Vorgang](setuseroofsettings-operation.md)

