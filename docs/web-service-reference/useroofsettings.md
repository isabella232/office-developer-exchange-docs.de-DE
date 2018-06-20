---
title: "' UserOofSettings '"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserOofSettings
api_type:
- schema
ms.assetid: 0a95ca63-660e-4cc0-82e4-3f74fb4ae21c
description: Das Element ' UserOofSettings ' gibt die Out of Office (OOF).
ms.openlocfilehash: a035fd89387ece632d83f5f72a564e4896bc6753
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839457"
---
# <a name="useroofsettings"></a>' UserOofSettings '

Das Element **' UserOofSettings '** gibt die Out of Office (OOF). 
  
[SetUserOofSettingsRequest](setuseroofsettingsrequest.md)
  
[' UserOofSettings '](useroofsettings.md)
  
```xml
<UserOofSettings>
   <OofState>...</OofState>
   <ExternalAudience>...</ExternalAudience>
   <Duration>...</Duration>
   <InternalReply>...</InternalReply>
   <ExternalReply>...</ExternalReply>
</UserOofSettings>
```

 **' UserOofSettings '**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[OofState](oofstate.md) <br/> |Legt den Status des Benutzers OOF fest.  <br/> |
|[ExternalAudience](externalaudience.md) <br/> |Legt fest, oder enthält einen Wert, der bestimmt, denen externe OOF Testnachrichten gesendet werden.  <br/> |
|[Dauer (' UserOofSettings ')](duration-useroofsettings.md) <br/> |Gibt die Dauer, für die der Status ABWESEND aktiviert ist, wenn das Element [OofState](oofstate.md) **geplant**festgelegt ist. Wenn das Element [OofState](oofstate.md) auf **aktiviert** oder **deaktiviert**festgelegt ist, wird der Wert der dieses Element ignoriert.  <br/> |
|[InternalReply](internalreply.md) <br/> |Enthält die OOF Antwort an andere Benutzer in der Domäne oder der vertrauenswürdigen Domänen des Benutzers gesendet.  <br/> |
|[ExternalReply](externalreply.md) <br/> |Enthält die OOF Antwort an Adressen außerhalb der Domäne oder der vertrauenswürdigen Domänen des Empfängers gesendet.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SetUserOofSettingsRequest](setuseroofsettingsrequest.md) <br/> |Enthält die Argumente verwendet, um eines Postfachbenutzers OOF Einstellungen und Nachrichten festzulegen.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/SetUserOofSettingsRequest` <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird eine Anforderung SetUserOofSettings legt die OoFState auf **aktiviert**, wird die Dauer der OOF für 10 Tage, und die internen und externen Abwesenheitsnachrichten.
  
```xml
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
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichten-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [SetUserOofSettings-Vorgang](setuseroofsettings-operation.md)

